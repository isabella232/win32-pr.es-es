---
description: El sistema de propiedades contiene una propiedad denominada System.Kind, que divide los elementos en tipos según la extensión de nombre de archivo y con los que los usuarios finales pueden identificarse fácilmente.
ms.assetid: 1466b4c7-49ea-417a-ac94-7b45515ccb96
title: Usar nombres de tipo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dca36d7c1de587efd8d96f0c18aaca9457721714
ms.sourcegitcommit: ecd0ba4732f5264aab9baa2839c11f7fea36318f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/07/2021
ms.locfileid: "113481880"
---
# <a name="using-kind-names"></a>Usar nombres de tipo

El sistema de propiedades contiene una propiedad denominada , que divide los elementos en tipos según la extensión de nombre de archivo y con los que los usuarios finales pueden `System.Kind` identificarse fácilmente.

Este tema se organiza de la siguiente manera:

-   [Acerca de la propiedad System.Kind](#about-the-systemkind-property)
-   [Jerarquía y registro de valores de tipo](#kind-value-hierarchy-and-registration)
-   [Recursos adicionales](#additional-resources)
-   [Temas relacionados](#related-topics)

## <a name="about-the-systemkind-property"></a>Acerca de la propiedad System.Kind

Kind se introdujo en Windows Vista para expresar una noción más fácil de usar del tipo de archivo. La propiedad divide los elementos en tipos y proporciona un nombre de tipo con el que los usuarios finales pueden `System.Kind` identificarse, como Documentos, Música, Imágenes, etc. Por lo tanto, los nombres de tipo se han conocido como fáciles de usar. Dado que la propiedad se establece en el mismo valor para los elementos del mismo tipo de archivo y asocia elementos que tienen características similares a una propiedad común, el sistema y el usuario pueden actuar en el grupo como `System.Kind` un todo. Por ejemplo, la propiedad se puede usar para limitar una búsqueda a elementos de un tipo específico, mostrar las propiedades más relevantes para un elemento en la vista Contenido o agrupar elementos `System.Kind` similares.

Dado que Kind es una propiedad de cadena de varios valores, puede tener un `audio;video` valor `link;document` o Kind. Un `System.Kind` valor es una lista ordenada de valores de cadena. En algunos casos, podría haber solo un elemento en esa lista. En otros casos, un elemento puede pertenecer a más de un tipo. Para obtener un ejemplo de un elemento que pertenece a más de un tipo, vea el ejemplo de clave del Registro de este tema. Los valores de cadena son de un conjunto predefinido de valores conocidos. Los valores se comparan mediante funciones de comparación de cadenas que no tienen en cuenta mayúsculas de minúsculas y que no tienen en cuenta la configuración regional. Estas cadenas no están localizadas.

Algunos nombres de tipo ya están asociados a propiedades y patrones de diseño. Por ejemplo, los elementos asociados a los elementos y asociados a muestran propiedades diferentes incluso cuando están en la misma vista, debido a las propiedades y los patrones de diseño que ya están asociados a esos dos nombres `Kind.Picture` `Kind.Document` kind. Cada tipo de elemento se puede asociar a uno de los cuatro patrones de diseño únicos que definen el número de propiedades que se muestran para cada elemento y su diseño. Para obtener más información, vea [Vista de contenido basada en el tipo de archivo o la asociación de tipo](/previous-versions/windows/desktop/legacy/ee330739(v=vs.85)).

## <a name="kind-value-hierarchy-and-registration"></a>Jerarquía y registro de valores de tipo

Un `Kind` valor debe representar uno de los valores de la lista siguiente.

```
Item
   Folder
   Program
   Game
   WebHistory
   Feed
   Document
   Link
   Movie
   Music
   RecordedTV
   Video
   Picture
   Communications
      Calendar
      Contact
      E-Mail
      Task
      Journal
      Note
      InstantMessage
```

Los controladores de propiedades pueden declarar su propiedad estáticamente a través del Registro, o bien pueden proporcionar el valor dinámicamente a través de su código como lo harían con `System.Kind` una propiedad estándar.

Para definir estáticamente la propiedad , se agrega una entrada de valor REG SZ en la clave del Registro KindMap como se `Kind` muestra en el ejemplo siguiente. **\_** 

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  KindMap
                     .recipe = Document
                     .ccc = Contact; Communications
```

Tenga en cuenta `Kind` que puede ser un valor único o varios valores en una cadena delimitada por punto y coma. Al proporcionar varios valores, el valor más `Kind` específico se muestra primero con el siguiente valor menos específico. En el ejemplo, contact se denomina primero porque es jerárquicamente más específico que Communications. Se supone **que el** valor Item no debe proporcionarse explícitamente.

## <a name="additional-resources"></a>Recursos adicionales

-   Para obtener documentación de referencia sobre las propiedades, [vea System.Kind](./props-system-kind.md) y [System.KindText](./props-system-kindtext.md).
-   Para obtener más información sobre cómo crear tipos de archivo nuevos o existentes, vea [Tipos de archivo](../shell/fa-file-types.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Descripción de los controladores de propiedades](./building-property-handlers-properties.md)
</dt> <dt>

[Usar listas de propiedades](./building-property-handlers-property-lists.md)
</dt> <dt>

[Inicialización de controladores de propiedades](./building-property-handlers-property-handlers.md)
</dt> <dt>

[Registro y distribución de controladores de propiedades](./prophand-reg-dist.md)
</dt> <dt>

[Procedimientos recomendados y preguntas más frecuentes sobre el controlador de propiedades](./prophand-bestprac-faq.yml)
</dt> </dl>

 

 
