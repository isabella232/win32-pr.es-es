---
description: Inicia un trabajo para crear un ResourcePool raíz. El ámbito del ResourcePool se establecerá en el mismo sistema que este servicio.
ms.assetid: 357880dc-125a-452c-89f5-44cd17684436
title: Método CreateResourcePool de la clase CIM_ResourcePoolConfigurationService
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
ms.openlocfilehash: ca339eb2e2a4ec0fb441c5ed1a657608d71248bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810334"
---
# <a name="createresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a>Método CreateResourcePool de la \_ clase ResourcePoolConfigurationService de CIM

Inicia un trabajo para crear un ResourcePool raíz. El ámbito del ResourcePool se establecerá en el mismo sistema que este servicio.

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

*ElementName* \[ de\]
</dt> <dd>

Nombre relevante del usuario final para el grupo que se va a crear. Si **es null**, se puede usar un nombre predeterminado proporcionado por el sistema. El valor se almacenará en la propiedad **ElementName** del grupo creado.

</dd> <dt>

*HostResources* \[ de\]
</dt> <dd>

Matriz de cero o más [**dispositivos \_ lógicos de CIM**](cim-logicaldevice.md) que se usan para crear el grupo o modificar las extensiones de origen. Todos los elementos de la matriz deben ser del mismo tipo.

</dd> <dt>

*ResourceType* \[in\]
</dt> <dd>

El tipo de recursos que el grupo creado administrará. Si *HostResources* contiene elementos, esta propiedad debe Machar su tipo.

</dd> <dt>

*Grupo* \[ de enuncia\]
</dt> <dd>

Si se ejecuta correctamente, devuelve una referencia a [**la \_ ResourcePool CIM**](cim-resourcepool.md)resultante. Cuando se devuelve un trabajo, esto puede ser **null**, en cuyo caso, el cliente debe usar el trabajo para buscar el ResourcePool resultante una vez completado el trabajo.

</dd> <dt>

*Trabajo* \[ de enuncia\]
</dt> <dd>

Referencia a un [**\_ ConcreteJob de CIM**](cim-concretejob.md) que representa el trabajo (puede ser null si el trabajo se completó).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un error.

<dl> <dt>

**Trabajo completado sin errores** (0)
</dt> <dt>

**No compatible** (1)
</dt> <dt>

**Desconocido** (2)
</dt> <dt>

**Tiempo de espera** (3)
</dt> <dt>

**Error** (4)
</dt> <dt>

**Parámetro no válido** (5)
</dt> <dt>

**En uso** (6)
</dt> <dt>

**Resourcetype incorrecto para el grupo** (7)
</dt> <dt>

**DMTF reservado** (..)
</dt> <dt>

**Parámetros de método comprobados: trabajo iniciado** (4096)
</dt> <dt>

**Tamaño no compatible** (4097)
</dt> <dt>

**Método reservado** (4098.. 32767)
</dt> <dt>

**Específico del proveedor** (32768... 65535)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_RESOURCEPOOLCONFIGURATIONSERVICE CIM**](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




