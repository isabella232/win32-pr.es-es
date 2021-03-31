---
title: delete sslcert
description: Elimina los enlaces de certificado de servidor SSL y las directivas de certificado de cliente correspondientes para una dirección IP y un puerto.
ms.assetid: 2adea7a8-f31f-4c02-8279-7d452e36cd9b
keywords:
- eliminar sslcert HTTP
topic_type:
- apiref
api_name:
- delete sslcert
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7672df5eee1634c41ff153435edcbecc58c2595
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2019
ms.locfileid: "103784540"
---
# <a name="delete-sslcert"></a>delete sslcert

Elimina los enlaces de certificado de servidor SSL y las directivas de certificado de cliente correspondientes para una dirección IP y un puerto.

``` syntax
delete sslcert [ipport=]IP Address:port
 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>**\[ipport = \] * * * dirección IP: Puerto*
</dt> <dd>

Especifica la dirección IPv4 o IPv6 y el puerto para el que se eliminarán los enlaces de certificado SSL.

</dd> </dl>

## <a name="examples"></a>Ejemplos

**delete sslcert ipport=1.1.1.1:443**

**delete sslcert ipport=0.0.0.0:443**

**Delete sslcert ipport = \[ ::: \] 443**

 

 




