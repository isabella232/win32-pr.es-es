---
title: Método INapSystemHealthValidationRequest SetPrivateData (NapSystemHealthValidator. h)
description: Permite que NapServer almacene información de estado.
ms.assetid: 128f9beb-e5da-4b20-bf5e-fcf064209da3
keywords:
- Método SetPrivateData NAP
- Método SetPrivateData NAP, interfaz INapSystemHealthValidationRequest
- Interfaz INapSystemHealthValidationRequest NAP, método SetPrivateData
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.SetPrivateData
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da50ca236c08388632e17916decee162b3b71743
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802816"
---
# <a name="inapsystemhealthvalidationrequestsetprivatedata-method"></a>INapSystemHealthValidationRequest:: SetPrivateData (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El método **INapSystemHealthValidationRequest:: SetPrivateData** permite que NapServer almacene información de estado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetPrivateData(
  [in] const PrivateData *privateData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*privateData* \[ de\]
</dt> <dd>

Un puntero a un BLOB de datos [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) que contiene la información de estado opaca.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> </dl>           | Operación realizada correctamente.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Límite de recursos del sistema, no se pudo realizar la operación.<br/> |



 

## <a name="remarks"></a>Observaciones

Solo NapServer puede interpretar el BLOB de datos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                    |
| Encabezado<br/>                   | <dl> <dt>NapSystemHealthValidator. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthValidator. idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





