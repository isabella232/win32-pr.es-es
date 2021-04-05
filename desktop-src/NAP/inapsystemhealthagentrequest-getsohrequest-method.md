---
title: Método INapSystemHealthAgentRequest GetSoHRequest (NapSystemHealthAgent. h)
description: Lo pueden usar Sha Get SOH previamente almacenados en caché por NapAgent.
ms.assetid: 187a4513-79db-45cb-8d64-6a92a2d3b004
keywords:
- Método GetSoHRequest NAP
- Método GetSoHRequest NAP, interfaz INapSystemHealthAgentRequest
- Interfaz INapSystemHealthAgentRequest NAP, método GetSoHRequest
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetSoHRequest
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab52e52c952c2dc1f891098e10c3ecb688052295
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079698"
---
# <a name="inapsystemhealthagentrequestgetsohrequest-method"></a>INapSystemHealthAgentRequest:: GetSoHRequest (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El método **INapSystemHealthAgentRequest:: GetSoHRequest** puede usarse por los Shas Get SOH previamente almacenados en caché por NapAgent.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetSoHRequest(
  [out] SoHRequest **sohRequest
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*sohRequest* \[ enuncia\]
</dt> <dd>

Un puntero a un puntero a un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                            | Descripción                                                            |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> </dl>                  | Operación realizada correctamente.<br/>                                        |
| <dl> <dt>**\_no se \_ ha \_ almacenado en caché el \_ SOH de NAP E**</dt> </dl> | No se encuentra el SoH; NapAgent no tiene una copia almacenada en caché.<br/> |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>        | Error de permisos, acceso denegado.<br/>                           |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>         | Límite de recursos del sistema, no se pudo realizar la operación.<br/>     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>NapSystemHealthAgent. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthAgent. idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qagentrt.dll</dt> </dl>             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





