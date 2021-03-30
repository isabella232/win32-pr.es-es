---
description: El control InkEdit proporciona una manera fácil de capturar, reconocer y mostrar la entrada de lápiz.
ms.assetid: a1dfa254-cade-44c5-8fdd-74bb40849063
title: Control InkEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf6d5441506ee791eefddba05b9b1f3ddb8a8ec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910757"
---
# <a name="inkedit-control"></a><span data-ttu-id="34882-103">Control InkEdit</span><span class="sxs-lookup"><span data-stu-id="34882-103">InkEdit Control</span></span>

<span data-ttu-id="34882-104">El control [InkEdit](inkedit-control-reference.md) proporciona una manera fácil de capturar, reconocer y mostrar la entrada de lápiz.</span><span class="sxs-lookup"><span data-stu-id="34882-104">The [InkEdit](inkedit-control-reference.md) control provides an easy way to capture, recognize, and display ink.</span></span>

<span data-ttu-id="34882-105">Esta implementación del control [InkEdit](inkedit-control-reference.md) se basa en el control [**RichEdit**](/windows/desktop/api/richole/nn-richole-iricheditole) .</span><span class="sxs-lookup"><span data-stu-id="34882-105">This implementation of the [InkEdit](inkedit-control-reference.md) control is based on the [**RichEdit**](/windows/desktop/api/richole/nn-richole-iricheditole) control.</span></span> <span data-ttu-id="34882-106">La implementación administrada (.NET Framework) de [InkEdit](/previous-versions/ms835842(v=msdn.10)) se basa en el control [**RichTextBox**](/previous-versions/windows/) .</span><span class="sxs-lookup"><span data-stu-id="34882-106">The managed (.NET Framework) implementation of [InkEdit](/previous-versions/ms835842(v=msdn.10)) is based on the [**RichTextBox**](/previous-versions/windows/) control.</span></span>

<span data-ttu-id="34882-107">El propósito principal del control [InkEdit](inkedit-control-reference.md) es recopilar la tinta, reconocerla y mostrarla en forma de texto.</span><span class="sxs-lookup"><span data-stu-id="34882-107">The primary purpose of the [InkEdit](inkedit-control-reference.md) control is to collect ink, recognize it, and display it in text form.</span></span> <span data-ttu-id="34882-108">Además, permite mostrar la entrada de lápiz como un objeto incrustado con capacidades de formato de texto, como negrita y subrayado.</span><span class="sxs-lookup"><span data-stu-id="34882-108">Additionally, it supports displaying ink as an embedded object with text formatting capabilities, such as bold and underline.</span></span>

## <a name="gestures-and-correction"></a><span data-ttu-id="34882-109">Gestos y corrección</span><span class="sxs-lookup"><span data-stu-id="34882-109">Gestures and Correction</span></span>

<span data-ttu-id="34882-110">[InkEdit](inkedit-control-reference.md) admite los siguientes gestos.</span><span class="sxs-lookup"><span data-stu-id="34882-110">[InkEdit](inkedit-control-reference.md) supports the following gestures.</span></span>



