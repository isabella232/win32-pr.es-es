---
description: La clase \_ de asociación CIM SoftwareElementChecks relaciona un elemento de software con la información de condición o ubicación que puede requerir una característica.
ms.assetid: ff130fe9-ddb2-4e4f-86d3-53f1d8ed14aa
ms.tgt_platform: multiple
title: CIM_SoftwareElementChecks clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareElementChecks
- CIM_SoftwareElementChecks.Check
- CIM_SoftwareElementChecks.Element
- CIM_SoftwareElementChecks.Phase
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ea6fcb02794174e825994f70270745741c9b7713
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160346"
---
# <a name="cim_softwareelementchecks-class"></a>Cim \_ SoftwareElementChecks (clase)

La **clase \_ de asociación CIM SoftwareElementChecks** relaciona un elemento de software con la información de condición o ubicación que puede requerir una característica.

Dado que los elementos de software en un estado listo para ejecutarse no pueden pasar a otro estado, el valor de la propiedad **Phase** está restringido a en estado para los objetos [**\_ SoftwareElement**](cim-softwareelement.md) de CIM en un estado listo para ejecutarse.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DE DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de la versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica a partir Managed Object Format (MOF) e incluye todas sus propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[UUID("{24783E8A-DB31-11d2-85FC-0000F8102E5F}"), Association, Aggregation, Abstract, AMENDMENT]
class CIM_SoftwareElementChecks
{
  CIM_Check           REF Check;
  CIM_SoftwareElement REF Element;
  uint16                  Phase;
};
```

## <a name="members"></a>Members

La **clase \_ CIM SoftwareElementChecks** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ CIM SoftwareElementChecks** tiene estas propiedades.

<dl> <dt>

**Comprobación**
</dt> <dd> <dl> <dt>

Tipo de datos: **Comprobación de CIM \_**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Referencia a la comprobación.

</dd> <dt>

**Element**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ SoftwareElement**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Referencia al elemento .

</dd> <dt>

**Fase**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la comprobación a la que se hace referencia es una comprobación en estado o una comprobación de estado siguiente.

<dt>

<span id="In-State"></span><span id="in-state"></span><span id="IN-STATE"></span>

**En estado** (0)


</dt> <dd></dd> <dt>

<span id="Next-State"></span><span id="next-state"></span><span id="NEXT-STATE"></span>

**Estado siguiente** (1)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Observaciones

WMI no implementa esta clase. Para las clases WMI derivadas de **\_ CIM SoftwareElementChecks,** vea [Clases Win32](win32-provider.md).

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

