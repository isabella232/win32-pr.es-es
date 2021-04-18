---
description: Envía un paquete de finalización de e/s a un puerto de finalización de e/s.
ms.assetid: 69a9b1e5-2d40-42de-a14a-f7b6f29bf571
title: Función PostQueuedCompletionStatus (IoAPI. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PostQueuedCompletionStatus
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: f12de10032df7fec32dd9a577353dd20c0f4eaa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668273"
---
# <a name="postqueuedcompletionstatus-function"></a><span data-ttu-id="a52f9-103">PostQueuedCompletionStatus función)</span><span class="sxs-lookup"><span data-stu-id="a52f9-103">PostQueuedCompletionStatus function</span></span>

<span data-ttu-id="a52f9-104">Envía un paquete de finalización de e/s a un puerto de finalización de e/s.</span><span class="sxs-lookup"><span data-stu-id="a52f9-104">Posts an I/O completion packet to an I/O completion port.</span></span>

## <a name="syntax"></a><span data-ttu-id="a52f9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a52f9-105">Syntax</span></span>


```C++
BOOL WINAPI PostQueuedCompletionStatus(
  _In_     HANDLE       CompletionPort,
  _In_     DWORD        dwNumberOfBytesTransferred,
  _In_     ULONG_PTR    dwCompletionKey,
  _In_opt_ LPOVERLAPPED lpOverlapped
);
```



## <a name="parameters"></a><span data-ttu-id="a52f9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a52f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a52f9-107">*CompletionPort* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a52f9-107">*CompletionPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a52f9-108">Identificador de un puerto de finalización de e/s en el que se va a publicar el paquete de finalización de e/s.</span><span class="sxs-lookup"><span data-stu-id="a52f9-108">A handle to an I/O completion port to which the I/O completion packet is to be posted.</span></span>

</dd> <dt>

<span data-ttu-id="a52f9-109">*dwNumberOfBytesTransferred* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a52f9-109">*dwNumberOfBytesTransferred* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a52f9-110">Valor que se va a devolver mediante el parámetro *lpNumberOfBytesTransferred* de la función [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="a52f9-110">The value to be returned through the *lpNumberOfBytesTransferred* parameter of the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="a52f9-111">*dwCompletionKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a52f9-111">*dwCompletionKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a52f9-112">Valor que se va a devolver mediante el parámetro *lpCompletionKey* de la función [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="a52f9-112">The value to be returned through the *lpCompletionKey* parameter of the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="a52f9-113">*lpOverlapped* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a52f9-113">*lpOverlapped* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a52f9-114">Valor que se va a devolver mediante el parámetro *lpOverlapped* de la función [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="a52f9-114">The value to be returned through the *lpOverlapped* parameter of the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a52f9-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a52f9-115">Return value</span></span>

<span data-ttu-id="a52f9-116">Si la función se realiza correctamente, el valor devuelto es distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="a52f9-116">If the function succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="a52f9-117">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="a52f9-117">If the function fails, the return value is zero.</span></span> <span data-ttu-id="a52f9-118">Para obtener información de error extendida, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="a52f9-118">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span></span>

## <a name="remarks"></a><span data-ttu-id="a52f9-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a52f9-119">Remarks</span></span>

<span data-ttu-id="a52f9-120">El paquete de finalización de e/s satisfará una llamada pendiente a la función [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="a52f9-120">The I/O completion packet will satisfy an outstanding call to the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span> <span data-ttu-id="a52f9-121">Esta función devuelve con los tres valores pasados como el segundo, tercer y cuarto parámetro de la llamada a **PostQueuedCompletionStatus**.</span><span class="sxs-lookup"><span data-stu-id="a52f9-121">This function returns with the three values passed as the second, third, and fourth parameters of the call to **PostQueuedCompletionStatus**.</span></span> <span data-ttu-id="a52f9-122">El sistema no usa ni valida estos valores.</span><span class="sxs-lookup"><span data-stu-id="a52f9-122">The system does not use or validate these values.</span></span> <span data-ttu-id="a52f9-123">En concreto, el parámetro *lpOverlapped* no debe apuntar a una estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="a52f9-123">In particular, the *lpOverlapped* parameter need not point to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="a52f9-124">En Windows 8 y Windows Server 2012, esta función es compatible con las siguientes tecnologías.</span><span class="sxs-lookup"><span data-stu-id="a52f9-124">In Windows 8 and Windows Server 2012, this function is supported by the following technologies.</span></span>



| <span data-ttu-id="a52f9-125">Technology</span><span class="sxs-lookup"><span data-stu-id="a52f9-125">Technology</span></span>                                           | <span data-ttu-id="a52f9-126">Compatible</span><span class="sxs-lookup"><span data-stu-id="a52f9-126">Supported</span></span>      |
|------------------------------------------------------|----------------|
| <span data-ttu-id="a52f9-127">Protocolo bloque de mensajes del servidor (SMB) 3,0</span><span class="sxs-lookup"><span data-stu-id="a52f9-127">Server Message Block (SMB) 3.0 protocol</span></span><br/>   | <span data-ttu-id="a52f9-128">Sí</span><span class="sxs-lookup"><span data-stu-id="a52f9-128">Yes</span></span><br/> |
| <span data-ttu-id="a52f9-129">Conmutación por error transparente SMB 3,0 (TFO)</span><span class="sxs-lookup"><span data-stu-id="a52f9-129">SMB 3.0 Transparent Failover (TFO)</span></span><br/>        | <span data-ttu-id="a52f9-130">Sí</span><span class="sxs-lookup"><span data-stu-id="a52f9-130">Yes</span></span><br/> |
| <span data-ttu-id="a52f9-131">SMB 3,0 con recursos compartidos de archivos de escalabilidad horizontal (por lo tanto)</span><span class="sxs-lookup"><span data-stu-id="a52f9-131">SMB 3.0 with Scale-out File Shares (SO)</span></span><br/>   | <span data-ttu-id="a52f9-132">Sí</span><span class="sxs-lookup"><span data-stu-id="a52f9-132">Yes</span></span><br/> |
| <span data-ttu-id="a52f9-133">Sistema de archivos Volumen compartido de clúster (CsvFS)</span><span class="sxs-lookup"><span data-stu-id="a52f9-133">Cluster Shared Volume File System (CsvFS)</span></span><br/> | <span data-ttu-id="a52f9-134">Sí</span><span class="sxs-lookup"><span data-stu-id="a52f9-134">Yes</span></span><br/> |
| <span data-ttu-id="a52f9-135">Sistema de archivos resistente a errores (ReFS)</span><span class="sxs-lookup"><span data-stu-id="a52f9-135">Resilient File System (ReFS)</span></span><br/>              | <span data-ttu-id="a52f9-136">Sí</span><span class="sxs-lookup"><span data-stu-id="a52f9-136">Yes</span></span><br/> |



 

<span data-ttu-id="a52f9-137">CsvFs realizará la e/s redirigida para archivos comprimidos.</span><span class="sxs-lookup"><span data-stu-id="a52f9-137">CsvFs will do redirected IO for compressed files.</span></span>

## <a name="requirements"></a><span data-ttu-id="a52f9-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a52f9-138">Requirements</span></span>



| <span data-ttu-id="a52f9-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="a52f9-139">Requirement</span></span> | <span data-ttu-id="a52f9-140">Value</span><span class="sxs-lookup"><span data-stu-id="a52f9-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a52f9-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a52f9-141">Minimum supported client</span></span><br/> | <span data-ttu-id="a52f9-142">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows XP \|\]</span><span class="sxs-lookup"><span data-stu-id="a52f9-142">Windows XP \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="a52f9-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a52f9-143">Minimum supported server</span></span><br/> | <span data-ttu-id="a52f9-144">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2003 \|\]</span><span class="sxs-lookup"><span data-stu-id="a52f9-144">Windows Server 2003 \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                                              |
| <span data-ttu-id="a52f9-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a52f9-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="a52f9-146"><dt>IoAPI. h (incluye Windows. h); </dt> <dt>Winbase. h en Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 y Windows XP (incluido Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a52f9-146"><dt>IoAPI.h (include Windows.h); </dt> <dt>WinBase.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="a52f9-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a52f9-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="a52f9-148"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="a52f9-148"><dt>Kernel32.lib</dt></span></span> </dl>                                                                                                                                                                                                                  |
| <span data-ttu-id="a52f9-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a52f9-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a52f9-150"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a52f9-150"><dt>Kernel32.dll</dt></span></span> </dl>                                                                                                                                                                                                                  |



## <a name="see-also"></a><span data-ttu-id="a52f9-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="a52f9-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a52f9-152">**CreateIoCompletionPort**</span><span class="sxs-lookup"><span data-stu-id="a52f9-152">**CreateIoCompletionPort**</span></span>](createiocompletionport.md)
</dt> <dt>

[<span data-ttu-id="a52f9-153">Funciones de administración de archivos</span><span class="sxs-lookup"><span data-stu-id="a52f9-153">File Management Functions</span></span>](file-management-functions.md)
</dt> <dt>

[<span data-ttu-id="a52f9-154">**GetQueuedCompletionStatus**</span><span class="sxs-lookup"><span data-stu-id="a52f9-154">**GetQueuedCompletionStatus**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[<span data-ttu-id="a52f9-155">**SUPERPUESTA**</span><span class="sxs-lookup"><span data-stu-id="a52f9-155">**OVERLAPPED**</span></span>](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)
</dt> </dl>

 

