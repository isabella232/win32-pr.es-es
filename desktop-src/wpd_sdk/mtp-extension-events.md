---
description: Eventos de extensión MTP
ms.assetid: c04554cd-d68d-455e-afa3-29d4186dad65
title: Eventos de extensión MTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10389df9105615befa9ba0f32824615977cc3cb7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572108"
---
# <a name="mtp-extension-events"></a>Eventos de extensión MTP

Los eventos notifican a una aplicación que se han producido cambios en un dispositivo o con él. Por ejemplo, una aplicación puede registrarse para recibir notificaciones de que se ha quitado un dispositivo.

## <a name="vendor-extended-event-codes"></a>Códigos de evento extendidos por el proveedor

Cuando un fabricante de dispositivos admite un evento extendido por el proveedor, su controlador combina el código de evento del proveedor (UINT16) con los 16 bits más altos del GUID de eventos extendidos de **WPD \_ EVENT \_ MTP \_ VENDOR. \_ \_**

Por ejemplo, si el código extendido por el proveedor es 0xC001, el GUID resultante sería como se muestra en el ejemplo siguiente:


```C++
{C0010000-5738-4ff2-8445-BE3126691059}
```



## <a name="vendor-extended-event-parameters"></a>Parámetros de eventos extendidos por el proveedor

Los parámetros de un evento extendido por el proveedor se notifican mediante el GUID del identificador de EVENTO del PARÁMETRO DE EVENTO WPD y el PARÁMETRO DE EVENTOS **MTP EXT DE WPD \_ \_ PROPERTY, \_ \_ \_** que es una colección de **PROPVARIANTS**. **\_ \_ \_ \_** Estos **PROPVARIANTS corresponden** a los parámetros de evento. Si no hay parámetros, esta colección está vacía.


```C++
{C0010000-5738-4ff2-8445-BE3126691059}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compatibilidad con extensiones de MTP](supporting-mtp-extensions.md)
</dt> </dl>

 

 



