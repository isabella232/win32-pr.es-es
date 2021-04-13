---
title: Método Initialize INapSystemHealthAgentBinding (NapSystemHealthAgent. h)
description: Inicializa el agente de mantenimiento del sistema (SHA) y enlaza el SHA al servicio NapAgent.
ms.assetid: abbc942b-0217-4b07-bf43-fab55ca9c411
keywords:
- Inicializar el método NAP
- Inicializar método NAP, interfaz INapSystemHealthAgentBinding
- Interfaz INapSystemHealthAgentBinding NAP, método Initialize
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.Initialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ee4d4f602303ca1943e47c04ba30ab8f6e75e72
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359676"
---
# <a name="inapsystemhealthagentbindinginitialize-method"></a>INapSystemHealthAgentBinding:: Initialize (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El método **INapSystemHealthAgentBinding:: Initialize** inicializa el agente de mantenimiento del sistema (SHA) y enlaza el Sha con el servicio NapAgent. Se debe llamar a este método antes de llamar a cualquier otro método en la interfaz [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Initialize(
  [in] SystemHealthEntityId          id,
  [in] INapSystemHealthAgentCallback *callback
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ID.* \[ en\]
</dt> <dd>

Un [SystemHealthEntityId](nap-datatypes.md) único que contiene el identificador del Sha que se está enlazando al servicio NapAgent.

</dd> <dt>

*devolución de llamada* \[ de\]
</dt> <dd>

Puntero COM a una interfaz [**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md) que usa NapAgent para devolver una llamada al agente de mantenimiento con una notificación/proceso. NapAgent contiene una referencia al objeto asociado a esta interfaz hasta que se llama a [**UnInitialize**](inapsystemhealthagentbinding-uninitialize-method.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                                | Descripción                                                                                                                    |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> </dl>                      | Operación realizada correctamente.<br/>                                                                                                |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>            | Error de permisos, acceso denegado.<br/>                                                                                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>             | Límite de recursos del sistema, no se pudo realizar la operación.<br/>                                                             |
| <dl> <dt>**ERROR \_ ya \_ inicializado**</dt> </dl> | Si se ha inicializado SHA previamente, se devuelve este error.<br/>                                                      |
| <dl> <dt>**NAP \_ E \_ no \_ registrado**</dt> </dl>     | Si el SHA no se ha registrado anteriormente, se devuelve este error.<br/>                                                      |
| <dl> <dt>**RPC \_ E \_ desconectado**</dt> </dl>        | NapAgent se ha detenido. Este objeto se recuperará automáticamente y se volverá a enlazar a NapAgent, una vez que se reinicie.<br/> |



 

## <a name="remarks"></a>Observaciones

NapAgent no desencadena un intercambio de SoH como resultado de la inicialización. Un agente de mantenimiento del sistema debe llamar a [**NotifySoHChange**](inapsystemhealthagentbinding-notifysohchange-method.md) para solicitar un intercambio de paquetes de SOH después de inicializarse con NapAgent.

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

 

 





