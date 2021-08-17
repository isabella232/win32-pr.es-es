---
title: Nombres para mostrar de clases y atributos
description: Este tema contiene información sobre y directrices para los nombres para mostrar de clases y atributos.
ms.assetid: c85905b2-ed8b-4032-8c54-fd4de8b34ecf
ms.tgt_platform: multiple
keywords:
- display specifiers AD ,class and attribute display names
- nombres para mostrar de clase de AD
- nombres para mostrar de atributos de AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 213132acfa6463b1c1e8a7615f5d7f488e53edfcdf9b75f8df5759fcd0e4d398
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118022596"
---
# <a name="class-and-attribute-display-names"></a>Nombres para mostrar de clases y atributos

El especificador para mostrar de una clase de objeto contiene los siguientes atributos que se pueden usar para especificar los nombres para mostrar localizados usados en la interfaz de usuario para los objetos de esa clase:

-   El **atributo classDisplayName** es una cadena Unicode de un solo valor que especifica el nombre para mostrar de la clase.
-   El **atributo attributeDisplayNames** es una propiedad de varios valores que especifica los nombres que se usarán en la interfaz de usuario para los atributos de la clase de objeto.

Los **valores attributeDisplayNames** son cadenas Unicode; cada elemento consta de un par de nombres delimitados por comas:


```C++
<attribute name>,<display text>
```



En este ejemplo, " attribute name " es &lt; &gt; el **lDAPDisplayName** del atributo y " display text " es el texto que se va a mostrar como el nombre de ese atributo en la interfaz &lt; de &gt; usuario.

## <a name="guidelines-for-class-and-attribute-display-names"></a>Directrices para los nombres para mostrar de clases y atributos

Dado que muchos proveedores pueden extender clases con atributos nuevos o crear clases completamente nuevas, es importante que los nombres para mostrar de clase y atributo sean inequívocos y no provocan conflictos.

Cada proveedor debe antecer el nombre para mostrar de la clase con un identificador descriptivo único basado en el nombre del proveedor. Por ejemplo, si la compañía ficticia Fabrikam Inc., crea una nueva clase derivada de la clase "contact", puede tener un nombre para mostrar de clase único "Fabrikam Contact".

Si un proveedor extiende una clase existente con nuevos atributos, debe identificar de nuevo de forma única el nombre para mostrar del atributo para que no se produzca ningún conflicto con otros nombres para mostrar de atributos. Una vez más, es una buena práctica prefiriendo el nombre para mostrar del atributo con un identificador descriptivo único basado en el nombre del proveedor. Por ejemplo, si la empresa Fabrikam extiende la clase de usuario con un nuevo atributo hr, podría mostrar de forma única el atributo como "Información de RR. UU. de Fabrikam".

Además, desde una perspectiva de localización, cada proveedor debe localizar los nombres para mostrar de clase y atributo en cada idioma admitido por Windows 2000.

## <a name="adding-a-value-to-the-attributedisplaynames-attribute"></a>Agregar un valor al atributo attributeDisplayNames

**Para agregar un valor de asignación de nombre al **atributo attributeDisplayNames****

1.  Determine si existe el valor de asignación de nombres para el atributo. Si se va a reemplazar un valor de asignación de nombre, elimine primero el valor existente mediante el método [**IADs::P utEx,**](/windows/desktop/api/iads/nf-iads-iads-putex) con el parámetro *lnControlCode* establecido en **ADS PROPERTY \_ \_ DELETE** y el parámetro *vProp* establecido en el valor que se va a quitar. No use **ADS PROPERTY CLEAR \_ \_ o** **ADS PROPERTY \_ \_ UPDATE** para *lnControlCode*.
2.  Cree la cadena que representa el nombre para mostrar del atributo. Para obtener un ejemplo, vea el formato anterior.
3.  Use el [**método IADs::P utEx**](/windows/desktop/api/iads/nf-iads-iads-putex) con el parámetro *lnControlCode* establecido en **ADS PROPERTY \_ \_ APPEND** para agregar el nuevo valor.
4.  Llame [**a IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) para confirmar los cambios en el directorio.

Para obtener más información sobre cómo asignar nombres a nuevas clases y atributos, vea [Asignar nombres a atributos y clases.](naming-attributes-and-classes.md)

 

 