---
description: El objeto CollectionOfMSEs de CIM permite la agrupación de objetos ManagedSystemElement de CIM con el fin de asociar \_ \_ configuraciones y configuraciones. Es abstracto requerir más definición y perfeccionamiento semántico en subclases.
ms.assetid: 9448a7a1-defc-4bac-9ce6-29ec2406d573
ms.tgt_platform: multiple
title: CIM_CollectionOfMSEs clase (proveedores WMI CIMWin32)
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
ms.openlocfilehash: d67b51e90a9a3c2eff420a5251c1b4e75f323d48e796a3190b662fb844c1517a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119579055"
---
# <a name="cim_collectionofmses-class-cimwin32-wmi-providers"></a>CIM_CollectionOfMSEs clase (proveedores WMI CIMWin32)

El **objeto \_ CollectionOfMSEs** de CIM permite la agrupación de objetos [**\_ ManagedSystemElement**](cim-managedsystemelement.md) de CIM con el fin de asociar configuraciones y configuraciones. Es abstracto requerir más definición y perfeccionamiento semántico en subclases.

El **objeto \_ CollectionOfMSEs** de CIM no contiene ninguna información de estado o estado, sino que solo representa una agrupación de elementos. Por esta razón, es incorrecto para los grupos de subclases que tienen estado o estado de **\_ CIM CollectionOfMSEs**, un ejemplo es [**Cim \_ RedundancyGroup**](cim-redundancygroup.md) (que se ha subclasificado correctamente de [**CIM \_ LogicalElement**](cim-logicalelement.md)). Las colecciones suelen agregar objetos "like" y representan una optimización. Sin colecciones, se obliga a definir asociaciones [**individuales \_ de ElementSetting**](cim-elementsetting.md) y [**\_ ELEMENTConfiguration**](cim-elementconfiguration.md) de CIM, para vincular valores y objetos de configuración a elementos [**\_ ManagedSystemElements de CIM individuales.**](cim-managedsystemelement.md) Puede haber mucha duplicación en la asignación de la misma configuración a varios objetos. Además, el uso del objeto de colección permite determinar que las asociaciones de configuración y configuración son realmente las mismas para los miembros de la colección. De lo contrario, esta información se obtendría definiendo la colección de forma propietaria y, a continuación, consultando las asociaciones **\_ ElementSetting** y **\_ CIM ElementConfiguration** de CIM para determinar si el conjunto de recopilación está completamente cubierto.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se construyen las clases WMI. WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

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

La **clase \_ CollectionOfMSEs** de CIM tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ CollectionOfMSEs** de CIM tiene estas propiedades.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Breve descripción textual del objeto CollectionOfMSEs.

</dd> <dt>

**CollectionID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificación del objeto Collection. Cuando se encuentra en subclases, la propiedad CollectionID se puede invalidar para que sea una propiedad Key.

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción textual del objeto CollectionOfMSEs.

</dd> </dl>

## <a name="remarks"></a>Comentarios

WMI no implementa esta clase. Vea [Clases Win32 para](win32-provider.md) clases WMI derivadas de Cim **\_ CollectionOfMSEs**.

Esta documentación se deriva de las descripciones de clases CIM publicadas por dmtf. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

 




