---
description: La dependencia \_ AssociatedAlarm de CIM asocia una alarma a un dispositivo lógico.
ms.assetid: ed0ccc81-6d1b-45b0-abf0-7a2bd9a50193
ms.tgt_platform: multiple
title: CIM_AssociatedAlarm clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedAlarm
- CIM_AssociatedAlarm.Dependent
- CIM_AssociatedAlarm.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1ee89533b6084999d6972da253276f1ee225dd1e517727761c893e9424f01f65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119439485"
---
# <a name="cim_associatedalarm-class"></a>Cim \_ AssociatedAlarm (clase)

La **dependencia \_ AssociatedAlarm de CIM** asocia una alarma a un dispositivo lógico.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. ACTUALMENTE, WMI solo admite los [esquemas de la versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{2280CB02-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_AssociatedAlarm : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_AlarmDevice   REF Antecedent;
};
```

## <a name="members"></a>Miembros

La **clase \_ AssociatedAlarm de CIM** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ AssociatedAlarm de CIM** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ AlarmDevice**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedente")
</dt> </dl>

AlarmDevice [**\_ cim que**](cim-alarmdevice.md) contiene el dispositivo de alarma.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ LogicalDevice**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependiente")
</dt> </dl>

Un [**dispositivo \_ lógico CIM**](cim-logicaldevice.md) que contiene el dispositivo lógico que está alarmado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ AssociatedAlarm de CIM** se deriva de la dependencia [**\_ CIM**](cim-dependency.md).

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

 

