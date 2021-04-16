---
title: Sincronización de devolución de llamada
description: Sincronización de devolución de llamada
ms.assetid: e8268f18-49e7-4e09-9006-77858b734bf4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c274c35a6df176f65c505f2a3fecc9a53a20e5d9
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105714470"
---
# <a name="callback-synchronization"></a><span data-ttu-id="f5bc4-103">Sincronización de devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="f5bc4-103">Callback Synchronization</span></span>

<span data-ttu-id="f5bc4-104">La API de [WinInet](/windows/desktop/WinInet/portal) asincrónica (utilizada para los protocolos más comunes) deja la sincronización del mecanismo de devolución de llamada y la aplicación que realiza la llamada como un ejercicio para el cliente.</span><span class="sxs-lookup"><span data-stu-id="f5bc4-104">The asynchronous [WinInet API](/windows/desktop/WinInet/portal) (used for the most common protocols) leaves the synchronization of the callback mechanism and the calling application as an exercise for the client.</span></span> <span data-ttu-id="f5bc4-105">Esto es intencionado porque permite el mayor grado de flexibilidad.</span><span class="sxs-lookup"><span data-stu-id="f5bc4-105">This is intentional because it allows the greatest degree of flexibility.</span></span> <span data-ttu-id="f5bc4-106">Los protocolos predeterminados y la implementación de moniker de dirección URL realizan esta sincronización y garantizan que las aplicaciones de un solo subproceso y de subprocesamiento controlado nunca tienen que tratar con la contención de estilo de subproceso libre.</span><span class="sxs-lookup"><span data-stu-id="f5bc4-106">The default protocols and the URL moniker implementation perform this synchronization and guarantee that single-threaded and apartment-threaded applications never have to deal with free-thread-style contention.</span></span> <span data-ttu-id="f5bc4-107">Es decir, solo se llama a las interfaces [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) y [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) del cliente en los subprocesos correspondientes.</span><span class="sxs-lookup"><span data-stu-id="f5bc4-107">That is, the client's [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) and [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) interfaces are called only on their proper threads.</span></span> <span data-ttu-id="f5bc4-108">Esta característica es transparente para el usuario de la dirección URL mMoniker siempre que cada subproceso que llama a [**IMoniker:: BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) y [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) tiene una cola de mensajes.</span><span class="sxs-lookup"><span data-stu-id="f5bc4-108">This feature is transparent to the user of the URL mMoniker as long each thread that calls [**IMoniker::BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) and [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) has a message queue.</span></span>

<span data-ttu-id="f5bc4-109">La especificación de moniker asincrónico requiere un control más preciso sobre la priorización y la administración de las descargas que se permite en WinSock o WinInet.</span><span class="sxs-lookup"><span data-stu-id="f5bc4-109">The asynchronous moniker specification requires more precise control over the prioritization and management of downloads than is allowed for by either WinSock or WinInet.</span></span> <span data-ttu-id="f5bc4-110">En consecuencia, un moniker de dirección URL administra todas las descargas de cualquier subproceso del llamador determinado, usando (como parte de su sincronización) un esquema de prioridad basado en la especificación [**IBinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="f5bc4-110">Accordingly, a URL moniker manages all the downloads for any given caller's thread, using (as part of its synchronization) a priority scheme based on the [**IBinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85)) specification.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f5bc4-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f5bc4-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5bc4-112">Monikers de URL</span><span class="sxs-lookup"><span data-stu-id="f5bc4-112">URL Monikers</span></span>](url-monikers.md)
</dt> </dl>

 

 