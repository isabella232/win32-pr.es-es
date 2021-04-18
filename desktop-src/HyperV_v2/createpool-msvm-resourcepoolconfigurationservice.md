---
description: Crea un grupo de recursos secundarios.
ms.assetid: 30a70231-f1b7-4f0e-ac47-cf5a79ddb8ab
title: Método CreatePool de la clase Msvm_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService.CreatePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fb29a4b5a47d88232a6b0df6a828d482030b3f1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687851"
---
# <a name="createpool-method-of-the-msvm_resourcepoolconfigurationservice-class"></a>Método CreatePool de la \_ clase ResourcePoolConfigurationService de MSVM

Crea un grupo de recursos secundarios. El grupo de recursos de servidor se limitará al mismo sistema que este servicio. El grupo resultante será un grupo secundario.

## <a name="syntax"></a>Sintaxis


```mof
uint32 CreatePool(
  [in]  string               PoolSettings,
  [in]  CIM_ResourcePool REF ParentPools[],
  [in]  string               AllocationSettings[],
  [out] CIM_ResourcePool REF Pool,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PoolSettings* \[ de\]
</dt> <dd>

Instancia insertada de la clase [**MSVM \_ ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md) que se usa para especificar la configuración del grupo que no está relacionada con la asignación.

</dd> <dt>

*ParentPools* \[ de\]
</dt> <dd>

Una matriz de referencias de [**\_ ResourcePool de MSVM**](msvm-resourcepool.md) que representan el grupo o los grupos de los que se va a crear el nuevo grupo.

</dd> <dt>

*AllocationSettings* \[ de\]
</dt> <dd>

Una matriz de una o varias instancias incrustadas de la clase [**MSVM \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) que se usan para especificar la configuración relacionada con la asignación del grupo. Esta matriz debe contener un elemento para cada elemento de la matriz *ParentPools* o exactamente un elemento. Si esta matriz contiene un elemento y *ParentPools* contiene más de un elemento, *AlllocationSettings* especifica una asignación de capacidad compartida que puede satisfacer cualquiera de los grupos primarios.

Se usa para restringir los recursos que se pueden asignar desde el elemento secundario al grupo a un límite inferior al de la capacidad agregada proporcionada por sus elementos primarios. Esta opción no es compatible con todos los tipos de recursos. Si un tipo de recurso no admite la asignación de capacidad compartida, este método devolverá 32770 (no se admite).

</dd> <dt>

*Grupo* \[ de enuncia\]
</dt> <dd>

Referencia al grupo resultante.

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

 

