---
description: En función del código de retorno de una llamada anterior a AcceptSecurityContext (general), el servidor puede esperar una respuesta del cliente y puede participar en intercambios adicionales con el cliente.
ms.assetid: 281e1f81-3524-4034-bee5-cef6b13cf402
title: Continuación del servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22fba8a60bea12daae0e6aaf93fed55fead5738c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667111"
---
# <a name="server-continuation"></a><span data-ttu-id="6fc2f-103">Continuación del servidor</span><span class="sxs-lookup"><span data-stu-id="6fc2f-103">Server Continuation</span></span>

<span data-ttu-id="6fc2f-104">En función del código de retorno de una llamada anterior a [**AcceptSecurityContext (general)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext), el servidor puede esperar una respuesta del cliente y puede participar en intercambios adicionales con el cliente.</span><span class="sxs-lookup"><span data-stu-id="6fc2f-104">Based on the return code from a previous call to [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext), the server can wait for a response from the client and can participate in additional exchanges with the client.</span></span> <span data-ttu-id="6fc2f-105">Para continuar el protocolo de autenticación, el servidor repite las llamadas a **AcceptSecurityContext (general)**.</span><span class="sxs-lookup"><span data-stu-id="6fc2f-105">To continue the authentication protocol, the server repeats calls to **AcceptSecurityContext (General)**.</span></span>

<span data-ttu-id="6fc2f-106">El estado devuelto por [**AcceptSecurityContext (general)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) se comprueba para ver si el servidor tiene que esperar más mensajes del cliente.</span><span class="sxs-lookup"><span data-stu-id="6fc2f-106">The status returned by [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) is checked to see if the server needs to wait for additional messages from the client.</span></span> <span data-ttu-id="6fc2f-107">En la mayoría de los protocolos de autenticación, hay un número máximo de intercambios incluso para la autenticación mutua.</span><span class="sxs-lookup"><span data-stu-id="6fc2f-107">In most authentication protocols, there is a maximum number of exchanges even for mutual authentication.</span></span> <span data-ttu-id="6fc2f-108">Actualmente, los protocolos NTLM y [*Kerberos*](../secgloss/k-gly.md) realizan la autenticación mutua con tres intercambios.</span><span class="sxs-lookup"><span data-stu-id="6fc2f-108">Currently, both the NTLM and [*Kerberos protocols*](../secgloss/k-gly.md) do mutual authentication with three exchanges.</span></span>

 

 
