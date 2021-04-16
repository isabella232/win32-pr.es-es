---
description: Los siguientes subtipos definen formatos RGB sin comprimir sin canal alfa.
ms.assetid: 49c91c8c-6889-48c6-8fa5-84929c03d951
title: Subtipos de vídeo RGB sin comprimir (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e04237a61fa91f4fe648dcb7743c893604adbe7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671432"
---
# <a name="uncompressed-rgb-video-subtypes"></a>Subtipos de vídeo RGB sin comprimir

Los siguientes subtipos definen formatos RGB sin comprimir sin canal alfa.



| Constante                                                                                                                                                                        | Descripción                                       |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------|
| <span id="MEDIASUBTYPE_RGB1"></span><span id="mediasubtype_rgb1"></span><dl> <dt>**MEDIASUBTYPE \_ RGB1**</dt> </dl>       | RGB, 1 bit por píxel (BPP), con paleta<br/> |
| <span id="MEDIASUBTYPE_RGB4"></span><span id="mediasubtype_rgb4"></span><dl> <dt>**MEDIASUBTYPE \_ RGB4**</dt> </dl>       | RGB, 4 BPP, con paleta<br/>                 |
| <span id="MEDIASUBTYPE_RGB8"></span><span id="mediasubtype_rgb8"></span><dl> <dt>**MEDIASUBTYPE \_ RGB8**</dt> </dl>       | RGB, 8 BPP, con paleta<br/>                 |
| <span id="MEDIASUBTYPE_RGB555"></span><span id="mediasubtype_rgb555"></span><dl> <dt>**MEDIASUBTYPE \_ RGB555**</dt> </dl> | RGB 555, 16 BPP<br/>                        |
| <span id="MEDIASUBTYPE_RGB565"></span><span id="mediasubtype_rgb565"></span><dl> <dt>**MEDIASUBTYPE \_ RGB565**</dt> </dl> | RGB 565, 16 BPP<br/>                        |
| <span id="MEDIASUBTYPE_RGB24"></span><span id="mediasubtype_rgb24"></span><dl> <dt>**MEDIASUBTYPE \_ RGB24**</dt> </dl>    | RGB, 24 BPP<br/>                            |
| <span id="MEDIASUBTYPE_RGB32"></span><span id="mediasubtype_rgb32"></span><dl> <dt>**MEDIASUBTYPE \_ RGB32**</dt> </dl>    | RGB, 32 bpp<br/>                            |



Los siguientes subtipos definen formatos RGB sin comprimir con canal alfa.



| Constante                                                                                                                                                                                       | Descripción                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| <span id="MEDIASUBTYPE_ARGB1555"></span><span id="mediasubtype_argb1555"></span><dl> <dt>**MEDIASUBTYPE \_ ARGB1555**</dt> </dl>          | RGB 555 con canal alfa<br/>                                                    |
| <span id="MEDIASUBTYPE_ARGB32"></span><span id="mediasubtype_argb32"></span><dl> <dt>**MEDIASUBTYPE \_ ARGB32**</dt> </dl>                | RGB 32 con canal alfa<br/>                                                     |
| <span id="MEDIASUBTYPE_ARGB4444"></span><span id="mediasubtype_argb4444"></span><dl> <dt>**MEDIASUBTYPE \_ ARGB4444**</dt> </dl>          | RGB de 16 bits con canal alfa; 4 bits por canal<br/>                             |
| <span id="MEDIASUBTYPE_A2R10G10B10"></span><span id="mediasubtype_a2r10g10b10"></span><dl> <dt>**MEDIASUBTYPE \_ A2R10G10B10**</dt> </dl> | RGB de 32 bits con canal alfa; 10 bits por canal RGB más 2 bits para alpha.<br/> |
| <span id="MEDIASUBTYPE_A2B10G10R10"></span><span id="mediasubtype_a2b10g10r10"></span><dl> <dt>**MEDIASUBTYPE \_ A2B10G10R10**</dt> </dl> | BGR de 32 bits con canal alfa; 10 bits por canal de BGR más 2 bits para alpha.<br/> |



## <a name="remarks"></a>Observaciones

En el caso de los formatos de paleta, el color de cada píxel se especifica como un índice en una paleta. La paleta debe estar incluida en el bloque de formato, siguiendo la estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) . En el caso de los formatos no de paleta, el color de cada píxel se especifica directamente; el diseño de memoria depende de la profundidad de bits:

-   RGB 555 usa el siguiente diseño de memoria:
    ```C++
    High-order byte:    Low-order byte: 
    X R R R R R G G     G G G B B B B B 

    X = Don't care, R = Red, G = Green, B = Blue
    ```

    

-   RGB 565 usa el siguiente diseño de memoria:
    ```C++
    High-order byte:    Low-order byte: 
    R R R R R G G G     G G G B B B B B 
    ```

    

-   En el caso de RGB 24, cada píxel es un [**RGBTRIPLE**](/windows/win32/api/wingdi/ns-wingdi-rgbtriple). Cada color es un byte, con un valor de 0 a 255, ambos incluidos. El diseño de memoria es: 

    |       |      |       |     |
    |-------|------|-------|-----|
    | Byte  | 0    | 1     | 2   |
    | Value | Azul | Verde | Rojo |

    

     

-   En el caso de RGB 32, cada píxel es un **RGBQUAD**. Cada color es un byte, con un valor de 0 a 255, ambos incluidos. El diseño de memoria es: 

    |       |      |       |     |                     |
    |-------|------|-------|-----|---------------------|
    | Byte  | 0    | 1     | 2   | 3                   |
    | Value | Azul | Verde | Rojo | Alfa o no tiene cuidado |

    

     

    Si el subtipo es MEDIASUBTYPE \_ ARGB32, el byte 3 contiene un valor para el canal alfa. Si el subtipo es MEDIASUBTYPE \_ RGB32, se debe omitir el byte 3.

-   A2R10G10B10 usa el siguiente diseño: 

    |       |       |         |         |         |
    |-------|-------|---------|---------|---------|
    | bit   | 0 - 9 | 10 - 19 | 20 - 29 | 30 - 31 |
    | Value | Azul  | Verde   | Rojo     | Alpha   |

    

     

-   A2B10G10R10 usa el siguiente diseño: 

    |       |       |         |         |         |
    |-------|-------|---------|---------|---------|
    | bit   | 0 - 9 | 10 - 19 | 20 - 29 | 30 - 31 |
    | Value | Rojo   | Verde   | Azul    | Alpha   |

    

     

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Subtipos de vídeo](video-subtypes.md)
</dt> <dt>

[Trabajar con fotogramas de vídeo](working-with-video-frames.md)
</dt> </dl>

 

 
