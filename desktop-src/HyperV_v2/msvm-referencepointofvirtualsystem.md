---
description: Asocia Msvm \_ VirtualSystemReferencePoint a los objetos Msvm \_ VirtualSystem correspondientes.
ms.assetid: 5a9cb099-c0ae-4088-a64c-f2720a6cb9c8
title: Msvm_ReferencePointOfVirtualSystem clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReferencePointOfVirtualSystem
- Msvm_ReferencePointOfVirtualSystem.Antecedent
- Msvm_ReferencePointOfVirtualSystem.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d9224e0ce51608904f7cf2459dc3d1341d84dd005bd8fe4daee5707d22b38163
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789595"
---
# <a name="msvm_referencepointofvirtualsystem-class"></a>Clase Msvm \_ ReferencePointOfVirtualSystem

Asocia [**Msvm \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) a los objetos [**Msvm \_ VirtualSystem**](msvm-virtualsystemresourcecomponent.md) correspondientes.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReferencePointOfVirtualSystem : CIM_Dependency
{
  Msvm_ComputerSystem              REF Antecedent;
  Msvm_VirtualSystemReferencePoint REF Dependent;
};
```

## <a name="members"></a>Miembros

La **clase \_ ReferencePointOfVirtualSystem de Msvm** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Msvm \_ ReferencePointOfVirtualSystem** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **Msvm \_ ComputerSystem**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedentes")
</dt> </dl>

[**Msvm \_ ComputerSystem que**](msvm-computersystem.md) representa el objeto independiente de esta asociación.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **Msvm \_ VirtualSystemReferencePoint**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")
</dt> </dl>

Objeto [**\_ VirtualSystemReferencePoint de Msvm**](msvm-virtualsystemreferencepoint.md) que representa el objeto que depende del **antecedente**.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Dependencia \_ cim**](cim-dependency.md)
</dt> </dl>

 

