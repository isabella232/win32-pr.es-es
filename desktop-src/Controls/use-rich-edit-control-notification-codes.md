---
title: Cómo usar los códigos de notificación de control Rich Edit
description: La ventana primaria de un control Rich Edit puede procesar los códigos de notificación para supervisar los eventos que afectan al control. Los controles Rich Edit admiten todos los códigos de notificación que se usan con controles de edición, así como varios otros.
ms.assetid: E045EADE-CB37-492A-85EC-6CF236677F08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e68e510bf7c5abe6109862a01d8926c8956736f9
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2020
ms.locfileid: "103995045"
---
# <a name="how-to-use-rich-edit-control-notification-codes"></a><span data-ttu-id="da0c0-104">Cómo usar los códigos de notificación de control Rich Edit</span><span class="sxs-lookup"><span data-stu-id="da0c0-104">How to Use Rich Edit Control Notification Codes</span></span>

<span data-ttu-id="da0c0-105">La ventana primaria de un control Rich Edit puede procesar los códigos de notificación para supervisar los eventos que afectan al control.</span><span class="sxs-lookup"><span data-stu-id="da0c0-105">A rich edit control's parent window can process notification codes to monitor events that affect the control.</span></span> <span data-ttu-id="da0c0-106">Los controles Rich Edit admiten todos los códigos de notificación que se usan con controles de edición, así como varios otros.</span><span class="sxs-lookup"><span data-stu-id="da0c0-106">Rich edit controls support all of the notification codes that are used with edit controls, as well as several additional ones.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="da0c0-107">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="da0c0-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="da0c0-108">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="da0c0-108">Technologies</span></span>

-   [<span data-ttu-id="da0c0-109">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="da0c0-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="da0c0-110">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="da0c0-110">Prerequisites</span></span>

-   <span data-ttu-id="da0c0-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="da0c0-111">C/C++</span></span>
-   <span data-ttu-id="da0c0-112">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="da0c0-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="da0c0-113">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="da0c0-113">Instructions</span></span>

### <a name="use-a-rich-edit-control-notification-code"></a><span data-ttu-id="da0c0-114">Usar un código de notificación de control de edición enriquecido</span><span class="sxs-lookup"><span data-stu-id="da0c0-114">Use a Rich Edit Control Notification Code</span></span>

<span data-ttu-id="da0c0-115">Puede determinar los códigos de notificación que un control Rich Edit envía su ventana primaria mediante el establecimiento de su máscara de eventos.</span><span class="sxs-lookup"><span data-stu-id="da0c0-115">You can determine which notification codes a rich edit control sends its parent window by setting its event mask.</span></span> <span data-ttu-id="da0c0-116">Para establecer la máscara de eventos para un control Rich Edit, utilice el mensaje de la [**\_ SETEVENTMASK em**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="da0c0-116">To set the event mask for a rich edit control, use the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span> <span data-ttu-id="da0c0-117">Puede recuperar la máscara de eventos actual para un control Rich Edit mediante el mensaje [**\_ GetEventMask (EM**](em-geteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="da0c0-117">You can retrieve the current event mask for a rich edit control by using the [**EM\_GETEVENTMASK**](em-geteventmask.md) message.</span></span> <span data-ttu-id="da0c0-118">Para obtener una lista de marcas de máscara de eventos, vea [marcas de máscara de eventos de control de edición enriquecida](rich-edit-control-event-mask-flags.md).</span><span class="sxs-lookup"><span data-stu-id="da0c0-118">For a list of event mask flags, see [Rich Edit Control Event Mask Flags](rich-edit-control-event-mask-flags.md).</span></span>

<span data-ttu-id="da0c0-119">La ventana primaria de un control Rich Edit puede filtrar todas las entradas del teclado y del mouse en el control procesando el código de notificación [en \_ MSGFILTER](en-msgfilter.md) .</span><span class="sxs-lookup"><span data-stu-id="da0c0-119">A rich edit control's parent window can filter all keyboard and mouse input to the control by processing the [EN\_MSGFILTER](en-msgfilter.md) notification code.</span></span> <span data-ttu-id="da0c0-120">La ventana primaria puede impedir que se procese el mensaje del teclado o del mouse, o bien cambiar el mensaje modificando la estructura [**MSGFILTER**](/windows/desktop/api/Richedit/ns-richedit-msgfilter) especificada.</span><span class="sxs-lookup"><span data-stu-id="da0c0-120">The parent window can prevent the keyboard or mouse message from being processed or can change the message by modifying the specified [**MSGFILTER**](/windows/desktop/api/Richedit/ns-richedit-msgfilter) structure.</span></span>

<span data-ttu-id="da0c0-121">Una aplicación puede procesar el código de notificación [en \_ protegido](en-protected.md) para detectar cuándo el usuario intenta modificar texto protegido.</span><span class="sxs-lookup"><span data-stu-id="da0c0-121">An application can process the [EN\_PROTECTED](en-protected.md) notification code to detect when the user attempts to modify protected text.</span></span> <span data-ttu-id="da0c0-122">Para marcar un intervalo de texto como protegido, puede establecer el efecto de carácter protegido.</span><span class="sxs-lookup"><span data-stu-id="da0c0-122">To mark a range of text as protected, you can set the protected character effect.</span></span>

<span data-ttu-id="da0c0-123">Puede permitir que el usuario coloque archivos en un control Rich Edit procesando el código de notificación [en \_ DROPFILES](en-dropfiles.md) .</span><span class="sxs-lookup"><span data-stu-id="da0c0-123">You can enable the user to drop files in a rich edit control by processing the [EN\_DROPFILES](en-dropfiles.md) notification code.</span></span> <span data-ttu-id="da0c0-124">La estructura [**ENDROPFILES**](/windows/desktop/api/Richedit/ns-richedit-endropfiles) especificada contiene información sobre los archivos que se van a quitar.</span><span class="sxs-lookup"><span data-stu-id="da0c0-124">The specified [**ENDROPFILES**](/windows/desktop/api/Richedit/ns-richedit-endropfiles) structure contains information about the files that are being dropped.</span></span>

## <a name="related-topics"></a><span data-ttu-id="da0c0-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="da0c0-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da0c0-126">Usar controles Rich Edit</span><span class="sxs-lookup"><span data-stu-id="da0c0-126">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="da0c0-127">[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="da0c0-127">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




