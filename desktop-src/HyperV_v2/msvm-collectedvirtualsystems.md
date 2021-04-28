---
description: 'Msvm_CollectedVirtualSystems clase : asocia Msvm \_ VirtualSystemCollection a los objetos ComputerSystem de Msvm \_ contenidos.'
ms.assetid: ad783188-b60a-4271-aa2d-8050c36e70eb
title: Msvm_CollectedVirtualSystems clase
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
ms.openlocfilehash: d6775f41a6e2ae7e45bac642fcd32b8deaec3fda
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119283"
---
# <a name="msvm_collectedvirtualsystems-class"></a>Clase Msvm \_ CollectedVirtualSystems

Asocia [**Msvm \_ VirtualSystemCollection a**](msvm-virtualsystemcollection.md) los objetos [**\_ Msvm ComputerSystem contenidos.**](msvm-computersystem.md)

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

La **clase Msvm \_ CollectedVirtualSystems** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Msvm \_ CollectedVirtualSystems** tiene estas propiedades.

<dl> <dt>

**Colección**
</dt> <dd> <dl> <dt>

Tipo de datos: **Msvm \_ VirtualSystemCollection**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")
</dt> </dl>

Objeto [**Msvm \_ VirtualSystemCollection**](msvm-virtualsystemcollection.md) que agrupa o "bag" que representa la colección.

</dd> <dt>

**Member**
</dt> <dd> <dl> <dt>

Tipo de datos: **Msvm \_ ComputerSystem**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")
</dt> </dl>

Objeto [**\_ ComputerSystem de Msvm**](msvm-computersystem.md) que contiene los miembros de la colección.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10 solo \[ aplicaciones de escritorio\]<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CIM \_ CollectedMSEs**](cim-collectedmses.md)
</dt> </dl>

 

