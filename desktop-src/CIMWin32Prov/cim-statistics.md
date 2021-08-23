---
description: La clase CIM \_ Statistics representa una asociación que relaciona los elementos administrados del sistema con los grupos estadísticos que se les aplican.
ms.assetid: fc75991b-adcd-4e47-b610-7503f6bb7c03
ms.tgt_platform: multiple
title: CIM_Statistics clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Statistics
- CIM_Statistics.Element
- CIM_Statistics.Stats
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 97f751460cc92e2f30fa734197e2bef3f2e48436b8ce9f20058cc921060188f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119505865"
---
# <a name="cim_statistics-class"></a>Cim \_ Statistics (clase)

La **clase CIM \_ Statistics** representa una asociación que relaciona los elementos administrados del sistema con los grupos estadísticos que se les aplican.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se construyen las clases WMI. WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintaxis siguiente se simplifica a partir Managed Object Format (MOF) e incluye todas sus propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, Association, UUID("{956597A3-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_Statistics
{
  CIM_ManagedSystemElement   REF Element;
  CIM_StatisticalInformation REF Stats;
};
```

## <a name="members"></a>Miembros

La **clase \_ CIM Statistics** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase CIM \_ Statistics** tiene estas propiedades.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ ManagedSystemElement**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia a la [**clase \_ ManagedSystemElement de CIM**](cim-managedsystemelement.md) para la que se definen datos estadísticos o de métricas.

</dd> <dt>

**Stats**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ StatisticalInformation**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia a la información estadística o al objeto .

</dd> </dl>

## <a name="remarks"></a>Comentarios

WMI no implementa esta clase.

Esta documentación se deriva de las descripciones de clases CIM publicadas por dmtf. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

 




