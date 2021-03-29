---
description: 'Versión remota del método IMFTopologyNode:: GetInputPrefType.'
ms.assetid: b02cf739-97a9-4bb0-abb1-0da491857c50
title: RemoteGetInputPrefType (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6461e804d6066b467378742ff02c8e708f5f6714
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810814"
---
# <a name="remotegetinputpreftype"></a><span data-ttu-id="30833-103">RemoteGetInputPrefType</span><span class="sxs-lookup"><span data-stu-id="30833-103">RemoteGetInputPrefType</span></span>

<span data-ttu-id="30833-104">Versión remota del método [**IMFTopologyNode:: GetInputPrefType**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinputpreftype) .</span><span class="sxs-lookup"><span data-stu-id="30833-104">Remotable version of the [**IMFTopologyNode::GetInputPrefType**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinputpreftype) method.</span></span>

``` syntax
[call_as(GetInputPrefType)] 
HRESULT RemoteGetInputPrefType(
    DWORD dwInputIndex,
    DWORD *pcbData,
    BYTE **ppbData
);
```

## <a name="remarks"></a><span data-ttu-id="30833-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="30833-105">Remarks</span></span>

<span data-ttu-id="30833-106">Las aplicaciones no pueden llamar directamente a este método y los objetos no implementan este método.</span><span class="sxs-lookup"><span data-stu-id="30833-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="30833-107">El método no aparece en la tabla vtable de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="30833-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="30833-108">Si se llama a [**GetInputPrefType**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinputpreftype) a través de los límites del proceso, el archivo DLL de Media Foundation proxy/stub traduce la llamada en una llamada al método remoto y, a continuación, la convierte de nuevo.</span><span class="sxs-lookup"><span data-stu-id="30833-108">If [**GetInputPrefType**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinputpreftype) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="30833-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30833-109">Requirements</span></span>



| <span data-ttu-id="30833-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="30833-110">Requirement</span></span> | <span data-ttu-id="30833-111">Value</span><span class="sxs-lookup"><span data-stu-id="30833-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30833-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30833-112">Minimum supported client</span></span><br/> | <span data-ttu-id="30833-113">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="30833-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="30833-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30833-114">Minimum supported server</span></span><br/> | <span data-ttu-id="30833-115">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="30833-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="30833-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="30833-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="30833-117"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="30833-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="30833-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="30833-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="30833-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="30833-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="30833-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="30833-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30833-121">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="30833-121">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 




