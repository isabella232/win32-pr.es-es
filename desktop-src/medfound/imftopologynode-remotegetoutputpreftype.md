---
description: 'Versión remota del método IMFTopologyNode:: GetOutputPrefType.'
ms.assetid: 56fbbf14-0c55-4f98-bcda-7f434cff803c
title: RemoteGetOutputPrefType (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46069add8f9d15a2b3742a083a1cf169a46b969f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705803"
---
# <a name="remotegetoutputpreftype"></a><span data-ttu-id="c501a-103">RemoteGetOutputPrefType</span><span class="sxs-lookup"><span data-stu-id="c501a-103">RemoteGetOutputPrefType</span></span>

<span data-ttu-id="c501a-104">Versión remota del método [**IMFTopologyNode:: GetOutputPrefType**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getoutputpreftype) .</span><span class="sxs-lookup"><span data-stu-id="c501a-104">Remotable version of the [**IMFTopologyNode::GetOutputPrefType**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getoutputpreftype) method.</span></span>

``` syntax
[call_as(GetOutputPrefType)] 
HRESULT RemoteGetOutputPrefType(
    DWORD dwOutputIndex,
    DWORD *pcbData,
    BYTE **ppbData
);
```

## <a name="remarks"></a><span data-ttu-id="c501a-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c501a-105">Remarks</span></span>

<span data-ttu-id="c501a-106">Las aplicaciones no pueden llamar directamente a este método y los objetos no implementan este método.</span><span class="sxs-lookup"><span data-stu-id="c501a-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="c501a-107">El método no aparece en la tabla vtable de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="c501a-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="c501a-108">Si se llama a **GetOutputPrefType** a través de los límites del proceso, el archivo DLL de Media Foundation proxy/stub traduce la llamada en una llamada al método remoto y, a continuación, la convierte de nuevo.</span><span class="sxs-lookup"><span data-stu-id="c501a-108">If **GetOutputPrefType** is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="c501a-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c501a-109">Requirements</span></span>



| <span data-ttu-id="c501a-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="c501a-110">Requirement</span></span> | <span data-ttu-id="c501a-111">Value</span><span class="sxs-lookup"><span data-stu-id="c501a-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c501a-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c501a-112">Minimum supported client</span></span><br/> | <span data-ttu-id="c501a-113">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c501a-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c501a-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c501a-114">Minimum supported server</span></span><br/> | <span data-ttu-id="c501a-115">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="c501a-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c501a-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c501a-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="c501a-117"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c501a-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="c501a-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c501a-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="c501a-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c501a-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="c501a-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="c501a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c501a-121">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="c501a-121">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 




