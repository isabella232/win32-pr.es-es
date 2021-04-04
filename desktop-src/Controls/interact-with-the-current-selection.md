---
title: Cómo interactuar con la selección actual
description: El usuario puede seleccionar texto en un control Rich Edit mediante el mouse o el teclado.
ms.assetid: A529792C-DFA7-4BE1-8607-5A1556B64626
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec776ab0c8e07bb61dcc0e12d13af46b17d094a
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2020
ms.locfileid: "103789358"
---
# <a name="how-to-interact-with-the-current-selection"></a><span data-ttu-id="d1c6f-103">Cómo interactuar con la selección actual</span><span class="sxs-lookup"><span data-stu-id="d1c6f-103">How to Interact with the Current Selection</span></span>

<span data-ttu-id="d1c6f-104">El usuario puede seleccionar texto en un control Rich Edit mediante el mouse o el teclado.</span><span class="sxs-lookup"><span data-stu-id="d1c6f-104">The user can select text in a rich edit control by using the mouse or the keyboard.</span></span> <span data-ttu-id="d1c6f-105">La *selección actual* es el intervalo de caracteres seleccionados o la posición del punto de inserción si no se selecciona ningún carácter.</span><span class="sxs-lookup"><span data-stu-id="d1c6f-105">The *current selection* is the range of selected characters, or the position of the insertion point if no characters are selected.</span></span> <span data-ttu-id="d1c6f-106">Una aplicación puede obtener información sobre la selección actual, establecerla, determinar cuándo cambia y mostrar u ocultar el resaltado de la selección.</span><span class="sxs-lookup"><span data-stu-id="d1c6f-106">An application can get information about the current selection, set it, determine when it changes, and show or hide the selection highlight.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="d1c6f-107">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="d1c6f-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="d1c6f-108">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="d1c6f-108">Technologies</span></span>

