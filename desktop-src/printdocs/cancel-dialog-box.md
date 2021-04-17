---
description: En este tema se describe cómo mostrar el progreso del trabajo de impresión al usuario y cómo concederles la opción de cancelar un trabajo de impresión que está actualmente en curso.
ms.assetid: 2b7a0ab7-bf7e-473d-ab43-8b79478d4453
title: 'Cómo: mostrar el progreso del trabajo de impresión'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9effc778f6affaba5b53cbd96a7a428ea5554d8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677787"
---
# <a name="how-to-display-the-print-job-progress"></a><span data-ttu-id="c146c-103">Cómo: mostrar el progreso del trabajo de impresión</span><span class="sxs-lookup"><span data-stu-id="c146c-103">How To: Display the Print Job Progress</span></span>

<span data-ttu-id="c146c-104">En este tema se describe cómo mostrar el progreso del trabajo de impresión al usuario y cómo concederles la opción de cancelar un trabajo de impresión que está actualmente en curso.</span><span class="sxs-lookup"><span data-stu-id="c146c-104">This topic describes how to display the print job progress to the user and give them the option to cancel a print job that is currently in progress.</span></span>

## <a name="overview"></a><span data-ttu-id="c146c-105">Información general</span><span class="sxs-lookup"><span data-stu-id="c146c-105">Overview</span></span>

<span data-ttu-id="c146c-106">Un procedimiento de cuadro de diálogo de progreso de impresión normalmente realiza las siguientes funciones.</span><span class="sxs-lookup"><span data-stu-id="c146c-106">A print progress dialog procedure typically performs the following functions.</span></span>

-   <span data-ttu-id="c146c-107">Muestra el progreso del trabajo de impresión al usuario.</span><span class="sxs-lookup"><span data-stu-id="c146c-107">Display print job progress to the user.</span></span>
-   <span data-ttu-id="c146c-108">Inicie el subproceso de procesamiento de impresión.</span><span class="sxs-lookup"><span data-stu-id="c146c-108">Start the print processing thread.</span></span>
-   <span data-ttu-id="c146c-109">Mostrar un botón **Cancelar** para que el usuario pueda detener un trabajo de impresión antes de que finalice.</span><span class="sxs-lookup"><span data-stu-id="c146c-109">Display a **Cancel** button so the user can stop a print job before it finishes.</span></span>

<span data-ttu-id="c146c-110">En realidad, lo único que debe hacer el procedimiento del cuadro de diálogo progreso de la impresión es mostrar el progreso del trabajo de impresión al usuario.</span><span class="sxs-lookup"><span data-stu-id="c146c-110">Strictly speaking, the only thing that the print progress dialog box procedure must do is display the print job progress to the user.</span></span> <span data-ttu-id="c146c-111">Sin embargo, dado que las otras dos funciones de la lista anterior están estrechamente relacionadas, también se han incluido en este módulo.</span><span class="sxs-lookup"><span data-stu-id="c146c-111">However, because the other two functions in the preceding list are closely related, they have also been included in this module.</span></span>

## <a name="displaying-print-job-progress"></a><span data-ttu-id="c146c-112">Mostrar el progreso del trabajo de impresión</span><span class="sxs-lookup"><span data-stu-id="c146c-112">Displaying Print Job Progress</span></span>

<span data-ttu-id="c146c-113">Un procedimiento de cuadro de diálogo de progreso de impresión controla los siguientes mensajes de ventana.</span><span class="sxs-lookup"><span data-stu-id="c146c-113">A print progress dialog box procedure handles the following window messages.</span></span>

-   <span data-ttu-id="c146c-114">**INITDIALOG de WM \_**</span><span class="sxs-lookup"><span data-stu-id="c146c-114">**WM\_INITDIALOG**</span></span>

    <span data-ttu-id="c146c-115">Inicializa los controles que usa el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c146c-115">Initializes the controls that the dialog box uses.</span></span>

-   <span data-ttu-id="c146c-116">**SETCURSOR de WM \_**</span><span class="sxs-lookup"><span data-stu-id="c146c-116">**WM\_SETCURSOR**</span></span>

    <span data-ttu-id="c146c-117">Establece el cursor en un puntero cuando el usuario puede cancelar un trabajo de impresión y en el cursor de espera cuando el trabajo de impresión se encuentra en un punto en el que no se puede cancelar.</span><span class="sxs-lookup"><span data-stu-id="c146c-117">Sets the cursor to a pointer when the user is able to cancel a print job, and to the wait cursor when the print job is at a point where it cannot be cancelled.</span></span>

-   <span data-ttu-id="c146c-118">**\_impresión de \_ Inicio \_ de impresión de usuario**</span><span class="sxs-lookup"><span data-stu-id="c146c-118">**USER\_PRINT\_START\_PRINTING**</span></span>

    <span data-ttu-id="c146c-119">Establece los parámetros de la barra de progreso para el trabajo de impresión y crea el subproceso de impresión para empezar a procesar el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="c146c-119">Sets the progress bar parameters for the print job, and creates the printing thread to start processing the print job.</span></span>

    <span data-ttu-id="c146c-120">Se trata de un mensaje de ventana específico de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c146c-120">This is an application-specific window message.</span></span>

-   <span data-ttu-id="c146c-121">**\_comando de WM-IDCANCEL**</span><span class="sxs-lookup"><span data-stu-id="c146c-121">**WM\_COMMAND - IDCANCEL**</span></span>

    <span data-ttu-id="c146c-122">Establece el evento CANCEL para indicar al subproceso de procesamiento de impresión que cancele el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="c146c-122">Sets the cancel event to tell the print processing thread to cancel the print job.</span></span>

-   <span data-ttu-id="c146c-123">**\_actualización de \_ Estado de impresión de usuario \_**</span><span class="sxs-lookup"><span data-stu-id="c146c-123">**USER\_PRINT\_STATUS\_UPDATE**</span></span>

    <span data-ttu-id="c146c-124">Actualiza la barra de progreso y el texto de estado para mostrar el estado actual del trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="c146c-124">Updates the progress bar and status text to show the current state of the print job.</span></span>

    <span data-ttu-id="c146c-125">Se trata de un mensaje de ventana específico de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c146c-125">This is an application-specific window message.</span></span>

-   <span data-ttu-id="c146c-126">**\_cierre de impresión del usuario \_**</span><span class="sxs-lookup"><span data-stu-id="c146c-126">**USER\_PRINT\_CLOSING**</span></span>

    <span data-ttu-id="c146c-127">Establece el texto de estado de cierre en el cuadro de diálogo de progreso para indicar que el trabajo de impresión se está cerrando.</span><span class="sxs-lookup"><span data-stu-id="c146c-127">Sets the closing status text in the progress dialog box to indicate that the print job is closing.</span></span>

    <span data-ttu-id="c146c-128">Se trata de un mensaje de ventana específico de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c146c-128">This is an application-specific window message.</span></span>

-   <span data-ttu-id="c146c-129">**impresión de usuario \_ \_ completada**</span><span class="sxs-lookup"><span data-stu-id="c146c-129">**USER\_PRINT\_COMPLETE**</span></span>

    <span data-ttu-id="c146c-130">Muestra el mensaje "trabajo de impresión completado" al usuario y libera los identificadores y eventos utilizados en este trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="c146c-130">Displays the "Print job complete" message to the user, and releases handles and events that were used in this print job.</span></span>

    <span data-ttu-id="c146c-131">Se trata de un mensaje de ventana específico de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c146c-131">This is an application-specific window message.</span></span>

 

 



