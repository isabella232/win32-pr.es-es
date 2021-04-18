---
description: Representa un controlador de protocolo que administra una interfaz SCSI.
ms.assetid: 01ef85fc-2f05-4453-b524-7d63b647f6fb
title: CIM_SCSIProtocolController (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SCSIProtocolController
- CIM_SCSIProtocolController.NameFormat
- CIM_SCSIProtocolController.OtherNameFormat
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d6479b405d3ca499615981d62744b1eaf25c7598
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686903"
---
# <a name="cim_scsiprotocolcontroller-class"></a>\_Clase SCSIProtocolController de CIM

Representa un controlador de protocolo que administra una interfaz SCSI.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, Version("2.8.1000"), UMLPackagePath("CIM::Device::ProtocolController"), AMENDMENT]
class CIM_SCSIProtocolController : CIM_ProtocolController
{
  uint16 NameFormat;
  string OtherNameFormat;
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ SCSIProtocolController** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ SCSIProtocolController** tiene estas propiedades.

<dl> <dt>

**NameFormat**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SCSIProtocolController**.**Name**","**CIM \_ SCSIProtocolController**.**OtherNameFormat**")
</dt> </dl>

El formato de la propiedad **Name** de la **\_ SCSIProtocolController CIM**.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otro** (1)


</dt> <dd></dd> <dt>

<span id="FC_Port_WWN"></span><span id="fc_port_wwn"></span><span id="FC_PORT_WWN"></span>

**WWN del puerto FC** (2)


</dt> <dd></dd> <dt>

<span id="iSCSI_Name"></span><span id="iscsi_name"></span><span id="ISCSI_NAME"></span>

**nombre iSCSI** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**OtherNameFormat**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SCSIProtocolController**.**Name**","**CIM \_ SCSIProtocolController**.**NameFormat**")
</dt> </dl>

Una descripción de la propiedad **nameFormat** cuando **NameFormat** se establece en "1" (otro).

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

[**\_PROTOCOLCONTROLLER CIM**](cim-protocolcontroller.md)
</dt> </dl>

 

