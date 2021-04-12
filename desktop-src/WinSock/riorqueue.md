---
description: Especifica un descriptor de socket utilizado por las solicitudes de envío y recepción con las extensiones de e/s registradas de Winsock.
ms.assetid: 50E9516C-6078-4466-A593-3F29E4783740
title: RIO_RQ (Mswsockdef. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c25abebbe40842532f3cca180868b5b3786e756d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360547"
---
# <a name="rio_rq"></a><span data-ttu-id="f70ec-103">Río \_ PET</span><span class="sxs-lookup"><span data-stu-id="f70ec-103">RIO\_RQ</span></span>

<span data-ttu-id="f70ec-104">La definición de tipo de **Rio \_ PET** especifica un descriptor de socket utilizado por las solicitudes de envío y recepción con las extensiones de e/s registradas de Winsock.</span><span class="sxs-lookup"><span data-stu-id="f70ec-104">The **RIO\_RQ** typedef specifies a socket descriptor used by send and receive requests with the Winsock registered I/O extensions.</span></span>


```C++
typedef struct RIO_RQ_t* RIO_RQ, **PRIO_RQ;
```



<dl> <dt>

<span data-ttu-id="f70ec-105">**Río \_ PET**</span><span class="sxs-lookup"><span data-stu-id="f70ec-105">**RIO\_RQ**</span></span>
</dt> <dd>

<span data-ttu-id="f70ec-106">Un tipo de datos que especifica un descriptor de socket utilizado por las solicitudes de envío y recepción.</span><span class="sxs-lookup"><span data-stu-id="f70ec-106">A data type that specifies a socket descriptor used by send and receive requests.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f70ec-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f70ec-107">Remarks</span></span>

<span data-ttu-id="f70ec-108">Las extensiones de e/s registradas de Winsock funcionan principalmente en un objeto **Rio \_ PET** en lugar de un socket.</span><span class="sxs-lookup"><span data-stu-id="f70ec-108">The Winsock registered I/O extensions operate primarily on a **RIO\_RQ** object rather than a socket.</span></span> <span data-ttu-id="f70ec-109">Una aplicación obtiene un **río \_ PET** para un socket existente mediante la función [**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue) .</span><span class="sxs-lookup"><span data-stu-id="f70ec-109">An application obtains a **RIO\_RQ** for an existing socket using the [**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue) function.</span></span> <span data-ttu-id="f70ec-110">Se debe haber creado el socket de entrada mediante una llamada a la función [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) con la marca de **Rio de \_ marca \_ WSA** establecida en el parámetro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="f70ec-110">The input socket must have been created by calling the [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) function with the **WSA\_FLAG\_RIO** flag set in the *dwFlags* parameter.</span></span>

<span data-ttu-id="f70ec-111">Después de obtener un objeto **Rio \_ PET** , el descriptor de socket subyacente sigue siendo válido.</span><span class="sxs-lookup"><span data-stu-id="f70ec-111">After obtaining a **RIO\_RQ** object, the underlying socket descriptor remains valid.</span></span> <span data-ttu-id="f70ec-112">Una aplicación puede seguir utilizando el socket subyacente para establecer y consultar las opciones de socket, emitir ioctl y, en última instancia, cerrar el socket.</span><span class="sxs-lookup"><span data-stu-id="f70ec-112">An application may continue to use the underlying socket to set and query socket options, issue IOCTLs and ultimately close the socket.</span></span>

> [!Note]  
> <span data-ttu-id="f70ec-113">Por motivos de eficacia, el acceso a las colas de finalización (estructuras [**\_ CQ de Rio**](riocqueue.md) ) y a las colas de solicitudes (Structs **\_ PET** ) no están protegidos por primitivas de sincronización.</span><span class="sxs-lookup"><span data-stu-id="f70ec-113">For purposes of efficiency, access to the completion queues ([**RIO\_CQ**](riocqueue.md) structs) and request queues (**RIO\_RQ** structs) are not protected by synchronization primitives.</span></span> <span data-ttu-id="f70ec-114">Si necesita tener acceso a una cola de finalización o solicitud desde varios subprocesos, el acceso debe coordinarse mediante una sección crítica, un bloqueo de escritura de lector fino o un mecanismo similar.</span><span class="sxs-lookup"><span data-stu-id="f70ec-114">If you need to access a completion or request queue from multiple threads, access should be coordinated by a critical section, slim reader write lock or similar mechanism.</span></span> <span data-ttu-id="f70ec-115">Este bloqueo no es necesario para el acceso a un único subproceso.</span><span class="sxs-lookup"><span data-stu-id="f70ec-115">This locking is not needed for access by a single thread.</span></span> <span data-ttu-id="f70ec-116">Distintos subprocesos pueden tener acceso a solicitudes o colas de finalización independientes sin bloqueos.</span><span class="sxs-lookup"><span data-stu-id="f70ec-116">Different threads can access separate requests/completion queues without locks.</span></span> <span data-ttu-id="f70ec-117">La necesidad de sincronización solo se produce cuando varios subprocesos intentan obtener acceso a la misma cola.</span><span class="sxs-lookup"><span data-stu-id="f70ec-117">The need for synchronization occurs only when multiple threads try to access the same queue.</span></span> <span data-ttu-id="f70ec-118">La sincronización también es necesaria si varios subprocesos emiten y reciben en el mismo socket porque las operaciones de envío y recepción utilizan la cola de solicitudes del socket.</span><span class="sxs-lookup"><span data-stu-id="f70ec-118">Synchronization is also required if multiple threads issue sends and receives on the same socket because the send and receive operations use the socket’s request queue.</span></span>

 

<span data-ttu-id="f70ec-119">La definición de tipo de [**Rio \_ PET**](riocqueue.md) se define en el archivo de encabezado *Mswsockdef. h* que se incluye automáticamente en el archivo de encabezado *mswsock. h* .</span><span class="sxs-lookup"><span data-stu-id="f70ec-119">The [**RIO\_RQ**](riocqueue.md) typedef is defined in the *Mswsockdef.h* header file which is automatically included in the *Mswsock.h* header file.</span></span> <span data-ttu-id="f70ec-120">El archivo de encabezado *Mswsockdef. h* nunca debe usarse directamente.</span><span class="sxs-lookup"><span data-stu-id="f70ec-120">The *Mswsockdef.h* header file should never be used directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="f70ec-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f70ec-121">Requirements</span></span>



| <span data-ttu-id="f70ec-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f70ec-122">Requirement</span></span> | <span data-ttu-id="f70ec-123">Value</span><span class="sxs-lookup"><span data-stu-id="f70ec-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f70ec-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f70ec-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f70ec-125">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="f70ec-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="f70ec-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f70ec-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f70ec-127">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="f70ec-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="f70ec-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f70ec-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f70ec-129"><dt>Mswsockdef. h (incluye mswsock. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f70ec-129"><dt>Mswsockdef.h (include Mswsock.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f70ec-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="f70ec-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f70ec-131">**RIOCreateRequestQueue**</span><span class="sxs-lookup"><span data-stu-id="f70ec-131">**RIOCreateRequestQueue**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue)
</dt> <dt>

[<span data-ttu-id="f70ec-132">**RIOReceive**</span><span class="sxs-lookup"><span data-stu-id="f70ec-132">**RIOReceive**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceive)
</dt> <dt>

[<span data-ttu-id="f70ec-133">**RIOReceiveEx**</span><span class="sxs-lookup"><span data-stu-id="f70ec-133">**RIOReceiveEx**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceiveex)
</dt> <dt>

<span data-ttu-id="f70ec-134">[**RIOResizeRequestQueue**](/previous-versions/windows/desktop/legacy/hh437204(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f70ec-134">[**RIOResizeRequestQueue**](/previous-versions/windows/desktop/legacy/hh437204(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f70ec-135">**RIOSend**</span><span class="sxs-lookup"><span data-stu-id="f70ec-135">**RIOSend**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_riosend)
</dt> <dt>

<span data-ttu-id="f70ec-136">[**RIOSendEx**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f70ec-136">[**RIOSendEx**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f70ec-137">**WSASocket**</span><span class="sxs-lookup"><span data-stu-id="f70ec-137">**WSASocket**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)
</dt> </dl>

 

 