-   [<span data-ttu-id="d1c6f-109">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="d1c6f-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="d1c6f-110">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d1c6f-110">Prerequisites</span></span>

-   <span data-ttu-id="d1c6f-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="d1c6f-111">C/C++</span></span>
-   <span data-ttu-id="d1c6f-112">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="d1c6f-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="d1c6f-113">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="d1c6f-113">Instructions</span></span>

### <a name="interact-with-the-current-selection"></a><span data-ttu-id="d1c6f-114">Interactuar con la selección actual</span><span class="sxs-lookup"><span data-stu-id="d1c6f-114">Interact with the Current Selection</span></span>

<span data-ttu-id="d1c6f-115">Para determinar la selección actual en un control Rich Edit, utilice el [**mensaje \_ EXGETSEL em**](em-exgetsel.md) .</span><span class="sxs-lookup"><span data-stu-id="d1c6f-115">To determine the current selection in a rich edit control, use the [**EM\_EXGETSEL**](em-exgetsel.md) message.</span></span> <span data-ttu-id="d1c6f-116">Para establecer la selección actual, use el [**mensaje \_ EXSETSEL em**](em-exsetsel.md) .</span><span class="sxs-lookup"><span data-stu-id="d1c6f-116">To set the current selection, use the [**EM\_EXSETSEL**](em-exsetsel.md) message.</span></span> <span data-ttu-id="d1c6f-117">La estructura [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) se usa con ambos mensajes y especifica un intervalo de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d1c6f-117">The [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) structure is used with both messages and specifies a range of characters.</span></span> <span data-ttu-id="d1c6f-118">Para recuperar información sobre el contenido de la selección actual, puede usar el mensaje [**\_ SELECTIONTYPE em**](em-selectiontype.md) .</span><span class="sxs-lookup"><span data-stu-id="d1c6f-118">To retrieve information about the contents of the current selection, you can use the [**EM\_SELECTIONTYPE**](em-selectiontype.md) message.</span></span>

<span data-ttu-id="d1c6f-119">Una aplicación puede detectar cuándo cambia la selección actual procesando el código de notificación [en \_ SELCHANGE](en-selchange.md) .</span><span class="sxs-lookup"><span data-stu-id="d1c6f-119">An application can detect when the current selection changes by processing the [EN\_SELCHANGE](en-selchange.md) notification code.</span></span> <span data-ttu-id="d1c6f-120">El código de notificación especifica una estructura [**SELCHANGE**](/windows/desktop/api/Richedit/ns-richedit-selchange) que contiene información sobre la nueva selección.</span><span class="sxs-lookup"><span data-stu-id="d1c6f-120">The notification code specifies a [**SELCHANGE**](/windows/desktop/api/Richedit/ns-richedit-selchange) structure that contains information about the new selection.</span></span> <span data-ttu-id="d1c6f-121">Un control Rich Edit envía este código de notificación solo si se habilita mediante el mensaje [**em \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="d1c6f-121">A rich edit control sends this notification code only if you enable it by using the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

<span data-ttu-id="d1c6f-122">De forma predeterminada, un control Rich Edit muestra y oculta el resaltado de la selección cuando gana y pierde el foco.</span><span class="sxs-lookup"><span data-stu-id="d1c6f-122">By default, a rich edit control shows and hides the selection highlight when it gains and loses the focus.</span></span> <span data-ttu-id="d1c6f-123">Puede mostrar u ocultar el resaltado de la selección en cualquier momento mediante el mensaje de [**\_ HIDESELECTION em**](em-hideselection.md) .</span><span class="sxs-lookup"><span data-stu-id="d1c6f-123">You can show or hide the selection highlight at any time by using the [**EM\_HIDESELECTION**](em-hideselection.md) message.</span></span> <span data-ttu-id="d1c6f-124">Por ejemplo, una aplicación podría proporcionar un cuadro de diálogo de búsqueda para buscar texto en un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="d1c6f-124">For example, an application might provide a Search dialog box to find text in a rich edit control.</span></span> <span data-ttu-id="d1c6f-125">La aplicación podría seleccionar texto coincidente sin cerrar el cuadro de diálogo, en cuyo caso debe usar el mensaje de **\_ HIDESELECTION em** para resaltar la selección.</span><span class="sxs-lookup"><span data-stu-id="d1c6f-125">The application might select matching text without closing the dialog box, in which case it must use the **EM\_HIDESELECTION** message to highlight the selection.</span></span>

<span data-ttu-id="d1c6f-126">Al igual que con los controles de edición, puede especificar el estilo de ventana [**\_ NOHIDESEL es**](edit-control-styles.md) para evitar que un control Rich Edit oculte el resaltado de la selección cuando pierde el foco.</span><span class="sxs-lookup"><span data-stu-id="d1c6f-126">As with edit controls, you can specify the [**ES\_NOHIDESEL**](edit-control-styles.md) window style to prevent a rich edit control from hiding the selection highlight when it loses the focus.</span></span>

<span data-ttu-id="d1c6f-127">Como alternativa al uso de los [**mensajes \_ em EXGETSEL**](em-exgetsel.md) y [**em \_ EXSETSEL**](em-exsetsel.md) , puede recuperar y establecer la selección actual mediante los mensajes de control de edición [**em \_ GETSEL**](em-getsel.md) y [**em \_ SETSEL**](em-setsel.md) .</span><span class="sxs-lookup"><span data-stu-id="d1c6f-127">As an alternative to using the [**EM\_EXGETSEL**](em-exgetsel.md) and [**EM\_EXSETSEL**](em-exsetsel.md) messages, you can retrieve and set the current selection by using the [**EM\_GETSEL**](em-getsel.md) and [**EM\_SETSEL**](em-setsel.md) edit control messages.</span></span> <span data-ttu-id="d1c6f-128">El **carácter \_ GETSEL de EM** de paquetes de mensajes 2 16 bits indiza en el valor devuelto de 32 bits y, por lo tanto, solo funciona para las selecciones que se encuentran completamente dentro de los primeros 64 KB.</span><span class="sxs-lookup"><span data-stu-id="d1c6f-128">The **EM\_GETSEL** message packs two 16-bit character indexes into its 32-bit return value and therefore, works only for selections that fall entirely within the first 64K.</span></span> <span data-ttu-id="d1c6f-129">Sin embargo, un control Rich Edit nunca contendrá más de 32 000 caracteres de texto, a menos que amplíe este límite mediante el mensaje [**em \_ LIMITTEXT**](em-limittext.md) o [**em \_ EXLIMITTEXT**](em-exlimittext.md) .</span><span class="sxs-lookup"><span data-stu-id="d1c6f-129">However, a rich edit control will never contain more than 32K characters of text, unless you extend this limit by using the [**EM\_LIMITTEXT**](em-limittext.md) or [**EM\_EXLIMITTEXT**](em-exlimittext.md) message.</span></span> <span data-ttu-id="d1c6f-130">En las selecciones que superen los primeros 64 KB de texto, el mensaje **\_ GETSEL em** devuelve – 1.</span><span class="sxs-lookup"><span data-stu-id="d1c6f-130">For selections that extend beyond the first 64 KB of text, the **EM\_GETSEL** message returns –1.</span></span> <span data-ttu-id="d1c6f-131">En tal caso, puede seguir usando los valores que se devuelven en *wParam* e *lParam* para buscar los caracteres inicial y final de la selección.</span><span class="sxs-lookup"><span data-stu-id="d1c6f-131">In such a case you can still use the values that are returned in *wParam* and *lParam* to find the start and end characters of the selection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1c6f-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d1c6f-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1c6f-133">Usar controles Rich Edit</span><span class="sxs-lookup"><span data-stu-id="d1c6f-133">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="d1c6f-134">[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="d1c6f-134">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




