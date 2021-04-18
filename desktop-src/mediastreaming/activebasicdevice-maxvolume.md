---
title: Propiedad ActiveBasicDevice MaxVolume (PlayToDevice. h)
description: Obtiene el volumen máximo compatible con el dispositivo.
ms.assetid: EA0EC323-4A18-4CC1-8FA4-7BD302318863
keywords:
- Propiedad MaxVolume API de streaming de multimedia
- Propiedad MaxVolume API de streaming de multimedia, interfaz ActiveBasicDevice
- Interfaz ActiveBasicDevice API de streaming de multimedia, propiedad MaxVolume
topic_type:
- apiref
api_name:
- ActiveBasicDevice.MaxVolume
- ActiveBasicDevice.get_MaxVolume
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b48c25ef6c0e25c35ba07914c00fb063b4e8dc79
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492982"
---
# <a name="activebasicdevicemaxvolume-property"></a><span data-ttu-id="8d299-106">ActiveBasicDevice:: MaxVolume (propiedad)</span><span class="sxs-lookup"><span data-stu-id="8d299-106">ActiveBasicDevice::MaxVolume property</span></span>

<span data-ttu-id="8d299-107">Obtiene el volumen máximo compatible con el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8d299-107">Gets the maximum volume supported by the device.</span></span>

<span data-ttu-id="8d299-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="8d299-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d299-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8d299-109">Syntax</span></span>


```C++
HRESULT get_MaxVolume(
  [out] boolean *UINT32
);
```



## <a name="property-value"></a><span data-ttu-id="8d299-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="8d299-110">Property value</span></span>

<span data-ttu-id="8d299-111">Un puntero a un **UINT32** que especifica el volumen máximo admitido por el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8d299-111">A pointer to a **UINT32** that specifies the maximum volume supported by the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d299-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d299-112">Requirements</span></span>



| <span data-ttu-id="8d299-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d299-113">Requirement</span></span> | <span data-ttu-id="8d299-114">Value</span><span class="sxs-lookup"><span data-stu-id="8d299-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d299-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8d299-115">Minimum supported client</span></span><br/> | <span data-ttu-id="8d299-116">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="8d299-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8d299-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8d299-117">Minimum supported server</span></span><br/> | <span data-ttu-id="8d299-118">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="8d299-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8d299-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8d299-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d299-120"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d299-120"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="8d299-121">IDL</span><span class="sxs-lookup"><span data-stu-id="8d299-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8d299-122"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8d299-122"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="8d299-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8d299-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d299-124"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d299-124"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d299-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="8d299-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="8d299-126">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8d299-126">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

