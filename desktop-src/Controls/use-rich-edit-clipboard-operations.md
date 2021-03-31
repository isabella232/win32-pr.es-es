---
title: Cómo usar las operaciones de edición enriquecida del portapapeles
description: Una aplicación puede pegar el contenido del portapapeles en un control Rich Edit mediante el mejor formato de Portapapeles disponible o un formato específico del portapapeles.
ms.assetid: 1FEFFD95-839B-4A26-A26E-B8429D5FF4C0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a46432054956914b484c9faeeeda78f2a18e132
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103995677"
---
# <a name="how-to-use-rich-edit-clipboard-operations"></a><span data-ttu-id="1d31d-103">Cómo usar las operaciones de edición enriquecida del portapapeles</span><span class="sxs-lookup"><span data-stu-id="1d31d-103">How to Use Rich Edit Clipboard Operations</span></span>

<span data-ttu-id="1d31d-104">Una aplicación puede pegar el contenido del portapapeles en un control Rich Edit mediante el mejor formato de Portapapeles disponible o un formato específico del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="1d31d-104">An application can paste the contents of the clipboard into a rich edit control by using either the best available clipboard format or a specific clipboard format.</span></span> <span data-ttu-id="1d31d-105">También puede determinar si un control Rich Edit es capaz de pegar un formato de Portapapeles.</span><span class="sxs-lookup"><span data-stu-id="1d31d-105">You can also determine whether a rich edit control is capable of pasting a clipboard format.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="1d31d-106">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="1d31d-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="1d31d-107">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="1d31d-107">Technologies</span></span>

-   [<span data-ttu-id="1d31d-108">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="1d31d-108">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="1d31d-109">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1d31d-109">Prerequisites</span></span>

-   <span data-ttu-id="1d31d-110">C/C++</span><span class="sxs-lookup"><span data-stu-id="1d31d-110">C/C++</span></span>
-   <span data-ttu-id="1d31d-111">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="1d31d-111">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="1d31d-112">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="1d31d-112">Instructions</span></span>

### <a name="use-a-rich-edit-clipboard-operation"></a><span data-ttu-id="1d31d-113">Usar una operación de edición enriquecida del portapapeles</span><span class="sxs-lookup"><span data-stu-id="1d31d-113">Use a Rich Edit Clipboard Operation</span></span>

<span data-ttu-id="1d31d-114">Al igual que con un control de edición, puede copiar o cortar el contenido de la selección actual mediante el mensaje de [**\_ copia de WM**](/windows/desktop/dataxchg/wm-copy) o de [**\_ corte de WM**](/windows/desktop/dataxchg/wm-cut) .</span><span class="sxs-lookup"><span data-stu-id="1d31d-114">As with an edit control, you can copy or cut the contents of the current selection by using the [**WM\_COPY**](/windows/desktop/dataxchg/wm-copy) or [**WM\_CUT**](/windows/desktop/dataxchg/wm-cut) message.</span></span> <span data-ttu-id="1d31d-115">Del mismo modo, puede pegar el contenido del portapapeles en un control Rich Edit mediante el mensaje de [**\_ pegado de WM**](/windows/desktop/dataxchg/wm-paste) .</span><span class="sxs-lookup"><span data-stu-id="1d31d-115">Similarly, you can paste the contents of the clipboard into a rich edit control by using the [**WM\_PASTE**](/windows/desktop/dataxchg/wm-paste) message.</span></span> <span data-ttu-id="1d31d-116">El control pega el primer formato disponible que reconoce, lo que supuestamente es el formato más descriptivo.</span><span class="sxs-lookup"><span data-stu-id="1d31d-116">The control pastes the first available format that it recognizes, which presumably is the most descriptive format.</span></span>

<span data-ttu-id="1d31d-117">Para pegar un formato específico del portapapeles, puede usar el mensaje de la [**\_ PASTESPECIAL em**](em-pastespecial.md) .</span><span class="sxs-lookup"><span data-stu-id="1d31d-117">To paste a specific clipboard format, you can use the [**EM\_PASTESPECIAL**](em-pastespecial.md) message.</span></span> <span data-ttu-id="1d31d-118">Este mensaje es útil para las aplicaciones con un comando **Pegar especial** que permite al usuario seleccionar el formato del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="1d31d-118">This message is useful for applications with a **Paste Special** command that enables the user to select the clipboard format.</span></span> <span data-ttu-id="1d31d-119">Puede usar el mensaje [**de \_ CANPASTE de EM**](em-canpaste.md) para determinar si el control reconoce un formato determinado.</span><span class="sxs-lookup"><span data-stu-id="1d31d-119">You can use the [**EM\_CANPASTE**](em-canpaste.md) message to determine whether a given format is recognized by the control.</span></span>

<span data-ttu-id="1d31d-120">También puede usar el mensaje de la [**\_ CANPASTE de EM**](em-canpaste.md) para determinar si un control Rich Edit reconoce cualquier formato de Portapapeles disponible.</span><span class="sxs-lookup"><span data-stu-id="1d31d-120">You can also use the [**EM\_CANPASTE**](em-canpaste.md) message to determine whether any available clipboard format is recognized by a rich edit control.</span></span> <span data-ttu-id="1d31d-121">Este mensaje es útil cuando se procesa el mensaje de [**\_ INITMENUPOPUP de WM**](/windows/desktop/menurc/wm-initmenupopup) .</span><span class="sxs-lookup"><span data-stu-id="1d31d-121">This message is useful when processing the [**WM\_INITMENUPOPUP**](/windows/desktop/menurc/wm-initmenupopup) message.</span></span> <span data-ttu-id="1d31d-122">Una aplicación podría habilitar o atenuar el comando **pegar** dependiendo de si el control puede pegar cualquier formato disponible.</span><span class="sxs-lookup"><span data-stu-id="1d31d-122">An application might enable or gray its **Paste** command depending on whether the control can paste any available format.</span></span>

<span data-ttu-id="1d31d-123">Los controles Rich Edit registran dos formatos de portapapeles:</span><span class="sxs-lookup"><span data-stu-id="1d31d-123">Rich edit controls register two clipboard formats:</span></span>

-   <span data-ttu-id="1d31d-124">Formato de texto enriquecido</span><span class="sxs-lookup"><span data-stu-id="1d31d-124">Rich Text Format</span></span>
-   <span data-ttu-id="1d31d-125">Formato de texto enriquecido sin objetos</span><span class="sxs-lookup"><span data-stu-id="1d31d-125">Rich Text Format Without Objects</span></span>
-   <span data-ttu-id="1d31d-126">Texto y objetos de RichEdit</span><span class="sxs-lookup"><span data-stu-id="1d31d-126">RichEdit Text and Objects</span></span>

<span data-ttu-id="1d31d-127">Una aplicación puede registrar estos formatos mediante la función [**RegisterClipboardFormat**](/windows/desktop/api/winuser/nf-winuser-registerclipboardformata) , especificando los valores de CF \_ RTF, CF \_ RTFNOOBJS y CF \_ RETEXTOBJ.</span><span class="sxs-lookup"><span data-stu-id="1d31d-127">An application can register these formats by using the [**RegisterClipboardFormat**](/windows/desktop/api/winuser/nf-winuser-registerclipboardformata) function, specifying the CF\_RTF, CF\_RTFNOOBJS, and CF\_RETEXTOBJ values.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d31d-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1d31d-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d31d-129">Usar controles Rich Edit</span><span class="sxs-lookup"><span data-stu-id="1d31d-129">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="1d31d-130">[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="1d31d-130">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 