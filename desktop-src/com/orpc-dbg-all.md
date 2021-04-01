---
title: Estructura de ORPC_DBG_ALL
description: La \_ estructura ORPC dbg \_ All se usa para pasar parámetros a los métodos de la interfaz IOrpcDebugNotify.
ms.assetid: 05371beb-9202-40a6-96d2-4b91497e2ee9
keywords:
- Estructura de ORPC_DBG_ALL COM
- LPORPC_DBG_ALL puntero de estructura COM
topic_type:
- apiref
api_name:
- ORPC_DBG_ALL
api_location:
- N/A
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a17f5b09e5fe2f668bf2bcd21e2e7fe6f0f766a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150083"
---
# <a name="orpc_dbg_all-structure"></a><span data-ttu-id="f3d96-105">ORPC \_ dbg \_ All (estructura)</span><span class="sxs-lookup"><span data-stu-id="f3d96-105">ORPC\_DBG\_ALL structure</span></span>

<span data-ttu-id="f3d96-106">La estructura **ORPC \_ dbg \_ All** se usa para pasar parámetros a los métodos de la interfaz [**IOrpcDebugNotify**](iorpcdebugnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="f3d96-106">The **ORPC\_DBG\_ALL** structure is used to pass parameters to the methods of the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

> [!Note]  
> <span data-ttu-id="f3d96-107">Cada método de la interfaz [**IOrpcDebugNotify**](iorpcdebugnotify.md) utiliza una combinación diferente de los miembros siguientes.</span><span class="sxs-lookup"><span data-stu-id="f3d96-107">Each method of the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface uses a different combination of the members below.</span></span> <span data-ttu-id="f3d96-108">Si un miembro no se indica como lo usa un método, no está definido cuando se pasa a ese método.</span><span class="sxs-lookup"><span data-stu-id="f3d96-108">If a member is not indicated as used by a method, it is undefined when passed to that method.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="f3d96-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f3d96-109">Syntax</span></span>


```C++
typedef struct ORPC_DBG_ALL {
  BYTE              *pSignature;
  RPCOLEMESSAGE     *pMessage;
  const IID         *refiid;
  IRpcChannelBuffer *pChannel;
  IUnknown          *pUnkProxyMgr;
  void              *pInterface;
  IUnknown          *pUnkObject;
  HRESULT           hresult;
  void              *pvBuffer;
  ULONG             *cbBuffer;
  ULONG             *lpcbBuffer;
  void              *reserved;
} ORPC_DBG_ALL, *LPORPC_DBG_ALL;
```



## <a name="members"></a><span data-ttu-id="f3d96-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="f3d96-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="f3d96-111">**pSignature**</span><span class="sxs-lookup"><span data-stu-id="f3d96-111">**pSignature**</span></span>
</dt> <dd>

<span data-ttu-id="f3d96-112">Un puntero a un búfer de **bytes** que contiene:</span><span class="sxs-lookup"><span data-stu-id="f3d96-112">A pointer to a **BYTE** buffer that contains:</span></span>

-   <span data-ttu-id="f3d96-113">Primeros cuatro bytes: los caracteres ASCII "MARB" al aumentar el orden de la memoria.</span><span class="sxs-lookup"><span data-stu-id="f3d96-113">First four bytes: the ASCII characters "MARB" in increasing memory order.</span></span>
-   <span data-ttu-id="f3d96-114">16 bytes siguientes: un **GUID** que identifica la notificación a la que se llama.</span><span class="sxs-lookup"><span data-stu-id="f3d96-114">Next 16 bytes: A **GUID** that identifies the notification being called.</span></span> <span data-ttu-id="f3d96-115">Contiene uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="f3d96-115">It contains one of the following:</span></span>
    1.  <span data-ttu-id="f3d96-116">[**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md): 9ED14F80-9673-101A-B07B-00DD01113F11</span><span class="sxs-lookup"><span data-stu-id="f3d96-116">[**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md): 9ED14F80-9673-101A-B07B-00DD01113F11</span></span>
    2.  <span data-ttu-id="f3d96-117">[**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md):D a45f3e0-9673-101A-B07B-00DD01113F11</span><span class="sxs-lookup"><span data-stu-id="f3d96-117">[**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md):DA45F3E0-9673-101A-B07B-00DD01113F11</span></span>
    3.  <span data-ttu-id="f3d96-118">[**ClientNotify**](iorpcdebugnotify-clientnotify.md): 4F60E540-9674-101A-B07B-00DD01113F11</span><span class="sxs-lookup"><span data-stu-id="f3d96-118">[**ClientNotify**](iorpcdebugnotify-clientnotify.md):4F60E540-9674-101A-B07B-00DD01113F11</span></span>
    4.  <span data-ttu-id="f3d96-119">[**ServerNotify**](iorpcdebugnotify-servernotify.md): 1084FA00-9674-101A-B07B-00DD01113F11</span><span class="sxs-lookup"><span data-stu-id="f3d96-119">[**ServerNotify**](iorpcdebugnotify-servernotify.md):1084FA00-9674-101A-B07B-00DD01113F11</span></span>
    5.  <span data-ttu-id="f3d96-120">[**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md): 22080240-9674-101A-B07B-00DD01113F11</span><span class="sxs-lookup"><span data-stu-id="f3d96-120">[**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md):22080240-9674-101A-B07B-00DD01113F11</span></span>
    6.  <span data-ttu-id="f3d96-121">[**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md): 2FC09500-9674-101A-B07B-00DD01113F11</span><span class="sxs-lookup"><span data-stu-id="f3d96-121">[**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md):2FC09500-9674-101A-B07B-00DD01113F11</span></span>
-   <span data-ttu-id="f3d96-122">Siguientes cuatro bytes: reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="f3d96-122">Next four-bytes: Reserved for future use.</span></span>

> [!Note]
>
> <span data-ttu-id="f3d96-123">Lo usan todos los métodos de la interfaz [**IOrpcDebugNotify**](iorpcdebugnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="f3d96-123">Used by all methods of the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

 

</dd> <dt>

<span data-ttu-id="f3d96-124">**pMessage**</span><span class="sxs-lookup"><span data-stu-id="f3d96-124">**pMessage**</span></span>
</dt> <dd>

<span data-ttu-id="f3d96-125">Puntero a una estructura [**RPCOLEMESSAGE**](/windows/win32/api/objidlbase/ns-objidlbase-rpcolemessage) que contiene información de cálculo de referencias de datos RPC.</span><span class="sxs-lookup"><span data-stu-id="f3d96-125">A pointer to an [**RPCOLEMESSAGE**](/windows/win32/api/objidlbase/ns-objidlbase-rpcolemessage) structure that contains RPC data marshalling information.</span></span>

> [!Note]
>
> <span data-ttu-id="f3d96-126">Lo usan los métodos [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)y [**ServerNotify**](iorpcdebugnotify-servernotify.md) .</span><span class="sxs-lookup"><span data-stu-id="f3d96-126">Used by the [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md), and [**ServerNotify**](iorpcdebugnotify-servernotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="f3d96-127">**REFIID**</span><span class="sxs-lookup"><span data-stu-id="f3d96-127">**refiid**</span></span>
</dt> <dd>

<span data-ttu-id="f3d96-128">Puntero al IID de la interfaz [**IOrpcDebugNotify**](iorpcdebugnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="f3d96-128">A pointer to the IID of the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

> [!Note]
>
> <span data-ttu-id="f3d96-129">Lo usan los métodos [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)y [**ServerNotify**](iorpcdebugnotify-servernotify.md) .</span><span class="sxs-lookup"><span data-stu-id="f3d96-129">Used by the [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md), and [**ServerNotify**](iorpcdebugnotify-servernotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="f3d96-130">**pChannel**</span><span class="sxs-lookup"><span data-stu-id="f3d96-130">**pChannel**</span></span>
</dt> <dd>

<span data-ttu-id="f3d96-131">Puntero a la interfaz [**IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer) de la implementación del canal RPC de com en el servidor.</span><span class="sxs-lookup"><span data-stu-id="f3d96-131">A pointer to the [**IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer) interface of the COM RPC channel implementation on the server.</span></span>

> [!Note]
>
> <span data-ttu-id="f3d96-132">Lo usan los métodos [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)y [**ServerNotify**](iorpcdebugnotify-servernotify.md) .</span><span class="sxs-lookup"><span data-stu-id="f3d96-132">Used by the [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md), and [**ServerNotify**](iorpcdebugnotify-servernotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="f3d96-133">**pUnkProxyMgr**</span><span class="sxs-lookup"><span data-stu-id="f3d96-133">**pUnkProxyMgr**</span></span>
</dt> <dd>

<span data-ttu-id="f3d96-134">Puntero a la interfaz [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) del objeto implicado en esta invocación del depurador.</span><span class="sxs-lookup"><span data-stu-id="f3d96-134">A pointer to the [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface of the object involved in this debugger invocation.</span></span> <span data-ttu-id="f3d96-135">Sin embargo, puede ser **null**, lo que reduce la funcionalidad del depurador.</span><span class="sxs-lookup"><span data-stu-id="f3d96-135">May be **NULL**, however, this reduces debugger functionality.</span></span>

> [!Note]
>
> <span data-ttu-id="f3d96-136">Lo usan los métodos [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md)y [**ClientNotify**](iorpcdebugnotify-clientnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="f3d96-136">Used by the [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), and [**ClientNotify**](iorpcdebugnotify-clientnotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="f3d96-137">**pInterface**</span><span class="sxs-lookup"><span data-stu-id="f3d96-137">**pInterface**</span></span>
</dt> <dd>

<span data-ttu-id="f3d96-138">Puntero a la interfaz COM del método que va a invocar esta RPC.</span><span class="sxs-lookup"><span data-stu-id="f3d96-138">A pointer to the COM interface of the method that will be invoked by this RPC.</span></span> <span data-ttu-id="f3d96-139">No debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="f3d96-139">Must not be **NULL**.</span></span>

> [!Note]
>
> <span data-ttu-id="f3d96-140">Lo usan los métodos [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)y [**ServerNotify**](iorpcdebugnotify-servernotify.md) .</span><span class="sxs-lookup"><span data-stu-id="f3d96-140">Used by the [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md), and [**ServerNotify**](iorpcdebugnotify-servernotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="f3d96-141">**pUnkObject**</span><span class="sxs-lookup"><span data-stu-id="f3d96-141">**pUnkObject**</span></span>
</dt> <dd>

<span data-ttu-id="f3d96-142">Debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="f3d96-142">Must be **NULL**.</span></span>

> [!Note]
>
> <span data-ttu-id="f3d96-143">Lo usan los métodos [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)y [**ServerNotify**](iorpcdebugnotify-servernotify.md) .</span><span class="sxs-lookup"><span data-stu-id="f3d96-143">Used by the [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md), and [**ServerNotify**](iorpcdebugnotify-servernotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="f3d96-144">**valor**</span><span class="sxs-lookup"><span data-stu-id="f3d96-144">**hresult**</span></span>
</dt> <dd>

<span data-ttu-id="f3d96-145">El propósito de este miembro cambia para cada una de las notificaciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="f3d96-145">This member's purpose changes for each of the notifications below:</span></span>

<span data-ttu-id="f3d96-146">[**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md): el número de bytes que el depurador del cliente transmitirá al depurador del servidor.</span><span class="sxs-lookup"><span data-stu-id="f3d96-146">[**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md): the number of bytes the client debugger will transmit to the server debugger.</span></span> <span data-ttu-id="f3d96-147">Si es cero, no es necesario transmitir información.</span><span class="sxs-lookup"><span data-stu-id="f3d96-147">If zero, no information need be transmitted.</span></span>

<span data-ttu-id="f3d96-148">[**ClientNotify**](iorpcdebugnotify-clientnotify.md): **HRESULT** de la última RPC.</span><span class="sxs-lookup"><span data-stu-id="f3d96-148">[**ClientNotify**](iorpcdebugnotify-clientnotify.md): the **HRESULT** of the last RPC.</span></span>

<span data-ttu-id="f3d96-149">[**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md): el número de bytes que el depurador del cliente transmitirá al depurador del servidor.</span><span class="sxs-lookup"><span data-stu-id="f3d96-149">[**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md): the number of bytes the client debugger will transmit to the server debugger.</span></span> <span data-ttu-id="f3d96-150">Si es cero, no es necesario transmitir información.</span><span class="sxs-lookup"><span data-stu-id="f3d96-150">If zero, no information need be transmitted.</span></span>

> [!Note]
>
> <span data-ttu-id="f3d96-151">Lo usan los métodos [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md)y [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md) .</span><span class="sxs-lookup"><span data-stu-id="f3d96-151">Used by the [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), and [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="f3d96-152">**pvBuffer**</span><span class="sxs-lookup"><span data-stu-id="f3d96-152">**pvBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="f3d96-153">Puntero a una estructura [**de \_ \_ búfer de ORPC dbg**](orpc-dbg-buffer.md) que contiene la información de depuración de serialización de RPC.</span><span class="sxs-lookup"><span data-stu-id="f3d96-153">A pointer to an [**ORPC\_DBG\_BUFFER**](orpc-dbg-buffer.md) structure that contains the RPC marshalled debug information.</span></span> <span data-ttu-id="f3d96-154">Es indefinido si **cbBuffer** es cero.</span><span class="sxs-lookup"><span data-stu-id="f3d96-154">Is undefined if **cbBuffer** is zero.</span></span>

> [!Note]
>
> <span data-ttu-id="f3d96-155">Lo usan los métodos [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md)y [**ServerNotify**](iorpcdebugnotify-servernotify.md) .</span><span class="sxs-lookup"><span data-stu-id="f3d96-155">Used by the [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), and [**ServerNotify**](iorpcdebugnotify-servernotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="f3d96-156">**cbBuffer**</span><span class="sxs-lookup"><span data-stu-id="f3d96-156">**cbBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="f3d96-157">La longitud, en bytes, de los datos a los que apunta **pvBuffer**.</span><span class="sxs-lookup"><span data-stu-id="f3d96-157">The length, in bytes, of the data pointed to by **pvBuffer**.</span></span>

> [!Note]
>
> <span data-ttu-id="f3d96-158">Lo usan los métodos [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md)y [**ServerNotify**](iorpcdebugnotify-servernotify.md) .</span><span class="sxs-lookup"><span data-stu-id="f3d96-158">Used by the [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), and [**ServerNotify**](iorpcdebugnotify-servernotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="f3d96-159">**lpcbBuffer**</span><span class="sxs-lookup"><span data-stu-id="f3d96-159">**lpcbBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="f3d96-160">El número de bytes que el depurador del cliente transmitirá al depurador del servidor.</span><span class="sxs-lookup"><span data-stu-id="f3d96-160">The number of bytes the client debugger will transmit to the server debugger.</span></span> <span data-ttu-id="f3d96-161">Si es cero, no es necesario transmitir información.</span><span class="sxs-lookup"><span data-stu-id="f3d96-161">If zero, no information need be transmitted.</span></span> <span data-ttu-id="f3d96-162">Este valor reemplaza el valor devuelto en **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f3d96-162">This value supersedes the value returned in **hresult**.</span></span>

> [!Note]
>
> <span data-ttu-id="f3d96-163">Lo usan los métodos [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md) .</span><span class="sxs-lookup"><span data-stu-id="f3d96-163">Used by the [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="f3d96-164">**sector**</span><span class="sxs-lookup"><span data-stu-id="f3d96-164">**reserved**</span></span>
</dt> <dd>

<span data-ttu-id="f3d96-165">Reservado.</span><span class="sxs-lookup"><span data-stu-id="f3d96-165">Reserved.</span></span> <span data-ttu-id="f3d96-166">No utilizar.</span><span class="sxs-lookup"><span data-stu-id="f3d96-166">Do not use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f3d96-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3d96-167">Requirements</span></span>



| <span data-ttu-id="f3d96-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3d96-168">Requirement</span></span> | <span data-ttu-id="f3d96-169">Value</span><span class="sxs-lookup"><span data-stu-id="f3d96-169">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="f3d96-170">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f3d96-170">Minimum supported client</span></span><br/> | <span data-ttu-id="f3d96-171">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f3d96-171">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="f3d96-172">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f3d96-172">Minimum supported server</span></span><br/> | <span data-ttu-id="f3d96-173">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f3d96-173">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f3d96-174">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f3d96-174">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3d96-175"><dt>N/D</dt></span><span class="sxs-lookup"><span data-stu-id="f3d96-175"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3d96-176">Vea también</span><span class="sxs-lookup"><span data-stu-id="f3d96-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3d96-177">**\_búfer ORPC dbg \_**</span><span class="sxs-lookup"><span data-stu-id="f3d96-177">**ORPC\_DBG\_BUFFER**</span></span>](orpc-dbg-buffer.md)
</dt> <dt>

[<span data-ttu-id="f3d96-178">**ORPC \_ init \_ args**</span><span class="sxs-lookup"><span data-stu-id="f3d96-178">**ORPC\_INIT\_ARGS**</span></span>](orpc-init-args.md)
</dt> <dt>

[<span data-ttu-id="f3d96-179">**DllDebugObjectRPCHook**</span><span class="sxs-lookup"><span data-stu-id="f3d96-179">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> <dt>

[<span data-ttu-id="f3d96-180">**IOrpcDebugNotify**</span><span class="sxs-lookup"><span data-stu-id="f3d96-180">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

