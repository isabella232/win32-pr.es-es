---
title: Propiedad RedirectionWarningType de IMsRdpClientNonScriptable4
description: Controla la presencia y la apariencia del cuadro de diálogo que notifica al usuario sobre la redirección.
ms.assetid: 1aa79fc3-9620-466d-a93f-77a55ad76ede
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad RedirectionWarningType
- Propiedad RedirectionWarningType Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable4, propiedad RedirectionWarningType
- Propiedad RedirectionWarningType Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad RedirectionWarningType
- Servicios de Escritorio remoto de la propiedad RedirectionWarningType, objeto MsRdpClient6
- Servicios de Escritorio remoto de objeto MsRdpClient6, propiedad RedirectionWarningType
- Servicios de Escritorio remoto de la propiedad RedirectionWarningType, objeto MsRdpClient7
- Servicios de Escritorio remoto de objeto MsRdpClient7, propiedad RedirectionWarningType
- Servicios de Escritorio remoto de la propiedad RedirectionWarningType, objeto MsRdpClient8
- Servicios de Escritorio remoto de objeto MsRdpClient8, propiedad RedirectionWarningType
- Servicios de Escritorio remoto de la propiedad RedirectionWarningType, objeto MsRdpClient9
- Servicios de Escritorio remoto de objeto MsRdpClient9, propiedad RedirectionWarningType
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.RedirectionWarningType
- IMsRdpClientNonScriptable4.get_RedirectionWarningType
- IMsRdpClientNonScriptable4.put_RedirectionWarningType
- IMsRdpClientNonScriptable5.RedirectionWarningType
- IMsRdpClientNonScriptable5.get_RedirectionWarningType
- IMsRdpClientNonScriptable5.put_RedirectionWarningType
- MsRdpClient6.RedirectionWarningType
- MsRdpClient7.RedirectionWarningType
- MsRdpClient8.RedirectionWarningType
- MsRdpClient9.RedirectionWarningType
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 077c8f78c61cc9b7dd090db26f58ca7e28c14abb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686028"
---
# <a name="imsrdpclientnonscriptable4redirectionwarningtype-property"></a><span data-ttu-id="504ad-116">IMsRdpClientNonScriptable4:: RedirectionWarningType (propiedad)</span><span class="sxs-lookup"><span data-stu-id="504ad-116">IMsRdpClientNonScriptable4::RedirectionWarningType property</span></span>

<span data-ttu-id="504ad-117">Controla la presencia y la apariencia del cuadro de diálogo que notifica al usuario sobre la redirección.</span><span class="sxs-lookup"><span data-stu-id="504ad-117">Controls the presence and appearance of the dialog box that notifies the user about redirection.</span></span>

<span data-ttu-id="504ad-118">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="504ad-118">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="504ad-119">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="504ad-119">Syntax</span></span>


```C++
HRESULT put_RedirectionWarningType(
  [in]  RedirectionWarningType wrnType
);

HRESULT get_RedirectionWarningType(
  [out] RedirectionWarningType *pWrnType
);
```



## <a name="property-value"></a><span data-ttu-id="504ad-120">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="504ad-120">Property value</span></span>

<span data-ttu-id="504ad-121">Establece el tipo del cuadro de diálogo que notifica al usuario de la redirección.</span><span class="sxs-lookup"><span data-stu-id="504ad-121">Sets the type of the dialog box that notifies the user of redirection.</span></span>

<dt>

<span id="RedirectionWarningTypeDefault"></span><span id="redirectionwarningtypedefault"></span><span id="REDIRECTIONWARNINGTYPEDEFAULT"></span>

<span data-ttu-id="504ad-122"><span id="RedirectionWarningTypeDefault"></span><span id="redirectionwarningtypedefault"></span><span id="REDIRECTIONWARNINGTYPEDEFAULT"></span>**RedirectionWarningTypeDefault** (0x0000)</span><span class="sxs-lookup"><span data-stu-id="504ad-122"><span id="RedirectionWarningTypeDefault"></span><span id="redirectionwarningtypedefault"></span><span id="REDIRECTIONWARNINGTYPEDEFAULT"></span>**RedirectionWarningTypeDefault** (0x0000)</span></span>


</dt> <dd>

<span data-ttu-id="504ad-123">El cuadro de diálogo no es específico del editor.</span><span class="sxs-lookup"><span data-stu-id="504ad-123">The dialog box is not publisher specific.</span></span>

