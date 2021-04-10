---
description: La \_ clase CIM ErrorCountersForDevice asocia la \_ clase DEVICEERRORCOUNTS de CIM al dispositivo lógico al que se aplica.
ms.assetid: 200971ab-df85-4a45-beb3-4ffe11ce92dc
ms.tgt_platform: multiple
title: CIM_ErrorCountersForDevice (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ErrorCountersForDevice
- CIM_ErrorCountersForDevice.Element
- CIM_ErrorCountersForDevice.Stats
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7c4e11b1f58cae7b544b251044657bb737525b37
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907298"
---
# <a name="cim_errorcountersfordevice-class"></a>\_Clase ErrorCountersForDevice de CIM

La clase **CIM \_ ErrorCountersForDevice** asocia la clase [**\_ DeviceErrorCounts de CIM**](cim-deviceerrorcounts.md) al dispositivo lógico al que se aplica.

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{2D79F3A0-D025-11d2-85F5-0000F8102E5F}"), AMENDMENT]
class CIM_ErrorCountersForDevice : CIM_Statistics
{
  CIM_LogicalDevice     REF Element;
  CIM_DeviceErrorCounts REF Stats;
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ ErrorCountersForDevice** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ ErrorCountersForDevice** tiene estas propiedades.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ LogicalDevice de CIM**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Un [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) que describe el dispositivo al que se aplican los contadores de errores.

</dd> <dt>

**Stats**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ DeviceErrorCounts**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("estadísticas"), [**débil**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Un [**\_ DeviceErrorCounts de CIM**](cim-deviceerrorcounts.md) que describe el objeto estadístico (en este caso, la clase de contador de errores).

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase **CIM \_ ErrorCountersForDevice** se hereda de [**las \_ estadísticas CIM**](cim-statistics.md).

WMI no implementa esta clase.

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estadísticas de CIM \_**](cim-statistics.md)
</dt> </dl>

 

