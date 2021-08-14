---
description: La dependencia \_ AssociatedBattery de CIM asocia una batería a un dispositivo lógico. Use esta asociación para modelar baterías individuales que conste una fuente de alimentación ininterrumpida (UPS).
ms.assetid: f8d8b3d3-edc5-438a-8be6-3ea4d765085b
ms.tgt_platform: multiple
title: CIM_AssociatedBattery clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedBattery
- CIM_AssociatedBattery.Dependent
- CIM_AssociatedBattery.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 76529a63b2600543602727c14aea4c7972e8b51f7c67924da9eb06f1185c427e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119284595"
---
# <a name="cim_associatedbattery-class"></a>Cim \_ AssociatedBattery (clase)

La **dependencia \_ AssociatedBattery de CIM** asocia una batería a un dispositivo lógico. Use esta asociación para modelar baterías individuales que conste una fuente de alimentación ininterrumpida (UPS).

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de la versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{8502C578-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_AssociatedBattery : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_Battery       REF Antecedent;
};
```

## <a name="members"></a>Miembros

La **clase \_ AssociatedBattery de CIM** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ AssociatedBattery de CIM** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **batería CIM \_**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedente")
</dt> </dl>

Una [**batería CIM \_**](cim-battery.md) que describe la batería.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ Cim LogicalDevice**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Invalidar**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependiente")
</dt> </dl>

Un [**dispositivo \_ lógico CIM**](cim-logicaldevice.md) que contiene el dispositivo lógico que necesita o está asociado a la batería.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ AssociatedBattery de CIM** se deriva de la dependencia [**\_ CIM**](cim-dependency.md).

WMI no implementa esta clase. Para obtener más información sobre las clases derivadas de **CIM \_ AssociatedBattery,** vea [Clases win32.](win32-provider.md)

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

 