</dd> <dt>

<span id="RedirectionWarningTypeUnsigned"></span><span id="redirectionwarningtypeunsigned"></span><span id="REDIRECTIONWARNINGTYPEUNSIGNED"></span>

<span data-ttu-id="504ad-124"><span id="RedirectionWarningTypeUnsigned"></span><span id="redirectionwarningtypeunsigned"></span><span id="REDIRECTIONWARNINGTYPEUNSIGNED"></span>**RedirectionWarningTypeUnsigned** (0x0001)</span><span class="sxs-lookup"><span data-stu-id="504ad-124"><span id="RedirectionWarningTypeUnsigned"></span><span id="redirectionwarningtypeunsigned"></span><span id="REDIRECTIONWARNINGTYPEUNSIGNED"></span>**RedirectionWarningTypeUnsigned** (0x0001)</span></span>


</dt> <dd>

<span data-ttu-id="504ad-125">El cuadro de diálogo es para archivos sin firmar.</span><span class="sxs-lookup"><span data-stu-id="504ad-125">The dialog box is for unsigned files.</span></span>

</dd> <dt>

<span id="RedirectionWarningTypeUnknown"></span><span id="redirectionwarningtypeunknown"></span><span id="REDIRECTIONWARNINGTYPEUNKNOWN"></span>

<span data-ttu-id="504ad-126"><span id="RedirectionWarningTypeUnknown"></span><span id="redirectionwarningtypeunknown"></span><span id="REDIRECTIONWARNINGTYPEUNKNOWN"></span>**RedirectionWarningTypeUnknown** (0x0002)</span><span class="sxs-lookup"><span data-stu-id="504ad-126"><span id="RedirectionWarningTypeUnknown"></span><span id="redirectionwarningtypeunknown"></span><span id="REDIRECTIONWARNINGTYPEUNKNOWN"></span>**RedirectionWarningTypeUnknown** (0x0002)</span></span>


</dt> <dd>

<span data-ttu-id="504ad-127">El cuadro de diálogo es para un publicador desconocido.</span><span class="sxs-lookup"><span data-stu-id="504ad-127">The dialog box is for an unknown publisher.</span></span>

</dd> <dt>

<span id="RedirectionWarningTypeUser"></span><span id="redirectionwarningtypeuser"></span><span id="REDIRECTIONWARNINGTYPEUSER"></span>

<span data-ttu-id="504ad-128"><span id="RedirectionWarningTypeUser"></span><span id="redirectionwarningtypeuser"></span><span id="REDIRECTIONWARNINGTYPEUSER"></span>**RedirectionWarningTypeUser** (0x0003)</span><span class="sxs-lookup"><span data-stu-id="504ad-128"><span id="RedirectionWarningTypeUser"></span><span id="redirectionwarningtypeuser"></span><span id="REDIRECTIONWARNINGTYPEUSER"></span>**RedirectionWarningTypeUser** (0x0003)</span></span>


</dt> <dd>

<span data-ttu-id="504ad-129">El cuadro de diálogo es para los archivos del usuario.</span><span class="sxs-lookup"><span data-stu-id="504ad-129">The dialog box is for the user's files.</span></span>

</dd> <dt>

<span id="RedirectionWarningTypeThirdPartySigned"></span><span id="redirectionwarningtypethirdpartysigned"></span><span id="REDIRECTIONWARNINGTYPETHIRDPARTYSIGNED"></span>

<span data-ttu-id="504ad-130"><span id="RedirectionWarningTypeThirdPartySigned"></span><span id="redirectionwarningtypethirdpartysigned"></span><span id="REDIRECTIONWARNINGTYPETHIRDPARTYSIGNED"></span>**RedirectionWarningTypeThirdPartySigned** (0x0004)</span><span class="sxs-lookup"><span data-stu-id="504ad-130"><span id="RedirectionWarningTypeThirdPartySigned"></span><span id="redirectionwarningtypethirdpartysigned"></span><span id="REDIRECTIONWARNINGTYPETHIRDPARTYSIGNED"></span>**RedirectionWarningTypeThirdPartySigned** (0x0004)</span></span>


</dt> <dd>

