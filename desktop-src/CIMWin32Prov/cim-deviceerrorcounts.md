---
description: La \_ clase CIM DeviceErrorCounts es una clase estadística que contiene contadores relacionados con errores para un dispositivo lógico. Los tipos de errores se definen mediante CCITt (REC X. 733) e ISO (IEC 10164-4).
ms.assetid: d65cbc78-40f2-4846-bd47-76e04b2f588b
ms.tgt_platform: multiple
title: CIM_DeviceErrorCounts (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceErrorCounts
- CIM_DeviceErrorCounts.Caption
- CIM_DeviceErrorCounts.Description
- CIM_DeviceErrorCounts.CriticalErrorCount
- CIM_DeviceErrorCounts.DeviceCreationClassName
- CIM_DeviceErrorCounts.DeviceID
- CIM_DeviceErrorCounts.Name
- CIM_DeviceErrorCounts.IndeterminateErrorCount
- CIM_DeviceErrorCounts.MajorErrorCount
- CIM_DeviceErrorCounts.MinorErrorCount
- CIM_DeviceErrorCounts.SystemCreationClassName
- CIM_DeviceErrorCounts.SystemName
- CIM_DeviceErrorCounts.WarningCount
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1602e68b7254811ba8c09726feda8baa7bf23d29
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000693"
---
# <a name="cim_deviceerrorcounts-class"></a>\_Clase DeviceErrorCounts de CIM

La clase **CIM \_ DeviceErrorCounts** es una clase estadística que contiene contadores relacionados con errores para un dispositivo lógico. Los tipos de errores se definen mediante CCITt (REC X. 733) e ISO (IEC 10164-4).

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{117FDB8C-D025-11d2-85F5-0000F8102E5F}"), AMENDMENT]
class CIM_DeviceErrorCounts : CIM_StatisticalInformation
{
  string Caption;
  string Description;
  uint64 CriticalErrorCount;
  string DeviceCreationClassName;
  string DeviceID;
  string Name;
  uint64 IndeterminateErrorCount;
  uint64 MajorErrorCount;
  uint64 MinorErrorCount;
  string SystemCreationClassName;
  string SystemName;
  uint64 WarningCount;
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ DeviceErrorCounts** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase **CIM \_ DeviceErrorCounts** tiene estos métodos.



| Método                                                                     | Descripción                                                               |
|:---------------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [**ResetCounter**](resetcounter-method-in-class-cim-deviceerrorcounts.md) | Restablece los contadores de error y ADVERTENCIA. No implementado por WMI.<br/> |



 

### <a name="properties"></a>Propiedades

La clase **CIM \_ DeviceErrorCounts** tiene estas propiedades.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Breve descripción textual de la estadística o la métrica.

Esta propiedad se hereda de [**\_ StatisticalInformation CIM**](cim-statisticalinformation.md).

</dd> <dt>

**CriticalErrorCount**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,7 ")
</dt> </dl>

Recuento de los errores críticos.

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción textual de la estadística o la métrica.

Esta propiedad se hereda de [**\_ StatisticalInformation CIM**](cim-statisticalinformation.md).

</dd> <dt>

**DeviceCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ LogicalDevice de CIM**](cim-logicaldevice.md).**CreationClassName**"), [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Propiedad **CreationClassName** del dispositivo de ámbito.

</dd> <dt>

**ID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ LogicalDevice de CIM**](cim-logicaldevice.md).**DeviceID**"), [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Identificador del dispositivo de ámbito.

</dd> <dt>

**IndeterminateErrorCount**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Recuento de los errores indeterminados.

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**MajorErrorCount**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,8 ")
</dt> </dl>

Recuento de los errores principales.

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**MinorErrorCount**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Recuento de los errores menores.

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre"), [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

La propiedad de nombre heredado sirve como parte de la clave de la instancia de **\_ DeviceErrorCounts de CIM** . El ámbito del objeto es el dispositivo lógico al que se aplican las estadísticas.

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ LogicalDevice de CIM**](cim-logicaldevice.md).**SystemCreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

El ámbito de **CreationClassName** del sistema.

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ LogicalDevice de CIM**](cim-logicaldevice.md).**SystemName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Propiedad de **nombre** del sistema de ámbito.

</dd> <dt>

**WarningCount**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,9 ")
</dt> </dl>

Recuento de las advertencias.

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Observaciones

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

[**\_STATISTICALINFORMATION CIM**](cim-statisticalinformation.md)
</dt> </dl>

 

