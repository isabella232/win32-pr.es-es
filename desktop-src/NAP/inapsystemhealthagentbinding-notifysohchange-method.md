---
title: Método INapSystemHealthAgentBinding NotifySoHChange (NapSystemHealthAgent. h)
description: Sha usa cuando cambia el SoH.
ms.assetid: 3a653282-03b0-49d5-833f-966497f46faa
keywords:
- Método NotifySoHChange NAP
- Método NotifySoHChange NAP, interfaz INapSystemHealthAgentBinding
- Interfaz INapSystemHealthAgentBinding NAP, método NotifySoHChange
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.NotifySoHChange
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b18c03be03c4bc5282e9ea62ec10d5356871cf5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535332"
---
# <a name="inapsystemhealthagentbindingnotifysohchange-method"></a>INapSystemHealthAgentBinding:: NotifySoHChange (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Sha usa el método **INapSystemHealthAgentBinding:: NotifySoHChange** cuando su SOH cambia.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT NotifySoHChange();
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

Los Sha no deben llamar a esta API speculatively, ya que se produce un intercambio de SoH en la conexión. Las llamadas a esta API solo deben realizarse cuando sea necesario.

NapAgent no contiene este subproceso para procesar el cambio de SoH. En su lugar, devuelve inmediatamente y procesa el cambio de forma asincrónica.

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

 

 





