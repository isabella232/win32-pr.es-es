---
title: Para buscar por tiempo mediante el lector asincrónico
description: Para buscar por tiempo mediante el lector asincrónico
ms.assetid: 731b0a6e-1472-45a7-998c-e395be86036f
keywords:
- Formato de sistemas avanzados (ASF), búsqueda por hora
- ASF (formato de sistemas avanzados), buscar por hora
- Formato de sistemas avanzados (ASF), lectores asincrónicos
- ASF (formato de sistemas avanzados), lectores asincrónicos
- lectores asincrónicos, buscando por hora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 070d480cade395cdbead99b1aedde8928c6fb18b4af15bf6b72c1bcc0dcd6dc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118196464"
---
# <a name="to-seek-by-time-using-the-asynchronous-reader"></a>Para buscar por tiempo mediante el lector asincrónico

Si desea buscar un tiempo de presentación específico en un archivo ASF, el archivo debe estar configurado correctamente. Puede buscar solo en archivos de audio de forma predeterminada, pero los archivos de vídeo deben indexarse antes de buscar. Si no está seguro de cómo se ha creado un archivo, puede comprobar el atributo g wszWMSeekable en el encabezado del archivo llamando a \_ [**IWMHeaderInfo::GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).

Para buscar datos en un archivo ASF por tiempo de presentación mediante el lector asincrónico, llame a [**IWMReader::Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start), pasando el tiempo y la duración deseados de la parte del archivo que desea leer como *cnsStart* y *cnsDuration* respectivamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMReader (Interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Lectura de archivos con el lector asincrónico**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Lectura de metadatos durante la reproducción**](reading-metadata-at-playback.md)
</dt> <dt>

[**Trabajar con índices**](working-with-indexes.md)
</dt> </dl>

 

 




