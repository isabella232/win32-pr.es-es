---
description: Implementar extensiones de hoja de propiedades
ms.assetid: 5d1f9d91-e8a1-4cbb-b1de-4262a61e3cb7
title: Implementar extensiones de hoja de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2a351678c2377aacdd73ec750841a32a81ad973
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717145"
---
# <a name="implementing-property-sheet-extensions"></a><span data-ttu-id="fa015-103">Implementar extensiones de hoja de propiedades</span><span class="sxs-lookup"><span data-stu-id="fa015-103">Implementing Property Sheet Extensions</span></span>

<span data-ttu-id="fa015-104">La extensión de espacio de nombres de WPD admite hojas de propiedades extensibles.</span><span class="sxs-lookup"><span data-stu-id="fa015-104">The WPD Namespace Extension supports extensible property sheets.</span></span> <span data-ttu-id="fa015-105">Estos son los cuadros de diálogo de propiedades que aparecen cuando un usuario hace clic con el botón secundario en un objeto, como un archivo o una carpeta, y selecciona **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="fa015-105">These are the property dialogs that appear when a user right-clicks on an object, such as a file or a folder, and selects **Properties**.</span></span> <span data-ttu-id="fa015-106">Algunas aplicaciones de WPD aprovecharán estas hojas de propiedades extensibles para mostrar las propiedades del contenido del dispositivo (o los objetos que residen en el dispositivo).</span><span class="sxs-lookup"><span data-stu-id="fa015-106">Some WPD applications will take advantage of these extensible property sheets to display properties for device-side content (or objects that reside on the device).</span></span>

<span data-ttu-id="fa015-107">Las interfaces que se describen en la tabla siguiente admiten hojas de propiedades extensibles.</span><span class="sxs-lookup"><span data-stu-id="fa015-107">Extensible property sheets are supported by the interfaces described in the following table.</span></span> <span data-ttu-id="fa015-108">Para obtener más información sobre cualquiera de estas interfaces, vea el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="fa015-108">For more information about any of these interfaces, see the Windows SDK.</span></span>



| <span data-ttu-id="fa015-109">Interfaz</span><span class="sxs-lookup"><span data-stu-id="fa015-109">Interface</span></span>           | <span data-ttu-id="fa015-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="fa015-110">Description</span></span>                                                                  |
|---------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="fa015-111">IDataObject</span><span class="sxs-lookup"><span data-stu-id="fa015-111">IDataObject</span></span>         | <span data-ttu-id="fa015-112">Se usa para pasar la matriz PIDL del menú contextual al controlador del menú contextual.</span><span class="sxs-lookup"><span data-stu-id="fa015-112">Used to pass the context menu's PIDL array to the context menu handler.</span></span>      |
| <span data-ttu-id="fa015-113">IPropertySetStorage</span><span class="sxs-lookup"><span data-stu-id="fa015-113">IPropertySetStorage</span></span> | <span data-ttu-id="fa015-114">Esta interfaz se utiliza para recuperar las propiedades de WPD para el objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="fa015-114">This interface is used to retrieve WPD properties for the given object.</span></span>      |
| <span data-ttu-id="fa015-115">IPropertyStorage</span><span class="sxs-lookup"><span data-stu-id="fa015-115">IPropertyStorage</span></span>    | <span data-ttu-id="fa015-116">Esta interfaz también se utiliza para recuperar las propiedades de WPD para el objeto dado.</span><span class="sxs-lookup"><span data-stu-id="fa015-116">This interface is also used to retrieve WPD properties for the given object.</span></span> |
| <span data-ttu-id="fa015-117">IShellExtInit</span><span class="sxs-lookup"><span data-stu-id="fa015-117">IShellExtInit</span></span>       | <span data-ttu-id="fa015-118">Inicializa las extensiones de Shell de Windows Vista para el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="fa015-118">Initializes the Windows Vista Shell extensions for the context menu.</span></span>         |
| <span data-ttu-id="fa015-119">IShellPropSheetExt</span><span class="sxs-lookup"><span data-stu-id="fa015-119">IShellPropSheetExt</span></span>  | <span data-ttu-id="fa015-120">Admite la adición de extensiones de la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="fa015-120">Supports addition of property sheet extensions.</span></span>                              |



 

<span data-ttu-id="fa015-121">Las hojas de propiedades de WPD se implementan como cualquier otra hoja de propiedades de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fa015-121">Property sheets for WPD are implemented like any other property sheet in Windows Vista.</span></span> <span data-ttu-id="fa015-122">Si ya ha implementado un controlador de la hoja de propiedades, puede modificar el código existente para que sea compatible con el contenido del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fa015-122">If you've already implemented a property sheet handler, you can modify your existing code so that it supports device-side content.</span></span> <span data-ttu-id="fa015-123">Si nunca ha creado un controlador de menú contextual, consulte el tema crear controladores de hoja de propiedades en el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="fa015-123">If you've never created a context menu handler, see the Creating Property Sheet Handlers topic in the Windows SDK.</span></span>

<span data-ttu-id="fa015-124">Los dos puntos en los que un controlador de la hoja de propiedades de WPD difiere de cualquier otro controlador se encuentran en el registro del controlador y en la compatibilidad del contenido del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fa015-124">The two points at which a WPD property sheet handler differs from any other handler is in the handler registration and the support of device-side content.</span></span>

 

 



