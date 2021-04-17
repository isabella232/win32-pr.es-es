---
description: 'Versión remota del método IMFSourceResolver:: BeginCreateObjectFromURL.'
ms.assetid: 3c0b0aaf-832b-4708-bed9-6f448770ee77
title: RemoteBeginCreateObjectFromURL (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9d9a72ab5522b56fc0b78238f6a1dbc9aae0c6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705839"
---
# <a name="remotebegincreateobjectfromurl"></a><span data-ttu-id="f808c-103">RemoteBeginCreateObjectFromURL</span><span class="sxs-lookup"><span data-stu-id="f808c-103">RemoteBeginCreateObjectFromURL</span></span>

<span data-ttu-id="f808c-104">Versión remota del método [**IMFSourceResolver:: BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) .</span><span class="sxs-lookup"><span data-stu-id="f808c-104">Remotable version of the [**IMFSourceResolver::BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) method.</span></span>

``` syntax
[call_as(BeginCreateObjectFromURL)]
HRESULT RemoteBeginCreateObjectFromURL(
    LPCWSTR pwszURL,
    DWORD dwFlags,
    IPropertyStore *pProps,
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a><span data-ttu-id="f808c-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f808c-105">Remarks</span></span>

<span data-ttu-id="f808c-106">Las aplicaciones no pueden llamar directamente a este método y los objetos no implementan este método.</span><span class="sxs-lookup"><span data-stu-id="f808c-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="f808c-107">El método no aparece en la tabla vtable de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="f808c-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="f808c-108">Si se llama a [**BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) a través de los límites del proceso, el archivo DLL de Media Foundation proxy/stub traduce la llamada en una llamada al método remoto y, a continuación, la convierte de nuevo.</span><span class="sxs-lookup"><span data-stu-id="f808c-108">If [**BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="f808c-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f808c-109">Requirements</span></span>



| <span data-ttu-id="f808c-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="f808c-110">Requirement</span></span> | <span data-ttu-id="f808c-111">Value</span><span class="sxs-lookup"><span data-stu-id="f808c-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f808c-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f808c-112">Minimum supported client</span></span><br/> | <span data-ttu-id="f808c-113">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="f808c-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="f808c-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f808c-114">Minimum supported server</span></span><br/> | <span data-ttu-id="f808c-115">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="f808c-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="f808c-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f808c-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="f808c-117"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f808c-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="f808c-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f808c-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="f808c-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f808c-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="f808c-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="f808c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f808c-121">**IMFSourceResolver**</span><span class="sxs-lookup"><span data-stu-id="f808c-121">**IMFSourceResolver**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver)
</dt> </dl>

 

 




