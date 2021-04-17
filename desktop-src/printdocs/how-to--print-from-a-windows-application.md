---
description: En esta sección se describe cómo imprimir desde un programa de Windows nativo.
ms.assetid: D0AE8FF8-D02D-43D3-80CA-E13EAA894F87
title: 'Cómo: imprimir desde un programa de Windows'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84229823944d7f7104da359b953e579f1b21cdca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697694"
---
# <a name="how-to-print-from-a-windows-program"></a><span data-ttu-id="ad0f8-103">Cómo: imprimir desde un programa de Windows</span><span class="sxs-lookup"><span data-stu-id="ad0f8-103">How To: Print from a Windows Program</span></span>

<span data-ttu-id="ad0f8-104">En esta sección se describe cómo imprimir desde un programa de Windows nativo.</span><span class="sxs-lookup"><span data-stu-id="ad0f8-104">This section describes how to print from a native Windows program.</span></span>

## <a name="overview"></a><span data-ttu-id="ad0f8-105">Información general</span><span class="sxs-lookup"><span data-stu-id="ad0f8-105">Overview</span></span>

<span data-ttu-id="ad0f8-106">La impresión suele ser una parte integral de un programa de Windows nativo.</span><span class="sxs-lookup"><span data-stu-id="ad0f8-106">Printing is usually an integral part of a native Windows program.</span></span> <span data-ttu-id="ad0f8-107">Por lo tanto, no es una característica que se puede agregar fácilmente después de haber escrito el programa.</span><span class="sxs-lookup"><span data-stu-id="ad0f8-107">Therefore, it is not a feature that you can add easily after you have written the program.</span></span> <span data-ttu-id="ad0f8-108">Dicho esto, si el programa está diseñado para usar documentos XPS, no necesitará mucho, si lo hay, código adicional para representar el contenido del documento para imprimirlo.</span><span class="sxs-lookup"><span data-stu-id="ad0f8-108">That being said, if the program is designed to use XPS documents it will not need much, if any, additional code to render the document content for printing.</span></span> <span data-ttu-id="ad0f8-109">Los documentos XPS de la aplicación se pueden enviar directamente a una impresora que tenga un controlador de impresora XPSDrv.</span><span class="sxs-lookup"><span data-stu-id="ad0f8-109">The XPS documents of the application can be sent directly to a printer that has an XPSDrv printer driver.</span></span>

<span data-ttu-id="ad0f8-110">Use la [API de documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)) para crear el contenido del documento y la [API de impresión XPS](xps-printing.md) para enviar el contenido del documento a la impresora.</span><span class="sxs-lookup"><span data-stu-id="ad0f8-110">Use the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)) to create the document content and the [XPS Print API](xps-printing.md) to send the document content to the printer.</span></span> <span data-ttu-id="ad0f8-111">La API de impresión XPS procesa el contenido del documento para la impresora de destino.</span><span class="sxs-lookup"><span data-stu-id="ad0f8-111">The XPS Print API processes the document content for the destination printer.</span></span> <span data-ttu-id="ad0f8-112">Si la impresora seleccionada tiene un controlador de impresora XPSDrv, el documento se enviará a la impresora sin ninguna conversión adicional.</span><span class="sxs-lookup"><span data-stu-id="ad0f8-112">If the selected printer has an XPSDrv printer driver, the document will be sent to the printer without any additional conversion.</span></span> <span data-ttu-id="ad0f8-113">Si la impresora seleccionada tiene un controlador de impresora basado en GDI, el programa también puede enviar el contenido a la impresora y la API de impresión XPS convierte el contenido del documento para que sea compatible con el controlador de impresora basado en GDI.</span><span class="sxs-lookup"><span data-stu-id="ad0f8-113">If the selected printer has a GDI-based printer driver, the program can also send the content to the printer, and the XPS Print API converts the document content so that it will be compatible with the GDI-based printer driver.</span></span> <span data-ttu-id="ad0f8-114">En cualquier caso, el procesamiento que realiza la aplicación es el mismo.</span><span class="sxs-lookup"><span data-stu-id="ad0f8-114">In either case, the processing that the application performs is the same.</span></span>

