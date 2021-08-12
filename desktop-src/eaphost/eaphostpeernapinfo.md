---
title: Estructura EapHostPeerNapInfo (Eaphostpeerapis.h)
description: Contiene la información de Protección de acceso a redes (NAP) en un suplicante eap.
ms.assetid: 703eda56-5932-44d5-ae7f-0a6328d82237
keywords:
- EapHostPeerNapInfo (estructura EAPHost)
topic_type:
- apiref
api_name:
- EapHostPeerNapInfo
api_location:
- eaphostpeerapis.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5fe91c88f633f2e42599938e45e1291c90f1ec9c08559a84f132f3af9269de39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118274549"
---
# <a name="eaphostpeernapinfo-structure"></a>EapHostPeerNapInfo (estructura)

La **estructura EapHostPeerNapInfo** contiene la información de Protección de acceso a redes (NAP) sobre un suplicante de EAP.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _tagEapHostPeerNapInfo {
  ISOLATION_STATE isolationState;
  ProbationTime   probationTime;
  UINT32          stringCorrelationIdLength;
} EapHostPeerNapInfo;
```



## <a name="members"></a>Miembros

<dl> <dt>

**isolationState**
</dt> <dd>

Estructura [**ISOLATION \_ STATE**](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-isolation_state) que especifica el estado de aislamiento nap de un equipo. El estado de aislamiento determina el nivel de acceso de red concedido.

</dd> <dt>

**probationTime**
</dt> <dd>

Estructura **ProbationTime** que especifica el tiempo necesario para que la conexión salga de la cuarentena después de la cual se descartará la conexión. Una **estructura ProbationTime** es idéntica a una [estructura FILETIME.](/windows/win32/api/minwinbase/ns-minwinbase-filetime)

</dd> <dt>

**stringCorrelationIdLength**
</dt> <dd>

Longitud, en bytes, de la cadena [NAPCorrelationId](/windows/desktop/NAP/nap-datatypes) que sigue a esta estructura.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **estructura EapHostPeerNapInfo** precede a la cadena [NAPCorrelationId](/windows/desktop/NAP/nap-datatypes) del tipo de datos **WCHAR** en el flujo de bytes RPC.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                                   |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                      |
| Header<br/>                   | <dl> <dt>Eaphostpeerapis.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras suplicantes de EAPHost](eap-host-supplicant-structures.md)
</dt> <dt>

[**EapHostPeerGetAuthStatus**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetauthstatus)
</dt> <dt>

[**EapHostPeerMethodAuthParams**](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerauthparams)
</dt> </dl>

 

