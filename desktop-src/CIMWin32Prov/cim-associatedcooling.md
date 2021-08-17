---
description: La asociación Associated Cooling de CIM indica cuándo los ventiladores u otros dispositivos de refrigeración son específicos de un dispositivo (en lugar de proporcionar refrigeración del gabinete \_ o del gabinete).
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
ms.openlocfilehash: 71f9c129a7883e5594affeefab8de9c20cf30ff092c5ce315471dbf5bc0a316a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119218945"
---
# <a name="cim_associatedcooling-class"></a>Cim \_ AssociatedAttributeing (clase)

La **\_ asociación Associated Cooling** de CIM indica cuándo los ventiladores u otros dispositivos de refrigeración son específicos de un dispositivo (en lugar de proporcionar refrigeración del gabinete o del gabinete).

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

## <a name="members"></a>Miembros

La **clase \_ AssociatedAttributeing** de CIM tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase CIM Associated \_ Cooling** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ CoolingDevice**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedente")
</dt> </dl>

Un [**dispositivo \_ lógico CIM**](cim-logicaldevice.md) que describe el dispositivo de refrigeración.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ LogicalDevice**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependiente")
</dt> </dl>

Un [**dispositivo \_ lógico CIM**](cim-logicaldevice.md) que hace referencia al dispositivo lógico que se está enfríando.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ AssociatedAttributeing** de CIM se deriva de la [**dependencia \_ CIM**](cim-dependency.md).

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

 

