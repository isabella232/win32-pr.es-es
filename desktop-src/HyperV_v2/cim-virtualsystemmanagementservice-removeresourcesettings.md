---
description: 'Método RemoveResourceSettings de la clase CIM_VirtualSystemManagementService: quita la configuración de recursos virtuales de una configuración del sistema virtual.'
ms.assetid: 7934a5e4-f54c-43fd-9ec3-d1fc1aad0acd
title: Método RemoveResourceSettings de la CIM_VirtualSystemManagementService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.RemoveResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4a3b94ff6ecd42ea362cc5caec91bdbd6c7f484acc687dc52d22acf4c1047f09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682725"
---
# <a name="removeresourcesettings-method-of-the-cim_virtualsystemmanagementservice-class"></a>Método RemoveResourceSettings de la clase \_ CIM VirtualSystemManagementService

Quita la configuración de recursos virtuales de una configuración del sistema virtual.

Cuando se aplica a partes de una configuración del sistema virtual "actual", como efecto secundario se pueden quitar los recursos del sistema virtual activo.

## <a name="syntax"></a>Sintaxis


```mof
uint32 RemoveResourceSettings(
  [in]  CIM_ResourceAllocationSettingData REF ResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ResourceSettings* \[ En\]
</dt> <dd>

Matriz de referencias a instancias de la clase [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) donde cada instancia representa la configuración de un recurso virtual dentro de una configuración del sistema virtual que se va a quitar.

</dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Si la operación es de larga duración, opcionalmente se puede devolver [**un \_ concretejob CIM**](cim-concretejob.md) que representa el trabajo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un 0 si se ejecuta correctamente; de lo contrario, devuelve un error.

<dl> <dt>

**Completado sin error** (0)
</dt> <dt>

**No compatible** (1)
</dt> <dt>

**Error** (2)
</dt> <dt>

**Tiempo de** espera (3)
</dt> <dt>

**Parámetro no válido** (4)
</dt> <dt>

**Estado no válido** (5)
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



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ VirtualSystemManagementService**](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




