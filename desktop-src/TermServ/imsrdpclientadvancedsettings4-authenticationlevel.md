---
title: Propiedad AuthenticationLevel de IMsRdpClientAdvancedSettings4
description: Especifica el nivel de autenticación que se va a utilizar para la conexión.
ms.assetid: 09ff1508-f13d-4bb0-8458-6f5a5e099bae
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad AuthenticationLevel
- Propiedad AuthenticationLevel Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad AuthenticationLevel
- Propiedad AuthenticationLevel Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad AuthenticationLevel
- Propiedad AuthenticationLevel Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad AuthenticationLevel
- Propiedad AuthenticationLevel Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad AuthenticationLevel
- Propiedad AuthenticationLevel Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad AuthenticationLevel
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings4.AuthenticationLevel
- IMsRdpClientAdvancedSettings4.get_AuthenticationLevel
- IMsRdpClientAdvancedSettings4.put_AuthenticationLevel
- IMsRdpClientAdvancedSettings5.AuthenticationLevel
- IMsRdpClientAdvancedSettings5.get_AuthenticationLevel
- IMsRdpClientAdvancedSettings5.put_AuthenticationLevel
- IMsRdpClientAdvancedSettings6.AuthenticationLevel
- IMsRdpClientAdvancedSettings6.get_AuthenticationLevel
- IMsRdpClientAdvancedSettings6.put_AuthenticationLevel
- IMsRdpClientAdvancedSettings7.AuthenticationLevel
- IMsRdpClientAdvancedSettings7.get_AuthenticationLevel
- IMsRdpClientAdvancedSettings7.put_AuthenticationLevel
- IMsRdpClientAdvancedSettings8.AuthenticationLevel
- IMsRdpClientAdvancedSettings8.get_AuthenticationLevel
- IMsRdpClientAdvancedSettings8.put_AuthenticationLevel
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c748416650ec7e6ec3d26fe6236a254eb012d67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905192"
---
# <a name="imsrdpclientadvancedsettings4authenticationlevel-property"></a><span data-ttu-id="31f13-114">IMsRdpClientAdvancedSettings4:: AuthenticationLevel (propiedad)</span><span class="sxs-lookup"><span data-stu-id="31f13-114">IMsRdpClientAdvancedSettings4::AuthenticationLevel property</span></span>

<span data-ttu-id="31f13-115">Especifica el nivel de autenticación que se va a utilizar para la conexión.</span><span class="sxs-lookup"><span data-stu-id="31f13-115">Specifies the authentication level to use for the connection.</span></span>

<span data-ttu-id="31f13-116">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="31f13-116">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="31f13-117">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="31f13-117">Syntax</span></span>


```C++
HRESULT put_AuthenticationLevel(
  [in]  UINT uiAuthLevel
);

HRESULT get_AuthenticationLevel(
  [out] UINT *puiAuthLevel
);
```



## <a name="property-value"></a><span data-ttu-id="31f13-118">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="31f13-118">Property value</span></span>

<span data-ttu-id="31f13-119">Valor de la propiedad **AuthenticationLevel** .</span><span class="sxs-lookup"><span data-stu-id="31f13-119">The value of the **AuthenticationLevel** property.</span></span>

<dt>

<span data-ttu-id="31f13-120">0</span><span class="sxs-lookup"><span data-stu-id="31f13-120">0</span></span>
</dt> <dd>

<span data-ttu-id="31f13-121">No hay autenticación del servidor.</span><span class="sxs-lookup"><span data-stu-id="31f13-121">No authentication of the server.</span></span>

</dd> <dt>

<span data-ttu-id="31f13-122">1</span><span class="sxs-lookup"><span data-stu-id="31f13-122">1</span></span>
</dt> <dd>

<span data-ttu-id="31f13-123">La autenticación del servidor es necesaria y debe completarse correctamente para que la conexión continúe.</span><span class="sxs-lookup"><span data-stu-id="31f13-123">Server authentication is required and must complete successfully for the connection to proceed.</span></span>

</dd> <dt>

<span data-ttu-id="31f13-124">2</span><span class="sxs-lookup"><span data-stu-id="31f13-124">2</span></span>
</dt> <dd>

<span data-ttu-id="31f13-125">Intente la autenticación del servidor.</span><span class="sxs-lookup"><span data-stu-id="31f13-125">Attempt authentication of the server.</span></span> <span data-ttu-id="31f13-126">Si se produce un error en la autenticación, se le solicitará al usuario la posibilidad de cancelar la conexión o continuar sin la autenticación del servidor.</span><span class="sxs-lookup"><span data-stu-id="31f13-126">If authentication fails, the user will be prompted with the option to cancel the connection or to proceed without server authentication.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="31f13-127">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="31f13-127">Error codes</span></span>

<span data-ttu-id="31f13-128">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="31f13-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="31f13-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="31f13-129">Remarks</span></span>

<span data-ttu-id="31f13-130">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="31f13-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="31f13-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31f13-131">Requirements</span></span>



| <span data-ttu-id="31f13-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="31f13-132">Requirement</span></span> | <span data-ttu-id="31f13-133">Value</span><span class="sxs-lookup"><span data-stu-id="31f13-133">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31f13-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31f13-134">Minimum supported client</span></span><br/> | <span data-ttu-id="31f13-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="31f13-135">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="31f13-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31f13-136">Minimum supported server</span></span><br/> | <span data-ttu-id="31f13-137">Windows Server 2008, Windows Server 2008 con SP1</span><span class="sxs-lookup"><span data-stu-id="31f13-137">Windows Server 2008, Windows Server 2008 with SP1</span></span><br/>                                     |
| <span data-ttu-id="31f13-138">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="31f13-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="31f13-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31f13-139"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="31f13-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="31f13-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31f13-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31f13-141"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="31f13-142">IID</span><span class="sxs-lookup"><span data-stu-id="31f13-142">IID</span></span><br/>                      | <span data-ttu-id="31f13-143">IID \_ IMsRdpClientAdvancedSettings4 se define como FBA7F64E-7345-4405-AE50-FA4A763DC0DE</span><span class="sxs-lookup"><span data-stu-id="31f13-143">IID\_IMsRdpClientAdvancedSettings4 is defined as FBA7F64E-7345-4405-AE50-FA4A763DC0DE</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="31f13-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="31f13-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31f13-145">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="31f13-145">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="31f13-146">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="31f13-146">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="31f13-147">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="31f13-147">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="31f13-148">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="31f13-148">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="31f13-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="31f13-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> </dl>

 

 





