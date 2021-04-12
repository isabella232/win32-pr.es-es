---
description: Devolución de llamada que notifica al host la información de fotogramas devuelta por la solicitud asociada.
MS-HAID: vspixengine.IFrameBufferCallback\_ResultCallback\_DWORD\_DWORD\_DWORD\_DWORD\_double\_DWORD\_BYTE\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IFrameBufferCallback:: ResultCallback (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F0276125-2DA9-45BC-A295-BD67C21EE601
api_name:
- IFrameBufferCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5433c7bbf5fe67455b60fd754eecb2c2877c5d6f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152368"
---
# <a name="span-idvspixengineiframebuffercallback_resultcallback_dword_dword_dword_dword_double_dword_byte_arrspaniframebuffercallbackresultcallback-method"></a><span data-ttu-id="4807a-103"><span id="vspixengine.iframebuffercallback_resultcallback_dword_dword_dword_dword_double_dword_byte_arr"></span>IFrameBufferCallback:: ResultCallback (método)</span><span class="sxs-lookup"><span data-stu-id="4807a-103"><span id="vspixengine.iframebuffercallback_resultcallback_dword_dword_dword_dword_double_dword_byte_arr"></span>IFrameBufferCallback::ResultCallback method</span></span>

<span data-ttu-id="4807a-104">Devolución de llamada que notifica al host la información de fotogramas devuelta por la solicitud asociada.</span><span class="sxs-lookup"><span data-stu-id="4807a-104">A callback that notifies the host of framebuffer information returned by the associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="4807a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4807a-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD   frameNumber,
   DWORD   width,
   DWORD   height,
   DWORD   renderTargetPtr,
   double  frameDuraction,
   DWORD   size,
   BYTE [] count5_buffer
);
```

## <a name="parameters"></a><span data-ttu-id="4807a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4807a-106">Parameters</span></span>

<span data-ttu-id="4807a-107">*Númeromarco* </span><span class="sxs-lookup"><span data-stu-id="4807a-107">*frameNumber* </span></span>  
<span data-ttu-id="4807a-108">Número de marco.</span><span class="sxs-lookup"><span data-stu-id="4807a-108">The frame number.</span></span>

<span data-ttu-id="4807a-109">*Ancho* </span><span class="sxs-lookup"><span data-stu-id="4807a-109">*width* </span></span>  
<span data-ttu-id="4807a-110">Ancho del marco.</span><span class="sxs-lookup"><span data-stu-id="4807a-110">The width of the frame.</span></span>

<span data-ttu-id="4807a-111">*alto* </span><span class="sxs-lookup"><span data-stu-id="4807a-111">*height* </span></span>  
<span data-ttu-id="4807a-112">Alto del marco.</span><span class="sxs-lookup"><span data-stu-id="4807a-112">The height of the frame.</span></span>

<span data-ttu-id="4807a-113">*renderTargetPtr* </span><span class="sxs-lookup"><span data-stu-id="4807a-113">*renderTargetPtr* </span></span>  
<span data-ttu-id="4807a-114">Destino de representación del que proceden los resultados.</span><span class="sxs-lookup"><span data-stu-id="4807a-114">The render target that the results come from.</span></span> <span data-ttu-id="4807a-115">Siempre es una ranura especificada por la solicitud de búfer de fotogramas, o si no es una llamada a Draw, entonces el primer RTV Bount al origen de salida.</span><span class="sxs-lookup"><span data-stu-id="4807a-115">It is always a slot specified by the frame buffer request, or if not a draw call, then the first RTV bount to the output source.</span></span>

<span data-ttu-id="4807a-116">*frameDuraction* </span><span class="sxs-lookup"><span data-stu-id="4807a-116">*frameDuraction* </span></span>  
<span data-ttu-id="4807a-117">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4807a-117">Not used.</span></span>

<span data-ttu-id="4807a-118">*ajusta* </span><span class="sxs-lookup"><span data-stu-id="4807a-118">*size* </span></span>  
<span data-ttu-id="4807a-119">Tamaño del búfer de salida en bytes.</span><span class="sxs-lookup"><span data-stu-id="4807a-119">The size of the output buffer in bytes.</span></span>

<span data-ttu-id="4807a-120">*\_búfer count5* </span><span class="sxs-lookup"><span data-stu-id="4807a-120">*count5\_buffer* </span></span>  
<span data-ttu-id="4807a-121">Contenido del destino de representación en formato R8G8B8A8 \_ UNORM.</span><span class="sxs-lookup"><span data-stu-id="4807a-121">The contents of the render target in R8G8B8A8\_UNORM format.</span></span>

## <a name="return-value"></a><span data-ttu-id="4807a-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4807a-122">Return value</span></span>

<span data-ttu-id="4807a-123">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="4807a-123">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4807a-124">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4807a-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4807a-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4807a-125">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="4807a-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4807a-126">Header</span></span></p></td><td><span data-ttu-id="4807a-127">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="4807a-127">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="4807a-128"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="4807a-128"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="4807a-129">**IFrameBufferCallback**</span><span class="sxs-lookup"><span data-stu-id="4807a-129">**IFrameBufferCallback**</span></span>](/windows/desktop/direct3dtools/iframebuffercallback)

 

 
