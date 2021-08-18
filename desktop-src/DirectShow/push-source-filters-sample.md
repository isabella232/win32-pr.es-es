---
description: Ejemplo de filtros de origen de inserción
ms.assetid: fc52f7bc-e9c7-4cd4-91e8-5c8f3450ca95
title: Ejemplo de filtros de origen de inserción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0e72a9be7e5fa81d4fe2dc006c6d12e42f4f94d91561823b7f26a8400bbddda
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747795"
---
# <a name="push-source-filters-sample"></a>Ejemplo de filtros de origen de inserción

## <a name="description"></a>Descripción

Este ejemplo consta de un conjunto de tres filtros de origen que proporcionan los siguientes datos de origen como secuencia de vídeo:

-   CPushSourceBitmap: mapa de bits único (cargado desde el directorio actual)
-   CPushSourceBitmapSet: conjunto de mapas de bits (cargados desde el directorio actual)
-   CPushSourceDesktop: copia de la imagen de escritorio actual (solo GDI)

## <a name="usage"></a>Uso

Para usar un filtro, cárbalo en GraphEdit y represente su pin de salida. Esto conectará un representador de vídeo (y posiblemente un filtro convertidor de espacio de color) y le permitirá mostrar la salida. Si desea representar la salida en un archivo AVI, cargue el Mux avi, cargue un filtro de escritor de archivos, proporcione un nombre de salida al escritor de archivos y represente el pin de salida del filtro PushSource. También puede cargar y conectar vídeos, efectos de vídeo, entre otros.

> [!Note]  
> El filtro de captura de escritorio no admite superposiciones de hardware, por lo que no capturará vídeo representado en una superficie superpuesta ni cursores mostrados a través de la superposición de hardware. Usa GDI para convertir la imagen de escritorio actual en un mapa de bits, que se pasa a la marca de salida como un ejemplo multimedia.

 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Para descargar los ejemplos DirectShow SDK, instale la versión más reciente del [SDK de Windows.](https://msdn.microsoft.com/windowsvista/bb980924.aspx)

Este ejemplo se instala en la siguiente ruta de acceso: Ejemplos raíz del *\[ SDK \]* \\ Multimedia DirectShow Filtros \\ \\ \\ \\ pushSource.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Muestras](directshow-samples.md)
</dt> </dl>

 

 



