---
title: Método INapSystemHealthAgentBinding Initialize (NapSystemHealthAgent.h)
description: Inicializa el agente de mantenimiento del sistema (SHA) y enlaza sha al servicio NapAgent.
ms.assetid: abbc942b-0217-4b07-bf43-fab55ca9c411
keywords:
- Inicialización del método NAP
- Inicializar el método NAP , INapSystemHealthAgentBinding (interfaz)
- INapSystemHealthAgentBinding interfaz NAP , Initialize (método)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071658"
---
# <a name="inapsystemhealthagentbindinginitialize-method"></a>INapSystemHealthAgentBinding::Initialize (Método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El **método INapSystemHealthAgentBinding::Initialize** inicializa el agente de mantenimiento del sistema (SHA) y enlaza sha al servicio NapAgent. Se debe llamar a este método antes de llamar a cualquier otro método en la [**interfaz INapSystemHealthAgentBinding2.**](inapsystemhealthagentbinding2.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Initialize(
  [in] SystemHealthEntityId          id,
  [in] INapSystemHealthAgentCallback *callback
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*id* \[ en\]
</dt> <dd>

[SystemHealthEntityId único](nap-datatypes.md) que contiene el identificador del SHA que se enlaza al servicio NapAgent.

</dd> <dt>

*devolución de llamada* \[ En\]
</dt> <dd>

Puntero COM a una [**interfaz INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md) usada por NapAgent para devolución de llamada al agente de mantenimiento con un proceso o notificación. NapAgent contiene una referencia al objeto asociado a esta interfaz hasta que se llama a [**Uninitialize.**](inapsystemhealthagentbinding-uninitialize-method.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                                | Descripción                                                                                                                    |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>                      | Operación realizada correctamente.<br/>                                                                                                |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>            | Error de permisos, acceso denegado.<br/>                                                                                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>             | El límite de recursos del sistema no pudo realizar la operación.<br/>                                                             |
| <dl> <dt>**ERROR \_ YA \_ INICIALIZADO**</dt> </dl> | Si sha se ha inicializado anteriormente, se devuelve este error.<br/>                                                      |
| <dl> <dt>**NAP \_ E \_ NO \_ REGISTRADO**</dt> </dl>     | Si sha no se ha registrado anteriormente, se devuelve este error.<br/>                                                      |
| <dl> <dt>**RPC \_ E \_ DESCONECTADO**</dt> </dl>        | NapAgent se ha detenido. Este objeto se recuperará automáticamente y se volverá a conectar a NapAgent, una vez que se reinicie.<br/> |



 

## <a name="remarks"></a>Observaciones

NapAgent no desencadena un intercambio de SoH como resultado de la inicialización. Un agente de mantenimiento del sistema debe llamar [**a NotifySoHChange para**](inapsystemhealthagentbinding-notifysohchange-method.md) solicitar un intercambio de paquetes SoH después de inicializar con NapAgent.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





