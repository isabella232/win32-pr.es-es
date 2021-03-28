---
description: El suavizado de contorno de ClearType de Microsoft es un método de suavizado que mejora la resolución de la presentación de fuentes sobre el suavizado de contorno tradicional.
ms.assetid: b9896934-1e4f-4ae1-922a-ef30e0edf94f
title: Suavizado de contorno de ClearType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffbe7ae1a6c99fcee826c576b7671aea6e9ce6c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985047"
---
# <a name="cleartype-antialiasing"></a>Suavizado de contorno de ClearType

El suavizado de contorno de ClearType de Microsoft es un método de suavizado que mejora la resolución de la presentación de fuentes sobre el suavizado de contorno tradicional. Mejora drásticamente la legibilidad en monitores LCD de color con una interfaz digital, como los equipos portátiles y las pantallas de escritorio plano de alta calidad. La legibilidad en pantallas de CRT también se ha mejorado en cierto modo.

Sin embargo, ClearType depende de la orientación y el orden de las franjas LCD. Actualmente, ClearType solo se implementa para los monitores de LCD con bandas verticales que se ordenan por RGB. En concreto, esto afecta a los Tablet PC, donde la pantalla se puede orientar en cualquier dirección y a las pantallas que se pueden convertir de horizontal a vertical.

Se permite el suavizado de contorno de ClearType:

-   Para el color de 16, 24 y 32 bits (deshabilitado para 256 colores o menos)
-   Para DC de pantalla y DC de memoria (no para el DC de impresora)
-   Para fuentes TrueType y fuentes OpenType con esquemas TrueType

El suavizado de contorno de ClearType está deshabilitado:

-   En cliente de Terminal Server
-   Para fuentes de mapa de bits, fuentes vectoriales, fuentes de dispositivo, fuentes de tipo 1 o fuentes OpenType PostScript sin contornos TrueType
-   Si la fuente ha optimizado los mapas de bits incrustados, solo para aquellos tamaños de fuente que contengan los mapas de bits incrustados

Para activar el suavizado de contorno de ClearType, llame a [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) una vez para activar el suavizado de fuentes y, después, una segunda vez para establecer el tipo de suavizado en fe \_ FONTSMOOTHINGCLEARTYPE, como se muestra en el ejemplo de código siguiente:


```C++
SystemParametersInfo(SPI_SETFONTSMOOTHING,
                     TRUE,
                     0,
                     SPIF_UPDATEINIFILE | SPIF_SENDCHANGE);
SystemParametersInfo(SPI_SETFONTSMOOTHINGTYPE,
                     0,
                     (PVOID)FE_FONTSMOOTHINGCLEARTYPE,
                     SPIF_UPDATEINIFILE | SPIF_SENDCHANGE); 
```



Puede ajustar el aspecto del texto cambiando el valor de contraste utilizado en el algoritmo ClearType. El valor predeterminado es 1.400, pero puede ser cualquier valor entre 1.000 y 2.200. En función del dispositivo de pantalla y la sensibilidad del usuario a los colores, un valor de contraste mayor o menor puede mejorar la legibilidad. Para cambiar el contraste, llame a [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) con SPI \_ SETFONTSMOOTHINGCONTRAST. En el código siguiente se establece el valor de contraste en 1.600.


```C++
SystemParametersInfo(SPI_SETFONTSMOOTHINGCONTRAST,
                     0,
                     (PVOID)1600,
                     SPIF_UPDATEINIFILE | SPIF_SENDCHANGE); 
```



Debe tener en cuenta los siguientes detalles para la compatibilidad de aplicaciones:

-   La representación de texto con ClearType es ligeramente más lenta que con el suavizado de contorno estándar.
-   Las aplicaciones no deben usar XOR para mostrar el texto seleccionado. Las aplicaciones deben establecer el color de fondo y volver a mostrar el texto seleccionado.
-   Las aplicaciones no deben pintar el mismo texto sobre sí mismo en modo transparente. Si esto ocurre, los píxeles del borde con suavizado de contorno establecerán la combinación de colores en lugar de con el color de fondo. Esto da como resultado bordes oscurecidos y multicolor.
-   Las aplicaciones no deben pintar texto pintando los caracteres individualmente en el modo opaco porque el borde de un carácter puede recortarse por el siguiente carácter. Esto se debe a que un carácter suavizado con ClearType puede tener un ancho negativo A o C, donde el carácter normal tiene un ancho positivo o de C. Solo se garantiza que el ancho B del carácter es el mismo. Del mismo modo, las aplicaciones deben tener cuidado si el texto suavizado está junto al texto sin suavizar.
-   Si una aplicación representa texto y, a continuación, manipula el mapa de bits, el suavizado de fuentes debe desactivarse estableciendo el miembro **lfQuality** de la estructura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) en NONANTIALIASED \_ Quality. Por ejemplo, un juego puede Agregar un efecto de sombra de mapa de bits o el texto representado en un mapa de bits se puede escalar para generar un ThumbView.
-   Si el usuario se ejecuta en modo vertical (es decir, la segmentación del monitor es horizontal), se debe deshabilitar el suavizado de contorno de ClearType.

El parámetro *fdwQuality* de [**CreateFont**](/windows/desktop/api/Wingdi/nf-wingdi-createfonta) y el miembro **lfQuality** de [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) aceptan la marca de calidad de CLEARTYPE \_ . La rasterización de las fuentes creadas con esta marca usará el rasterizador de ClearType. Esta marca no tiene ningún efecto en las versiones anteriores del sistema operativo.

 

 
