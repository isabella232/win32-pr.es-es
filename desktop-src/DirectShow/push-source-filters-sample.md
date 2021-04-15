---
description: Ejemplo de filtros de origen de la instalación
ms.assetid: fc52f7bc-e9c7-4cd4-91e8-5c8f3450ca95
title: Ejemplo de filtros de origen de la instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ce22c7c6d73f54152ce469b4b3bb40c20db6c29
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537150"
---
# <a name="push-source-filters-sample"></a>Ejemplo de filtros de origen de la instalación

## <a name="description"></a>Descripción

Este ejemplo consta de un conjunto de tres filtros de origen que proporcionan los siguientes datos de origen como una secuencia de vídeo:

-   CPushSourceBitmap: mapa de bits único (cargado desde el directorio actual)
-   CPushSourceBitmapSet: conjunto de mapas de bits (cargados desde el directorio actual)
-   CPushSourceDesktop: copia de la imagen de escritorio actual (solo GDI)

## <a name="usage"></a>Uso

Para usar un filtro, cárguelo en GraphEdit y represente su PIN de salida. Esto conectará un representador de vídeo (y posiblemente un filtro de convertidor de espacio de colores) y le permitirá mostrar la salida. Si desea representar el resultado en un archivo AVI, cárguelo, cargue el filtro del escritor de archivos, proporcione un nombre de salida al escritor de archivos y represente el PIN de salida del filtro PushSource. También puede cargar y conectar compresores de vídeo, efectos de vídeo, etc.

> [!Note]  
> El filtro de captura del escritorio no es compatible con las superposiciones de hardware, por lo que no capturará el vídeo representado en una superficie de superposición o los cursores que se muestran a través de la superposición de hardware. Usa GDI para convertir la imagen de escritorio actual en un mapa de bits, que se pasa al pin de salida como un ejemplo multimedia.

 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Para descargar los ejemplos del SDK de DirectShow, instale la versión más reciente de la [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Este ejemplo se instala en la siguiente ruta de acceso: ejemplos *\[ raíz \] del SDK* \\ \\ filtros DirectShow de multimedia \\ \\ \\ PushSource.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos de DirectShow](directshow-samples.md)
</dt> </dl>

 

 



