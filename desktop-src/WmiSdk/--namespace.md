---
description: Representa un espacio de nombres WMI.
ms.assetid: d5f0abc7-32cf-4d85-b5cd-5d60c991bcbc
ms.tgt_platform: multiple
title: __Namespace clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Namespace
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 4640570dd834b42652d04262b70ec84fac106d99f463ca22144e28ad388a0937
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118320773"
---
# <a name="__namespace-class"></a>\_\_Clase de espacio de nombres

La **\_ \_ clase del** sistema Namespace representa un espacio de nombres WMI.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class __Namespace : __SystemClass
{
  string Name;
};
```

## <a name="members"></a>Miembros

La **\_ \_ clase Namespace** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **\_ \_ clase Namespace** tiene estas propiedades.

<dl> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [ **Clave**](standard-qualifiers.md)
</dt> </dl>

Nombre del espacio de nombres.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **\_ \_ clase Namespace** se deriva de [**\_ \_ SystemClass**](--systemclass.md), que no tiene propiedades.

Puede usar **\_ \_ Espacio de nombres** para identificar, crear y eliminar espacios de nombres secundarios dentro del espacio de nombres de trabajo actual para el que tiene un objeto [**IWbemServices.**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) Al crear una nueva instancia de **\_ \_ Namespace dentro de** cualquier espacio de nombres de trabajo, se crea un espacio de nombres secundario dentro del espacio de nombres de trabajo. Por el contrario, al eliminar una instancia de **\_ \_ Namespace** se quita el espacio de nombres secundario del espacio de nombres de trabajo. Tenga en cuenta que la eliminación de un espacio de nombres secundario también elimina todas sus clases e instancias.

La enumeración de instancias de esta clase dentro de cualquier espacio de nombres de trabajo proporciona los espacios de nombres secundarios disponibles.

Por ejemplo, dentro del espacio \\ de nombres raíz hay dos instancias de **\_ \_ Namespace**. Una tiene su **propiedad Name** establecida en "Default", la otra tiene **nombre** establecido en "Cimv2". Estas instancias representan los espacios de nombres raíz default y \\ \\ root \\ \\ cimv2, respectivamente.

## <a name="examples"></a>Ejemplos

En [el ejemplo de VBScript Enumerar](https://Gallery.TechNet.Microsoft.Com/4a8e84f1-4b52-452c-ae4f-e4e00e266257) todos los espacios de nombres WMI de la Galería de TechNet se usa una llamada recursiva para enumerar todas las instancias de la clase Namespace en un \_ \_ sistema.

En el ejemplo de código siguiente se recuperan todos los espacios de nombres de PowerShell.


```PowerShell
get-wmiobject __namespace -namespace 'root' -list -recurse | format-table __namespace
```



El ejemplo de código siguiente mejora con respecto al ejemplo anterior y agrega información adicional.


```PowerShell
# Set computer name 
$comp = "." 
 
# Get the name spaces on the local computer, and the local computer name 
$Namespace = get-wmiobject __namespace -namespace 'root' -list -recurse -computer $comp  
$hotsname = hostname 
 
# Display number of and names of the namespaces 
"{0} Namespaces on: {1}" -f $namespace.count, $hostname 
$NameSpace| sort __namespace  | Format-Table @{Expression = "__Namespace"; Label = "Namespace"}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |
| Espacio de nombres<br/>                | Todos los espacios de nombres WMI<br/>  |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**\_\_SystemClass**](--systemclass.md)
</dt> <dt>

[Clases del sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

 




