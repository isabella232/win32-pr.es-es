---
title: Cómo mostrar la información sobre herramientas de los botones
description: Al especificar el estilo de \_ información sobre herramientas de TBSTYLE, la barra de herramientas crea y administra un control de información sobre herramientas. El control ToolTip está oculto y solo aparece cuando los usuarios mueven el puntero sobre un botón de la barra de herramientas y lo dejan ahí durante aproximadamente un segundo.
ms.assetid: 0383DB63-A10E-4235-A974-AB21551E086B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb37de7c21c904673a1f656533497130d50bd8f7
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2020
ms.locfileid: "103904453"
---
# <a name="how-to-display-tooltips-for-buttons"></a><span data-ttu-id="a9a58-104">Cómo mostrar la información sobre herramientas de los botones</span><span class="sxs-lookup"><span data-stu-id="a9a58-104">How to Display Tooltips for Buttons</span></span>

<span data-ttu-id="a9a58-105">Al especificar el estilo [**de \_ información sobre herramientas de TBSTYLE**](toolbar-control-and-button-styles.md) , la barra de herramientas crea y administra un control de información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="a9a58-105">When you specify the [**TBSTYLE\_TOOLTIPS**](toolbar-control-and-button-styles.md) style, the toolbar creates and manages a tooltip control.</span></span> <span data-ttu-id="a9a58-106">El control ToolTip está oculto y solo aparece cuando los usuarios mueven el puntero sobre un botón de la barra de herramientas y lo dejan ahí durante aproximadamente un segundo.</span><span class="sxs-lookup"><span data-stu-id="a9a58-106">The tooltip control is hidden and appears only when users move the pointer over a toolbar button and leave it there for approximately one second.</span></span>

<span data-ttu-id="a9a58-107">La aplicación puede proporcionar texto al control ToolTip de cualquiera de las maneras siguientes:</span><span class="sxs-lookup"><span data-stu-id="a9a58-107">Your application can supply text to the tooltip control in any one of the following ways:</span></span>

