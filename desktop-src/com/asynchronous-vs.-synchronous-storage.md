---
title: Almacenamiento asincrónico y sincrónico
description: Almacenamiento asincrónico y sincrónico
ms.assetid: de8c50f8-1733-439f-ab53-f98ac21a1fae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 884b8613bebf8ef401f76e4761f48fa0ddd831c2
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104533544"
---
# <a name="asynchronous-and-synchronous-storage"></a><span data-ttu-id="b80ea-103">Almacenamiento asincrónico y sincrónico</span><span class="sxs-lookup"><span data-stu-id="b80ea-103">Asynchronous and Synchronous Storage</span></span>

<span data-ttu-id="b80ea-104">Los monikers asincrónicos también pueden devolver un objeto de [almacenamiento asincrónico](/windows/desktop/Stg/asynchronous-storage) en la notificación [**IBindStatusCallback:: ondataavailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b80ea-104">Asynchronous monikers may also return an [Asynchronous Storage](/windows/desktop/Stg/asynchronous-storage) object in the [**IBindStatusCallback::OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)) notification.</span></span> <span data-ttu-id="b80ea-105">Este objeto de almacenamiento puede permitir el acceso a algunos de los datos persistentes del objeto mientras el enlace todavía está en curso.</span><span class="sxs-lookup"><span data-stu-id="b80ea-105">This storage object may allow access to some of the object's persistent data while the binding is still in progress.</span></span> <span data-ttu-id="b80ea-106">Un cliente puede elegir entre dos modos de almacenamiento: bloqueo y desbloqueo.</span><span class="sxs-lookup"><span data-stu-id="b80ea-106">A client can choose between two modes for the storage: blocking and nonblocking.</span></span>

<span data-ttu-id="b80ea-107">En el modo de bloqueo, que es compatible con las implementaciones actuales de los objetos de almacenamiento, si los datos no están disponibles, la llamada se bloquea hasta que llegan los datos.</span><span class="sxs-lookup"><span data-stu-id="b80ea-107">In blocking mode, which is compatible with current implementations of storage objects, if data is unavailable, the call blocks until data arrives.</span></span> <span data-ttu-id="b80ea-108">En el modo de no bloqueo, en lugar de bloquear la llamada, el objeto de almacenamiento devuelve un nuevo error E \_ pendiente cuando los datos no están disponibles.</span><span class="sxs-lookup"><span data-stu-id="b80ea-108">In nonblocking mode, rather than blocking the call, the storage object returns a new error E\_PENDING when data is unavailable.</span></span> <span data-ttu-id="b80ea-109">Un cliente que reconoce el enlace asincrónico y el almacenamiento anota este error y espera notificaciones adicionales ([**ondataavailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))) para volver a intentar la operación.</span><span class="sxs-lookup"><span data-stu-id="b80ea-109">A client aware of asynchronous binding and storage notes this error and waits for further notifications ([**OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))) to retry the operation.</span></span> <span data-ttu-id="b80ea-110">Un cliente puede elegir entre un almacenamiento sincrónico (bloqueo) y asincrónico (sin bloqueo) Si elige establecer la \_ marca BINDF ASYNCSTORAGE en el valor *grfBINDF* devuelto a [**IBindStatusCallback:: GetBindInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b80ea-110">A client can choose between a synchronous (blocking) and asynchronous (nonblocking) storage by choosing whether to set the BINDF\_ASYNCSTORAGE flag in the *grfBINDF* value returned to [**IBindStatusCallback::GetBindInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b80ea-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b80ea-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b80ea-112">Monikers asincrónicos</span><span class="sxs-lookup"><span data-stu-id="b80ea-112">Asynchronous Monikers</span></span>](asynchronous-monikers.md)
</dt> </dl>

 

 