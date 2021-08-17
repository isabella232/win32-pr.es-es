---
title: Identificadores de contexto de proveedor integrados (Fwpmu.h)
description: Los contextos de proveedor integrados identifican las directivas predeterminadas que se usarán con sockets seguros.
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
ms.openlocfilehash: c0247b58b38de55eb67479c68e0c0955fb9d2a56a793215330366ca8ccfbe4e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951334"
---
# <a name="built-in-provider-context-identifiers"></a>Identificadores de contexto de proveedor integrados

Los identificadores de los contextos de proveedor integrados en Windows Filtering Platform (WFP) se representan mediante un GUID. Estos contextos de proveedor integrados identifican las directivas predeterminadas que se usarán con sockets seguros.

Estos identificadores se definen de la manera siguiente.

<dl> <dt>

<span id="FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_AUTHIP"></span><span id="fwpm_provider_context_secure_socket_authip"></span>**FWPM \_ PROVIDER \_ CONTEXT \_ SECURE \_ SOCKET \_ AUTHIP**
</dt> <dd> <dl> <dt>



protocolo de Internet autenticado directiva predeterminada del modo principal (AuthIP) para sockets seguros.


</dt> </dl> </dd> <dt>

<span id="FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_IPSEC"></span><span id="fwpm_provider_context_secure_socket_ipsec"></span>**IPSEC DE SOCKET SEGURO DE CONTEXTO \_ \_ DE PROVEEDOR \_ \_ \_ FWPM**
</dt> <dd> <dl> <dt>



Directiva predeterminada del modo rápido de seguridad de protocolos de Internet (IPsec) para sockets seguros.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Fwpmu.h</dt> </dl> |



 

 





