---
title: Propiedad WarnAboutPrinterRedirection de IMsRdpClientNonScriptable4
description: Controla si el cuadro de diálogo de redirección muestra un mensaje sobre la redirección de la impresora antes de iniciar una sesión.
ms.assetid: 12c5bc8d-7bc1-4a94-a9b8-6b852772c936
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad WarnAboutPrinterRedirection
- Propiedad WarnAboutPrinterRedirection Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable4, propiedad WarnAboutPrinterRedirection
- Propiedad WarnAboutPrinterRedirection Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad WarnAboutPrinterRedirection
- Servicios de Escritorio remoto de la propiedad WarnAboutPrinterRedirection, objeto MsRdpClient6
- Servicios de Escritorio remoto de objeto MsRdpClient6, propiedad WarnAboutPrinterRedirection
- Servicios de Escritorio remoto de la propiedad WarnAboutPrinterRedirection, objeto MsRdpClient7
- Servicios de Escritorio remoto de objeto MsRdpClient7, propiedad WarnAboutPrinterRedirection
- Servicios de Escritorio remoto de la propiedad WarnAboutPrinterRedirection, objeto MsRdpClient8
- Servicios de Escritorio remoto de objeto MsRdpClient8, propiedad WarnAboutPrinterRedirection
- Servicios de Escritorio remoto de la propiedad WarnAboutPrinterRedirection, objeto MsRdpClient9
- Servicios de Escritorio remoto de objeto MsRdpClient9, propiedad WarnAboutPrinterRedirection
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable4.get_WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable4.put_WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable5.WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable5.get_WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable5.put_WarnAboutPrinterRedirection
- MsRdpClient6.WarnAboutPrinterRedirection
- MsRdpClient7.WarnAboutPrinterRedirection
- MsRdpClient8.WarnAboutPrinterRedirection
- MsRdpClient9.WarnAboutPrinterRedirection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24e2fa93995946e741caa76f1ee5b84be79d9c90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359759"
---
# <a name="imsrdpclientnonscriptable4warnaboutprinterredirection-property"></a><span data-ttu-id="ce0bc-116">IMsRdpClientNonScriptable4:: WarnAboutPrinterRedirection (propiedad)</span><span class="sxs-lookup"><span data-stu-id="ce0bc-116">IMsRdpClientNonScriptable4::WarnAboutPrinterRedirection property</span></span>

<span data-ttu-id="ce0bc-117">Controla si el cuadro de diálogo de redirección muestra un mensaje sobre la redirección de la impresora antes de iniciar una sesión.</span><span class="sxs-lookup"><span data-stu-id="ce0bc-117">Controls whether the redirection dialog box displays a message about printer redirection before starting a session.</span></span>

<span data-ttu-id="ce0bc-118">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="ce0bc-118">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce0bc-119">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ce0bc-119">Syntax</span></span>


```C++
HRESULT put_WarnAboutPrinterRedirection(
  [in]  VARIANT_BOOL fWarn
);

HRESULT get_WarnAboutPrinterRedirection(
  [out] VARIANT_BOOL *pfWarn
);
```



## <a name="property-value"></a><span data-ttu-id="ce0bc-120">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ce0bc-120">Property value</span></span>

<span data-ttu-id="ce0bc-121">Establece si el cuadro de diálogo de redirección muestra un mensaje sobre la redirección de la impresora.</span><span class="sxs-lookup"><span data-stu-id="ce0bc-121">Sets whether the redirection dialog box displays a message about printer redirection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ce0bc-122">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="ce0bc-122">Error codes</span></span>

<span data-ttu-id="ce0bc-123">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="ce0bc-123">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce0bc-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce0bc-124">Requirements</span></span>



| <span data-ttu-id="ce0bc-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce0bc-125">Requirement</span></span> | <span data-ttu-id="ce0bc-126">Value</span><span class="sxs-lookup"><span data-stu-id="ce0bc-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce0bc-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce0bc-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ce0bc-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ce0bc-128">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="ce0bc-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce0bc-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ce0bc-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ce0bc-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="ce0bc-131">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ce0bc-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="ce0bc-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce0bc-132"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="ce0bc-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ce0bc-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce0bc-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce0bc-134"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="ce0bc-135">IID</span><span class="sxs-lookup"><span data-stu-id="ce0bc-135">IID</span></span><br/>                      | <span data-ttu-id="ce0bc-136">IMsRdpClientNonScriptable4 se define como f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span><span class="sxs-lookup"><span data-stu-id="ce0bc-136">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ce0bc-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="ce0bc-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce0bc-138">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="ce0bc-138">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="ce0bc-139">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="ce0bc-139">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





