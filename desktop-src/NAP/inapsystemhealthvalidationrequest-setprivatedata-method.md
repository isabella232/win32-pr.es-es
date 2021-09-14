---
title: Método INapSystemHealthValidationRequest SetPrivateData (NapSystemHealthValidator.h)
description: Permite que NapServer almacene información de estado.
ms.assetid: 128f9beb-e5da-4b20-bf5e-fcf064209da3
keywords:
- Nap del método SetPrivateData
- Método NAP de SetPrivateData , interfaz INapSystemHealthValidationRequest
- Interfaz NAP de INapSystemHealthValidationRequest, método SetPrivateData
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161280"
---
# <a name="inapsystemhealthvalidationrequestsetprivatedata-method"></a>INapSystemHealthValidationRequest::SetPrivateData (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El **método INapSystemHealthValidationRequest::SetPrivateData** permite que NapServer almacene información de estado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetPrivateData(
  [in] const PrivateData *privateData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*privateData* \[ En\]
</dt> <dd>

Puntero a un blob [**de datos PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) que contiene la información de estado opaco.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>           | Operación realizada correctamente.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | El límite de recursos del sistema no pudo realizar la operación.<br/> |



 

## <a name="remarks"></a>Observaciones

Solo NapServer puede interpretar el blob de datos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                    |
| Encabezado<br/>                   | <dl> <dt>NapSystemHealthValidator.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthValidator.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





