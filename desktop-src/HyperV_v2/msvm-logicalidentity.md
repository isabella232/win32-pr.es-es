---
description: Asocia dos elementos administrados que representan distintos aspectos de la misma entidad subyacente.
ms.assetid: 107A2B15-09F2-490A-8AB2-F9FE5F6FEE60
title: Msvm_LogicalIdentity (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_LogicalIdentity
- Msvm_LogicalIdentity.SameElement
- Msvm_LogicalIdentity.SystemElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c2f8d2ee522fde3769c08bcbb78611b99eed8e16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545422"
---
# <a name="msvm_logicalidentity-class"></a>MSVM \_ LogicalIdentity (clase)

Asocia dos elementos administrados que representan distintos aspectos de la misma entidad subyacente. Esta clase deriva de [**\_ LogicalIdentity CIM**](/windows/desktop/CIMWin32Prov/cim-logicalidentity).

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_LogicalIdentity : CIM_LogicalIdentity
{
  CIM_LogicalElement REF SameElement;
  CIM_LogicalElement REF SystemElement;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ LogicalIdentity** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ LogicalIdentity** tiene estas propiedades.

<dl> <dt>

**SameElement**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ LogicalElement**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia a un aspecto alternativo de la entidad del sistema.

</dd> <dt>

**SystemElement**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ LogicalElement**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia a un aspecto del elemento lógico.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio Windows 8.1\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]<br/>                                                 |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_LOGICALIDENTITY CIM**](cim-logicalidentity.md)
</dt> <dt>

[**\_LOGICALIDENTITY CIM**](/windows/desktop/CIMWin32Prov/cim-logicalidentity)
</dt> </dl>

 

