---
description: Crea un grupo de recursos secundario.
ms.assetid: 30a70231-f1b7-4f0e-ac47-cf5a79ddb8ab
title: Método CreatePool de la Msvm_ResourcePoolConfigurationService clase
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
ms.openlocfilehash: ff1c8a3357a019d9036dd2ac97482a2b106115d06375e96d428ce3d38f6244d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119254355"
---
# <a name="createpool-method-of-the-msvm_resourcepoolconfigurationservice-class"></a>Método CreatePool de la clase ResourcePoolConfigurationService de Msvm \_

Crea un grupo de recursos secundario. El ámbito del grupo de recursos será el mismo sistema que este servicio. El grupo resultante será un grupo secundario.

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

*PoolSettings* \[ En\]
</dt> <dd>

Instancia incrustada de la clase [**\_ ResourcePoolSettingData de Msvm**](msvm-resourcepoolsettingdata.md) que se usa para especificar la configuración del grupo que no está relacionada con la asignación.

</dd> <dt>

*ParentPools* \[ En\]
</dt> <dd>

Matriz de referencias [**de \_ ResourcePool de Msvm**](msvm-resourcepool.md) que representan el grupo o grupos desde los que se va a crear el nuevo grupo.

</dd> <dt>

*AllocationSettings* \[ En\]
</dt> <dd>

Matriz de una o varias instancias incrustadas de la clase [**\_ ResourceAllocationSettingData de Msvm**](msvm-resourceallocationsettingdata.md) que se usan para especificar la configuración relacionada con la asignación de grupos. Esta matriz debe contener un elemento para cada elemento de la *matriz ParentPools* o exactamente un elemento. Si esta matriz contiene un elemento y *ParentPools* contiene más de un elemento, *AlllocationSettings* especifica una asignación de capacidad compartida que cualquiera de los grupos primarios puede satisfacer.

Esto se usa para restringir los recursos que se pueden asignar desde el elemento secundario al grupo a un límite inferior que la capacidad agregada proporcionada por sus elementos secundarios. Esta opción no es compatible con todos los tipos de recursos. Si un tipo de recurso no admite la asignación de capacidad compartida, este método devolverá 32770 (no compatible).

</dd> <dt>

*Grupo* \[ out\]
</dt> <dd>

Referencia al grupo resultante.

</dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ CIM ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve uno de los valores siguientes.

<dl> <dt>

**Trabajo completado sin error** (0)
</dt> <dt>

**DMTF reservado** (..)
</dt> <dt>

**Parámetros de método comprobados: trabajo iniciado** (4096)
</dt> <dt>

**Método reservado** (4097..32767)
</dt> <dt>

**Error** (32768)
</dt> <dt>

**Acceso denegado** (32769)
</dt> <dt>

**No compatible** (32770)
</dt> <dt>

**Desconocido** (32771)
</dt> <dt>

**Tiempo de** espera (32772)
</dt> <dt>

**Parámetro no** válido (32773)
</dt> <dt>

**En uso** (32774)
</dt> <dt>

**Estado no** válido (32775)
</dt> <dt>

**Tipo de recurso incorrecto para el grupo** (32776)
</dt> <dt>

**No disponible** (32777)
</dt> <dt>

**Memoria no suficiente** (32778)
</dt> <dt>

**Vendor Reserved** (32779)
</dt> <dt>

**Recursos insuficientes** (32780)
</dt> <dt>

**Objeto no encontrado** (32781..32787)
</dt> <dt>

**Objeto existe** (32788)
</dt> <dt>

**Específico del** proveedor (32768..65535)
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

[**Msvm \_ ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md)
</dt> </dl>

 

