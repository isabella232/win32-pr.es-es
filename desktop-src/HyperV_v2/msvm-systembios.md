---
description: Se usa para asociar una máquina virtual a su BIOS.
ms.assetid: 494E9D9F-64D5-49D5-A6C7-ABE469ABA4CA
title: Msvm_SystemBIOS (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemBIOS
- Msvm_SystemBIOS.GroupComponent
- Msvm_SystemBIOS.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e1ad159a3ac0b86abd8b01e5c38105590ea8db0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153898"
---
# <a name="msvm_systembios-class"></a>MSVM \_ SystemBIOS (clase)

Se usa para asociar una máquina virtual a su BIOS.

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemBIOS : CIM_SystemBIOS
{
  CIM_ComputerSystem REF GroupComponent;
  Msvm_BIOSElement   REF PartComponent;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ SystemBIOS** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ SystemBIOS** tiene estas propiedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **CIM \_ ComputerSystem**](msvm-computersystem.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

La máquina virtual que se inicia desde el BIOS.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **MSVM \_ BIOSElement**](msvm-bioselement.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

BIOS asociado a la máquina virtual.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El acceso a la clase **MSVM \_ SystemBIOS** puede estar restringido por el filtrado de UAC. Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**\_SYSTEMBIOS CIM**](cim-systembios.md)
</dt> <dt>

[Clases de BIOS](bios-classes.md)
</dt> </dl>

 

