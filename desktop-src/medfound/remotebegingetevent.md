---
description: 'Versión remota del método IMFMediaEventGenerator:: BeginGetEvent.'
ms.assetid: 96a16fd3-10bc-4cd9-967a-ceb92e26ccc8
title: RemoteBeginGetEvent (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d728653df99baf0e816c53d8d22d7720c9aefac9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908374"
---
# <a name="remotebegingetevent"></a><span data-ttu-id="ca5b8-103">RemoteBeginGetEvent</span><span class="sxs-lookup"><span data-stu-id="ca5b8-103">RemoteBeginGetEvent</span></span>

<span data-ttu-id="ca5b8-104">Versión remota del método [**IMFMediaEventGenerator:: BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) .</span><span class="sxs-lookup"><span data-stu-id="ca5b8-104">Remotable version of the [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) method.</span></span>

``` syntax
[call_as(BeginGetEvent)]
HRESULT RemoteBeginGetEvent(
    IMFRemoteAsyncCallback* pCallback
);
```

## <a name="remarks"></a><span data-ttu-id="ca5b8-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ca5b8-105">Remarks</span></span>

<span data-ttu-id="ca5b8-106">Las aplicaciones no pueden llamar directamente a este método y los objetos no implementan este método.</span><span class="sxs-lookup"><span data-stu-id="ca5b8-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="ca5b8-107">El método no aparece en la tabla vtable de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="ca5b8-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="ca5b8-108">Si se llama a [**BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) a través de los límites del proceso, el archivo DLL de Media Foundation proxy/stub traduce la llamada en una llamada al método remoto y, a continuación, la convierte de nuevo.</span><span class="sxs-lookup"><span data-stu-id="ca5b8-108">If [**BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca5b8-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca5b8-109">Requirements</span></span>



| <span data-ttu-id="ca5b8-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca5b8-110">Requirement</span></span> | <span data-ttu-id="ca5b8-111">Value</span><span class="sxs-lookup"><span data-stu-id="ca5b8-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca5b8-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ca5b8-112">Minimum supported client</span></span><br/> | <span data-ttu-id="ca5b8-113">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="ca5b8-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="ca5b8-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ca5b8-114">Minimum supported server</span></span><br/> | <span data-ttu-id="ca5b8-115">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="ca5b8-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="ca5b8-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ca5b8-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca5b8-117"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ca5b8-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="ca5b8-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ca5b8-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="ca5b8-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ca5b8-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="ca5b8-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="ca5b8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca5b8-121">**IMFMediaEventGenerator**</span><span class="sxs-lookup"><span data-stu-id="ca5b8-121">**IMFMediaEventGenerator**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
</dt> </dl>

 

 




