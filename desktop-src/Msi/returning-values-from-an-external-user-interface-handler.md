---
description: Un controlador de interfaz de usuario (IU) externo puede devolver cualquier número de valores para Windows Installer en función del tipo de botón proporcionado en el parámetro de tipo de mensaje que el instalador pasa al controlador.
ms.assetid: a918082d-709d-4b4f-ae3b-5f16ed0ca910
title: Devolver valores de un controlador de interfaz de usuario externo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b466f6bc3cc034551a01bd2b87caa7292824e0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811803"
---
# <a name="returning-values-from-an-external-user-interface-handler"></a><span data-ttu-id="d4707-103">Devolver valores de un controlador de interfaz de usuario externo</span><span class="sxs-lookup"><span data-stu-id="d4707-103">Returning Values from an External User Interface Handler</span></span>

<span data-ttu-id="d4707-104">Un controlador de interfaz de usuario (IU) externo puede devolver cualquier número de valores para Windows Installer en función del tipo de botón proporcionado en el parámetro de tipo de mensaje que el instalador pasa al controlador.</span><span class="sxs-lookup"><span data-stu-id="d4707-104">An external user interface (UI) handler can return any number of values to Windows Installer depending on the button type provided in the message type parameter the installer passes to the handler.</span></span>

<span data-ttu-id="d4707-105">El controlador de la interfaz de usuario externa puede devolver los valores-1 y 0 en cualquier momento, ya que no están relacionados con los tipos de botón.</span><span class="sxs-lookup"><span data-stu-id="d4707-105">The external UI handler can return the values –1 and 0 at any time because these are not related to the button types.</span></span> <span data-ttu-id="d4707-106">Un valor devuelto de – 1 indica que se ha producido un error interno en el controlador de la interfaz de usuario externa.</span><span class="sxs-lookup"><span data-stu-id="d4707-106">A return value of –1 indicates that an internal error occurred in the external UI handler.</span></span> <span data-ttu-id="d4707-107">Un valor devuelto de 0 indica que el controlador de la interfaz de usuario externa no ha controlado el mensaje del instalador y el instalador debe controlar el mensaje en su lugar.</span><span class="sxs-lookup"><span data-stu-id="d4707-107">A return value of 0 indicates that the external UI handler has not handled the installer message and the installer must handle the message instead.</span></span>

<span data-ttu-id="d4707-108">En el caso de los mensajes que no incluyen un tipo de botón, como INSTALLMESSAGE \_ ACTIONDATA y INSTALLMESSAGE \_ Progress, la devolución de IDCANCEL cancela la instalación.</span><span class="sxs-lookup"><span data-stu-id="d4707-108">For messages that do not include a button type, such as INSTALLMESSAGE\_ACTIONDATA and INSTALLMESSAGE\_PROGRESS, returning IDCANCEL cancels the installation.</span></span> <span data-ttu-id="d4707-109">Al devolver IDOK, se notifica al instalador que el controlador de la interfaz de usuario externa controló el mensaje.</span><span class="sxs-lookup"><span data-stu-id="d4707-109">Returning IDOK notifies the installer that the message was handled by the external UI handler.</span></span>

<span data-ttu-id="d4707-110">Los valores devueltos restantes, como se describe a continuación, se relacionan directamente con los tipos de botón que se incluyen con el tipo de mensaje.</span><span class="sxs-lookup"><span data-stu-id="d4707-110">The remaining return values, as described below, are directly related to the button types that are included with the message type.</span></span>



