---
title: Método INapServerManagement UnregisterSystemHealthValidator (NapServerManagement. h)
description: Se usa para anular el registro de un SHV con el servidor NAP.
ms.assetid: f4148df1-a230-4845-ac8b-9e04be9e0d6c
keywords:
- Método UnregisterSystemHealthValidator NAP
- Método UnregisterSystemHealthValidator NAP, interfaz INapServerManagement
- Interfaz INapServerManagement NAP, método UnregisterSystemHealthValidator
topic_type:
- apiref
api_name:
- INapServerManagement.UnregisterSystemHealthValidator
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0715445504b862d9ae9e8478b543f8e80378f08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535014"
---
# <a name="inapservermanagementunregistersystemhealthvalidator-method"></a>INapServerManagement:: UnregisterSystemHealthValidator (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El método **INapServerManagement:: UnregisterSystemHealthValidator** se usa para anular el registro de un SHV con el servidor NAP.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT UnregisterSystemHealthValidator(
  [in] SystemHealthEntityId id
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ID.* \[ en\]
</dt> <dd>

[**SystemHealthEntityId**](nap-type-constants.md) que contiene el identificador único del SHV cuyo registro se va a anular.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> </dl>           | Operación realizada correctamente.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Límite de recursos del sistema, no se pudo realizar la operación.<br/> |



 

## <a name="remarks"></a>Observaciones

Si hay llamadas asincrónicas pendientes en el SHV, se completarán en un momento posterior y se descartarán.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                               |
| Encabezado<br/>                   | <dl> <dt>NapServerManagement. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapServerManagement. idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qsvrmgmt.dll</dt> </dl>            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapServerManagement**](inapservermanagement.md)
</dt> </dl>

 

 





