---
description: 'Versión remota del método IMFWorkQueueServices:: BeginRegisterTopologyWorkQueuesWithMMCSS.'
ms.assetid: 1ea258c9-1f7f-4324-a17a-d044a4864ea4
title: RemoteBeginRegisterTopologyWorkQueuesWithMMCSS (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 448008c29e34574263f04ebbc7dee54d60b6f4ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697616"
---
# <a name="remotebeginregistertopologyworkqueueswithmmcss"></a><span data-ttu-id="53683-103">RemoteBeginRegisterTopologyWorkQueuesWithMMCSS</span><span class="sxs-lookup"><span data-stu-id="53683-103">RemoteBeginRegisterTopologyWorkQueuesWithMMCSS</span></span>

<span data-ttu-id="53683-104">Versión remota del método [**IMFWorkQueueServices:: BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) .</span><span class="sxs-lookup"><span data-stu-id="53683-104">Remotable version of the [**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) method.</span></span>

``` syntax
[call_as(BeginRegisterTopologyWorkQueuesWithMMCSS)]
HRESULT RemoteBeginRegisterTopologyWorkQueuesWithMMCSS(
    IMFRemoteAsyncCallback *pCallback
); 
```

## <a name="remarks"></a><span data-ttu-id="53683-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="53683-105">Remarks</span></span>

<span data-ttu-id="53683-106">Las aplicaciones no pueden llamar directamente a este método y los objetos no implementan este método.</span><span class="sxs-lookup"><span data-stu-id="53683-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="53683-107">El método no aparece en la tabla vtable de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="53683-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="53683-108">Si se llama a [**BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) a través de los límites del proceso, el archivo DLL de Media Foundation proxy/stub traduce la llamada en una llamada al método remoto y, a continuación, la convierte de nuevo.</span><span class="sxs-lookup"><span data-stu-id="53683-108">If [**BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="53683-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53683-109">Requirements</span></span>



| <span data-ttu-id="53683-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="53683-110">Requirement</span></span> | <span data-ttu-id="53683-111">Value</span><span class="sxs-lookup"><span data-stu-id="53683-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53683-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53683-112">Minimum supported client</span></span><br/> | <span data-ttu-id="53683-113">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="53683-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="53683-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53683-114">Minimum supported server</span></span><br/> | <span data-ttu-id="53683-115">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="53683-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="53683-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="53683-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="53683-117"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="53683-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="53683-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="53683-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="53683-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="53683-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="53683-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="53683-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53683-121">**IMFWorkQueueServices**</span><span class="sxs-lookup"><span data-stu-id="53683-121">**IMFWorkQueueServices**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




