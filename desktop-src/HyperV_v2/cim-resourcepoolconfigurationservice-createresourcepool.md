---
description: Inicia un trabajo para crear una clase ResourcePool raíz. ResourcePool tendrá como ámbito el mismo sistema que este servicio.
ms.assetid: 357880dc-125a-452c-89f5-44cd17684436
title: Método CreateResourcePool de la CIM_ResourcePoolConfigurationService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.CreateResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 723ff669a44a7459f52a389e1ad61d236d00489a95e1bbf1038ce9c6eb21caab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119980895"
---
# <a name="createresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a>Método CreateResourcePool de la clase \_ ResourcePoolConfigurationService de CIM

Inicia un trabajo para crear una clase ResourcePool raíz. ResourcePool tendrá como ámbito el mismo sistema que este servicio.

## <a name="syntax"></a>Sintaxis


```mof
uint32 CreateResourcePool(
  [in]  string                ElementName,
  [in]  CIM_LogicalDevice REF HostResources[],
  [in]  string                ResourceType,
  [out] CIM_ResourcePool  REF Pool,
  [out] CIM_ConcreteJob   REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ElementName* \[ En\]
</dt> <dd>

Nombre pertinente del usuario final para el grupo que se va a crear. Si **es NULL,** se puede usar un nombre predeterminado proporcionado por el sistema. El valor se almacenará en la **propiedad ElementName** del grupo creado.

</dd> <dt>

*HostResources* \[ En\]
</dt> <dd>

Matriz de cero o más [**dispositivos \_ LogicalDevice de CIM**](cim-logicaldevice.md) que se usan para crear el grupo o modificar las extensiones de origen. Todos los elementos de la matriz deben ser del mismo tipo.

</dd> <dt>

*ResourceType* \[ En\]
</dt> <dd>

Tipo de recursos que administrará el grupo creado. Si *HostResources* contiene elementos, esta propiedad debe cambiar su tipo.

</dd> <dt>

*Grupo* \[ out\]
</dt> <dd>

Si se ejecuta correctamente, devuelve una referencia al elemento [**\_ ResourcePool de CIM resultante.**](cim-resourcepool.md) Cuando se devuelve un trabajo, puede ser **NULL,** en cuyo caso, el cliente debe usar el trabajo para buscar el grupo de recursos resultante una vez completado el trabajo.

</dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Referencia a un [**\_ ConcreteJob de CIM**](cim-concretejob.md) que representa el trabajo (puede ser NULL si el trabajo se ha completado).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor 0 si se ejecuta correctamente; de lo contrario, devuelve un error.

<dl> <dt>

**Trabajo completado sin error** (0)
</dt> <dt>

**No compatible** (1)
</dt> <dt>

**Desconocido** (2)
</dt> <dt>

**Tiempo de** espera (3)
</dt> <dt>

**Error** (4)
</dt> <dt>

**Parámetro no válido** (5)
</dt> <dt>

**En uso** (6)
</dt> <dt>

**ResourceType incorrecto para el grupo** (7)
</dt> <dt>

**DMTF reservado** (..)
</dt> <dt>

**Parámetros de método comprobados: trabajo iniciado** (4096)
</dt> <dt>

**Tamaño no admitido** (4097)
</dt> <dt>

**Método reservado** (4098..32767)
</dt> <dt>

**Específico del** proveedor (32768..65535)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ ResourcePoolConfigurationService**](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




