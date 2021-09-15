---
title: Método INapEnforcementClientConnection2 SetIsolationInfoEx (NapEnforcementClient.h)
description: NapAgent lo usa para establecer la información de aislamiento del cliente.
ms.assetid: 1b1a41a1-73a6-4c81-8366-15d06c67e228
keywords:
- Método NAP de SetIsolationInfoEx
- Método NAP de SetIsolationInfoEx , interfaz INapEnforcementClientConnection2
- INapEnforcementClientConnection2 interfaz NAP , Método SetIsolationInfoEx
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
ms.openlocfilehash: 711b4bfd27c3bd92d48a78f4767f5ed452b2d4f5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473788"
---
# <a name="inapenforcementclientconnection2setisolationinfoex-method"></a>Método INapEnforcementClientConnection2::SetIsolationInfoEx

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



 

## <a name="remarks"></a>Observaciones

NapAgent establece esta información después de procesar un [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) y el aplicador no debe establecer esta información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md)
</dt> </dl>

 

 





