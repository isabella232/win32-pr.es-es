---
description: La asociación Associated Cooling de CIM indica cuándo los ventiladores u otros dispositivos de refrigeración son específicos de un dispositivo (en lugar de proporcionar refrigeración de \_ gabinetes o gabinetes).
ms.assetid: 7b20e429-593c-4365-a340-1aef9b0fadf5
ms.tgt_platform: multiple
title: CIM_AssociatedCooling clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedCooling
- CIM_AssociatedCooling.Dependent
- CIM_AssociatedCooling.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bb838129226b225f024917e8f8e77ddc92ddf2ff
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062755"
---
# <a name="cim_associatedcooling-class"></a>Cim \_ Associated Cooling (clase)

La **\_ asociación Associated Cooling** de CIM indica cuándo los ventiladores u otros dispositivos de refrigeración son específicos de un dispositivo (en lugar de proporcionar refrigeración de gabinetes o gabinetes).

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{306F88F2-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_AssociatedCooling : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_CoolingDevice REF Antecedent;
};
```

## <a name="members"></a>Members

La **clase \_ Associated Cooling de CIM** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ Associated Cooling de CIM** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ CoolingDevice**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedente")
</dt> </dl>

Un [**\_ dispositivo lógico CIM**](cim-logicaldevice.md) que describe el dispositivo de refrigeración.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ Cim LogicalDevice**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Invalidar**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependiente")
</dt> </dl>

Un [**dispositivo lógico CIM \_ que**](cim-logicaldevice.md) hace referencia al dispositivo lógico que se está enfriado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ AssociatedAttributeing** de CIM se deriva de [**la dependencia \_ CIM**](cim-dependency.md).

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

 

