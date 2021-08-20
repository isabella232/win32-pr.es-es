---
title: delete iplisten
description: Especifica una dirección IPv4 o IPv6 que se va a eliminar de la lista de escucha de IP.
ms.assetid: 1d0935a5-77de-4fdf-8d3b-88c8578bd5c7
keywords:
- delete iplisten HTTP
topic_type:
- apiref
api_name:
- delete iplisten
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42dbe9716ae19fdbbfb8f147b0f5f7f5a592adbf7b241c2f4e4548e0ee7e6e7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014873"
---
# <a name="delete-iplisten"></a>delete iplisten

Especifica una dirección IPv4 o IPv6 que se va a eliminar de la lista de escucha de IP.

``` syntax
delete iplisten [ address=] IPAddress
 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="_address___IPAddress"></span><span id="_address___ipaddress"></span><span id="_ADDRESS___IPADDRESS"></span>**\[ address= \]** *IPAddress*
</dt> <dd>

Especifica la dirección IPv4 o IPv6 que se va a eliminar de la lista de escucha de IP.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Elimina una dirección IP en la lista de escucha de IP. No incluye el número de puerto. La lista de escucha de IP se utiliza para establecer el ámbito de la lista de direcciones a las que se enlaza el servicio HTTP. "0.0.0.0" significa cualquier dirección IPv4 y "::" significa cualquier dirección IPv6.

## <a name="examples"></a>Ejemplos

**delete iplisten address=fe80::1**

**delete iplisten address=1.1.1.1**

**delete iplisten address=0.0.0.0**

**delete iplisten address=::**

 

 




