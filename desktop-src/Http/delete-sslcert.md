---
title: delete sslcert
description: Elimina los enlaces de certificado de servidor SSL y las directivas de certificado de cliente correspondientes para una dirección IP y un puerto.
ms.assetid: 2adea7a8-f31f-4c02-8279-7d452e36cd9b
keywords:
- delete sslcert HTTP
topic_type:
- apiref
api_name:
- delete sslcert
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a45d811bedfa1d2a228cd29decf2272d85b8ca6de5c1d27656b3e37b8d6b4d4e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870545"
---
# <a name="delete-sslcert"></a>delete sslcert

Elimina los enlaces de certificado de servidor SSL y las directivas de certificado de cliente correspondientes para una dirección IP y un puerto.

``` syntax
delete sslcert [ipport=]IP Address:port
 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>**\[ ipport= \]**_Dirección IP:puerto_
</dt> <dd>

Especifica la dirección y el puerto IPv4 o IPv6 para los que se eliminarán los enlaces de certificado SSL.

</dd> </dl>

## <a name="examples"></a>Ejemplos

**delete sslcert ipport=1.1.1.1:443**

**delete sslcert ipport=0.0.0.0:443**

**delete sslcert ipport= \[ :: \] :443**

 

 




