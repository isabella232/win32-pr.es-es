---
description: 'Msvm_CollectedCollections clase : asocia Msvm VirtualSystemCollection a los objetos ComputerSystem de \_ Msvm \_ contenidos.'
ms.assetid: bbf7713a-b331-4b40-bcb4-3545c26c6f3a
title: Msvm_CollectedCollections clase
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
ms.openlocfilehash: c645bc4c6dbf7cf6f7b3fb43cc229af3ef744b264b088356d192e4ad58e68a88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790185"
---
# <a name="msvm_collectedcollections-class"></a>Clase Msvm \_ CollectedCollections

Asocia [**Msvm \_ VirtualSystemCollection a**](msvm-virtualsystemcollection.md) los objetos [**de Msvm \_ ComputerSystem contenidos.**](msvm-computersystem.md)

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

La **clase \_ CollectedCollections de Msvm** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ CollectedCollections de Msvm** tiene estas propiedades.

<dl> <dt>

**Colección**
</dt> <dd> <dl> <dt>

Tipo de datos: **Msvm \_ ManagementCollection**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")
</dt> </dl>

Objeto [**Msvm \_ ManagementCollection**](msvm-managementcollection.md) que agrupa o 'bag' que representa la colección.

</dd> <dt>

**Miembro**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ CollectionOfMSEs**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")
</dt> </dl>

Colección [**\_ CIMOfMSEs**](cim-collectionofmses.md) que contiene los miembros de la colección.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ CollectedMSEs**](cim-collectedmses.md)
</dt> </dl>

 

