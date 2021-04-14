---
description: Asociación que describe cómo se pueden ensamblar las extensiones de almacenamiento de las extensiones de nivel inferior.
ms.assetid: 8be9bb2c-ef46-454b-bfc3-0398c64d17b7
title: Msvm_BasedOn (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BasedOn
- Msvm_BasedOn.Antecedent
- Msvm_BasedOn.Dependent
- Msvm_BasedOn.StartingAddress
- Msvm_BasedOn.EndingAddress
- Msvm_BasedOn.OrderIndex
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8262ae5e510574bf02630410b584d9df10d64ecf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668430"
---
# <a name="msvm_basedon-class"></a>MSVM \_ BasedOn (clase)

Asociación que describe cómo se pueden ensamblar las extensiones de almacenamiento de las extensiones de nivel inferior. Por ejemplo, ProtectedSpaceExtents son partes de PhysicalExtents, mientras que VolumeSets se ensamblan desde uno o varios físicos o ProtectedSpaceExtents. Como otro ejemplo, CacheMemory puede definirse de forma independiente y realizarse en un PhysicalElement o puede basarse en volatile o NonVolatileStorageExtents.

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BasedOn : CIM_BasedOn
{
  CIM_StorageExtent REF Antecedent;
  CIM_StorageExtent REF Dependent;
  uint64                StartingAddress;
  uint64                EndingAddress;
  uint16                OrderIndex;
};
```

## <a name="members"></a>Miembros

La **clase \_ basada en MSVM** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ basada en MSVM** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La extensión de almacenamiento de nivel inferior. Esta propiedad se hereda de [**\_ BasedOn CIM**](/windows/desktop/CIMWin32Prov/cim-basedon).

</dd> <dt>

**Dependientes**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La extensión de almacenamiento de nivel superior. Esta propiedad se hereda de [**\_ BasedOn CIM**](/windows/desktop/CIMWin32Prov/cim-basedon).

</dd> <dt>

**EndingAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Dirección final en la que finaliza la extensión de nivel superior en el almacenamiento de nivel inferior. Esta propiedad es útil cuando se asignan extensiones no contiguas en una agrupación de nivel superior. Esta propiedad se hereda de [**\_ BasedOn CIM**](/windows/desktop/CIMWin32Prov/cim-basedon).

</dd> <dt>

**OrderIndex**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si hay un pedido al basado en asociaciones que describen cómo se ensambla una extensión de almacenamiento de nivel superior, la propiedad **OrderIndex** indica esto. Cuando existe un pedido, las instancias con el mismo valor **dependiente** (la misma extensión de nivel superior) deben colocar valores únicos en la propiedad **OrderIndex** . El valor más bajo implica al primer miembro de la colección de extensiones de nivel inferior y los valores que aumentan implican a miembros sucesivos de la colección. Si no hay ninguna relación ordenada, se debe especificar un valor de cero. Un ejemplo del uso de esta propiedad es definir una matriz seccionada RAID-0 de tres discos. La matriz RAID resultante es una extensión de almacenamiento que depende de las extensiones de almacenamiento que describen cada uno de los tres discos. El **OrderIndex** de cada Asociación de las extensiones de disco a la matriz RAID podría especificarse como 1, 2 y 3 para indicar el orden en que se usan las extensiones de disco para tener acceso a los datos de RAID. Esta propiedad se hereda de [**\_ BasedOn CIM**](/windows/desktop/CIMWin32Prov/cim-basedon).

</dd> <dt>

**StartingAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La dirección inicial en la que se inicia la extensión de nivel superior en el almacenamiento de nivel inferior. Esta propiedad se hereda de [**\_ BasedOn CIM**](/windows/desktop/CIMWin32Prov/cim-basedon).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

