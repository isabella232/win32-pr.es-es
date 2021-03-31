---
title: Propiedad ConnectToServerConsole de IMsRdpClientAdvancedSettings
description: Esta propiedad no es compatible. Las llamadas a ConnectToServerConsole siempre devuelven S \_ false.
ms.assetid: 58f79085-4364-408f-8bf1-97a82ad68f4b
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad ConnectToServerConsole
- Propiedad ConnectToServerConsole Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad ConnectToServerConsole
- Propiedad ConnectToServerConsole Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad ConnectToServerConsole
- Propiedad ConnectToServerConsole Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad ConnectToServerConsole
- Propiedad ConnectToServerConsole Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad ConnectToServerConsole
- Propiedad ConnectToServerConsole Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad ConnectToServerConsole
- Propiedad ConnectToServerConsole Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad ConnectToServerConsole
- Propiedad ConnectToServerConsole Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad ConnectToServerConsole
- Propiedad ConnectToServerConsole Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad ConnectToServerConsole
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.ConnectToServerConsole
- IMsRdpClientAdvancedSettings.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings2.ConnectToServerConsole
- IMsRdpClientAdvancedSettings2.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings2.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings3.ConnectToServerConsole
- IMsRdpClientAdvancedSettings3.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings3.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings4.ConnectToServerConsole
- IMsRdpClientAdvancedSettings4.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings4.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings5.ConnectToServerConsole
- IMsRdpClientAdvancedSettings5.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings5.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings6.ConnectToServerConsole
- IMsRdpClientAdvancedSettings6.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings6.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings7.ConnectToServerConsole
- IMsRdpClientAdvancedSettings7.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings7.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings8.ConnectToServerConsole
- IMsRdpClientAdvancedSettings8.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings8.put_ConnectToServerConsole
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18e3385b25a9dbe3e77085ae011b85e9be21b224
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996314"
---
# <a name="imsrdpclientadvancedsettingsconnecttoserverconsole-property"></a><span data-ttu-id="78064-121">IMsRdpClientAdvancedSettings:: ConnectToServerConsole (propiedad)</span><span class="sxs-lookup"><span data-stu-id="78064-121">IMsRdpClientAdvancedSettings::ConnectToServerConsole property</span></span>

<span data-ttu-id="78064-122">Esta propiedad no es compatible.</span><span class="sxs-lookup"><span data-stu-id="78064-122">This property is not supported.</span></span> <span data-ttu-id="78064-123">Las llamadas a **ConnectToServerConsole** siempre devuelven **S \_ false**.</span><span class="sxs-lookup"><span data-stu-id="78064-123">Calls to **ConnectToServerConsole** always return **S\_FALSE**.</span></span>

<span data-ttu-id="78064-124">Use la propiedad [**ConnectToAdministerServer**](imsrdpclientadvancedsettings6-connecttoadministerserver.md) para conectarse a la sesión que se usa con fines administrativos.</span><span class="sxs-lookup"><span data-stu-id="78064-124">Use the [**ConnectToAdministerServer**](imsrdpclientadvancedsettings6-connecttoadministerserver.md) property to connect to the session that is used for administrative purposes.</span></span>

<span data-ttu-id="78064-125">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="78064-125">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="78064-126">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="78064-126">Syntax</span></span>


```C++
HRESULT put_ConnectToServerConsole(
  [in]  VARIANT_BOOL connectToServerConsole
);

HRESULT get_ConnectToServerConsole(
  [out] VARIANT_BOOL *pconnectToServerConsole
);
```



## <a name="property-value"></a><span data-ttu-id="78064-127">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="78064-127">Property value</span></span>

<span data-ttu-id="78064-128">Establezca este parámetro en **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="78064-128">Set this parameter to **VARIANT\_FALSE**.</span></span> <span data-ttu-id="78064-129">**Variante \_ TRUE** no se admite.</span><span class="sxs-lookup"><span data-stu-id="78064-129">**VARIANT\_TRUE** is not supported.</span></span>

## <a name="error-codes"></a><span data-ttu-id="78064-130">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="78064-130">Error codes</span></span>

<span data-ttu-id="78064-131">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="78064-131">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="78064-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="78064-132">Remarks</span></span>

<span data-ttu-id="78064-133">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="78064-133">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="78064-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78064-134">Requirements</span></span>



| <span data-ttu-id="78064-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="78064-135">Requirement</span></span> | <span data-ttu-id="78064-136">Value</span><span class="sxs-lookup"><span data-stu-id="78064-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78064-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="78064-137">Minimum supported client</span></span><br/> | <span data-ttu-id="78064-138">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="78064-138">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="78064-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="78064-139">Minimum supported server</span></span><br/> | <span data-ttu-id="78064-140">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="78064-140">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="78064-141">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="78064-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="78064-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78064-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="78064-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="78064-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78064-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78064-144"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="78064-145">IID</span><span class="sxs-lookup"><span data-stu-id="78064-145">IID</span></span><br/>                      | <span data-ttu-id="78064-146">IID \_ IMsRdpClientAdvancedSettings se define como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="78064-146">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="78064-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="78064-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78064-148">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="78064-148">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="78064-149">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="78064-149">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="78064-150">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="78064-150">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="78064-151">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="78064-151">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="78064-152">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="78064-152">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="78064-153">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="78064-153">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="78064-154">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="78064-154">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="78064-155">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="78064-155">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





