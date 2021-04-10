---
title: Cómo proporcionar controles Rich Edit sin ventanas con funcionalidad de ventana
description: La funcionalidad de la ventana incluye la capacidad de recibir mensajes y la propiedad de un contexto de dispositivo en el que dibujar. Los controles de edición enriquecida sin ventanas reciben esta funcionalidad por medio de un par de interfaces ITextServices y ITextHost.
ms.assetid: 085CBC61-50AE-4F74-8C6A-436176DE0031
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce987630c21b1e15a2237066b39dd264125a857
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2020
ms.locfileid: "103995041"
---
# <a name="how-to-provide-windowless-rich-edit-controls-with-window-functionality"></a><span data-ttu-id="92b56-104">Cómo proporcionar controles Rich Edit sin ventanas con funcionalidad de ventana</span><span class="sxs-lookup"><span data-stu-id="92b56-104">How to Provide Windowless Rich Edit Controls with Window Functionality</span></span>

<span data-ttu-id="92b56-105">La funcionalidad de la ventana incluye la capacidad de recibir mensajes y la propiedad de un contexto de dispositivo en el que dibujar.</span><span class="sxs-lookup"><span data-stu-id="92b56-105">Window functionality includes the ability to receive messages and the ownership of a device context into which to draw.</span></span> <span data-ttu-id="92b56-106">Los controles de edición enriquecida sin ventanas reciben esta funcionalidad por medio de un par de interfaces: [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) y [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost).</span><span class="sxs-lookup"><span data-stu-id="92b56-106">Windowless rich edit controls receive this functionality by way of a pair of interfaces: [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) and [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="92b56-107">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="92b56-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="92b56-108">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="92b56-108">Technologies</span></span>

-   [<span data-ttu-id="92b56-109">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="92b56-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="92b56-110">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="92b56-110">Prerequisites</span></span>

-   <span data-ttu-id="92b56-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="92b56-111">C/C++</span></span>
-   <span data-ttu-id="92b56-112">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="92b56-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="92b56-113">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="92b56-113">Instructions</span></span>

### <a name="establish-the-window-functionality"></a><span data-ttu-id="92b56-114">Establecer la funcionalidad de la ventana</span><span class="sxs-lookup"><span data-stu-id="92b56-114">Establish the Window Functionality</span></span>

<span data-ttu-id="92b56-115">En el ejemplo de código siguiente se muestra cómo crear el host de texto y los servicios de texto.</span><span class="sxs-lookup"><span data-stu-id="92b56-115">The following example code demonstrates how to create the text host and text services.</span></span>


```
    HRESULT hr;
    
    IUnknown* pUnk               = NULL;
    ITextServices* pTextServices = NULL;
    
    // Create an instance of the application-defined object that implements the ITextHost interface.
    TextHost* pTextHost = new TextHost();
    
    if (pTextHost == NULL) 
        goto errorHandler;

    // Create an instance of the text services object.
    hr = CreateTextServices(NULL, pTextHost, &pUnk);
    
    if (FAILED(hr))
        goto errorHandler;
        
    // Retrieve the IID_ITextServices interface identifier from Msftedit.dll. 
    IID* pIID_ITS = (IID*) (VOID*) GetProcAddress(hmodRichEdit, "IID_ITextServices");
               
    // Retrieve the ITextServices interface.    
    hr = pUnk->QueryInterface(*pIID_ITS, (void **)&pTextServices);
    
    if (FAILED(hr))
        goto errorHandler;
```



## <a name="remarks"></a><span data-ttu-id="92b56-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="92b56-116">Remarks</span></span>

<span data-ttu-id="92b56-117">El parámetro *hmodRichEdit* en el ejemplo de código es un identificador del módulo de Msftedit.dll y se supone que ya se ha recuperado este identificador mediante una llamada a la función **GetModuleHandle** .</span><span class="sxs-lookup"><span data-stu-id="92b56-117">The *hmodRichEdit* parameter in the code example is a handle to the Msftedit.dll module, and it is assumed that this handle has already been retrieved by a call to the **GetModuleHandle** function.</span></span>

## <a name="complete-example"></a><span data-ttu-id="92b56-118">Ejemplo completo</span><span class="sxs-lookup"><span data-stu-id="92b56-118">Complete example</span></span>

## <a name="related-topics"></a><span data-ttu-id="92b56-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="92b56-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92b56-120">Usar controles Rich Edit sin ventanas</span><span class="sxs-lookup"><span data-stu-id="92b56-120">Using Windowless Rich Edit Controls</span></span>](using-windowless-rich-edit-controls.md)
</dt> <dt>

[<span data-ttu-id="92b56-121">Usar controles Rich Edit</span><span class="sxs-lookup"><span data-stu-id="92b56-121">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="92b56-122">[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="92b56-122">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




