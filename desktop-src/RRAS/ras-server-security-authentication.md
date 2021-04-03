---
title: Autenticación de seguridad del servidor RAS
description: Cuando un servidor RAS de Windows NT/Windows 2000 recibe una llamada, invoca la función RasSecurityDialogBegin del archivo DLL de seguridad RAS registrado, si hay alguno.
ms.assetid: dd9469ec-9bb1-4444-af5b-72e3ba8b4cb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27184388b418e0fec2a1988fd9e693e942c08e03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075630"
---
# <a name="ras-server-security-authentication"></a><span data-ttu-id="d4fce-103">Autenticación de seguridad del servidor RAS</span><span class="sxs-lookup"><span data-stu-id="d4fce-103">RAS Server Security Authentication</span></span>

<span data-ttu-id="d4fce-104">Cuando un servidor RAS de Windows NT/Windows 2000 recibe una llamada, invoca la función [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) del archivo dll de seguridad ras registrado, si hay alguno.</span><span class="sxs-lookup"><span data-stu-id="d4fce-104">When a Windows NT/Windows 2000 RAS server receives a call, it invokes the [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) function of the registered RAS security DLL, if there is one.</span></span> <span data-ttu-id="d4fce-105">Esta llamada notifica a la DLL de seguridad que comienza su autenticación del usuario remoto.</span><span class="sxs-lookup"><span data-stu-id="d4fce-105">This call notifies the security DLL to begin its authentication of the remote user.</span></span> <span data-ttu-id="d4fce-106">El servidor RAS llama a **RasSecurityDialogBegin** antes de realizar la autenticación PPP o ras.</span><span class="sxs-lookup"><span data-stu-id="d4fce-106">The RAS server calls **RasSecurityDialogBegin** before performing its PPP or RAS authentication.</span></span>

<span data-ttu-id="d4fce-107">La llamada a [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) pasa la siguiente información al archivo dll de seguridad:</span><span class="sxs-lookup"><span data-stu-id="d4fce-107">The [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) call passes the following information to the security DLL:</span></span>

-   <span data-ttu-id="d4fce-108">Identificador de puerto para identificar la conexión.</span><span class="sxs-lookup"><span data-stu-id="d4fce-108">A port handle to identify the connection.</span></span>
-   <span data-ttu-id="d4fce-109">Punteros a los búferes que se van a usar al comunicarse con el usuario remoto.</span><span class="sxs-lookup"><span data-stu-id="d4fce-109">Pointers to buffers to use when communicating with the remote user.</span></span>
-   <span data-ttu-id="d4fce-110">Puntero a una función [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) que se va a llamar cuando se haya completado la autenticación.</span><span class="sxs-lookup"><span data-stu-id="d4fce-110">A pointer to a [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) function to call when the authentication has been completed.</span></span>

<span data-ttu-id="d4fce-111">Los punteros de identificador de puerto y de búfer son válidos hasta que el archivo DLL de seguridad llama a [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) para finalizar la transacción de autenticación.</span><span class="sxs-lookup"><span data-stu-id="d4fce-111">The port handle and buffer pointers are valid until the security DLL calls [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) to terminate the authentication transaction.</span></span>

<span data-ttu-id="d4fce-112">[**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) notifica al servidor RAS los resultados de la autenticación del archivo dll de seguridad del usuario remoto.</span><span class="sxs-lookup"><span data-stu-id="d4fce-112">The [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) notifies the RAS server of the results of the security DLL's authentication of the remote user.</span></span> <span data-ttu-id="d4fce-113">Si el archivo DLL de seguridad informa del éxito, el servidor RAS continúa con su autenticación PPP y RAS del usuario remoto.</span><span class="sxs-lookup"><span data-stu-id="d4fce-113">If the security DLL reports success, the RAS server proceeds with its PPP and RAS authentication of the remote user.</span></span> <span data-ttu-id="d4fce-114">Si el archivo DLL de seguridad informa de que el usuario remoto no ha superado la autenticación, o que se ha producido un error, el servidor RAS cuelga y registra el error o no se ha podido realizar la autenticación en el registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="d4fce-114">If the security DLL reports that the remote user failed the authentication, or that an error occurred, the RAS server hangs up and logs the error or failed authentication in the event log.</span></span>

 

 




