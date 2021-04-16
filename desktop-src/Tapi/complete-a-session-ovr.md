---
description: Las operaciones de finalización permiten a una aplicación especificar cómo desea controlar una sesión cuando factores como un destino de ocupado impiden la conexión normal.
ms.assetid: 71e61376-7913-42a9-a8e2-2ea6e4918f30
title: Completar una sesión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5736b6be452413811f3530f44db280fe4e2a682f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687020"
---
# <a name="complete-a-session"></a><span data-ttu-id="6d17e-103">Completar una sesión</span><span class="sxs-lookup"><span data-stu-id="6d17e-103">Complete a Session</span></span>

<span data-ttu-id="6d17e-104">Las operaciones de finalización permiten a una aplicación especificar cómo desea controlar una sesión cuando factores como un destino de ocupado impiden la conexión normal.</span><span class="sxs-lookup"><span data-stu-id="6d17e-104">Completion operations allow an application to specify how it wants to handle a session when factors such as a busy destination prevent normal connection.</span></span>

<span data-ttu-id="6d17e-105">Las [ \_ constantes LINECALLCOMPLMODE](./linecallcomplmode--constants.md) definen las posibles opciones que podría tener una aplicación, en función de las capacidades del proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="6d17e-105">The [LINECALLCOMPLMODE\_ Constants](./linecallcomplmode--constants.md) define the possible options an application might have, depending on service provider capabilities.</span></span>

<span data-ttu-id="6d17e-106">Puede haber varias solicitudes de finalización de llamada pendientes para una dirección determinada en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="6d17e-106">Multiple call completion requests might be outstanding for a given address at any one time.</span></span> <span data-ttu-id="6d17e-107">Para identificar solicitudes individuales, la implementación devuelve un [identificador de finalización](completion-id-ovr.md).</span><span class="sxs-lookup"><span data-stu-id="6d17e-107">To identify individual requests, the implementation returns a [completion identifier](completion-id-ovr.md).</span></span> <span data-ttu-id="6d17e-108">La cancelación de una solicitud de finalización de llamada en curso también utiliza este identificador de finalización de llamada.</span><span class="sxs-lookup"><span data-stu-id="6d17e-108">Canceling a call completion request in progress also uses this call completion identifier.</span></span>

<span data-ttu-id="6d17e-109">**TAPI 2. x:** Vea [**lineCompleteCall**](/windows/win32/api/tapi/nf-tapi-linecompletecall), [**lineUncompleteCall**](/windows/win32/api/tapi/nf-tapi-lineuncompletecall).</span><span class="sxs-lookup"><span data-stu-id="6d17e-109">**TAPI 2.x:** See [**lineCompleteCall**](/windows/win32/api/tapi/nf-tapi-linecompletecall), [**lineUncompleteCall**](/windows/win32/api/tapi/nf-tapi-lineuncompletecall).</span></span>

<span data-ttu-id="6d17e-110">**TAPI 3. x:** Vea [**ITBasicCallControl:: Connect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-connect), [**ITBasicCallControl::D Ulta**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect).</span><span class="sxs-lookup"><span data-stu-id="6d17e-110">**TAPI 3.x:** See [**ITBasicCallControl::Connect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-connect), [**ITBasicCallControl::Disconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect).</span></span>

 

 
