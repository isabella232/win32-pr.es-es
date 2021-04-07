---
description: Cambia la configuración de recursos del grupo primario para los recursos asignados a un grupo secundario.
ms.assetid: 419fca70-5f15-4593-80ac-ef2af2c3dde5
title: Método ModifyPoolResources de la clase Msvm_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService.ModifyPoolResources
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2efffdbcc34577f675556874c4153eea2670768c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911689"
---
# <a name="modifypoolresources-method-of-the-msvm_resourcepoolconfigurationservice-class"></a>Método ModifyPoolResources de la \_ clase ResourcePoolConfigurationService de MSVM

Cambia la configuración de recursos del grupo primario para los recursos asignados a un grupo secundario.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ModifyPoolResources(
  [in]  CIM_ResourcePool REF ChildPool,
  [in]  CIM_ResourcePool REF ParentPools[],
  [in]  string               AllocationSettings[],
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ChildPool* \[ de\]
</dt> <dd>

Referencia a una instancia de la clase [**\_ ResourcePool de CIM**](cim-resourcepool.md) que representa el grupo secundario que se va a modificar.

</dd> <dt>

*ParentPools* \[ de\]
</dt> <dd>

Una matriz de [**referencias \_ ResourcePool CIM**](cim-resourcepool.md) que representan los nuevos grupos primarios que se asignarán al grupo secundario.

</dd> <dt>

*AllocationSettings* \[ de\]
</dt> <dd>

Una matriz opcional de una o varias instancias incrustadas de la clase [**MSVM \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) que se usan para especificar la configuración relacionada con la asignación del grupo.

</dd> <dt>

*Trabajo* \[ de enuncia\]
</dt> <dd>

Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve uno de los valores siguientes.

<dl> <dt>

**Trabajo completado sin errores** (0)
</dt> <dt>

**DMTF reservado** (..)
</dt> <dt>

**Parámetros de método comprobados: trabajo iniciado** (4096)
</dt> <dt>

**Método reservado** (de no.. 32767)
</dt> <dt>

**Error** (32768)
</dt> <dt>

**Acceso denegado** (32769)
</dt> <dt>

**No compatible** (32770)
</dt> <dt>

**Desconocido** (32771)
</dt> <dt>

**Tiempo de espera** (32772)
</dt> <dt>

**Parámetro no válido** (32773)
</dt> <dt>

**En uso** (32774)
</dt> <dt>

**Estado no válido** (32775)
</dt> <dt>

**Tipo de recurso incorrecto para el grupo** (32776)
</dt> <dt>

**No disponible** (32777)
</dt> <dt>

**Memoria insuficiente** (32778)
</dt> <dt>

**Proveedor reservado** (32779)
</dt> <dt>

**Recursos insuficientes** (32780)
</dt> <dt>

**No se encontró el objeto** (32781.. 32787)
</dt> <dt>

**Existe el objeto** (32788)
</dt> <dt>

**Específico del proveedor** (32768... 65535)
</dt> </dl>

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

[**MSVM \_ ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md)
</dt> </dl>

 

