---
title: Cómo etiquetar dinámicamente botones de barra de herramientas
description: Puede asignar texto a un botón existente mediante el \_ mensaje TB SETBUTTONINFO.
ms.assetid: 571C7FB9-2806-47AF-8933-0D3541AE6ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38dbf6cbefffa799f60909859c99d3e8c2d65e8e
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2020
ms.locfileid: "104487375"
---
# <a name="how-to-dynamically-label-toolbar-buttons"></a><span data-ttu-id="1c9e5-103">Cómo etiquetar dinámicamente botones de barra de herramientas</span><span class="sxs-lookup"><span data-stu-id="1c9e5-103">How to Dynamically Label Toolbar Buttons</span></span>

<span data-ttu-id="1c9e5-104">Puede asignar texto a un botón existente mediante el mensaje [**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md) .</span><span class="sxs-lookup"><span data-stu-id="1c9e5-104">You can assign text to an existing button by using the [**TB\_SETBUTTONINFO**](tb-setbuttoninfo.md) message.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="1c9e5-105">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="1c9e5-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="1c9e5-106">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="1c9e5-106">Technologies</span></span>

-   [<span data-ttu-id="1c9e5-107">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="1c9e5-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="1c9e5-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1c9e5-108">Prerequisites</span></span>

-   <span data-ttu-id="1c9e5-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="1c9e5-109">C/C++</span></span>
-   <span data-ttu-id="1c9e5-110">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="1c9e5-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="1c9e5-111">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="1c9e5-111">Instructions</span></span>

### <a name="dynamically-label-a-toolbar-button"></a><span data-ttu-id="1c9e5-112">Etiquetar dinámicamente un botón de la barra de herramientas</span><span class="sxs-lookup"><span data-stu-id="1c9e5-112">Dynamically Label a Toolbar Button</span></span>

<span data-ttu-id="1c9e5-113">En el ejemplo siguiente se muestra cómo cambiar el texto del tercer botón en los ejemplos anteriores de **Guardar** para **Guardar como**.</span><span class="sxs-lookup"><span data-stu-id="1c9e5-113">The following example demonstrates how to change the text of the third button in the previous examples from **Save** to **Save As**.</span></span>


```C++
LRESULT RelabelButton(HWND hWndToolbar)
{
    TBBUTTONINFO tbInfo;
    
    tbInfo.cbSize  = sizeof(TBBUTTONINFO);
    tbInfo.dwMask  = TBIF_TEXT;
    tbInfo.pszText = L"Save As";
    
    return SendMessage(hWndToolbar, TB_SETBUTTONINFO, (WPARAM)IDM_SAVE, (LPARAM)&tbInfo);
}
```



## <a name="remarks"></a><span data-ttu-id="1c9e5-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1c9e5-114">Remarks</span></span>

<span data-ttu-id="1c9e5-115">Cambiar el texto de un botón mediante [**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md) no afecta a la cadena asignada a ese botón en la lista de cadenas internas.</span><span class="sxs-lookup"><span data-stu-id="1c9e5-115">Changing a button's text by using [**TB\_SETBUTTONINFO**](tb-setbuttoninfo.md) does not affect the string that is assigned to that button in the internal string list.</span></span>

<span data-ttu-id="1c9e5-116">Si agrega una cadena de botón de barra de herramientas a la lista de texto interno, no puede recuperar el índice de esa cadena mediante una llamada a [TBN \_ GETBUTTONINFO](tbn-getbuttoninfo.md); debe usar el mensaje [**\_ GETBUTTON TB**](tb-getbutton.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="1c9e5-116">If you add a toolbar button string to the internal text list, you cannot retrieve the index of that string by calling [TBN\_GETBUTTONINFO](tbn-getbuttoninfo.md)—you must use the [**TB\_GETBUTTON**](tb-getbutton.md) message instead.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1c9e5-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1c9e5-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c9e5-118">Usar controles Toolbar</span><span class="sxs-lookup"><span data-stu-id="1c9e5-118">Using Toolbar Controls</span></span>](using-toolbar-controls.md)
</dt> <dt>

<span data-ttu-id="1c9e5-119">[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="1c9e5-119">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




