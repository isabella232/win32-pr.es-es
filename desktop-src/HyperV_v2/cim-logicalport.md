---
description: Abstracción de un puerto o punto de conexión de un dispositivo.
ms.assetid: ee725c64-587b-4e5f-9b1c-7a58902b0631
title: CIM_LogicalPort (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalPort
- CIM_LogicalPort.Speed
- CIM_LogicalPort.MaxSpeed
- CIM_LogicalPort.RequestedSpeed
- CIM_LogicalPort.UsageRestriction
- CIM_LogicalPort.PortType
- CIM_LogicalPort.OtherPortType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: eeed69e9669048377340cb0ca21e7a2e89f4baff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000899"
---
# <a name="cim_logicalport-class"></a>\_Clase LogicalPort de CIM

Abstracción de un puerto o punto de conexión de un dispositivo.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Ports"), AMENDMENT]
class CIM_LogicalPort : CIM_LogicalDevice
{
  uint64 Speed;
  uint64 MaxSpeed;
  uint64 RequestedSpeed;
  uint16 UsageRestriction;
  uint16 PortType;
  string OtherPortType;
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ LogicalPort** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ LogicalPort** tiene estas propiedades.

<dl> <dt>

**MaxSpeed**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits por segundo"), **punitivo** ("bit por segundo")
</dt> </dl>

Ancho de banda máximo del puerto, en bits por segundo.

</dd> <dt>

**OtherPortType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ LogicalPort**.**PortType**")
</dt> </dl>

Describe el tipo de módulo, cuando **portType** se establece en **other** ("1").

</dd> <dt>

**PortType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ NetworkPort**](cim-networkport.md).**OtherNetworkPortType**")
</dt> </dl>

El tipo de puerto.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otro** (1)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**No aplicable** (2)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (3.. 15999)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Proveedor reservado** (16000.. 65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**RequestedSpeed**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits por segundo"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ LogicalPort CIM**.**Speed**"), **punitivo** (" bit/segundo ")
</dt> </dl>

Ancho de banda solicitado del puerto, en bits por segundo. El ancho de banda real se registra en la propiedad **Speed** .

</dd> <dt>

**Velocidad**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits por segundo"), **punitivo** ("bit por segundo")
</dt> </dl>

Ancho de banda del puerto, en bits por segundo.

</dd> <dt>

**UsageRestriction**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el puerto está restringido a ser un puerto front-end o back-end.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>

**Solo front-end** (2)


</dt> <dd></dd> <dt>

<span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>

**Solo back-end** (3)


</dt> <dd></dd> <dt>

<span id="Not_restricted"></span><span id="not_restricted"></span><span id="NOT_RESTRICTED"></span>

**No restringido** (4)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                          |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LogicalDevice de CIM \_**](cim-logicaldevice.md)
</dt> </dl>

 

