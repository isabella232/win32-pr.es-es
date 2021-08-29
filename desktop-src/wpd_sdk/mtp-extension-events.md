---
description: Eventos de extensión MTP
ms.assetid: c04554cd-d68d-455e-afa3-29d4186dad65
title: Eventos de extensión MTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a95999557e67ee8929fddc56dd7fd8eb43e6831af9f81f884303a2089bbe3fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806715"
---
# <a name="mtp-extension-events"></a>Eventos de extensión MTP

Los eventos notifican a una aplicación que se han producido cambios en un dispositivo o con él. Por ejemplo, una aplicación puede registrarse para recibir notificaciones de que se ha quitado un dispositivo.

## <a name="vendor-extended-event-codes"></a>Códigos de evento extendidos del proveedor

Cuando un fabricante de dispositivos admite un evento extendido por el proveedor, su controlador combina el código de evento del proveedor (UINT16) con los 16 bits más altos del GUID de EVENTOS EXTENDIDOS DEL PROVEEDOR MTP DE **WPD \_ EVENT \_ MTP. \_ \_ \_**

Por ejemplo, si el código extendido del proveedor 0xC001, el GUID resultante sería como se muestra en el ejemplo siguiente:


```C++
{C0010000-5738-4ff2-8445-BE3126691059}
```



## <a name="vendor-extended-event-parameters"></a>Parámetros de eventos extendidos del proveedor

Los parámetros de un evento extendido por el proveedor se notifican mediante el GUID de id. de evento del parámetro de evento WPD y el PARÁMETRO DE EVENTO **\_ \_ MTP \_ EXT \_ \_** DE PROPIEDAD DE **WPD, \_ \_ \_ \_** que es una colección de **PROPVARIANTS**. Estos **PROPVARIANTS corresponden** a los parámetros de evento. Si no hay parámetros, esta colección está vacía.


```C++
{C0010000-5738-4ff2-8445-BE3126691059}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compatibilidad con extensiones MTP](supporting-mtp-extensions.md)
</dt> </dl>

 

 



