---
description: Inicia un trabajo para agregar recursos a un grupo de recursos.
ms.assetid: b163619a-19bd-43d7-ba35-ec4bd8192100
title: Método AddResourcesToResourcePool de la clase CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.AddResourcesToResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d3aed59267bd064e95b62431064fbd54bb9168aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686909"
---
# <a name="addresourcestoresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a>Método AddResourcesToResourcePool de la \_ clase ResourcePoolConfigurationService de CIM

Inicia un trabajo para agregar recursos a un grupo de recursos.

## <a name="syntax"></a>Sintaxis


```mof
uint32 AddResourcesToResourcePool(
  [in]  CIM_LogicalDevice REF HostResources[],
  [in]  CIM_ResourcePool  REF Pool,
  [out] CIM_ConcreteJob   REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*HostResources* \[ de\]
</dt> <dd>

Matriz de instancias de [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) que se va a agregar al grupo.

</dd> <dt>

*Grupo* \[ de de\]
</dt> <dd>

[**\_ ResourcePool CIM**](cim-resourcepool.md) que representa el grupo al que se van a agregar los recursos.

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

 

 




