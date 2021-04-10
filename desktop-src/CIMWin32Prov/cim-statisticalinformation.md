---
description: La \_ clase CIM StatisticalInformation es una clase raíz para la colección arbitraria de datos estadísticos o métricas aplicables a uno o varios elementos del sistema administrados.
ms.assetid: ecc3b310-c553-416b-b4e3-705965557945
ms.tgt_platform: multiple
title: CIM_StatisticalInformation (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StatisticalInformation
- CIM_StatisticalInformation.Caption
- CIM_StatisticalInformation.Description
- CIM_StatisticalInformation.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b6eda3e2463c880a58c4e23a6d09dcab99417ead
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907495"
---
# <a name="cim_statisticalinformation-class"></a>\_Clase StatisticalInformation de CIM

La clase **CIM \_ StatisticalInformation** es una clase raíz para la colección arbitraria de datos estadísticos o métricas aplicables a uno o varios elementos del sistema administrados.

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{956597A1-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_StatisticalInformation
{
  string Caption;
  string Description;
  string Name;
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ StatisticalInformation** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ StatisticalInformation** tiene estas propiedades.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Breve descripción textual de la estadística o la métrica.

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción textual de la estadística o la métrica.

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Etiqueta por la que se conoce la estadística o la métrica. Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.

</dd> </dl>

## <a name="remarks"></a>Observaciones

WMI no implementa esta clase. Para las clases WMI derivadas de **CIM \_ StatisticalInformation**, vea [clases Win32](win32-provider.md).

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

