---
description: Representa una asociación entre un objeto StorageExtent CIM de nivel superior \_ y un objeto STORAGEEXTENT CIM de nivel inferior \_ . Por ejemplo, un \_ objeto de CIM ProtectedSpaceExtent forma parte de un \_ objeto PHYSICALEXTENT de CIM.
ms.assetid: 40a88927-981b-4fc4-af5f-be91d9933284
title: CIM_BasedOn (clase, administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BasedOn
- CIM_BasedOn.Antecedent
- CIM_BasedOn.Dependent
- CIM_BasedOn.StartingAddress
- CIM_BasedOn.EndingAddress
- CIM_BasedOn.OrderIndex
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 47d2e44d1106eba57f4c46c0957662c348c9ca1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907898"
---
# <a name="cim_basedon-class-hyper-v-management"></a>CIM_BasedOn (clase, administración de Hyper-V)

Representa una asociación entre un objeto **\_ StorageExtent CIM** de nivel superior y un objeto **\_ StorageExtent CIM** de nivel inferior. Por ejemplo, un objeto de [**CIM \_ ProtectedSpaceExtent**](/windows/desktop/CIMWin32Prov/cim-protectedspaceextent) forma parte de un objeto [**\_ PhysicalExtent de CIM**](/windows/desktop/CIMWin32Prov/cim-physicalextent) .

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Core::StorageExtent"), AMENDMENT]
class CIM_BasedOn : CIM_Dependency
{
  CIM_StorageExtent REF Antecedent;
  CIM_StorageExtent REF Dependent;
  uint64                StartingAddress;
  uint64                EndingAddress;
  uint16                OrderIndex;
};
```

## <a name="members"></a>Miembros

La **clase \_ basada en CIM** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ basada en CIM** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ StorageExtent**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")
</dt> </dl>

Objeto StorageExtent de **CIM \_** de nivel inferior.

</dd> <dt>

**Dependientes**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ StorageExtent**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")
</dt> </dl>

Objeto StorageExtent de **CIM \_** de nivel superior.

</dd> <dt>

**EndingAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La dirección que indica en qué lugar de almacenamiento de nivel inferior se termina el objeto **\_ StorageExtent CIM** de nivel superior. Esta propiedad es útil cuando se asignan objetos **\_ StorageExtent CIM** no contiguos en una agrupación de nivel superior.

</dd> <dt>

**OrderIndex**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Índice que se usa para especificar el orden de las **asociaciones \_ basadas en CIM** en una colección; de lo contrario, "0" indica que no hay orden. **CIM \_** Las instancias basadas en con el mismo valor dependiente deben colocar valores únicos en la propiedad **OrderIndex** . El valor de **OrderIndex** más bajo especifica el primer miembro de la colección.

Un ejemplo del uso de esta propiedad es definir una matriz seccionada RAID-0 de 3 discos. La matriz RAID resultante es una extensión de almacenamiento que depende de las extensiones de almacenamiento que describen cada uno de los tres discos. El valor **OrderIndex** de cada **Asociación \_ basada en CIM** de las extensiones de disco a la matriz RAID podría especificarse como 1, 2 y 3 para indicar el orden en el que se usan las extensiones de disco para tener acceso a los datos de RAID.

</dd> <dt>

**StartingAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La dirección que indica en qué lugar de almacenamiento de nivel inferior se inicia el objeto **\_ StorageExtent CIM** de nivel superior.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                          |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Dependencia de CIM \_**](cim-dependency.md)
</dt> </dl>

 

