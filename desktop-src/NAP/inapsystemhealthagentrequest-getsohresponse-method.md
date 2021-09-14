---
title: Método INapSystemHealthAgentRequest GetSoHResponse (NapSystemHealthAgent.h)
description: El agente de mantenimiento lo usa para recuperar su blob SoHResponse cuando NapAgent llama a INapSystemHealthAgentCallback ProcessSoHResponse.
ms.assetid: 60319256-d5c2-46cc-a59b-f81732e21a7f
keywords:
- Método NAP de GetSoHResponse
- Método NAP de GetSoHResponse, interfaz INapSystemHealthAgentRequest
- Interfaz NAP de INapSystemHealthAgentRequest, método GetSoHResponse
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetSoHResponse
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d593ff897e69b86b554365561e43308adead5250
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161300"
---
# <a name="inapsystemhealthagentrequestgetsohresponse-method"></a>Método INapSystemHealthAgentRequest::GetSoHResponse

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El agente de mantenimiento usa el método **INapSystemHealthAgentRequest::GetSoHResponse** para recuperar su blob SoHResponse cuando NapAgent llama a [**INapSystemHealthAgentCallback::P rocessSoHResponse**](inapsystemhealthagentcallback-processsohresponse-method.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetSoHResponse(
  [out] SoHResponse **sohResponse,
  [out] UINT8       *flags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*sohResponse* \[ out\]
</dt> <dd>

Puntero a un puntero a un [**paquete SoHResponse.**](/windows/win32/api/naptypes/ns-naptypes-soh)

</dd> <dt>

*flags* \[ out\]
</dt> <dd>

Puntero a una marca que habilita la corrección mediante SHA si se establece el bit [**shaFixup;**](nap-type-constants.md) de lo contrario, la corrección está deshabilitada.



| Valores posibles                                                                                                                                                          | Significado                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="shaFixup"></span><span id="shafixup"></span><span id="SHAFIXUP"></span><dl> <dt>**shaFixup**</dt> </dl> | Se espera que SHA realice la corrección en función de la respuesta. Si no se establece esta marca, sha no debe realizar una corrección aunque [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) indique que es incorrecto.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>           | Operación realizada correctamente.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | El límite de recursos del sistema no pudo realizar la operación.<br/> |



 

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

 

 





