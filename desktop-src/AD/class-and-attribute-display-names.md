---
title: Nombres para mostrar de clases y atributos
description: Este tema contiene información acerca de las instrucciones y los nombres para mostrar de clases y atributos.
ms.assetid: c85905b2-ed8b-4032-8c54-fd4de8b34ecf
ms.tgt_platform: multiple
keywords:
- especificadores de pantalla AD, nombres para mostrar de clases y atributos
- nombres para mostrar de clase AD
- nombres para mostrar de atributos AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d65cd6ac6fc3077ff0d2bba15ffa9904b147654
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104487498"
---
# <a name="class-and-attribute-display-names"></a>Nombres para mostrar de clases y atributos

El especificador de presentación de una clase de objeto contiene los siguientes atributos que se pueden utilizar para especificar los nombres para mostrar localizados que se usan en la interfaz de usuario para los objetos de esa clase:

-   El atributo **classDisplayName** es una cadena Unicode de valor único que especifica el nombre para mostrar de la clase.
-   El atributo **attributeDisplayNames** es una propiedad de varios valores que especifica los nombres que se van a usar en la interfaz de usuario para los atributos de la clase de objeto.

Los valores de **attributeDisplayNames** son cadenas Unicode; cada elemento consta de un par de nombres delimitados por comas:


```C++
<attribute name>,<display text>
```



En este ejemplo, " &lt; nombre de atributo &gt; " es el **lDAPDisplayName** del atributo y " &lt; Mostrar texto &gt; " es el texto que se muestra como el nombre de ese atributo en la interfaz de usuario.

## <a name="guidelines-for-class-and-attribute-display-names"></a>Directrices para nombres para mostrar de clases y atributos

Dado que muchos proveedores pueden extender las clases con nuevos atributos o crear clases completamente nuevas, es importante que los nombres para mostrar de la clase y el atributo sean inequívocos y no produzcan conflictos.

Cada proveedor debe prefijar el nombre para mostrar de la clase con un identificador descriptivo único basado en el nombre del proveedor. Por ejemplo, si la empresa ficticia Fabrikam Inc. crea una nueva clase derivada de la clase "Contact", puede tener un nombre para mostrar de clase único "contacto de Fabrikam".

Si un proveedor extiende una clase existente con nuevos atributos, debe identificar de nuevo de forma única el nombre para mostrar del atributo para que no se produzcan conflictos con otros nombres para mostrar del atributo. Una vez más, el prefijo del nombre para mostrar del atributo con un identificador descriptivo único basado en el nombre del proveedor es un procedimiento recomendado. Por ejemplo, si la compañía de Fabrikam extiende la clase de usuario con un nuevo atributo HR, podría mostrar el atributo de forma exclusiva como "información de empresa de recursos humanos".

Además, desde una perspectiva de localización, cada proveedor debe localizar los nombres para mostrar de clase y atributo en cada idioma admitido por Windows 2000.

## <a name="adding-a-value-to-the-attributedisplaynames-attribute"></a>Agregar un valor al atributo attributeDisplayNames

**Para agregar un valor de asignación de nombres al atributo **attributeDisplayNames****

1.  Determine si existe el valor de asignación de nombres para el atributo. Si se va a reemplazar un valor de asignación de nombres, elimine primero el valor existente mediante el método [**IADs::P Utex**](/windows/desktop/api/iads/nf-iads-iads-putex) , con el parámetro *LnControlCode* establecido en **ADS \_ Property \_ Delete** y el parámetro *vProp* establecido en el valor que se va a quitar. No use la **\_ propiedad ADS \_ Clear** o la actualización de la **\_ propiedad \_ ADS** para *lnControlCode*.
2.  Cree la cadena que representa el nombre para mostrar del atributo. Para obtener un ejemplo, vea el formato anterior.
3.  Use el método [**IADs::P Utex**](/windows/desktop/api/iads/nf-iads-iads-putex) con el parámetro *lnControlCode* establecido en **la \_ propiedad ADS \_ Append** para agregar el nuevo valor.
4.  Llame a [**IADs:: SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) para confirmar los cambios en el directorio.

Para obtener más información sobre la nomenclatura de nuevas clases y atributos, vea [asignar nombres a atributos y clases](naming-attributes-and-classes.md).

 

 