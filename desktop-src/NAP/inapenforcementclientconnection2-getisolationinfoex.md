---
title: Método INapEnforcementClientConnection2 GetIsolationInfoEx (NapEnforcementClient. h)
description: Se usa para obtener información de aislamiento sobre el cliente.
ms.assetid: ebacd056-5ab8-4096-821c-8f2987d853c4
keywords:
- Método GetIsolationInfoEx NAP
- Método GetIsolationInfoEx NAP, interfaz INapEnforcementClientConnection2
- Interfaz INapEnforcementClientConnection2 NAP, método GetIsolationInfoEx
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2.GetIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6586dd5fc277e62d4478e685f49ac132e744bcc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493240"
---
# <a name="inapenforcementclientconnection2getisolationinfoex-method"></a>INapEnforcementClientConnection2:: GetIsolationInfoEx (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El método **INapEnforcementClientConnection2:: GetIsolationInfoEx** se usa para obtener información de aislamiento sobre el cliente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetIsolationInfoEx(
  [out] IsolationInfoEx **isolationInfo
) const;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*isolationInfo* \[ enuncia\]
</dt> <dd>

Un puntero a un puntero a una estructura [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) que contiene la información de conectividad y de Estado extendido del cliente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> </dl>           | Operación realizada correctamente.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Límite de recursos del sistema, no se pudo realizar la operación.<br/> |



 

## <a name="remarks"></a>Observaciones

NapAgent establece esta información después de procesar una [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) y el exigidor no debe establecerla.

SHA debe liberar la estructura [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) llamando a [**FreeIsolationInfoEx**](freeisolationinfoex.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>NapEnforcementClient. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapEnforcementClient. idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md)
</dt> </dl>

 

 





