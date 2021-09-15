---
title: Método INapServerCallback OnComplete (NapSystemHealthValidator.h)
description: Usado por shvs para indicar la finalización de solicitudes asincrónicas.
ms.assetid: 959ee4ac-7c29-4013-a174-24abc6a580c7
keywords:
- Nap del método OnComplete
- Método OnComplete NAP , interfaz INapServerCallback
- INapServerCallback interface NAP , Método OnComplete
topic_type:
- apiref
api_name:
- INapServerCallback.OnComplete
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ef846d3d9dc2d6618f0eca9f097d74222606eb4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473783"
---
# <a name="inapservercallbackoncomplete-method"></a>INapServerCallback::OnComplete (Método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Los SHV usan el **método INapServerCallback::OnComplete** para indicar la finalización de solicitudes asincrónicas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OnComplete(
  [in] INapSystemHealthValidationRequest *request,
  [in] HRESULT                           errorCode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*solicitud* \[ En\]
</dt> <dd>

Puntero a un [**objeto INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) que representa una solicitud de validación.

</dd> <dt>

*errorCode* \[ En\]
</dt> <dd>

Código [**de error nap**](nap-error-constants.md) que indica el motivo por el que no se pudo realizar la validación.

> [!Note]  
> Normalmente, el valor devuelto del método [**INapSystemHealthValidationRequest::SetSoHResponse**](inapsystemhealthvalidationrequest-setsohresponse-method.md) se pasa a este parámetro. Sin embargo, si no se pudo llamar a **SetSoHResponse** debido a un error de reprocesamiento, se pasa el valor devuelto por el comando con error.

 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>           | Operación realizada correctamente.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | El límite de recursos del sistema no pudo realizar la operación.<br/> |



 

## <a name="remarks"></a>Observaciones

Los validadores deben devolver S OK si se pudo completar la validación \_ [**de SoHRequest,**](/windows/win32/api/naptypes/ns-naptypes-soh) independientemente de si **SoHRequest** superó la comprobación de estado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                    |
| Encabezado<br/>                   | <dl> <dt>NapSystemHealthValidator.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthValidator.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Vea también

<dl> <dt>


</dt> <dt>

[**INapServerCallback**](inapservercallback.md)
</dt> <dt>

[**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





