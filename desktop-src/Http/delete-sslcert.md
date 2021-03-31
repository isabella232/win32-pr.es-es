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
# <a name="delete-sslcert"></a><span data-ttu-id="828d6-104">delete sslcert</span><span class="sxs-lookup"><span data-stu-id="828d6-104">delete sslcert</span></span>

<span data-ttu-id="828d6-105">Elimina los enlaces de certificado de servidor SSL y las directivas de certificado de cliente correspondientes para una dirección IP y un puerto.</span><span class="sxs-lookup"><span data-stu-id="828d6-105">Deletes SSL server certificate bindings and the corresponding client certificate policies for an IP address and port.</span></span>

``` syntax
delete sslcert [ipport=]IP Address:port
 
```

## <a name="parameters"></a><span data-ttu-id="828d6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="828d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="828d6-107"><span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>\**\[ipport = \] \* \* \* dirección IP: Puerto*</span><span class="sxs-lookup"><span data-stu-id="828d6-107"><span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>\**\[ipport=\]\*\*\*IP Address:port*</span></span>
</dt> <dd>

<span data-ttu-id="828d6-108">Especifica la dirección IPv4 o IPv6 y el puerto para el que se eliminarán los enlaces de certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="828d6-108">Specifies the IPv4 or IPv6 address and port for which the SSL certificate bindings will be deleted.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="828d6-109">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="828d6-109">Examples</span></span>

<span data-ttu-id="828d6-110">**delete sslcert ipport=1.1.1.1:443**</span><span class="sxs-lookup"><span data-stu-id="828d6-110">**delete sslcert ipport=1.1.1.1:443**</span></span>

<span data-ttu-id="828d6-111">**delete sslcert ipport=0.0.0.0:443**</span><span class="sxs-lookup"><span data-stu-id="828d6-111">**delete sslcert ipport=0.0.0.0:443**</span></span>

<span data-ttu-id="828d6-112">**Delete sslcert ipport = \[ ::: \] 443**</span><span class="sxs-lookup"><span data-stu-id="828d6-112">**delete sslcert ipport=\[::\]:443**</span></span>

 

 




