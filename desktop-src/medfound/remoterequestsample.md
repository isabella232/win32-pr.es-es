---
description: 'Versión remota del método IMFMediaStream:: RequestSample.'
ms.assetid: 05ed4de0-fe5c-4183-8f1d-55d5a27e436a
title: RemoteRequestSample (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c8b06f0501de9cc041bf5776adb5e17e59a8c17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705889"
---
# <a name="remoterequestsample"></a><span data-ttu-id="9b5ed-103">RemoteRequestSample</span><span class="sxs-lookup"><span data-stu-id="9b5ed-103">RemoteRequestSample</span></span>

<span data-ttu-id="9b5ed-104">Versión remota del método [**IMFMediaStream:: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) .</span><span class="sxs-lookup"><span data-stu-id="9b5ed-104">Remotable version of the [**IMFMediaStream::RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) method.</span></span>

``` syntax
[call_as(RequestSample)]
HRESULT RemoteRequestSample();
```

## <a name="remarks"></a><span data-ttu-id="9b5ed-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9b5ed-105">Remarks</span></span>

<span data-ttu-id="9b5ed-106">Las aplicaciones no pueden llamar directamente a este método y los objetos no implementan este método.</span><span class="sxs-lookup"><span data-stu-id="9b5ed-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="9b5ed-107">El método no aparece en la tabla vtable de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="9b5ed-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="9b5ed-108">Si se llama a [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) a través de los límites del proceso, el archivo DLL de Media Foundation proxy/stub traduce la llamada en una llamada al método remoto y, a continuación, la convierte de nuevo.</span><span class="sxs-lookup"><span data-stu-id="9b5ed-108">If [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b5ed-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b5ed-109">Requirements</span></span>



| <span data-ttu-id="9b5ed-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b5ed-110">Requirement</span></span> | <span data-ttu-id="9b5ed-111">Value</span><span class="sxs-lookup"><span data-stu-id="9b5ed-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b5ed-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b5ed-112">Minimum supported client</span></span><br/> | <span data-ttu-id="9b5ed-113">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="9b5ed-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="9b5ed-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b5ed-114">Minimum supported server</span></span><br/> | <span data-ttu-id="9b5ed-115">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="9b5ed-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="9b5ed-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9b5ed-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b5ed-117"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9b5ed-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="9b5ed-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9b5ed-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="9b5ed-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9b5ed-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="9b5ed-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="9b5ed-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b5ed-121">**IMFMediaStream**</span><span class="sxs-lookup"><span data-stu-id="9b5ed-121">**IMFMediaStream**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)
</dt> </dl>

 

 




