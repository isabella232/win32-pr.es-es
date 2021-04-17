---
description: 'Versión remota del método IMFWorkQueueServices:: EndUnregisterTopologyWorkQueuesWithMMCSS.'
ms.assetid: 8767a145-07b9-4427-9446-cee25e9074fa
title: RemoteEndUnregisterTopologyWorkQueuesWithMMCSS (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd1131fcd920e306bc6d5f2954c283d41d61310f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716356"
---
# <a name="remoteendunregistertopologyworkqueueswithmmcss"></a><span data-ttu-id="fc1e9-103">RemoteEndUnregisterTopologyWorkQueuesWithMMCSS</span><span class="sxs-lookup"><span data-stu-id="fc1e9-103">RemoteEndUnregisterTopologyWorkQueuesWithMMCSS</span></span>

<span data-ttu-id="fc1e9-104">Versión remota del método [**IMFWorkQueueServices:: EndUnregisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregistertopologyworkqueueswithmmcss) .</span><span class="sxs-lookup"><span data-stu-id="fc1e9-104">Remotable version of the [**IMFWorkQueueServices::EndUnregisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregistertopologyworkqueueswithmmcss) method.</span></span>

``` syntax
[call_as(EndUnregisterTopologyWorkQueuesWithMMCSS)]
HRESULT RemoteEndUnregisterTopologyWorkQueuesWithMMCSS(
    IUnknown *pResult
);
```

## <a name="remarks"></a><span data-ttu-id="fc1e9-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fc1e9-105">Remarks</span></span>

<span data-ttu-id="fc1e9-106">Las aplicaciones no pueden llamar directamente a este método y los objetos no implementan este método.</span><span class="sxs-lookup"><span data-stu-id="fc1e9-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="fc1e9-107">El método no aparece en la tabla vtable de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="fc1e9-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="fc1e9-108">Si se llama a [**EndUnregisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregistertopologyworkqueueswithmmcss) a través de los límites del proceso, el archivo DLL de Media Foundation proxy/stub traduce la llamada en una llamada al método remoto y, a continuación, la convierte de nuevo.</span><span class="sxs-lookup"><span data-stu-id="fc1e9-108">If [**EndUnregisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregistertopologyworkqueueswithmmcss) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc1e9-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc1e9-109">Requirements</span></span>



| <span data-ttu-id="fc1e9-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc1e9-110">Requirement</span></span> | <span data-ttu-id="fc1e9-111">Value</span><span class="sxs-lookup"><span data-stu-id="fc1e9-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc1e9-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc1e9-112">Minimum supported client</span></span><br/> | <span data-ttu-id="fc1e9-113">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="fc1e9-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fc1e9-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc1e9-114">Minimum supported server</span></span><br/> | <span data-ttu-id="fc1e9-115">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="fc1e9-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fc1e9-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fc1e9-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc1e9-117"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fc1e9-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="fc1e9-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fc1e9-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="fc1e9-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fc1e9-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="fc1e9-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="fc1e9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc1e9-121">**IMFWorkQueueServices**</span><span class="sxs-lookup"><span data-stu-id="fc1e9-121">**IMFWorkQueueServices**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




