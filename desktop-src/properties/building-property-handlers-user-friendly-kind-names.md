---
description: El sistema de propiedades contiene una propiedad denominada System. Kind, que divide los elementos en tipos de acuerdo con la extensión de nombre de archivo, y los usuarios finales pueden identificar con facilidad con.
ms.assetid: 1466b4c7-49ea-417a-ac94-7b45515ccb96
title: Usar nombres de tipo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f358306deaeb04d4ea30b10b0665cdc8323b4d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360562"
---
# <a name="using-kind-names"></a>Usar nombres de tipo

El sistema de propiedades contiene una propiedad denominada `System.Kind` , que divide los elementos en tipos de acuerdo con la extensión de nombre de archivo, y los usuarios finales pueden identificar con facilidad con.

Este tema se organiza de la siguiente manera:

-   [Acerca de la propiedad System. Kind](#about-the-systemkind-property)
-   [Jerarquía y registro de valores de clase](#kind-value-hierarchy-and-registration)
-   [Recursos adicionales](#additional-resources)
-   [Temas relacionados](#related-topics)

## <a name="about-the-systemkind-property"></a>Acerca de la propiedad System. Kind

Se presentó en Windows Vista para expresar una noción más fácil de ver del tipo de archivo. La `System.Kind` propiedad divide los elementos en tipos y proporciona un nombre de clase que los usuarios finales pueden identificar con, como documentos, música, imágenes, etc. Por lo tanto, los nombres de tipo deben conocerse como fáciles de usar. Dado que la `System.Kind` propiedad se establece en el mismo valor para los elementos del mismo tipo de archivo, y asocia elementos que tienen características similares con una propiedad común, el sistema y el usuario pueden actuar en el grupo en su totalidad. Por ejemplo, la `System.Kind` propiedad se puede utilizar para limitar una búsqueda a elementos de un tipo específico, mostrar las propiedades más importantes de un elemento en la vista de contenido o agrupar elementos similares.

Dado que Kind es una propiedad de cadena de varios valores, puede tener `audio;video` un `link;document` valor de tipo o. Un `System.Kind` valor es una lista ordenada de valores de cadena. En algunos casos, puede haber solo un elemento en esa lista. En otros casos, un elemento puede pertenecer a más de un tipo. Para obtener un ejemplo de un elemento que pertenece a más de un tipo, consulte el ejemplo de la clave del registro en este tema. Los valores de cadena provienen de un conjunto predefinido de valores conocidos. Los valores se comparan mediante funciones de comparación de cadenas que no distinguen entre mayúsculas y minúsculas y que no distinguen entre ellas. Estas cadenas no están localizadas.

Algunos nombres de tipo ya están asociados a propiedades y patrones de diseño. Por ejemplo, los elementos asociados a `Kind.Picture` los elementos y asociados a `Kind.Document` muestran propiedades diferentes incluso cuando están en la misma vista, debido a las propiedades y patrones de diseño que ya están asociados a esos dos nombres de tipos. Cada tipo de elemento puede asociarse a uno de cuatro patrones de diseño únicos que define el número de propiedades que se muestran para cada elemento y su diseño. Para obtener más información, vea [vista de contenido basada en el tipo de archivo o la Asociación de tipos](/previous-versions/windows/desktop/legacy/ee330739(v=vs.85)).

## <a name="kind-value-hierarchy-and-registration"></a>Jerarquía y registro de valores de clase

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

Los controladores de propiedades pueden declarar su `System.Kind` propiedad estáticamente a través del registro, o bien pueden proporcionar el valor dinámicamente a través de su código como lo harían con una propiedad estándar.

Para definir la propiedad estáticamente `Kind` , se agrega una entrada de valor **reg \_ SZ** en la clave del registro **KindMap** , tal y como se muestra en el ejemplo siguiente.

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

Tenga en cuenta que `Kind` puede ser un valor único o varios valores en una cadena delimitada por punto y coma. Al proporcionar varios valores, el valor más específico `Kind` se enumera primero con los menos específicos que se indican a continuación. En el ejemplo, el contacto se denomina primero porque es jerárquicamente más específico que las comunicaciones. Se supone el **elemento** de valor y no se debe proporcionar explícitamente.

## <a name="additional-resources"></a>Recursos adicionales

-   Para obtener documentación de referencia sobre las propiedades, vea [System. Kind](./props-system-kind.md) y [System. KindText](./props-system-kindtext.md).
-   Para obtener más información sobre la creación de nuevos tipos de archivo o el uso de ellos, consulte [tipos de archivo](../shell/fa-file-types.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Descripción de los controladores de propiedades](./building-property-handlers-properties.md)
</dt> <dt>

[Usar listas de propiedades](./building-property-handlers-property-lists.md)
</dt> <dt>

[Inicializar controladores de propiedades](./building-property-handlers-property-handlers.md)
</dt> <dt>

[Registrar y distribuir controladores de propiedades](./prophand-reg-dist.md)
</dt> <dt>

[Prácticas recomendadas y preguntas más frecuentes sobre controladores de propiedades](./prophand-bestprac-faq.md)
</dt> </dl>

 

 
