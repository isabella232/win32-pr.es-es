---
title: Propiedad ActiveBasicDevice IsMuteSupported (PlayToDevice. h)
description: Obtiene un valor que indica si el dispositivo admite el silenciamiento del audio.
ms.assetid: FF4B533F-B416-4DBE-BF86-FA34E785FFA2
keywords:
- Propiedad IsMuteSupported API de streaming de multimedia
- Propiedad IsMuteSupported API de streaming de multimedia, interfaz ActiveBasicDevice
- Interfaz ActiveBasicDevice API de streaming de multimedia, propiedad IsMuteSupported
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsMuteSupported
- ActiveBasicDevice.get_IsMuteSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcec2e4520bd3b15b715c01e4369da87887355e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491261"
---
# <a name="activebasicdeviceismutesupported-property"></a><span data-ttu-id="7c289-106">ActiveBasicDevice:: IsMuteSupported (propiedad)</span><span class="sxs-lookup"><span data-stu-id="7c289-106">ActiveBasicDevice::IsMuteSupported property</span></span>

<span data-ttu-id="7c289-107">Obtiene un valor que indica si el dispositivo admite el silenciamiento del audio.</span><span class="sxs-lookup"><span data-stu-id="7c289-107">Gets a value that indicates if the device supports muting the audio.</span></span>

<span data-ttu-id="7c289-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7c289-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c289-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7c289-109">Syntax</span></span>


```C++
HRESULT get_IsMuteSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a><span data-ttu-id="7c289-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="7c289-110">Property value</span></span>

<span data-ttu-id="7c289-111">Un puntero a un **valor booleano** que indica si el dispositivo admite el silenciamiento del audio.</span><span class="sxs-lookup"><span data-stu-id="7c289-111">A pointer to a **boolean** that indicates if the device supports muting the audio.</span></span>

<span data-ttu-id="7c289-112">**true** si el dispositivo admite el silenciamiento del audio; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="7c289-112">**true** if the device supports muting the audio; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c289-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c289-113">Requirements</span></span>



| <span data-ttu-id="7c289-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c289-114">Requirement</span></span> | <span data-ttu-id="7c289-115">Value</span><span class="sxs-lookup"><span data-stu-id="7c289-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c289-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c289-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7c289-117">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="7c289-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7c289-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c289-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7c289-119">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="7c289-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7c289-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7c289-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c289-121"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c289-121"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="7c289-122">IDL</span><span class="sxs-lookup"><span data-stu-id="7c289-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7c289-123"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7c289-123"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="7c289-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7c289-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c289-125"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c289-125"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c289-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="7c289-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="7c289-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7c289-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

