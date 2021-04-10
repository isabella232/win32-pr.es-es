---
description: Una clase de asociación Modelo de información común (CIM) que establece relaciones entre un sistema y los elementos del sistema administrados en los que se compone.
ms.assetid: 11ad6dc1-a09a-4bab-bb1d-2131a8fdb812
ms.tgt_platform: multiple
title: CIM_SystemComponent (clase) (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SystemComponent
- CIM_SystemComponent.PartComponent
- CIM_SystemComponent.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9d9aae4e4ef916916f54bddea814844f23ed7315
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153238"
---
# <a name="cim_systemcomponent-class-cimwin32-wmi-providers"></a>CIM_SystemComponent (clase) (proveedores WMI de CIMWin32)

La **clase \_ SystemComponent de CIM** es una clase de asociación modelo de información común (CIM) que establece relaciones entre un sistema y los elementos del sistema administrados en los que se compone.

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{527BC6CE-BAFE-11d2-85E5-0000F8102E5F}"), AMENDMENT]
class CIM_SystemComponent : CIM_Component
{
  CIM_ManagedSystemElement REF PartComponent;
  CIM_System               REF GroupComponent;
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ SystemComponent** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ SystemComponent** tiene estas propiedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ Sistema CIM**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")
</dt> </dl>

[**\_ Sistema CIM**](cim-system.md) que describe el sistema primario de la asociación.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ ManagedSystemElement de CIM**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Un [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md) que describe el elemento secundario que es un componente de un sistema.

</dd> </dl>

## <a name="remarks"></a>Observaciones

WMI no implementa esta clase. Para las clases WMI derivadas de **CIM \_ SystemComponent**, vea [clases Win32](win32-provider.md).

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

 