| <span data-ttu-id="34882-111">Gesto</span><span class="sxs-lookup"><span data-stu-id="34882-111">Gesture</span></span>                                                                    | <span data-ttu-id="34882-112">Nombre del gesto</span><span class="sxs-lookup"><span data-stu-id="34882-112">Gesture Name</span></span>              | <span data-ttu-id="34882-113">Acción</span><span class="sxs-lookup"><span data-stu-id="34882-113">Action</span></span>               |
|----------------------------------------------------------------------------|---------------------------|----------------------|
| ![gesto de abajo a la izquierda](images/d8b00c0a-f450-4f71-980f-3bca1b558e4c.gif)      | <span data-ttu-id="34882-115">Inferior izquierda</span><span class="sxs-lookup"><span data-stu-id="34882-115">Down-left</span></span><br/>      | <span data-ttu-id="34882-116">Entrar</span><span class="sxs-lookup"><span data-stu-id="34882-116">Enter</span></span><br/>     |
| ![gesto hacia abajo-izquierda-largo](images/b8cb23b5-b947-477d-922f-2ffb42756804.gif) | <span data-ttu-id="34882-118">Abajo-izquierda-largo</span><span class="sxs-lookup"><span data-stu-id="34882-118">Down-left-long</span></span><br/> | <span data-ttu-id="34882-119">Entrar</span><span class="sxs-lookup"><span data-stu-id="34882-119">Enter</span></span><br/>     |
| ![gesto de arriba a la derecha](images/02c34d24-c2d7-404f-b99a-742ba6de7f0c.gif)       | <span data-ttu-id="34882-121">Arriba a la derecha</span><span class="sxs-lookup"><span data-stu-id="34882-121">Up-right</span></span><br/>       | <span data-ttu-id="34882-122">Pestaña</span><span class="sxs-lookup"><span data-stu-id="34882-122">Tab</span></span><br/>       |
| ![gesto de arriba a la derecha.](images/5e3522d3-2920-4a86-86ae-f29b01d93993.gif) | <span data-ttu-id="34882-124">Arriba-a la derecha</span><span class="sxs-lookup"><span data-stu-id="34882-124">Up-right-long</span></span><br/>  | <span data-ttu-id="34882-125">Pestaña</span><span class="sxs-lookup"><span data-stu-id="34882-125">Tab</span></span><br/>       |
| ![gesto derecho](images/864cf4e1-2619-49cf-ac96-72994232e465.jpg)          | <span data-ttu-id="34882-127">Right</span><span class="sxs-lookup"><span data-stu-id="34882-127">Right</span></span><br/>          | <span data-ttu-id="34882-128">Space</span><span class="sxs-lookup"><span data-stu-id="34882-128">Space</span></span><br/>     |
| ![gesto izquierdo](images/ce60cc20-1769-428d-80de-7f47c86021fb.jpg)           | <span data-ttu-id="34882-130">Left</span><span class="sxs-lookup"><span data-stu-id="34882-130">Left</span></span><br/>           | <span data-ttu-id="34882-131">Retroceso</span><span class="sxs-lookup"><span data-stu-id="34882-131">Backspace</span></span><br/> |



 

<span data-ttu-id="34882-132">Los eventos de gestos que puede controlar contienen información de movimiento, trazo y cursor que puede usar para enviar texto a [InkEdit](inkedit-control-reference.md) o colocar datos en el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="34882-132">Gesture events that you can handle contain gesture, stroke, and cursor information you can use to send text to [InkEdit](inkedit-control-reference.md) or place data on the clipboard.</span></span>

<span data-ttu-id="34882-133">[InkEdit](inkedit-control-reference.md) también proporciona una interfaz de usuario de corrección que permite a los usuarios ver y seleccionar alternativas, usar el teclado en pantalla y reconocedores de caracteres, letras y bloques.</span><span class="sxs-lookup"><span data-stu-id="34882-133">[InkEdit](inkedit-control-reference.md) also provides a correction user interface that enables users to view and select from alternates, use the on-screen keyboard, and character/letter/block recognizers.</span></span>

## <a name="other-details"></a><span data-ttu-id="34882-134">Otros detalles</span><span class="sxs-lookup"><span data-stu-id="34882-134">Other Details</span></span>

<span data-ttu-id="34882-135">[InkEdit](inkedit-control-reference.md) está diseñado para funcionar bien en un escenario de formulario para una sola línea, así como para la entrada y edición de texto de varias líneas.</span><span class="sxs-lookup"><span data-stu-id="34882-135">[InkEdit](inkedit-control-reference.md) is designed to work well in a form scenario for single line as well as multiline text entry and editing.</span></span> <span data-ttu-id="34882-136">El uso previsto principal de InkEdit es obtener la entrada de texto de un usuario en forma de escritura a mano.</span><span class="sxs-lookup"><span data-stu-id="34882-136">The primary intended use for InkEdit is to get text input from a user in the form of handwriting.</span></span> <span data-ttu-id="34882-137">De forma predeterminada, se reconoce la entrada manuscrita y el texto se inserta en su lugar.</span><span class="sxs-lookup"><span data-stu-id="34882-137">By default, ink input is recognized and text is inserted in its place.</span></span> <span data-ttu-id="34882-138">La interfaz de usuario predeterminada para InkEdit es similar a la del control [**RichTextBox**](/previous-versions/windows/) , excepto cuando el usuario está poniendo la tinta.</span><span class="sxs-lookup"><span data-stu-id="34882-138">The default user interface for InkEdit resembles that of the [**RichTextBox**](/previous-versions/windows/) control, except when the user is laying down ink.</span></span> <span data-ttu-id="34882-139">Puede mostrar la entrada de lápiz original en lugar de texto; sin embargo, la tinta se escala hasta el tamaño de la fuente de entrada actual del control InkEdit y se muestra en línea con otro texto.</span><span class="sxs-lookup"><span data-stu-id="34882-139">You can display original ink rather than text; however, the ink is scaled to the current input font size of the InkEdit control and is displayed inline with other text.</span></span>

