---
title: Propiedad HotKeyFocusReleaseRight de IMsRdpClientAdvancedSettings6
description: Especifica el código de tecla virtual que se va a agregar a Ctrl + Alt para determinar el reemplazo de la tecla de cambio de teclas para Ctrl + Alt + flecha derecha.
ms.assetid: 9AEEB712-E4C4-435E-A847-40C2B3A41C15
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad HotKeyFocusReleaseRight
- Propiedad HotKeyFocusReleaseRight Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad HotKeyFocusReleaseRight
- Propiedad HotKeyFocusReleaseRight Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad HotKeyFocusReleaseRight
- Propiedad HotKeyFocusReleaseRight Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad HotKeyFocusReleaseRight
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings6.get_HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings6.put_HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings7.HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings7.get_HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings7.put_HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings8.HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings8.get_HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings8.put_HotKeyFocusReleaseRight
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2ce11df170b8b0a0a9a3f58a625955cecb41973
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686202"
---
# <a name="imsrdpclientadvancedsettings6hotkeyfocusreleaseright-property"></a><span data-ttu-id="b283b-110">IMsRdpClientAdvancedSettings6:: HotKeyFocusReleaseRight (propiedad)</span><span class="sxs-lookup"><span data-stu-id="b283b-110">IMsRdpClientAdvancedSettings6::HotKeyFocusReleaseRight property</span></span>

<span data-ttu-id="b283b-111">Especifica el código de tecla virtual que se va a agregar a Ctrl + Alt para determinar el reemplazo de la tecla de cambio de teclas para Ctrl + Alt + flecha derecha.</span><span class="sxs-lookup"><span data-stu-id="b283b-111">Specifies the virtual-key code to add to Ctrl+Alt to determine the hotkey replacement for Ctrl+Alt+Right Arrow.</span></span>

<span data-ttu-id="b283b-112">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="b283b-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b283b-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b283b-113">Syntax</span></span>


```C++
HRESULT put_HotKeyFocusReleaseRight(
  [in]  LONG hotKeyFocusReleaseRight
);

HRESULT get_HotKeyFocusReleaseRight(
  [out] LONG *hotKeyFocusReleaseRight
);
```



## <a name="property-value"></a><span data-ttu-id="b283b-114">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="b283b-114">Property value</span></span>

<span data-ttu-id="b283b-115">El nuevo código de tecla virtual.</span><span class="sxs-lookup"><span data-stu-id="b283b-115">The new virtual-key code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b283b-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b283b-116">Remarks</span></span>

<span data-ttu-id="b283b-117">Esta propiedad solo es compatible con clientes Conexión a Escritorio remoto 6,1 y 7,0.</span><span class="sxs-lookup"><span data-stu-id="b283b-117">This property is only supported by Remote Desktop Connection 6.1 and 7.0 clients.</span></span>

## <a name="requirements"></a><span data-ttu-id="b283b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b283b-118">Requirements</span></span>



| <span data-ttu-id="b283b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b283b-119">Requirement</span></span> | <span data-ttu-id="b283b-120">Value</span><span class="sxs-lookup"><span data-stu-id="b283b-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b283b-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b283b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b283b-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b283b-122">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="b283b-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b283b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b283b-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b283b-124">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="b283b-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b283b-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="b283b-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b283b-126"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="b283b-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b283b-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b283b-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b283b-128"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="b283b-129">IID</span><span class="sxs-lookup"><span data-stu-id="b283b-129">IID</span></span><br/>                      | <span data-ttu-id="b283b-130">IID \_ IMsRdpClientAdvancedSettings6 se define como 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="b283b-130">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b283b-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="b283b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b283b-132">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="b283b-132">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="b283b-133">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="b283b-133">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="b283b-134">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="b283b-134">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





