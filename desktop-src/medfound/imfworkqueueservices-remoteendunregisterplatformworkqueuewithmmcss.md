---
description: 'Versión remota del método IMFWorkQueueServices:: EndUnregisterPlatformWorkQueueWithMMCSS.'
ms.assetid: 92eef511-0af0-4146-ac81-7dfa4a649016
title: RemoteEndUnregisterPlatformWorkQueueWithMMCSS (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a03f8cdc1bfdded539c8143c3fa50c6bafb54de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912649"
---
# <a name="remoteendunregisterplatformworkqueuewithmmcss"></a><span data-ttu-id="b3d5e-103">RemoteEndUnregisterPlatformWorkQueueWithMMCSS</span><span class="sxs-lookup"><span data-stu-id="b3d5e-103">RemoteEndUnregisterPlatformWorkQueueWithMMCSS</span></span>

<span data-ttu-id="b3d5e-104">Versión remota del método [**IMFWorkQueueServices:: EndUnregisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregisterplatformworkqueuewithmmcss) .</span><span class="sxs-lookup"><span data-stu-id="b3d5e-104">Remotable version of the [**IMFWorkQueueServices::EndUnregisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregisterplatformworkqueuewithmmcss) method.</span></span>

``` syntax
[call_as(EndUnregisterPlatformWorkQueueWithMMCSS)]
HRESULT RemoteEndUnregisterPlatformWorkQueueWithMMCSS(
    IUnknown *pResult
);
```

## <a name="remarks"></a><span data-ttu-id="b3d5e-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b3d5e-105">Remarks</span></span>

<span data-ttu-id="b3d5e-106">Las aplicaciones no pueden llamar directamente a este método y los objetos no implementan este método.</span><span class="sxs-lookup"><span data-stu-id="b3d5e-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="b3d5e-107">El método no aparece en la tabla vtable de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="b3d5e-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="b3d5e-108">Si se llama a [**EndUnregisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregisterplatformworkqueuewithmmcss) a través de los límites del proceso, el archivo DLL de Media Foundation proxy/stub traduce la llamada en una llamada al método remoto y, a continuación, la convierte de nuevo.</span><span class="sxs-lookup"><span data-stu-id="b3d5e-108">If [**EndUnregisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregisterplatformworkqueuewithmmcss) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3d5e-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3d5e-109">Requirements</span></span>



| <span data-ttu-id="b3d5e-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3d5e-110">Requirement</span></span> | <span data-ttu-id="b3d5e-111">Value</span><span class="sxs-lookup"><span data-stu-id="b3d5e-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3d5e-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b3d5e-112">Minimum supported client</span></span><br/> | <span data-ttu-id="b3d5e-113">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b3d5e-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b3d5e-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b3d5e-114">Minimum supported server</span></span><br/> | <span data-ttu-id="b3d5e-115">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b3d5e-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b3d5e-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b3d5e-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3d5e-117"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b3d5e-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="b3d5e-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b3d5e-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="b3d5e-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b3d5e-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="b3d5e-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="b3d5e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3d5e-121">**IMFWorkQueueServices**</span><span class="sxs-lookup"><span data-stu-id="b3d5e-121">**IMFWorkQueueServices**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




