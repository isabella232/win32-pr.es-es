---
description: Agrega recursos a una configuración del sistema virtual.
ms.assetid: c2541571-74f0-48f8-997c-56c152980eea
title: Método AddResourceSettings de la CIM_VirtualSystemManagementService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.AddResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0387d3d46723aede1d0858d647a555db57b3de28e6c1fb5fbb68b6d56342fcb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118646473"
---
# <a name="addresourcesettings-method-of-the-cim_virtualsystemmanagementservice-class"></a>Método AddResourceSettings de la clase \_ CIM VirtualSystemManagementService

Agrega recursos a una configuración del sistema virtual.

Cuando se aplica a una configuración del sistema virtual de "estado", como efecto secundario se agregan recursos al sistema virtual activo.

## <a name="syntax"></a>Sintaxis


```mof
uint32 AddResourceSettings(
  [in]  CIM_VirtualSystemSettingData      REF AffectedConfiguration,
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*AffectedConfiguration* \[ En\]
</dt> <dd>

Una [**referencia CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) a la configuración del sistema virtual afectada.

</dd> <dt>

*ResourceSettings* \[ En\]
</dt> <dd>

Matriz de cadenas que contiene una instancia incrustada de la clase [**\_ CIM ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) que describe los aspectos virtuales de un recurso virtual que se va a agregar al sistema virtual.

</dd> <dt>

*ResultingResourceSettings* \[ out\]
</dt> <dd>

Matriz de referencias a instancias de la clase [**\_ CIM ResourceAllocationSettingData que**](cim-resourceallocationsettingdata.md) representa aspectos virtuales de los recursos virtuales agregados.

</dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Si la operación es de larga duración, opcionalmente se puede devolver un trabajo. En este caso, las instancias de la clase [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) que representan la configuración de recursos agregada están disponibles a través de la asociación **CIM \_ ConreteComponent desde** la instancia de la clase CIM [**\_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) que representa la configuración del sistema virtual afectada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor 0 si se ejecuta correctamente; de lo contrario, devuelve un error.

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

 

 




