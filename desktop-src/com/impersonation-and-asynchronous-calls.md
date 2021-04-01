---
title: Suplantación y llamadas asincrónicas
description: Suplantación y llamadas asincrónicas
ms.assetid: 7eaa0a66-7a80-4831-b0b6-b8eff4abd036
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0854946b619f7580173ffcbc97c9af3f2540361b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103794158"
---
# <a name="impersonation-and-asynchronous-calls"></a><span data-ttu-id="28f9e-103">Suplantación y llamadas asincrónicas</span><span class="sxs-lookup"><span data-stu-id="28f9e-103">Impersonation and Asynchronous Calls</span></span>

<span data-ttu-id="28f9e-104">El servidor no puede suplantar al cliente después de que se complete la llamada del servidor a [**ISynchronize:: Signal**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal) , aunque \_ no se haya completado aún el método Begin.</span><span class="sxs-lookup"><span data-stu-id="28f9e-104">The server cannot impersonate the client after the server's call to [**ISynchronize::Signal**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal) completes, even if the Begin\_ method has not yet completed.</span></span> <span data-ttu-id="28f9e-105">Por ejemplo, supongamos que un cliente llama al \_ método Begin, el servidor procesa la llamada inmediatamente y el servidor llama a **Signal** para indicar que ha finalizado el procesamiento.</span><span class="sxs-lookup"><span data-stu-id="28f9e-105">For example, suppose a client calls the Begin\_ method, the server processes the call immediately, and the server calls **Signal** to indicate it is finished processing.</span></span> <span data-ttu-id="28f9e-106">Aunque el trabajo siga siendo realizado en el método Begin \_ , el servidor no puede suplantar al cliente después de que se complete la llamada a **Signal** .</span><span class="sxs-lookup"><span data-stu-id="28f9e-106">Even if work remains to be done in the Begin\_ method, the server cannot impersonate the client after the call to **Signal** completes.</span></span>

<span data-ttu-id="28f9e-107">Si el servidor suplanta al cliente antes de llamar a [**Signal**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal), el token de suplantación no se quitará del subproceso hasta que el servidor llame a [**IServerSecurity:: RevertToSelf**](/windows/win32/api/objidlbase/nf-objidlbase-iserversecurity-reverttoself) o hasta que la llamada del servidor a Begin vuelva, lo que suceda \_ primero.</span><span class="sxs-lookup"><span data-stu-id="28f9e-107">If the server impersonates the client before it calls [**Signal**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal), the impersonation token will not be removed from the thread until the server calls [**IServerSecurity::RevertToSelf**](/windows/win32/api/objidlbase/nf-objidlbase-iserversecurity-reverttoself) or until the server's call to Begin\_ returns, whichever comes first.</span></span>

## <a name="related-topics"></a><span data-ttu-id="28f9e-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="28f9e-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28f9e-109">Delegación y suplantación</span><span class="sxs-lookup"><span data-stu-id="28f9e-109">Delegation and Impersonation</span></span>](delegation-and-impersonation.md)
</dt> <dt>

[<span data-ttu-id="28f9e-110">Realización de una llamada asincrónica</span><span class="sxs-lookup"><span data-stu-id="28f9e-110">Making an Asynchronous Call</span></span>](making-an-asynchronous-call.md)
</dt> </dl>

 

 