## <a name="printing-tasks"></a><span data-ttu-id="ad0f8-115">Tareas de impresión</span><span class="sxs-lookup"><span data-stu-id="ad0f8-115">Printing tasks</span></span>

<span data-ttu-id="ad0f8-116">En los temas siguientes se describen los pasos básicos para imprimir el contenido del programa.</span><span class="sxs-lookup"><span data-stu-id="ad0f8-116">The following topics describe the basic steps of printing program content.</span></span>

1.  <span data-ttu-id="ad0f8-117">**Recopilar información del trabajo de impresión del usuario.**</span><span class="sxs-lookup"><span data-stu-id="ad0f8-117">**Collect print job information from user.**</span></span>

    <span data-ttu-id="ad0f8-118">Normalmente, un usuario inicia un trabajo de impresión cuando selecciona la opción Imprimir en un menú y el programa muestra un cuadro de diálogo Imprimir para recopilar los detalles del trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="ad0f8-118">Typically, a user initiates a print job when they select the print option from a menu and the program displays a print dialog box to collect the details of the print job.</span></span> <span data-ttu-id="ad0f8-119">Normalmente, el usuario selecciona la impresora, el número de copias y los detalles de configuración de la impresora, como la impresión a dos caras y el grapado.</span><span class="sxs-lookup"><span data-stu-id="ad0f8-119">The user typically selects the printer, the number of copies, and printer configuration details such as two-sided printing and stapling.</span></span>

    <span data-ttu-id="ad0f8-120">Para obtener información sobre cómo hacerlo, consulte [Cómo: recopilar información del trabajo de impresión del usuario](preparing-to-print.md).</span><span class="sxs-lookup"><span data-stu-id="ad0f8-120">For information about how to do this, see [How To: Collect Print Job Information from the User](preparing-to-print.md).</span></span>

2.  <span data-ttu-id="ad0f8-121">**Cree el indicador de progreso.**</span><span class="sxs-lookup"><span data-stu-id="ad0f8-121">**Create progress indicator.**</span></span>

    <span data-ttu-id="ad0f8-122">Un indicador de progreso proporciona al usuario comentarios sobre cómo progresa el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="ad0f8-122">A progress indicator provides the user with feedback about how the print job is progressing.</span></span> <span data-ttu-id="ad0f8-123">El indicador de progreso puede ser una barra de progreso que forma parte de un cuadro de diálogo que incluye el botón **Cancelar** del trabajo, o bien una barra de progreso en la barra de estado en la parte inferior de la ventana principal.</span><span class="sxs-lookup"><span data-stu-id="ad0f8-123">The progress indicator can be a progress bar that is part of a dialog box that includes the **Cancel** button for the job, or it can be a progress bar in the status bar at the bottom of the main window.</span></span>

    <span data-ttu-id="ad0f8-124">Para obtener información acerca del funcionamiento del indicador de progreso, vea [Cómo: mostrar el progreso del trabajo de impresión](cancel-dialog-box.md).</span><span class="sxs-lookup"><span data-stu-id="ad0f8-124">For information about the progress indicator works, see [How To: Display the Print Job Progress](cancel-dialog-box.md).</span></span>

    <span data-ttu-id="ad0f8-125">Para obtener más ideas sobre cómo mostrar el progreso del trabajo de impresión, consulte la información de las instrucciones de desarrollo de la interfaz de usuario de la [aplicación Windows](/windows/desktop/windows-application-ui-development) .</span><span class="sxs-lookup"><span data-stu-id="ad0f8-125">For more ideas about how to display the progress of the print job, see the information in the [Windows Application UI Development](/windows/desktop/windows-application-ui-development) guidelines.</span></span>

