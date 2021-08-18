---
title: Método INapSystemHealthAgentBinding GetSystemIsolationInfo (NapSystemHealthAgent.h)
description: Las SHA llaman a para determinar el estado de aislamiento del sistema.
ms.assetid: 0401a846-0da2-4975-87bc-3e9fe8b5b67d
keywords:
- Método NAP GetSystemIsolationInfo
- Método NAP de GetSystemIsolationInfo , interfaz INapSystemHealthAgentBinding
- INapSystemHealthAgentBinding (método NAP de la interfaz INapSystemHealthAgentBinding), método GetSystemIsolationInfo
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.GetSystemIsolationInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9058b78bcff60b27bb27f25f11b785a8cd341f9addafe1829c1e8a7f3fb02a15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939562"
---
# <a name="inapsystemhealthagentbindinggetsystemisolationinfo-method"></a>Método INapSystemHealthAgentBinding::GetSystemIsolationInfo

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Las SHA llaman al método **INapSystemHealthAgentBinding::GetSystemIsolationInfo** para determinar el estado de aislamiento del sistema.

> [!Note]  
> Use [**INapSystemHealthAgentBinding2::GetSystemIsolationInfoEx**](inapsystemhealthagentbinding2-getsystemisolationinfoex.md) para determinar el estado de aislamiento extendido del sistema.

 

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetSystemIsolationInfo(
  [out] IsolationInfo **isolationInfo,
  [out] BOOL          *unknownConnections
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*isolationInfo* \[ out\]
</dt> <dd>

Puntero a un puntero a una estructura [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) que contiene el estado de aislamiento del sistema para las conexiones conocidas. *isolationInfoindica si* el sistema está en un estado de acceso restringido, sondeo o acceso sin restricciones.

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



 

## <a name="remarks"></a>Comentarios

Sha debe llamar a [**Initialize antes**](inapsystemhealthagentbinding-initialize-method.md) de llamar a este método o a cualquier otro método de la [**interfaz INapSystemHealthAgentBinding2.**](inapsystemhealthagentbinding2.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





