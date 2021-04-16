---
description: Implementar extensiones de menú contextual
ms.assetid: b8bea667-b9ea-476d-942f-281cb2e9636c
title: Implementar extensiones de menú contextual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c65918f385984355490456cccb626ba297bd3368
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716065"
---
# <a name="implementing-context-menu-extensions"></a><span data-ttu-id="95056-103">Implementar extensiones de menú contextual</span><span class="sxs-lookup"><span data-stu-id="95056-103">Implementing Context Menu Extensions</span></span>

<span data-ttu-id="95056-104">La extensión de espacio de nombres de WPD admite menús de contexto extensible (o acceso directo).</span><span class="sxs-lookup"><span data-stu-id="95056-104">The WPD Namespace Extension supports extensible context (or shortcut) menus.</span></span> <span data-ttu-id="95056-105">Estos son los menús que aparecen cuando un usuario hace clic con el botón secundario en un objeto, como un archivo o una carpeta.</span><span class="sxs-lookup"><span data-stu-id="95056-105">These are the menus that appear when a user right-clicks on an object such as a file or a folder.</span></span> <span data-ttu-id="95056-106">Algunas aplicaciones de WPD aprovecharán estos menús extensibles para admitir operaciones en el contenido del dispositivo (o los objetos que residen en el dispositivo).</span><span class="sxs-lookup"><span data-stu-id="95056-106">Some WPD applications will take advantage of these extensible menus to support operations on device-side content (or objects that reside on the device).</span></span>

<span data-ttu-id="95056-107">Los menús contextuales extensibles son compatibles con las interfaces descritas en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="95056-107">Extensible context menus are supported by the interfaces described in the following table.</span></span> <span data-ttu-id="95056-108">Para obtener más información sobre cualquiera de estas interfaces, vea el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="95056-108">For more information about any of these interfaces, see the Windows SDK.</span></span>



| <span data-ttu-id="95056-109">Interfaz</span><span class="sxs-lookup"><span data-stu-id="95056-109">Interface</span></span>           | <span data-ttu-id="95056-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="95056-110">Description</span></span>                                                                                                                |
|---------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95056-111">IContextMenu</span><span class="sxs-lookup"><span data-stu-id="95056-111">IContextMenu</span></span>        | <span data-ttu-id="95056-112">El shell de Windows Vista llama a los métodos de esta interfaz para crear o combinar el nuevo menú contextual con el objeto dado.</span><span class="sxs-lookup"><span data-stu-id="95056-112">The Windows Vista Shell calls the methods in this interface to create or merge the new context menu with the given object.</span></span> |
| <span data-ttu-id="95056-113">IDataObject</span><span class="sxs-lookup"><span data-stu-id="95056-113">IDataObject</span></span>         | <span data-ttu-id="95056-114">Se usa para pasar la matriz PIDL del menú contextual al controlador del menú contextual.</span><span class="sxs-lookup"><span data-stu-id="95056-114">Used to pass the context menu's PIDL array to the context menu handler.</span></span>                                                    |
| <span data-ttu-id="95056-115">IPropertySetStorage</span><span class="sxs-lookup"><span data-stu-id="95056-115">IPropertySetStorage</span></span> | <span data-ttu-id="95056-116">Esta interfaz se utiliza para recuperar las propiedades de WPD para el objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="95056-116">This interface is used to retrieve WPD properties for the given object.</span></span>                                                    |
| <span data-ttu-id="95056-117">IPropertyStorage</span><span class="sxs-lookup"><span data-stu-id="95056-117">IPropertyStorage</span></span>    | <span data-ttu-id="95056-118">Esta interfaz también se utiliza para recuperar las propiedades de WPD para el objeto dado.</span><span class="sxs-lookup"><span data-stu-id="95056-118">This interface is also used to retrieve WPD properties for the given object.</span></span>                                               |
| <span data-ttu-id="95056-119">IShellExtInit</span><span class="sxs-lookup"><span data-stu-id="95056-119">IShellExtInit</span></span>       | <span data-ttu-id="95056-120">Inicializa las extensiones de Shell de Windows Vista para el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="95056-120">Initializes the Windows Vista Shell extensions for the context menu.</span></span>                                                       |
| <span data-ttu-id="95056-121">IStream</span><span class="sxs-lookup"><span data-stu-id="95056-121">IStream</span></span>             | <span data-ttu-id="95056-122">Que se va a proporcionar.</span><span class="sxs-lookup"><span data-stu-id="95056-122">To be supplied.</span></span>                                                                                                            |



 

<span data-ttu-id="95056-123">Los menús contextuales de WPD se implementan como cualquier otro menú contextual en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="95056-123">Context menus for WPD are implemented like any other context menu in Windows Vista.</span></span> <span data-ttu-id="95056-124">Si ya ha implementado un controlador de menú contextual, puede modificar el código existente para que sea compatible con el contenido del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="95056-124">If you've already implemented a context menu handler, you can modify your existing code so that it supports device-side content.</span></span> <span data-ttu-id="95056-125">Si nunca ha creado un controlador de menú contextual, consulte el tema creación de controladores de menú contextual en el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="95056-125">If you have never created a context menu handler, see the Creating Context Menu Handlers topic in the Windows SDK.</span></span>

<span data-ttu-id="95056-126">Los dos puntos en los que un controlador de menú contextual de WPD difiere de cualquier otro controlador se encuentran en el registro del controlador y en la compatibilidad del contenido del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="95056-126">The two points at which a WPD context menu handler differs from any other handler is in the handler registration and the support of device-side content.</span></span>

 

 



