---
description: Define un sistema virtual.
ms.assetid: c3964e99-9227-4b98-af87-7caa59296306
title: Método DefineSystem de la clase CIM_VirtualSystemManagementService
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
ms.openlocfilehash: 2e38111d52044ed385fdd8cd19dd9094834e794c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687340"
---
# <a name="definesystem-method-of-the-cim_virtualsystemmanagementservice-class"></a>Método DefineSystem de la \_ clase VirtualSystemManagementService de CIM

Define un sistema virtual.

La entrada que no se ha especificado completamente puede rellenarse con valores predeterminados.

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

*Configuración* \[ de\]
</dt> <dd>

Cadena que contiene una instancia incrustada de la clase [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) que se utiliza para definir los atributos del sistema virtual que se va a crear.

</dd> <dt>

*ResourceSettings* \[ de\]
</dt> <dd>

Matriz de cadenas que contiene una instancia incrustada de la clase [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) que describe los aspectos virtuales de un recurso virtual que se va a crear en el ámbito del nuevo sistema virtual.

</dd> <dt>

*ReferenceConfiguration* \[ de\]
</dt> <dd>

Referencia a una instancia del objeto [**\_ VirtualSystemSettingDat de CIM**](cim-virtualsystemsettingdata.md) que es el objeto de nivel superior de una configuración de sistema virtual de referencia. La configuración de referencia se utiliza para complementar la configuración del nuevo sistema virtual si los parámetros *configuración* y *ResourceSettings* no proporcionaron la información correspondiente.

</dd> <dt>

*ResultingSystem* \[ enuncia\]
</dt> <dd>

Si un equipo virtual se define correctamente, se devuelve una referencia a una instancia de la clase [**CIM \_ ComputerSystem**](cim-computersystem.md) que representa el sistema del equipo virtual recién definido.

</dd> <dt>

*Trabajo* \[ de enuncia\]
</dt> <dd>

Si la operación es de larga ejecución, opcionalmente se puede devolver un trabajo. En este caso, la instancia de la [**clase CIM \_ ComputerSystem**](cim-computersystem.md) que representa el nuevo sistema virtual se presenta a través de la Asociación [**CIM \_ AffectedJobElement**](cim-affectedjobelement.md) con la propiedad **AffectedElement** que hace referencia a la nueva instancia de la clase **CIM \_ ComputerSystem** y la propiedad **ElementEffects** establecida en 5 (Create).

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

 

 




