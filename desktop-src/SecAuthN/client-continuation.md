---
description: Algunos protocolos requieren varios mensajes de autenticación.
ms.assetid: b4c4c38c-0286-49b1-b93d-4c6b885fe0f6
title: Continuación del cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca363489cf87a8fdf2743a8c26a7848c257212e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908601"
---
# <a name="client-continuation"></a><span data-ttu-id="f6aa0-103">Continuación del cliente</span><span class="sxs-lookup"><span data-stu-id="f6aa0-103">Client Continuation</span></span>

<span data-ttu-id="f6aa0-104">Algunos protocolos requieren varios mensajes de autenticación.</span><span class="sxs-lookup"><span data-stu-id="f6aa0-104">Some protocols require multiple authentication messages.</span></span> <span data-ttu-id="f6aa0-105">En este caso, el cliente analiza la respuesta del servidor y llama a [**InitializeSecurityContext (general)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) de nuevo con el estado continue de la llamada anterior.</span><span class="sxs-lookup"><span data-stu-id="f6aa0-105">In this case, the client parses the response from the server and calls [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) again using the continue status from the previous call.</span></span> <span data-ttu-id="f6aa0-106">El cliente comprueba el estado de devolución de esta llamada y podría ser necesario continuar para otras piernas.</span><span class="sxs-lookup"><span data-stu-id="f6aa0-106">The client checks the return status from this call and might be required to continue for additional legs.</span></span> <span data-ttu-id="f6aa0-107">Usa la información de *pOutput* para construir un mensaje y lo envía al servidor.</span><span class="sxs-lookup"><span data-stu-id="f6aa0-107">It uses the information in *pOutput* to construct a message and sends it to the server.</span></span>

 

 
