---
description: Solicita que el estado del trabajo se cambie al estado especificado.
ms.assetid: 5D7D7D20-4BB9-4375-BBBF-7AA64FEE6D13
title: Método RequestStateChange de la clase Msvm_ConcreteJob
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
ms.openlocfilehash: 0e7abf5f4bf78ac469e528ab72bb5786130e9cf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667818"
---
# <a name="requeststatechange-method-of-the-msvm_concretejob-class"></a>Método RequestStateChange de la \_ clase ConcreteJob de MSVM

Solicita que el estado del trabajo se cambie al estado especificado. Al invocar el método **RequestStateChange** varias veces, se puede provocar que se sobrescriban o se pierdan solicitudes anteriores. Si se devuelve 0, la tarea se completó correctamente. Cualquier otro código de retorno indica una condición de error.

## <a name="syntax"></a>Sintaxis


```mof
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*RequestedState* \[ de\]
</dt> <dd>

Tipo: **UInt16**

Nuevo estado de un trabajo.

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span id="Start"></span><span id="start"></span><span id="START"></span>**Inicio** (2)


</dt> <dd>

Cambia el estado a "en ejecución".

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspender** (3)


</dt> <dd>

Detiene el trabajo temporalmente. La intención es reiniciar posteriormente el trabajo con "Start". Es posible que se pueda entrar en el estado "servicio" mientras se suspende. (Esto es específico del trabajo).

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Finalizar** (4)


</dt> <dd>

Detiene el trabajo limpiamente, guarda los datos, conserva el estado y cerrando todos los procesos subyacentes de forma ordenada.

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)


</dt> <dd>

Finaliza el trabajo inmediatamente sin necesidad de guardar los datos ni de conservar el estado.

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Servicio** (6)


</dt> <dd>

Coloca el trabajo en un estado de servicio específico del proveedor. Es posible que se pueda reiniciar el trabajo.

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

*TimeoutPeriod* \[ de\]
</dt> <dd>

Tipo: **DateTime**

Un período de tiempo de espera que especifica la cantidad máxima de tiempo que el cliente espera que se realice la transición al nuevo estado. El formato de intervalo debe usarse para especificar el período de tiempo de espera. Un valor de 0 o **null** indica que el cliente no tiene ningún requisito de tiempo para la transición. Si esta propiedad no contiene 0 o **null** y la implementación no admite este parámetro, se debe devolver un código de retorno de 4098 (no se admite el uso del parámetro timeout).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Este método devuelve uno de los valores siguientes.

<dl> <dt>

**Completado sin error** (0)
</dt> <dt>

**No compatible** (1)
</dt> <dt>

**Error desconocido o no especificado** (2)
</dt> <dt>

**No se puede completar en el período de tiempo de espera** (3)
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

**Transición de estado no válida** (4097)
</dt> <dt>

**No se admite el uso de parámetros de tiempo de espera** (4098)
</dt> <dt>

**Ocupado** (4099)
</dt> <dt>

**Método reservado** (4100 32767)
</dt> <dt>

**Específico del proveedor** (32768 65535)
</dt> </dl>

## <a name="remarks"></a>Observaciones

El acceso a la clase [**MSVM \_ ConcreteJob**](msvm-concretejob.md) puede estar restringido por el filtrado de UAC. Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSVM \_ ConcreteJob**](msvm-concretejob.md)
</dt> </dl>

 

