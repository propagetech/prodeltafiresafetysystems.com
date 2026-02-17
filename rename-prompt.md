You are a naming assistant. Given a list of file paths and minimal context from a static website, suggest a new filename (basename only, same extension) for each file. Rules:
- Lowercase, kebab-case, no spaces. SEO-friendly and human-readable.
- For HTML: use page purpose (e.g. about-us.html, contact.html). Keep index.html as index.html.
- For CSS/JS: use purpose (e.g. main-styles.css, analytics.js).
- For images: use content (e.g. logo-infygate.webp, hero-banner.webp). Use alt/title when provided.
- Return a JSON object: keys = exact original path strings, values = new basename only (e.g. "main.css"). Preserve extension.
- Do not change path prefix (e.g. css/ stays css/ by returning "name.css" not "css/name.css").

Files and context:
[
  {
    "path": "404.html",
    "context": {
      "title": "",
      "first_heading": "404"
    }
  },
  {
    "path": "css/559e64bf161e61fa0aca6e864c78191d.css",
    "context": {
      "path": "css/559e64bf161e61fa0aca6e864c78191d.css"
    }
  },
  {
    "path": "css/5e3a198b9f557dce8bcf744d800929a9.css",
    "context": {
      "path": "css/5e3a198b9f557dce8bcf744d800929a9.css"
    }
  },
  {
    "path": "css/84d4a0216f16f715d9b301db3a8da352.css",
    "context": {
      "path": "css/84d4a0216f16f715d9b301db3a8da352.css"
    }
  },
  {
    "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css",
    "context": {
      "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css"
    }
  },
  {
    "path": "css/c363a15baf9b3719c1570c22b012b369.css",
    "context": {
      "path": "css/c363a15baf9b3719c1570c22b012b369.css"
    }
  },
  {
    "path": "css/d09d646f062b67daeff66ff1410b63fc.css",
    "context": {
      "path": "css/d09d646f062b67daeff66ff1410b63fc.css"
    }
  },
  {
    "path": "css/internal-styles.css",
    "context": {
      "path": "css/internal-styles.css"
    }
  },
  {
    "path": "fire-detection-and-alarm.html",
    "context": {
      "title": "Pro Delta Fire Safety Systems | Products | Fire Alarm Systems",
      "first_heading": "Fire Alarm Systems"
    }
  },
  {
    "path": "fire-extinguisher-refilling-services.html",
    "context": {
      "title": "Pro Delta Fire Safety Systems | Products | Fire Extinguisher Refilling Services",
      "first_heading": "Fire Extinguisher Refilling Services"
    }
  },
  {
    "path": "fire-extinguishers.html",
    "context": {
      "title": "Pro Delta Fire Safety Systems | Products | Fire Extinguishers",
      "first_heading": "Fire Extinguishers"
    }
  },
  {
    "path": "fire-hydrant-systems.html",
    "context": {
      "title": "Pro Delta Fire Safety Systems | Products | Fire Hydrant Systems",
      "first_heading": "Fire Hydrant Systems"
    }
  },
  {
    "path": "fire-proof-doors.html",
    "context": {
      "title": "Pro Delta Fire Safety Systems | Products | Fire Proof Doors",
      "first_heading": "Fire Proof Doors"
    }
  },
  {
    "path": "fire-suppression-system.html",
    "context": {
      "title": "Pro Delta Fire Safety Systems | Products | Fire Suppression Systems",
      "first_heading": "Fire Suppression Systems"
    }
  },
  {
    "path": "imgs/0026ac50a63aa0d94e5caa2f2a0fe46f.gif",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/035a436551851c270c76db78282f7164.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/089e77bde6b061881ae392f0cd5d0e6c.webp",
    "context": {
      "refs": [
        {
          "alt": "Kitchen Fire Suppression Systems",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/09969d29d7bca1468b8280453ae66de9.webp",
    "context": {
      "refs": [
        {
          "alt": "DELTA FIRE ALARM SYSTEM",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/09b63c662f80d515ed328178588d6f21.webp",
    "context": {
      "refs": [
        {
          "alt": "logo1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/09e0acb36505ae7a5459773c7b069091.webp",
    "context": {
      "refs": [
        {
          "alt": "FM-200: The best people compatible, clean agent fire protection.",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0b69206acfe956cf85e86f1414d51844.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0bae859bc78609cb5d09040f021000e1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0c014124b6218399dc908ae10413c64b.webp",
    "context": {
      "refs": [
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0f8181168736ecde7e30513b3cfceda0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0fc5258b093607045847678aef1b036e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/107189e606054f4d072ce9211c352b9e.webp",
    "context": {
      "refs": [
        {
          "alt": "DCP (ABC) Stored Pressure Type Fire Extinguishers",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/10fb8552e3e9088d53e7876cb487fc38.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/112aa1aac1fd224db0132b2b65489883.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/11b2431f34d110caf439430c3d071af0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/14540c2dbc05ad02220e1e35c6386f9b.webp",
    "context": {
      "refs": [
        {
          "alt": "MSFIREDOOR",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/15296116bc80379311d19c874473befb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/154032f9f51a4f4dd8704729bb0f574b.webp",
    "context": {
      "refs": [
        {
          "alt": "logo1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1b2f2613431629fd41d5e0ced693483b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2043bbdd6b655e72b592fab2f1ef4671.webp",
    "context": {
      "refs": [
        {
          "alt": "Protect yourself from the risk of fire through DELTA\u00ae",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/23bac93de931f68c9211a18d6def7a9b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/23e7a4408d4a700b3002febc3ec78127.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/23f298409fc8ddbe67209ebe9db8552c.webp",
    "context": {
      "refs": [
        {
          "alt": "firefighters-115800_1280",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/245f4ca23ecdd86c35217f2f027bd1f5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/26e125559d15db42e857a2d3e454493e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2781d9a53a9ff6e832919a41ff27e27f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2929b8b9defe28e4823c912af74f5edd.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2a07f56a238022ef5c9fcac2a56b3cae.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2b1f7c3e6fd687315e9902a524008000.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2b49a7ca220fcf28cd5cd66b2e6bd1fa.webp",
    "context": {
      "refs": [
        {
          "alt": "Fire Extinguisher Refilling Services",
          "title": ""
        },
        {
          "alt": "Fire Extinguisher Refilling Services",
          "title": ""
        },
        {
          "alt": "Fire Extinguisher Refilling Services",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2d28f4e941535b894c267849adbaad33.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2da1c1ecda2e62625b44ebd84583f3ea.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2ea322370ff418f9f2bc087fd8e8ddf4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/321958668c2a31c9f02b49040de2c673.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3306746a29897fddc433e435109d74b6.webp",
    "context": {
      "refs": [
        {
          "alt": "firefighters-115800_1280",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/34404f7a0a81e9011a01cd34ffcbc339.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/35fdfab22e4702ff0c6c3e9729547885.webp",
    "context": {
      "refs": [
        {
          "alt": "firefighters-115800_1280",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/367e4b9ea4016745e89c6f4db5323240.webp",
    "context": {
      "refs": [
        {
          "alt": "Stored Pressure M. Foam Type Fire Extinguishers",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/38d840dfcaf528e9ef6b4a7e7e145a5f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3b44fb2ebda23e40a4533b83f30e8878.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3b88798f8a0bd07058f61ccaaee8d24d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3ce4dd6fd7aa29abebebfaf509bba264.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3e95de8b27b9771540bdd865fbe1fcbc.webp",
    "context": {
      "refs": [
        {
          "alt": "firefighters-115800_1280",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3f76b9b50a68c942dec56c911f7327ae.webp",
    "context": {
      "refs": [
        {
          "alt": "firefighters-115800_1280",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3fd06f7ab6145b1c35d4e0850865a52a.webp",
    "context": {
      "refs": [
        {
          "alt": "Fire Suppression System",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3ffbcea1e4a2a36405d4a97e452c275a.webp",
    "context": {
      "refs": [
        {
          "alt": "firefighters-115800_1280",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4202e4f9bc1f5fdef6d87126cd0085c7.webp",
    "context": {
      "refs": [
        {
          "alt": "firefighters-115800_1280",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/429ca9fbbf876866fefd7b99c11bb7a7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/43190c31c4a88327cf9e4fbc2561b156.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/45efcf5209cf4beabaa8397c863480ad.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/493b23e944c7c0c330a0a25c1f1bd09f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4b0e01c203afe8613e7ae0a18a78ab42.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4b288d406327b74f5e687cd060a5f091.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4b751f7fa0e8eb714223596d9b6e25d3.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4def0fd679124ba3b3831ec45ff89e86.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4ee95d9a6e8efc38d56284955ec27734.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4f54302b37bc5a1d3a6b9630d1940c53.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/519e6501e258114876fb40796c42dca8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5e3d7c52748c1277ecc07a8bdecb5d65.webp",
    "context": {
      "refs": [
        {
          "alt": "Stored Pressure Clean Agent Type Fire Extinguishers",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5eaddc54499ae1c6f7b5c0fda81a0308.webp",
    "context": {
      "refs": [
        {
          "alt": "Effluent Treatment Plants (ETP)",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5f27b2a2b9315c7fd64c4fd635a47335.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5f449c2e9462a7f91f5fea4cc719a167.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/680ecc368384933e3d1e84e439408bf2.webp",
    "context": {
      "refs": [
        {
          "alt": "MSFIREDOOR",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/685c69fd63885a2f1ef7da5dcc2b0504.webp",
    "context": {
      "refs": [
        {
          "alt": "MSFIREDOOR",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7219839156f5966f09e307d1fd46a78c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/744920850bbf8f4ee0325163498ad0ec.webp",
    "context": {
      "refs": [
        {
          "alt": "firefighters-115800_1280",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/74944ef0895551f5f342d2e26dbe2840.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/75971e9c1866b6c91316cfa7f1c3876d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7c27944711ae8966cbf98da23d614bb2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7d1a9895043be81e37b858706c2399fc.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7d7669ae1757276b4eaadfa8efeeed6a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7e04d47dbd2f0e70290784066ad5f95c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/803fdcb4b189491e217accd3e5abdbff.gif",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8090bdf538f53200b9aaf715257c3bcc.webp",
    "context": {
      "refs": [
        {
          "alt": "firefighters-115800_1280",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/849804925df79e7935218ebd9b89e471.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8552c376831aa5dfadda30df2fbefa97.webp",
    "context": {
      "refs": [
        {
          "alt": "CO2: A low cost, non-damaging, non-conductive, multi-hazard protectant.",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/86288ea256338ca424bf3ed47f1dfad6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8995226fa7fdeca9167fff0c21b4c060.webp",
    "context": {
      "refs": [
        {
          "alt": "firefighters-115800_1280",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8a93a777a2a0a4bc7a1111635f4c989b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8eadee0afc8f9be947a593b41286e720.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8f2de29ae767ab905efb4bf88e0b4ba8.webp",
    "context": {
      "refs": [
        {
          "alt": "firefighters-115800_1280",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8f3dbc13abd321bb67ac1d1094b57017.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/90d30ef868311b50023182cbf6863acf.webp",
    "context": {
      "refs": [
        {
          "alt": "Stored Pressure Water Type Fire Extinguishers",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/924c385e19766ee1a1ffd4032bf4a50b.webp",
    "context": {
      "refs": [
        {
          "alt": "firefighters-115800_1280",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/927fb3c9a34cb8f2bbdc24113d77091b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/92bc91e388af58b69a00b16e10a54e17.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9474b566fd72996970e720b375d124aa.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/961d56afe17e6a1d4572cad2fbe58f41.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/96be58be13f6a78932fbc399dcfd724a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/98b76ffa0ec92f121057e1138ae9cc1d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9a5d56fe7cf99def911b506a1bd3a76c.webp",
    "context": {
      "refs": [
        {
          "alt": "Carbon Dioxide Type Fire Extinguishers",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9a8ed86d0abc4696a6a687b786311aa1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9ae7fd7807f8b5727aa42b81467940ae.webp",
    "context": {
      "refs": [
        {
          "alt": "firefighters-115800_1280",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9e74238a877e1cc612d57fb34d7d5b97.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9fa3ec282eee6a0ab2fcb966673dcfa0.webp",
    "context": {
      "refs": [
        {
          "alt": "Fire Proof Doors",
          "title": ""
        },
        {
          "alt": "Wooden Fire Doors 2 hrs",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a1286869c5275c2a1ea789296ff6a2dc.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a27512c126f1ec076d07c4a6616608d3.gif",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a53d930ce351c641782a2f4cc311c078.webp",
    "context": {
      "refs": [
        {
          "alt": "Fire Extinguishers",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a603fd8036c746c410fedb55199a738a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a6776c27f98ee709864f4f5e6b84a71f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a67eb435391537b25ae664c56b606ffe.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a855188e971861ca205d9f001772ca54.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ab85f59c212727ff14628cd8f39629cb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "firefighters-115800_1280",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/abdb57c0905c39f85e4ea944e044bf82.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ae02fb3005814a57c94a0d64ba75629e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b0d8a52af9705875479716cc31092feb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b1a7672e9c40a7f762ba96427fef186d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b1cf9e24ba51a17f0dee699be4140a75.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b40145b7c8a4e0ab1d6ecaccbd8d9449.webp",
    "context": {
      "refs": [
        {
          "alt": "Fire Hydrant Systems",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b49b159143203b4e645c4dd170301d38.webp",
    "context": {
      "refs": [
        {
          "alt": "Sewage Treatment Plants (STP)",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b70c2451d0f8085f84c3c596de2ef9b1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bf99e258e154e69ca2d21c0a13137d0e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c19d150266a115c11617093dc5a125c2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c20b2b6ad52cb0c672e17605128ece6e.gif",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c69eebdd5c9793986a9db0405b3faca0.webp",
    "context": {
      "refs": [
        {
          "alt": "firefighters-115800_1280",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ca8ad123e117bd98c292088def70ba4e.webp",
    "context": {
      "refs": [
        {
          "alt": "logo1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/caa95dccc1617d3e0e217d2e7dddd60f.webp",
    "context": {
      "refs": [
        {
          "alt": "firefighters-115800_1280",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cab4c54fc08841a00045fc6d67666618.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cab926cf5309770046edf7e70abf23f1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cbf8e727a0d3e93b75af0396c49cad2d.webp",
    "context": {
      "refs": [
        {
          "alt": "firefighters-115800_1280",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cd828ab584870b7b1aeb6386340e2511.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ce7b351e1c973a6edb742fcaf695ad0d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d0716526e8c1fc5cd2caecde4d66c792.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d0812aba8db21f85c7b044fb6ed4e408.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d1ca0d8e2c23c9f4ff315412dc7eec83.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d87ab1a0a18a86ade5d7bd2e07fb874d.webp",
    "context": {
      "refs": [
        {
          "alt": "Fire Detection & Fire Alarm Systems",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/da3e235b188fe3d30ecb06f538391220.webp",
    "context": {
      "refs": [
        {
          "alt": "firefighters-115800_1280",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/da75570e459aa07b9ade0aa3a7ad07c3.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/db8f6e439a3a144a166d9ceaefe7f974.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/dd5516c2e2481574478f8d782a87de2f.webp",
    "context": {
      "refs": [
        {
          "alt": "logo1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/de44a41091e2b12a243e2904c2e6bafc.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e05b9b3535a90095e9d4eefc7685b871.webp",
    "context": {
      "refs": [
        {
          "alt": "Raw Water Clarification",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e31cf585c63f84b94deec239c14d74ae.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/e5c062c53063a32c398c95d375fc1b77.webp",
    "context": {
      "refs": [
        {
          "alt": "firefighters-115800_1280",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e7adddb96f93ab12e1ee0307339bed8f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e8ba02558534f36494d95b2dbca97436.webp",
    "context": {
      "refs": [
        {
          "alt": "firefighters-115800_1280",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ea19ca50061b0e9dba538f15c2e19bdf.gif",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ec22013728a78a66eb1084c1678d2fd9.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ecbc7cdb64cd86155205558e21f2dcec.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/efcc7594983be5b87729a5b4ba88601f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f56a1863eb023b7b6a8d3dc5d8b10522.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f5dca8dfc0a36d50874d8d7bffaeab83.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f7c4fa8b3b0fe92b772ff8e673edb57e.webp",
    "context": {
      "refs": [
        {
          "alt": "solaronaflatroof",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fbfd817dfac7542cac20141b43e12cd6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fc3a7bc5e3b0bdcb60086265f6afc5aa.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ff310b42915487bae1c96c2fc48a03f7.gif",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "index.html",
    "context": {
      "title": "Pro Delta Fire Safety Systems Pvt Ltd",
      "first_heading": "Welcome to Pro Delta Fire Safety Systems Private Limited"
    }
  },
  {
    "path": "js/03b2eaae6007054a68c38e495f894dba.js",
    "context": {
      "path": "js/03b2eaae6007054a68c38e495f894dba.js"
    }
  },
  {
    "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js",
    "context": {
      "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js"
    }
  },
  {
    "path": "js/0c46896987137b0016246f6bc2243099.js",
    "context": {
      "path": "js/0c46896987137b0016246f6bc2243099.js"
    }
  },
  {
    "path": "js/165d7b0ddfa33362140feea997351b77.js",
    "context": {
      "path": "js/165d7b0ddfa33362140feea997351b77.js"
    }
  },
  {
    "path": "js/16df9ef05001a1741857bf99f5a5738f.js",
    "context": {
      "path": "js/16df9ef05001a1741857bf99f5a5738f.js"
    }
  },
  {
    "path": "js/2a85c11e395a8380b5915443e926b569.js",
    "context": {
      "path": "js/2a85c11e395a8380b5915443e926b569.js"
    }
  },
  {
    "path": "js/34be5330971fdbd18985525bd994b0aa.js",
    "context": {
      "path": "js/34be5330971fdbd18985525bd994b0aa.js"
    }
  },
  {
    "path": "js/35c5f9e096d4da33d2a62031daf14248.js",
    "context": {
      "path": "js/35c5f9e096d4da33d2a62031daf14248.js"
    }
  },
  {
    "path": "js/3d70953a848219e749fedc2cdb906675.js",
    "context": {
      "path": "js/3d70953a848219e749fedc2cdb906675.js"
    }
  },
  {
    "path": "js/3e940a33e44b65c1c0af8bb80a893530.js",
    "context": {
      "path": "js/3e940a33e44b65c1c0af8bb80a893530.js"
    }
  },
  {
    "path": "js/544d012df7acf9c3f0920f67c9e322b9.js",
    "context": {
      "path": "js/544d012df7acf9c3f0920f67c9e322b9.js"
    }
  },
  {
    "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js",
    "context": {
      "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js"
    }
  },
  {
    "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js",
    "context": {
      "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js"
    }
  },
  {
    "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js",
    "context": {
      "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js"
    }
  },
  {
    "path": "js/7260bab328b0ad74815a5efb377bcc67.js",
    "context": {
      "path": "js/7260bab328b0ad74815a5efb377bcc67.js"
    }
  },
  {
    "path": "js/893de96f1b6da546bd7c814964723eca.js",
    "context": {
      "path": "js/893de96f1b6da546bd7c814964723eca.js"
    }
  },
  {
    "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js",
    "context": {
      "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js"
    }
  },
  {
    "path": "js/9455859483e31e4da0e28f10d0742c2a.js",
    "context": {
      "path": "js/9455859483e31e4da0e28f10d0742c2a.js"
    }
  },
  {
    "path": "js/9db10375d298678e53777a2347b87073.js",
    "context": {
      "path": "js/9db10375d298678e53777a2347b87073.js"
    }
  },
  {
    "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js",
    "context": {
      "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js"
    }
  },
  {
    "path": "js/a2261649751fa61b606222c9b2ea3b80.js",
    "context": {
      "path": "js/a2261649751fa61b606222c9b2ea3b80.js"
    }
  },
  {
    "path": "js/b0bade6d42c2702ca85774296cc507c4.js",
    "context": {
      "path": "js/b0bade6d42c2702ca85774296cc507c4.js"
    }
  },
  {
    "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js",
    "context": {
      "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js"
    }
  },
  {
    "path": "js/cecb447a04bbe3e8982190dd6e697120.js",
    "context": {
      "path": "js/cecb447a04bbe3e8982190dd6e697120.js"
    }
  },
  {
    "path": "js/d80b370d82680fc786dcc943a327b9f2.js",
    "context": {
      "path": "js/d80b370d82680fc786dcc943a327b9f2.js"
    }
  },
  {
    "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js",
    "context": {
      "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js"
    }
  },
  {
    "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js",
    "context": {
      "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js"
    }
  },
  {
    "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js",
    "context": {
      "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js"
    }
  },
  {
    "path": "solar-photovoltaic-system.html",
    "context": {
      "title": "Pro Delta Fire Safety Systems | Products | Solar Photovoltatic System",
      "first_heading": "Solar Photovoltatic System"
    }
  },
  {
    "path": "wastewater-treatment.html",
    "context": {
      "title": "Pro Delta Fire Safety Systems | Products | Wastewater Treatment",
      "first_heading": "Wastewater Treatment"
    }
  }
]

Return only a JSON object mapping each path to its new basename (same extension). No other text.