---
title: Reproductor de Windows Media Convención de trabajo de BITS
description: Reproductor de Windows Media descargar y agregar automáticamente elementos multimedia digitales a la biblioteca si usa Servicio de transferencia inteligente en segundo plano (BITS).
ms.assetid: 643faba7-9af2-4292-8d92-e321d7690a5b
keywords:
- Reproductor de Windows Media en línea, Servicio de transferencia inteligente en segundo plano (BITS)
- tiendas en línea, Servicio de transferencia inteligente en segundo plano (BITS)
- tiendas en línea de tipo 2, Servicio de transferencia inteligente en segundo plano (BITS)
- Servicio de transferencia inteligente en segundo plano (BITS)
- BITS (Servicio de transferencia inteligente en segundo plano)
- Reproductor de Windows Media en línea, convención de trabajo bits
- tiendas en línea, convención de trabajo de BITS
- tiendas en línea de tipo 2, convención de trabajo bits
- Convención de trabajo de BITS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85278593ce151f46370ca491ccac8e1645f9bb70
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073182"
---
# <a name="windows-media-player-bits-job-convention"></a>Reproductor de Windows Media Convención de trabajo de BITS

Reproductor de Windows Media descargar y agregar automáticamente elementos multimedia digitales a la biblioteca si usa [Servicio de transferencia inteligente en segundo plano (BITS).](/windows/desktop/Bits/background-intelligent-transfer-service-portal) Para aprovechar esta característica, debe agregar el trabajo a la cola de transferencia de BITS y llamar a **IBackgroundCopyJob::SetDescription**, proporcionando una cadena de descripción que use el formato correcto.

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

## <a name="syntax"></a>Sintaxis

``` syntax
::WMP_JOB:1:serviceId:Provider:AlbumArtist:AlbumTitle:TrackNumber:Title:Duration:Rating
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="serviceId"></span><span id="serviceid"></span><span id="SERVICEID"></span>*serviceId*
</dt> <dd>

Valor de 32 bits generado aleatoriamente que Reproductor de Windows Media usa para identificar el servicio.

</dd> <dt>

<span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>*Proveedor*
</dt> <dd>

Nombre del proveedor. Este valor debe coincidir con un nombre de clave de tienda en línea válido.

</dd> <dt>

<span id="AlbumArtist"></span><span id="albumartist"></span><span id="ALBUMARTIST"></span>*AlbumArtist*
</dt> <dd>

Nombre del intérprete principal del álbum.

</dd> <dt>

<span id="AlbumTitle"></span><span id="albumtitle"></span><span id="ALBUMTITLE"></span>*AlbumTitle*
</dt> <dd>

Título del álbum.

</dd> <dt>

<span id="TrackNumber"></span><span id="tracknumber"></span><span id="TRACKNUMBER"></span>*TrackNumber*
</dt> <dd>

Número de pista de CD.

</dd> <dt>

<span id="Title"></span><span id="title"></span><span id="TITLE"></span>*Título*
</dt> <dd>

Título del contenido.

</dd> <dt>

<span id="Duration"></span><span id="duration"></span><span id="DURATION"></span>*Duración*
</dt> <dd>

Duración del contenido.

</dd> <dt>

<span id="Rating"></span><span id="rating"></span><span id="RATING"></span>*Clasificación*
</dt> <dd>

Clasificación del contenido.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Cuando Reproductor de Windows Media 10 o posterior usa BITS para descargar contenido, enumera los trabajos de la cola de transferencia e inspecciona la cadena de descripción de cada trabajo. Si la cadena de descripción coincide con la convención esperada, Reproductor de Windows Media descarga el contenido.

Solo debe agregar un archivo multimedia digital para su descarga a cada trabajo de BITS.

Después de iniciar un trabajo de BITS mediante esta convención, debe dejar que Reproductor de Windows Media el trabajo. Reproductor de Windows Media quitará el trabajo de la cola de BITS, moverá el archivo descargado a la ubicación donde se guarda la música desgarrada y agregará el archivo descargado a la biblioteca.

El *parámetro serviceId* debe contener un valor distinto de cero de 32 bits. Se recomienda usar la función [**CryptGenRandom para**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) crear este valor.

El nombre de archivo que especifique mediante el parámetro *localName* de **IBackgroundCopyJob::AddFile** debe tener una extensión de nombre de archivo .wma, .wmv, .mp3 o .asf.

Los parámetros restantes están diseñados para contener valores de metadatos relacionados con el contenido. Puede recuperar estos valores de la página web de la tienda en línea mediante **DownloadItem.getItemInfo**. Puede recuperar la colección de descarga correcta llamando **a DownloadManager.getDownloadCollection** y proporcionando *serviceId* como *parámetro collectionId.*

Reproductor de Windows Media la cola de BITS periódicamente mientras se ejecuta el reproductor. Para asegurarse de que Reproductor de Windows Media la cola de BITS en busca de trabajos de descarga, debe crear un valor en la siguiente subclave del Registro:

**HKEY \_ CURRENT \_ USER \\ Software \\ Microsoft \\ MediaPlayer \\ Services**

El valor debe crearse como se muestra a continuación.



| Nombre                | Tipo      | Descripción                                                                                                                                                                                                          |
|---------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **RefreshDownload** | **DWORD** | Especifica si Reproductor de Windows Media debe inspeccionar la cola de BITS en busca de trabajos de descarga. Si el valor es cero, el reproductor no inspeccionará la cola bits. El reproductor debe inspeccionar la cola si el valor es distinto de cero. |



 

Puede usar la siguiente sintaxis alternativa para agregar trabajos de BITS Reproductor de Windows Media no se completa, pero para los que simplemente muestra información de estado:

``` syntax
::WMP_STATUS:1:serviceId:Provider:AlbumArtist:AlbumTitle:TrackNumber:Title:Duration:Rating
```

Cuando use la sintaxis anterior, debe escribir código para completar la descarga de BITS, organizar el contenido en el equipo del usuario y agregar el contenido a la biblioteca, si lo desea.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[CryptGenRandom](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom)
</dt> <dt>

[**DownloadItem.getItemInfo**](downloaditem-getiteminfo.md)
</dt> <dt>

[**DownloadManager.getDownloadCollection**](downloadmanager-getdownloadcollection.md)
</dt> <dt>

[**Referencia de las tiendas en línea de tipo 2**](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 