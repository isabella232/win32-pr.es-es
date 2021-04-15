---
title: Propiedad BitmapVirtualCache32BppSize de IMsRdpClientAdvancedSettings5
description: Establece o recupera el tamaño del archivo de caché virtual para mapas de bits de 32 bits por píxel (BPP).
ms.assetid: 7084293a-ae75-4711-a8d8-f813117333e7
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad BitmapVirtualCache32BppSize
- Propiedad BitmapVirtualCache32BppSize Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad BitmapVirtualCache32BppSize
- Propiedad BitmapVirtualCache32BppSize Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad BitmapVirtualCache32BppSize
- Propiedad BitmapVirtualCache32BppSize Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad BitmapVirtualCache32BppSize
- Propiedad BitmapVirtualCache32BppSize Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad BitmapVirtualCache32BppSize
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings5.get_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings5.put_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings6.BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings6.get_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings6.put_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings7.BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings7.get_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings7.put_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings8.BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings8.get_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings8.put_BitmapVirtualCache32BppSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d43de82b97e16fa36f83a5edde43712b2a9cbbb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422133"
---
# <a name="imsrdpclientadvancedsettings5bitmapvirtualcache32bppsize-property"></a><span data-ttu-id="19ffd-112">IMsRdpClientAdvancedSettings5:: BitmapVirtualCache32BppSize (propiedad)</span><span class="sxs-lookup"><span data-stu-id="19ffd-112">IMsRdpClientAdvancedSettings5::BitmapVirtualCache32BppSize property</span></span>

<span data-ttu-id="19ffd-113">Establece o recupera el tamaño del archivo de caché virtual para mapas de bits de 32 bits por píxel (BPP).</span><span class="sxs-lookup"><span data-stu-id="19ffd-113">Sets or retrieves the virtual cache file size for 32 bits per pixel (bpp) bitmaps.</span></span>

<span data-ttu-id="19ffd-114">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="19ffd-114">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="19ffd-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="19ffd-115">Syntax</span></span>


```C++
HRESULT put_BitmapVirtualCache32BppSize(
  [in]  LONG bitmapVirtualCache32BppSize
);

HRESULT get_BitmapVirtualCache32BppSize(
  [out] LONG *pbitmapVirtualCache32BppSize
);
```



## <a name="property-value"></a><span data-ttu-id="19ffd-116">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="19ffd-116">Property value</span></span>

<span data-ttu-id="19ffd-117">Establece el tamaño del archivo de caché virtual para los mapas de bits 32 bpp, en megabytes (MB).</span><span class="sxs-lookup"><span data-stu-id="19ffd-117">Sets the size of the virtual cache file for 32 bpp bitmaps, in megabytes (MB).</span></span> <span data-ttu-id="19ffd-118">El valor máximo es 48 MB.</span><span class="sxs-lookup"><span data-stu-id="19ffd-118">The maximum value is 48 MB.</span></span>

## <a name="requirements"></a><span data-ttu-id="19ffd-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19ffd-119">Requirements</span></span>



| <span data-ttu-id="19ffd-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="19ffd-120">Requirement</span></span> | <span data-ttu-id="19ffd-121">Value</span><span class="sxs-lookup"><span data-stu-id="19ffd-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19ffd-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="19ffd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="19ffd-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="19ffd-123">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="19ffd-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="19ffd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="19ffd-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="19ffd-125">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="19ffd-126">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="19ffd-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="19ffd-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19ffd-127"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="19ffd-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="19ffd-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19ffd-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19ffd-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="19ffd-130">IID</span><span class="sxs-lookup"><span data-stu-id="19ffd-130">IID</span></span><br/>                      | <span data-ttu-id="19ffd-131">IID \_ IMsRdpClientAdvancedSettings5 se define como FBA7F64E-6783-4405-DA45-FA4A763DABD0</span><span class="sxs-lookup"><span data-stu-id="19ffd-131">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="19ffd-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="19ffd-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19ffd-133">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="19ffd-133">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="19ffd-134">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="19ffd-134">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="19ffd-135">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="19ffd-135">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="19ffd-136">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="19ffd-136">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





