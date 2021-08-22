---
description: Inicie un trabajo para eliminar un grupo de recursos.
ms.assetid: af3d9c7c-a825-4568-822d-044b3d92d144
title: Método DeleteResourcePool de la CIM_ResourcePoolConfigurationService clase
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
ms.openlocfilehash: a5fb895eb76a503d6199bf1057a9f9eaff0c72e4af59460c63551a7c581ff0cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118648094"
---
# <a name="deleteresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a>Método DeleteResourcePool de la clase \_ ResourcePoolConfigurationService de CIM

Inicie un trabajo para eliminar un grupo de recursos. No puede haber ninguna asignación pendiente o la eliminación producirá un error con "En uso". Si el grupo de recursos es un grupo de recursos raíz, los recursos de host se devuelven al sistema subyacente.

## <a name="syntax"></a>Sintaxis


```mof
uint32 DeleteResourcePool(
  [in]  CIM_ResourcePool REF Pool,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Grupo* \[ En\]
</dt> <dd>

Grupo [**de recursos CIM \_ que**](cim-resourcepool.md) hace referencia al grupo que se debe eliminar.

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

**Método reservado** (4097..32767)
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

 

 




