---
title: Almacenamiento de contenido
description: Almacenamiento de contenido
ms.assetid: 22f4e580-43a4-48b5-8eb3-90e1346a1093
keywords:
- Windows Media Format SDK, guardar contenido
- SDK de Windows Media Format, streaming de caché rápido
- Advanced Systems Format (ASF), guardar contenido
- ASF (formato de sistemas avanzados), guardar contenido
- Advanced Systems Format (ASF), streaming de caché rápido
- ASF (formato de sistemas avanzados), streaming de caché rápido
- flujos, guardar contenido
- Streaming de caché rápido, guardar contenido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba6c215a81accef29f8943ed52ca24264f785d94
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "103789208"
---
# <a name="saving-content"></a>Almacenamiento de contenido

Mediante este SDK, una aplicación puede guardar el contenido descargado o transmitido en el equipo local del usuario, llamando al método [**IWMReaderAdvanced2:: saveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-savefileas) en el objeto del lector. En el caso del contenido transmitido por secuencias, el servidor debe usar el streaming de caché rápido, que se describe en la sección [habilitación del streaming de caché rápido desde el cliente](enabling-fast-cache-streaming-from-the-client.md). En el caso del contenido transmitido por secuencias, el método **saveFileAs** crea un archivo ASX que señala a un archivo ASF que contiene el contenido guardado. Si el objeto lector está transmitiendo una lista de reproducción del servidor, cada entrada se guarda como un archivo ASF independiente y el archivo ASX apunta a cada uno de los archivos ASF. En el caso del contenido descargado, el método **saveFileAs** simplemente crea un archivo ASF.

Para guardar el contenido en un archivo local, haga lo siguiente:

1.  Llame a [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) con la dirección URL. **Open** es una llamada asincrónica y se devuelve inmediatamente. Espere a que se complete la operación, como se describe en [para crear un lector y abrir un archivo](to-create-a-reader-and-open-a-file.md).
2.  Consulte el objeto de lector para la interfaz [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4) .
3.  Compruebe si el contenido se puede guardar llamando al método [**IWMReaderAdvanced4:: CanSaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-cansavefileas) . Si el método devuelve false, el contenido no se puede guardar localmente. En caso contrario, continúe en el paso 4.
4.  Llame al método [**IWMReaderAdvanced4:: IsUsingFastCache**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-isusingfastcache) para determinar si el servidor usa el streaming de caché rápido.
5.  Llame a [**IWMReaderAdvanced2:: saveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-savefileas) con un nombre de archivo para el archivo local. Si el método **IsUsingFastCache** devuelve true, asigne a la extensión. ASX el nombre de archivo. De lo contrario, asigne al nombre de archivo una extensión. ASF,. WMA o. wmv.

La aplicación puede cancelar la operación de guardar mientras está en curso, llamando al método [**IWMReaderAdvanced4:: CancelSaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-cancelsavefileas) .

El contenido guardado podría estar protegido con DRM, por lo que es posible que no sea posible reproducir el archivo en otro equipo. Para obtener más información sobre la protección de contenido, vea [características de Rights Management digital](digital-rights-management-features.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaz IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Interfaz IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> </dl>

 

 




