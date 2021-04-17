---
description: 'Versión remota del método IMFSourceResolver:: EndCreateObjectFromURL.'
ms.assetid: 42764869-9cbc-4f41-a3af-f2d869db9f99
title: RemoteEndCreateObjectFromURL (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26fff650dca012b58dc6fd46b26f13b1c2ac3c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705785"
---
# <a name="remoteendcreateobjectfromurl"></a><span data-ttu-id="46b23-103">RemoteEndCreateObjectFromURL</span><span class="sxs-lookup"><span data-stu-id="46b23-103">RemoteEndCreateObjectFromURL</span></span>

<span data-ttu-id="46b23-104">Versión remota del método [**IMFSourceResolver:: EndCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfromurl) .</span><span class="sxs-lookup"><span data-stu-id="46b23-104">Remotable version of the [**IMFSourceResolver::EndCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfromurl) method.</span></span>

``` syntax
[call_as(EndCreateObjectFromURL)]
HRESULT RemoteEndCreateObjectFromURL(
    IUnknown *pResult,
    MF_OBJECT_TYPE *pObjectType,
    IUnknown **ppObject
);
```

## <a name="remarks"></a><span data-ttu-id="46b23-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="46b23-105">Remarks</span></span>

<span data-ttu-id="46b23-106">Las aplicaciones no pueden llamar directamente a este método y los objetos no implementan este método.</span><span class="sxs-lookup"><span data-stu-id="46b23-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="46b23-107">El método no aparece en la tabla vtable de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="46b23-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="46b23-108">Si se llama a [**EndCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfromurl) a través de los límites del proceso, el archivo DLL de Media Foundation proxy/stub traduce la llamada en una llamada al método remoto y, a continuación, la convierte de nuevo.</span><span class="sxs-lookup"><span data-stu-id="46b23-108">If [**EndCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfromurl) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="46b23-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46b23-109">Requirements</span></span>



| <span data-ttu-id="46b23-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="46b23-110">Requirement</span></span> | <span data-ttu-id="46b23-111">Value</span><span class="sxs-lookup"><span data-stu-id="46b23-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46b23-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="46b23-112">Minimum supported client</span></span><br/> | <span data-ttu-id="46b23-113">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="46b23-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="46b23-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="46b23-114">Minimum supported server</span></span><br/> | <span data-ttu-id="46b23-115">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="46b23-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="46b23-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="46b23-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="46b23-117"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="46b23-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="46b23-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="46b23-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="46b23-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="46b23-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="46b23-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="46b23-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46b23-121">**IMFSourceResolver**</span><span class="sxs-lookup"><span data-stu-id="46b23-121">**IMFSourceResolver**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver)
</dt> </dl>

 

 




