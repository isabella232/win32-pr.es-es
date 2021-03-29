---
description: El \_ objeto CIM CollectionOfMSEs permite la agrupación de \_ objetos MANAGEDSYSTEMELEMENT de CIM con el fin de asociar configuraciones y configuraciones. Es abstracto requerir más definición y perfeccionamiento semántico en las subclases.
ms.assetid: 9448a7a1-defc-4bac-9ce6-29ec2406d573
ms.tgt_platform: multiple
title: CIM_CollectionOfMSEs (clase) (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectionOfMSEs
- CIM_CollectionOfMSEs.Caption
- CIM_CollectionOfMSEs.CollectionID
- CIM_CollectionOfMSEs.Description
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 57942dd6e00d819e4375ddd316e5e15126621b97
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153242"
---
# <a name="cim_collectionofmses-class-cimwin32-wmi-providers"></a>CIM_CollectionOfMSEs (clase) (proveedores WMI de CIMWin32)

El objeto **CIM \_ CollectionOfMSEs** permite la agrupación de objetos [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md) con el fin de asociar configuraciones y configuraciones. Es abstracto requerir más definición y perfeccionamiento semántico en las subclases.

El objeto **CIM \_ CollectionOfMSEs** no tiene ningún Estado o información de estado, pero solo representa una agrupación de elementos. Por esta razón, es incorrecto que los grupos de subclases que tienen el estado/estado de **CIM \_ CollectionOfMSEs**, un ejemplo es [**CIM \_ RedundancyGroup**](cim-redundancygroup.md) (que se subclase correctamente de [**CIM \_ LogicalElement**](cim-logicalelement.md)). Las colecciones suelen agregar objetos ' like ' y representan una optimización. Sin las colecciones, se fuerza la definición de las asociaciones de [**\_ ElementSetting**](cim-elementsetting.md) CIM y [**\_ ElementConfiguration CIM**](cim-elementconfiguration.md) individuales, para vincular los objetos de configuración y de configuración a los [**\_ ManagedSystemElements de CIM**](cim-managedsystemelement.md)individuales. Puede haber mucha duplicación en la asignación de la misma configuración a varios objetos. Además, el uso del objeto Collection permite determinar que las asociaciones de configuración y configuración son realmente iguales para los miembros de la colección. De lo contrario, esta información se obtenería definiendo la colección de forma propietaria y, a continuación, consultando las asociaciones **CIM \_ ElementSetting** y **CIM \_ ElementConfiguration** para determinar si el conjunto de recopilación está totalmente incluido.

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class CIM_CollectionOfMSEs
{
  string Caption;
  string CollectionID;
  string Description;
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ CollectionOfMSEs** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ CollectionOfMSEs** tiene estas propiedades.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción textual breve del objeto CollectionOfMSEs.

</dd> <dt>

**Recopilación**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificación del objeto de colección. Cuando se subclasen, la propiedad CollectionID se puede invalidar para ser una propiedad de clave.

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción textual del objeto CollectionOfMSEs.

</dd> </dl>

## <a name="remarks"></a>Observaciones

WMI no implementa esta clase. Vea [clases Win32](win32-provider.md) para clases WMI derivadas de **CIM \_ CollectionOfMSEs**.

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

 




