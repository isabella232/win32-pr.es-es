---
description: 'Versión remota de IMFWorkQueueServicesEX:: BeginRegisterPlatformWorkQueueWithMMCSSEx.'
ms.assetid: 75af7ce6-9b74-4d61-b7f2-5d07538f91cf
title: RemoteBeginRegisterPlatformWorkQueueWithMMCSSEx
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9d519d13f1e23927f1d34a18d5c5f860e007881
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278927"
---
# <a name="remotebeginregisterplatformworkqueuewithmmcssex"></a><span data-ttu-id="08101-103">RemoteBeginRegisterPlatformWorkQueueWithMMCSSEx</span><span class="sxs-lookup"><span data-stu-id="08101-103">RemoteBeginRegisterPlatformWorkQueueWithMMCSSEx</span></span>

<span data-ttu-id="08101-104">Versión remota de [**IMFWorkQueueServicesEX:: BeginRegisterPlatformWorkQueueWithMMCSSEx**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservicesex-beginregisterplatformworkqueuewithmmcssex).</span><span class="sxs-lookup"><span data-stu-id="08101-104">Remotable version of [**IMFWorkQueueServicesEX::BeginRegisterPlatformWorkQueueWithMMCSSEx**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservicesex-beginregisterplatformworkqueuewithmmcssex).</span></span>

``` syntax
[call_as(BeginRegisterPlatformWorkQueueWithMMCSSEx)]
HRESULT RemoteBeginRegisterPlatformWorkQueueWithMMCSSEx(
    DWORD dwPlatformWorkQueue,
    LPCWSTR wszClass,
    DWORD dwTaskId, 
    LONG lPriority,
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a><span data-ttu-id="08101-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="08101-105">Remarks</span></span>

<span data-ttu-id="08101-106">Las aplicaciones no pueden llamar directamente a este método y los objetos no implementan este método.</span><span class="sxs-lookup"><span data-stu-id="08101-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="08101-107">El método no aparece en la tabla vtable de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="08101-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="08101-108">Si se llama a [**BeginRegisterPlatformWorkQueueWithMMCSSEx**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservicesex-beginregisterplatformworkqueuewithmmcssex) a través de los límites del proceso, el archivo DLL de Media Foundation proxy/stub traduce la llamada en una llamada al método remoto y, a continuación, la convierte de nuevo.</span><span class="sxs-lookup"><span data-stu-id="08101-108">If [**BeginRegisterPlatformWorkQueueWithMMCSSEx**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservicesex-beginregisterplatformworkqueuewithmmcssex) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="08101-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08101-109">Requirements</span></span>



| <span data-ttu-id="08101-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="08101-110">Requirement</span></span> | <span data-ttu-id="08101-111">Value</span><span class="sxs-lookup"><span data-stu-id="08101-111">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="08101-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08101-112">Minimum supported client</span></span><br/> | <span data-ttu-id="08101-113">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="08101-113">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="08101-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08101-114">Minimum supported server</span></span><br/> | <span data-ttu-id="08101-115">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="08101-115">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="08101-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="08101-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="08101-117"><dt>Mfidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="08101-117"><dt>Mfidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08101-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="08101-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08101-119">**IMFWorkQueueServicesEx**</span><span class="sxs-lookup"><span data-stu-id="08101-119">**IMFWorkQueueServicesEx**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservicesex)
</dt> </dl>

 

 




