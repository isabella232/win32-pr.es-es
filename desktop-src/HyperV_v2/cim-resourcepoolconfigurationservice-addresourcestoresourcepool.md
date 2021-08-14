---
description: Inicia un trabajo para agregar recursos a un grupo de recursos.
ms.assetid: b163619a-19bd-43d7-ba35-ec4bd8192100
title: Método AddResourcesToResourcePool de la CIM_ResourcePoolConfigurationService clase
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
ms.openlocfilehash: 55191f3ddce5672d1b76987b8a7c2ce1f87b9cca330a7ba14aa4ae10bacc5b67
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119980935"
---
# <a name="addresourcestoresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a>Método AddResourcesToResourcePool de la clase \_ ResourcePoolConfigurationService de CIM

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

*HostResources* \[ En\]
</dt> <dd>

Matriz [**de instancias \_ logicalDevice**](cim-logicaldevice.md) de CIM que se agregarán al grupo.

</dd> <dt>

*Grupo* \[ En\]
</dt> <dd>

Grupo [**\_ de recursos CIM**](cim-resourcepool.md) que representa el grupo al que se agregarán los recursos.

</dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Un [**\_ objeto ConcreteJob de CIM**](cim-concretejob.md) que hace referencia al trabajo (puede ser NULL **si** el trabajo se ha completado).

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



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CIM \_ ResourcePoolConfigurationService**](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




