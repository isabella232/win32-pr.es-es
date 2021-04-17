---
description: Inicie un trabajo para eliminar un grupo de recursos.
ms.assetid: af3d9c7c-a825-4568-822d-044b3d92d144
title: Método DeleteResourcePool de la clase CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.DeleteResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9cab27df07a6a3a9679cb5e6595b6ba558d8b05e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666569"
---
# <a name="deleteresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a>Método DeleteResourcePool de la \_ clase ResourcePoolConfigurationService de CIM

Inicie un trabajo para eliminar un grupo de recursos. No puede haber ninguna asignación pendiente o se producirá un error en la eliminación con "en uso". Si el grupo de recursos de servidor es un grupo de recursos raíz, los recursos del host se devuelven al sistema subyacente.

## <a name="syntax"></a>Sintaxis


```mof
uint32 DeleteResourcePool(
  [in]  CIM_ResourcePool REF Pool,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Grupo* \[ de de\]
</dt> <dd>

[**\_ ResourcePool CIM**](cim-resourcepool.md) que hace referencia al grupo que se va a eliminar.

</dd> <dt>

*Trabajo* \[ de enuncia\]
</dt> <dd>

Un [**\_ ConcreteJob de CIM**](cim-concretejob.md) que hace referencia al trabajo (puede ser **null** si el trabajo se completó).

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

**Método reservado** (de no.. 32767)
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

 

 




