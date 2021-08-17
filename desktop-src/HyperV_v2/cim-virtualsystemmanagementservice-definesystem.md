---
description: Define un sistema virtual.
ms.assetid: c3964e99-9227-4b98-af87-7caa59296306
title: Método DefineSystem de la CIM_VirtualSystemManagementService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.DefineSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a18145a2b59e1ba93967ad7f1d529466dfc1e6ac094b74d139a36fbe6f77a57a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068645"
---
# <a name="definesystem-method-of-the-cim_virtualsystemmanagementservice-class"></a>Método DefineSystem de la clase \_ CIM VirtualSystemManagementService

Define un sistema virtual.

La entrada que no se especifica completamente se puede rellenar con valores predeterminados.

## <a name="syntax"></a>Sintaxis


```mof
uint32 DefineSystem(
  [in]  string                           SystemSettings,
  [in]  string                           ResourceSettings[],
  [in]  CIM_VirtualSystemSettingData REF ReferenceConfiguration,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SystemSettings* \[ En\]
</dt> <dd>

Cadena que contiene una instancia incrustada de la clase [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) que se usa para definir los atributos del sistema virtual que se va a crear.

</dd> <dt>

*ResourceSettings* \[ En\]
</dt> <dd>

Matriz de cadenas que contiene una instancia incrustada de la clase [**\_ CIM ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) que describe los aspectos virtuales de un recurso virtual que se va a crear en el ámbito del nuevo sistema virtual.

</dd> <dt>

*ReferenceConfiguration* \[ En\]
</dt> <dd>

Referencia a una [**instancia de objeto CIM \_ VirtualSystemSettingDat**](cim-virtualsystemsettingdata.md) que es el objeto de nivel superior de una configuración del sistema virtual de referencia. La configuración de referencia se usa para complementar la configuración del nuevo sistema virtual si los parámetros *SystemSettings* y *ResourceSettings* no proporcionaron la información respectiva.

</dd> <dt>

*ResultingSystem* \[ out\]
</dt> <dd>

Si un sistema de equipos virtuales se define correctamente, se devuelve una referencia a una instancia de la clase [**CIM \_ ComputerSystem**](cim-computersystem.md) que representa el sistema de equipos virtuales recién definido.

</dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Si la operación es de larga duración, opcionalmente se puede devolver un trabajo. En este caso, la instancia de la clase [**CIM \_ ComputerSystem**](cim-computersystem.md) que representa el nuevo sistema virtual se presenta a través de la asociación [**CIM \_ AffectedJobElement**](cim-affectedjobelement.md) con la propiedad **AffectedElement** que hace referencia a la nueva instancia de la clase **CIM \_ ComputerSystem** y la propiedad **ElementEffects** establecida en 5 (Crear).

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

 

 




