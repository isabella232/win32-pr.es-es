---
title: Funciones de autorización (RPC)
description: Cada vez que un programa de servidor recibe una solicitud de cliente para obtener acceso a uno de los procedimientos remotos de administración, la biblioteca en tiempo de ejecución de RPC invoca una función de autorización predeterminada.
ms.assetid: e3edbf6f-2876-49ac-a93e-14fd0b5adf53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 490c06ba8e40f132c17986edaef4dc02bbe056d7
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/12/2019
ms.locfileid: "104077056"
---
# <a name="authorization-functions"></a><span data-ttu-id="f50ed-103">Funciones de autorización</span><span class="sxs-lookup"><span data-stu-id="f50ed-103">Authorization Functions</span></span>

<span data-ttu-id="f50ed-104">Cada vez que un programa de servidor recibe una solicitud de cliente para obtener acceso a uno de los procedimientos remotos de administración, la biblioteca en tiempo de ejecución de RPC invoca una función de autorización predeterminada.</span><span class="sxs-lookup"><span data-stu-id="f50ed-104">Each time a server program receives a client request for access to one of the management remote procedures, the RPC run-time library invokes a default authorization function.</span></span> <span data-ttu-id="f50ed-105">Esta función usa el SSP para comprobar las credenciales del cliente y autorizar o rechazar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f50ed-105">This function uses the SSP to check the client's credentials and authorize or reject the request.</span></span>

<span data-ttu-id="f50ed-106">El programa de servidor puede invalidar la función de autorización que proporciona el SSP.</span><span class="sxs-lookup"><span data-stu-id="f50ed-106">Your server program can override the authorization function that the SSP provides.</span></span> <span data-ttu-id="f50ed-107">Invoque la función [**RpcMgmtSetAuthorizationFn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetauthorizationfn) y pásela a la dirección de la función de autorización.</span><span class="sxs-lookup"><span data-stu-id="f50ed-107">Invoke the function [**RpcMgmtSetAuthorizationFn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetauthorizationfn) and pass it to the address of your authorization function.</span></span> <span data-ttu-id="f50ed-108">Una vez que el programa de servidor establece la función de autorización, la biblioteca en tiempo de ejecución de RPC la llama cada vez que el programa de servidor recibe una solicitud de cliente a una de las funciones de administración.</span><span class="sxs-lookup"><span data-stu-id="f50ed-108">Once the server program sets the authorization function, the RPC run-time library calls it every time the server program receives a client request to one of the management functions.</span></span> <span data-ttu-id="f50ed-109">Para obtener más información, consulte [**RpcMgmtIsServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtisserverlistening), [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening), [**RpcMgmtInqIfIds**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqifids), [**RpcMgmtInqServerPrincName**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname)y [**RpcMgmtInqStats**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqstats).</span><span class="sxs-lookup"><span data-stu-id="f50ed-109">For more information, see [**RpcMgmtIsServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtisserverlistening), [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening), [**RpcMgmtInqIfIds**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqifids), [**RpcMgmtInqServerPrincName**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname), and [**RpcMgmtInqStats**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqstats).</span></span>

 

 




