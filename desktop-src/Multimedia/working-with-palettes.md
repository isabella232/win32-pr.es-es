---
title: Trabajar con paletas
description: Trabajar con paletas
ms.assetid: 0ad0d78b-4c2c-499c-ad5e-8324b59e89fc
keywords:
- WM_CAP_PAL_PASTE mensaje
- CapPalettePaste macro
- WM_CAP_PAL_OPEN mensaje
- capPaletteOpen macro
- WM_CAP_PAL_AUTOCREATE mensaje
- capPaletteAuto macro
- WM_CAP_PAL_MANUALCREATE mensaje
- capPalette Macromanual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f09cbbe3ffc8ea21d1ecf8545f036f5ba6dfb927
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161313"
---
# <a name="working-with-palettes"></a>Trabajar con paletas

Inicialmente, si el formato de captura de vídeo requiere una paleta, la ventana de captura usa la paleta proporcionada por el controlador de captura. Esta paleta puede constar de valores de escala de grises para reproducción en blanco y negro, o una amplia selección de valores de color. Puede recuperar una paleta existente para reemplazar la paleta predeterminada mediante el mensaje [**WM \_ CAP PAL \_ \_ PASTE**](wm-cap-pal-paste.md) o [**WM CAP PAL \_ \_ \_ OPEN**](wm-cap-pal-open.md) (o la macro [**capPalettePaste**](/windows/desktop/api/Vfw/nf-vfw-cappalettepaste) o [**capPaletteOpen).**](/windows/desktop/api/Vfw/nf-vfw-cappaletteopen) Como alternativa, puede crear una paleta personalizada para reemplazar la paleta predeterminada mediante el mensaje [**WM \_ CAP PAL \_ \_ AUTOCREATE**](wm-cap-pal-autocreate.md) o [**WM CAP PAL \_ \_ \_ MANUALCREATE**](wm-cap-pal-manualcreate.md) (o la macro [**capPaletteAuto**](/windows/desktop/api/Vfw/nf-vfw-cappaletteauto) o [**capPaletteManual).**](/windows/desktop/api/Vfw/nf-vfw-cappalettemanual) Después de reemplazar la paleta predeterminada, la ventana de captura y el controlador usan la paleta de reemplazo hasta que cree o abra otra paleta.

El mensaje WM \_ CAP \_ PAL AUTOCREATE o WM CAP PAL MANUALCREATE crea una paleta optimizada \_ basada en la entrada de vídeo \_ \_ \_ actual. Esta paleta personalizada proporciona a una secuencia de vídeo la mejor fidelidad de color porque se basa en los colores que existen en la secuencia. La ventana de captura crea un histograma tridimensional de los colores que muestrea. Reduce el número de colores examinando el error absoluto entre los colores adyacentes y consolidando los que tienen el valor de error más pequeño.

Al enviar WM CAP PAL AUTOCREATE, debe especificar el número de fotogramas para que AVICap muestree y especificar el \_ tamaño de la paleta de \_ \_ colores. Al especificar el número de fotogramas, incluya suficientes fotogramas para asegurarse de que se muestrea todos los colores de la secuencia.

Puede muestrear el marco actual mediante WM \_ CAP \_ PAL \_ MANUALCREATE. Con este mensaje con varios fotogramas seleccionados manualmente, puede crear una paleta que contenga los colores que desea que aparezcan en la paleta.

Una paleta puede contener hasta 256 colores. Si combina paletas o si la secuencia de vídeo se va a mostrar simultáneamente con otros vídeos o imágenes, debe usar una selección de color más pequeña para que los colores de cada imagen o clip de vídeo puedan coexistir.

Guarde una nueva paleta mediante el mensaje SAVE de [**WM \_ CAP \_ \_ PAL**](wm-cap-pal-save.md) (o la macro [**capPaletteSave)**](/windows/desktop/api/Vfw/nf-vfw-cappalettesave) y, posteriormente, recupérelo mediante el mensaje [**WM CAP PAL \_ \_ \_ OPEN.**](wm-cap-pal-open.md) Puede guardar una paleta para el procesamiento posterior de la paleta o para su uso en otra aplicación.

Puede pegar una paleta desde el Portapapeles en la ventana de captura mediante el mensaje [**PASTE de WM CAP \_ \_ PAL. \_**](wm-cap-pal-paste.md) La ventana de captura pasa la paleta al controlador de captura. Otras aplicaciones pueden copiar paletas en el Portapapeles. También puede copiar una paleta en el Portapapeles mediante el mensaje [**EDIT \_ \_ \_ COPY**](wm-cap-edit-copy.md) de WM CAP (o la [**macro capEditCopy).**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy) Este mensaje copia el búfer de fotogramas de vídeo, incluida la paleta, en el Portapapeles.

 

 




