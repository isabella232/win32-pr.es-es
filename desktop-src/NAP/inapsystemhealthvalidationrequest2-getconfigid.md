---
title: Método INapSystemHealthValidationRequest2 GetConfigID (NapSystemHealthValidator.h)
description: Lo usan los validadores de estado del sistema (SHV) para recuperar el identificador de configuración en una solicitud de validación.
ms.assetid: 6d5564e4-8386-444b-a859-f0c855e4ee30
keywords:
- Método NAP de GetConfigID
- Método NAP de GetConfigID, interfaz INapSystemHealthValidationRequest2
- Interfaz NAP de INapSystemHealthValidationRequest2, método GetConfigID
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest2.GetConfigID
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72acdd170726d2d94e4fbc46864a7e5aab6b902d7b1ee25b63ee0fa9e376c75e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119625985"
---
# <a name="inapsystemhealthvalidationrequest2getconfigid-method"></a>INapSystemHealthValidationRequest2::GetConfigID (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Los validadores de estado del sistema (SHV) usan el método **INapSystemHealthValidationRequest2::GetConfigId** para recuperar el identificador de configuración en una solicitud de validación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetConfigID(
  [out] UINT32 *configID
) const;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*configID* \[ out\]
</dt> <dd>

En la devolución, puntero a UINT32 que contiene un identificador de configuración de shv.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes códigos de error en función del resultado de esta operación.



| Código devuelto                                                                                  | Descripción                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Operación correcta.<br/>                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | El parámetro configID era **NULL.**<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>NapSystemHealthValidator.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthValidator.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapSystemHealthValidationRequest2**](inapsystemhealthvalidationrequest2.md)
</dt> </dl>

 

 





