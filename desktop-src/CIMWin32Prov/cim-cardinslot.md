---
description: La clase \_ CIM CardInSlot asocia una tarjeta adaptadora con el contenedor en el que se inserta.
ms.assetid: 253fb444-2a9e-4099-a4d5-352b643d8e32
ms.tgt_platform: multiple
title: CIM_CardInSlot clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CardInSlot
- CIM_CardInSlot.Dependent
- CIM_CardInSlot.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 19c6e7334b8a13854241c3fd2ee41dd7010255b5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061558"
---
# <a name="cim_cardinslot-class"></a>Cim \_ CardInSlot (clase)

La **clase \_ CIM CardInSlot** asocia una tarjeta adaptadora con el contenedor en el que se inserta.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, MappingStrings("MIF.DMTF|System Slot|004.4"), UUID("{FAF76B8A-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_CardInSlot : CIM_PackageInSlot
{
  CIM_Card REF Dependent;
  CIM_Slot REF Antecedent;
};
```

## <a name="members"></a>Members

La **clase \_ Cim CardInSlot** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ CIM CardInSlot** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **Ranura CIM \_**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedente")
</dt> </dl>

Una [**ranura CIM \_**](cim-slot.md) que describe la ranura en la que se inserta la tarjeta.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **Tarjeta CIM \_**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Una [**tarjeta CIM \_**](cim-card.md) que describe la tarjeta en la ranura.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ CardInSlot** de CIM se deriva de [**CIM \_ PackageInSlot**](cim-packageinslot.md).

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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Paquete \_ CIMInSlot**](cim-packageinslot.md)
</dt> </dl>

 

