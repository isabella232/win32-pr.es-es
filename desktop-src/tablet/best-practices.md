---
description: Información general sobre los procedimientos recomendados al usar el objeto del panel de entrada del lápiz.
ms.assetid: 5b127743-0c88-4c4c-bcb6-5a91690cd2a1
title: Prácticas recomendadas (Tablet PC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd492dfeda94ce9dce056b286ef1989f3389658c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279386"
---
# <a name="best-practices-tablet-pc"></a><span data-ttu-id="3d8d9-103">Prácticas recomendadas (Tablet PC)</span><span class="sxs-lookup"><span data-stu-id="3d8d9-103">Best Practices (Tablet PC)</span></span>

<span data-ttu-id="3d8d9-104">Hay algunas instrucciones que deben tenerse en cuenta al usar el objeto [**PenInputPanel**](peninputpanel-class.md) .</span><span class="sxs-lookup"><span data-stu-id="3d8d9-104">There are a few guidelines to keep in mind when using the [**PenInputPanel**](peninputpanel-class.md) object.</span></span>

-   [<span data-ttu-id="3d8d9-105">Preferir el control InkEdit</span><span class="sxs-lookup"><span data-stu-id="3d8d9-105">Prefer InkEdit Control</span></span>](#prefer-inkedit-control)
-   [<span data-ttu-id="3d8d9-106">Deshabilitar el modo de tinta en los controles InkEdit</span><span class="sxs-lookup"><span data-stu-id="3d8d9-106">Disable Ink Mode on InkEdit Controls</span></span>](#disable-ink-mode-on-inkedit-controls)
-   [<span data-ttu-id="3d8d9-107">Usar controles sin ventana</span><span class="sxs-lookup"><span data-stu-id="3d8d9-107">Using Windowless Controls</span></span>](#using-windowless-controls)
-   [<span data-ttu-id="3d8d9-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3d8d9-108">Related topics</span></span>](#related-topics)

## <a name="prefer-inkedit-control"></a><span data-ttu-id="3d8d9-109">Preferir el control InkEdit</span><span class="sxs-lookup"><span data-stu-id="3d8d9-109">Prefer InkEdit Control</span></span>

<span data-ttu-id="3d8d9-110">[InkEdit](inkedit-control-reference.md) es el control preferido al que adjuntar el objeto [**PenInputPanel**](peninputpanel-class.md) .</span><span class="sxs-lookup"><span data-stu-id="3d8d9-110">[InkEdit](inkedit-control-reference.md) is the preferred control to which to attach the [**PenInputPanel**](peninputpanel-class.md) object.</span></span> <span data-ttu-id="3d8d9-111">El control InkEdit proporciona compatibilidad con el [marco de trabajo de servicios de texto (TSF)](text-services-framework.md).</span><span class="sxs-lookup"><span data-stu-id="3d8d9-111">The InkEdit control provides support for the [Text Services Framework (TSF)](text-services-framework.md).</span></span>

## <a name="disable-ink-mode-on-inkedit-controls"></a><span data-ttu-id="3d8d9-112">Deshabilitar el modo de tinta en los controles InkEdit</span><span class="sxs-lookup"><span data-stu-id="3d8d9-112">Disable Ink Mode on InkEdit Controls</span></span>

<span data-ttu-id="3d8d9-113">Cuando se asocia a un control [InkEdit](inkedit-control-reference.md) , establezca la propiedad [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) del control InkEdit en el valor [**InkMode**](/windows/desktop/api/inked/ne-inked-inkmode) .</span><span class="sxs-lookup"><span data-stu-id="3d8d9-113">When attached to an [InkEdit](inkedit-control-reference.md) control, set the [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) property of the InkEdit control to the [**InkMode**](/windows/desktop/api/inked/ne-inked-inkmode) value.</span></span> <span data-ttu-id="3d8d9-114">Si la propiedad **InkMode** no se establece en el valor **InkMode** , el control InkEdit interpreta el primer punteo como un trazo, lo pasa al reconocedor e inserta el texto en el control InkEdit.</span><span class="sxs-lookup"><span data-stu-id="3d8d9-114">If the **InkMode** property is not set to the **InkMode** value, the InkEdit control interprets the first tap as a stroke, passes it to the recognizer, and inserts the text in the InkEdit control.</span></span> <span data-ttu-id="3d8d9-115">Puesto que ya tiene un objeto [**PenInputPanel**](peninputpanel-class.md) asociado para aceptar la entrada de lápiz, no es necesario que el control InkEdit también esté habilitado para la entrada de lápiz.</span><span class="sxs-lookup"><span data-stu-id="3d8d9-115">Since you already have a [**PenInputPanel**](peninputpanel-class.md) object attached to accept ink input, there is no need to have the InkEdit control also enabled for ink input.</span></span>

## <a name="using-windowless-controls"></a><span data-ttu-id="3d8d9-116">Usar controles sin ventana</span><span class="sxs-lookup"><span data-stu-id="3d8d9-116">Using Windowless Controls</span></span>

<span data-ttu-id="3d8d9-117">Cuando un objeto [**PenInputPanel**](peninputpanel-class.md) se adjunta a una ventana primaria que contiene más de un control sin ventana, el objeto **PenInputPanel** no sabe cómo realizar un seguimiento del símbolo de intercalación a medida que el foco se mueve entre los elementos secundarios sin ventanas.</span><span class="sxs-lookup"><span data-stu-id="3d8d9-117">When a [**PenInputPanel**](peninputpanel-class.md) object is attached to a parent window that contains more than one windowless control, the **PenInputPanel** object does not know how to track the caret as focus moves among windowless children.</span></span> <span data-ttu-id="3d8d9-118">La entrada de escritura a mano se puede enviar a un elemento secundario incorrecto cuando el foco se mueve de un control sin ventana a otro mientras está pendiente la entrada.</span><span class="sxs-lookup"><span data-stu-id="3d8d9-118">Handwriting input can be sent to the wrong child when focus moves from one windowless control to another while input is pending.</span></span>

<span data-ttu-id="3d8d9-119">Para usar el objeto [**PenInputPanel**](peninputpanel-class.md) en un entorno sin ventanas, se puede usar la técnica siguiente:</span><span class="sxs-lookup"><span data-stu-id="3d8d9-119">To use the [**PenInputPanel**](peninputpanel-class.md) object in a windowless environment, the following technique can be used:</span></span>

1.  <span data-ttu-id="3d8d9-120">Cree una instancia de un control [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) y colóquelo sobre el control sin ventana.</span><span class="sxs-lookup"><span data-stu-id="3d8d9-120">Instantiate a [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) control and position it over the windowless control.</span></span>
2.  <span data-ttu-id="3d8d9-121">Adjunte el objeto [**PenInputPanel**](peninputpanel-class.md) al nuevo control cuadro de texto.</span><span class="sxs-lookup"><span data-stu-id="3d8d9-121">Attach the [**PenInputPanel**](peninputpanel-class.md) object to the new text box control.</span></span>
3.  <span data-ttu-id="3d8d9-122">Permita que el control de cuadro de texto recopile el texto reconocido del objeto [**PenInputPanel**](peninputpanel-class.md) .</span><span class="sxs-lookup"><span data-stu-id="3d8d9-122">Let the text box control collect the recognized text from the [**PenInputPanel**](peninputpanel-class.md) object.</span></span>
4.  <span data-ttu-id="3d8d9-123">Cuando el foco cambie fuera del control cuadro de texto, llame al método [**CommitPendingInput**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-commitpendinginput) del objeto [**PenInputPanel**](peninputpanel-class.md) .</span><span class="sxs-lookup"><span data-stu-id="3d8d9-123">When focus changes away from the text box control, call the [**CommitPendingInput**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-commitpendinginput) method of the [**PenInputPanel**](peninputpanel-class.md) object.</span></span>
5.  <span data-ttu-id="3d8d9-124">Copie el texto reconocido del control de cuadro de texto en el elemento secundario sin ventanas.</span><span class="sxs-lookup"><span data-stu-id="3d8d9-124">Copy the recognized text from the text box control to the windowless child.</span></span>
6.  <span data-ttu-id="3d8d9-125">Desasocie el objeto [**PenInputPanel**](peninputpanel-class.md) estableciendo su propiedad [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) (solo código administrado) o [**AttachedEditWindow**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_attachededitwindow) en NULL.</span><span class="sxs-lookup"><span data-stu-id="3d8d9-125">Detach the [**PenInputPanel**](peninputpanel-class.md) object by setting its [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) (managed code only) property or [**AttachedEditWindow**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_attachededitwindow) property to null.</span></span>
7.  <span data-ttu-id="3d8d9-126">Destruya el control cuadro de texto.</span><span class="sxs-lookup"><span data-stu-id="3d8d9-126">Destroy the text box control.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3d8d9-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3d8d9-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d8d9-128">**Clase PenInputPanel**</span><span class="sxs-lookup"><span data-stu-id="3d8d9-128">**PenInputPanel Class**</span></span>](peninputpanel-class.md)
</dt> <dt>

<span data-ttu-id="3d8d9-129">[Microsoft. Ink. PenInputPanel](/previous-versions/ms583923(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="3d8d9-129">[Microsoft.Ink.PenInputPanel](/previous-versions/ms583923(v=vs.100))</span></span>
</dt> <dt>

[<span data-ttu-id="3d8d9-130">Text Services Framework (TSF)</span><span class="sxs-lookup"><span data-stu-id="3d8d9-130">Text Services Framework</span></span>](../tsf/text-services-framework.md)
</dt> </dl>

 

 
