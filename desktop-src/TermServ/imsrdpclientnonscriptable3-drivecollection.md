---
title: Propiedad DriveCollection de IMsRdpClientNonScriptable3
description: Recupera la colección de objetos de unidad que se va a redirigir.
ms.assetid: 5aaac605-584b-442e-9d67-1cb8213a70b3
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad DriveCollection
- Propiedad DriveCollection Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable3, propiedad DriveCollection
- Propiedad DriveCollection Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable4, propiedad DriveCollection
- Propiedad DriveCollection Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad DriveCollection
- Servicios de Escritorio remoto de la propiedad DriveCollection, objeto MsRdpClient5
- Servicios de Escritorio remoto de objeto MsRdpClient5, propiedad DriveCollection
- Servicios de Escritorio remoto de la propiedad DriveCollection, objeto MsRdpClient6
- Servicios de Escritorio remoto de objeto MsRdpClient6, propiedad DriveCollection
- Servicios de Escritorio remoto de la propiedad DriveCollection, objeto MsRdpClient7
- Servicios de Escritorio remoto de objeto MsRdpClient7, propiedad DriveCollection
- Servicios de Escritorio remoto de la propiedad DriveCollection, objeto MsRdpClient8
- Servicios de Escritorio remoto de objeto MsRdpClient8, propiedad DriveCollection
- Servicios de Escritorio remoto de la propiedad DriveCollection, objeto MsRdpClient9
- Servicios de Escritorio remoto de objeto MsRdpClient9, propiedad DriveCollection
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.DriveCollection
- IMsRdpClientNonScriptable3.get_DriveCollection
- IMsRdpClientNonScriptable4.DriveCollection
- IMsRdpClientNonScriptable4.get_DriveCollection
- IMsRdpClientNonScriptable5.DriveCollection
- IMsRdpClientNonScriptable5.get_DriveCollection
- MsRdpClient5.DriveCollection
- MsRdpClient6.DriveCollection
- MsRdpClient7.DriveCollection
- MsRdpClient8.DriveCollection
- MsRdpClient9.DriveCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37d4bfcaa52d483adc8b0d0885d8316f10ce01d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489676"
---
# <a name="imsrdpclientnonscriptable3drivecollection-property"></a><span data-ttu-id="5b92c-120">IMsRdpClientNonScriptable3::D propiedad riveCollection</span><span class="sxs-lookup"><span data-stu-id="5b92c-120">IMsRdpClientNonScriptable3::DriveCollection property</span></span>

<span data-ttu-id="5b92c-121">Recupera la colección de objetos de unidad que se va a redirigir.</span><span class="sxs-lookup"><span data-stu-id="5b92c-121">Retrieves the collection of drive objects to be redirected.</span></span>

<span data-ttu-id="5b92c-122">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5b92c-122">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b92c-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5b92c-123">Syntax</span></span>


```C++
HRESULT get_DriveCollection(
  [out] IMsRdpDriveCollection **ppDriveCollection
);
```



## <a name="property-value"></a><span data-ttu-id="5b92c-124">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="5b92c-124">Property value</span></span>

<span data-ttu-id="5b92c-125">Recupera la colección de objetos Drive de tipo [**IMSRdpDrive**](imsrdpdrive.md).</span><span class="sxs-lookup"><span data-stu-id="5b92c-125">Retrieves the collection of drive objects of type [**IMSRdpDrive**](imsrdpdrive.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5b92c-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b92c-126">Requirements</span></span>



| <span data-ttu-id="5b92c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b92c-127">Requirement</span></span> | <span data-ttu-id="5b92c-128">Value</span><span class="sxs-lookup"><span data-stu-id="5b92c-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b92c-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5b92c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5b92c-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5b92c-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="5b92c-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5b92c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5b92c-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5b92c-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="5b92c-133">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="5b92c-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="5b92c-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b92c-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="5b92c-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5b92c-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b92c-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b92c-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="5b92c-137">IID</span><span class="sxs-lookup"><span data-stu-id="5b92c-137">IID</span></span><br/>                      | <span data-ttu-id="5b92c-138">IID \_ IMsRdpClientNonScriptable3 se define como b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="5b92c-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5b92c-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="5b92c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b92c-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="5b92c-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="5b92c-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="5b92c-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="5b92c-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="5b92c-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





