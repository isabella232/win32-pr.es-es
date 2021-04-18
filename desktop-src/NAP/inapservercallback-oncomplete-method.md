---
title: Método INapServerCallback (NapSystemHealthValidator. h)
description: Lo usan los SHV para indicar la finalización de la solicitud asincrónica.
ms.assetid: 959ee4ac-7c29-4013-a174-24abc6a580c7
keywords:
- Método alcomplete NAP
- Método alcomplete NAP, interfaz INapServerCallback
- Interfaz INapServerCallback NAP, método alcomplete
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493235"
---
# <a name="inapservercallbackoncomplete-method"></a>INapServerCallback:: alcomplete (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Los SHV usan el método **INapServerCallback:: alcomplete** para indicar la finalización de la solicitud asincrónica.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OnComplete(
  [in] INapSystemHealthValidationRequest *request,
  [in] HRESULT                           errorCode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*solicitud* \[ de de\]
</dt> <dd>

Un puntero a un objeto [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) que representa una solicitud de validación.

</dd> <dt>

*ErrorCode* \[ de\]
</dt> <dd>

Un [**código de error de NAP**](nap-error-constants.md) que indica el motivo por el que no se pudo realizar la validación.

> [!Note]  
> Normalmente, el valor devuelto del método [**INapSystemHealthValidationRequest:: SetSoHResponse**](inapsystemhealthvalidationrequest-setsohresponse-method.md) se pasa a este parámetro. Sin embargo, si no se pudo llamar a **SetSoHResponse** debido a un error de reprocesamiento, se pasa el valor devuelto por el comando con errores.

 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> </dl>           | Operación realizada correctamente.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Límite de recursos del sistema, no se pudo realizar la operación.<br/> |



 

## <a name="remarks"></a>Observaciones

Los validadores deben devolver los valores \_ correctos si se pudo completar la validación de [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) , independientemente de si el **SoHRequest** ha superado la comprobación de estado.

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


</dt> <dt>

[**INapServerCallback**](inapservercallback.md)
</dt> <dt>

[**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





