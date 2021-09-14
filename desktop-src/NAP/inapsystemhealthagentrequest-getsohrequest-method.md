---
title: Método INapSystemHealthAgentRequest GetSoHRequest (NapSystemHealthAgent.h)
description: Los SHA pueden usar los objetos SOH almacenados previamente en caché por NapAgent.
ms.assetid: 187a4513-79db-45cb-8d64-6a92a2d3b004
keywords:
- Método NAP de GetSoHRequest
- Método NAP de GetSoHRequest, interfaz INapSystemHealthAgentRequest
- Interfaz NAP de INapSystemHealthAgentRequest, método GetSoHRequest
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161301"
---
# <a name="inapsystemhealthagentrequestgetsohrequest-method"></a>INapSystemHealthAgentRequest::GetSoHRequest (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El **método INapSystemHealthAgentRequest::GetSoHRequest** lo pueden usar las SHA get SoHs previamente almacenadas en caché por NapAgent.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetSoHRequest(
  [out] SoHRequest **sohRequest
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*sohRequest* \[ out\]
</dt> <dd>

Puntero a un puntero a [**soHRequest.**](/windows/win32/api/naptypes/ns-naptypes-soh)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                            | Descripción                                                            |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>                  | Operación realizada correctamente.<br/>                                        |
| <dl> <dt>**NAP \_ E \_ NO \_ CACHED \_ SOH**</dt> </dl> | No se encuentra el SoH; NapAgent no tiene una copia almacenada en caché.<br/> |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>        | Error de permisos, acceso denegado.<br/>                           |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>         | El límite de recursos del sistema no pudo realizar la operación.<br/>     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qagentrt.dll</dt> </dl>             |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





