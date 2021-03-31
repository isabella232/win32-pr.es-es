---
title: Seguridad de Server-Side
description: Seguridad de Server-Side
ms.assetid: 6c1d210e-daf0-490a-a6b9-65d99b9e1d7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77501c395c3ae1f14c8451d4691e7e776545e756
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103995665"
---
# <a name="server-side-security"></a><span data-ttu-id="e374c-103">Seguridad de Server-Side</span><span class="sxs-lookup"><span data-stu-id="e374c-103">Server-Side Security</span></span>

<span data-ttu-id="e374c-104">El servidor puede recuperar información de seguridad sobre un llamador o suplantar al autor de la llamada mediante los métodos de [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity).</span><span class="sxs-lookup"><span data-stu-id="e374c-104">The server can retrieve security information about a caller or impersonate the caller by using the methods of [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity).</span></span> <span data-ttu-id="e374c-105">COM proporciona una implementación de **IServerSecurity** en el objeto de contexto para la llamada actual cuando se utiliza la serialización estándar.</span><span class="sxs-lookup"><span data-stu-id="e374c-105">An implementation of **IServerSecurity** is supplied by COM on the context object for the current call when standard marshaling is used.</span></span> <span data-ttu-id="e374c-106">Sin embargo, es posible que esta interfaz no esté presente para algunas interfaces de serialización personalizadas.</span><span class="sxs-lookup"><span data-stu-id="e374c-106">However, this interface may be absent for some custom-marshaled interfaces.</span></span>

<span data-ttu-id="e374c-107">Cuando una llamada llega al servidor, el servidor puede llamar a [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) para obtener un puntero a la interfaz [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) .</span><span class="sxs-lookup"><span data-stu-id="e374c-107">When a call arrives at the server, the server can call [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) to obtain a pointer to the [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) interface.</span></span> <span data-ttu-id="e374c-108">Con este puntero, el servidor puede llamar a los métodos **IServerSecurity** para averiguar cuál es la configuración de autenticación del cliente y suplantar al cliente, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="e374c-108">With this pointer, **IServerSecurity** methods can be called by the server to find out what the client's authentication settings are and to impersonate the client, if needed.</span></span> <span data-ttu-id="e374c-109">El objeto **IServerSecurity** es válido en cualquier subproceso del apartamento hasta que se complete la llamada representada por **IServerSecurity** .</span><span class="sxs-lookup"><span data-stu-id="e374c-109">The **IServerSecurity** object is valid on any thread in the apartment until the call represented by **IServerSecurity** completes.</span></span> <span data-ttu-id="e374c-110">Para obtener más información sobre la suplantación, vea [suplantación](impersonation.md) y [Cloaking](cloaking.md).</span><span class="sxs-lookup"><span data-stu-id="e374c-110">For more information about impersonation, see [Impersonation](impersonation.md) and [Cloaking](cloaking.md).</span></span>

<span data-ttu-id="e374c-111">También están disponibles las siguientes funciones auxiliares que se basan en la implementación de la interfaz [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) del objeto de contexto de llamada:</span><span class="sxs-lookup"><span data-stu-id="e374c-111">The following helper functions that rely on the call context object's [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) interface implementation are also available:</span></span>

-   [<span data-ttu-id="e374c-112">**CoQueryClientBlanket**</span><span class="sxs-lookup"><span data-stu-id="e374c-112">**CoQueryClientBlanket**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket)
-   [<span data-ttu-id="e374c-113">**CoImpersonateClient**</span><span class="sxs-lookup"><span data-stu-id="e374c-113">**CoImpersonateClient**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient)
-   [<span data-ttu-id="e374c-114">**CoRevertToSelf**</span><span class="sxs-lookup"><span data-stu-id="e374c-114">**CoRevertToSelf**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself)

## <a name="related-topics"></a><span data-ttu-id="e374c-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e374c-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e374c-116">Seguridad en COM</span><span class="sxs-lookup"><span data-stu-id="e374c-116">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 