---
title: Cómo crear controles Rich Edit
description: Para crear un control Rich Edit, llame a la función CreateWindowEx y especifique la clase Rich Edit Window.
ms.assetid: E0F3E458-7907-42BD-841A-CB3D12628AA8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6585e606cc77b307bf41aa938ed49e8baecb1349
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078420"
---
# <a name="how-to-create-rich-edit-controls"></a><span data-ttu-id="d8fdd-103">Cómo crear controles Rich Edit</span><span class="sxs-lookup"><span data-stu-id="d8fdd-103">How to Create Rich Edit Controls</span></span>

<span data-ttu-id="d8fdd-104">Para crear un control Rich Edit, llame a la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) y especifique la clase Rich Edit Window.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-104">To create a rich edit control, call the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying the rich edit window class.</span></span> <span data-ttu-id="d8fdd-105">Para Microsoft Rich Edit 4,1 (Msftedit.dll), especifique \_ la clase MSFTEDIT como clase de ventana.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-105">For Microsoft Rich Edit 4.1 (Msftedit.dll), specify MSFTEDIT\_CLASS as the window class.</span></span> <span data-ttu-id="d8fdd-106">En todas las versiones anteriores, especifique la \_ clase RICHEDIT.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-106">For all previous versions, specify RICHEDIT\_CLASS.</span></span> <span data-ttu-id="d8fdd-107">Para obtener más información, vea [versiones de Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="d8fdd-107">For more information, see [Versions of Rich Edit](about-rich-edit-controls.md).</span></span>

<span data-ttu-id="d8fdd-108">Los controles Rich Edit admiten la mayoría de los estilos de ventana que se usan con los controles de edición, así como estilos adicionales.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-108">Rich edit controls support most of the window styles used with edit controls as well as additional styles.</span></span> <span data-ttu-id="d8fdd-109">Debe especificar el estilo de ventana de [**\_ varias líneas Multiline**](edit-control-styles.md) si desea permitir más de una línea de texto en el control.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-109">You should specify the [**ES\_MULTILINE**](edit-control-styles.md) window style if you want to allow more than one line of text in the control.</span></span> <span data-ttu-id="d8fdd-110">Para obtener más información, vea [estilos de control Rich Edit](rich-edit-control-styles.md).</span><span class="sxs-lookup"><span data-stu-id="d8fdd-110">For more information, see [Rich Edit Control Styles](rich-edit-control-styles.md).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="d8fdd-111">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="d8fdd-111">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="d8fdd-112">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="d8fdd-112">Technologies</span></span>

-   [<span data-ttu-id="d8fdd-113">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="d8fdd-113">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="d8fdd-114">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d8fdd-114">Prerequisites</span></span>

-   <span data-ttu-id="d8fdd-115">C/C++</span><span class="sxs-lookup"><span data-stu-id="d8fdd-115">C/C++</span></span>
-   <span data-ttu-id="d8fdd-116">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="d8fdd-116">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="d8fdd-117">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="d8fdd-117">Instructions</span></span>

### <a name="create-a-rich-edit-control"></a><span data-ttu-id="d8fdd-118">Crear un control Rich Edit</span><span class="sxs-lookup"><span data-stu-id="d8fdd-118">Create a Rich Edit Control</span></span>

<span data-ttu-id="d8fdd-119">En la función de ejemplo siguiente se crea un control Rich Edit y se inicializa con texto.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-119">The following example function creates a rich edit control and initializes it with some text.</span></span>


```C++
HWND CreateRichEdit(HWND hwndOwner,        // Dialog box handle.
                    int x, int y,          // Location.
                    int width, int height, // Dimensions.
                    HINSTANCE hinst)       // Application or DLL instance.
{
    LoadLibrary(TEXT("Msftedit.dll"));
    
    HWND hwndEdit= CreateWindowEx(0, MSFTEDIT_CLASS, TEXT("Type here"),
        ES_MULTILINE | WS_VISIBLE | WS_CHILD | WS_BORDER | WS_TABSTOP, 
        x, y, width, height, 
        hwndOwner, NULL, hinst, NULL);
        
    return hwndEdit;
}
```



<span data-ttu-id="d8fdd-120">En Microsoft Visual Studio 2005 y versiones posteriores, es posible agregar un control Rich Edit en una plantilla de cuadro de diálogo arrastrando el control desde el cuadro de herramientas.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-120">In Microsoft Visual Studio 2005 and later, it is possible to add a rich edit control into a dialog template by dragging the control from the toolbox.</span></span> <span data-ttu-id="d8fdd-121">Sin embargo, si lo hace en el editor de cuadros de diálogo, no se asegura de que se cargue la biblioteca necesaria antes de crear el control.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-121">However, doing this in the dialog editor does not ensure that the required library will be loaded before the control is created.</span></span> <span data-ttu-id="d8fdd-122">Es necesario llamar a la función [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) para cargar Riched32.dll, Riched20.dll o Msftedit.dll antes de que se cree el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-122">It is necessary to call the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) function to load Riched32.dll, Riched20.dll, or Msftedit.dll before the dialog is created.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8fdd-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d8fdd-123">Remarks</span></span>

<span data-ttu-id="d8fdd-124">Para usar estilos visuales con estos controles, una aplicación debe incluir un manifiesto y debe llamar a la función [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) al principio del programa.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-124">To use visual styles with these controls, an application must include a manifest and must call the [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) function at the beginning of the program.</span></span> <span data-ttu-id="d8fdd-125">Para obtener información sobre los estilos visuales, vea [estilos visuales](themes-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d8fdd-125">For information on visual styles, see [Visual Styles](themes-overview.md).</span></span> <span data-ttu-id="d8fdd-126">Para obtener información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d8fdd-126">For information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d8fdd-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d8fdd-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8fdd-128">Usar controles Rich Edit</span><span class="sxs-lookup"><span data-stu-id="d8fdd-128">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="d8fdd-129">[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="d8fdd-129">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 