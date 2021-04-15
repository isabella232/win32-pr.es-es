---
title: Tiendas en línea exclusivas
description: Tiendas en línea exclusivas
ms.assetid: f2b7f9a7-2299-48f4-b915-2c1a5e0d68bb
keywords:
- Windows Media Player tiendas en línea, exclusivas
- tiendas en línea, exclusivas
- tipo 1 tiendas en línea, exclusivas
- tipo 2 tiendas en línea, exclusivas
- tiendas en línea exclusivas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f408a0ada0de46d637537ffccd3ec162da04e8ce
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105695532"
---
# <a name="exclusive-online-stores"></a>Tiendas en línea exclusivas

Con Windows Media Player 11, una aplicación que incrusta el control del reproductor de forma remota puede especificar una tienda en línea exclusiva. En ese caso, el selector de servicio de Windows Media Player está deshabilitado y solo la tienda en línea especificada está disponible para el usuario. Además, Windows Media Player adopta el color especificado por el elemento **color** del documento ServiceInfo de la tienda en línea exclusiva.

Para especificar una tienda en línea exclusiva, una aplicación debe anexar ExclusiveService:*keyName* al final de la cadena que devuelve de [IWMPRemoteMediaServices:: GetServiceType](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getservicetype). Por ejemplo, supongamos que Proseware es el nombre de clave que se asigna a una tienda en línea determinada. Si **GetServiceType** devuelve la cadena "Remote ExclusiveService: Proseware", Proseware será la única tienda en línea disponible en el control Player Embedded de forma remota.

Una aplicación puede limitar el Media Player de Windows a una tienda en línea exclusiva solo si Windows Media Player no se está ejecutando cuando se inicia la aplicación. Es responsabilidad de la aplicación informar al usuario de que debe cerrar Windows Media Player antes de ejecutar la aplicación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Información común para las tiendas en línea de tipo 1 y 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Control remoto del Reproductor de Windows Media**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 




