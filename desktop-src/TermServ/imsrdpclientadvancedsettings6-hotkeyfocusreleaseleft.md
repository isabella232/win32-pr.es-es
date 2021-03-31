---
title: Propiedad HotKeyFocusReleaseLeft de IMsRdpClientAdvancedSettings6
description: Especifica el código de tecla virtual que se va a agregar a Ctrl + Alt para determinar el reemplazo de la tecla de cambio de teclas para Ctrl + Alt + flecha izquierda.
ms.assetid: 9F2942BD-9F5C-4E02-A330-42C30C6C8F87
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad HotKeyFocusReleaseLeft
- Propiedad HotKeyFocusReleaseLeft Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad HotKeyFocusReleaseLeft
- Propiedad HotKeyFocusReleaseLeft Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad HotKeyFocusReleaseLeft
- Propiedad HotKeyFocusReleaseLeft Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad HotKeyFocusReleaseLeft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings6.get_HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings6.put_HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings7.HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings7.get_HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings7.put_HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings8.HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings8.get_HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings8.put_HotKeyFocusReleaseLeft
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27e0e6d4e334edeffbf0ef025e59454e0f26c34c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801154"
---
# <a name="imsrdpclientadvancedsettings6hotkeyfocusreleaseleft-property"></a><span data-ttu-id="e293d-110">IMsRdpClientAdvancedSettings6:: HotKeyFocusReleaseLeft (propiedad)</span><span class="sxs-lookup"><span data-stu-id="e293d-110">IMsRdpClientAdvancedSettings6::HotKeyFocusReleaseLeft property</span></span>

<span data-ttu-id="e293d-111">Especifica el código de tecla virtual que se va a agregar a Ctrl + Alt para determinar el reemplazo de la tecla de cambio de teclas para Ctrl + Alt + flecha izquierda.</span><span class="sxs-lookup"><span data-stu-id="e293d-111">Specifies the virtual-key code to add to Ctrl+Alt to determine the hotkey replacement for Ctrl+Alt+Left Arrow.</span></span>

<span data-ttu-id="e293d-112">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="e293d-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e293d-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e293d-113">Syntax</span></span>


```C++
HRESULT put_HotKeyFocusReleaseLeft(
  [in]  LONG hotKeyFocusReleaseLeft
);

HRESULT get_HotKeyFocusReleaseLeft(
  [out] LONG *hotKeyFocusReleaseLeft
);
```



## <a name="property-value"></a><span data-ttu-id="e293d-114">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e293d-114">Property value</span></span>

<span data-ttu-id="e293d-115">El nuevo código de tecla virtual.</span><span class="sxs-lookup"><span data-stu-id="e293d-115">The new virtual-key code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e293d-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e293d-116">Remarks</span></span>

<span data-ttu-id="e293d-117">Esta propiedad solo es compatible con clientes Conexión a Escritorio remoto 6,1 y 7,0.</span><span class="sxs-lookup"><span data-stu-id="e293d-117">This property is only supported by Remote Desktop Connection 6.1 and 7.0 clients.</span></span>

## <a name="requirements"></a><span data-ttu-id="e293d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e293d-118">Requirements</span></span>



| <span data-ttu-id="e293d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e293d-119">Requirement</span></span> | <span data-ttu-id="e293d-120">Value</span><span class="sxs-lookup"><span data-stu-id="e293d-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e293d-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e293d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e293d-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e293d-122">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="e293d-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e293d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e293d-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e293d-124">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="e293d-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e293d-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="e293d-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e293d-126"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="e293d-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e293d-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e293d-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e293d-128"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="e293d-129">IID</span><span class="sxs-lookup"><span data-stu-id="e293d-129">IID</span></span><br/>                      | <span data-ttu-id="e293d-130">IID \_ IMsRdpClientAdvancedSettings6 se define como 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="e293d-130">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e293d-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="e293d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e293d-132">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="e293d-132">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="e293d-133">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="e293d-133">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="e293d-134">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="e293d-134">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





