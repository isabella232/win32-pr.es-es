---
title: Método INapClientManagement2 GetSystemIsolationInfoEx (NapManagement.h)
description: Recupera información sobre el estado de aislamiento y el estado de aislamiento extendido de NapClient.
ms.assetid: 614bcf19-873e-4043-98b2-dcb152bae3e2
keywords:
- Método NAP de GetSystemIsolationInfoEx
- Método NAP de GetSystemIsolationInfoEx, interfaz INapClientManagement2
- Nap de interfaz INapClientManagement2, método GetSystemIsolationInfoEx
topic_type:
- apiref
api_name:
- INapClientManagement2.GetSystemIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d03630cbd0647dc177460f92abc28e6aa66cbb663465ba7e9e93eefbc283ac00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118621932"
---
# <a name="inapclientmanagement2getsystemisolationinfoex-method"></a>Método INapClientManagement2::GetSystemIsolationInfoEx

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El **método GetSystemIsolationInfoEx** recupera información sobre el estado de aislamiento y el estado de aislamiento extendido de NapClient.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetSystemIsolationInfoEx(
  [out] IsolationInfoEx **isolationInfo,
  [out] BOOL            *unknownConnections
) const;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*isolationInfo* \[ out\]
</dt> <dd>

Puntero a un puntero a una [**estructura IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) que contiene información de estado de aislamiento.

</dd> <dt>

*unknownConnections* \[ out\]
</dt> <dd>

Puntero a un bool que es **TRUE** si alguna de las conexiones está en un estado desconocido y **FALSE en** caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un código de estado HRESULT que incluye, entre otros, uno de los siguientes.



| Código devuelto                                                                                         | Descripción                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | Operación correcta.<br/>                                   |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>      | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>       | El límite de recursos del sistema no pudo realizar la operación.<br/> |
| <dl> <dt>**RPC \_ E \_ DESCONECTADO**</dt> </dl> | NapAgent no se está ejecutando.<br/>                            |



 

## <a name="remarks"></a>Observaciones

La información de aislamiento que se recupera no refleja estados desconocidos.

Sha debe liberar la estructura [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) llamando [**a FreeIsolationInfoEx.**](freeisolationinfoex.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                         |
| Header<br/>                   | <dl> <dt>NapManagement.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapManagement.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapClientManagement2**](inapclientmanagement2.md)
</dt> </dl>

 

 





