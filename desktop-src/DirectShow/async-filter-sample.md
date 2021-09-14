---
description: Ejemplo de filtro asincrónico
ms.assetid: ad1f2386-6d23-4a6d-8542-bbca53df4825
title: Ejemplo de filtro asincrónico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 099931e9a20c977da18a67f9fe232c2ec391dd4e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162241"
---
# <a name="async-filter-sample"></a>Ejemplo de filtro asincrónico

## <a name="description"></a>Descripción

El ejemplo de filtro asincrónico es un filtro de lector de archivos que admite la descarga progresiva. Este filtro de ejemplo implementa las [**interfaces IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) [**e IFileSourceFilter.**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) Admite archivos MPEG, pero no archivos AVI.

## <a name="usage"></a>Uso

Este ejemplo incluye una pequeña aplicación de línea de comandos, Memfile.exe, que muestra el filtro. Los argumentos de la línea de comandos especifican un archivo multimedia y una velocidad de bits, en kilobytes por segundo. La aplicación lee el archivo en memoria a la velocidad especificada y reproduce el archivo. Para ello, crea una instancia del filtro, agrega el filtro al gráfico de filtros y representa el pin de salida del filtro.

En la línea de comandos, escriba:

**Velocidad de bits de nombre de archivo de Memfile**  

El filtro de ejemplo asincrónico no admite archivos AVI, ya que no se puede conectar al filtro [divisor avi.](avi-splitter-filter.md) El pin de salida del filtro asincrónico propone la secuencia MEDIATYPE \_ y MEDIASUBTYPE \_ NULL para el tipo de medio. El pin de entrada en el filtro divisor AVI no acepta MEDIASUBTYPE NULL y no propone \_ ningún tipo propio. Por lo tanto, se produce un error en la conexión de pin. El filtro asincrónico podría mejorarse para ofrecer MEDIASUBTYPE \_ Avi cuando corresponda. Por ejemplo, podría examinar el formato de archivo o usar la extensión de archivo.

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Para descargar los ejemplos DirectShow SDK, instale la versión más reciente del [SDK de Windows.](https://msdn.microsoft.com/windowsvista/bb980924.aspx)

Este ejemplo se instala en la siguiente ruta de acceso: Ejemplos raíz del \[ *SDK* \] \\ Multimedia DirectShow Filtros \\ \\ \\ \\ asincrónicos.

## <a name="related-topics"></a>Temas relacionados



[DirectShow Muestras](directshow-samples.md)


 

 



