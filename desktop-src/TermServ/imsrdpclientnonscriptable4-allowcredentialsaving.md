---
title: Propiedad AllowCredentialSaving de IMsRdpClientNonScriptable4
description: Especifica si el cuadro de diálogo credenciales muestra una casilla que permite guardar las credenciales.
ms.assetid: c5148ff0-0d7f-413d-b2a8-ff942668bee6
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad AllowCredentialSaving
- Propiedad AllowCredentialSaving Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable4, propiedad AllowCredentialSaving
- Propiedad AllowCredentialSaving Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad AllowCredentialSaving
- Servicios de Escritorio remoto de la propiedad AllowCredentialSaving, objeto MsRdpClient6
- Servicios de Escritorio remoto de objeto MsRdpClient6, propiedad AllowCredentialSaving
- Servicios de Escritorio remoto de la propiedad AllowCredentialSaving, objeto MsRdpClient7
- Servicios de Escritorio remoto de objeto MsRdpClient7, propiedad AllowCredentialSaving
- Servicios de Escritorio remoto de la propiedad AllowCredentialSaving, objeto MsRdpClient8
- Servicios de Escritorio remoto de objeto MsRdpClient8, propiedad AllowCredentialSaving
- Servicios de Escritorio remoto de la propiedad AllowCredentialSaving, objeto MsRdpClient9
- Servicios de Escritorio remoto de objeto MsRdpClient9, propiedad AllowCredentialSaving
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.AllowCredentialSaving
- IMsRdpClientNonScriptable4.get_AllowCredentialSaving
- IMsRdpClientNonScriptable4.put_AllowCredentialSaving
- IMsRdpClientNonScriptable5.AllowCredentialSaving
- IMsRdpClientNonScriptable5.get_AllowCredentialSaving
- IMsRdpClientNonScriptable5.put_AllowCredentialSaving
- MsRdpClient6.AllowCredentialSaving
- MsRdpClient7.AllowCredentialSaving
- MsRdpClient8.AllowCredentialSaving
- MsRdpClient9.AllowCredentialSaving
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 240e2eb8e80209ee5c90d63f2996231cf84bb2dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686030"
---
# <a name="imsrdpclientnonscriptable4allowcredentialsaving-property"></a><span data-ttu-id="0d1b7-116">IMsRdpClientNonScriptable4:: AllowCredentialSaving (propiedad)</span><span class="sxs-lookup"><span data-stu-id="0d1b7-116">IMsRdpClientNonScriptable4::AllowCredentialSaving property</span></span>

<span data-ttu-id="0d1b7-117">Especifica si el cuadro de diálogo credenciales muestra una casilla que permite guardar las credenciales.</span><span class="sxs-lookup"><span data-stu-id="0d1b7-117">Specifies whether the credentials dialog box displays a check box that enables the saving of credentials.</span></span>

<span data-ttu-id="0d1b7-118">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="0d1b7-118">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d1b7-119">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0d1b7-119">Syntax</span></span>


```C++
HRESULT put_AllowCredentialSaving(
  [in]  VARIANT_BOOL fAllowSave
);

HRESULT get_AllowCredentialSaving(
  [out] VARIANT_BOOL *pfAllowSave
);
```



## <a name="property-value"></a><span data-ttu-id="0d1b7-120">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="0d1b7-120">Property value</span></span>

<span data-ttu-id="0d1b7-121">Establece si el cuadro de diálogo credenciales muestra una casilla que permite guardar las credenciales.</span><span class="sxs-lookup"><span data-stu-id="0d1b7-121">Sets whether the credentials dialog box displays a check box that enables the saving of credentials.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0d1b7-122">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="0d1b7-122">Error codes</span></span>

<span data-ttu-id="0d1b7-123">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="0d1b7-123">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d1b7-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d1b7-124">Requirements</span></span>



| <span data-ttu-id="0d1b7-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d1b7-125">Requirement</span></span> | <span data-ttu-id="0d1b7-126">Value</span><span class="sxs-lookup"><span data-stu-id="0d1b7-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d1b7-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d1b7-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0d1b7-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0d1b7-128">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="0d1b7-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d1b7-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0d1b7-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0d1b7-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="0d1b7-131">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="0d1b7-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="0d1b7-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d1b7-132"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="0d1b7-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0d1b7-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d1b7-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d1b7-134"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="0d1b7-135">IID</span><span class="sxs-lookup"><span data-stu-id="0d1b7-135">IID</span></span><br/>                      | <span data-ttu-id="0d1b7-136">IMsRdpClientNonScriptable4 se define como f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span><span class="sxs-lookup"><span data-stu-id="0d1b7-136">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0d1b7-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="0d1b7-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d1b7-138">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="0d1b7-138">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="0d1b7-139">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="0d1b7-139">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





