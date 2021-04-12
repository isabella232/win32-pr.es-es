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
# <a name="class-and-attribute-display-names"></a><span data-ttu-id="455d3-106">Nombres para mostrar de clases y atributos</span><span class="sxs-lookup"><span data-stu-id="455d3-106">Class and Attribute Display Names</span></span>

<span data-ttu-id="455d3-107">El especificador de presentación de una clase de objeto contiene los siguientes atributos que se pueden utilizar para especificar los nombres para mostrar localizados que se usan en la interfaz de usuario para los objetos de esa clase:</span><span class="sxs-lookup"><span data-stu-id="455d3-107">The display specifier for an object class contains the following attributes that can be used to specify the localized display names used in the UI for objects of that class:</span></span>

-   <span data-ttu-id="455d3-108">El atributo **classDisplayName** es una cadena Unicode de valor único que especifica el nombre para mostrar de la clase.</span><span class="sxs-lookup"><span data-stu-id="455d3-108">The **classDisplayName** attribute is a single-value Unicode string that specifies the class display name.</span></span>
-   <span data-ttu-id="455d3-109">El atributo **attributeDisplayNames** es una propiedad de varios valores que especifica los nombres que se van a usar en la interfaz de usuario para los atributos de la clase de objeto.</span><span class="sxs-lookup"><span data-stu-id="455d3-109">The **attributeDisplayNames** attribute is a multi-value property that specifies the names to use in the UI for attributes of the object class.</span></span>

<span data-ttu-id="455d3-110">Los valores de **attributeDisplayNames** son cadenas Unicode; cada elemento consta de un par de nombres delimitados por comas:</span><span class="sxs-lookup"><span data-stu-id="455d3-110">The **attributeDisplayNames** values are Unicode strings; each element consists of a comma-delimited name pair:</span></span>


```C++
<attribute name>,<display text>
```



<span data-ttu-id="455d3-111">En este ejemplo, " &lt; nombre de atributo &gt; " es el **lDAPDisplayName** del atributo y " &lt; Mostrar texto &gt; " es el texto que se muestra como el nombre de ese atributo en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="455d3-111">In this example, "&lt;attribute name&gt;" is the **lDAPDisplayName** of the attribute and "&lt;display text&gt;" is the text to display as the name of that attribute in the user interface.</span></span>

## <a name="guidelines-for-class-and-attribute-display-names"></a><span data-ttu-id="455d3-112">Directrices para nombres para mostrar de clases y atributos</span><span class="sxs-lookup"><span data-stu-id="455d3-112">Guidelines for Class and Attribute Display Names</span></span>

<span data-ttu-id="455d3-113">Dado que muchos proveedores pueden extender las clases con nuevos atributos o crear clases completamente nuevas, es importante que los nombres para mostrar de la clase y el atributo sean inequívocos y no produzcan conflictos.</span><span class="sxs-lookup"><span data-stu-id="455d3-113">Because many vendors may extend classes with new attributes or creating entirely new classes, it is important that the class and attribute display names are unambiguous and do not result in conflicts.</span></span>

<span data-ttu-id="455d3-114">Cada proveedor debe prefijar el nombre para mostrar de la clase con un identificador descriptivo único basado en el nombre del proveedor.</span><span class="sxs-lookup"><span data-stu-id="455d3-114">Each vendor should prefix the class display name with a unique friendly identifier based on the vendor name.</span></span> <span data-ttu-id="455d3-115">Por ejemplo, si la empresa ficticia Fabrikam Inc. crea una nueva clase derivada de la clase "Contact", puede tener un nombre para mostrar de clase único "contacto de Fabrikam".</span><span class="sxs-lookup"><span data-stu-id="455d3-115">For example, if the fictitious company, Fabrikam Inc., creates a new class derived from the "contact" class, they can have a unique class display name "Fabrikam Contact."</span></span>