3.  <span data-ttu-id="ad0f8-126">**Inicie el subproceso de impresión.**</span><span class="sxs-lookup"><span data-stu-id="ad0f8-126">**Start the printing thread.**</span></span>

    <span data-ttu-id="ad0f8-127">Una vez que el programa ha recopilado la información del trabajo de impresión del usuario, puede iniciar el subproceso de impresión para realizar el procesamiento real del documento para imprimirlo.</span><span class="sxs-lookup"><span data-stu-id="ad0f8-127">After the program has collected the print job information from the user, it can start the printing thread to perform the actual processing of the document for printing.</span></span>

    <span data-ttu-id="ad0f8-128">Para obtener información sobre el subproceso de impresión, consulte [Cómo: iniciar y detener un subproceso de impresión](how-to--start-and-stop-a-printing-thread.md).</span><span class="sxs-lookup"><span data-stu-id="ad0f8-128">For information about the printing thread, see [How To: Start and Stop a Printing Thread](how-to--start-and-stop-a-printing-thread.md).</span></span>

4.  <span data-ttu-id="ad0f8-129">**Representan los datos del trabajo de impresión.**</span><span class="sxs-lookup"><span data-stu-id="ad0f8-129">**Render print job data.**</span></span>

    <span data-ttu-id="ad0f8-130">El subproceso de impresión representa los datos del documento para imprimirlos.</span><span class="sxs-lookup"><span data-stu-id="ad0f8-130">The printing thread renders the document data for printing.</span></span> <span data-ttu-id="ad0f8-131">Debe dividir este procesamiento en pasos de procesamiento discretos para que el usuario pueda interrumpir el procesamiento y cancelar el trabajo, así como no permitir que el subproceso de procesamiento bloquee otros subprocesos y procesos.</span><span class="sxs-lookup"><span data-stu-id="ad0f8-131">You should break down this processing into discrete processing steps so that the user can interrupt the processing and cancel the job as well as to not allow the processing thread to block other threads and processes.</span></span>

    <span data-ttu-id="ad0f8-132">Para obtener información sobre cómo representa los datos del trabajo de impresión, vea [Cómo: representar datos de trabajos de impresión](how-to--render-the-print-job-data.md).</span><span class="sxs-lookup"><span data-stu-id="ad0f8-132">For information about how the renders the print job data, see [How To: Render Print Job Data](how-to--render-the-print-job-data.md).</span></span>

5.  <span data-ttu-id="ad0f8-133">**Supervise el progreso del trabajo de impresión.**</span><span class="sxs-lookup"><span data-stu-id="ad0f8-133">**Monitor print job progress.**</span></span>

    <span data-ttu-id="ad0f8-134">Cuando se realice cada paso de procesamiento, actualice la barra de progreso para informar del uso.</span><span class="sxs-lookup"><span data-stu-id="ad0f8-134">As each processing step is performed, update the progress bar to inform the use.</span></span> <span data-ttu-id="ad0f8-135">Calcule los pasos de procesamiento para completar el trabajo solicitado y, a continuación, actualice la barra de progreso a medida que se realicen los pasos.</span><span class="sxs-lookup"><span data-stu-id="ad0f8-135">Compute the processing steps to complete the requested job and then updates the progress bar as those steps are performed.</span></span>

6.  <span data-ttu-id="ad0f8-136">**Cierre el trabajo de impresión y termine el subproceso de impresión.**</span><span class="sxs-lookup"><span data-stu-id="ad0f8-136">**Close print job and terminate printing thread.**</span></span>

    <span data-ttu-id="ad0f8-137">Una vez que el programa ha enviado el trabajo de impresión a la impresora, o si el usuario ha cancelado el trabajo de impresión, debe cerrar el trabajo de impresión y liberar los recursos utilizados por el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="ad0f8-137">After the program has sent the print job to the printer, or if the user has cancelled the print job, you must close the print job and release the resources used by the print job.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ad0f8-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ad0f8-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad0f8-139">Cómo: recopilar información del trabajo de impresión del usuario</span><span class="sxs-lookup"><span data-stu-id="ad0f8-139">How To: Collect Print Job Information from the User</span></span>](preparing-to-print.md)
</dt> </dl>

 

 
