---
description: 'Msvm_CollectedCollections clase : asocia Msvm \_ VirtualSystemCollection a los objetos ComputerSystem de Msvm \_ contenidos.'
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
ms.openlocfilehash: 83719d364fac22923d68206c8cfe7d37adad5edb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112133"
---
# <a name="msvm_collectedcollections-class"></a>Clase Msvm \_ CollectedCollections

Asocia [**Msvm \_ VirtualSystemCollection a**](msvm-virtualsystemcollection.md) los objetos [**\_ ComputerSystem de Msvm**](msvm-computersystem.md) contenidos.

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

Una [**agrupación \_ Msvm ManagementCollection**](msvm-managementcollection.md) o un objeto "bag" que representa la colección.

</dd> <dt>

**Member**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ Cim CollectionOfMSEs**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")
</dt> </dl>

Colección [**\_ CIMOfMSE**](cim-collectionofmses.md) que contiene los miembros de la colección.

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

 

