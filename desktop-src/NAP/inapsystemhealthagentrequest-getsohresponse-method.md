---
title: Método INapSystemHealthAgentRequest GetSoHResponse (NapSystemHealthAgent. h)
description: Lo usa el agente de mantenimiento para recuperar su BLOB de SoHResponse cuando NapAgent llama a INapSystemHealthAgentCallback ProcessSoHResponse.
ms.assetid: 60319256-d5c2-46cc-a59b-f81732e21a7f
keywords:
- Método GetSoHResponse NAP
- Método GetSoHResponse NAP, interfaz INapSystemHealthAgentRequest
- Interfaz INapSystemHealthAgentRequest NAP, método GetSoHResponse
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150100"
---
# <a name="inapsystemhealthagentrequestgetsohresponse-method"></a>INapSystemHealthAgentRequest:: GetSoHResponse (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El agente de mantenimiento usa el método **INapSystemHealthAgentRequest:: GetSoHResponse** para recuperar su BLOB de SoHResponse cuando el NapAgent llama a [**INapSystemHealthAgentCallback::P rocesssohresponse**](inapsystemhealthagentcallback-processsohresponse-method.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetSoHResponse(
  [out] SoHResponse **sohResponse,
  [out] UINT8       *flags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*sohResponse* \[ enuncia\]
</dt> <dd>

Un puntero a un puntero a un paquete [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) .

</dd> <dt>

*marcas* \[ de enuncia\]
</dt> <dd>

Un puntero a una marca que habilita la corrección del SHA si se establece el bit [**shaFixup**](nap-type-constants.md) ; de lo contrario, se deshabilita la corrección.



| Valores posibles                                                                                                                                                          | Significado                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="shaFixup"></span><span id="shafixup"></span><span id="SHAFIXUP"></span><dl> <dt>**shaFixup**</dt> </dl> | Se espera que SHA realice la corrección basada en la respuesta. Si no se establece esta marca, SHA no debe realizar ninguna corrección, aunque el [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) indica que está en mal estado.<br/> |



 

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

 

 





