---
description: Solicita que el estado del trabajo de migración cambie al estado especificado.
ms.assetid: f0be5ea8-7e21-407e-b84d-8bd4ca5a6a2c
title: Método RequestStateChange de la Msvm_MigrationJob clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MigrationJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a7a5934049860e92aa9986a301fe3d75bed8022bda064653ee9e405ad16f6619
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014323"
---
# <a name="requeststatechange-method-of-the-msvm_migrationjob-class"></a>Método RequestStateChange de la clase \_ MigrationJob de Msvm

Solicita que el estado del trabajo de migración cambie al estado especificado. Invocar el método **RequestStateChange** varias veces puede dar lugar a que las solicitudes anteriores se sobrescriban o se pierdan. Si se devuelve 0, la tarea se completó correctamente. Cualquier otro código de retorno indica una condición de error.

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

Período de tiempo de espera que especifica la cantidad máxima de tiempo que el cliente espera que se lleve la transición al nuevo estado. El formato de intervalo debe usarse para especificar el período de tiempo de espera. Un valor de 0 o **Null** indica que el cliente no tiene ningún requisito de tiempo para la transición. Si esta propiedad no contiene 0 o **Null** y la implementación no admite este parámetro, se debe devolver un código de retorno 4098 (No se admite el uso del parámetro de tiempo de espera).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

<dl> <dt>

  (0)
</dt> <dt>

 (32768)
</dt> <dt>

 (32769)
</dt> <dt>

 (32770)
</dt> <dt>

 (32771)
</dt> <dt>

 (32772)
</dt> <dt>

 (32773)
</dt> <dt>

 (32774)
</dt> <dt>

 (32775)
</dt> <dt>

 (32776)
</dt> <dt>

 (32777)
</dt> <dt>

 (32778)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Msvm \_ MigrationJob**](msvm-migrationjob.md)
</dt> </dl>

 

 




