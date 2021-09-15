---
title: Referencia de las tiendas en línea de tipo 2
description: Referencia de las tiendas en línea de tipo 2
ms.assetid: b3f580cc-b02d-4312-a7a1-a35778a222bc
keywords:
- Reproductor de Windows Media online stores,reference
- tiendas en línea, referencia
- tiendas en línea de tipo 2, referencia
- Referencia de las tiendas en línea de tipo 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c164ad74481030a52cd31605b29833d3bfbd3f1d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568216"
---
# <a name="reference-for-type-2-online-stores"></a>Referencia de las tiendas en línea de tipo 2

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

Reproductor de Windows Media 10 o posterior proporciona objetos, interfaces, propiedades y métodos que admiten almacenes en línea de tipo 2. En las secciones siguientes se documentan en detalle.



| Sección                                                                                                        | Descripción                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IWMPSubscriptionService (interfaz)](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice)                                               | Proporciona métodos para aumentar la administración de derechos digitales (DRM) e iniciar procesos en segundo plano.                                                                              |
| [IWMPSubscriptionService2 (Interfaz)](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2)                                             | Proporciona métodos para iniciar procesos en segundo plano, para proporcionar información sobre la actividad de la tienda en línea y para proporcionar un puntero a la Reproductor de Windows Media principal. |
| [IWMPSubscriptionServiceCallback (Interfaz)](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservicecallback)                               | Define un método que los almacenes en línea usan para notificar Reproductor de Windows Media cuando se completa un proceso en segundo plano.                                                              |
| [WMPNotifySubscriptionPluginAddRemove](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-wmpnotifysubscriptionpluginaddremove)                               | Función que se usa para notificar Reproductor de Windows Media que se ha instalado o desinstalado un complemento.                                                                            |
| [DownloadCollection (objeto)](downloadcollection-object.md)                                                     | Proporciona métodos y propiedades para administrar colecciones de elementos de descarga.                                                                                                    |
| [DownloadItem (objeto)](downloaditem-object.md)                                                                 | Proporciona métodos y propiedades relacionados con las solicitudes de descarga.                                                                                                              |
| [DownloadManager (objeto)](downloadmanager-object.md)                                                           | Proporciona métodos para administrar colecciones de descarga.                                                                                                                            |
| [Objeto externo para almacenes en línea de tipo 2](external-object-for-type-2-online-stores.md)                       | Proporciona propiedades, métodos y un evento accesible desde páginas web de la tienda en línea.                                                                                           |
| [Enumeraciones para almacenes en línea de tipo 2](enumerations-for-type-2-online-stores.md)                             | Describe las enumeraciones usadas por los almacenes en línea.                                                                                                                               |
| [Reproductor de Windows Media Convención de trabajo de BITS](windows-media-player-bits-job-convention.md)                       | Describe una convención para usar el Servicio de transferencia inteligente en segundo plano (BITS).                                                                                        |
| [Claves y entradas del Registro para un almacén en línea de tipo 2](registry-keys-and-entries-for-a-type-2-online-store.md) | Describe las entradas del Registro que debe crear un almacén en línea en el registro en el equipo del usuario.                                                                         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Tiendas en línea de tipo 2**](type-2-online-stores.md)
</dt> </dl>

 

 




