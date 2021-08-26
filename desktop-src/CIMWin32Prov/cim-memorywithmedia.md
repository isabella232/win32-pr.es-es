---
description: La clase \_ CIM MemoryWithMedia asocia la memoria física a un medio físico y su esfuerzo. La memoria proporciona identificación de medios y almacena datos específicos del usuario.
ms.assetid: 99806d2d-6575-431d-9149-dc8ea767146c
ms.tgt_platform: multiple
title: CIM_MemoryWithMedia clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemoryWithMedia
- CIM_MemoryWithMedia.Dependent
- CIM_MemoryWithMedia.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: eff54c8ac48c9e6e998e720815a9a3529f5484f8a089e8ea510559d2e7cfa488
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921415"
---
# <a name="cim_memorywithmedia-class"></a>Clase \_ CIM MemoryWithMedia

La **clase \_ CIM MemoryWithMedia** asocia la memoria física a un medio físico y su esfuerzo. La memoria proporciona identificación de medios y almacena datos específicos del usuario.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se construyen las clases WMI. WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{FAF76B7E-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_MemoryWithMedia : CIM_Dependency
{
  CIM_PhysicalMedia  REF Dependent;
  CIM_PhysicalMemory REF Antecedent;
};
```

## <a name="members"></a>Miembros

La **clase \_ CIM MemoryWithMedia** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ CIM MemoryWithMedia** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ CIM PhysicalMemory**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedente")
</dt> </dl>

Memoria [**física \_ CIM que**](cim-physicalmemory.md) describe la memoria asociada a medios físicos.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ PhysicalMedia**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependiente")
</dt> </dl>

Cim [**\_ PhysicalMedia**](cim-physicalmedia.md) que describe los medios físicos.

</dd> </dl>

## <a name="remarks"></a>Comentarios

**CIM \_ MemoryWithMedia se** hereda de la [**dependencia \_ CIM**](cim-dependency.md).

WMI no implementa esta clase.

Esta documentación se deriva de las descripciones de clases CIM publicadas por dmtf. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Dependencia \_ cim**](cim-dependency.md)
</dt> </dl>

 

