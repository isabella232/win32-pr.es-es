---
description: 'Versión remota del método IMFMediaSource:: CreatePresentationDescriptor.'
ms.assetid: 9ad6793e-32ca-471b-8639-41098b3e8216
title: RemoteCreatePresentationDescriptor (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c02d78c1febe8c1a82ae3e91c50e06c750bcfef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155328"
---
# <a name="remotecreatepresentationdescriptor"></a><span data-ttu-id="6f5a7-103">RemoteCreatePresentationDescriptor</span><span class="sxs-lookup"><span data-stu-id="6f5a7-103">RemoteCreatePresentationDescriptor</span></span>

<span data-ttu-id="6f5a7-104">Versión remota del método [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) .</span><span class="sxs-lookup"><span data-stu-id="6f5a7-104">Remotable version of the [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) method.</span></span>

``` syntax
[call_as(CreatePresentationDescriptor)]
HRESULT RemoteCreatePresentationDescriptor(
    DWORD *pcbPD,
    BYTE **pbPD,
    IMFPresentationDescriptor **ppRemotePD
);
```

## <a name="remarks"></a><span data-ttu-id="6f5a7-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6f5a7-105">Remarks</span></span>

<span data-ttu-id="6f5a7-106">Las aplicaciones no pueden llamar directamente a este método y los objetos no implementan este método.</span><span class="sxs-lookup"><span data-stu-id="6f5a7-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="6f5a7-107">El método no aparece en la tabla vtable de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="6f5a7-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="6f5a7-108">Si se llama a [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) a través de los límites del proceso, el archivo DLL de Media Foundation proxy/stub traduce la llamada en una llamada al método remoto y, a continuación, la convierte de nuevo.</span><span class="sxs-lookup"><span data-stu-id="6f5a7-108">If [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f5a7-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f5a7-109">Requirements</span></span>



| <span data-ttu-id="6f5a7-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f5a7-110">Requirement</span></span> | <span data-ttu-id="6f5a7-111">Value</span><span class="sxs-lookup"><span data-stu-id="6f5a7-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f5a7-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f5a7-112">Minimum supported client</span></span><br/> | <span data-ttu-id="6f5a7-113">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="6f5a7-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="6f5a7-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f5a7-114">Minimum supported server</span></span><br/> | <span data-ttu-id="6f5a7-115">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="6f5a7-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="6f5a7-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6f5a7-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f5a7-117"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6f5a7-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="6f5a7-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6f5a7-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="6f5a7-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6f5a7-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="6f5a7-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f5a7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f5a7-121">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="6f5a7-121">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
</dt> </dl>

 

 




