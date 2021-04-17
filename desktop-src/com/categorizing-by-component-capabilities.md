---
title: Categorización por funcionalidad de componentes
description: Las categorías de componentes se pueden usar para mostrar un subconjunto de todos los componentes instalados.
ms.assetid: 522af5d7-ba7b-4127-9cdb-48ef4d0f8e65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff44e03e9eae0226ac57279c37d4a5dfd32fc6bd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714143"
---
# <a name="categorizing-by-component-capabilities"></a><span data-ttu-id="fca46-103">Categorización por funcionalidad de componentes</span><span class="sxs-lookup"><span data-stu-id="fca46-103">Categorizing by Component Capabilities</span></span>

<span data-ttu-id="fca46-104">Las categorías de componentes se pueden usar para mostrar un subconjunto de todos los componentes instalados.</span><span class="sxs-lookup"><span data-stu-id="fca46-104">Component categories can be used to display a subset of all of the installed components.</span></span> <span data-ttu-id="fca46-105">Cada categoría de componente se identifica mediante un GUID, denominado ID. de categoría (CATId).</span><span class="sxs-lookup"><span data-stu-id="fca46-105">Each component category is identified by a GUID, referred to as a Category ID (CATID).</span></span> <span data-ttu-id="fca46-106">Cada CATId tiene una lista de nombres legibles etiquetados por la configuración regional asociados a él.</span><span class="sxs-lookup"><span data-stu-id="fca46-106">Each CATID has a list of locale-tagged, human-readable names associated with it.</span></span> <span data-ttu-id="fca46-107">Una lista de los CATID y los nombres legibles se almacena en una ubicación conocida en el registro.</span><span class="sxs-lookup"><span data-stu-id="fca46-107">A listing of the CATIDs and the human-readable names is stored in a well-known location in the registry.</span></span>

<span data-ttu-id="fca46-108">Por ejemplo, todos los componentes que implementan la funcionalidad para la incrustación de documentos OLE se pueden clasificar en una categoría de componente.</span><span class="sxs-lookup"><span data-stu-id="fca46-108">For example, all components that implement the functionality for OLE document embedding can be classified within a component category.</span></span> <span data-ttu-id="fca46-109">En el pasado, estos objetos se identificaban con la clave "insertable" en el registro.</span><span class="sxs-lookup"><span data-stu-id="fca46-109">In the past, these objects would have been identified by the "Insertable" key in the registry.</span></span> <span data-ttu-id="fca46-110">Para utilizar las categorías de componentes en su lugar, se agregaría la siguiente información al registro:</span><span class="sxs-lookup"><span data-stu-id="fca46-110">To use component categories instead, the following information would be added to the registry:</span></span>

```
HKEY_CLASSES_ROOT\Component Categories\{40FC6ED3-2438-11cf-A3DB-080036F12502}
   (Default) = ""
   409 = "Embeddable Objects"
```

<span data-ttu-id="fca46-111">Cada clase que implementa la funcionalidad correspondiente a una categoría de componente muestra el identificador de categoría de esa categoría dentro de la clave CLSID en el registro.</span><span class="sxs-lookup"><span data-stu-id="fca46-111">Each class that implements the functionality corresponding to a component category lists the category ID for that category within the CLSID key in the registry.</span></span> <span data-ttu-id="fca46-112">Dado que un único componente puede admitir una amplia gama de funciones, los componentes pueden pertenecer a varias categorías de componentes.</span><span class="sxs-lookup"><span data-stu-id="fca46-112">Because a single component can support a wide range of functionality, components can belong to multiple component categories.</span></span> <span data-ttu-id="fca46-113">Por ejemplo, un control OLE determinado podría admitir toda la funcionalidad necesaria para participar como la incrustación de documentos OLE, el enlace de datos de Microsoft Visual Basic y la funcionalidad de Internet.</span><span class="sxs-lookup"><span data-stu-id="fca46-113">For example, a particular OLE control might support all of the functionality required to participate as OLE document embedding, Microsoft Visual Basic data binding, and Internet functionality.</span></span> <span data-ttu-id="fca46-114">Este tipo de control tendría la siguiente información almacenada en su clave CLSID en el registro:</span><span class="sxs-lookup"><span data-stu-id="fca46-114">Such a control would have the following information stored in its CLSID key in the registry:</span></span>

``` syntax
;The CLSID for "My Super OLE Control" is {12345678-ABCD-4321-0101-00000000000C}HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}\Implemented Categories
;The CATID for "Insertable" is {40FC6ED3-2438-11cf-A3DB-080036F12502} HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}Implemented Categories\{40FC6ED3-2438-11cf-A3DB-080036F12502}
;The CATID for "Control" is {40FC6ED4-2438-11cf-A3DB-080036F12502} HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}Implemented Categories\{40FC6ED4-2438-11cf-A3DB-080036F12502}
;The CATID for an internet aware control is {...CATID_InternetAware...} HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}Implemented Categories\{...CATID_InternetAware...}
 
```

<span data-ttu-id="fca46-115">Con esta información, un contenedor puede enumerar los controles instalados en un sistema y mostrar solo los controles que admiten la funcionalidad requerida por el contenedor.</span><span class="sxs-lookup"><span data-stu-id="fca46-115">With this information, a container can enumerate the controls installed on a system and display only those controls that support the functionality required by the container.</span></span> <span data-ttu-id="fca46-116">El uso de categorías de componentes proporciona una manera de clasificar los componentes por la funcionalidad implementada del componente.</span><span class="sxs-lookup"><span data-stu-id="fca46-116">The use of component categories provides a way to categorize components by the implemented functionality of the component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fca46-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fca46-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fca46-118">Asociar iconos a una categoría</span><span class="sxs-lookup"><span data-stu-id="fca46-118">Associating Icons with a Category</span></span>](associating-icons-with-a-category.md)
</dt> <dt>

[<span data-ttu-id="fca46-119">Clasificar por capacidades de contenedor</span><span class="sxs-lookup"><span data-stu-id="fca46-119">Categorizing by Container Capabilities</span></span>](categorizing-by-container-capabilities.md)
</dt> <dt>

[<span data-ttu-id="fca46-120">Clases y asociaciones predeterminadas</span><span class="sxs-lookup"><span data-stu-id="fca46-120">Default Classes and Associations</span></span>](default-classes-and-associations.md)
</dt> <dt>

[<span data-ttu-id="fca46-121">Definir categorías de componentes</span><span class="sxs-lookup"><span data-stu-id="fca46-121">Defining Component Categories</span></span>](defining-component-categories.md)
</dt> <dt>

[<span data-ttu-id="fca46-122">Administrador de categorías de componentes</span><span class="sxs-lookup"><span data-stu-id="fca46-122">The Component Categories Manager</span></span>](the-component-categories-manager.md)
</dt> </dl>

 

 




