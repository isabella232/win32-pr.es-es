---
title: Estructura EapHostPeerNapInfo (Eaphostpeerapis. h)
description: Contiene la información de protección de acceso a redes (NAP) de un suplicante EAP.
ms.assetid: 703eda56-5932-44d5-ae7f-0a6328d82237
keywords:
- EapHostPeerNapInfo estructura EAPHost
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
ms.openlocfilehash: 3221f40dea9e84e410a1a643bbbcdc94e9039b21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079688"
---
# <a name="eaphostpeernapinfo-structure"></a>Estructura EapHostPeerNapInfo

La estructura **EapHostPeerNapInfo** contiene la información de protección de acceso a redes (NAP) de un suplicante EAP.

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

Una estructura de [**\_ Estado de aislamiento**](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-isolation_state) que especifica el estado de aislamiento de NAP de un equipo. El estado de aislamiento determina el nivel de acceso a la red concedido.

</dd> <dt>

**probationTime**
</dt> <dd>

Estructura **ProbationTime** que especifica el tiempo necesario para que la conexión salga de la cuarentena después de la cual se quitará la conexión. Una estructura **ProbationTime** es idéntica a una estructura [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) .

</dd> <dt>

**stringCorrelationIdLength**
</dt> <dd>

La longitud, en bytes, del [STRINGCORRELATIONID](/windows/desktop/NAP/nap-datatypes) NAP que sigue a esta estructura.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La estructura **EapHostPeerNapInfo** precede a la [stringCorrelationId](/windows/desktop/NAP/nap-datatypes) NAP del tipo de datos **WCHAR** en el flujo de bytes RPC.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                   |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                      |
| Encabezado<br/>                   | <dl> <dt>Eaphostpeerapis. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de suplicante de EAPHost](eap-host-supplicant-structures.md)
</dt> <dt>

[**EapHostPeerGetAuthStatus**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetauthstatus)
</dt> <dt>

[**EapHostPeerMethodAuthParams**](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerauthparams)
</dt> </dl>

 

