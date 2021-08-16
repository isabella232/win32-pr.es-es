---
description: Se usa para asociar una máquina virtual a su BIOS.
ms.assetid: 494E9D9F-64D5-49D5-A6C7-ABE469ABA4CA
title: Msvm_SystemBIOS clase
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
ms.openlocfilehash: d7656ab14a206e11f444cdb406c1ff7c820ad737d9744cd9030875448b383650
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118391901"
---
# <a name="msvm_systembios-class"></a>Clase SystemBIOS de Msvm \_

Se usa para asociar una máquina virtual a su BIOS.

La sintaxis siguiente se simplifica Managed Object Format (MOF) e incluye todas las propiedades heredadas.

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

La **clase \_ SystemBIOS de Msvm** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ SystemBIOS de Msvm** tiene estas propiedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **CIM \_ ComputerSystem**](msvm-computersystem.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Máquina virtual que se inicia desde el BIOS.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **Msvm \_ BIOSElement**](msvm-bioselement.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

BIOS asociado a la máquina virtual.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El acceso a la **clase \_ SystemBIOS de Msvm** podría estar restringido por el filtrado de UAC. Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CIM \_ SystemBIOS**](cim-systembios.md)
</dt> <dt>

[Clases de BIOS](bios-classes.md)
</dt> </dl>

 

