---
description: Asociación que describe cómo se pueden ensamblar extensiones de almacenamiento desde extensiones de nivel inferior.
ms.assetid: 8be9bb2c-ef46-454b-bfc3-0398c64d17b7
title: Msvm_BasedOn clase
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
ms.openlocfilehash: f3f8138fcc06d5e2d100f38b0333dcbfc5e76c61366da686b313a70d40ffa120
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790255"
---
# <a name="msvm_basedon-class"></a>Clase BasedOn de Msvm \_

Asociación que describe cómo se pueden ensamblar extensiones de almacenamiento desde extensiones de nivel inferior. Por ejemplo, ProtectedSpaceExtents son partes de PhysicalExtents, mientras que volumeSets se ensamblan desde uno o varios elementos Physical o ProtectedSpaceExtents. Como otro ejemplo, CacheMemory se puede definir de forma independiente y realizarse en un elemento PhysicalElement o se puede basar en Volatile o NonVolatileStorageExtents.

La sintaxis siguiente se Managed Object Format código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

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

La **clase \_ BasedOn de Msvm** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ BasedOn de Msvm** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **Cim \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Extensión de almacenamiento de nivel inferior. Esta propiedad se hereda de [**CIM \_ BasedOn.**](/windows/desktop/CIMWin32Prov/cim-basedon)

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **Cim \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Extensión de almacenamiento de nivel superior. Esta propiedad se hereda de [**CIM \_ BasedOn.**](/windows/desktop/CIMWin32Prov/cim-basedon)

</dd> <dt>

**EndingAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Dirección final donde, en el almacenamiento de nivel inferior, finaliza la extensión de nivel superior. Esta propiedad es útil al asignar extensiones no contiguas a una agrupación de nivel superior. Esta propiedad se hereda de [**CIM \_ BasedOn.**](/windows/desktop/CIMWin32Prov/cim-basedon)

</dd> <dt>

**OrderIndex**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si hay un pedido a en función de las asociaciones que describen cómo se ensambla una extensión de almacenamiento de nivel superior, la propiedad **OrderIndex** lo indica. Cuando existe un pedido, las instancias con el mismo valor **Dependiente** (la misma extensión de nivel superior) deben colocar valores únicos en la **propiedad OrderIndex.** El valor más bajo implica el primer miembro de la colección de extensiones de nivel inferior, y el aumento de los valores implica miembros sucesivos de la colección. Si no hay ninguna relación ordenada, se debe especificar un valor de cero. Un ejemplo del uso de esta propiedad es definir una matriz seccionada RAID-0 de tres discos. La matriz RAID resultante es una extensión de almacenamiento que depende de las extensiones de almacenamiento que describen cada uno de los tres discos. **OrderIndex** de cada asociación de las extensiones de disco a la matriz RAID podría especificarse como 1, 2 y 3 para indicar el orden en que se usan las extensiones de disco para acceder a los datos RAID. Esta propiedad se hereda de [**CIM \_ BasedOn.**](/windows/desktop/CIMWin32Prov/cim-basedon)

</dd> <dt>

**StartingAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Dirección inicial donde, en el almacenamiento de nivel inferior, comienza la extensión de nivel superior. Esta propiedad se hereda de [**CIM \_ BasedOn.**](/windows/desktop/CIMWin32Prov/cim-basedon)

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

