---
description: Eventos de extensión MTP
ms.assetid: c04554cd-d68d-455e-afa3-29d4186dad65
title: Eventos de extensión MTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10389df9105615befa9ba0f32824615977cc3cb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720748"
---
# <a name="mtp-extension-events"></a>Eventos de extensión MTP

Los eventos notifican a una aplicación que se han producido cambios en un dispositivo o con él. Por ejemplo, una aplicación puede registrarse para recibir notfications de que se ha quitado un dispositivo.

## <a name="vendor-extended-event-codes"></a>Códigos de eventos extendidos de proveedor

Cuando un fabricante de dispositivos admite un evento extendido de proveedor, el controlador combina el código de evento del proveedor (UINT16) con los 16 bits más altos del GUID de **\_ \_ \_ \_ \_ eventos extendidos del evento de WPD** .

Por ejemplo, si el código extendido del proveedor es 0xC001, el GUID resultante sería como se muestra en el ejemplo siguiente:


```C++
{C0010000-5738-4ff2-8445-BE3126691059}
```



## <a name="vendor-extended-event-parameters"></a>Parámetros de eventos extendidos de proveedor

Los parámetros de un evento extendido de proveedor se indican mediante el **\_ identificador de \_ \_ evento del \_ parámetro de evento WPD** GUID y la propiedad de WPD parámetros de **\_ \_ \_ \_ evento ext ext \_**, que es una colección de **PROPVARIANTS**. Estos **PROPVARIANTS** se corresponden con los parámetros de evento. Si no hay ningún parámetro, esta colección está vacía.


```C++
{C0010000-5738-4ff2-8445-BE3126691059}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compatibilidad con extensiones MTP](supporting-mtp-extensions.md)
</dt> </dl>

 

 



