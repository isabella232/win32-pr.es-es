---
title: Tiendas en línea exclusivas
description: Tiendas en línea exclusivas
ms.assetid: f2b7f9a7-2299-48f4-b915-2c1a5e0d68bb
keywords:
- Reproductor de Windows Media en línea, exclusivo
- tiendas en línea, exclusivas
- tiendas en línea de tipo 1, exclusiva
- tiendas en línea de tipo 2, exclusiva
- tiendas en línea exclusivas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d199c47a201743ca56f9f9f199b5202bbdbe5fb320628afc5052b0ca8b969c24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650095"
---
# <a name="exclusive-online-stores"></a>Tiendas en línea exclusivas

Con Reproductor de Windows Media 11, una aplicación que inserta el control Player de forma remota puede especificar una tienda en línea exclusiva. En ese caso, el selector de servicio de Reproductor de Windows Media está deshabilitado y solo el usuario tiene disponible la tienda en línea especificada. Además, Reproductor de Windows Media adopta el color especificado por el **elemento Color** del documento ServiceInfo de la tienda en línea exclusiva.

Para especificar un almacén en línea exclusivo, una aplicación debe anexar ExclusiveService:*keyname* al final de la cadena que devuelve de [IWMPRemoteMediaServices::GetServiceType](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getservicetype). Por ejemplo, suponga que Proseware es el nombre de clave dado a una tienda en línea determinada. Si **GetServiceType** devuelve la cadena "Remote ExclusiveService:Proseware", Proseware será la única tienda en línea disponible en el control Player insertado de forma remota.

Una aplicación puede limitar Reproductor de Windows Media a una tienda en línea exclusiva solo si Reproductor de Windows Media no se está ejecutando cuando se inicia la aplicación. Es responsabilidad de la aplicación informar al usuario de que debe cerrar Reproductor de Windows Media antes de ejecutar la aplicación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Información común a las tiendas en línea de tipo 1 y tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Control remoto del Reproductor de Windows Media**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 




