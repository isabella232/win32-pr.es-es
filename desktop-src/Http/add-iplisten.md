---
title: add iplisten
description: Especifica una dirección IPv4 o IPv6 que se va a agregar a la lista de escucha de IP.
ms.assetid: 38253818-c029-4a46-ab52-095cbfdeeaf4
keywords:
- Agregar iplisten HTTP
topic_type:
- apiref
api_name:
- add iplisten
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6090d3044be134035edb5f1f42a9790859d0301d
ms.sourcegitcommit: 243954e695c6ab5372b2935b095c3cd0b1202e16
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/04/2020
ms.locfileid: "103994999"
---
# <a name="add-iplisten"></a>add iplisten

Especifica una dirección IPv4 o IPv6 que se va a agregar a la lista de escucha de IP.

``` syntax
add iplisten [ ipaddress=] IPAddress
 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="__ipaddress___IPAddress"></span><span id="__ipaddress___ipaddress"></span><span id="__ipADDRESS___IPADDRESS"></span>**\[ IPAddress = \]** *IPAddress*
</dt> <dd>

Especifica la dirección IPv4 o IPv6 que se va a agregar a la lista de escucha de IP.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Agrega una nueva dirección IP a la lista de escucha de IP. No incluye el número de puerto. La lista de escucha de IP se utiliza para establecer el ámbito de la lista de direcciones a las que se enlaza el servicio HTTP. "0.0.0.0" significa cualquier dirección IPv4 y "::" significa cualquier dirección IPv6.

## <a name="examples"></a>Ejemplos

**add iplisten ipaddress=fe80::1**

**add iplisten ipaddress=1.1.1.1**

**add iplisten ipaddress=0.0.0.0**

**add iplisten ipaddress=::**

 

 




