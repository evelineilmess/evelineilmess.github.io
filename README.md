import React from "react";
import { FooterSection } from "./FooterSection";
import { HeroSection } from "./HeroSection";
import { ProjectsSection } from "./ProjectsSection";

export const HomeDarkMode = (): JSX.Element => {
  const navigationItems = [
    { label: "Home", active: true },
    { label: "Projects", active: false },
    { label: "About", active: false },
    { label: "Contact", active: false },
  ];

  return (
    <div className="bg-blackblack-900 w-full min-w-[1440px] min-h-[5297px] flex flex-col">
      <nav className="inline-flex h-14 w-[456px] self-center relative mt-[104px] items-center justify-center gap-4 px-[5px] py-0 bg-blackblack-400 rounded-[80px] shadow-navigation">
        {navigationItems.map((item, index) => (
          <a
            key={index}
            href={`#${item.label.toLowerCase()}`}
            className={`inline-flex h-[46px] items-center justify-center gap-1 p-4 relative flex-[0_0_auto] rounded-[48px] ${
              item.active ? "bg-whitewhite-500" : ""
            }`}
          >
            <span
              className={`relative w-fit mt-[-8.00px] mb-[-6.00px] [font-family:'Work_Sans-Regular',Helvetica] font-normal text-xl tracking-[-0.20px] leading-[28.0px] whitespace-nowrap ${
                item.active ? "text-blackblack-500" : "text-greygrey-500"
              }`}
            >
              {item.label}
            </span>
          </a>
        ))}
      </nav>

      <h1 className="ml-px h-[311px] w-[1217px] self-center mt-[100px] [font-family:'Berghan-Regular',Helvetica] font-normal text-whitewhite-500 text-[140px] tracking-[0] leading-[140px]">
        Graphic &amp;
        <br />
        Product Design
      </h1>

      <ProjectsSection />

      <div className="flex ml-28 w-[1217px] h-[58px] relative mt-[100px] items-end gap-[754px]">
        <div className="items-start gap-[11px] inline-flex flex-col relative flex-[0_0_auto]">
          <h2 className="relative w-fit mt-[-1.00px] font-heading-h2 font-[number:var(--heading-h2-font-weight)] text-whitewhite-500 text-[length:var(--heading-h2-font-size)] tracking-[var(--heading-h2-letter-spacing)] leading-[var(--heading-h2-line-height)] whitespace-nowrap [font-style:var(--heading-h2-font-style)]">
            Projects
          </h2>
        </div>
      </div>

      <HeroSection />
      <FooterSection />
    </div>
  );
};
