---
description: Las siguientes constantes, definidas en Gdipluspixelformats.h, especifican varios formatos de píxel usados en mapas de bits.
ms.assetid: 362204c5-5dd7-461a-b90b-15826c025689
title: Constantes de formato de píxel de imagen (Gdipluspixelformats.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b62abc8b0ed606b958764e27171f8b45e619d23b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170265"
---
# <a name="image-pixel-format-constants"></a>Constantes de formato de píxel de imagen

Las siguientes constantes, definidas en Gdipluspixelformats.h, especifican varios formatos de píxel usados en mapas de bits.



| Constante                                                                                                                                                                                                                                     | Descripción                                                                                                                                                                                                               |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PixelFormat1bppIndexed"></span><span id="pixelformat1bppindexed"></span><span id="PIXELFORMAT1BPPINDEXED"></span><dl> <dt>**PixelFormat1bppIndexed**</dt> </dl>             | Especifica que el formato es de 1 bit por píxel, indexado.<br/>                                                                                                                                                         |
| <span id="PixelFormat4bppIndexed"></span><span id="pixelformat4bppindexed"></span><span id="PIXELFORMAT4BPPINDEXED"></span><dl> <dt>**PixelFormat4bppIndexed**</dt> </dl>             | Especifica que el formato es de 4 bits por píxel, indizado.<br/>                                                                                                                                                        |
| <span id="PixelFormat8bppIndexed"></span><span id="pixelformat8bppindexed"></span><span id="PIXELFORMAT8BPPINDEXED"></span><dl> <dt>**PixelFormat8bppIndexed**</dt> </dl>             | Especifica que el formato es de 8 bits por píxel, indexado.<br/>                                                                                                                                                        |
| <span id="PixelFormat16bppARGB1555"></span><span id="pixelformat16bppargb1555"></span><span id="PIXELFORMAT16BPPARGB1555"></span><dl> <dt>**PixelFormat16bppARGB1555**</dt> </dl>     | Especifica que el formato es de 16 bits por píxel; Se usa 1 bit para el componente alfa y 5 bits para los componentes rojo, verde y azul.<br/>                                                       |
| <span id="PixelFormat16bppGrayScale"></span><span id="pixelformat16bppgrayscale"></span><span id="PIXELFORMAT16BPPGRAYSCALE"></span><dl> <dt>**PixelFormat16bppGrayScale**</dt> </dl> | Especifica que el formato es de 16 bits por píxel, escala de grises.<br/>                                                                                                                                                     |
| <span id="PixelFormat16bppRGB555"></span><span id="pixelformat16bpprgb555"></span><span id="PIXELFORMAT16BPPRGB555"></span><dl> <dt>**PixelFormat16bppRGB555**</dt> </dl>             | Especifica que el formato es de 16 bits por píxel, de los cuales se utilizan 5 bits para cada uno de los componentes rojo, verde y azul. El bit restante no se utiliza.<br/>                                                                   |
| <span id="PixelFormat16bppRGB565"></span><span id="pixelformat16bpprgb565"></span><span id="PIXELFORMAT16BPPRGB565"></span><dl> <dt>**PixelFormat16bppRGB565**</dt> </dl>             | Especifica que el formato es de 16 bits por píxel; 5 bits se utilizan para el componente rojo, 6 bits para el componente verde y 5 bits para el componente azul.<br/>                                    |
| <span id="PixelFormat24bppRGB"></span><span id="pixelformat24bpprgb"></span><span id="PIXELFORMAT24BPPRGB"></span><dl> <dt>**PixelFormat24bppRGB**</dt> </dl>                         | Especifica que el formato es de 24 bits por píxel, de los cuales se usan 8 bits para cada uno de los componentes rojo, verde y azul.<br/>                                                                                                  |
| <span id="PixelFormat32bppARGB"></span><span id="pixelformat32bppargb"></span><span id="PIXELFORMAT32BPPARGB"></span><dl> <dt>**PixelFormat32bppARGB**</dt> </dl>                     | Especifica que el formato es de 32 bits por píxel, de los cuales se utilizan 8 bits para los componentes alfa, rojo, verde y azul.<br/>                                                                                           |
| <span id="PixelFormat32bppPARGB"></span><span id="pixelformat32bpppargb"></span><span id="PIXELFORMAT32BPPPARGB"></span><dl> <dt>**PixelFormat32bppPARGB**</dt> </dl>                 | Especifica que el formato es de 32 bits por píxel, de los cuales se utilizan 8 bits para los componentes alfa, rojo, verde y azul. Los componentes rojo, verde y azul se multiplican previamente según el componente alfa.<br/>   |
| <span id="PixelFormat32bppRGB"></span><span id="pixelformat32bpprgb"></span><span id="PIXELFORMAT32BPPRGB"></span><dl> <dt>**PixelFormat32bppRGB**</dt> </dl>                         | Especifica que el formato es de 32 bits por píxel, de los cuales se usan 8 bits para cada uno de los componentes rojo, verde y azul. Los 8 bits restantes no se utilizan.<br/>                                                               |
| <span id="PixelFormat48bppRGB"></span><span id="pixelformat48bpprgb"></span><span id="PIXELFORMAT48BPPRGB"></span><dl> <dt>**PixelFormat48bppRGB**</dt> </dl>                         | Especifica que el formato es de 48 bits por píxel, de los cuales se usan 16 bits para cada uno de los componentes rojo, verde y azul.<br/>                                                                                                 |
| <span id="PixelFormat64bppARGB"></span><span id="pixelformat64bppargb"></span><span id="PIXELFORMAT64BPPARGB"></span><dl> <dt>**PixelFormat64bppARGB**</dt> </dl>                     | Especifica que el formato es de 64 bits por píxel, de los cuales se usan 16 bits para los componentes alfa, rojo, verde y azul.<br/>                                                                                          |
| <span id="PixelFormat64bppPARGB"></span><span id="pixelformat64bpppargb"></span><span id="PIXELFORMAT64BPPPARGB"></span><dl> <dt>**PixelFormat64bppPARGB**</dt> </dl>                 | Especifica que el formato es de 64 bits por píxel, de los cuales se usan 16 bits para los componentes alfa, rojo, verde y azul. Los componentes rojo, verde y azul se multiplican previamente según el componente alfa. <br/> |



## <a name="remarks"></a>Observaciones

**PixelFormat48bppRGB,** **PixelFormat64bppARGB** y **PixelFormat64bppPARGB** usan 16 bits por componente de color (canal). Windows GDI+ versión 1.0 puede leer imágenes de 16 bits por canal, pero dichas imágenes se convierten a un formato de 8 bits por canal para procesar, mostrar y guardar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Gdipluspixelformats.h</dt> </dl> |



 

 




