---
title: Propiedad ActiveBasicDevice IsAudioSupported (PlayToDevice. h)
description: Obtiene un valor que indica si el dispositivo admite audio.
ms.assetid: 22ABB97B-58E7-4C21-B359-C10DFC9C7194
keywords:
- Propiedad IsAudioSupported API de streaming de multimedia
- Propiedad IsAudioSupported API de streaming de multimedia, interfaz ActiveBasicDevice
- Interfaz ActiveBasicDevice API de streaming de multimedia, propiedad IsAudioSupported
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsAudioSupported
- ActiveBasicDevice.get_IsAudioSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66058da9dcdbac0ed1100b0ef21a4ed530d45a68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079747"
---
# <a name="activebasicdeviceisaudiosupported-property"></a><span data-ttu-id="496fa-106">ActiveBasicDevice:: IsAudioSupported (propiedad)</span><span class="sxs-lookup"><span data-stu-id="496fa-106">ActiveBasicDevice::IsAudioSupported property</span></span>

<span data-ttu-id="496fa-107">Obtiene un valor que indica si el dispositivo admite audio.</span><span class="sxs-lookup"><span data-stu-id="496fa-107">Gets a value that indicates if the device supports audio.</span></span>

<span data-ttu-id="496fa-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="496fa-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="496fa-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="496fa-109">Syntax</span></span>


```C++
HRESULT get_IsAudioSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a><span data-ttu-id="496fa-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="496fa-110">Property value</span></span>

<span data-ttu-id="496fa-111">Un puntero a un **valor booleano** que indica si el dispositivo admite audio.</span><span class="sxs-lookup"><span data-stu-id="496fa-111">A pointer to a **boolean** that indicates if the device supports audio.</span></span>

<span data-ttu-id="496fa-112">**true** si el dispositivo admite audio; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="496fa-112">**true** if the device supports audio; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="496fa-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="496fa-113">Requirements</span></span>



| <span data-ttu-id="496fa-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="496fa-114">Requirement</span></span> | <span data-ttu-id="496fa-115">Value</span><span class="sxs-lookup"><span data-stu-id="496fa-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="496fa-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="496fa-116">Minimum supported client</span></span><br/> | <span data-ttu-id="496fa-117">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="496fa-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="496fa-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="496fa-118">Minimum supported server</span></span><br/> | <span data-ttu-id="496fa-119">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="496fa-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="496fa-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="496fa-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="496fa-121"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="496fa-121"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="496fa-122">IDL</span><span class="sxs-lookup"><span data-stu-id="496fa-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="496fa-123"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="496fa-123"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="496fa-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="496fa-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="496fa-125"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="496fa-125"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="496fa-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="496fa-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="496fa-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="496fa-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

