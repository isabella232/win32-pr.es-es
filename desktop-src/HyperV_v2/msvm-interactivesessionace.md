---
description: Representa una entrada de control de acceso (ACE) que determina el acceso a la sesión interactiva de una máquina virtual.
ms.assetid: dfec83d6-8033-47b5-aa6f-fc7447a29f43
title: Msvm_InteractiveSessionACE (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_InteractiveSessionACE
- Msvm_InteractiveSessionACE.Trustee
- Msvm_InteractiveSessionACE.AccessType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6c4b63e769b04092323cd2da7362ef6b156886b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686935"
---
# <a name="msvm_interactivesessionace-class"></a>MSVM \_ InteractiveSessionACE (clase)

Representa una *entrada de control de acceso* (ACE) que determina el acceso a la sesión interactiva de una máquina virtual.

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_InteractiveSessionACE
{
  string Trustee;
  uint16 AccessType;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ InteractiveSessionACE** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ InteractiveSessionACE** tiene estas propiedades.

<dl> <dt>

**AccessType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la ACE concede o deniega el acceso al administrador de confianza.

<dt>

<span id="Access_Allowed"></span><span id="access_allowed"></span><span id="ACCESS_ALLOWED"></span>

**Acceso permitido** (0)


</dt> <dd></dd> <dt>

<span id="Access_Denied"></span><span id="access_denied"></span><span id="ACCESS_DENIED"></span>

**Acceso denegado** (1)


</dt> <dd></dd> </dl>

</dd> <dt>

**Confianza**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identifica la entidad de seguridad a la que la ACE concede o deniega el acceso. Los formatos válidos para esta propiedad incluyen el formato de nombre de usuario compatible con SAM de Windows y el formato de cadena SID de Windows.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetInteractiveSessionACL**](getinteractivesessionacl-msvm-terminalservice.md)
</dt> </dl>

 

 




