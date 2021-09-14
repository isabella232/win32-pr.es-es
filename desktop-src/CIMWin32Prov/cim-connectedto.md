---
description: La clase \_ CIM ConnectedTo representa una asociación que indica que hay dos o más conectores físicos conectados.
ms.assetid: fedd9227-8a3b-461a-995b-08cbceb81181
ms.tgt_platform: multiple
title: CIM_ConnectedTo clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConnectedTo
- CIM_ConnectedTo.Dependent
- CIM_ConnectedTo.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1f1a507cb529f2040607024e1a6167ddcd5dc7c0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062741"
---
# <a name="cim_connectedto-class"></a>Cim \_ ConnectedTo (clase)

La **clase \_ CIM ConnectedTo** representa una asociación que indica que hay dos o más conectores físicos conectados.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{FAF76B85-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ConnectedTo : CIM_Dependency
{
  CIM_PhysicalConnector REF Dependent;
  CIM_PhysicalConnector REF Antecedent;
};
```

## <a name="members"></a>Members

La **clase \_ ConnectedTo** de CIM tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ ConnectedTo** de CIM tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ PhysicalConnector**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedente")
</dt> </dl>

Un [**conector \_ físico CIM**](cim-physicalconnector.md) que representa un conector físico que actúa como un extremo de la conexión.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ PhysicalConnector**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependiente")
</dt> </dl>

Un [**conector físico CIM \_ que**](cim-physicalconnector.md) representa otro conector físico que actúa como el otro extremo de la conexión.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ ConnectedTo** de CIM se hereda de la [**dependencia \_ CIM**](cim-dependency.md).

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

[**Dependencia \_ cim**](cim-dependency.md)
</dt> </dl>

 

