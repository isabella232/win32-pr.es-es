---
title: add iplisten
description: Especifica una dirección IPv4 o IPv6 que se va a agregar a la lista de escucha de IP.
ms.assetid: 38253818-c029-4a46-ab52-095cbfdeeaf4
keywords:
- add iplisten HTTP
topic_type:
- apiref
api_name:
- add iplisten
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2133a3f590c46c9e27b518d7621c158b86895961acb07670f6603e03513d1cc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014983"
---
# <a name="add-iplisten"></a>add iplisten

Especifica una dirección IPv4 o IPv6 que se va a agregar a la lista de escucha de IP.

``` syntax
add iplisten [ ipaddress=] IPAddress
 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="__ipaddress___IPAddress"></span><span id="__ipaddress___ipaddress"></span><span id="__ipADDRESS___IPADDRESS"></span>**\[ ipaddress= \]** *IPAddress*
</dt> <dd>

Especifica la dirección IPv4 o IPv6 que se va a agregar a la lista de escucha de IP.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Agrega una nueva dirección IP a la lista de escucha de IP. No incluye el número de puerto. La lista de escucha de IP se utiliza para establecer el ámbito de la lista de direcciones a las que se enlaza el servicio HTTP. "0.0.0.0" significa cualquier dirección IPv4 y "::" significa cualquier dirección IPv6.

## <a name="examples"></a>Ejemplos

**add iplisten ipaddress=fe80::1**

**add iplisten ipaddress=1.1.1.1**

**add iplisten ipaddress=0.0.0.0**

**add iplisten ipaddress=::**

 

 