-   <span data-ttu-id="a9a58-108">Establezca el texto de la información sobre herramientas como el miembro **iString** de la estructura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) para cada botón.</span><span class="sxs-lookup"><span data-stu-id="a9a58-108">Set the tooltip text as the **iString** member of the [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure for each button.</span></span> <span data-ttu-id="a9a58-109">También debe enviar un mensaje de [**TB \_ SETMAXTEXTROWS**](tb-setmaxtextrows.md) y establecer el número máximo de filas de texto en 0, de modo que el texto no aparezca como etiqueta de botón en lugar de como información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="a9a58-109">You must also send a [**TB\_SETMAXTEXTROWS**](tb-setmaxtextrows.md) message and set the maximum text rows to 0, so that the text does not appear as the button label rather than as a tooltip.</span></span>
-   <span data-ttu-id="a9a58-110">Cree la barra de herramientas con el estilo de [**\_ lista TBSTYLE**](toolbar-control-and-button-styles.md) y, a continuación, establezca el estilo extendido [**TBSTYLE \_ ex \_ MIXEDBUTTONS**](toolbar-extended-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="a9a58-110">Create the toolbar with the [**TBSTYLE\_LIST**](toolbar-control-and-button-styles.md) style and then set the [**TBSTYLE\_EX\_MIXEDBUTTONS**](toolbar-extended-styles.md) extended style.</span></span> <span data-ttu-id="a9a58-111">Las etiquetas solo se muestran para los botones que tienen el estilo [**BTNS \_ SHOWTEXT**](toolbar-control-and-button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="a9a58-111">Labels are shown only for buttons that have the [**BTNS\_SHOWTEXT**](toolbar-control-and-button-styles.md) style.</span></span> <span data-ttu-id="a9a58-112">En el caso de los botones que no tienen este estilo, se muestra una información sobre herramientas que contiene el texto del botón.</span><span class="sxs-lookup"><span data-stu-id="a9a58-112">For buttons that do not have this style, a tooltip is shown that contains the button text.</span></span>
-   <span data-ttu-id="a9a58-113">Responda al código de notificación de [ \_ GETDISPINFO de TTN](ttn-getdispinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="a9a58-113">Respond to the [TTN\_GETDISPINFO](ttn-getdispinfo.md) notification code.</span></span>
-   <span data-ttu-id="a9a58-114">Responda al código de notificación de [ \_ GETINFOTIP de TBN](tbn-getinfotip.md) .</span><span class="sxs-lookup"><span data-stu-id="a9a58-114">Respond to the [TBN\_GETINFOTIP](tbn-getinfotip.md) notification code.</span></span>

<span data-ttu-id="a9a58-115">Una aplicación que necesita enviar mensajes directamente al control ToolTip puede recuperar el identificador del control mediante el mensaje [**TB \_ GETTOOLTIPS**](tb-gettooltips.md) .</span><span class="sxs-lookup"><span data-stu-id="a9a58-115">An application that needs to send messages directly to the tooltip control can retrieve the handle to the control by using the [**TB\_GETTOOLTIPS**](tb-gettooltips.md) message.</span></span> <span data-ttu-id="a9a58-116">Una aplicación puede reemplazar el control ToolTip de una barra de herramientas por otro control ToolTip mediante el mensaje [**\_ SETTOOLTIPS TB**](tb-settooltips.md) .</span><span class="sxs-lookup"><span data-stu-id="a9a58-116">An application can replace the tooltip control of a toolbar with another tooltip control by using the [**TB\_SETTOOLTIPS**](tb-settooltips.md) message.</span></span>

<span data-ttu-id="a9a58-117">La forma más flexible de proporcionar texto de información sobre herramientas es responder al código de notificación [TTN \_ GETDISPINFO](ttn-getdispinfo.md) o [TBN \_ GETINFOTIP](tbn-getinfotip.md) enviado por el control de la barra de herramientas a su elemento primario en forma de un mensaje de [**\_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="a9a58-117">The most flexible way of supplying tooltip text is to respond to the [TTN\_GETDISPINFO](ttn-getdispinfo.md) or [TBN\_GETINFOTIP](tbn-getinfotip.md) notification code sent by the toolbar control to its parent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <span data-ttu-id="a9a58-118">En el caso de [TTN \_ GETDISPINFO](ttn-getdispinfo.md), el parámetro *lParam* incluye un puntero a una estructura [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) (también definida como **LPTOOLTIPTEXT**) que especifica el identificador de comando del botón para el que se necesita texto de ayuda.</span><span class="sxs-lookup"><span data-stu-id="a9a58-118">For [TTN\_GETDISPINFO](ttn-getdispinfo.md), the *lParam* parameter includes a pointer to an [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) structure (also defined as **LPTOOLTIPTEXT**) that specifies the command identifier of the button for which Help text is needed.</span></span> <span data-ttu-id="a9a58-119">Este identificador está en el miembro **NMTTDISPINFO. HDR. idFrom** .</span><span class="sxs-lookup"><span data-stu-id="a9a58-119">This identifier is in the **NMTTDISPINFO.hdr.idFrom** member.</span></span> <span data-ttu-id="a9a58-120">Una aplicación puede copiar el texto de ayuda en la estructura, especificar la dirección de una cadena que contiene el texto de ayuda o especificar el identificador de instancia y el identificador de recurso de un recurso de cadena.</span><span class="sxs-lookup"><span data-stu-id="a9a58-120">An application can copy the Help text to the structure, specify the address of a string containing the Help text, or specify the instance handle and resource identifier of a string resource.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="a9a58-121">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="a9a58-121">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="a9a58-122">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="a9a58-122">Technologies</span></span>

-   [<span data-ttu-id="a9a58-123">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="a9a58-123">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="a9a58-124">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a9a58-124">Prerequisites</span></span>

-   <span data-ttu-id="a9a58-125">C/C++</span><span class="sxs-lookup"><span data-stu-id="a9a58-125">C/C++</span></span>
-   <span data-ttu-id="a9a58-126">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="a9a58-126">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="a9a58-127">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="a9a58-127">Instructions</span></span>

### <a name="display-a-tooltip-for-a-button"></a><span data-ttu-id="a9a58-128">Mostrar información sobre herramientas para un botón</span><span class="sxs-lookup"><span data-stu-id="a9a58-128">Display a Tooltip for a Button</span></span>

<span data-ttu-id="a9a58-129">En el ejemplo de código siguiente se controla el código de notificación de la información sobre herramientas de [TTN \_ GETDISPINFO](ttn-getdispinfo.md) proporcionando texto de los identificadores de recursos.</span><span class="sxs-lookup"><span data-stu-id="a9a58-129">The following example code handles the [TTN\_GETDISPINFO](ttn-getdispinfo.md) tooltip notification code by providing text from resource identifiers.</span></span>


```C++
case WM_NOTIFY: 
            
    switch (((LPNMHDR) lParam)->code) 
    {
    
    case TTN_GETDISPINFO: 
        { 
            LPTOOLTIPTEXT lpttt = (LPTOOLTIPTEXT)lParam; 
            
            // Set the instance of the module that contains the resource.
            lpttt->hinst = g_hInst; 
            
            UINT_PTR idButton = lpttt->hdr.idFrom;
            
            switch (idButton) 
            { 
            case IDM_NEW: 
                lpttt->lpszText = MAKEINTRESOURCE(IDS_TIPS_NEW); 
                break; 
                
            case IDM_OPEN: 
                lpttt->lpszText = MAKEINTRESOURCE(IDS_TIPS_OPEN); 
                break; 
                
            case IDM_SAVE: 
                lpttt->lpszText = MAKEINTRESOURCE(IDS_TIPS_SAVE); 
                break; 
            } 
            
            break; 
        } 
    }
    return TRUE;
```



## <a name="related-topics"></a><span data-ttu-id="a9a58-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a9a58-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9a58-131">Usar controles Toolbar</span><span class="sxs-lookup"><span data-stu-id="a9a58-131">Using Toolbar Controls</span></span>](using-toolbar-controls.md)
</dt> <dt>

<span data-ttu-id="a9a58-132">[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="a9a58-132">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




