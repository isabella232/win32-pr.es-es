---
title: Trabajar con paletas
description: Trabajar con paletas
ms.assetid: 0ad0d78b-4c2c-499c-ad5e-8324b59e89fc
keywords:
- Mensaje WM_CAP_PAL_PASTE
- capPalettePaste (macro)
- Mensaje WM_CAP_PAL_OPEN
- capPaletteOpen (macro)
- Mensaje WM_CAP_PAL_AUTOCREATE
- capPaletteAuto (macro)
- Mensaje WM_CAP_PAL_MANUALCREATE
- capPaletteManual (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f09cbbe3ffc8ea21d1ecf8545f036f5ba6dfb927
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105651286"
---
# <a name="working-with-palettes"></a>Trabajar con paletas

Inicialmente, si el formato de captura de vídeo requiere una paleta, la ventana de captura utiliza la paleta suministrada por el controlador de captura. Esta paleta puede constar de valores de escala de grises para la reproducción en blanco y negro, o una amplia selección de valores de color. Puede recuperar una paleta existente para reemplazar la paleta predeterminada mediante el mensaje [](/windows/desktop/api/Vfw/nf-vfw-cappalettepaste) [](/windows/desktop/api/Vfw/nf-vfw-cappaletteopen) Open [**\_ Cap Cap \_ de \_ WM mayúsculas**](wm-cap-pal-paste.md) o [**\_ Cap \_ \_ Cap de WM**](wm-cap-pal-open.md) (o la macro capPalettePaste o capPaletteOpen). Como alternativa, puede crear una paleta personalizada para reemplazar la paleta predeterminada mediante el mensaje MANUALCREATE [**Cap Cap de WM con la función de \_ \_ \_ creación**](wm-cap-pal-autocreate.md) de valores de [**Cap o \_ \_ PAL \_ Cap**](wm-cap-pal-manualcreate.md) de WM (o la macro [**capPaletteAuto**](/windows/desktop/api/Vfw/nf-vfw-cappaletteauto) o [**capPaletteManual**](/windows/desktop/api/Vfw/nf-vfw-cappalettemanual) ). Después de reemplazar la paleta predeterminada, la ventana captura y el controlador usan la paleta de reemplazo hasta que cree o abra otra paleta.

El \_ mensaje MANUALCREATE de WM Cap \_ PAL \_ AutoCreate o WM \_ Cap \_ PAL \_ crea una paleta optimizada basada en la entrada de vídeo actual. Esta paleta personalizada proporciona una secuencia de vídeo de la mejor fidelidad de color porque se basa en los colores que existen en la secuencia. La ventana captura crea un histograma tridimensional de los colores que muestrea. Reduce el número de colores mediante el examen del error absoluto entre los colores adyacentes y la consolidación de aquellos con el menor valor de error.

Al enviar la \_ \_ creación de \_ código PAL Cap de WM, debe especificar el número de fotogramas de AVICap para muestrear y especificar el tamaño de la paleta de colores. Al especificar el número de fotogramas, incluya suficientes fotogramas para asegurarse de que se muestrean todos los colores de la secuencia.

Puede muestrear el fotograma actual mediante el uso de MANUALCREATE de Cap de WM \_ \_ \_ . Si usa este mensaje con varios marcos seleccionados manualmente, puede crear una paleta que contenga los colores que desea que aparezcan en la paleta.

Una paleta puede contener hasta 256 colores. Si combina las paletas o si la secuencia de vídeo se va a mostrar al mismo tiempo que otros vídeos o imágenes, debe usar una selección de color más pequeña para que los colores de cada imagen o clip de vídeo puedan coexistir.

La nueva paleta se guarda con el mensaje [**de \_ \_ \_ guardado de PAL de Cap de WM**](wm-cap-pal-save.md) (o la macro [**capPaletteSave**](/windows/desktop/api/Vfw/nf-vfw-cappalettesave) ) y, posteriormente, se recupera mediante el mensaje [**\_ \_ \_ abierto PAL Cap de WM**](wm-cap-pal-open.md) . Puede guardar una paleta para el procesamiento posterior de la paleta o para su uso en otra aplicación.

Puede pegar una paleta desde el portapapeles en la ventana de captura mediante el mensaje de [**\_ \_ \_ pegado PAL de Cap de WM**](wm-cap-pal-paste.md) . La ventana captura pasa la paleta al controlador de captura. Otras aplicaciones pueden copiar las paletas en el portapapeles. También puede copiar una paleta en el portapapeles mediante el mensaje de [**\_ \_ Edición \_ de Cap de WM**](wm-cap-edit-copy.md) (o la macro [**capEditCopy**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy) ). Este mensaje copia el búfer de fotogramas de vídeo, incluida la paleta, en el portapapeles.

 

 




