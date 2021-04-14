---
title: Método INapSystemHealthValidationRequest GetCorrelationId (NapSystemHealthValidator. h)
description: Lo usan los validadores de mantenimiento del sistema (SHV) para recuperar el identificador de correlación. A continuación, el SHV debe registrar esta información.
ms.assetid: 72603d24-219e-4bb0-9b2b-b58d42939da8
keywords:
- Método GetCorrelationId NAP
- Método GetCorrelationId NAP, interfaz INapSystemHealthValidationRequest
- Interfaz INapSystemHealthValidationRequest NAP, método GetCorrelationId
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetCorrelationId
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1095a2c3eec90ff33613b6d37b43f31fdabd107
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490360"
---
# <a name="inapsystemhealthvalidationrequestgetcorrelationid-method"></a>INapSystemHealthValidationRequest:: GetCorrelationId (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Los validadores de mantenimiento del sistema (SHV) usan el método **INapSystemHealthValidationRequest:: GetCorrelationId** para recuperar el identificador de correlación. A continuación, el SHV debe registrar esta información.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetCorrelationId(
  [out] CorrelationId *correlationId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*CorrelationId* \[ enuncia\]
</dt> <dd>

Un puntero a un [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) único para el intercambio de SOH.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> </dl>           | Operación realizada correctamente.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Límite de recursos del sistema, no se pudo realizar la operación.<br/> |



 

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

 

 





