---
description: Ejemplo de filtro Async
ms.assetid: ad1f2386-6d23-4a6d-8542-bbca53df4825
title: Ejemplo de filtro Async
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 099931e9a20c977da18a67f9fe232c2ec391dd4e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104080056"
---
# <a name="async-filter-sample"></a>Ejemplo de filtro Async

## <a name="description"></a>Descripción

El ejemplo de filtro Async es un filtro de lector de archivos que admite la descarga progresiva. Este filtro de ejemplo implementa las interfaces [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) y [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) . Admite archivos MPEG, pero no archivos AVI.

## <a name="usage"></a>Uso

En este ejemplo se incluye una pequeña aplicación de línea de comandos, Memfile.exe, que muestra el filtro. Los argumentos de la línea de comandos especifican un archivo multimedia y una velocidad de bits, en kilobytes por segundo. La aplicación lee el archivo en la memoria a la velocidad especificada y reproduce el archivo. Para ello, crea una instancia del filtro, agrega el filtro al gráfico de filtro y representa el PIN de salida del filtro.

En la línea de comandos, escriba:

**Velocidad de bits de Memfile FILENAME**  

El filtro de ejemplo Async no admite archivos AVI porque no se puede conectar al filtro de [divisor de AVI](avi-splitter-filter.md) . El PIN de salida del filtro asincrónico propone \_ el flujo MEDIATYPE y MEDIASUBTYPE \_ null para el tipo de medio. El PIN de entrada en el filtro de divisor de AVI no acepta MEDIASUBTYPE \_ null y no propone ningún tipo propio. Por lo tanto, se produce un error en la conexión del PIN. El filtro Async se podría mejorar para ofrecer MEDIASUBTYPE \_ AVI cuando corresponda. Por ejemplo, podría examinar el formato de archivo o utilizar la extensión de archivo.

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Para descargar los ejemplos del SDK de DirectShow, instale la versión más reciente de la [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Este ejemplo se instala en la siguiente ruta de acceso: \[ ejemplos *raíz del SDK* \] \\ \\ filtros DirectShow de multimedia \\ \\ \\ Async.

## <a name="related-topics"></a>Temas relacionados



[Ejemplos de DirectShow](directshow-samples.md)


 

 



