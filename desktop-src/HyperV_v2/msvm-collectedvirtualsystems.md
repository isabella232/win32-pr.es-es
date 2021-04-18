---
description: Asocia el \_ VirtualSystemCollection MSVM a los objetos MSVM \_ ComputerSystem incluidos.
ms.assetid: ad783188-b60a-4271-aa2d-8050c36e70eb
title: Msvm_CollectedVirtualSystems (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectedVirtualSystems
- Msvm_CollectedVirtualSystems.Collection
- Msvm_CollectedVirtualSystems.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0803eda14ffbaf21ee2bf4491bd835123b7191e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688371"
---
# <a name="msvm_collectedvirtualsystems-class"></a>MSVM \_ CollectedVirtualSystems (clase)

Asocia el [**\_ VirtualSystemCollection MSVM**](msvm-virtualsystemcollection.md) a los objetos [**MSVM \_ ComputerSystem**](msvm-computersystem.md) incluidos.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedVirtualSystems : CIM_CollectedMSEs
{
  Msvm_VirtualSystemCollection REF Collection;
  Msvm_ComputerSystem          REF Member;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ CollectedVirtualSystems** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ CollectedVirtualSystems** tiene estas propiedades.

<dl> <dt>

**Colección**
</dt> <dd> <dl> <dt>

Tipo de datos: **MSVM \_ VirtualSystemCollection**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")
</dt> </dl>

Objeto de agrupación o contenedor de [**MSVM \_ VirtualSystemCollection**](msvm-virtualsystemcollection.md) que representa la colección.

</dd> <dt>

**Member**
</dt> <dd> <dl> <dt>

Tipo de datos: **MSVM \_ ComputerSystem**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("miembro")
</dt> </dl>

Objeto [**\_ ComputerSystem MSVM**](msvm-computersystem.md) que contiene los miembros de la colección.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_COLLECTEDMSES CIM**](cim-collectedmses.md)
</dt> </dl>

 

