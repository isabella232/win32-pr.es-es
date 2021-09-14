---
title: Método INapSystemHealthAgentBinding2 GetSystemIsolationInfoEx (NapSystemHealthAgent.h)
description: Las SHA llaman a para determinar el estado de aislamiento del sistema y el estado de aislamiento extendido.
ms.assetid: 237e5539-889c-457d-8db0-bf3379f28b85
keywords:
- Método NAP de GetSystemIsolationInfoEx
- Método NAP de GetSystemIsolationInfoEx, interfaz INapSystemHealthAgentBinding2
- INapSystemHealthAgentBinding2 interface NAP , Método GetSystemIsolationInfoEx
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding2.GetSystemIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2643d62afba1a35ebd96b8b39ea2fcf90397576
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071651"
---
# <a name="inapsystemhealthagentbinding2getsystemisolationinfoex-method"></a>Método INapSystemHealthAgentBinding2::GetSystemIsolationInfoEx

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Los SHA llaman al método **INapSystemHealthAgentBinding2::GetSystemIsolationInfoEx** para determinar el estado de aislamiento del sistema y el estado de aislamiento extendido.

> [!Note]  
> Use [**INapSystemHealthAgentBinding::GetSystemIsolationInfo**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md) para determinar solo el estado de aislamiento del sistema.

 

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

Puntero a un puntero a una estructura [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) que contiene el estado de aislamiento extendido del sistema para las conexiones conocidas. *isolationInfo* indica si el sistema está en un estado de acceso restringido, sondeo o acceso sin restricciones, así como la [**información de ExtendedIsolationState.**](/windows/win32/api/naptypes/ne-naptypes-extendedisolationstate)

</dd> <dt>

*unknownConnections* \[ out\]
</dt> <dd>

Puntero a un **valor BOOL que** es **TRUE** si alguna conexión está en un estado desconocido y **FALSE en** caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                             | Descripción                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>                   | Operación realizada correctamente.<br/>                                                                                                |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>         | Error de permisos, acceso denegado.<br/>                                                                                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | El límite de recursos del sistema no pudo realizar la operación.<br/>                                                             |
| <dl> <dt>**NAP \_ E \_ NO \_ INICIALIZADO**</dt> </dl> | El SHA no se ha inicializado previamente.<br/>                                                                        |
| <dl> <dt>**RPC \_ E \_ DESCONECTADO**</dt> </dl>     | NapAgent se ha detenido. Este objeto se recuperará automáticamente y se volverá a conectar a NapAgent, una vez que se reinicie.<br/> |



 

## <a name="remarks"></a>Observaciones

Sha debe liberar la estructura [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) llamando [**a FreeIsolationInfoEx.**](freeisolationinfoex.md)

Sha debe llamar a [**Initialize antes**](inapsystemhealthagentbinding-initialize-method.md) de llamar a este método o a cualquier otro método de la [**interfaz INapSystemHealthAgentBinding2.**](inapsystemhealthagentbinding2.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md)
</dt> </dl>

 

 





