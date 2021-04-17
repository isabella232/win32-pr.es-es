---
title: Macros para valores y colores CMYK
description: Las siguientes macros son útiles para manipular valores CMYK.
ms.assetid: e5d107fb-e010-400b-9ec5-90c2c0381dbe
keywords:
- Sistema de color de Windows (WCS), macros CMYK
- WCS (sistema de colores de Windows), macros CMYK
- Administración del color de imagen, macros CMYK
- Administración del color, macros CMYK
- colores, macros CMYK
- Referencia WCS, macros CMYK
- referencia de las macros WCS, CMYK
- CMYK (macros)
- Aguamarina fucsia amarillo negro (CMYK)
- CMYK (aguamarina fucsia amarillo negro)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a0efcbb6b0dc25f8f93f420113cc8c0797cba46
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/26/2021
ms.locfileid: "105721150"
---
# <a name="macros-for-cmyk-values-and-colors"></a>Macros para valores y colores CMYK

Las siguientes macros son útiles para manipular valores CMYK.



| Macro                          | Descripción                                                                  |
|--------------------------------|------------------------------------------------------------------------------|
| [**CMYK**](/windows/desktop/api/Wingdi/nf-wingdi-cmyk)           | Crea un valor CMYK a partir de los valores individuales de cian, magenta, amarillo y negro. |
| [**GetCValue**](/windows/desktop/api/Wingdi/nf-wingdi-getcvalue) | Recupera el valor de color aguamarina de un valor de color CMYK.                      |
| [**GetKValue**](/windows/desktop/api/Wingdi/nf-wingdi-getkvalue) | Recupera el valor de color negro de un valor de color CMYK.                     |
| [**GetMValue**](/windows/desktop/api/Wingdi/nf-wingdi-getmvalue) | Recupera el valor magenta de un valor de color CMYK.                         |
| [**GetYValue**](/windows/desktop/api/Wingdi/nf-wingdi-getyvalue) | Recupera el valor de color amarillo de un valor de color CMYK.                    |



 

Las macros siguientes se utilizan con el color.



| Macro                                | Descripción                                                                                                                                           |
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetBValue**](/windows/win32/api/wingdi/nf-wingdi-getbvalue)       | Obtiene un valor de color azul RGB.                                                                                                                               |
| [**GetGValue**](/windows/win32/api/wingdi/nf-wingdi-getgvalue)       | Obtiene un valor de color verde RGB.                                                                                                                              |
| [**GetRValue**](/windows/win32/api/wingdi/nf-wingdi-getrvalue)       | Obtiene un valor rojo RGB.                                                                                                                                |
| [**PALETTEINDEX**](/previous-versions//dd162770(v=vs.85)) | Acepta un índice para una entrada de la paleta de colores lógicos y devuelve un especificador de entrada de paleta.                                                              |
| [**PALETTERGB**](/windows/win32/api/wingdi/nf-wingdi-palettergb)     | Acepta tres valores que representan las intensidades relativas de rojo, verde y azul, y devuelve un especificador rojo, verde, azul (RGB) relativo a la paleta. |
| [RGB](/windows/win32/api/wingdi/nf-wingdi-rgb)                       | Selecciona un color rojo, verde y azul (RGB) en función de los argumentos proporcionados y las capacidades de color del dispositivo de salida.                               |



 

 

 