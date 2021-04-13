---
title: show sslcert
description: Enumera los enlaces de certificados de servidor SSL y las directivas de certificado de cliente correspondientes para una dirección IP y un puerto.
ms.assetid: 8e20f55e-a357-4f9c-a24e-e234607c3196
keywords:
- Mostrar sslcert HTTP
topic_type:
- apiref
api_name:
- show sslcert
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b71c2faf370066f5ce8d5ce6a20b173a74d0f645
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2019
ms.locfileid: "104358368"
---
# <a name="show-sslcert"></a>show sslcert

Enumera los enlaces de certificados de servidor SSL y las directivas de certificado de cliente correspondientes para una dirección IP y un puerto.

``` syntax
show sslcert [ipport=]IP Address:port
 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>**\[ipport = \] * * * dirección IP: Puerto*
</dt> <dd>

Especifica la dirección IPv4 o IPv6 y el puerto para el que se mostrarán los enlaces de certificado SSL. Si no se especifica un ipport, se enumeran todos los enlaces.

</dd> </dl>

## <a name="examples"></a>Ejemplos

**Show sslcert ipport = \[ fe80:: 1 \] : 443**

**show sslcert ipport=1.1.1.1:443**

**show sslcert ipport=0.0.0.0:443**

**Mostrar sslcert ipport = \[ ::: \] 443**

 

 




