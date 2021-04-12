---
title: Convención de trabajo de Windows Media Player BITS
description: Windows Media Player puede descargar y agregar elementos multimedia digitales a la biblioteca automáticamente si utiliza Servicio de transferencia inteligente en segundo plano (BITS).
ms.assetid: 643faba7-9af2-4292-8d92-e321d7690a5b
keywords:
- Windows Media Player tiendas en línea, Servicio de transferencia inteligente en segundo plano (BITS)
- tiendas en línea, Servicio de transferencia inteligente en segundo plano (BITS)
- tipo 2 tiendas en línea, Servicio de transferencia inteligente en segundo plano (BITS)
- Servicio de transferencia inteligente en segundo plano (BITS)
- BITS (Servicio de transferencia inteligente en segundo plano)
- Windows Media Player tiendas en línea, Convención de trabajo de BITS
- tiendas en línea, Convención de trabajos de BITS
- tipo 2 tiendas en línea, Convención de trabajos de BITS
- Convención de trabajos de BITS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85278593ce151f46370ca491ccac8e1645f9bb70
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104271337"
---
# <a name="windows-media-player-bits-job-convention"></a>Convención de trabajo de Windows Media Player BITS

Windows Media Player puede descargar y agregar elementos multimedia digitales a la biblioteca automáticamente si utiliza [servicio de transferencia inteligente en segundo plano (bits)](/windows/desktop/Bits/background-intelligent-transfer-service-portal). Para aprovechar esta característica, debe agregar el trabajo a la cola de transferencia de BITS y llamar a **IBackgroundCopyJob:: SetDescription**, proporcionando una cadena de descripción que use el formato correcto.

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

## <a name="syntax"></a>Sintaxis

``` syntax
::WMP_JOB:1:serviceId:Provider:AlbumArtist:AlbumTitle:TrackNumber:Title:Duration:Rating
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="serviceId"></span><span id="serviceid"></span><span id="SERVICEID"></span>*serviceId*
</dt> <dd>

Valor de bit 32 generado aleatoriamente que Windows Media Player usa para identificar el servicio.

</dd> <dt>

<span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>*Presta*
</dt> <dd>

Nombre del proveedor. Este valor debe coincidir con un nombre de clave de almacén en línea válido.

</dd> <dt>

<span id="AlbumArtist"></span><span id="albumartist"></span><span id="ALBUMARTIST"></span>*AlbumArtist*
</dt> <dd>

Nombre del intérprete principal del álbum.

</dd> <dt>

<span id="AlbumTitle"></span><span id="albumtitle"></span><span id="ALBUMTITLE"></span>*Álbum*
</dt> <dd>

Título del álbum.

</dd> <dt>

<span id="TrackNumber"></span><span id="tracknumber"></span><span id="TRACKNUMBER"></span>*TrackNumber*
</dt> <dd>

Número de pista del CD.

</dd> <dt>

<span id="Title"></span><span id="title"></span><span id="TITLE"></span>*Titulo*
</dt> <dd>

Título del contenido.

</dd> <dt>

<span id="Duration"></span><span id="duration"></span><span id="DURATION"></span>*Duration*
</dt> <dd>

La duración del contenido.

</dd> <dt>

<span id="Rating"></span><span id="rating"></span><span id="RATING"></span>*Clasific*
</dt> <dd>

Clasificación del contenido.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Cuando Windows Media Player 10 o una versión posterior usa BITS para descargar contenido, enumera los trabajos de la cola de transferencia e inspecciona la cadena de descripción de cada trabajo. Si la cadena de Descripción coincide con la Convención esperada, Windows Media Player descarga el contenido.

Solo debe agregar un archivo multimedia digital para su descarga en cada trabajo de BITS.

Después de iniciar un trabajo de BITS con esta Convención, debe permitir que Windows Media Player complete el trabajo. Windows Media Player también quitará el trabajo de la cola de BITS, moverá el archivo descargado a la ubicación donde se guarda la música copiada y agregará el archivo descargado a la biblioteca.

El parámetro *serviceId* debe contener un valor de bit 32 distinto de cero. Se recomienda usar la función [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) para crear este valor.

El nombre de archivo que especifique mediante el parámetro *localname* de **IBackgroundCopyJob:: AddFile** debe tener una extensión de nombre de archivo. WMA,. wmv,. mp3 o. ASF.

Los parámetros restantes están diseñados para contener valores de metadatos relacionados con el contenido. Puede recuperar estos valores de la Página Web de la tienda en línea mediante **DownloadItem. getItemInfo**. Puede recuperar la colección de descargas correcta llamando a **Downloadmanager. getDownloadCollection** y proporcionando *ServiceId* como parámetro *collectionId* .

Windows Media Player inspecciona la cola de BITS periódicamente mientras el reproductor se está ejecutando. Para asegurarse de que Windows Media Player comprueba la cola de BITS para los trabajos de descarga, debe crear un valor en la subclave del Registro siguiente:

**HKEY \_ Current \_ User \\ software \\ Microsoft \\ MediaPlayer \\ Services**

El valor debe crearse como se indica a continuación.



| Nombre                | Tipo      | Descripción                                                                                                                                                                                                          |
|---------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **RefreshDownload** | **DWORD** | Especifica si Windows Media Player debe inspeccionar la cola de BITS para los trabajos de descarga. Si el valor es cero, el reproductor no inspeccionará la cola de BITS. El reproductor debe inspeccionar la cola si el valor es distinto de cero. |



 

Puede usar la siguiente sintaxis alternativa para agregar trabajos de BITS que Windows Media Player no complete, pero para los que simplemente muestra información de estado:

``` syntax
::WMP_STATUS:1:serviceId:Provider:AlbumArtist:AlbumTitle:TrackNumber:Title:Duration:Rating
```

Cuando use la sintaxis anterior, debe escribir código para completar la descarga de BITS, organizar el contenido en el equipo del usuario y agregar el contenido a la biblioteca, si lo desea.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[CryptGenRandom](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom)
</dt> <dt>

[**DownloadItem. getItemInfo**](downloaditem-getiteminfo.md)
</dt> <dt>

[**DownloadManager.getDownloadCollection**](downloadmanager-getdownloadcollection.md)
</dt> <dt>

[**Referencia de las tiendas en línea de tipo 2**](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 