> [!Note]  
> <span data-ttu-id="34882-140">Por motivos de seguridad, debe utilizar los procedimientos estándar para abrir o cerrar un archivo, transmitir la entrada/salida y establecer la propiedad [**RTF**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selrtf) o [**Text**](/windows/desktop/api/inked/nf-inked-iinkedit-get_seltext) .</span><span class="sxs-lookup"><span data-stu-id="34882-140">For security reasons, you must use standard procedures to open or close a file, stream the input/output, and set the [**RTF**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selrtf) or [**Text**](/windows/desktop/api/inked/nf-inked-iinkedit-get_seltext) property.</span></span>

 

<span data-ttu-id="34882-141">El control [InkEdit](inkedit-control-reference.md) se establece para que reconozca la entrada de lápiz como texto de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="34882-141">The [InkEdit](inkedit-control-reference.md) control is set to recognize ink as text by default.</span></span> <span data-ttu-id="34882-142">Para permitir que los usuarios agreguen tinta como tinta, establezca la propiedad [**InkInsertMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkinsertmode) en **InsertAsInk**.</span><span class="sxs-lookup"><span data-stu-id="34882-142">To enable users to add ink as ink, set the [**InkInsertMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkinsertmode) property to **InsertAsInk**.</span></span>

<span data-ttu-id="34882-143">Para obtener información de referencia detallada sobre el control [InkEdit](inkedit-control-reference.md) , vea InkEdit.</span><span class="sxs-lookup"><span data-stu-id="34882-143">For detailed reference information about the [InkEdit](inkedit-control-reference.md) control, see InkEdit.</span></span>

> [!Note]  
> <span data-ttu-id="34882-144">Si usa el control Win32 [InkEdit](inkedit-control-reference.md) y lo coloca dentro de un cuadro de grupo, asegúrese de que el cuadro tiene un estilo transparente. de lo contrario, InkEdit no puede recopilar entradas manuscritas.</span><span class="sxs-lookup"><span data-stu-id="34882-144">If you use the Win32 [InkEdit](inkedit-control-reference.md) control and place it inside a group box, make sure the box has a transparent style; otherwise, InkEdit is not able to collect ink.</span></span>

 

> [!Note]  
> <span data-ttu-id="34882-145">Para asegurarse de que la tinta se muestra correctamente, llame al método de [**actualización**](/windows/desktop/api/inked/nf-inked-iinkedit-refresh) del control [InkEdit](inkedit-control-reference.md) cuando reciba un evento [**HScroll**](/dotnet/api/system.windows.forms.richtextbox.hscroll?view=netcore-3.1) o [**VScroll**](/dotnet/api/system.windows.forms.richtextbox.vscroll?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="34882-145">To ensure ink is displayed properly, call the [InkEdit](inkedit-control-reference.md) control [**Refresh**](/windows/desktop/api/inked/nf-inked-iinkedit-refresh) method when it receives an [**HScroll**](/dotnet/api/system.windows.forms.richtextbox.hscroll?view=netcore-3.1) or [**VScroll**](/dotnet/api/system.windows.forms.richtextbox.vscroll?view=netcore-3.1) event.</span></span>

 

<span data-ttu-id="34882-146">En las secciones siguientes se detalla el uso del control [InkEdit](inkedit-control-reference.md) :</span><span class="sxs-lookup"><span data-stu-id="34882-146">The following sections detail the use of the [InkEdit](inkedit-control-reference.md) control:</span></span>

-   [<span data-ttu-id="34882-147">Crear instancias de InkEdit</span><span class="sxs-lookup"><span data-stu-id="34882-147">Instantiating InkEdit</span></span>](instantiating-inkedit.md)
-   [<span data-ttu-id="34882-148">Diferencias entre Word y el reconocimiento de caracteres</span><span class="sxs-lookup"><span data-stu-id="34882-148">Word vs. Character Recognition</span></span>](word-vs--character-recognition.md)
-   [<span data-ttu-id="34882-149">Mostrar la entrada de lápiz como entrada de lápiz</span><span class="sxs-lookup"><span data-stu-id="34882-149">Displaying Ink as Ink</span></span>](displaying-ink-as-ink.md)
-   [<span data-ttu-id="34882-150">Usar InkEdit en versiones anteriores de Windows</span><span class="sxs-lookup"><span data-stu-id="34882-150">Using InkEdit on Earlier Versions of Windows</span></span>](using-inkedit-on-earlier-versions-of-windows.md)
-   [<span data-ttu-id="34882-151">Uso de un diccionario de aplicación con InkEdit</span><span class="sxs-lookup"><span data-stu-id="34882-151">Using an Application Dictionary with InkEdit</span></span>](using-an-application-dictionary-with-inkedit.md)

 

