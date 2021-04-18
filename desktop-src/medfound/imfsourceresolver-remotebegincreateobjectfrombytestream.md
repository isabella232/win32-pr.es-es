---
description: 'Versión remota del método IMFSourceResolver:: BeginCreateObjectFromByteStream.'
ms.assetid: 960b5c51-b9b1-4956-a270-abfb7eedd482
title: RemoteBeginCreateObjectFromByteStream (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac2cf089f0b80e83373c36731de4bd9a36d8835b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705804"
---
# <a name="remotebegincreateobjectfrombytestream"></a><span data-ttu-id="f9e5a-103">RemoteBeginCreateObjectFromByteStream</span><span class="sxs-lookup"><span data-stu-id="f9e5a-103">RemoteBeginCreateObjectFromByteStream</span></span>

<span data-ttu-id="f9e5a-104">Versión remota del método [**IMFSourceResolver:: BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream) .</span><span class="sxs-lookup"><span data-stu-id="f9e5a-104">Remotable version of the [**IMFSourceResolver::BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream) method.</span></span>

``` syntax
[call_as(BeginCreateObjectFromByteStream)]
HRESULT RemoteBeginCreateObjectFromByteStream(
    IMFByteStream* pByteStream,
    LPCWSTR pwszURL,
    IPropertyStore *pProps,
    DWORD dwFlags,
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a><span data-ttu-id="f9e5a-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f9e5a-105">Remarks</span></span>

<span data-ttu-id="f9e5a-106">Las aplicaciones no pueden llamar directamente a este método y los objetos no implementan este método.</span><span class="sxs-lookup"><span data-stu-id="f9e5a-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="f9e5a-107">El método no aparece en la tabla vtable de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="f9e5a-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="f9e5a-108">Si se llama a [**BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream) a través de los límites del proceso, el archivo DLL de Media Foundation proxy/stub traduce la llamada en una llamada al método remoto y, a continuación, la convierte de nuevo.</span><span class="sxs-lookup"><span data-stu-id="f9e5a-108">If [**BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9e5a-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9e5a-109">Requirements</span></span>



| <span data-ttu-id="f9e5a-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9e5a-110">Requirement</span></span> | <span data-ttu-id="f9e5a-111">Value</span><span class="sxs-lookup"><span data-stu-id="f9e5a-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9e5a-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9e5a-112">Minimum supported client</span></span><br/> | <span data-ttu-id="f9e5a-113">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="f9e5a-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="f9e5a-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9e5a-114">Minimum supported server</span></span><br/> | <span data-ttu-id="f9e5a-115">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="f9e5a-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="f9e5a-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f9e5a-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9e5a-117"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f9e5a-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="f9e5a-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f9e5a-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="f9e5a-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f9e5a-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="f9e5a-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="f9e5a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9e5a-121">**IMFSourceResolver**</span><span class="sxs-lookup"><span data-stu-id="f9e5a-121">**IMFSourceResolver**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver)
</dt> </dl>

 

 




