---
title: Administrador de categorías de componentes
description: Administrador de categorías de componentes
ms.assetid: bd43ef98-2299-4c8a-9f35-bf9aceb074ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fdf301e1b344bbc2403fd656dd90447ccffc357
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486771"
---
# <a name="the-component-categories-manager"></a><span data-ttu-id="8ff4a-103">Administrador de categorías de componentes</span><span class="sxs-lookup"><span data-stu-id="8ff4a-103">The Component Categories Manager</span></span>

<span data-ttu-id="8ff4a-104">Para facilitar el control de las categorías de componentes y garantizar la coherencia del registro, el sistema proporciona el administrador de categorías de componentes, un objeto COM con un CLSID de CLSID \_ StdComponentCategoriesMgr.</span><span class="sxs-lookup"><span data-stu-id="8ff4a-104">To facilitate the handling of component categories and to guarantee consistency of the registry, the system provides the Component Categories Manager, a COM object with a CLSID of CLSID\_StdComponentCategoriesMgr.</span></span> <span data-ttu-id="8ff4a-105">Este objeto COM proporciona las siguientes interfaces:</span><span class="sxs-lookup"><span data-stu-id="8ff4a-105">This COM object provides the following interfaces:</span></span>

-   [<span data-ttu-id="8ff4a-106">**ICatInformation**</span><span class="sxs-lookup"><span data-stu-id="8ff4a-106">**ICatInformation**</span></span>](/windows/desktop/api/ComCat/nn-comcat-icatinformation)
-   [<span data-ttu-id="8ff4a-107">**ICatRegister**</span><span class="sxs-lookup"><span data-stu-id="8ff4a-107">**ICatRegister**</span></span>](/windows/desktop/api/ComCat/nn-comcat-icatregister)

<span data-ttu-id="8ff4a-108">[**ICatInformation**](/windows/desktop/api/ComCat/nn-comcat-icatinformation) proporciona métodos para obtener información sobre las categorías implementadas o que requiere una determinada clase y proporciona información acerca de las categorías registradas en un equipo determinado.</span><span class="sxs-lookup"><span data-stu-id="8ff4a-108">[**ICatInformation**](/windows/desktop/api/ComCat/nn-comcat-icatinformation) provides methods for obtaining information about the categories implemented or required by a certain class and provides information about the categories registered on a given machine.</span></span>

<span data-ttu-id="8ff4a-109">[**ICatRegister**](/windows/desktop/api/ComCat/nn-comcat-icatregister) proporciona métodos para registrar y anular el registro de la información de categorías de componentes en el registro.</span><span class="sxs-lookup"><span data-stu-id="8ff4a-109">[**ICatRegister**](/windows/desktop/api/ComCat/nn-comcat-icatregister) provides methods for registering and unregistering component category information in the registry.</span></span> <span data-ttu-id="8ff4a-110">Esto incluye los nombres legibles de las categorías y las categorías implementadas o requeridas por un componente o clase determinados.</span><span class="sxs-lookup"><span data-stu-id="8ff4a-110">This includes both the human-readable names of categories and the categories implemented or required by a given component or class.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8ff4a-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8ff4a-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ff4a-112">Asociar iconos a una categoría</span><span class="sxs-lookup"><span data-stu-id="8ff4a-112">Associating Icons with a Category</span></span>](associating-icons-with-a-category.md)
</dt> <dt>

[<span data-ttu-id="8ff4a-113">Categorización por funcionalidad de componentes</span><span class="sxs-lookup"><span data-stu-id="8ff4a-113">Categorizing by Component Capabilities</span></span>](categorizing-by-component-capabilities.md)
</dt> <dt>

[<span data-ttu-id="8ff4a-114">Clasificar por capacidades de contenedor</span><span class="sxs-lookup"><span data-stu-id="8ff4a-114">Categorizing by Container Capabilities</span></span>](categorizing-by-container-capabilities.md)
</dt> <dt>

[<span data-ttu-id="8ff4a-115">Clases y asociaciones predeterminadas</span><span class="sxs-lookup"><span data-stu-id="8ff4a-115">Default Classes and Associations</span></span>](default-classes-and-associations.md)
</dt> <dt>

[<span data-ttu-id="8ff4a-116">Definir categorías de componentes</span><span class="sxs-lookup"><span data-stu-id="8ff4a-116">Defining Component Categories</span></span>](defining-component-categories.md)
</dt> </dl>

 

 




