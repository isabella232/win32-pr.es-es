---
description: 'Método ModifyResourceSettings de la clase CIM_VirtualSystemManagementService: modifica la configuración de recursos virtuales.'
ms.assetid: 4942f167-0e53-4ae2-b973-4a06b636b44a
title: Método ModifyResourceSettings de la CIM_VirtualSystemManagementService clase
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
ms.openlocfilehash: 26971c80ce6f7d0ffcdcef069d76aef5fdc15138
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112293"
---
# <a name="modifyresourcesettings-method-of-the-cim_virtualsystemmanagementservice-class"></a>Método ModifyResourceSettings de la clase \_ CIM VirtualSystemManagementService

Modifica la configuración de recursos virtuales.

Cuando se aplica a partes de una configuración del sistema virtual "actual", como efecto secundario se pueden modificar los recursos del sistema virtual activo.

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

*ResourceSettings* \[ En\]
</dt> <dd>

Matriz de cadenas que contiene una instancia incrustada de la clase [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) que describe las modificaciones en los aspectos virtuales de un recurso virtual existente. Todas las instancias deben tener un **instanceID** válido para identificar la configuración del recurso virtual que se va a modificar.

</dd> <dt>

*ResultingResourceSettings* \[ out\]
</dt> <dd>

Matriz de referencias a instancias de la clase [**CIM \_ ResourceAllocationSettingData que**](cim-resourceallocationsettingdata.md) representa aspectos virtuales de los recursos virtuales modificados.

</dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Si la operación es de larga duración, opcionalmente se devuelve un trabajo. En este caso, las instancias de la clase [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) que representan la configuración de recursos modificada están disponibles a través de la asociación **CIM \_ ConreteComponent** desde la instancia de la clase [**CIM \_ VirtualSystemSettingData que representa**](cim-virtualsystemsettingdata.md) la configuración del sistema virtual afectada.

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

**Estado no válido** (5)
</dt> <dt>

**Parámetros incompatibles** (6)
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

[**CIM \_ VirtualSystemManagementService**](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




