---
description: Inicia un trabajo para quitar recursos de un grupo de recursos.
ms.assetid: 1689ccbf-a524-45b7-bf95-6341a3b28f6c
title: Método RemoveResourcesFromResourcePool de la CIM_ResourcePoolConfigurationService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.RemoveResourcesFromResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 370944c9d8b8307a796b425dd4ff611429f59ccc72473a92528ef19b8c2f5910
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119980875"
---
# <a name="removeresourcesfromresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a>Método RemoveResourcesFromResourcePool de la clase \_ ResourcePoolConfigurationService de CIM

Inicia un trabajo para quitar recursos de un grupo de recursos.

## <a name="syntax"></a>Sintaxis


```mof
uint32 RemoveResourcesFromResourcePool(
  [in]  CIM_LogicalDevice REF HostResources[],
  [in]  CIM_ResourcePool  REF Pool,
  [out] CIM_ConcreteJob   REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*HostResources* \[ En\]
</dt> <dd>

Matriz [**de instancias \_ logicalDevice**](cim-logicaldevice.md) de CIM que se quitarán del grupo.

</dd> <dt>

*Grupo* \[ En\]
</dt> <dd>

Grupo [**de recursos CIM \_ que**](cim-resourcepool.md) representa el grupo del que se quitarán los recursos.

</dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Un [**\_ objeto ConcreteJob de CIM**](cim-concretejob.md) que hace referencia al trabajo (puede ser NULL **si** el trabajo se ha completado).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un 0 si se ejecuta correctamente; de lo contrario, devuelve un error.

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

 

 




