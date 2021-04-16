---
description: Iniciar un trabajo para crear un grupo secundario a partir de un grupo primario con la configuración de asignación especificada.
ms.assetid: 9b09221a-7c4e-4648-a2a8-012df1818c3e
title: Método CreateChildResourcePool de la clase CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.CreateChildResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e4e709fd240c849581f6dcd343001a9b1dee7003
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666570"
---
# <a name="createchildresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a>Método CreateChildResourcePool de la \_ clase ResourcePoolConfigurationService de CIM

Iniciar un trabajo para crear un grupo secundario a partir de un grupo primario con la configuración de asignación especificada.

## <a name="syntax"></a>Sintaxis


```mof
uint32 CreateChildResourcePool(
  [in]  string               ElementName,
  [in]  string               Settings[],
  [in]  CIM_ResourcePool REF ParentPool[],
  [out] CIM_ResourcePool REF Pool,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ElementName* \[ de\]
</dt> <dd>

Nombre relevante del usuario final para el grupo que se va a crear. Si **es null**, se puede usar un nombre predeterminado proporcionado por el sistema. El valor se almacenará en la propiedad **ElementName** del elemento creado.

</dd> <dt>

*Configuración* \[ de de\]
</dt> <dd>

Cadena que contiene una representación de una instancia de [**\_ SettingData de CIM**](cim-settingdata.md) que se usa para especificar la configuración del grupo secundario.

</dd> <dt>

*ParentPool* \[ de\]
</dt> <dd>

Un [**\_ ResourcePool CIM**](cim-resourcepool.md) a partir del cual se creará el nuevo grupo.

</dd> <dt>

*Grupo* \[ de enuncia\]
</dt> <dd>

[**\_ ResourcePool CIM**](cim-resourcepool.md) que hace referencia al grupo resultante.

</dd> <dt>

*Trabajo* \[ de enuncia\]
</dt> <dd>

Referencia al trabajo (puede ser null si el trabajo se completó).

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

 

 




