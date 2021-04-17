---
description: 'Versión remota del método IMFWorkQueueServices:: BeginUnregisterPlatformWorkQueueWithMMCSS.'
ms.assetid: c3117086-268e-4e52-acfb-2c8167adaa07
title: RemoteBeginUnregisterPlatformWorkQueueWithMMCSS (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ab364f041d6bc8d0f6275879c82a937e98f463b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697761"
---
# <a name="remotebeginunregisterplatformworkqueuewithmmcss"></a><span data-ttu-id="4dc38-103">RemoteBeginUnregisterPlatformWorkQueueWithMMCSS</span><span class="sxs-lookup"><span data-stu-id="4dc38-103">RemoteBeginUnregisterPlatformWorkQueueWithMMCSS</span></span>

<span data-ttu-id="4dc38-104">Versión remota del método [**IMFWorkQueueServices:: BeginUnregisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregisterplatformworkqueuewithmmcss) .</span><span class="sxs-lookup"><span data-stu-id="4dc38-104">Remotable version of the [**IMFWorkQueueServices::BeginUnregisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregisterplatformworkqueuewithmmcss) method.</span></span>

``` syntax
[call_as(BeginUnregisterPlatformWorkQueueWithMMCSS)]
HRESULT RemoteBeginUnregisterPlatformWorkQueueWithMMCSS(
    DWORD dwPlatformWorkQueue,
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a><span data-ttu-id="4dc38-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4dc38-105">Remarks</span></span>

<span data-ttu-id="4dc38-106">Las aplicaciones no pueden llamar directamente a este método y los objetos no implementan este método.</span><span class="sxs-lookup"><span data-stu-id="4dc38-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="4dc38-107">El método no aparece en la tabla vtable de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="4dc38-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="4dc38-108">Si se llama a [**BeginUnregisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregisterplatformworkqueuewithmmcss) a través de los límites del proceso, el archivo DLL de Media Foundation proxy/stub traduce la llamada en una llamada al método remoto y, a continuación, la convierte de nuevo.</span><span class="sxs-lookup"><span data-stu-id="4dc38-108">If [**BeginUnregisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregisterplatformworkqueuewithmmcss) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="4dc38-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4dc38-109">Requirements</span></span>



| <span data-ttu-id="4dc38-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="4dc38-110">Requirement</span></span> | <span data-ttu-id="4dc38-111">Value</span><span class="sxs-lookup"><span data-stu-id="4dc38-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4dc38-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4dc38-112">Minimum supported client</span></span><br/> | <span data-ttu-id="4dc38-113">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4dc38-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4dc38-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4dc38-114">Minimum supported server</span></span><br/> | <span data-ttu-id="4dc38-115">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="4dc38-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4dc38-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4dc38-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="4dc38-117"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4dc38-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="4dc38-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4dc38-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="4dc38-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4dc38-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="4dc38-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="4dc38-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4dc38-121">**IMFWorkQueueServices**</span><span class="sxs-lookup"><span data-stu-id="4dc38-121">**IMFWorkQueueServices**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




