---
description: Asocia el \_ VirtualSystemCollection MSVM a los objetos MSVM \_ ComputerSystem incluidos.
ms.assetid: bbf7713a-b331-4b40-bcb4-3545c26c6f3a
title: Msvm_CollectedCollections (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectedCollections
- Msvm_CollectedCollections.Collection
- Msvm_CollectedCollections.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 16ec6ad77c44e0a4e9001a0cb77d227573635ec6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669944"
---
# <a name="msvm_collectedcollections-class"></a>MSVM \_ CollectedCollections (clase)

Asocia el [**\_ VirtualSystemCollection MSVM**](msvm-virtualsystemcollection.md) a los objetos [**MSVM \_ ComputerSystem**](msvm-computersystem.md) incluidos.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedCollections : CIM_CollectedMSEs
{
  Msvm_ManagementCollection REF Collection;
  CIM_CollectionOfMSEs      REF Member;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ CollectedCollections** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ CollectedCollections** tiene estas propiedades.

<dl> <dt>

**Colección**
</dt> <dd> <dl> <dt>

Tipo de datos: **MSVM \_ ManagementCollection**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")
</dt> </dl>

Objeto de agrupación o contenedor de [**MSVM \_ ManagementCollection**](msvm-managementcollection.md) que representa la colección.

</dd> <dt>

**Member**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ CollectionOfMSEs**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("miembro")
</dt> </dl>

[**\_ CollectionOfMSEs de CIM**](cim-collectionofmses.md) que contiene los miembros de la colección.

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

 

