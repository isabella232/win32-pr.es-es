---
description: Solicita que el estado del componente de la interfaz de servicio invitado se cambie al valor especificado.
ms.assetid: D9F7CD03-0D86-4005-A600-5CC7082A5047
title: Msvm_GuestServiceInterfaceComponent::RequestStateChange (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestServiceInterfaceComponent.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2b04859406a2600650caa1d822215291a84656d6909740008c2a87a9787f87a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501015"
---
# <a name="msvm_guestserviceinterfacecomponentrequeststatechange-method"></a>Método Msvm \_ GuestServiceInterfaceComponent::RequestStateChange

Solicita que el estado del componente de la interfaz de servicio invitado se cambie al valor especificado.

## <a name="syntax"></a>Sintaxis


```C++
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*RequestedState* \[ En\]
</dt> <dd>

Tipo: **uint16**

El nuevo estado. La información se coloca en la **propiedad RequestedState** de la instancia si el código de retorno del método **RequestStateChange** es 0 o 4096. Para obtener más información, vea la descripción de las propiedades **EnabledState** y **RequestedState** del elemento. Debe ser uno de los siguientes valores.

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Habilitado** (2)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Deshabilitado** (3)


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

**Apagar** (4)


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

**Sin** conexión (6)


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

**Prueba** (7)


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

**Aplazar** (8)


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

**Quiesce** (9)


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

**Reinicio** (10)


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

**Restablecimiento** (11)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Vendor Reserved** (32768..65535)


</dt> <dd></dd> </dl> </dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Tipo: **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**

Referencia opcional a un objeto [**\_ ConcreteJob de Msvm**](msvm-concretejob.md) que se devuelve si la operación se ejecuta de forma asincrónica. Si está presente, la referencia devuelta se puede usar para supervisar el progreso y obtener el resultado del método .

</dd> <dt>

*TimeoutPeriod* \[ En\]
</dt> <dd>

Tipo: **datetime**

Período de tiempo de espera que especifica la cantidad máxima de tiempo que el cliente espera que se lleve la transición al nuevo estado. El formato de intervalo debe usarse para especificar el período de tiempo de espera. Un valor de 0 o **Null** indica que el cliente no tiene ningún requisito de tiempo para la transición. Si esta propiedad no contiene 0 o **Null** y la implementación no admite este parámetro, se debe devolver un código de retorno 4098 (**Use Of Timeout Parameter Not Supported**).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los valores siguientes.



| Código o valor devuelto                                                                                                                                                                       | Descripción         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**Completado sin error**</dt> <dt>0</dt> </dl>                           | Correcto.<br/> |
| <dl> <dt>**No compatible**</dt> <dt>con 1</dt> </dl>                                     |                     |
| <dl> <dt>**Error desconocido o no especificado**</dt> <dt>2</dt> </dl>                         |                     |
| <dl> <dt>**No se puede completar dentro del período de tiempo de espera**</dt> <dt>3</dt> </dl>            |                     |
| <dl> <dt>**Error**</dt> <dt>4</dt> </dl>                                            |                     |
| <dl> <dt>**Parámetro 5 no**</dt> <dt>válido</dt> </dl>                                 |                     |
| <dl> <dt>**En uso**</dt> <dt>6</dt> </dl>                                            |                     |
| <dl> <dt>**DMTF reservado**</dt> <dt>.</dt> </dl>                                    |                     |
| <dl> <dt>**Parámetros de método activados: transición iniciada**</dt> <dt>4096</dt> </dl> |                     |
| <dl> <dt>**Transición de estado**</dt> <dt>no válida 4097</dt> </dl>                       |                     |
| <dl> <dt>**No se admite el uso del parámetro timeout**</dt> <dt>4098</dt> </dl>         |                     |
| <dl> <dt>**Busy**</dt> <dt>4099</dt> </dl>                                           |                     |
| <dl> <dt>**Método reservado**</dt> <dt>4100..32767</dt> </dl>                         |                     |
| <dl> <dt>**Específico del**</dt> <dt>proveedor 32768..65535</dt> </dl>                        |                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                                                 |
| Espacio de nombres<br/>                | \\\\Root \\ Virtualization \\ V2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Msvm \_ GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md)
</dt> </dl>

 

