---
title: Propiedad ActiveBasicDevice IsSetNextSourceSupported (PlayToDevice. h)
description: Obtiene un valor que indica si se admite el establecimiento del código fuente siguiente.
ms.assetid: 0888A737-D2CC-4259-BC60-9D2B8E8302A0
keywords:
- Propiedad IsSetNextSourceSupported API de streaming de multimedia
- Propiedad IsSetNextSourceSupported API de streaming de multimedia, interfaz ActiveBasicDevice
- Interfaz ActiveBasicDevice API de streaming de multimedia, propiedad IsSetNextSourceSupported
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsSetNextSourceSupported
- ActiveBasicDevice.get_IsSetNextSourceSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b84190336678e677ad3f0436d7233a49d4587574
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714632"
---
# <a name="activebasicdeviceissetnextsourcesupported-property"></a><span data-ttu-id="78880-106">ActiveBasicDevice:: IsSetNextSourceSupported (propiedad)</span><span class="sxs-lookup"><span data-stu-id="78880-106">ActiveBasicDevice::IsSetNextSourceSupported property</span></span>

<span data-ttu-id="78880-107">Obtiene un valor que indica si se admite el establecimiento del código fuente siguiente.</span><span class="sxs-lookup"><span data-stu-id="78880-107">Gets a value that indicates if setting the next source is supported.</span></span>

<span data-ttu-id="78880-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="78880-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="78880-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="78880-109">Syntax</span></span>


```C++
HRESULT get_IsSetNextSourceSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a><span data-ttu-id="78880-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="78880-110">Property value</span></span>

<span data-ttu-id="78880-111">Un puntero a un **valor booleano** que indica si se admite el establecimiento del código fuente siguiente.</span><span class="sxs-lookup"><span data-stu-id="78880-111">A pointer to a **boolean** that indicates if setting the next source is supported.</span></span>

<span data-ttu-id="78880-112">**true** si se admite el establecimiento del código fuente siguiente; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="78880-112">**true** if setting the next source is supported; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="78880-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78880-113">Requirements</span></span>



| <span data-ttu-id="78880-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="78880-114">Requirement</span></span> | <span data-ttu-id="78880-115">Value</span><span class="sxs-lookup"><span data-stu-id="78880-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="78880-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="78880-116">Minimum supported client</span></span><br/> | <span data-ttu-id="78880-117">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="78880-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="78880-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="78880-118">Minimum supported server</span></span><br/> | <span data-ttu-id="78880-119">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="78880-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="78880-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="78880-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="78880-121"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="78880-121"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="78880-122">IDL</span><span class="sxs-lookup"><span data-stu-id="78880-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="78880-123"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="78880-123"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="78880-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="78880-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78880-125"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78880-125"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78880-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="78880-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="78880-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="78880-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

