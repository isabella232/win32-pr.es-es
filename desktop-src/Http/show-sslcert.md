---
title: show sslcert
description: Enumera los enlaces de certificado de servidor SSL y las directivas de certificado de cliente correspondientes para una dirección IP y un puerto.
ms.assetid: 8e20f55e-a357-4f9c-a24e-e234607c3196
keywords:
- show sslcert HTTP
topic_type:
- apiref
api_name:
- show sslcert
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18c624354d33826efa40c0969f1239e4029d03ab51412a77a3bf8acce97e0e66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117995936"
---
# <a name="show-sslcert"></a>show sslcert

Enumera los enlaces de certificado de servidor SSL y las directivas de certificado de cliente correspondientes para una dirección IP y un puerto.

``` syntax
show sslcert [ipport=]IP Address:port
 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>**\[ ipport= \]**_Dirección IP:puerto_
</dt> <dd>

Especifica la dirección iPv4 o IPv6 y el puerto para el que se mostrarán los enlaces de certificado SSL. Si no se especifica un ipport, se enumeran todos los enlaces.

</dd> </dl>

## <a name="examples"></a>Ejemplos

**show sslcert ipport= \[ fe80::1 \] :443**

**show sslcert ipport=1.1.1.1:443**

**show sslcert ipport=0.0.0.0:443**

**show sslcert ipport= \[ :: \] :443**

 

 




