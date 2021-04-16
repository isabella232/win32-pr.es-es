---
title: INapSystemHealthAgentBinding método UnInitialize (NapSystemHealthAgent. h)
description: Hace que el NapAgent libere todas sus referencias a punteros COM del agente de mantenimiento del sistema.
ms.assetid: 8b9fabc9-7453-41fe-a1e7-2ec5fa275a3a
keywords:
- Anular la inicialización del método NAP
- Método uninitial NAP, interfaz INapSystemHealthAgentBinding
- Interfaz INapSystemHealthAgentBinding NAP, método UnInitialize
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.Uninitialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a863e9d742610ab764a3b7a00966e8e112278317
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676791"
---
# <a name="inapsystemhealthagentbindinguninitialize-method"></a>INapSystemHealthAgentBinding:: UnInitialize (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El método **INapSystemHealthAgentBinding:: UnInitialize** hace que NapAgent libere todas sus referencias a punteros com del agente de mantenimiento del sistema.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Uninitialize();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                             | Descripción                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> </dl>                   | Operación realizada correctamente.<br/>                                                                                                |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>         | Error de permisos, acceso denegado.<br/>                                                                                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | Límite de recursos del sistema, no se pudo realizar la operación.<br/>                                                             |
| <dl> <dt>**NAP \_ E \_ no \_ inicializado**</dt> </dl> | SHA no se ha inicializado previamente.<br/>                                                                        |
| <dl> <dt>**RPC \_ E \_ desconectado**</dt> </dl>     | NapAgent se ha detenido. Este objeto se recuperará automáticamente y se volverá a enlazar a NapAgent, una vez que se reinicie.<br/> |



 

## <a name="remarks"></a>Observaciones

La NapAgent bloquea la ejecución de esta llamada al método hasta que se completen todas las llamadas existentes en las interfaces de enlace y devolución de llamada.

SHA debe llamar a [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) antes de llamar a este método o a cualquier otro método de la interfaz [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>NapSystemHealthAgent. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthAgent. idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





