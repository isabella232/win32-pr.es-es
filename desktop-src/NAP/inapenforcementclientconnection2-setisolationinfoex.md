---
title: Método INapEnforcementClientConnection2 SetIsolationInfoEx (NapEnforcementClient.h)
description: NapAgent lo usa para establecer la información de aislamiento del cliente.
ms.assetid: 1b1a41a1-73a6-4c81-8366-15d06c67e228
keywords:
- Método NAP de SetIsolationInfoEx
- Método NAP de SetIsolationInfoEx, interfaz INapEnforcementClientConnection2
- INapEnforcementClientConnection2 interface NAP , SetIsolationInfoEx method
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2.SetIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f86a678cce54a9872f8f3c059da3b3055f891160b042241769712b4424250690
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626205"
---
# <a name="inapenforcementclientconnection2setisolationinfoex-method"></a>INapEnforcementClientConnection2::SetIsolationInfoEx (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

NapAgent usa el método **INapEnforcementClientConnection2::SetIsolationInfoEx** para establecer la información de aislamiento del cliente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetIsolationInfoEx(
  [in] const IsolationInfoEx *isolationInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*isolationInfo* \[ En\]
</dt> <dd>

Puntero a una [**estructura IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) que contiene el estado de conectividad del cliente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>           | Operación realizada correctamente.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | El límite de recursos del sistema no pudo realizar la operación.<br/> |



 

## <a name="remarks"></a>Comentarios

NapAgent establece esta información después de procesar un [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) y el ejecutor no debe establecer esta información.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md)
</dt> </dl>

 

 





