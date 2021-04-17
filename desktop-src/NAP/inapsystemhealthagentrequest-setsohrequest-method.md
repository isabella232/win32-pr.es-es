---
title: Método INapSystemHealthAgentRequest SetSoHRequest (NapSystemHealthAgent. h)
description: Lo utilizan los agentes de mantenimiento para escribir su solicitud de SoH resultante de la llamada a INapSystemHealthAgentCallback GetSoHRequest.
ms.assetid: 76471cf2-e5df-4e07-b872-ccac0fd45998
keywords:
- Método SetSoHRequest NAP
- Método SetSoHRequest NAP, interfaz INapSystemHealthAgentRequest
- Interfaz INapSystemHealthAgentRequest NAP, método SetSoHRequest
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.SetSoHRequest
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be0fd1dcccad2a402d8455bcdf4f66052d41160b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105651392"
---
# <a name="inapsystemhealthagentrequestsetsohrequest-method"></a>INapSystemHealthAgentRequest:: SetSoHRequest (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Los agentes de mantenimiento usan el método **INapSystemHealthAgentRequest:: SetSoHRequest** para escribir su solicitud de SOH resultante de la llamada a [**INapSystemHealthAgentCallback:: GetSoHRequest**](inapsystemhealthagentcallback-getsohrequest-method.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetSoHRequest(
  [in] const SoHRequest *sohRequest,
  [in]       BOOL       cacheSohForLaterUse
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*sohRequest* \[ de\]
</dt> <dd>

Un puntero a un paquete [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) .

</dd> <dt>

*cacheSohForLaterUse* \[ de\]
</dt> <dd>

Valor **booleano** que es **true** si NapAgent debe almacenar en caché el [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) y **false** en caso contrario.

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

 

 





