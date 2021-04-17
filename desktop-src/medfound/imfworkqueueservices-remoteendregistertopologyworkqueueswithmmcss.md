---
description: 'Versión remota del método IMFWorkQueueServices:: EndRegisterTopologyWorkQueuesWithMMCSS.'
ms.assetid: 94dce412-6a72-4ddf-86a3-5176ee1eb6d2
title: RemoteEndRegisterTopologyWorkQueuesWithMMCSS (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3333becfcd7a3c5e2621b628b6435b96af017cf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697708"
---
# <a name="remoteendregistertopologyworkqueueswithmmcss"></a><span data-ttu-id="ef907-103">RemoteEndRegisterTopologyWorkQueuesWithMMCSS</span><span class="sxs-lookup"><span data-stu-id="ef907-103">RemoteEndRegisterTopologyWorkQueuesWithMMCSS</span></span>

<span data-ttu-id="ef907-104">Versión remota del método [**IMFWorkQueueServices:: EndRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregistertopologyworkqueueswithmmcss) .</span><span class="sxs-lookup"><span data-stu-id="ef907-104">Remotable version of the [**IMFWorkQueueServices::EndRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregistertopologyworkqueueswithmmcss) method.</span></span>

``` syntax
[call_as(EndRegisterTopologyWorkQueuesWithMMCSS)]
HRESULT RemoteEndRegisterTopologyWorkQueuesWithMMCSS(
    IUnknown *pResult
);
```

## <a name="remarks"></a><span data-ttu-id="ef907-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ef907-105">Remarks</span></span>

<span data-ttu-id="ef907-106">Las aplicaciones no pueden llamar directamente a este método y los objetos no implementan este método.</span><span class="sxs-lookup"><span data-stu-id="ef907-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="ef907-107">El método no aparece en la tabla vtable de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="ef907-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="ef907-108">Si se llama a [**EndRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregistertopologyworkqueueswithmmcss) a través de los límites del proceso, el archivo DLL de Media Foundation proxy/stub traduce la llamada en una llamada al método remoto y, a continuación, la convierte de nuevo.</span><span class="sxs-lookup"><span data-stu-id="ef907-108">If [**EndRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregistertopologyworkqueueswithmmcss) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef907-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef907-109">Requirements</span></span>



| <span data-ttu-id="ef907-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef907-110">Requirement</span></span> | <span data-ttu-id="ef907-111">Value</span><span class="sxs-lookup"><span data-stu-id="ef907-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef907-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef907-112">Minimum supported client</span></span><br/> | <span data-ttu-id="ef907-113">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ef907-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ef907-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef907-114">Minimum supported server</span></span><br/> | <span data-ttu-id="ef907-115">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ef907-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ef907-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ef907-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef907-117"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ef907-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="ef907-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ef907-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="ef907-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ef907-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="ef907-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="ef907-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef907-121">**IMFWorkQueueServices**</span><span class="sxs-lookup"><span data-stu-id="ef907-121">**IMFWorkQueueServices**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




