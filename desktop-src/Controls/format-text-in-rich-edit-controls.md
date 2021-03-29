---
title: Cómo dar formato al texto en los controles Rich Edit
description: Una aplicación puede enviar mensajes a un control Rich Edit con el fin de dar formato a caracteres y párrafos y recuperar información de formato.
ms.assetid: 19A4F0D1-88C5-407D-A70F-CB486DAD352E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 246c6309dec94538f47ed9ca7e464f1d6d17f240
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2020
ms.locfileid: "103789363"
---
# <a name="how-to-format-text-in-rich-edit-controls"></a><span data-ttu-id="33301-103">Cómo dar formato al texto en los controles Rich Edit</span><span class="sxs-lookup"><span data-stu-id="33301-103">How to Format Text in Rich Edit Controls</span></span>

<span data-ttu-id="33301-104">Una aplicación puede enviar mensajes a un control Rich Edit con el fin de dar formato a caracteres y párrafos y recuperar información de formato.</span><span class="sxs-lookup"><span data-stu-id="33301-104">An application can send messages to a rich edit control in order to format characters and paragraphs and retrieve formatting information.</span></span> <span data-ttu-id="33301-105">Los atributos de formato de párrafo incluyen alineación, tabulaciones, sangrías, numeración y tablas simples.</span><span class="sxs-lookup"><span data-stu-id="33301-105">Paragraph formatting attributes include alignment, tabs, indents, numbering, and simple tables.</span></span> <span data-ttu-id="33301-106">En el caso de los caracteres, puede especificar el nombre, el tamaño, el color y los efectos de la fuente, como Bold, Italic y protected.</span><span class="sxs-lookup"><span data-stu-id="33301-106">For characters, you can specify font name, size, color, and effects such as bold, italic, and protected.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="33301-107">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="33301-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="33301-108">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="33301-108">Technologies</span></span>

