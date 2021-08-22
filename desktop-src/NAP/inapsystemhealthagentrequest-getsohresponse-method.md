---
title: Método INapSystemHealthAgentRequest GetSoHResponse (NapSystemHealthAgent.h)
description: Lo usa el agente de mantenimiento para recuperar su blob SoHResponse cuando NapAgent llama a INapSystemHealthAgentCallback ProcessSoHResponse.
ms.assetid: 60319256-d5c2-46cc-a59b-f81732e21a7f
keywords:
- Nap del método GetSoHResponse
- Método NAP de GetSoHResponse , interfaz INapSystemHealthAgentRequest
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
ms.openlocfilehash: 1d78b67c38f54cfe1e7d342212be897ba1825b619324e6fc4cb5ab9ae4f5c4a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118621166"
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

Puntero a una marca que habilita la corrección por parte de SHA si se establece el bit [**shaFixup;**](nap-type-constants.md) de lo contrario, la corrección está deshabilitada.



| Valores posibles                                                                                                                                                          | Significado                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="shaFixup"></span><span id="shafixup"></span><span id="SHAFIXUP"></span><dl> <dt>**shaFixup**</dt> </dl> | Se espera que sha realice la corrección en función de la respuesta. Si no se establece esta marca, sha no debe realizar una corrección aunque [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) indique que está en mal estado.<br/> |



 

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
| Header<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qagentrt.dll</dt> </dl>             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





