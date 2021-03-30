---
description: 'Versión remota del método IMFWorkQueueServices:: BeginUnregisterTopologyWorkQueuesWithMMCSS.'
ms.assetid: 1a168462-400d-46c9-a489-7b861770469f
title: RemoteBeginUnregisterTopologyWorkQueuesWithMMCSS (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f52f82c55d692a2e1d9160c7a619338d82956ea0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910809"
---
# <a name="remotebeginunregistertopologyworkqueueswithmmcss"></a><span data-ttu-id="62507-103">RemoteBeginUnregisterTopologyWorkQueuesWithMMCSS</span><span class="sxs-lookup"><span data-stu-id="62507-103">RemoteBeginUnregisterTopologyWorkQueuesWithMMCSS</span></span>

<span data-ttu-id="62507-104">Versión remota del método [**IMFWorkQueueServices:: BeginUnregisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregistertopologyworkqueueswithmmcss) .</span><span class="sxs-lookup"><span data-stu-id="62507-104">Remotable version of the [**IMFWorkQueueServices::BeginUnregisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregistertopologyworkqueueswithmmcss) method.</span></span>

``` syntax
[call_as(BeginUnregisterTopologyWorkQueuesWithMMCSS)]
HRESULT RemoteBeginUnregisterTopologyWorkQueuesWithMMCSS(
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a><span data-ttu-id="62507-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="62507-105">Remarks</span></span>

<span data-ttu-id="62507-106">Las aplicaciones no pueden llamar directamente a este método y los objetos no implementan este método.</span><span class="sxs-lookup"><span data-stu-id="62507-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="62507-107">El método no aparece en la tabla vtable de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="62507-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="62507-108">Si se llama a [**BeginUnregisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregistertopologyworkqueueswithmmcss) a través de los límites del proceso, el archivo DLL de Media Foundation proxy/stub traduce la llamada en una llamada al método remoto y, a continuación, la convierte de nuevo.</span><span class="sxs-lookup"><span data-stu-id="62507-108">If [**BeginUnregisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregistertopologyworkqueueswithmmcss) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="62507-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62507-109">Requirements</span></span>



| <span data-ttu-id="62507-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="62507-110">Requirement</span></span> | <span data-ttu-id="62507-111">Value</span><span class="sxs-lookup"><span data-stu-id="62507-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62507-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62507-112">Minimum supported client</span></span><br/> | <span data-ttu-id="62507-113">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="62507-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="62507-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62507-114">Minimum supported server</span></span><br/> | <span data-ttu-id="62507-115">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="62507-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="62507-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="62507-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="62507-117"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="62507-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="62507-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="62507-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="62507-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="62507-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="62507-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="62507-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62507-121">**IMFWorkQueueServices**</span><span class="sxs-lookup"><span data-stu-id="62507-121">**IMFWorkQueueServices**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




