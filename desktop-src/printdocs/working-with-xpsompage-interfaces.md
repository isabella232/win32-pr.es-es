---
description: En este tema se describe cómo usar las interfaces de nivel de página que proporcionan acceso al contenido de una página en un OM XPS.
ms.assetid: 7127ee28-eca9-4e0e-a27a-9051eb105b27
title: Trabajar con interfaces de página de XPS OM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8350409f2f436cc4ec2293e735c3f020b49bea68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697330"
---
# <a name="working-with-xps-om-page-interfaces"></a><span data-ttu-id="d4e06-103">Trabajar con interfaces de página de XPS OM</span><span class="sxs-lookup"><span data-stu-id="d4e06-103">Working with XPS OM Page Interfaces</span></span>

<span data-ttu-id="d4e06-104">En este tema se describe cómo usar las interfaces de nivel de página que proporcionan acceso al contenido de una página en un OM XPS.</span><span class="sxs-lookup"><span data-stu-id="d4e06-104">This topic describes how to use the page-level interfaces that provide access to the contents of a page in an XPS OM.</span></span>



| <span data-ttu-id="d4e06-105">Nombre de interfaz</span><span class="sxs-lookup"><span data-stu-id="d4e06-105">Interface name</span></span>                                                                                                                                                                              | <span data-ttu-id="d4e06-106">Interfaces secundarias lógicas</span><span class="sxs-lookup"><span data-stu-id="d4e06-106">Logical child interfaces</span></span>                                                                                                                                                                                            | <span data-ttu-id="d4e06-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="d4e06-107">Description</span></span>                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d4e06-108">**IXpsOMPage**</span><span class="sxs-lookup"><span data-stu-id="d4e06-108">**IXpsOMPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)<br/>                                                                                                                                                 | [<span data-ttu-id="d4e06-109">**IXpsOMCanvas**</span><span class="sxs-lookup"><span data-stu-id="d4e06-109">**IXpsOMCanvas**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> [<span data-ttu-id="d4e06-110">**IXpsOMGlyphs**</span><span class="sxs-lookup"><span data-stu-id="d4e06-110">**IXpsOMGlyphs**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)<br/> [<span data-ttu-id="d4e06-111">**IXpsOMPath**</span><span class="sxs-lookup"><span data-stu-id="d4e06-111">**IXpsOMPath**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/>                                                                         | <span data-ttu-id="d4e06-112">Objeto raíz del contenido de la página.</span><span class="sxs-lookup"><span data-stu-id="d4e06-112">The root object of the page contents.</span></span><br/> <span data-ttu-id="d4e06-113">Este objeto representa un elemento de documento.</span><span class="sxs-lookup"><span data-stu-id="d4e06-113">This object represents a document part.</span></span><br/>                                                |
| [<span data-ttu-id="d4e06-114">**IXpsOMShareable**</span><span class="sxs-lookup"><span data-stu-id="d4e06-114">**IXpsOMShareable**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable)<br/>                                                                                                                                       | [<span data-ttu-id="d4e06-115">**IXpsOMVisual**</span><span class="sxs-lookup"><span data-stu-id="d4e06-115">**IXpsOMVisual**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)<br/> [<span data-ttu-id="d4e06-116">**IXpsOMMatrixTransform**</span><span class="sxs-lookup"><span data-stu-id="d4e06-116">**IXpsOMMatrixTransform**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform)<br/> [<span data-ttu-id="d4e06-117">**IXpsOMGeometry**</span><span class="sxs-lookup"><span data-stu-id="d4e06-117">**IXpsOMGeometry**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry)<br/> [<span data-ttu-id="d4e06-118">**IXpsOMBrush**</span><span class="sxs-lookup"><span data-stu-id="d4e06-118">**IXpsOMBrush**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush)<br/> | <span data-ttu-id="d4e06-119">Las interfaces que se derivan de la interfaz [**IXpsOMShareable**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable) se pueden almacenar en un diccionario de recursos y compartirse.</span><span class="sxs-lookup"><span data-stu-id="d4e06-119">Interfaces that derive from the [**IXpsOMShareable**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable) interface can be stored in a resource dictionary and shared.</span></span><br/> |
| [<span data-ttu-id="d4e06-120">**IXpsOMRemoteDictionaryResource**</span><span class="sxs-lookup"><span data-stu-id="d4e06-120">**IXpsOMRemoteDictionaryResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource)<br/> [<span data-ttu-id="d4e06-121">**IXpsOMRemoteDictionaryResourceCollection**</span><span class="sxs-lookup"><span data-stu-id="d4e06-121">**IXpsOMRemoteDictionaryResourceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresourcecollection)<br/> | [<span data-ttu-id="d4e06-122">**IXpsOMDictionary**</span><span class="sxs-lookup"><span data-stu-id="d4e06-122">**IXpsOMDictionary**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary)<br/>                                                                                                                                                             | <span data-ttu-id="d4e06-123">Contiene un diccionario de recursos.</span><span class="sxs-lookup"><span data-stu-id="d4e06-123">Contains a resource dictionary.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="d4e06-124">**IXpsOMDictionary**</span><span class="sxs-lookup"><span data-stu-id="d4e06-124">**IXpsOMDictionary**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary)<br/>                                                                                                                                     | <span data-ttu-id="d4e06-125">None</span><span class="sxs-lookup"><span data-stu-id="d4e06-125">None</span></span><br/>                                                                                                                                                                                                     | <span data-ttu-id="d4e06-126">Hace referencia a los recursos que comparten otros objetos.</span><span class="sxs-lookup"><span data-stu-id="d4e06-126">References the resources that are shared by other objects.</span></span><br/>                                                                              |
| [<span data-ttu-id="d4e06-127">**IXpsOMStoryFragmentsResource**</span><span class="sxs-lookup"><span data-stu-id="d4e06-127">**IXpsOMStoryFragmentsResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomstoryfragmentsresource)<br/>                                                                                                             | <span data-ttu-id="d4e06-128">None</span><span class="sxs-lookup"><span data-stu-id="d4e06-128">None</span></span><br/>                                                                                                                                                                                                     | <span data-ttu-id="d4e06-129">Proporciona acceso al contenido de la secuencia de recursos de la parte StoryFragments del documento.</span><span class="sxs-lookup"><span data-stu-id="d4e06-129">Provides access to the content of the resource stream of the StoryFragments part of the document.</span></span><br/>                                       |



 

## <a name="related-topics"></a><span data-ttu-id="d4e06-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d4e06-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4e06-131">**Interfaz IXpsOMDictionary**</span><span class="sxs-lookup"><span data-stu-id="d4e06-131">**IXpsOMDictionary Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary)
</dt> <dt>

[<span data-ttu-id="d4e06-132">**IXpsOMDocumentStructureResource**</span><span class="sxs-lookup"><span data-stu-id="d4e06-132">**IXpsOMDocumentStructureResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource)
</dt> <dt>

[<span data-ttu-id="d4e06-133">**Interfaz IXpsOMPage**</span><span class="sxs-lookup"><span data-stu-id="d4e06-133">**IXpsOMPage Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[<span data-ttu-id="d4e06-134">**Interfaz IXpsOMRemoteDictionaryResource**</span><span class="sxs-lookup"><span data-stu-id="d4e06-134">**IXpsOMRemoteDictionaryResource Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource)
</dt> <dt>

[<span data-ttu-id="d4e06-135">**Interfaz IXpsOMRemoteDictionaryResourceCollection**</span><span class="sxs-lookup"><span data-stu-id="d4e06-135">**IXpsOMRemoteDictionaryResourceCollection Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresourcecollection)
</dt> <dt>

[<span data-ttu-id="d4e06-136">**Interfaz IXpsOMStoryFragmentsResource**</span><span class="sxs-lookup"><span data-stu-id="d4e06-136">**IXpsOMStoryFragmentsResource Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomstoryfragmentsresource)
</dt> </dl>

 

 




