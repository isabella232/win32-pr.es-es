---
title: Clases y asociaciones predeterminadas
description: Para determinadas categorías, una sola clase puede asociarse como la clase predeterminada.
ms.assetid: 9c48615b-ab10-44e4-a032-49d5ee0c9b01
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 871c537535c57da0809effbe3ee8ec086a88fd5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418374"
---
# <a name="default-classes-and-associations"></a><span data-ttu-id="722ef-103">Clases y asociaciones predeterminadas</span><span class="sxs-lookup"><span data-stu-id="722ef-103">Default Classes and Associations</span></span>

<span data-ttu-id="722ef-104">Para determinadas categorías, una sola clase puede asociarse como la clase predeterminada.</span><span class="sxs-lookup"><span data-stu-id="722ef-104">For certain categories, a single class can be associated as the default class.</span></span> <span data-ttu-id="722ef-105">La clase predeterminada se selecciona siempre que se requiera esa categoría determinada de objeto.</span><span class="sxs-lookup"><span data-stu-id="722ef-105">The default class is selected whenever that particular category of object is required.</span></span> <span data-ttu-id="722ef-106">Aunque puede que esto no sea útil para todas las categorías de componentes, el establecimiento de una clase predeterminada puede ser útil cuando se debe cargar una clase determinada de una lista de clases posibles sin la intervención del usuario.</span><span class="sxs-lookup"><span data-stu-id="722ef-106">While this may not be useful for all component categories, establishing a default class can be helpful when a particular class must be loaded from a list of possible classes without user intervention.</span></span> <span data-ttu-id="722ef-107">Los administradores definen la clase que se puede usar manipulando el registro.</span><span class="sxs-lookup"><span data-stu-id="722ef-107">Administrators define which class can be used by manipulating the registry.</span></span>

<span data-ttu-id="722ef-108">Para asociar una clase predeterminada a una categoría, introduzca una clave CLSID con el mismo CLSID que el CATId de la categoría de componentes elegida como valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="722ef-108">To associate a default class with a category, introduce a CLSID key with the same CLSID as the CATID of the component category chosen as the default.</span></span> <span data-ttu-id="722ef-109">A continuación, agregue una clave treatAs a esta clave, utilizando el valor para el CLSID de la clase predeterminada de la categoría.</span><span class="sxs-lookup"><span data-stu-id="722ef-109">Then add a TreatAs key to this key, using the value for the CLSID of the default class for the category.</span></span> <span data-ttu-id="722ef-110">Para usar la clase predeterminada para una categoría de componentes, use [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) o [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), especificando el CATID para el parámetro CLSID.</span><span class="sxs-lookup"><span data-stu-id="722ef-110">To use the default class for a component category, use [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) or [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), specifying the CATID for the CLSID parameter.</span></span> <span data-ttu-id="722ef-111">Esto redirige automáticamente al CLSID establecido como valor predeterminado para esta categoría.</span><span class="sxs-lookup"><span data-stu-id="722ef-111">This automatically redirects to the CLSID established as the default for this category.</span></span> <span data-ttu-id="722ef-112">La entrada del registro es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="722ef-112">The registry entry is as follows:</span></span>

```
HKEY_CLASSES_ROOT\CLSID
   {catid}
      TreatAs
          = default clsid
```

<span data-ttu-id="722ef-113">Durante la instalación, un componente puede comprobar la existencia de cualquier clave de clase predeterminada para sus categorías y presentar al usuario opciones para invalidar la configuración actual.</span><span class="sxs-lookup"><span data-stu-id="722ef-113">During installation, a component can check for the existence of any default class keys for its categories and present the user with options for overriding the current settings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="722ef-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="722ef-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="722ef-115">Asociar iconos a una categoría</span><span class="sxs-lookup"><span data-stu-id="722ef-115">Associating Icons with a Category</span></span>](associating-icons-with-a-category.md)
</dt> <dt>

[<span data-ttu-id="722ef-116">Categorización por funcionalidad de componentes</span><span class="sxs-lookup"><span data-stu-id="722ef-116">Categorizing by Component Capabilities</span></span>](categorizing-by-component-capabilities.md)
</dt> <dt>

[<span data-ttu-id="722ef-117">Clasificar por capacidades de contenedor</span><span class="sxs-lookup"><span data-stu-id="722ef-117">Categorizing by Container Capabilities</span></span>](categorizing-by-container-capabilities.md)
</dt> <dt>

[<span data-ttu-id="722ef-118">Definir categorías de componentes</span><span class="sxs-lookup"><span data-stu-id="722ef-118">Defining Component Categories</span></span>](defining-component-categories.md)
</dt> <dt>

[<span data-ttu-id="722ef-119">Administrador de categorías de componentes</span><span class="sxs-lookup"><span data-stu-id="722ef-119">The Component Categories Manager</span></span>](the-component-categories-manager.md)
</dt> </dl>

 

 




