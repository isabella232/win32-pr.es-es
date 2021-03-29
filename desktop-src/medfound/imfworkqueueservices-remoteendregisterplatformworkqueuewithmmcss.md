---
description: 'Versión remota del método IMFWorkQueueServices:: EndRegisterPlatformWorkQueueWithMMCSS.'
ms.assetid: cb15129e-a3ad-4351-a7d6-dd4b883437bd
title: RemoteEndRegisterPlatformWorkQueueWithMMCSS (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 673281a8ed4e4c4174ecd2d874e7032776ea44c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808048"
---
# <a name="remoteendregisterplatformworkqueuewithmmcss"></a><span data-ttu-id="00c9c-103">RemoteEndRegisterPlatformWorkQueueWithMMCSS</span><span class="sxs-lookup"><span data-stu-id="00c9c-103">RemoteEndRegisterPlatformWorkQueueWithMMCSS</span></span>

<span data-ttu-id="00c9c-104">Versión remota del método [**IMFWorkQueueServices:: EndRegisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregisterplatformworkqueuewithmmcss) .</span><span class="sxs-lookup"><span data-stu-id="00c9c-104">Remotable version of the [**IMFWorkQueueServices::EndRegisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregisterplatformworkqueuewithmmcss) method.</span></span>

``` syntax
[call_as(EndRegisterPlatformWorkQueueWithMMCSS)]
HRESULT RemoteEndRegisterPlatformWorkQueueWithMMCSS(
    IUnknown *pResult,
    DWORD *pdwTaskId
);
```

## <a name="remarks"></a><span data-ttu-id="00c9c-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="00c9c-105">Remarks</span></span>

<span data-ttu-id="00c9c-106">Las aplicaciones no pueden llamar directamente a este método y los objetos no implementan este método.</span><span class="sxs-lookup"><span data-stu-id="00c9c-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="00c9c-107">El método no aparece en la tabla vtable de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="00c9c-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="00c9c-108">Si se llama a [**EndRegisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregisterplatformworkqueuewithmmcss) a través de los límites del proceso, el archivo DLL de Media Foundation proxy/stub traduce la llamada en una llamada al método remoto y, a continuación, la convierte de nuevo.</span><span class="sxs-lookup"><span data-stu-id="00c9c-108">If [**EndRegisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregisterplatformworkqueuewithmmcss) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="00c9c-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00c9c-109">Requirements</span></span>



| <span data-ttu-id="00c9c-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="00c9c-110">Requirement</span></span> | <span data-ttu-id="00c9c-111">Value</span><span class="sxs-lookup"><span data-stu-id="00c9c-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00c9c-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="00c9c-112">Minimum supported client</span></span><br/> | <span data-ttu-id="00c9c-113">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="00c9c-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="00c9c-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="00c9c-114">Minimum supported server</span></span><br/> | <span data-ttu-id="00c9c-115">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="00c9c-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="00c9c-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="00c9c-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="00c9c-117"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="00c9c-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="00c9c-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="00c9c-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="00c9c-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="00c9c-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="00c9c-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="00c9c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00c9c-121">**IMFWorkQueueServices**</span><span class="sxs-lookup"><span data-stu-id="00c9c-121">**IMFWorkQueueServices**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




