---
title: Método INapSystemHealthValidationRequest2 GetConfigID (NapSystemHealthValidator. h)
description: Lo usan los validadores de mantenimiento del sistema (SHV) para recuperar el identificador de configuración en una solicitud de validación.
ms.assetid: 6d5564e4-8386-444b-a859-f0c855e4ee30
keywords:
- Método GetConfigID NAP
- Método GetConfigID NAP, interfaz INapSystemHealthValidationRequest2
- Interfaz INapSystemHealthValidationRequest2 NAP, método GetConfigID
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
ms.openlocfilehash: 0f3b41d2f08dc117fd28e704d607c628ec73e6ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676961"
---
# <a name="inapsystemhealthvalidationrequest2getconfigid-method"></a>INapSystemHealthValidationRequest2:: GetConfigID (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Los validadores de mantenimiento del sistema (SHV) usan el método **INapSystemHealthValidationRequest2:: GetConfigId** para recuperar el identificador de configuración en una solicitud de validación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetConfigID(
  [out] UINT32 *configID
) const;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*configID* \[ enuncia\]
</dt> <dd>

En la devolución, un puntero a UINT32 que contiene un ID. de configuración del SHV.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes códigos de error en función del resultado de esta operación.



| Código devuelto                                                                                  | Descripción                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | Operación correcta.<br/>                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | El parámetro configID era **null**.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                                 |
| Encabezado<br/>                   | <dl> <dt>NapSystemHealthValidator. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthValidator. idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapSystemHealthValidationRequest2**](inapsystemhealthvalidationrequest2.md)
</dt> </dl>

 

 





