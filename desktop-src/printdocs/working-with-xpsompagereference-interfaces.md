---
description: En este tema se describe cómo usar las interfaces que proporcionan acceso a las referencias de página en un OM XPS.
ms.assetid: bb227536-3b29-4221-b2d5-bab5e9d91448
title: Trabajar con interfaces IXpsOMPageReference
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f4526e6c561a962b77fa3f2fc62d56431359aa6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910482"
---
# <a name="working-with-ixpsompagereference-interfaces"></a><span data-ttu-id="b3650-103">Trabajar con interfaces IXpsOMPageReference</span><span class="sxs-lookup"><span data-stu-id="b3650-103">Working with IXpsOMPageReference Interfaces</span></span>

<span data-ttu-id="b3650-104">En este tema se describe cómo usar las interfaces que proporcionan acceso a las referencias de página en un OM XPS.</span><span class="sxs-lookup"><span data-stu-id="b3650-104">This topic describes how to use the interfaces that provide access to page references in an XPS OM.</span></span>



| <span data-ttu-id="b3650-105">Nombre de interfaz</span><span class="sxs-lookup"><span data-stu-id="b3650-105">Interface name</span></span>                                                  | <span data-ttu-id="b3650-106">Interfaces secundarias lógicas</span><span class="sxs-lookup"><span data-stu-id="b3650-106">Logical child interfaces</span></span>                    | <span data-ttu-id="b3650-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="b3650-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b3650-108">**IXpsOMPageReference**</span><span class="sxs-lookup"><span data-stu-id="b3650-108">**IXpsOMPageReference**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/>   | [<span data-ttu-id="b3650-109">**IXpsOMPage**</span><span class="sxs-lookup"><span data-stu-id="b3650-109">**IXpsOMPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)<br/> | <span data-ttu-id="b3650-110">Virtualiza el contenido de una página de documento.</span><span class="sxs-lookup"><span data-stu-id="b3650-110">Virtualizes the content of a document page.</span></span> <br/> <span data-ttu-id="b3650-111">Una referencia de página contiene información básica acerca de la página, algunas propiedades de la página y un vínculo al contenido de la página.</span><span class="sxs-lookup"><span data-stu-id="b3650-111">A page reference contains basic information about the page, some page properties, and a link to the page contents.</span></span> <span data-ttu-id="b3650-112">El método [**IXpsOMPageReference:: GetPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getpage) devuelve la interfaz [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) que comprende el contenido de la página.</span><span class="sxs-lookup"><span data-stu-id="b3650-112">The [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) interface that comprises page contents is returned by the [**IXpsOMPageReference::GetPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getpage) method.</span></span><br/> |
| [<span data-ttu-id="b3650-113">**IXpsOMNameCollection**</span><span class="sxs-lookup"><span data-stu-id="b3650-113">**IXpsOMNameCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)<br/> | <span data-ttu-id="b3650-114">None</span><span class="sxs-lookup"><span data-stu-id="b3650-114">None</span></span><br/>                             | <span data-ttu-id="b3650-115">Contiene una lista de elementos de página que son destinos de hipervínculo.</span><span class="sxs-lookup"><span data-stu-id="b3650-115">Contains a list of page items that are hyperlink targets.</span></span> <span data-ttu-id="b3650-116">El método [**IXpsOMPageReference:: CollectLinkTargets**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectlinktargets) devuelve la lista.</span><span class="sxs-lookup"><span data-stu-id="b3650-116">The list is returned by the [**IXpsOMPageReference::CollectLinkTargets**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectlinktargets) method.</span></span><br/>                                                                                                                                                               |
| [<span data-ttu-id="b3650-117">**IXpsOMPartResources**</span><span class="sxs-lookup"><span data-stu-id="b3650-117">**IXpsOMPartResources**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources)<br/>   | <span data-ttu-id="b3650-118">None</span><span class="sxs-lookup"><span data-stu-id="b3650-118">None</span></span><br/>                             | <span data-ttu-id="b3650-119">Contiene una lista de los recursos basados en elementos que están asociados a la página.</span><span class="sxs-lookup"><span data-stu-id="b3650-119">Contains a list of the part-based resources that are associated with the page.</span></span> <span data-ttu-id="b3650-120">El método [**IXpsOMPageReference:: CollectPartResources**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectpartresources) devuelve esta lista.</span><span class="sxs-lookup"><span data-stu-id="b3650-120">This list is returned by the [**IXpsOMPageReference::CollectPartResources**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectpartresources) method.</span></span><br/>                                                                                                                                     |



 

