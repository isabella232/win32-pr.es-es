---
description: 'Versión remota del método IMFSourceResolver:: EndCreateObjectFromByteStream.'
ms.assetid: 6e4e9ace-e18a-45df-b20c-28e352fcdee7
title: RemoteEndCreateObjectFromByteStream (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ba53b7d22ed79cb97edba034dc4c61d9aa27fa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154996"
---
# <a name="remoteendcreateobjectfrombytestream"></a><span data-ttu-id="d0f36-103">RemoteEndCreateObjectFromByteStream</span><span class="sxs-lookup"><span data-stu-id="d0f36-103">RemoteEndCreateObjectFromByteStream</span></span>

<span data-ttu-id="d0f36-104">Versión remota del método [**IMFSourceResolver:: EndCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfrombytestream) .</span><span class="sxs-lookup"><span data-stu-id="d0f36-104">Remotable version of the [**IMFSourceResolver::EndCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfrombytestream) method.</span></span>

``` syntax
[call_as(EndCreateObjectFromByteStream)]
HRESULT RemoteEndCreateObjectFromByteStream(
    IUnknown *pResult,
    MF_OBJECT_TYPE *pObjectType,
    IUnknown **ppObject
);
```

## <a name="remarks"></a><span data-ttu-id="d0f36-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d0f36-105">Remarks</span></span>

<span data-ttu-id="d0f36-106">Las aplicaciones no pueden llamar directamente a este método y los objetos no implementan este método.</span><span class="sxs-lookup"><span data-stu-id="d0f36-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="d0f36-107">El método no aparece en la tabla vtable de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="d0f36-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="d0f36-108">Si se llama a [**EndCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfrombytestream) a través de los límites del proceso, el archivo DLL de Media Foundation proxy/stub traduce la llamada en una llamada al método remoto y, a continuación, la convierte de nuevo.</span><span class="sxs-lookup"><span data-stu-id="d0f36-108">If [**EndCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfrombytestream) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0f36-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0f36-109">Requirements</span></span>



| <span data-ttu-id="d0f36-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0f36-110">Requirement</span></span> | <span data-ttu-id="d0f36-111">Value</span><span class="sxs-lookup"><span data-stu-id="d0f36-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0f36-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0f36-112">Minimum supported client</span></span><br/> | <span data-ttu-id="d0f36-113">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="d0f36-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="d0f36-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0f36-114">Minimum supported server</span></span><br/> | <span data-ttu-id="d0f36-115">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="d0f36-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="d0f36-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d0f36-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0f36-117"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d0f36-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="d0f36-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d0f36-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="d0f36-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d0f36-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="d0f36-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0f36-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0f36-121">**IMFSourceResolver**</span><span class="sxs-lookup"><span data-stu-id="d0f36-121">**IMFSourceResolver**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver)
</dt> </dl>

 

 




