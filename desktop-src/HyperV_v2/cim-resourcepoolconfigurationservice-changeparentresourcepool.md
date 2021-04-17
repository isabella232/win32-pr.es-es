---
description: Iniciar un trabajo para cambiar un grupo primario con la configuración de asignación especificada.
ms.assetid: 2eea1a60-fbf0-49a7-8f79-52c62c295316
title: Método ChangeParentResourcePool de la clase CIM_ResourcePoolConfigurationService
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
ms.openlocfilehash: 6ef852d6af8f0973b6b3f29fca5fcd90e9ce726a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686908"
---
# <a name="changeparentresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a>Método ChangeParentResourcePool de la \_ clase ResourcePoolConfigurationService de CIM

Iniciar un trabajo para cambiar un grupo primario con la configuración de asignación especificada.

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

*ChildPool* \[ de\]
</dt> <dd>

[**\_ ResourcePool CIM**](cim-resourcepool.md) que hace referencia al grupo secundario.

</dd> <dt>

*ParentPool* \[ de\]
</dt> <dd>

Una [**matriz \_ ResourcePool de CIM**](cim-resourcepool.md) que hace referencia a los grupos primarios.

</dd> <dt>

*Configuración* \[ de de\]
</dt> <dd>

Cadena opcional que contiene una representación de una instancia de [**\_ SettingData de CIM**](cim-settingdata.md) que se usa para especificar la configuración del grupo primario.

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

**Recursos insuficientes** (8)
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

 

 




