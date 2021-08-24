---
description: La clase CIM ErrorCountersForDevice asocia la clase \_ DeviceErrorCounts de CIM al dispositivo lógico al \_ que se aplica.
ms.assetid: 200971ab-df85-4a45-beb3-4ffe11ce92dc
ms.tgt_platform: multiple
title: CIM_ErrorCountersForDevice clase
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
ms.openlocfilehash: c0c978e3f21cf1596f257f8e9942fc426cfd62b8ce73746d7331b8ee000839bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119080649"
---
# <a name="cim_errorcountersfordevice-class"></a>Cim \_ ErrorCountersForDevice (clase)

La **clase CIM \_ ErrorCountersForDevice** asocia la clase [**\_ DeviceErrorCounts de CIM**](cim-deviceerrorcounts.md) al dispositivo lógico al que se aplica.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de la versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

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

La **clase CIM \_ ErrorCountersForDevice** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase CIM \_ ErrorCountersForDevice** tiene estas propiedades.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ Cim LogicalDevice**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Un [**dispositivo \_ lógico CIM**](cim-logicaldevice.md) que describe el dispositivo al que se aplican los contadores de errores.

</dd> <dt>

**Stats**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ DeviceErrorCounts**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Stats"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Cim [**\_ DeviceErrorCounts**](cim-deviceerrorcounts.md) describe el objeto estadístico; en este caso, la clase de contador de errores.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase CIM \_ ErrorCountersForDevice** se hereda de [**cim \_ statistics**](cim-statistics.md).

WMI no implementa esta clase.

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Estadísticas de CIM \_**](cim-statistics.md)
</dt> </dl>

 

