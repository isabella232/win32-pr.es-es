---
description: Asocia dos elementos administrados que representan distintos aspectos de la misma entidad subyacente.
ms.assetid: 107A2B15-09F2-490A-8AB2-F9FE5F6FEE60
title: Msvm_LogicalIdentity clase
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
ms.openlocfilehash: 12ee48b85ae11b10a24bab35001baa45c8382105158050d110eb7448a8e883e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148368"
---
# <a name="msvm_logicalidentity-class"></a>Clase LogicalIdentity de Msvm \_

Asocia dos elementos administrados que representan distintos aspectos de la misma entidad subyacente. Esta clase se deriva de [**CIM \_ LogicalIdentity**](/windows/desktop/CIMWin32Prov/cim-logicalidentity).

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

La **clase Msvm \_ LogicalIdentity** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Msvm \_ LogicalIdentity** tiene estas propiedades.

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
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                                                 |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ LogicalIdentity**](cim-logicalidentity.md)
</dt> <dt>

[**CIM \_ LogicalIdentity**](/windows/desktop/CIMWin32Prov/cim-logicalidentity)
</dt> </dl>

 

