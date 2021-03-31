---
title: Propiedad ActiveBasicDevice PhysicalNetworkInterface (PlayToDevice. h)
description: Obtiene el identificador de la interfaz de red física.
ms.assetid: F426462F-CE26-4EE1-B679-A4C80B2919A5
keywords:
- Propiedad PhysicalNetworkInterface API de streaming de multimedia
- Propiedad PhysicalNetworkInterface API de streaming de multimedia, interfaz ActiveBasicDevice
- Interfaz ActiveBasicDevice API de streaming de multimedia, propiedad PhysicalNetworkInterface
topic_type:
- apiref
api_name:
- ActiveBasicDevice.PhysicalNetworkInterface
- ActiveBasicDevice.get_PhysicalNetworkInterface
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 479618ed4d22a3d78a351fb88fcb1108a27c618f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491260"
---
# <a name="activebasicdevicephysicalnetworkinterface-property"></a><span data-ttu-id="a16ec-106">ActiveBasicDevice::P propiedad hysicalNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a16ec-106">ActiveBasicDevice::PhysicalNetworkInterface property</span></span>

<span data-ttu-id="a16ec-107">Obtiene el identificador de la interfaz de red física.</span><span class="sxs-lookup"><span data-stu-id="a16ec-107">Gets the id of the physical network interface.</span></span>

<span data-ttu-id="a16ec-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a16ec-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a16ec-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a16ec-109">Syntax</span></span>


```C++
HRESULT get_PhysicalNetworkInterface(
  [out] GUID *value
);
```



## <a name="property-value"></a><span data-ttu-id="a16ec-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="a16ec-110">Property value</span></span>

<span data-ttu-id="a16ec-111">Un puntero a un **GUID** que especifica el identificador de la interfaz de red física.</span><span class="sxs-lookup"><span data-stu-id="a16ec-111">A pointer to a **GUID** that specifies the id of the physical network interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="a16ec-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a16ec-112">Requirements</span></span>



| <span data-ttu-id="a16ec-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="a16ec-113">Requirement</span></span> | <span data-ttu-id="a16ec-114">Value</span><span class="sxs-lookup"><span data-stu-id="a16ec-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a16ec-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a16ec-115">Minimum supported client</span></span><br/> | <span data-ttu-id="a16ec-116">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="a16ec-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a16ec-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a16ec-117">Minimum supported server</span></span><br/> | <span data-ttu-id="a16ec-118">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a16ec-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a16ec-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a16ec-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="a16ec-120"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="a16ec-120"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="a16ec-121">IDL</span><span class="sxs-lookup"><span data-stu-id="a16ec-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a16ec-122"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a16ec-122"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="a16ec-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a16ec-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a16ec-124"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a16ec-124"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a16ec-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="a16ec-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="a16ec-126">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a16ec-126">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

