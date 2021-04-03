---
title: Cómo usar métodos de ficha en TOM
description: En el ejemplo siguiente se proporcionan funciones de C que ilustran el uso de los métodos de tabulación en el modelo de objetos de texto (TOM).
ms.assetid: C74B4E43-615D-48B9-9884-F626BAF31F74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9851b30fdf58c0d4200600c0c4c83c7f9a00a555
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2020
ms.locfileid: "103904456"
---
# <a name="how-to-use-tab-methods-in-tom"></a><span data-ttu-id="ca607-103">Cómo usar métodos de ficha en TOM</span><span class="sxs-lookup"><span data-stu-id="ca607-103">How to Use Tab Methods in TOM</span></span>

<span data-ttu-id="ca607-104">En el ejemplo siguiente se proporcionan funciones de C que ilustran el uso de los métodos de tabulación en el modelo de objetos de texto (TOM).</span><span class="sxs-lookup"><span data-stu-id="ca607-104">The following example provides C functions that illustrate the use of the tab methods in the Text Object Model (TOM).</span></span> <span data-ttu-id="ca607-105">Se supone que la mayoría de las aplicaciones incluyen una barra de herramientas que muestra la posición actual y el tipo de las pestañas del párrafo seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="ca607-105">It is assumed that most applications include a toolbar that shows the current position and type of the tabs for the currently selected paragraph.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="ca607-106">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="ca607-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="ca607-107">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="ca607-107">Technologies</span></span>

-   [<span data-ttu-id="ca607-108">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="ca607-108">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="ca607-109">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ca607-109">Prerequisites</span></span>

-   <span data-ttu-id="ca607-110">C/C++</span><span class="sxs-lookup"><span data-stu-id="ca607-110">C/C++</span></span>
-   <span data-ttu-id="ca607-111">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="ca607-111">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="ca607-112">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="ca607-112">Instructions</span></span>

### <a name="use-a-tab-method"></a><span data-ttu-id="ca607-113">Usar un método de tabulación</span><span class="sxs-lookup"><span data-stu-id="ca607-113">Use a Tab Method</span></span>

<span data-ttu-id="ca607-114">En el ejemplo de código siguiente se muestra cómo actualizar una barra de herramientas con los detalles de la pestaña actual.</span><span class="sxs-lookup"><span data-stu-id="ca607-114">The following code example demonstrates how to update a toolbar with the current tab details.</span></span>


```C++
HRESULT UpdateToolbar(ITextSelection *pSel)
{
    HRESULT hr       = S_OK;        
    ITextPara *pPara = 0;
    
    float f;
    long tbt;            // tab type
    long tbp;

    hr = pSel->GetPara(&pPara);
    
    if (FAILED(hr))
        goto cleanup;    // Paragraph properties are not supported
    
    f = (float) -1.0;    // Start at beginning
    
    while (pPara->GetTab(tbgoNext, &f, &tbt, NULL) == S_OK)
    {
            // Do something like draw tab icon on toolbar here
            // DrawTabPicture(f, tbt);
    }
    
cleanup:

    if (pPara)
        pPara->Release();
        
    return hr;
    
}
```



### <a name="copy-tab-information"></a><span data-ttu-id="ca607-115">Copiar información de pestañas</span><span class="sxs-lookup"><span data-stu-id="ca607-115">Copy Tab Information</span></span>

<span data-ttu-id="ca607-116">En el ejemplo siguiente se muestra cómo copiar solo la información de la pestaña de una interfaz [**ITextPara**](/windows/desktop/api/Tom/nn-tom-itextpara) a otra.</span><span class="sxs-lookup"><span data-stu-id="ca607-116">The following example shows how to copy only the tab information from one [**ITextPara**](/windows/desktop/api/Tom/nn-tom-itextpara) interface to another.</span></span> <span data-ttu-id="ca607-117">Toma dos parámetros: **ITextPara** \* *pParaFrom* (el párrafo del que se copian las pestañas) y **ITextPara** \* *pParaFrom* (el párrafo en el que se copian las pestañas).</span><span class="sxs-lookup"><span data-stu-id="ca607-117">It takes two parameters: **ITextPara** \* *pParaFrom* (the paragraph from which to copy tabs) and **ITextPara** \* *pParaFrom* (the paragraph to which to copy tabs).</span></span>


```C++
HRESULT CopyOnlyTabs(ITextPara *pParaFrom, ITextPara *pParaTo)
{
    float f;
    short tbt;
    short style;
     
    pParaTo->ClearAllTabs();
    
    f = (float) -1.0;
    
    while (pParaFrom->GetTab(tbgoNext, &f, &tbt, &style) == S_OK)
        pParaTo->AddTab(f, tbt, style);
        
    return S_OK;                
    
}
```



## <a name="related-topics"></a><span data-ttu-id="ca607-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ca607-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca607-119">Usar el modelo de objetos de texto</span><span class="sxs-lookup"><span data-stu-id="ca607-119">Using The Text Object Model</span></span>](using-the-text-object-model.md)
</dt> <dt>

[<span data-ttu-id="ca607-120">Usar controles Rich Edit</span><span class="sxs-lookup"><span data-stu-id="ca607-120">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="ca607-121">[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="ca607-121">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




