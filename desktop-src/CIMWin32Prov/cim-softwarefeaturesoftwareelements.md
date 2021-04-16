---
description: La \_ Asociación SoftwareFeatureSoftwareElements de CIM identifica los elementos de software que componen una característica de software específica.
ms.assetid: 933586c5-b85e-4136-b557-5151a48abc32
ms.tgt_platform: multiple
title: CIM_SoftwareFeatureSoftwareElements (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareFeatureSoftwareElements
- CIM_SoftwareFeatureSoftwareElements.PartComponent
- CIM_SoftwareFeatureSoftwareElements.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 71712ebb3f8bf2ab2067325f16cf31af7fb1dc38
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659368"
---
# <a name="cim_softwarefeaturesoftwareelements-class"></a>\_Clase SoftwareFeatureSoftwareElements de CIM

La **Asociación \_ SoftwareFeatureSoftwareElements de CIM** identifica los elementos de software que componen una característica de software específica.

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[UUID("{A91081E2-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SoftwareFeatureSoftwareElements : CIM_Component
{
  CIM_SoftwareElement REF PartComponent;
  CIM_SoftwareFeature REF GroupComponent;
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ SoftwareFeatureSoftwareElements** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ SoftwareFeatureSoftwareElements** tiene estas propiedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ SoftwareFeature**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **agregado**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Componente de grupo.

Esta propiedad se hereda del [**\_ componente CIM**](cim-component.md).

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ SoftwareElement**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Componente del elemento.

Esta propiedad se hereda del [**\_ componente CIM**](cim-component.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **Asociación \_ SoftwareFeatureSoftwareElements de CIM** se deriva [**del \_ componente CIM**](cim-component.md).

WMI no implementa esta clase. Para las clases WMI derivadas de **CIM \_ SoftwareFeatureSoftwareElements**, vea [clases Win32](win32-provider.md).

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Componente CIM**](cim-component.md)
</dt> </dl>

 