| <span data-ttu-id="d4707-111">Valor devuelto de IU externa</span><span class="sxs-lookup"><span data-stu-id="d4707-111">External UI return value</span></span> | <span data-ttu-id="d4707-112">Significado</span><span class="sxs-lookup"><span data-stu-id="d4707-112">Meaning</span></span>                                                                                                |
|--------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4707-113">IDOK</span><span class="sxs-lookup"><span data-stu-id="d4707-113">IDOK</span></span>                     | <span data-ttu-id="d4707-114">El usuario presionó el botón **Aceptar** .</span><span class="sxs-lookup"><span data-stu-id="d4707-114">The **OK** button was pressed by the user.</span></span> <span data-ttu-id="d4707-115">Se entendió la información del mensaje.</span><span class="sxs-lookup"><span data-stu-id="d4707-115">The message information was understood.</span></span>                     |
| <span data-ttu-id="d4707-116">IDCANCEL</span><span class="sxs-lookup"><span data-stu-id="d4707-116">IDCANCEL</span></span>                 | <span data-ttu-id="d4707-117">Se presionó el botón **Cancelar** .</span><span class="sxs-lookup"><span data-stu-id="d4707-117">The **CANCEL** button was pressed.</span></span> <span data-ttu-id="d4707-118">Cancele la instalación.</span><span class="sxs-lookup"><span data-stu-id="d4707-118">Cancel the installation.</span></span>                                            |
| <span data-ttu-id="d4707-119">IDABORT</span><span class="sxs-lookup"><span data-stu-id="d4707-119">IDABORT</span></span>                  | <span data-ttu-id="d4707-120">Se presionó el botón **anular** .</span><span class="sxs-lookup"><span data-stu-id="d4707-120">The **ABORT** button was pressed.</span></span> <span data-ttu-id="d4707-121">Cancele la instalación.</span><span class="sxs-lookup"><span data-stu-id="d4707-121">Abort the installation.</span></span>                                              |
| <span data-ttu-id="d4707-122">IDRETRY</span><span class="sxs-lookup"><span data-stu-id="d4707-122">IDRETRY</span></span>                  | <span data-ttu-id="d4707-123">Se presionó el botón **Reintentar** .</span><span class="sxs-lookup"><span data-stu-id="d4707-123">The **RETRY** button was pressed.</span></span> <span data-ttu-id="d4707-124">Vuelva a intentar la acción.</span><span class="sxs-lookup"><span data-stu-id="d4707-124">Try the action again.</span></span>                                                |
| <span data-ttu-id="d4707-125">IDIGNORE</span><span class="sxs-lookup"><span data-stu-id="d4707-125">IDIGNORE</span></span>                 | <span data-ttu-id="d4707-126">Se presionó el botón **omitir** .</span><span class="sxs-lookup"><span data-stu-id="d4707-126">The **IGNORE** button was pressed.</span></span> <span data-ttu-id="d4707-127">Omita el error y continúe.</span><span class="sxs-lookup"><span data-stu-id="d4707-127">Ignore the error and continue.</span></span>                                      |
| <span data-ttu-id="d4707-128">IDYES</span><span class="sxs-lookup"><span data-stu-id="d4707-128">IDYES</span></span>                    | <span data-ttu-id="d4707-129">Se presionó el botón **sí** .</span><span class="sxs-lookup"><span data-stu-id="d4707-129">The **YES** button was pressed.</span></span> <span data-ttu-id="d4707-130">Respuesta afirmativa, continuar con la secuencia de eventos actual.</span><span class="sxs-lookup"><span data-stu-id="d4707-130">The affirmative response, continue with current sequence of events..</span></span>   |
| <span data-ttu-id="d4707-131">IDNO</span><span class="sxs-lookup"><span data-stu-id="d4707-131">IDNO</span></span>                     | <span data-ttu-id="d4707-132">Se presionó el botón **no** .</span><span class="sxs-lookup"><span data-stu-id="d4707-132">The **NO** button was pressed.</span></span> <span data-ttu-id="d4707-133">La respuesta negativa, no continuar con la secuencia de eventos actual.</span><span class="sxs-lookup"><span data-stu-id="d4707-133">The negative response, do not continue with current sequence of events.</span></span> |



 

<span data-ttu-id="d4707-134">Por ejemplo, si se envía un mensaje al controlador de la interfaz de usuario externa con la \_ marca de estilos de cuadro de mensaje MB ABORTRETRYIGNORE, el controlador de la interfaz de usuario externa puede devolver uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="d4707-134">For example, if the external UI handler is sent a message with the MB\_ABORTRETRYIGNORE message box styles flag, the external UI handler can return one of the following values:</span></span>

-   <span data-ttu-id="d4707-135">– 1 (error en el controlador de la interfaz de usuario externa)</span><span class="sxs-lookup"><span data-stu-id="d4707-135">–1 (error in external UI handler)</span></span>
-   <span data-ttu-id="d4707-136">0 (no se realiza ninguna acción en el controlador de la interfaz de usuario externa, se deja Windows Installer controlar)</span><span class="sxs-lookup"><span data-stu-id="d4707-136">0 (no action taken in external UI handler, let Windows Installer handle it)</span></span>
-   <span data-ttu-id="d4707-137">IDABORT (botón de **anulación** presionado)</span><span class="sxs-lookup"><span data-stu-id="d4707-137">IDABORT (**ABORT** button pressed)</span></span>
-   <span data-ttu-id="d4707-138">IDRETRY (botón **Reintentar** presionado)</span><span class="sxs-lookup"><span data-stu-id="d4707-138">IDRETRY (**RETRY** button pressed)</span></span>
-   <span data-ttu-id="d4707-139">IDIGNORE (botón **omitir** presionado)</span><span class="sxs-lookup"><span data-stu-id="d4707-139">IDIGNORE (**IGNORE** button pressed)</span></span>

 

 



