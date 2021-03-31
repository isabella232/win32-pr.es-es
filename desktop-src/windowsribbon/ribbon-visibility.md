---
title: Mostrar la cinta de opciones
description: El marco de la cinta de opciones de Windows expone un conjunto de propiedades que permiten a una aplicación especificar cómo se muestra la interfaz de usuario de la cinta en tiempo de ejecución.
ms.assetid: c6716183-ef32-4fb2-812a-2d8f27448db5
keywords:
- Cinta de Windows, personalizar colores
- Cinta, personalizar colores
- personalizar los colores de la cinta de opciones de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 090c77c5b47afd673bc7132a87e3de336683d876
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078044"
---
# <a name="displaying-the-ribbon"></a><span data-ttu-id="b9810-106">Mostrar la cinta de opciones</span><span class="sxs-lookup"><span data-stu-id="b9810-106">Displaying the Ribbon</span></span>

<span data-ttu-id="b9810-107">El marco de la cinta de opciones de Windows expone un conjunto de propiedades que permiten a una aplicación especificar cómo se muestra la interfaz de usuario de la cinta en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="b9810-107">The Windows Ribbon framework exposes a set of properties that allow an application to specify how the Ribbon UI is displayed at run time.</span></span>

-   [<span data-ttu-id="b9810-108">Introducción</span><span class="sxs-lookup"><span data-stu-id="b9810-108">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="b9810-109">Minimizar la cinta de opciones</span><span class="sxs-lookup"><span data-stu-id="b9810-109">Minimize the Ribbon</span></span>](#minimize-the-ribbon)
-   [<span data-ttu-id="b9810-110">Ocultar la cinta de opciones</span><span class="sxs-lookup"><span data-stu-id="b9810-110">Hide the Ribbon</span></span>](#hide-the-ribbon)
-   [<span data-ttu-id="b9810-111">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b9810-111">Example</span></span>](#example)
-   [<span data-ttu-id="b9810-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b9810-112">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="b9810-113">Introducción</span><span class="sxs-lookup"><span data-stu-id="b9810-113">Introduction</span></span>

<span data-ttu-id="b9810-114">Para maximizar el área disponible para el espacio del documento (o el puerto de vista) de una aplicación de marco de cinta, una aplicación puede especificar si la interfaz de usuario de la cinta de opciones está visible u oculta y, cuando está visible, si la cinta de opciones se encuentra en un estado expandido o contraído.</span><span class="sxs-lookup"><span data-stu-id="b9810-114">To maximize the area available for the document space (or view port) of a Ribbon framework application, an application can specify whether the ribbon UI is visible or hidden and, when visible, whether the ribbon is in an expanded or collapsed state.</span></span>

<span data-ttu-id="b9810-115">Las [claves de propiedad de marco](windowsribbon-reference-properties-framework.md) enumeradas en la tabla siguiente se usan para establecer explícitamente las características de presentación de la interfaz de usuario de la cinta en una aplicación de marco de cinta.</span><span class="sxs-lookup"><span data-stu-id="b9810-115">The [framework property keys](windowsribbon-reference-properties-framework.md) listed in the following table are used to explicitly set the display characteristics of the ribbon UI in a Ribbon framework application.</span></span> <span data-ttu-id="b9810-116">Estas propiedades no tienen ningún efecto en la presentación del control [emergente de contexto](windowsribbon-controls-contextpopup.md) .</span><span class="sxs-lookup"><span data-stu-id="b9810-116">These properties have no effect on the display of the [Context Popup](windowsribbon-controls-contextpopup.md) control.</span></span>



| <span data-ttu-id="b9810-117">Estado de presentación</span><span class="sxs-lookup"><span data-stu-id="b9810-117">Display State</span></span>         | <span data-ttu-id="b9810-118">Tecla de propiedad de la cinta</span><span class="sxs-lookup"><span data-stu-id="b9810-118">Ribbon Property Key</span></span>                                                            |
|-----------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="b9810-119">Expandido o contraído</span><span class="sxs-lookup"><span data-stu-id="b9810-119">Expanded or collapsed</span></span> | [<span data-ttu-id="b9810-120">PKEY de IU \_ \_ minimizada</span><span class="sxs-lookup"><span data-stu-id="b9810-120">UI\_PKEY\_Minimized</span></span>](windowsribbon-reference-properties-uipkey-minimized.md) |
| <span data-ttu-id="b9810-121">Visible u oculto</span><span class="sxs-lookup"><span data-stu-id="b9810-121">Visible or hidden</span></span>     | [<span data-ttu-id="b9810-122">PKEY de IU \_ \_ visible</span><span class="sxs-lookup"><span data-stu-id="b9810-122">UI\_PKEY\_Viewable</span></span>](windowsribbon-reference-properties-uipkey-viewable.md)   |



 

## <a name="minimize-the-ribbon"></a><span data-ttu-id="b9810-123">Minimizar la cinta de opciones</span><span class="sxs-lookup"><span data-stu-id="b9810-123">Minimize the Ribbon</span></span>

<span data-ttu-id="b9810-124">Una aplicación de marco de cinta puede establecer dinámicamente el estado minimizado de la barra de comandos de la cinta de opciones estableciendo el valor de la clave de la propiedad [ \_ PKEY \_ minimizada](windowsribbon-reference-properties-uipkey-minimized.md) de la interfaz de usuario en **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="b9810-124">A Ribbon framework application can dynamically set the minimized state of the ribbon command bar by setting the value of the [UI\_PKEY\_Minimized](windowsribbon-reference-properties-uipkey-minimized.md) property key to **true** or **false**.</span></span>



| <span data-ttu-id="b9810-125">Estado de presentación</span><span class="sxs-lookup"><span data-stu-id="b9810-125">Display State</span></span> | <span data-ttu-id="b9810-126">Valor de clave de propiedad</span><span class="sxs-lookup"><span data-stu-id="b9810-126">Property Key Value</span></span> |
|---------------|--------------------|
| <span data-ttu-id="b9810-127">Expandido</span><span class="sxs-lookup"><span data-stu-id="b9810-127">Expanded</span></span>      | <span data-ttu-id="b9810-128">**false**</span><span class="sxs-lookup"><span data-stu-id="b9810-128">**false**</span></span>          |
| <span data-ttu-id="b9810-129">Collapsed</span><span class="sxs-lookup"><span data-stu-id="b9810-129">Collapsed</span></span>     | <span data-ttu-id="b9810-130">**true**</span><span class="sxs-lookup"><span data-stu-id="b9810-130">**true**</span></span>           |



 

<span data-ttu-id="b9810-131">Cuando la interfaz de usuario de la cinta de opciones se encuentra en un estado minimizado, la fila de la pestaña de la cinta permanece visible y es totalmente funcional.</span><span class="sxs-lookup"><span data-stu-id="b9810-131">When the ribbon UI is in a minimized state, the ribbon Tab row remains visible and fully functional.</span></span>

<span data-ttu-id="b9810-132">En la captura de pantalla siguiente se muestra la cinta de opciones en el estado minimizado.</span><span class="sxs-lookup"><span data-stu-id="b9810-132">The following screen shot shows the ribbon in the minimized state.</span></span>

![captura de pantalla que muestra la interfaz de usuario de la cinta minimizada.](images/overviews/ribbon-minimized.png)

> [!Note]  
> <span data-ttu-id="b9810-134">El marco de la cinta de opciones expone esta funcionalidad al usuario final a través de la selección de "minimizar la cinta" del menú contextual de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="b9810-134">The Ribbon framework exposes this functionality to the end user through the "Minimize the Ribbon" selection of the ribbon context menu.</span></span>

 

## <a name="hide-the-ribbon"></a><span data-ttu-id="b9810-135">Ocultar la cinta de opciones</span><span class="sxs-lookup"><span data-stu-id="b9810-135">Hide the Ribbon</span></span>

<span data-ttu-id="b9810-136">Una aplicación de marco de cinta puede establecer dinámicamente el estado visible de la barra de comandos de la cinta de opciones estableciendo el valor de la clave de propiedad [ \_ PKEY \_ visible](windowsribbon-reference-properties-uipkey-viewable.md) de la interfaz de usuario en **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="b9810-136">A Ribbon framework application can dynamically set the viewable state of the ribbon command bar by setting the value of the [UI\_PKEY\_Viewable](windowsribbon-reference-properties-uipkey-viewable.md) property key to **true** or **false**.</span></span>



| <span data-ttu-id="b9810-137">Estado de presentación</span><span class="sxs-lookup"><span data-stu-id="b9810-137">Display State</span></span> | <span data-ttu-id="b9810-138">Valor de clave de propiedad</span><span class="sxs-lookup"><span data-stu-id="b9810-138">Property Key Value</span></span> |
|---------------|--------------------|
| <span data-ttu-id="b9810-139">Visible</span><span class="sxs-lookup"><span data-stu-id="b9810-139">Visible</span></span>       | <span data-ttu-id="b9810-140">**false**</span><span class="sxs-lookup"><span data-stu-id="b9810-140">**false**</span></span>          |
| <span data-ttu-id="b9810-141">Hidden</span><span class="sxs-lookup"><span data-stu-id="b9810-141">Hidden</span></span>        | <span data-ttu-id="b9810-142">**true**</span><span class="sxs-lookup"><span data-stu-id="b9810-142">**true**</span></span>           |



 

<span data-ttu-id="b9810-143">A diferencia de la propiedad PKEY de la interfaz de usuario [ \_ \_ minimizada](windowsribbon-reference-properties-uipkey-minimized.md) , el establecimiento de la [UI \_ PKEY \_ visible](windowsribbon-reference-properties-uipkey-viewable.md) en **false** representa la interfaz de usuario de la cinta de opciones invisible y totalmente inutilizable para un usuario final.</span><span class="sxs-lookup"><span data-stu-id="b9810-143">In contrast to the [UI\_PKEY\_Minimized](windowsribbon-reference-properties-uipkey-minimized.md) property, setting [UI\_PKEY\_Viewable](windowsribbon-reference-properties-uipkey-viewable.md) to **false** renders the ribbon UI invisible and completely unusable to an end user.</span></span>

<span data-ttu-id="b9810-144">En la captura de pantalla siguiente se muestra la cinta de opciones en estado oculto.</span><span class="sxs-lookup"><span data-stu-id="b9810-144">The following screen shot shows the ribbon in the hidden state.</span></span>

![captura de pantalla que muestra la interfaz de usuario de la cinta oculta.](images/overviews/ribbon-viewable.png)

## <a name="example"></a><span data-ttu-id="b9810-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b9810-146">Example</span></span>

<span data-ttu-id="b9810-147">En el ejemplo siguiente se muestra cómo establecer el estado de la interfaz de usuario de la cinta de opciones en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="b9810-147">The following example demonstrates how to set the state of the ribbon UI at run time.</span></span>

<span data-ttu-id="b9810-148">En este caso, la función [**IUICommandHandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) se usa para expandir o contraer la interfaz de usuario de la cinta de opciones según el estado de alternancia de un [botón de alternancia](windowsribbon-controls-togglebutton.md).</span><span class="sxs-lookup"><span data-stu-id="b9810-148">In this case, the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) function is used to expand or collapse the ribbon UI based on the toggle state of a [Toggle Button](windowsribbon-controls-togglebutton.md).</span></span>


```C++
//
//  FUNCTION: Execute()
//
//  PURPOSE: Called by the Ribbon framework when a Command is executed 
//           by the user. 
//           This example demonstrates a handler for a Toggle Button
//           that sets the minimized state of the ribbon UI.
//
//  NOTES: g_pFramework is a global pointer to an IUIFramework object 
//         that is assigned when the Ribbon framework is initialized.
//
//         g_pRibbon is a global pointer to the IUIRibbon object
//         that is assigned when the Ribbon framework is initialized.
//
STDMETHODIMP CCommandHandler::Execute(
    UINT nCmdID,
    UI_EXECUTIONVERB verb,
    __in_opt const PROPERTYKEY* key,
    __in_opt const PROPVARIANT* ppropvarValue,
    __in_opt IUISimplePropertySet* pCommandExecutionProperties)
{
    HRESULT hr = E_FAIL;

    if (verb == UI_EXECUTIONVERB_EXECUTE)
    {
        switch (nCmdID)
        {
            // Minimize ribbon Command handler.
            case IDR_CMD_MINIMIZE:
                if (g_pFramework)
                {
                    IPropertyStore *pPropertyStore = NULL;
                    hr = g_pRibbon->QueryInterface(__uuidof(IPropertyStore), 
                                                   (void**)&pPropertyStore);
                    if (SUCCEEDED(hr))
                    {
                        if (ppropvarValue != NULL)
                        {
                            // Is the ToggleButton state on or off?
                            BOOL fToggled;
                            hr = UIPropertyToBoolean(*key, *ppropvarValue, &fToggled);

                            if (SUCCEEDED(hr))
                            {
                                // Set the ribbon display state based on the toggle state.
                                PROPVARIANT propvar;
                                PropVariantInit(&propvar);
                                UIInitPropertyFromBoolean(UI_PKEY_Minimized, 
                                                          fToggled, 
                                                          &propvar);
                                hr = pPropertyStore->SetValue(UI_PKEY_Minimized, 
                                                              propvar);
                                pPropertyStore->Commit();
                            }
                            pPropertyStore->Release();
                        }
                    }
                }
                break;
        }
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="b9810-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b9810-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9810-150">Propiedades de la cinta</span><span class="sxs-lookup"><span data-stu-id="b9810-150">Ribbon Properties</span></span>](windowsribbon-reference-properties-ribbon.md)
</dt> </dl>

 

 