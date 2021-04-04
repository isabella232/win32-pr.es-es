---
title: delete iplisten
description: Especifica una dirección IPv4 o IPv6 que se va a eliminar de la lista de escucha de IP.
ms.assetid: 1d0935a5-77de-4fdf-8d3b-88c8578bd5c7
keywords:
- eliminar iplisten HTTP
topic_type:
- apiref
api_name:
- delete iplisten
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ed7356d8dea3b4313a46c7d7906de15b7389edc
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2019
ms.locfileid: "104076977"
---
# <a name="delete-iplisten"></a>delete iplisten

Especifica una dirección IPv4 o IPv6 que se va a eliminar de la lista de escucha de IP.

``` syntax
delete iplisten [ address=] IPAddress
 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="_address___IPAddress"></span><span id="_address___ipaddress"></span><span id="_ADDRESS___IPADDRESS"></span>**\[ Address = \]** *IPAddress*
</dt> <dd>

Especifica la dirección IPv4 o IPv6 que se va a eliminar de la lista de escucha de IP.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Elimina una dirección IP de la lista de escucha de IP. No incluye el número de puerto. La lista de escucha de IP se utiliza para establecer el ámbito de la lista de direcciones a las que se enlaza el servicio HTTP. "0.0.0.0" significa cualquier dirección IPv4 y "::" significa cualquier dirección IPv6.

## <a name="examples"></a>Ejemplos

**eliminar dirección iplisten = fe80:: 1**

**Delete iplisten Address = pág**

**eliminar dirección iplisten = 0.0.0.0**

**eliminar dirección iplisten =::**

 

 