## <a name="code-examples"></a><span data-ttu-id="b3650-121">Ejemplos de código</span><span class="sxs-lookup"><span data-stu-id="b3650-121">Code Examples</span></span>

<span data-ttu-id="b3650-122">En los siguientes ejemplos de código se muestra cómo trabajar con las interfaces de referencia de página en un programa.</span><span class="sxs-lookup"><span data-stu-id="b3650-122">The following code examples illustrate how to work with the page reference interfaces in a program.</span></span>

-   [<span data-ttu-id="b3650-123">Obtener el contenido de la página</span><span class="sxs-lookup"><span data-stu-id="b3650-123">Get the page contents</span></span>](#get-the-page-contents)
-   [<span data-ttu-id="b3650-124">Obtiene la lista de destinos de hipervínculo en esta página.</span><span class="sxs-lookup"><span data-stu-id="b3650-124">Get the list of hyperlink targets on this page</span></span>](#get-the-list-of-hyperlink-targets-on-this-page)
-   [<span data-ttu-id="b3650-125">Obtener los recursos del elemento que están asociados a esta página</span><span class="sxs-lookup"><span data-stu-id="b3650-125">Get the part resources that are associated with this page</span></span>](#get-the-part-resources-that-are-associated-with-this-page)

### <a name="get-the-page-contents"></a><span data-ttu-id="b3650-126">Obtener el contenido de la página</span><span class="sxs-lookup"><span data-stu-id="b3650-126">Get the page contents</span></span>

<span data-ttu-id="b3650-127">En el ejemplo de código siguiente se obtiene un puntero a la interfaz [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) que comprende el contenido de la página.</span><span class="sxs-lookup"><span data-stu-id="b3650-127">The following code example gets a pointer to the [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) interface that comprises the page contents.</span></span> <span data-ttu-id="b3650-128">Si la página no se ha cargado en el OM de XPS, como sucede cuando el OM de XPS se inicializa llamando a [**IXpsOMObjectFactory:: CreatePackageFromFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromfile), al llamar a [**IXpsOMPageReference:: GetPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getpage) se cargará la página en el OM XPS.</span><span class="sxs-lookup"><span data-stu-id="b3650-128">If the page has not been loaded into the XPS OM, as happens when the XPS OM is initialized by calling [**IXpsOMObjectFactory::CreatePackageFromFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromfile), calling [**IXpsOMPageReference::GetPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getpage) will load the page into the XPS OM.</span></span>


```C++
    {
    HRESULT        hr = S_OK;
    IXpsOMPage     *page = NULL;

    // pageRef contains the current page reference
    // and is passed in as a parameter

    // get the page content of this page reference
    hr = pageRef->GetPage (&page);
```



### <a name="get-the-list-of-hyperlink-targets-on-this-page"></a><span data-ttu-id="b3650-129">Obtiene la lista de destinos de hipervínculo en esta página.</span><span class="sxs-lookup"><span data-stu-id="b3650-129">Get the list of hyperlink targets on this page</span></span>

<span data-ttu-id="b3650-130">En el ejemplo de código siguiente se obtiene un puntero a la interfaz [**IXpsOMNameCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection) que contiene la lista de elementos de página que son destinos de hipervínculo.</span><span class="sxs-lookup"><span data-stu-id="b3650-130">The following code example gets a pointer to the [**IXpsOMNameCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection) interface that contains the list of page items that are hyperlink targets.</span></span> <span data-ttu-id="b3650-131">Si la página no se ha cargado en el OM XPS, la lista de destinos de hipervínculo se lee desde el marcado **PageContent. LinkTargets** .</span><span class="sxs-lookup"><span data-stu-id="b3650-131">If the page has not been loaded into the XPS OM, the list of hyperlink targets is read from the **PageContent.LinkTargets** markup.</span></span> <span data-ttu-id="b3650-132">Si se carga la página, [**CollectLinkTargets**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectlinktargets) comprueba cada elemento de la página y devuelve una lista de elementos cuyo atributo **IsHyperlinkTarget** es **true**.</span><span class="sxs-lookup"><span data-stu-id="b3650-132">If the page has been loaded, [**CollectLinkTargets**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectlinktargets) checks each element in the page and returns a list of elements whose **IsHyperlinkTarget** attribute is **TRUE**.</span></span>


```C++
    HRESULT                         hr = S_OK;
    IXpsOMPage                      *page = NULL;
    IXpsOMNameCollection            *linkTargets = NULL;

    UINT32 numTargets = 0;
    UINT32 thisTarget = 0;
    LPWSTR thisTargetName = NULL;

    // pageRef contains the current page reference 

    // if the page hasn't been loaded yet, for example, if the XPS OM 
    //  was loaded from an XPS document, CollectLinkTargets obtains the
    //  list of link targets from the <PageContent.LinkTargets> markup
    hr = pageRef->CollectLinkTargets(&linkTargets);

    // get the page content of this page reference
    hr = pageRef->GetPage (&page);

    // after the page object has been loaded and calling GetPage or 
    //  by creating a page in the XPS OM, CollectLinkTargets will now check
    //  each of the page elements to return the list so this call to
    //  CollectLinkTargets might take longer to return than the previous
    //  call above if the XPS OM was created from a file
    linkTargets->Release(); // release previous collection
    hr = pageRef->CollectLinkTargets(&linkTargets);
    
    // walk the list of link targets returned
    hr = linkTargets->GetCount( &numTargets );
    thisTarget = 0;
    while (thisTarget < numTargets) {
        hr = linkTargets->GetAt (thisTarget, &thisTargetName);
        printf ("%s\n", thisTargetName);
        // release the target string returned to prevent memory leaks
        CoTaskMemFree (thisTargetName);
        // get next target in list
        thisTarget++;
    }
    // release page and the link target collection
    page->Release();
    linkTargets->Release();
```



### <a name="get-the-part-resources-that-are-associated-with-this-page"></a><span data-ttu-id="b3650-133">Obtener los recursos del elemento que están asociados a esta página</span><span class="sxs-lookup"><span data-stu-id="b3650-133">Get the part resources that are associated with this page</span></span>

<span data-ttu-id="b3650-134">En el ejemplo de código siguiente se obtienen las listas de los distintos recursos utilizados por esta página.</span><span class="sxs-lookup"><span data-stu-id="b3650-134">The following code example gets the lists of the different resources that are used by this page.</span></span>


```C++
    HRESULT                                   hr = S_OK;
    IXpsOMPartResources                       *resources;

    IXpsOMColorProfileResourceCollection      *colorProfileResources;
    IXpsOMFontResourceCollection              *fontResources;
    IXpsOMImageResourceCollection             *imageResources;
    IXpsOMRemoteDictionaryResourceCollection  *dictionaryResources; 

    // pageRef contains the current page reference 
    hr = pageRef->CollectPartResources ( &resources );

    // Get pointers to each type of resource
    hr = resources->GetColorProfileResources( &colorProfileResources );
    hr = resources->GetFontResources( &fontResources );
    hr = resources->GetImageResources( &imageResources );
    hr = resources->GetRemoteDictionaryResources( &dictionaryResources );
```



## <a name="related-topics"></a><span data-ttu-id="b3650-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b3650-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3650-136">**IXpsOMNameCollection**</span><span class="sxs-lookup"><span data-stu-id="b3650-136">**IXpsOMNameCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)
</dt> <dt>

[<span data-ttu-id="b3650-137">**IXpsOMPage**</span><span class="sxs-lookup"><span data-stu-id="b3650-137">**IXpsOMPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[<span data-ttu-id="b3650-138">**IXpsOMPageReference**</span><span class="sxs-lookup"><span data-stu-id="b3650-138">**IXpsOMPageReference**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)
</dt> <dt>

[<span data-ttu-id="b3650-139">**IXpsOMPartResources**</span><span class="sxs-lookup"><span data-stu-id="b3650-139">**IXpsOMPartResources**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources)
</dt> <dt>

[<span data-ttu-id="b3650-140">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="b3650-140">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 




