---
title: Cómo procesar mensajes de notificación
description: Una hoja de propiedades envía \_ mensajes de notificación de WM para recuperar información de las páginas y para notificar a las páginas las acciones del usuario.
ms.assetid: 82768E43-97BA-451A-9373-D5B8FD06ABED
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c544910e44e0c865e738427285d7488147b9c1
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2020
ms.locfileid: "103789357"
---
# <a name="how-to-process-notification-messages"></a><span data-ttu-id="dbafa-103">Cómo procesar mensajes de notificación</span><span class="sxs-lookup"><span data-stu-id="dbafa-103">How to Process Notification Messages</span></span>

<span data-ttu-id="dbafa-104">Una hoja de propiedades envía mensajes de [**\_ notificación de WM**](wm-notify.md) para recuperar información de las páginas y para notificar a las páginas las acciones del usuario.</span><span class="sxs-lookup"><span data-stu-id="dbafa-104">A property sheet sends [**WM\_NOTIFY**](wm-notify.md) messages to retrieve information from the pages and to notify the pages of user actions.</span></span>

<span data-ttu-id="dbafa-105">El parámetro *lParam* del mensaje es la dirección de una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene el identificador del cuadro de diálogo de la hoja de propiedades, el identificador del cuadro de diálogo de la página y un código de notificación.</span><span class="sxs-lookup"><span data-stu-id="dbafa-105">The *lParam* parameter of the message is the address of an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure, which contains the handle to the property sheet dialog box, the handle to the page dialog box, and a notification code.</span></span> <span data-ttu-id="dbafa-106">La página debe responder a algunos mensajes de notificación estableciendo el \_ valor de DWL MSGRESULT de la página en **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="dbafa-106">The page must respond to some notification messages by setting the DWL\_MSGRESULT value of the page to either **TRUE** or **FALSE**.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="dbafa-107">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="dbafa-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="dbafa-108">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="dbafa-108">Technologies</span></span>

-   [<span data-ttu-id="dbafa-109">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="dbafa-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="dbafa-110">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="dbafa-110">Prerequisites</span></span>

-   <span data-ttu-id="dbafa-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="dbafa-111">C/C++</span></span>
-   <span data-ttu-id="dbafa-112">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="dbafa-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="dbafa-113">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="dbafa-113">Instructions</span></span>

### <a name="process-notification-messages"></a><span data-ttu-id="dbafa-114">Procesar mensajes de notificación</span><span class="sxs-lookup"><span data-stu-id="dbafa-114">Process Notification Messages</span></span>

<span data-ttu-id="dbafa-115">El ejemplo siguiente es un fragmento de código del procedimiento de cuadro de diálogo para una página.</span><span class="sxs-lookup"><span data-stu-id="dbafa-115">The following example is a code fragment from the dialog box procedure for a page.</span></span> <span data-ttu-id="dbafa-116">Muestra cómo procesar el código de notificación de la [ \_ ayuda de PSN](psn-help.md) .</span><span class="sxs-lookup"><span data-stu-id="dbafa-116">It shows how to process the [PSN\_HELP](psn-help.md) notification code.</span></span>


```C++
case WM_NOTIFY:

    switch (((NMHDR FAR *) lParam)->code) 
    {
    case PSN_HELP:
        {
         
        char szBuf[FILE_LEN]; // Buffer for name of Help file

        // Display Help for the font properties page.
        LoadString(g_hinst, IDS_HELPFILE, &szBuf, sizeof(szBuf)/sizeof(szBuf[0]));
        WinHelp(((NMHDR FAR *)lParam)->hwndFrom, &szBuf, HELP_CONTEXT, IDH_FONT_PROPERTIES);                
        
        break;
        
         }
         
        // Process other property sheet notifications here.
    }
    
```



## <a name="related-topics"></a><span data-ttu-id="dbafa-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dbafa-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dbafa-118">Usar hojas de propiedades</span><span class="sxs-lookup"><span data-stu-id="dbafa-118">Using Property Sheets</span></span>](using-property-sheets.md)
</dt> <dt>

<span data-ttu-id="dbafa-119">[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="dbafa-119">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




