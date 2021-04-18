---
title: Propiedad ActiveBasicDevice IsVideoSupported (PlayToDevice. h)
description: Obtiene un valor que indica si el dispositivo admite vídeo.
ms.assetid: E8D33A04-748D-42F8-878F-35D973A6B559
keywords:
- Propiedad IsVideoSupported API de streaming de multimedia
- Propiedad IsVideoSupported API de streaming de multimedia, interfaz ActiveBasicDevice
- Interfaz ActiveBasicDevice API de streaming de multimedia, propiedad IsVideoSupported
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsVideoSupported
- ActiveBasicDevice.get_IsVideoSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2be369b34355b199cd47518065724242b9a422e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714639"
---
# <a name="activebasicdeviceisvideosupported-property"></a><span data-ttu-id="e3a24-106">ActiveBasicDevice:: IsVideoSupported (propiedad)</span><span class="sxs-lookup"><span data-stu-id="e3a24-106">ActiveBasicDevice::IsVideoSupported property</span></span>

<span data-ttu-id="e3a24-107">Obtiene un valor que indica si el dispositivo admite vídeo.</span><span class="sxs-lookup"><span data-stu-id="e3a24-107">Gets a value that indicates if the device supports video.</span></span>

<span data-ttu-id="e3a24-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e3a24-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3a24-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e3a24-109">Syntax</span></span>


```C++
HRESULT get_IsVideoSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a><span data-ttu-id="e3a24-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e3a24-110">Property value</span></span>

<span data-ttu-id="e3a24-111">Un puntero a un **valor booleano** que indica si el dispositivo admite vídeo.</span><span class="sxs-lookup"><span data-stu-id="e3a24-111">A pointer to a **boolean** that indicates if the device supports video.</span></span>

<span data-ttu-id="e3a24-112">**true** si el dispositivo admite vídeo; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="e3a24-112">**true** if the device supports video; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3a24-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3a24-113">Requirements</span></span>



| <span data-ttu-id="e3a24-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3a24-114">Requirement</span></span> | <span data-ttu-id="e3a24-115">Value</span><span class="sxs-lookup"><span data-stu-id="e3a24-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3a24-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3a24-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e3a24-117">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="e3a24-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e3a24-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3a24-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e3a24-119">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e3a24-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e3a24-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e3a24-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3a24-121"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3a24-121"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="e3a24-122">IDL</span><span class="sxs-lookup"><span data-stu-id="e3a24-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e3a24-123"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e3a24-123"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="e3a24-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e3a24-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3a24-125"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3a24-125"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3a24-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="e3a24-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="e3a24-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e3a24-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

