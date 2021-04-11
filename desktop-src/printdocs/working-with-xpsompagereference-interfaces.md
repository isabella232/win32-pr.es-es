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
# <a name="working-with-ixpsompagereference-interfaces"></a>Trabajar con interfaces IXpsOMPageReference

En este tema se describe cómo usar las interfaces que proporcionan acceso a las referencias de página en un OM XPS.



| Nombre de interfaz                                                  | Interfaces secundarias lógicas                    | Descripción                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/>   | [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)<br/> | Virtualiza el contenido de una página de documento. <br/> Una referencia de página contiene información básica acerca de la página, algunas propiedades de la página y un vínculo al contenido de la página. El método [**IXpsOMPageReference:: GetPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getpage) devuelve la interfaz [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) que comprende el contenido de la página.<br/> |
| [**IXpsOMNameCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)<br/> | None<br/>                             | Contiene una lista de elementos de página que son destinos de hipervínculo. El método [**IXpsOMPageReference:: CollectLinkTargets**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectlinktargets) devuelve la lista.<br/>                                                                                                                                                               |
| [**IXpsOMPartResources**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources)<br/>   | None<br/>                             | Contiene una lista de los recursos basados en elementos que están asociados a la página. El método [**IXpsOMPageReference:: CollectPartResources**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectpartresources) devuelve esta lista.<br/>                                                                                                                                     |



 

## <a name="code-examples"></a>Ejemplos de código

En los siguientes ejemplos de código se muestra cómo trabajar con las interfaces de referencia de página en un programa.

-   [Obtener el contenido de la página](#get-the-page-contents)
-   [Obtiene la lista de destinos de hipervínculo en esta página.](#get-the-list-of-hyperlink-targets-on-this-page)
-   [Obtener los recursos del elemento que están asociados a esta página](#get-the-part-resources-that-are-associated-with-this-page)

### <a name="get-the-page-contents"></a>Obtener el contenido de la página

En el ejemplo de código siguiente se obtiene un puntero a la interfaz [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) que comprende el contenido de la página. Si la página no se ha cargado en el OM de XPS, como sucede cuando el OM de XPS se inicializa llamando a [**IXpsOMObjectFactory:: CreatePackageFromFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromfile), al llamar a [**IXpsOMPageReference:: GetPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getpage) se cargará la página en el OM XPS.


```C++
    {
    HRESULT        hr = S_OK;
    IXpsOMPage     *page = NULL;

    // pageRef contains the current page reference
    // and is passed in as a parameter

    // get the page content of this page reference
    hr = pageRef->GetPage (&page);
```



### <a name="get-the-list-of-hyperlink-targets-on-this-page"></a>Obtiene la lista de destinos de hipervínculo en esta página.

En el ejemplo de código siguiente se obtiene un puntero a la interfaz [**IXpsOMNameCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection) que contiene la lista de elementos de página que son destinos de hipervínculo. Si la página no se ha cargado en el OM XPS, la lista de destinos de hipervínculo se lee desde el marcado **PageContent. LinkTargets** . Si se carga la página, [**CollectLinkTargets**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectlinktargets) comprueba cada elemento de la página y devuelve una lista de elementos cuyo atributo **IsHyperlinkTarget** es **true**.


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



### <a name="get-the-part-resources-that-are-associated-with-this-page"></a>Obtener los recursos del elemento que están asociados a esta página

En el ejemplo de código siguiente se obtienen las listas de los distintos recursos utilizados por esta página.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IXpsOMNameCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)
</dt> <dt>

[**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)
</dt> <dt>

[**IXpsOMPartResources**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 




