---
description: La clase CIM CollectedCollections es una asociación de agregación que representa una colección de elementos del sistema administrado (MSE) contenidos en una \_ colección de MSE.
ms.assetid: 7baaf429-1211-4545-ace2-c6312d53c0f6
ms.tgt_platform: multiple
title: CIM_CollectedCollections clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectedCollections
- CIM_CollectedCollections.Collection
- CIM_CollectedCollections.CollectionInCollection
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: cecac67d96aba6b8ad8c5937f098eaef312af89b80c28febaa8073c5f7be26f5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119322295"
---
# <a name="cim_collectedcollections-class"></a>Cim \_ CollectedCollections (clase)

La **clase \_ CIM CollectedCollections** es una asociación de agregación que representa una colección de elementos del sistema administrado (MSE) contenidos en una colección de MSE.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se construyen las clases WMI. WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class CIM_CollectedCollections
{
  CIM_CollectionOfMSEs REF Collection;
  CIM_CollectionOfMSEs REF CollectionInCollection;
};
```

## <a name="members"></a>Miembros

La **clase \_ CIM CollectedCollections** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ CIM CollectedCollections** tiene estas propiedades.

<dl> <dt>

**Colección**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ Cim CollectionOfMSEs**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia al "nivel superior" o elemento primario de la agregación.

</dd> <dt>

**CollectionInCollection**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ Cim CollectionOfMSEs**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia a la colección **"recopilada".**

</dd> </dl>

## <a name="remarks"></a>Comentarios

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



 

 




