---
description: Inicie un trabajo para cambiar un grupo primario con la configuración de asignación especificada.
ms.assetid: 2eea1a60-fbf0-49a7-8f79-52c62c295316
title: Método ChangeParentResourcePool de la CIM_ResourcePoolConfigurationService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.ChangeParentResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b7030cb4ed9333ad5c56722954a24a1ee7bff351a15873423dbfe6e8dca1830d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119980905"
---
# <a name="changeparentresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a>Método ChangeParentResourcePool de la clase \_ ResourcePoolConfigurationService de CIM

Inicie un trabajo para cambiar un grupo primario con la configuración de asignación especificada.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ChangeParentResourcePool(
  [in]  CIM_ResourcePool REF ChildPool,
  [in]  CIM_ResourcePool REF ParentPool[],
  [in]  string               Settings[],
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ChildPool* \[ En\]
</dt> <dd>

Grupo [**\_ de recursos CIM que**](cim-resourcepool.md) hace referencia al grupo secundario.

</dd> <dt>

*ParentPool* \[ En\]
</dt> <dd>

Matriz [**\_ ResourcePool**](cim-resourcepool.md) de CIM que hace referencia a los grupos primarios.

</dd> <dt>

*Configuración* \[ En\]
</dt> <dd>

Cadena opcional que contiene una representación de una instancia [**\_ settingData**](cim-settingdata.md) de CIM que se usa para especificar la configuración del grupo primario.

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

**Recursos insuficientes** (8)
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

 

 




