---
title: Propiedad ActiveBasicDevice IsSearchSupported (PlayToDevice. h)
description: Obtiene un valor que indica si el dispositivo admite la búsqueda.
ms.assetid: 091D467A-1FF6-4635-BF89-4E62AC9C660A
keywords:
- Propiedad IsSearchSupported API de streaming de multimedia
- Propiedad IsSearchSupported API de streaming de multimedia, interfaz ActiveBasicDevice
- Interfaz ActiveBasicDevice API de streaming de multimedia, propiedad IsSearchSupported
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsSearchSupported
- ActiveBasicDevice.get_IsSearchSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff97b20697388b1e3079f6993b97b948fa12091e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422587"
---
# <a name="activebasicdeviceissearchsupported-property"></a><span data-ttu-id="fcf3a-106">ActiveBasicDevice:: IsSearchSupported (propiedad)</span><span class="sxs-lookup"><span data-stu-id="fcf3a-106">ActiveBasicDevice::IsSearchSupported property</span></span>

<span data-ttu-id="fcf3a-107">Obtiene un valor que indica si el dispositivo admite la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="fcf3a-107">Gets a value that indicates if the device supports search.</span></span>

<span data-ttu-id="fcf3a-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="fcf3a-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcf3a-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fcf3a-109">Syntax</span></span>


```C++
HRESULT get_IsSearchSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a><span data-ttu-id="fcf3a-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="fcf3a-110">Property value</span></span>

<span data-ttu-id="fcf3a-111">Un puntero a un **valor booleano** que indica si el dispositivo admite la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="fcf3a-111">A pointer to a **boolean** that indicates if the device supports search.</span></span>

<span data-ttu-id="fcf3a-112">**true** si el dispositivo admite la búsqueda; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="fcf3a-112">**true** if the device supports search; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcf3a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fcf3a-113">Requirements</span></span>



| <span data-ttu-id="fcf3a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="fcf3a-114">Requirement</span></span> | <span data-ttu-id="fcf3a-115">Value</span><span class="sxs-lookup"><span data-stu-id="fcf3a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcf3a-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fcf3a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fcf3a-117">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="fcf3a-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="fcf3a-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fcf3a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fcf3a-119">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="fcf3a-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fcf3a-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fcf3a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fcf3a-121"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="fcf3a-121"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="fcf3a-122">IDL</span><span class="sxs-lookup"><span data-stu-id="fcf3a-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fcf3a-123"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fcf3a-123"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="fcf3a-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fcf3a-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fcf3a-125"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fcf3a-125"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fcf3a-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="fcf3a-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="fcf3a-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fcf3a-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

