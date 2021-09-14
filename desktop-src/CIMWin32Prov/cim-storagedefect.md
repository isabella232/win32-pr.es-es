---
description: La \_ agregación StorageDefect de CIM recopila los errores de almacenamiento de una extensión de almacenamiento.
ms.assetid: 7acd3d25-4691-43cb-badc-662684989345
ms.tgt_platform: multiple
title: CIM_StorageDefect clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageDefect
- CIM_StorageDefect.Error
- CIM_StorageDefect.Extent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8e6c2be45fe2f44afa407dc72e3ae90c486593ec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255872"
---
# <a name="cim_storagedefect-class"></a>Clase \_ StorageDefect de CIM

La **\_ agregación StorageDefect de CIM** recopila los errores de almacenamiento de una extensión de almacenamiento.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintaxis siguiente se simplifica a Managed Object Format (MOF) e incluye todas sus propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{5CC70817-DB31-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_StorageDefect
{
  CIM_StorageError  REF Error;
  CIM_StorageExtent REF Extent;
};
```

## <a name="members"></a>Members

La **clase \_ StorageDefect de CIM** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ StorageDefect de CIM** tiene estas propiedades.

<dl> <dt>

**Error**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ StorageError**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **Débil**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Referencia al objeto de error, que define las direcciones inicial y final que se asignan fuera de la extensión de almacenamiento.

</dd> <dt>

**Extensión**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ Cim StorageExtent**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Agregado,**](/windows/desktop/WmiSdk/standard-qualifiers) [**Máximo**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Mínimo**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Referencia a la extensión de almacenamiento en la que se produjeron los errores.

</dd> </dl>

## <a name="remarks"></a>Observaciones

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



 

