---
description: Los subtipos siguientes definen formatos RGB sin comprimir sin canal alfa.
ms.assetid: 49c91c8c-6889-48c6-8fa5-84929c03d951
title: Subtipos de vídeo RGB sin comprimir (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8fc35faaa5b6a58a597bf8d563ded4a920b0a112f61a4858f32c1b61fa29966
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130985"
---
# <a name="uncompressed-rgb-video-subtypes"></a>Subtipos de vídeo RGB sin comprimir

Los subtipos siguientes definen formatos RGB sin comprimir sin canal alfa.



| Constante                                                                                                                                                                        | Descripción                                       |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------|
| <span id="MEDIASUBTYPE_RGB1"></span><span id="mediasubtype_rgb1"></span><dl> <dt>**MEDIASUBTYPE \_ RGB1**</dt> </dl>       | RGB, 1 bit por píxel (bpp), con efectos<br/> |
| <span id="MEDIASUBTYPE_RGB4"></span><span id="mediasubtype_rgb4"></span><dl> <dt>**MEDIASUBTYPE \_ RGB4**</dt> </dl>       | RGB, 4 bpp, desenlazado<br/>                 |
| <span id="MEDIASUBTYPE_RGB8"></span><span id="mediasubtype_rgb8"></span><dl> <dt>**MEDIASUBTYPE \_ RGB8**</dt> </dl>       | RGB, 8 bpp, coloreteado<br/>                 |
| <span id="MEDIASUBTYPE_RGB555"></span><span id="mediasubtype_rgb555"></span><dl> <dt>**MEDIASUBTYPE \_ RGB555**</dt> </dl> | RGB 555, 16 bpp<br/>                        |
| <span id="MEDIASUBTYPE_RGB565"></span><span id="mediasubtype_rgb565"></span><dl> <dt>**MEDIASUBTYPE \_ RGB565**</dt> </dl> | RGB 565, 16 bpp<br/>                        |
| <span id="MEDIASUBTYPE_RGB24"></span><span id="mediasubtype_rgb24"></span><dl> <dt>**MEDIASUBTYPE \_ RGB24**</dt> </dl>    | RGB, 24 bpp<br/>                            |
| <span id="MEDIASUBTYPE_RGB32"></span><span id="mediasubtype_rgb32"></span><dl> <dt>**MEDIASUBTYPE \_ RGB32**</dt> </dl>    | RGB, 32 bpp<br/>                            |



Los subtipos siguientes definen formatos RGB sin comprimir con canal alfa.



| Constante                                                                                                                                                                                       | Descripción                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| <span id="MEDIASUBTYPE_ARGB1555"></span><span id="mediasubtype_argb1555"></span><dl> <dt>**MEDIASUBTYPE \_ ARGB1555**</dt> </dl>          | RGB 555 con canal alfa<br/>                                                    |
| <span id="MEDIASUBTYPE_ARGB32"></span><span id="mediasubtype_argb32"></span><dl> <dt>**MEDIASUBTYPE \_ ARGB32**</dt> </dl>                | RGB 32 con canal alfa<br/>                                                     |
| <span id="MEDIASUBTYPE_ARGB4444"></span><span id="mediasubtype_argb4444"></span><dl> <dt>**MEDIASUBTYPE \_ ARGB4444**</dt> </dl>          | RGB de 16 bits con canal alfa; 4 bits por canal<br/>                             |
| <span id="MEDIASUBTYPE_A2R10G10B10"></span><span id="mediasubtype_a2r10g10b10"></span><dl> <dt>**MEDIASUBTYPE \_ A2R10G10B10**</dt> </dl> | RGB de 32 bits con canal alfa; 10 bits por canal RGB más 2 bits para alfa.<br/> |
| <span id="MEDIASUBTYPE_A2B10G10R10"></span><span id="mediasubtype_a2b10g10r10"></span><dl> <dt>**MEDIASUBTYPE \_ A2B10G10R10**</dt> </dl> | BGR de 32 bits con canal alfa; 10 bits por canal BGR más 2 bits para alfa.<br/> |



## <a name="remarks"></a>Comentarios

En el caso de los formatos de color, el color de cada píxel se especifica como un índice en una paleta. La paleta debe incluirse en el bloque de formato, siguiendo la [**estructura BITMAPINFOHEADER.**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) En el caso de los formatos no tachados, el color de cada píxel se especifica directamente; el diseño de memoria depende de la profundidad de bits:

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

    

-   Para RGB 24, cada píxel es [**un RGBTRIPLE.**](/windows/win32/api/wingdi/ns-wingdi-rgbtriple) Cada color es de un byte, con un valor de 0 a 255, ambos incluidos. El diseño de memoria es:

    |       | Layout     | Layout      | Layout     |
    |-------|------|-------|-----|
    | **Byte**  | 0    | 1     | 2   |
    | **Valor** | Azul | Verde | Rojo |

    

     

-   Para RGB 32, cada píxel es **un RGBQUAD**. Cada color es de un byte, con un valor de 0 a 255, ambos incluidos. El diseño de memoria es: 

    |       | Layout     | Layout      | Layout     | Layout |
    |-------|------|-------|-----|---------------------|
    | **Byte**  | 0    | 1     | 2   | 3                   |
    | **Valor** | Azul | Verde | Rojo | Alfa o No le importa |

    

     

    Si el subtipo es MEDIASUBTYPE \_ ARGB32, el byte 3 contiene un valor para el canal alfa. Si el subtipo es MEDIASUBTYPE RGB32, se debe omitir el \_ byte 3.

-   A2R10G10B10 usa el diseño siguiente: 

    |       | Layout     | Layout      | Layout     | Layout |
    |-------|-------|---------|---------|---------|
    | **Poco**   | 0 - 9 | 10 - 19 | 20 - 29 | 30 - 31 |
    | **Valor** | Azul  | Verde   | Rojo     | Alpha   |

    

     

-   A2B10G10R10 usa el diseño siguiente: 

    |       | Layout     | Layout      | Layout     | Layout |
    |-------|-------|---------|---------|---------|
    | **Poco**   | 0 - 9 | 10 - 19 | 20 - 29 | 30 - 31 |
    | **Valor** | Rojo   | Verde   | Azul    | Alpha   |

    

     

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Subtipos de vídeo](video-subtypes.md)
</dt> <dt>

[Trabajar con fotogramas de vídeo](working-with-video-frames.md)
</dt> </dl>

 

 
