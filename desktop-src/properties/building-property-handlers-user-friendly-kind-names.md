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
# <a name="using-kind-names"></a><span data-ttu-id="29083-103">Usar nombres de tipo</span><span class="sxs-lookup"><span data-stu-id="29083-103">Using Kind Names</span></span>

<span data-ttu-id="29083-104">El sistema de propiedades contiene una propiedad denominada `System.Kind` , que divide los elementos en tipos de acuerdo con la extensión de nombre de archivo, y los usuarios finales pueden identificar con facilidad con.</span><span class="sxs-lookup"><span data-stu-id="29083-104">The property system contains a property called `System.Kind`, which divides items into types according to the file name extension, and which end users can easily identify with.</span></span>

<span data-ttu-id="29083-105">Este tema se organiza de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="29083-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="29083-106">Acerca de la propiedad System. Kind</span><span class="sxs-lookup"><span data-stu-id="29083-106">About the System.Kind Property</span></span>](#about-the-systemkind-property)
-   [<span data-ttu-id="29083-107">Jerarquía y registro de valores de clase</span><span class="sxs-lookup"><span data-stu-id="29083-107">Kind Value Hierarchy and Registration</span></span>](#kind-value-hierarchy-and-registration)
-   [<span data-ttu-id="29083-108">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="29083-108">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="29083-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="29083-109">Related topics</span></span>](#related-topics)

## <a name="about-the-systemkind-property"></a><span data-ttu-id="29083-110">Acerca de la propiedad System. Kind</span><span class="sxs-lookup"><span data-stu-id="29083-110">About the System.Kind Property</span></span>

<span data-ttu-id="29083-111">Se presentó en Windows Vista para expresar una noción más fácil de ver del tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="29083-111">Kind was introduced in Windows Vista to express a more user-friendly notion of file type.</span></span> <span data-ttu-id="29083-112">La `System.Kind` propiedad divide los elementos en tipos y proporciona un nombre de clase que los usuarios finales pueden identificar con, como documentos, música, imágenes, etc.</span><span class="sxs-lookup"><span data-stu-id="29083-112">The `System.Kind` property divides items into types and provides a Kind name that end users can identify with, such as Documents, Music, Pictures, and so forth.</span></span> <span data-ttu-id="29083-113">Por lo tanto, los nombres de tipo deben conocerse como fáciles de usar.</span><span class="sxs-lookup"><span data-stu-id="29083-113">Hence, Kind names have come to be known as user-friendly.</span></span> <span data-ttu-id="29083-114">Dado que la `System.Kind` propiedad se establece en el mismo valor para los elementos del mismo tipo de archivo, y asocia elementos que tienen características similares con una propiedad común, el sistema y el usuario pueden actuar en el grupo en su totalidad.</span><span class="sxs-lookup"><span data-stu-id="29083-114">Because the `System.Kind` property is set to the same value for items of the same file type, and associates items that have similar characteristics with a common property, the system and the user can act on the group as a whole.</span></span> <span data-ttu-id="29083-115">Por ejemplo, la `System.Kind` propiedad se puede utilizar para limitar una búsqueda a elementos de un tipo específico, mostrar las propiedades más importantes de un elemento en la vista de contenido o agrupar elementos similares.</span><span class="sxs-lookup"><span data-stu-id="29083-115">For example, the `System.Kind` property can be used to limit a search to items of a specific kind, display the most relevant properties for an item in the Content view, or group similar items together.</span></span>

<span data-ttu-id="29083-116">Dado que Kind es una propiedad de cadena de varios valores, puede tener `audio;video` un `link;document` valor de tipo o.</span><span class="sxs-lookup"><span data-stu-id="29083-116">Because Kind is a multi-value string property, you can have an `audio;video` or `link;document` Kind value.</span></span> <span data-ttu-id="29083-117">Un `System.Kind` valor es una lista ordenada de valores de cadena.</span><span class="sxs-lookup"><span data-stu-id="29083-117">A `System.Kind` values is an ordered list of string values.</span></span> <span data-ttu-id="29083-118">En algunos casos, puede haber solo un elemento en esa lista.</span><span class="sxs-lookup"><span data-stu-id="29083-118">In some cases, there might be only one element in that list.</span></span> <span data-ttu-id="29083-119">En otros casos, un elemento puede pertenecer a más de un tipo.</span><span class="sxs-lookup"><span data-stu-id="29083-119">In other cases, an item can belong to more than one Kind.</span></span> <span data-ttu-id="29083-120">Para obtener un ejemplo de un elemento que pertenece a más de un tipo, consulte el ejemplo de la clave del registro en este tema.</span><span class="sxs-lookup"><span data-stu-id="29083-120">For an example of an item that belongs to more than one Kind, see the registry key example in this topic.</span></span> <span data-ttu-id="29083-121">Los valores de cadena provienen de un conjunto predefinido de valores conocidos.</span><span class="sxs-lookup"><span data-stu-id="29083-121">The string values are from a predefined set of known values.</span></span> <span data-ttu-id="29083-122">Los valores se comparan mediante funciones de comparación de cadenas que no distinguen entre mayúsculas y minúsculas y que no distinguen entre ellas.</span><span class="sxs-lookup"><span data-stu-id="29083-122">The values are compared by using case-insensitive and locale-insensitive string-compare functions.</span></span> <span data-ttu-id="29083-123">Estas cadenas no están localizadas.</span><span class="sxs-lookup"><span data-stu-id="29083-123">These strings are not localized.</span></span>

<span data-ttu-id="29083-124">Algunos nombres de tipo ya están asociados a propiedades y patrones de diseño.</span><span class="sxs-lookup"><span data-stu-id="29083-124">Some Kind names are already associated with properties and layout patterns.</span></span> <span data-ttu-id="29083-125">Por ejemplo, los elementos asociados a `Kind.Picture` los elementos y asociados a `Kind.Document` muestran propiedades diferentes incluso cuando están en la misma vista, debido a las propiedades y patrones de diseño que ya están asociados a esos dos nombres de tipos.</span><span class="sxs-lookup"><span data-stu-id="29083-125">For example, items associated with `Kind.Picture` and items associated with `Kind.Document` display different properties even when they are in the same view, because of the properties and layout patterns that are already associated with those two Kind names.</span></span> <span data-ttu-id="29083-126">Cada tipo de elemento puede asociarse a uno de cuatro patrones de diseño únicos que define el número de propiedades que se muestran para cada elemento y su diseño.</span><span class="sxs-lookup"><span data-stu-id="29083-126">Each item Kind can be associated with one of four unique layout patterns that defines the number of properties displayed for each item and their layout.</span></span> <span data-ttu-id="29083-127">Para obtener más información, vea [vista de contenido basada en el tipo de archivo o la Asociación de tipos](/previous-versions/windows/desktop/legacy/ee330739(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="29083-127">For more information, see [Content View based on the File Type or Kind Association](/previous-versions/windows/desktop/legacy/ee330739(v=vs.85)).</span></span>

## <a name="kind-value-hierarchy-and-registration"></a><span data-ttu-id="29083-128">Jerarquía y registro de valores de clase</span><span class="sxs-lookup"><span data-stu-id="29083-128">Kind Value Hierarchy and Registration</span></span>

<span data-ttu-id="29083-129">Un `Kind` valor debe representar uno de los valores de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="29083-129">A `Kind` value must represent one of the values in the following list.</span></span>

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

<span data-ttu-id="29083-130">Los controladores de propiedades pueden declarar su `System.Kind` propiedad estáticamente a través del registro, o bien pueden proporcionar el valor dinámicamente a través de su código como lo harían con una propiedad estándar.</span><span class="sxs-lookup"><span data-stu-id="29083-130">Property handlers can declare their `System.Kind` property statically through the registry, or they can provide the value dynamically through their code as they would with a standard property.</span></span>

<span data-ttu-id="29083-131">Para definir la propiedad estáticamente `Kind` , se agrega una entrada de valor **reg \_ SZ** en la clave del registro **KindMap** , tal y como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="29083-131">To statically define the `Kind` property, a **REG\_SZ** value entry is added under the **KindMap** registry key as shown in the following example.</span></span>

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

<span data-ttu-id="29083-132">Tenga en cuenta que `Kind` puede ser un valor único o varios valores en una cadena delimitada por punto y coma.</span><span class="sxs-lookup"><span data-stu-id="29083-132">Note that the `Kind` can be a single value or multiple values in a semi-colon delimited string.</span></span> <span data-ttu-id="29083-133">Al proporcionar varios valores, el valor más específico `Kind` se enumera primero con los menos específicos que se indican a continuación.</span><span class="sxs-lookup"><span data-stu-id="29083-133">When providing multiple values, the most specific `Kind` value is listed first with the least specific following.</span></span> <span data-ttu-id="29083-134">En el ejemplo, el contacto se denomina primero porque es jerárquicamente más específico que las comunicaciones.</span><span class="sxs-lookup"><span data-stu-id="29083-134">In the example, Contact is named first because it is hierarchically more specific than Communications.</span></span> <span data-ttu-id="29083-135">Se supone el **elemento** de valor y no se debe proporcionar explícitamente.</span><span class="sxs-lookup"><span data-stu-id="29083-135">The value **Item** is assumed and should not be explicity provided.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="29083-136">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="29083-136">Additional Resources</span></span>

-   <span data-ttu-id="29083-137">Para obtener documentación de referencia sobre las propiedades, vea [System. Kind](./props-system-kind.md) y [System. KindText](./props-system-kindtext.md).</span><span class="sxs-lookup"><span data-stu-id="29083-137">For reference documentation about properties, see [System.Kind](./props-system-kind.md) and [System.KindText](./props-system-kindtext.md).</span></span>
-   <span data-ttu-id="29083-138">Para obtener más información sobre la creación de nuevos tipos de archivo o el uso de ellos, consulte [tipos de archivo](../shell/fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="29083-138">For more information about creating new or using existing file types, see [File Types](../shell/fa-file-types.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="29083-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="29083-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29083-140">Descripción de los controladores de propiedades</span><span class="sxs-lookup"><span data-stu-id="29083-140">Understanding Property Handlers</span></span>](./building-property-handlers-properties.md)
</dt> <dt>

[<span data-ttu-id="29083-141">Usar listas de propiedades</span><span class="sxs-lookup"><span data-stu-id="29083-141">Using Property Lists</span></span>](./building-property-handlers-property-lists.md)
</dt> <dt>

[<span data-ttu-id="29083-142">Inicializar controladores de propiedades</span><span class="sxs-lookup"><span data-stu-id="29083-142">Initializing Property Handlers</span></span>](./building-property-handlers-property-handlers.md)
</dt> <dt>

[<span data-ttu-id="29083-143">Registrar y distribuir controladores de propiedades</span><span class="sxs-lookup"><span data-stu-id="29083-143">Registering and Distributing Property Handlers</span></span>](./prophand-reg-dist.md)
</dt> <dt>

[<span data-ttu-id="29083-144">Prácticas recomendadas y preguntas más frecuentes sobre controladores de propiedades</span><span class="sxs-lookup"><span data-stu-id="29083-144">Property Handler Best Practices and FAQ</span></span>](./prophand-bestprac-faq.md)
</dt> </dl>

 

 
