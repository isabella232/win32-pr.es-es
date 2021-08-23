---
description: La clase de asociación CollectedMSEs de CIM representa los miembros del objeto \_ de agrupación, una clase CollectionOfMSEs.
ms.assetid: 3dca2094-57f1-447e-809c-f924f88a185a
ms.tgt_platform: multiple
title: CIM_CollectedMSEs clase (proveedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectedMSEs
- CIM_CollectedMSEs.Collection
- CIM_CollectedMSEs.Member
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 82ffbf9e3c00a9a0463e1337ee5c5ed6ab188dc5258c622cfa6b41eb717d8589
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959084"
---
# <a name="cim_collectedmses-class-cimwin32-wmi-providers"></a>CIM_CollectedMSEs clase (proveedores WMI CIMWin32)

La **clase \_ de asociación CollectedMSEs** de CIM representa los miembros del objeto de agrupación, [**una clase CollectionOfMSEs.**](cim-collectionofmses.md)

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de la versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class CIM_CollectedMSEs
{
  CM_CollectionOfMSEs      REF Collection;
  CIM_ManagedSystemElement REF Member;
};
```

## <a name="members"></a>Miembros

La **clase \_ CollectedMSEs** de CIM tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ CollectedMSEs** de CIM tiene estas propiedades.

<dl> <dt>

**Colección**
</dt> <dd> <dl> <dt>

Tipo de datos: **Colección \_ de CMOfMSEs**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia al objeto de agrupación o "bolsa" que representa la colección.

</dd> <dt>

**Miembro**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ ManagedSystemElement**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia a un miembro de la colección.

</dd> </dl>

## <a name="remarks"></a>Comentarios

WMI no implementa esta clase. Para obtener más información acerca de las clases WMI derivadas de **\_ LOS OBJETOS RECOPILADOS DE CIM,** vea [Clases win32.](win32-provider.md)

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

 




