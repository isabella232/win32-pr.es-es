---
title: Identificadores de contexto de proveedor integrados (Fwpmu. h)
description: Los contextos de proveedor integrados identifican las directivas predeterminadas que se usarán con los sockets seguros.
ms.assetid: 439a5abc-08ac-4514-a126-d738e5311003
topic_type:
- apiref
api_name:
- FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_AUTHIP
- FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_IPSEC
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 942ed1d21d2acd46f0dc6b303049e0936e3cf63d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104488998"
---
# <a name="built-in-provider-context-identifiers"></a>Identificadores de contexto de proveedor integrados

Los identificadores de los contextos de proveedor integrados en la plataforma de filtrado de Windows (WFP) se representan mediante un GUID. Estos contextos de proveedor integrados identifican las directivas predeterminadas que se usarán con los sockets seguros.

Estos identificadores se definen como se indica a continuación.

<dl> <dt>

<span id="FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_AUTHIP"></span><span id="fwpm_provider_context_secure_socket_authip"></span>**\_proveedor de \_ \_ \_ sockets seguros \_ AUTHIP de contexto de proveedor FWPM**
</dt> <dd> <dl> <dt>



Directiva predeterminada de modo principal de protocolo de Internet autenticado (AuthIP) para sockets seguros.


</dt> </dl> </dd> <dt>

<span id="FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_IPSEC"></span><span id="fwpm_provider_context_secure_socket_ipsec"></span>**\_contexto de proveedor \_ seguro de \_ \_ sockets seguros \_ IPSec de FWPM**
</dt> <dd> <dl> <dt>



Directiva predeterminada de modo rápido del Protocolo de seguridad de Internet (IPsec) para sockets seguros.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Fwpmu. h</dt> </dl> |



 

 





