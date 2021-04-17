---
description: Modifica la configuración de recursos virtuales.
ms.assetid: 4942f167-0e53-4ae2-b973-4a06b636b44a
title: Método ModifyResourceSettings de la clase CIM_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.ModifyResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e27729429d02c2412e05344779cc40461dbd9dfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497776"
---
# <a name="modifyresourcesettings-method-of-the-cim_virtualsystemmanagementservice-class"></a>Método ModifyResourceSettings de la \_ clase VirtualSystemManagementService de CIM

Modifica la configuración de recursos virtuales.

Cuando se aplica a partes de una configuración de sistema virtual "actual", es posible que se modifiquen los recursos de efecto secundario del sistema virtual activo.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ModifyResourceSettings(
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ResourceSettings* \[ de\]
</dt> <dd>

Matriz de cadenas que contiene una instancia incrustada de la clase [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) que describe las modificaciones de los aspectos virtuales de un recurso virtual existente. Todas las instancias deben tener un **InstanceID** válido para poder identificar la configuración de recursos virtuales que se va a modificar.

</dd> <dt>

*ResultingResourceSettings* \[ enuncia\]
</dt> <dd>

Matriz de referencias a instancias de la clase [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) que representan aspectos virtuales de los recursos virtuales modificados.

</dd> <dt>

*Trabajo* \[ de enuncia\]
</dt> <dd>

Si la operación es de larga ejecución, opcionalmente se devuelve un trabajo. En este caso, las instancias de la clase [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) que representan la configuración de recursos modificada están disponibles a través de la Asociación **CIM \_ ConreteComponent** desde la instancia de la clase [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) que representa la configuración del sistema virtual afectada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un error.

<dl> <dt>

**Completado sin error** (0)
</dt> <dt>

**No compatible** (1)
</dt> <dt>

**Error** (2)
</dt> <dt>

**Tiempo de espera** (3)
</dt> <dt>

**Parámetro no válido** (4)
</dt> <dt>

**Estado no válido** (5)
</dt> <dt>

**Parámetros incompatibles** (6)
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

[**\_VIRTUALSYSTEMMANAGEMENTSERVICE CIM**](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