<span data-ttu-id="455d3-116">Si un proveedor extiende una clase existente con nuevos atributos, debe identificar de nuevo de forma única el nombre para mostrar del atributo para que no se produzcan conflictos con otros nombres para mostrar del atributo.</span><span class="sxs-lookup"><span data-stu-id="455d3-116">If a vendor extends an existing class with new attributes, they should again uniquely identify the attribute display name so that no conflicts occur with other attribute display names.</span></span> <span data-ttu-id="455d3-117">Una vez más, el prefijo del nombre para mostrar del atributo con un identificador descriptivo único basado en el nombre del proveedor es un procedimiento recomendado.</span><span class="sxs-lookup"><span data-stu-id="455d3-117">Again, prefixing the attribute display name with unique friendly identifier based on the vendor name is good practice.</span></span> <span data-ttu-id="455d3-118">Por ejemplo, si la compañía de Fabrikam extiende la clase de usuario con un nuevo atributo HR, podría mostrar el atributo de forma exclusiva como "información de empresa de recursos humanos".</span><span class="sxs-lookup"><span data-stu-id="455d3-118">For example, if the Fabrikam company extends the user class with a new HR attribute, they could uniquely display the attribute as "Fabrikam HR Information."</span></span>

<span data-ttu-id="455d3-119">Además, desde una perspectiva de localización, cada proveedor debe localizar los nombres para mostrar de clase y atributo en cada idioma admitido por Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="455d3-119">In addition, from a localization perspective, each vendor should localize the class and attribute display names into each language supported by Windows 2000.</span></span>

## <a name="adding-a-value-to-the-attributedisplaynames-attribute"></a><span data-ttu-id="455d3-120">Agregar un valor al atributo attributeDisplayNames</span><span class="sxs-lookup"><span data-stu-id="455d3-120">Adding a Value to the attributeDisplayNames Attribute</span></span>

<span data-ttu-id="455d3-121">\*\*Para agregar un valor de asignación de nombres al atributo \*\*attributeDisplayNames\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="455d3-121">**To add a name mapping value to the **attributeDisplayNames** attribute**</span></span>

1.  <span data-ttu-id="455d3-122">Determine si existe el valor de asignación de nombres para el atributo.</span><span class="sxs-lookup"><span data-stu-id="455d3-122">Determine if the name mapping value for the attribute exists.</span></span> <span data-ttu-id="455d3-123">Si se va a reemplazar un valor de asignación de nombres, elimine primero el valor existente mediante el método [**IADs::P Utex**](/windows/desktop/api/iads/nf-iads-iads-putex) , con el parámetro *LnControlCode* establecido en **ADS \_ Property \_ Delete** y el parámetro *vProp* establecido en el valor que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="455d3-123">If a name mapping value is to be replaced, first deleted the existing value, using the [**IADs::PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) method, with the *lnControlCode* parameter set to **ADS\_PROPERTY\_DELETE** and the *vProp* parameter set to the value to be removed.</span></span> <span data-ttu-id="455d3-124">No use la **\_ propiedad ADS \_ Clear** o la actualización de la **\_ propiedad \_ ADS** para *lnControlCode*.</span><span class="sxs-lookup"><span data-stu-id="455d3-124">Do not use **ADS\_PROPERTY\_CLEAR** or **ADS\_PROPERTY\_UPDATE** for *lnControlCode*.</span></span>
2.  <span data-ttu-id="455d3-125">Cree la cadena que representa el nombre para mostrar del atributo.</span><span class="sxs-lookup"><span data-stu-id="455d3-125">Create the string that represents the attribute display name.</span></span> <span data-ttu-id="455d3-126">Para obtener un ejemplo, vea el formato anterior.</span><span class="sxs-lookup"><span data-stu-id="455d3-126">For an example, see the format above.</span></span>
3.  <span data-ttu-id="455d3-127">Use el método [**IADs::P Utex**](/windows/desktop/api/iads/nf-iads-iads-putex) con el parámetro *lnControlCode* establecido en **la \_ propiedad ADS \_ Append** para agregar el nuevo valor.</span><span class="sxs-lookup"><span data-stu-id="455d3-127">Use the [**IADs::PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) method with the *lnControlCode* parameter set to **ADS\_PROPERTY\_APPEND** to add the new value.</span></span>
4.  <span data-ttu-id="455d3-128">Llame a [**IADs:: SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) para confirmar los cambios en el directorio.</span><span class="sxs-lookup"><span data-stu-id="455d3-128">Call [**IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) to commit the changes to the directory.</span></span>

<span data-ttu-id="455d3-129">Para obtener más información sobre la nomenclatura de nuevas clases y atributos, vea [asignar nombres a atributos y clases](naming-attributes-and-classes.md).</span><span class="sxs-lookup"><span data-stu-id="455d3-129">For more information about naming new classes and attributes, see [Naming Attributes and Classes](naming-attributes-and-classes.md).</span></span>

 

 