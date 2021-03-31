---
title: Propiedad RedirectClipboard de IMsRdpClientAdvancedSettings5
description: Establece o recupera la configuración para la redirección del portapapeles.
ms.assetid: c653f593-9912-4ade-a0a3-70d9afac2ab1
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad RedirectClipboard
- Propiedad RedirectClipboard Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad RedirectClipboard
- Propiedad RedirectClipboard Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad RedirectClipboard
- Propiedad RedirectClipboard Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad RedirectClipboard
- Propiedad RedirectClipboard Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad RedirectClipboard
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.RedirectClipboard
- IMsRdpClientAdvancedSettings5.get_RedirectClipboard
- IMsRdpClientAdvancedSettings5.put_RedirectClipboard
- IMsRdpClientAdvancedSettings6.RedirectClipboard
- IMsRdpClientAdvancedSettings6.get_RedirectClipboard
- IMsRdpClientAdvancedSettings6.put_RedirectClipboard
- IMsRdpClientAdvancedSettings7.RedirectClipboard
- IMsRdpClientAdvancedSettings7.get_RedirectClipboard
- IMsRdpClientAdvancedSettings7.put_RedirectClipboard
- IMsRdpClientAdvancedSettings8.RedirectClipboard
- IMsRdpClientAdvancedSettings8.get_RedirectClipboard
- IMsRdpClientAdvancedSettings8.put_RedirectClipboard
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2aba9950b8d602ca239d66364279a5876a432d04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996143"
---
# <a name="imsrdpclientadvancedsettings5redirectclipboard-property"></a><span data-ttu-id="fb44b-112">IMsRdpClientAdvancedSettings5:: RedirectClipboard (propiedad)</span><span class="sxs-lookup"><span data-stu-id="fb44b-112">IMsRdpClientAdvancedSettings5::RedirectClipboard property</span></span>

<span data-ttu-id="fb44b-113">Establece o recupera la configuración para la redirección del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="fb44b-113">Sets or retrieves the configuration for clipboard redirection.</span></span>

<span data-ttu-id="fb44b-114">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="fb44b-114">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb44b-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fb44b-115">Syntax</span></span>


```C++
HRESULT put_RedirectClipboard(
  [in]  VARIANT_BOOL fRedirectClipboard
);

HRESULT get_RedirectClipboard(
  [out] VARIANT_BOOL *pfRedirectClipboard
);
```



## <a name="property-value"></a><span data-ttu-id="fb44b-116">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="fb44b-116">Property value</span></span>

<span data-ttu-id="fb44b-117">Establece el modo de redirección del portapapeles en **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="fb44b-117">Sets the clipboard redirection mode to **TRUE** or **FALSE**.</span></span> <span data-ttu-id="fb44b-118">Si se establece en **true**, se habilita el modo de redirección del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="fb44b-118">If set to **TRUE**, clipboard redirection mode is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb44b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb44b-119">Requirements</span></span>



| <span data-ttu-id="fb44b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb44b-120">Requirement</span></span> | <span data-ttu-id="fb44b-121">Value</span><span class="sxs-lookup"><span data-stu-id="fb44b-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb44b-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb44b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="fb44b-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fb44b-123">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="fb44b-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb44b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="fb44b-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fb44b-125">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="fb44b-126">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="fb44b-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="fb44b-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb44b-127"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="fb44b-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fb44b-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb44b-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb44b-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="fb44b-130">IID</span><span class="sxs-lookup"><span data-stu-id="fb44b-130">IID</span></span><br/>                      | <span data-ttu-id="fb44b-131">IID \_ IMsRdpClientAdvancedSettings5 se define como FBA7F64E-6783-4405-DA45-FA4A763DABD0</span><span class="sxs-lookup"><span data-stu-id="fb44b-131">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fb44b-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="fb44b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb44b-133">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="fb44b-133">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="fb44b-134">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="fb44b-134">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="fb44b-135">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="fb44b-135">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="fb44b-136">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="fb44b-136">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





