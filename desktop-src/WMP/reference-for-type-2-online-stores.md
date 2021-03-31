---
title: Referencia de las tiendas en línea de tipo 2
description: Referencia de las tiendas en línea de tipo 2
ms.assetid: b3f580cc-b02d-4312-a7a1-a35778a222bc
keywords:
- Windows Media Player tiendas en línea, referencia
- tiendas en línea, referencia
- tipo 2 tiendas en línea, referencia
- referencia de las tiendas en línea de tipo 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c164ad74481030a52cd31605b29833d3bfbd3f1d
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2020
ms.locfileid: "103789291"
---
# <a name="reference-for-type-2-online-stores"></a>Referencia de las tiendas en línea de tipo 2

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

Windows Media Player 10 o posterior proporciona objetos, interfaces, propiedades y métodos que admiten las tiendas en línea de tipo 2. En las secciones siguientes se documentan en detalle.



| Sección                                                                                                        | Descripción                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Interfaz IWMPSubscriptionService](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice)                                               | Proporciona métodos para aumentar la administración de derechos digitales (DRM) e iniciar procesos en segundo plano.                                                                              |
| [Interfaz IWMPSubscriptionService2](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2)                                             | Proporciona métodos para iniciar procesos en segundo plano, proporcionar información sobre la actividad de la tienda en línea y proporcionar un puntero a la interfaz principal de Windows Media Player. |
| [Interfaz IWMPSubscriptionServiceCallback](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservicecallback)                               | Define un método que las tiendas en línea usan para notificar a Windows Media Player cuando se completa un proceso en segundo plano.                                                              |
| [WMPNotifySubscriptionPluginAddRemove](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-wmpnotifysubscriptionpluginaddremove)                               | Función que se usa para notificar a Windows Media Player que se ha instalado o desinstalado un complemento.                                                                            |
| [Objeto DownloadCollection](downloadcollection-object.md)                                                     | Proporciona métodos y propiedades para administrar colecciones de elementos de descarga.                                                                                                    |
| [Objeto DownloadItem](downloaditem-object.md)                                                                 | Proporciona métodos y propiedades relacionados con las solicitudes de descarga.                                                                                                              |
| [Objeto DownloadManager](downloadmanager-object.md)                                                           | Proporciona métodos para administrar colecciones de descargas.                                                                                                                            |
| [Objeto externo para las tiendas en línea de tipo 2](external-object-for-type-2-online-stores.md)                       | Proporciona propiedades, métodos y un evento accesible desde páginas web de la tienda en línea.                                                                                           |
| [Enumeraciones de las tiendas en línea de tipo 2](enumerations-for-type-2-online-stores.md)                             | Describe las enumeraciones usadas por las tiendas en línea.                                                                                                                               |
| [Convención de trabajo de Windows Media Player BITS](windows-media-player-bits-job-convention.md)                       | Describe una Convención para usar el Servicio de transferencia inteligente en segundo plano (BITS).                                                                                        |
| [Claves del registro y entradas para una tienda en línea de tipo 2](registry-keys-and-entries-for-a-type-2-online-store.md) | Describe las entradas del registro que una tienda en línea debe crear en el registro del equipo del usuario.                                                                         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Tipo 2 tiendas en línea**](type-2-online-stores.md)
</dt> </dl>

 

 




