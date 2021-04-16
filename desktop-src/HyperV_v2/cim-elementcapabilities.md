---
description: Representa una asociación entre un elemento administrado y sus capacidades.
ms.assetid: 0e080042-4a56-40b7-acc5-cf69eb2a0604
title: CIM_ElementCapabilities (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementCapabilities
- CIM_ElementCapabilities.ManagedElement
- CIM_ElementCapabilities.Capabilities
- CIM_ElementCapabilities.Characteristics
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7c705d0bb4743d4919ca840f51b3324510558078
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687033"
---
# <a name="cim_elementcapabilities-class"></a>\_Clase ElementCapabilities de CIM

Representa una asociación entre un elemento administrado y sus capacidades.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Abstract, Version("2.24.0"), UMLPackagePath("CIM::Core::Capabilities"), AMENDMENT]
class CIM_ElementCapabilities
{
  CIM_ManagedElement REF ManagedElement;
  CIM_Capabilities   REF Capabilities;
  uint16                 Characteristics[];
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ ElementCapabilities** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ ElementCapabilities** tiene estas propiedades.

<dl> <dt>

**Capabilities**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ capacidades de CIM**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Las capacidades asociadas al elemento administrado.

</dd> <dt>

**Características**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Un conjunto de información descriptiva sobre las capacidades.

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

**Predeterminado** (2)


</dt> <dd></dd> <dt>

<span id="Current"></span><span id="current"></span><span id="CURRENT"></span>

**Actual** (3)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

**Específico del proveedor** (32768... 65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**ManagedElement**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ ManagedElement**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**mín**](/windows/desktop/WmiSdk/standard-qualifiers) . (1)
</dt> </dl>

Elemento administrado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                          |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

