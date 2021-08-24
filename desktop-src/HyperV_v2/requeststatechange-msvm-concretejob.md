---
description: Solicita que el estado del trabajo cambie al estado especificado.
ms.assetid: 5D7D7D20-4BB9-4375-BBBF-7AA64FEE6D13
title: Método RequestStateChange de la Msvm_ConcreteJob clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 579ad52bd83bd43dc3071f704914eb7b5f9cae4f0be89f018e56b9608b1c12be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501135"
---
# <a name="requeststatechange-method-of-the-msvm_concretejob-class"></a>Método RequestStateChange de la clase ConcreteJob de Msvm \_

Solicita que el estado del trabajo cambie al estado especificado. Invocar el método **RequestStateChange** varias veces puede dar lugar a que las solicitudes anteriores se sobrescriban o se pierdan. Si se devuelve 0, la tarea se completó correctamente. Cualquier otro código de retorno indica una condición de error.

## <a name="syntax"></a>Sintaxis


```mof
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*RequestedState* \[ En\]
</dt> <dd>

Tipo: **uint16**

Nuevo estado de un trabajo.

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span id="Start"></span><span id="start"></span><span id="START"></span>**Inicio** (2)


</dt> <dd>

Cambia el estado a "En ejecución".

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspender** (3)


</dt> <dd>

Detiene temporalmente el trabajo. La intención es reiniciar posteriormente el trabajo con "Start". Es posible especificar el estado "Servicio" mientras se suspende. (Esto es específico del trabajo).

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)


</dt> <dd>

Detiene el trabajo de forma limpia, guardando datos, conservando el estado y cerrando todos los procesos subyacentes de forma ordenada.

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)


</dt> <dd>

Finaliza el trabajo inmediatamente sin necesidad de guardar datos o conservar el estado.

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Servicio** (6)


</dt> <dd>

Coloca el trabajo en un estado de servicio específico del proveedor. Es posible reiniciar el trabajo.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado**


</dt> <dd>

Reservado.

</dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Proveedor reservado**


</dt> <dd>

Reservado.

</dd> </dl> </dd> <dt>

*TimeoutPeriod* \[ En\]
</dt> <dd>

Tipo: **datetime**

Período de tiempo de espera que especifica la cantidad máxima de tiempo que el cliente espera que se lleve la transición al nuevo estado. El formato de intervalo debe usarse para especificar el período de tiempo de espera. Un valor de 0 o **Null** indica que el cliente no tiene requisitos de tiempo para la transición. Si esta propiedad no contiene 0 o **Null** y la implementación no admite este parámetro, se debe devolver un código de retorno 4098 (No se admite el uso del parámetro de tiempo de espera).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los valores siguientes.

<dl> <dt>

**Completado sin error** (0)
</dt> <dt>

**No compatible** (1)
</dt> <dt>

**Error desconocido o no especificado** (2)
</dt> <dt>

**No se puede completar dentro del período de tiempo de espera** (3)
</dt> <dt>

**Error** (4)
</dt> <dt>

**Parámetro no válido** (5)
</dt> <dt>

**En uso** (6)
</dt> <dt>

**DMTF reservado** (7 4095)
</dt> <dt>

**Parámetros de método comprobados: transición iniciada** (4096)
</dt> <dt>

**Transición de estado no** válida (4097)
</dt> <dt>

**No se admite el uso del parámetro timeout** (4098)
</dt> <dt>

**Ocupado** (4099)
</dt> <dt>

**Método reservado** (4100 32767)
</dt> <dt>

**Específico del** proveedor (32768 65535)
</dt> </dl>

## <a name="remarks"></a>Comentarios

El acceso a [**la clase \_ Msvm ConcreteJob**](msvm-concretejob.md) podría estar restringido por el filtrado de UAC. Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Msvm \_ ConcreteJob**](msvm-concretejob.md)
</dt> </dl>

 

