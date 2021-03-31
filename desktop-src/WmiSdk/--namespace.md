---
description: Representa un espacio de nombres WMI.
ms.assetid: d5f0abc7-32cf-4d85-b5cd-5d60c991bcbc
ms.tgt_platform: multiple
title: __Namespace (clase)
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
ms.openlocfilehash: 9f396b588f372f26a808e97593ffcc30eac9b3ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912754"
---
# <a name="__namespace-class"></a>\_\_Namespace (clase)

La clase de sistema de **\_ \_ espacio de nombres** representa un espacio de nombres WMI.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class __Namespace : __SystemClass
{
  string Name;
};
```

## <a name="members"></a>Miembros

La clase de **\_ \_ espacio de nombres** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase de **\_ \_ espacio de nombres** tiene estas propiedades.

<dl> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: [ **clave**](standard-qualifiers.md)
</dt> </dl>

Nombre del espacio de nombres.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase de **\_ \_ espacio de nombres** se deriva de [**\_ \_ SystemClass**](--systemclass.md), que no tiene propiedades.

Puede usar el **\_ \_ espacio de nombres** para identificar, crear y eliminar espacios de nombres secundarios en el espacio de nombres de trabajo actual para el que tiene un objeto [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) . Al crear una nueva instancia del **\_ \_ espacio** de nombres en cualquier espacio de nombres de trabajo, se crea un espacio de nombres secundario en el espacio de nombres de trabajo. A la inversa, al eliminar una instancia del **\_ \_ espacio de nombres** se quita el espacio de nombres secundario del espacio de nombres de trabajo. Tenga en cuenta que al eliminar un espacio de nombres secundario también se eliminan todas sus clases e instancias.

La enumeración de instancias de esta clase en cualquier espacio de nombres de trabajo proporciona los espacios de nombres secundarios disponibles.

Por ejemplo, en el \\ espacio de nombres raíz hay dos instancias de **\_ \_ espacio de nombres**. Uno tiene la propiedad **Name** establecida en "default", el otro tiene el **nombre** establecido en "Cimv2". Estas instancias representan el \\ \\ valor predeterminado raíz y los \\ espacios de nombres raíz de \\ cimv2, respectivamente.

## <a name="examples"></a>Ejemplos

En el ejemplo de VBScript de [lista de todos los espacios de nombres de WMI](https://Gallery.TechNet.Microsoft.Com/4a8e84f1-4b52-452c-ae4f-e4e00e266257) de la galería de TechNet se usa una llamada recursiva para mostrar todas las instancias de la clase de espacio de \_ \_ nombres en un sistema.

En el ejemplo de código siguiente se recuperan todos los espacios de nombres en PowerShell.


```PowerShell
get-wmiobject __namespace -namespace 'root' -list -recurse | format-table __namespace
```



En el ejemplo de código siguiente se mejora el ejemplo anterior y se agrega información adicional.


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



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |
| Espacio de nombres<br/>                | Todos los espacios de nombres WMI<br/>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_\_SystemClass**](--systemclass.md)
</dt> <dt>

[Clases del sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

 




