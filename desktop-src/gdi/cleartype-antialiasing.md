---
description: El suavizado de contorno de Microsoft ClearType es un método de suavizado que mejora la resolución de la visualización de fuentes sobre el suavizado de contorno tradicional.
ms.assetid: b9896934-1e4f-4ae1-922a-ef30e0edf94f
title: Suavizado de contorno de ClearType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcc8444c1e1b594559f9c5b7f96529a0db00b20c6a10e560bc1dcb4574e079d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117888104"
---
# <a name="cleartype-antialiasing"></a>Suavizado de contorno de ClearType

El suavizado de contorno de Microsoft ClearType es un método de suavizado que mejora la resolución de la visualización de fuentes sobre el suavizado de contorno tradicional. Mejora drásticamente la legibilidad en monitores DE COLOR DE COLOR con una interfaz digital, como las de los equipos portátiles y las pantallas de escritorio planas de alta calidad. La legibilidad en las pantallas de CRT también se ha mejorado ligeramente.

Sin embargo, ClearType depende de la orientación y el orden de las franjas de LAN. Actualmente, ClearType solo se implementa para LCD con franjas verticales ordenadas rgb. En concreto, esto afecta a los equipos de tableta, donde la pantalla se puede orientar en cualquier dirección y a las pantallas que se pueden convertir de horizontal a vertical.

Se permite el suavizado de contorno ClearType:

-   Para colores de 16, 24 y 32 bits (deshabilitado para 256 colores o menos)
-   Para dc de pantalla y controlador de dominio de memoria (no para controlador de dominio de impresora)
-   Para fuentes TrueType y fuentes OpenType con contornos de TrueType

El suavizado de contorno ClearType está deshabilitado:

-   En el cliente de Terminal Server
-   Para fuentes de mapa de bits, fuentes vectoriales, fuentes de dispositivo, fuentes de tipo 1 o fuentes Postscript OpenType sin contornos de TrueType
-   Si la fuente ha optimizado los mapas de bits incrustados, solo para los tamaños de fuente que contienen los mapas de bits incrustados.

Para activar el suavizado de contorno ClearType, llame a [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) una vez para activar el suavizado de fuentes y, a continuación, una segunda vez para establecer el tipo de suavizado en FE FONTSMOOTHINGCLEARTYPE, como se muestra en el ejemplo de código \_ siguiente:


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



Puede ajustar la apariencia del texto cambiando el valor de contraste utilizado en el algoritmo ClearType. El valor predeterminado es 1400, pero puede ser cualquier valor de 1000 a 2200. En función del dispositivo de visualización y la sensibilidad del usuario a los colores, un valor de contraste superior o inferior puede mejorar la legibilidad. Para cambiar el contraste, llame [**a SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) con SPI \_ SETFONTSMOOTHINGCONTRAST. El código siguiente establece el valor de contraste en 1600.


```C++
SystemParametersInfo(SPI_SETFONTSMOOTHINGCONTRAST,
                     0,
                     (PVOID)1600,
                     SPIF_UPDATEINIFILE | SPIF_SENDCHANGE); 
```



Debe tener en cuenta los siguientes detalles para la compatibilidad de aplicaciones:

-   La representación de texto con ClearType es ligeramente más lenta que con el suavizado de contorno estándar.
-   Las aplicaciones no deben usar XOR para mostrar el texto seleccionado. Las aplicaciones deben establecer el color de fondo y volver a mostrar el texto seleccionado.
-   Las aplicaciones no deben pintar el mismo texto encima de sí mismos en modo transparente. Si esto ocurre, los píxeles de borde con suavizado de contorno se combinarán por sí mismos en lugar de con el color de fondo. Esto da como resultado bordes oscuros y de colores.
-   Las aplicaciones no deben pintar texto pintando los caracteres individualmente en modo opaco porque el borde de un carácter puede recortarse con el carácter siguiente. Esto se produce porque un carácter suavizado con ClearType puede tener un ancho A o C negativo, donde el carácter normal tiene un ancho A o C positivo. Solo se garantiza que el ancho B del carácter sea el mismo. Del mismo modo, las aplicaciones deben tener cuidado si el texto suavizado está junto al texto no desenfocado.
-   Si una aplicación representa texto y, a continuación, manipula el mapa de bits, el suavizado de fuentes debe desactivarse estableciendo el miembro **lfQuality** de la estructura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) en NONANTIALIASED \_ QUALITY. Por ejemplo, un juego puede agregar un efecto de sombra de mapa de bits o el texto representado en un mapa de bits se puede escalar para generar una vista digital.
-   Si el usuario se ejecuta en modo vertical (es decir, el seccionado de supervisión es horizontal), debe deshabilitarse el suavizado de contorno ClearType.

El *parámetro fdwQuality* de [**CreateFont y**](/windows/desktop/api/Wingdi/nf-wingdi-createfonta) el miembro **lfQuality** de [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) aceptan la marca CLEARTYPE \_ QUALITY. La rasterización de las fuentes creadas con esta marca usará el rasterizador ClearType. Esta marca no tiene ningún efecto en las versiones anteriores del sistema operativo.

 

 