<span data-ttu-id="504ad-131">El cuadro de diálogo se muestra para archivos firmados con certificado de terceros.</span><span class="sxs-lookup"><span data-stu-id="504ad-131">The dialog box is displayed for third-party-certified, signed files.</span></span>

</dd> <dt>

<span id="RedirectionWarningTypeTrusted"></span><span id="redirectionwarningtypetrusted"></span><span id="REDIRECTIONWARNINGTYPETRUSTED"></span>

<span data-ttu-id="504ad-132"><span id="RedirectionWarningTypeTrusted"></span><span id="redirectionwarningtypetrusted"></span><span id="REDIRECTIONWARNINGTYPETRUSTED"></span>**RedirectionWarningTypeTrusted** (0x0005)</span><span class="sxs-lookup"><span data-stu-id="504ad-132"><span id="RedirectionWarningTypeTrusted"></span><span id="redirectionwarningtypetrusted"></span><span id="REDIRECTIONWARNINGTYPETRUSTED"></span>**RedirectionWarningTypeTrusted** (0x0005)</span></span>


</dt> <dd>

<span data-ttu-id="504ad-133">No se muestra el cuadro de diálogo porque la aplicación está publicada por un editor de confianza.</span><span class="sxs-lookup"><span data-stu-id="504ad-133">The dialog box is not displayed because the application is published by a trusted publisher.</span></span>

</dd> <dt>

<span id="RedirectionWarningTypeMax"></span><span id="redirectionwarningtypemax"></span><span id="REDIRECTIONWARNINGTYPEMAX"></span>

<span data-ttu-id="504ad-134"><span id="RedirectionWarningTypeMax"></span><span id="redirectionwarningtypemax"></span><span id="REDIRECTIONWARNINGTYPEMAX"></span>**RedirectionWarningTypeMax** (0x0005)</span><span class="sxs-lookup"><span data-stu-id="504ad-134"><span id="RedirectionWarningTypeMax"></span><span id="redirectionwarningtypemax"></span><span id="REDIRECTIONWARNINGTYPEMAX"></span>**RedirectionWarningTypeMax** (0x0005)</span></span>


</dt> <dd>

<span data-ttu-id="504ad-135">No se muestra el cuadro de diálogo porque la aplicación está publicada por un editor de confianza.</span><span class="sxs-lookup"><span data-stu-id="504ad-135">The dialog box is not displayed because the application is published by a trusted publisher.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="504ad-136">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="504ad-136">Error codes</span></span>

<span data-ttu-id="504ad-137">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="504ad-137">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="504ad-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="504ad-138">Remarks</span></span>

<span data-ttu-id="504ad-139">El valor **RedirectionWarningTypeDefault**, que es el valor predeterminado de esta propiedad, no ejerce ningún control sobre el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="504ad-139">The value **RedirectionWarningTypeDefault**, which is the default value of this property, exerts no control over the dialog box.</span></span> <span data-ttu-id="504ad-140">En este caso, la propiedad de control es [**ShowRedirectionWarningDialog**](imsrdpclientnonscriptable3-showredirectionwarningdialog.md) en [**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md).</span><span class="sxs-lookup"><span data-stu-id="504ad-140">The controlling property in this case is [**ShowRedirectionWarningDialog**](imsrdpclientnonscriptable3-showredirectionwarningdialog.md) in [**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="504ad-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="504ad-141">Requirements</span></span>



| <span data-ttu-id="504ad-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="504ad-142">Requirement</span></span> | <span data-ttu-id="504ad-143">Value</span><span class="sxs-lookup"><span data-stu-id="504ad-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="504ad-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="504ad-144">Minimum supported client</span></span><br/> | <span data-ttu-id="504ad-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="504ad-145">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="504ad-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="504ad-146">Minimum supported server</span></span><br/> | <span data-ttu-id="504ad-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="504ad-147">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="504ad-148">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="504ad-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="504ad-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="504ad-149"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="504ad-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="504ad-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="504ad-151"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="504ad-151"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="504ad-152">IID</span><span class="sxs-lookup"><span data-stu-id="504ad-152">IID</span></span><br/>                      | <span data-ttu-id="504ad-153">IMsRdpClientNonScriptable4 se define como f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span><span class="sxs-lookup"><span data-stu-id="504ad-153">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="504ad-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="504ad-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="504ad-155">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="504ad-155">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="504ad-156">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="504ad-156">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





