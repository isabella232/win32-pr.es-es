---
title: Para buscar por tiempo mediante el lector asincrónico
description: Para buscar por tiempo mediante el lector asincrónico
ms.assetid: 731b0a6e-1472-45a7-998c-e395be86036f
keywords:
- Advanced Systems Format (ASF), búsqueda por tiempo
- ASF (formato de sistemas avanzados), búsqueda por hora
- Advanced Systems Format (ASF), lectores asincrónicos
- ASF (formato de sistemas avanzados), lectores asincrónicos
- lectores asincrónicos, búsqueda por hora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f3e24c04d75d762aef6bac498d4b4c8dfa9552
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788812"
---
# <a name="to-seek-by-time-using-the-asynchronous-reader"></a>Para buscar por tiempo mediante el lector asincrónico

Si desea buscar un tiempo de presentación específico en un archivo ASF, el archivo debe estar configurado correctamente. Puede buscar en archivos de solo audio de forma predeterminada, pero los archivos de vídeo se deben indexar antes de la búsqueda. Si no está seguro de cómo se ha creado un archivo, puede comprobar el \_ atributo g wszWMSeekable en el encabezado del archivo llamando a [**IWMHeaderInfo:: GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).

Para buscar datos en un archivo ASF en el momento de la presentación mediante el lector asincrónico, llame a [**IWMReader:: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start), pasando el tiempo deseado y la duración de la parte del archivo que desea leer como *cnsStart* y *cnsDuration* , respectivamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaz IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Leer archivos con el lector asincrónico**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Leer metadatos en la reproducción**](reading-metadata-at-playback.md)
</dt> <dt>

[**Trabajar con índices**](working-with-indexes.md)
</dt> </dl>

 

 




