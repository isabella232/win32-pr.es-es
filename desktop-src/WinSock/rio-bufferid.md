---
description: Especifica un descriptor de búfer registrado usado con las extensiones de e/s registradas de Winsock.
ms.assetid: 87D0A3F6-A44C-4D7F-B276-7FD5DC2DE7A3
title: RIO_BUFFERID (Mswsockdef. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75bb439a567c361a056b750728d986891a1da468
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082401"
---
# <a name="rio_bufferid"></a><span data-ttu-id="f0ed9-103">Río \_ BUFFERID</span><span class="sxs-lookup"><span data-stu-id="f0ed9-103">RIO\_BUFFERID</span></span>

<span data-ttu-id="f0ed9-104">La definición de tipo de **Rio \_ BUFFERID** especifica un descriptor de búfer registrado que se usa con las extensiones de e/s registradas de Winsock.</span><span class="sxs-lookup"><span data-stu-id="f0ed9-104">The **RIO\_BUFFERID** typedef specifies a registered buffer descriptor used with the Winsock registered I/O extensions.</span></span>


```C++
typedef struct RIO_BUFFERID_t* RIO_BUFFERID, **PRIO_BUFFERID;
```



<dl> <dt>

<span data-ttu-id="f0ed9-105">**Río \_ BUFFERID**</span><span class="sxs-lookup"><span data-stu-id="f0ed9-105">**RIO\_BUFFERID**</span></span>
</dt> <dd>

<span data-ttu-id="f0ed9-106">Un tipo de datos que especifica un descriptor de búfer registrado utilizado con solicitudes de envío y recepción.</span><span class="sxs-lookup"><span data-stu-id="f0ed9-106">A data type that specifies a registered buffer descriptor used with send and receive requests.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f0ed9-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f0ed9-107">Remarks</span></span>

<span data-ttu-id="f0ed9-108">Las extensiones de e/s registradas de Winsock funcionan principalmente en búferes registrados mediante objetos **río \_ BUFFERID** .</span><span class="sxs-lookup"><span data-stu-id="f0ed9-108">The Winsock registered I/O extensions operate primarily on registered buffers using **RIO\_BUFFERID** objects.</span></span> <span data-ttu-id="f0ed9-109">Una aplicación obtiene un **río \_ BUFFERID** para un búfer existente mediante la función [**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="f0ed9-109">An application obtains a **RIO\_BUFFERID** for an existing buffer using the [**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) function.</span></span> <span data-ttu-id="f0ed9-110">Una aplicación puede liberar un registro mediante la función [**RIODeregisterBuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) .</span><span class="sxs-lookup"><span data-stu-id="f0ed9-110">An application can release a registration using the [**RIODeregisterBuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) function.</span></span>

<span data-ttu-id="f0ed9-111">Cuando un búfer existente se registra como un objeto **río \_ BUFFERID** mediante la función [**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) , se asignan determinados recursos internos de la memoria física y el búfer de aplicación existente se bloqueará en la memoria física.</span><span class="sxs-lookup"><span data-stu-id="f0ed9-111">When an existing buffer is registered as a **RIO\_BUFFERID** object using the [**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) function, certain internal resources are allocated from physical memory, and the existing application buffer will be locked into physical memory.</span></span> <span data-ttu-id="f0ed9-112">Se llama a la función [**RIODeregisterBuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) para anular el registro del búfer, liberar estos recursos internos y permitir que el búfer se desbloquee y se libere de la memoria física.</span><span class="sxs-lookup"><span data-stu-id="f0ed9-112">The [**RIODeregisterBuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) function is called to deregister the buffer, free these internal resources, and allow the buffer to be unlocked and released from physical memory.</span></span>

<span data-ttu-id="f0ed9-113">El registro y la cancelación de registro repetidos de los búferes de la aplicación mediante las extensiones de e/s registradas de Winsock pueden provocar una degradación significativa del rendimiento.</span><span class="sxs-lookup"><span data-stu-id="f0ed9-113">Repeated registration and deregistration of application buffers using the Winsock registered I/O extensions may cause significant performance degradation.</span></span> <span data-ttu-id="f0ed9-114">Se deben tener en cuenta los siguientes enfoques de administración de búfer al diseñar una aplicación mediante las extensiones de e/s registradas de Winsock para minimizar el registro y la cancelación de registro repetidos de los búferes de la aplicación:</span><span class="sxs-lookup"><span data-stu-id="f0ed9-114">The following buffer management approaches should be considered when designing an application using the Winsock registered I/O extensions to minimize repeated registration and deregistration of application buffers:</span></span>

-   <span data-ttu-id="f0ed9-115">• Maximice la reutilización de búferes.</span><span class="sxs-lookup"><span data-stu-id="f0ed9-115">• Maximize the reuse of buffers.</span></span>
-   <span data-ttu-id="f0ed9-116">• Mantener un grupo limitado de búferes registrados no utilizados para que la aplicación los use.</span><span class="sxs-lookup"><span data-stu-id="f0ed9-116">• Maintain a limited pool of unused registered buffers for use by the application.</span></span>
-   <span data-ttu-id="f0ed9-117">• Mantener un grupo limitado de búferes registrados y realizar copias de búfer entre estos búferes registrados y otros búferes no registrados.</span><span class="sxs-lookup"><span data-stu-id="f0ed9-117">• Maintain a limited pool of registered buffers and perform buffer copies between these registered buffers and other unregistered buffers.</span></span>

<span data-ttu-id="f0ed9-118">La definición de tipo de **Rio \_ BUFFERID** se define en el archivo de encabezado *Mswsockdef. h* que se incluye automáticamente en el archivo de encabezado *mswsock. h* .</span><span class="sxs-lookup"><span data-stu-id="f0ed9-118">The **RIO\_BUFFERID** typedef is defined in the *Mswsockdef.h* header file which is automatically included in the *Mswsock.h* header file.</span></span> <span data-ttu-id="f0ed9-119">El archivo de encabezado *Mswsockdef. h* nunca debe usarse directamente.</span><span class="sxs-lookup"><span data-stu-id="f0ed9-119">The *Mswsockdef.h* header file should never be used directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0ed9-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0ed9-120">Requirements</span></span>



| <span data-ttu-id="f0ed9-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0ed9-121">Requirement</span></span> | <span data-ttu-id="f0ed9-122">Value</span><span class="sxs-lookup"><span data-stu-id="f0ed9-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0ed9-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0ed9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f0ed9-124">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="f0ed9-124">Windows 8 \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="f0ed9-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0ed9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f0ed9-126">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="f0ed9-126">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="f0ed9-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f0ed9-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0ed9-128"><dt>Mswsockdef. h (incluye mswsock. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f0ed9-128"><dt>Mswsockdef.h (include Mswsock.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0ed9-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0ed9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0ed9-130">**Río \_ BUF**</span><span class="sxs-lookup"><span data-stu-id="f0ed9-130">**RIO\_BUF**</span></span>](/windows/desktop/api/Mswsockdef/ns-mswsockdef-rio_buf)
</dt> <dt>

[<span data-ttu-id="f0ed9-131">**RIODeregisterBuffer**</span><span class="sxs-lookup"><span data-stu-id="f0ed9-131">**RIODeregisterBuffer**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer)
</dt> <dt>

[<span data-ttu-id="f0ed9-132">**RIOReceive**</span><span class="sxs-lookup"><span data-stu-id="f0ed9-132">**RIOReceive**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceive)
</dt> <dt>

[<span data-ttu-id="f0ed9-133">**RIOReceiveEx**</span><span class="sxs-lookup"><span data-stu-id="f0ed9-133">**RIOReceiveEx**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceiveex)
</dt> <dt>

<span data-ttu-id="f0ed9-134">[**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f0ed9-134">[**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f0ed9-135">**RIOSend**</span><span class="sxs-lookup"><span data-stu-id="f0ed9-135">**RIOSend**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_riosend)
</dt> <dt>

<span data-ttu-id="f0ed9-136">[**RIOSendEx**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f0ed9-136">[**RIOSendEx**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85))</span></span>
</dt> </dl>

 

 
