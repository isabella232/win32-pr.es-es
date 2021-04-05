---
title: Cómo cambiar automáticamente el tamaño de los controles Rich Edit
description: Una aplicación puede cambiar el tamaño de un control Rich Edit según sea necesario para que tenga siempre el mismo tamaño que su contenido.
ms.assetid: CCAFC039-AC9E-4BC4-ABE1-8C56FA9DD3F5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ee9ead05c4c04526a9290dc115f7a2fa7741397
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078460"
---
# <a name="how-to-automatically-resize-rich-edit-controls"></a><span data-ttu-id="ffa2b-103">Cómo cambiar automáticamente el tamaño de los controles Rich Edit</span><span class="sxs-lookup"><span data-stu-id="ffa2b-103">How to Automatically Resize Rich Edit Controls</span></span>

<span data-ttu-id="ffa2b-104">Una aplicación puede cambiar el tamaño de un control Rich Edit según sea necesario para que tenga siempre el mismo tamaño que su contenido.</span><span class="sxs-lookup"><span data-stu-id="ffa2b-104">An application can resize a rich edit control as needed so that it is always the same size as its contents.</span></span> <span data-ttu-id="ffa2b-105">Un control Rich Edit es compatible con esto, lo que *se denomina funcionalidad* sin límite mediante el envío de su ventana primaria a un código de notificación [en \_ REQUESTRESIZE](en-requestresize.md) cada vez que cambia el tamaño del contenido del control.</span><span class="sxs-lookup"><span data-stu-id="ffa2b-105">A rich edit control supports this so-called *bottomless* functionality by sending its parent window an [EN\_REQUESTRESIZE](en-requestresize.md) notification code whenever the size of the control's content changes.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="ffa2b-106">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="ffa2b-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="ffa2b-107">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="ffa2b-107">Technologies</span></span>

-   [<span data-ttu-id="ffa2b-108">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="ffa2b-108">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="ffa2b-109">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ffa2b-109">Prerequisites</span></span>

-   <span data-ttu-id="ffa2b-110">C/C++</span><span class="sxs-lookup"><span data-stu-id="ffa2b-110">C/C++</span></span>
-   <span data-ttu-id="ffa2b-111">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="ffa2b-111">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="ffa2b-112">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="ffa2b-112">Instructions</span></span>

### <a name="automatically-resize-a-rich-edit-control"></a><span data-ttu-id="ffa2b-113">Cambiar automáticamente el tamaño de un control Rich Edit</span><span class="sxs-lookup"><span data-stu-id="ffa2b-113">Automatically Resize a Rich Edit Control</span></span>

<span data-ttu-id="ffa2b-114">Al procesar el código de notificación [en \_ REQUESTRESIZE](en-requestresize.md) , una aplicación debe cambiar el tamaño del control a las dimensiones de la estructura [**REQRESIZE**](/windows/desktop/api/Richedit/ns-richedit-reqresize) especificada.</span><span class="sxs-lookup"><span data-stu-id="ffa2b-114">When processing the [EN\_REQUESTRESIZE](en-requestresize.md) notification code, an application should resize the control to the dimensions in the specified [**REQRESIZE**](/windows/desktop/api/Richedit/ns-richedit-reqresize) structure.</span></span> <span data-ttu-id="ffa2b-115">Una aplicación también puede trasladar cualquier información que esté cerca del control para acomodar el cambio de alto del control.</span><span class="sxs-lookup"><span data-stu-id="ffa2b-115">An application might also move any information that is near the control to accommodate the control's change in height.</span></span> <span data-ttu-id="ffa2b-116">Para cambiar el tamaño del control, puede usar la función [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) .</span><span class="sxs-lookup"><span data-stu-id="ffa2b-116">To resize the control, you can use the [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) function.</span></span>

<span data-ttu-id="ffa2b-117">Puede forzar que un control Rich Edit con un control Rich-less envíe un código de notificación [en \_ REQUESTRESIZE](en-requestresize.md) mediante el mensaje [**\_ REQUESTRESIZE em**](em-requestresize.md) .</span><span class="sxs-lookup"><span data-stu-id="ffa2b-117">You can force a bottomless rich edit control to send an [EN\_REQUESTRESIZE](en-requestresize.md) notification code by using the [**EM\_REQUESTRESIZE**](em-requestresize.md) message.</span></span> <span data-ttu-id="ffa2b-118">Este mensaje puede ser útil al procesar el mensaje de [**\_ tamaño de WM**](/windows/desktop/winmsg/wm-size) .</span><span class="sxs-lookup"><span data-stu-id="ffa2b-118">This message can be useful when processing the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffa2b-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ffa2b-119">Remarks</span></span>

<span data-ttu-id="ffa2b-120">Para recibir los códigos de notificación [en \_ REQUESTRESIZE](en-requestresize.md) , debe habilitar la notificación mediante el mensaje [em \_ SETEVENTMASK](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="ffa2b-120">To receive [EN\_REQUESTRESIZE](en-requestresize.md) notification codes, you must enable the notification by using the [EM\_SETEVENTMASK](em-seteventmask.md) message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ffa2b-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ffa2b-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ffa2b-122">Usar controles Rich Edit</span><span class="sxs-lookup"><span data-stu-id="ffa2b-122">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="ffa2b-123">[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="ffa2b-123">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 