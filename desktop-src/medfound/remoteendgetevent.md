---
description: 'Versión remota del método IMFMediaEventGenerator:: EndGetEvent.'
ms.assetid: 5b793760-546c-43d4-8251-d89d8d7152ad
title: RemoteEndGetEvent (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66f3c4a5fe87dddf5fc1d256d61d8c863c2f1d9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811563"
---
# <a name="remoteendgetevent"></a><span data-ttu-id="89106-103">RemoteEndGetEvent</span><span class="sxs-lookup"><span data-stu-id="89106-103">RemoteEndGetEvent</span></span>

<span data-ttu-id="89106-104">Versión remota del método [**IMFMediaEventGenerator:: EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) .</span><span class="sxs-lookup"><span data-stu-id="89106-104">Remotable version of the [**IMFMediaEventGenerator::EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) method.</span></span>

``` syntax
[call_as(EndGetEvent)]
HRESULT RemoteEndGetEvent(
    IUnknown *pResult,
    DWORD *pcbEvent,
    BYTE **ppbEvent
);
```

## <a name="remarks"></a><span data-ttu-id="89106-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="89106-105">Remarks</span></span>

<span data-ttu-id="89106-106">Las aplicaciones no pueden llamar directamente a este método y los objetos no implementan este método.</span><span class="sxs-lookup"><span data-stu-id="89106-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="89106-107">El método no aparece en la tabla vtable de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="89106-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="89106-108">Si se llama a [**EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) a través de los límites del proceso, el archivo DLL de Media Foundation proxy/stub traduce la llamada en una llamada al método remoto y, a continuación, la convierte de nuevo.</span><span class="sxs-lookup"><span data-stu-id="89106-108">If [**EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="89106-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89106-109">Requirements</span></span>



| <span data-ttu-id="89106-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="89106-110">Requirement</span></span> | <span data-ttu-id="89106-111">Value</span><span class="sxs-lookup"><span data-stu-id="89106-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89106-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="89106-112">Minimum supported client</span></span><br/> | <span data-ttu-id="89106-113">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="89106-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="89106-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="89106-114">Minimum supported server</span></span><br/> | <span data-ttu-id="89106-115">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="89106-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="89106-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="89106-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="89106-117"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="89106-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="89106-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="89106-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="89106-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="89106-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="89106-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="89106-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89106-121">**IMFMediaEventGenerator**</span><span class="sxs-lookup"><span data-stu-id="89106-121">**IMFMediaEventGenerator**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
</dt> </dl>

 

 




