---
description: La clase BasedOn de CIM representa una asociación que describe cómo se pueden ensamblar las extensiones de almacenamiento desde \_ extensiones de nivel inferior.
ms.assetid: 82132012-5851-4be8-82db-edbdb50b70e5
ms.tgt_platform: multiple
title: CIM_BasedOn clase (proveedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BasedOn
- CIM_BasedOn.Dependent
- CIM_BasedOn.Antecedent
- CIM_BasedOn.EndingAddress
- CIM_BasedOn.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5e25cd9a5f194df8c5cbc0c7dc24a4777cee3417
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061574"
---
# <a name="cim_basedon-class-cimwin32-wmi-providers"></a>CIM_BasedOn clase (proveedores WMI CIMWin32)

La **clase \_ BasedOn** de CIM representa una asociación que describe cómo se pueden ensamblar las extensiones de almacenamiento desde extensiones de nivel inferior. Por ejemplo, las extensiones físicas incluyen extensiones de espacio protegido. Por lo tanto, los conjuntos de volúmenes se ensamblan a partir de una o varias extensiones de espacio físico o protegido. La memoria caché se puede definir de forma independiente y realizarse en un elemento físico, o puede basarse en extensiones de almacenamiento volátiles o no volátiles.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DE DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de la versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{8502C53E-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_BasedOn : CIM_Dependency
{
  CIM_StorageExtent REF Dependent;
  CIM_StorageExtent REF Antecedent;
  uint64                EndingAddress;
  uint64                StartingAddress;
};
```

## <a name="members"></a>Members

La **clase \_ BasedOn** de CIM tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ BasedOn** de CIM tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ StorageExtent**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedente")
</dt> </dl>

[**\_ StorageExtent de CIM**](cim-storageextent.md) que describe la extensión de almacenamiento de nivel inferior.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ StorageExtent**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Invalidar**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependiente")
</dt> </dl>

[**\_ StorageExtent de CIM**](cim-storageextent.md) que describe la extensión de almacenamiento de nivel superior.

</dd> <dt>

**EndingAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica el final de la extensión de alto nivel en el almacenamiento de nivel inferior. Esta propiedad es útil al asignar extensiones no contiguas a una agrupación de nivel superior.

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**StartingAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica el principio de la extensión de alto nivel en el almacenamiento de nivel inferior.

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ Cim BasedOn** se deriva de la [**dependencia \_ CIM**](cim-dependency.md).

WMI no implementa esta clase.

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Dependencia \_ cim**](cim-dependency.md)
</dt> </dl>

 