-   [<span data-ttu-id="33301-109">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="33301-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="33301-110">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="33301-110">Prerequisites</span></span>

-   <span data-ttu-id="33301-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="33301-111">C/C++</span></span>
-   <span data-ttu-id="33301-112">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="33301-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="33301-113">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="33301-113">Instructions</span></span>

### <a name="format-text-in-a-rich-edit-control"></a><span data-ttu-id="33301-114">Dar formato al texto en un control Rich Edit</span><span class="sxs-lookup"><span data-stu-id="33301-114">Format Text in a Rich Edit Control</span></span>

<span data-ttu-id="33301-115">Puede aplicar formato de párrafo mediante el mensaje [**em \_ SETPARAFORMAT**](em-setparaformat.md) .</span><span class="sxs-lookup"><span data-stu-id="33301-115">You can apply paragraph formatting by using the [**EM\_SETPARAFORMAT**](em-setparaformat.md) message.</span></span> <span data-ttu-id="33301-116">Para determinar el formato de párrafo actual del texto seleccionado, use el [**mensaje \_ GETPARAFORMAT em**](em-getparaformat.md) .</span><span class="sxs-lookup"><span data-stu-id="33301-116">To determine the current paragraph formatting for the selected text, use the [**EM\_GETPARAFORMAT**](em-getparaformat.md) message.</span></span> <span data-ttu-id="33301-117">La estructura [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) o [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) se usa con ambos mensajes para especificar los atributos de formato de párrafo.</span><span class="sxs-lookup"><span data-stu-id="33301-117">The [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) or [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) structure is used with both messages to specify paragraph formatting attributes.</span></span>

<span data-ttu-id="33301-118">Puede aplicar el formato de caracteres mediante el [**mensaje \_ SETCHARFORMAT em**](em-setcharformat.md) .</span><span class="sxs-lookup"><span data-stu-id="33301-118">You can apply character formatting by using the [**EM\_SETCHARFORMAT**](em-setcharformat.md) message.</span></span> <span data-ttu-id="33301-119">Para determinar el formato de caracteres actual del texto seleccionado, puede usar el mensaje [**\_ GETCHARFORMAT em**](em-getcharformat.md) .</span><span class="sxs-lookup"><span data-stu-id="33301-119">To determine the current character formatting for the selected text, you can use the [**EM\_GETCHARFORMAT**](em-getcharformat.md) message.</span></span> <span data-ttu-id="33301-120">La estructura [**Charformat**](/windows/win32/api/richedit/ns-richedit-charformata) o [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) se usa con ambos mensajes para especificar atributos de caracteres.</span><span class="sxs-lookup"><span data-stu-id="33301-120">The [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) or [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) structure is used with both messages to specify character attributes.</span></span>

<span data-ttu-id="33301-121">También puede usar los mensajes [**em \_ SETCHARFORMAT**](em-setcharformat.md) y [**em \_ GETCHARFORMAT**](em-getcharformat.md) para establecer y recuperar el formato de caracteres del punto de inserción, que es el formato que se aplica a los caracteres insertados posteriormente.</span><span class="sxs-lookup"><span data-stu-id="33301-121">You can also use [**EM\_SETCHARFORMAT**](em-setcharformat.md) and [**EM\_GETCHARFORMAT**](em-getcharformat.md) messages to set and retrieve the character formatting of the insertion point, which is the formatting that is applied to any subsequently inserted characters.</span></span> <span data-ttu-id="33301-122">Por ejemplo, si una aplicación establece el formato de caracteres predeterminado en negrita y el usuario escribe un carácter, ese carácter está en negrita.</span><span class="sxs-lookup"><span data-stu-id="33301-122">For example, if an application sets the default character formatting to bold and the user then types a character, that character is bold.</span></span>

<span data-ttu-id="33301-123">El formato de caracteres del punto de inserción se aplica al texto recién insertado solo si la selección actual está vacía (si la selección actual es un punto de inserción).</span><span class="sxs-lookup"><span data-stu-id="33301-123">The character formatting of the insertion point is applied to newly inserted text only if the current selection is empty (if the current selection is an insertion point).</span></span> <span data-ttu-id="33301-124">De lo contrario, el nuevo texto asume el formato de caracteres del texto que reemplaza.</span><span class="sxs-lookup"><span data-stu-id="33301-124">Otherwise, the new text assumes the character formatting of the text it replaces.</span></span> <span data-ttu-id="33301-125">Si cambia la selección, el formato de caracteres predeterminado cambia para coincidir con el primer carácter de la nueva selección.</span><span class="sxs-lookup"><span data-stu-id="33301-125">If the selection changes, the default character formatting changes to match the first character in the new selection.</span></span>

<span data-ttu-id="33301-126">El efecto de carácter protegido es único en el sentido de que no cambia la apariencia del texto.</span><span class="sxs-lookup"><span data-stu-id="33301-126">The protected character effect is unique in that it does not change the appearance of text.</span></span> <span data-ttu-id="33301-127">Si el usuario intenta modificar texto protegido, un control Rich Edit envía a su ventana primaria un código de notificación [ \_ protegido](en-protected.md) , lo que permite a la ventana primaria permitir o impedir el cambio.</span><span class="sxs-lookup"><span data-stu-id="33301-127">If the user attempts to modify protected text, a rich edit control sends its parent window an [EN\_PROTECTED](en-protected.md) notification code, allowing the parent window to allow or prevent the change.</span></span> <span data-ttu-id="33301-128">Para recibir este código de notificación, debe habilitarlo mediante el mensaje [**em \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="33301-128">To receive this notification code, you must enable it by using the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

<span data-ttu-id="33301-129">El color de primer plano es siempre un atributo de carácter.</span><span class="sxs-lookup"><span data-stu-id="33301-129">Foreground color is always a character attribute.</span></span> <span data-ttu-id="33301-130">En Microsoft Rich Edit 1,0, el color de fondo solo es una propiedad del control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="33301-130">In Microsoft Rich Edit 1.0, background color is only a property of the rich edit control.</span></span> <span data-ttu-id="33301-131">Para establecer el color de fondo predeterminado, utilice el mensaje [**\_ SETBKGNDCOLOR em**](em-setbkgndcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="33301-131">To set the default background color, use the [**EM\_SETBKGNDCOLOR**](em-setbkgndcolor.md) message.</span></span> <span data-ttu-id="33301-132">Tenga en cuenta que la edición enriquecida no admite el mensaje [**\_ CTLCOLOREDIT de WM**](wm-ctlcoloredit.md) .</span><span class="sxs-lookup"><span data-stu-id="33301-132">Note that Rich Edit does not support the [**WM\_CTLCOLOREDIT**](wm-ctlcoloredit.md) message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="33301-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="33301-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33301-134">Usar controles Rich Edit</span><span class="sxs-lookup"><span data-stu-id="33301-134">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="33301-135">[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="33301-135">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




