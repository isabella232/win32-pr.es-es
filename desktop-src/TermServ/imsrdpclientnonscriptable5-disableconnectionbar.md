---
title: Propiedad DisableConnectionBar de IMsRdpClientNonScriptable5
description: Especifica si el control ActiveX Escritorio remoto debe deshabilitar la barra de conexión.
ms.assetid: 82c57b93-f976-43e6-97f9-3602bf97e466
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad DisableConnectionBar
- Propiedad DisableConnectionBar Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad DisableConnectionBar
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.DisableConnectionBar
- IMsRdpClientNonScriptable5.put_DisableConnectionBar
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a129d4781db69a564eecbca3a715c3c5ccf1a9cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535577"
---
# <a name="imsrdpclientnonscriptable5disableconnectionbar-property"></a><span data-ttu-id="32b5e-106">IMsRdpClientNonScriptable5::D propiedad isableConnectionBar</span><span class="sxs-lookup"><span data-stu-id="32b5e-106">IMsRdpClientNonScriptable5::DisableConnectionBar property</span></span>

<span data-ttu-id="32b5e-107">Especifica si el control ActiveX Escritorio remoto debe deshabilitar la barra de conexión.</span><span class="sxs-lookup"><span data-stu-id="32b5e-107">Specifies whether the Remote Desktop ActiveX control should disable the connection bar.</span></span> <span data-ttu-id="32b5e-108">Si esta propiedad contiene **Variant \_ true**, la barra de conexión debe estar deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="32b5e-108">If this property contains **VARIANT\_TRUE**, the connection bar should be disabled.</span></span> <span data-ttu-id="32b5e-109">Si esta propiedad contiene **Variant \_ false**, la barra de conexión debe estar habilitada.</span><span class="sxs-lookup"><span data-stu-id="32b5e-109">If this property contains **VARIANT\_FALSE**, the connection bar should be enabled.</span></span>

<span data-ttu-id="32b5e-110">Esta propiedad es de solo escritura.</span><span class="sxs-lookup"><span data-stu-id="32b5e-110">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="32b5e-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="32b5e-111">Syntax</span></span>


```C++
HRESULT put_DisableConnectionBar(
  [in] VARIANT_BOOL fDisableConnectionBar
);
```



## <a name="property-value"></a><span data-ttu-id="32b5e-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="32b5e-112">Property value</span></span>

<span data-ttu-id="32b5e-113">Especifica el nuevo valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="32b5e-113">Specifies the new property value.</span></span>

## <a name="requirements"></a><span data-ttu-id="32b5e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32b5e-114">Requirements</span></span>



| <span data-ttu-id="32b5e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="32b5e-115">Requirement</span></span> | <span data-ttu-id="32b5e-116">Value</span><span class="sxs-lookup"><span data-stu-id="32b5e-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="32b5e-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32b5e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="32b5e-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="32b5e-118">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="32b5e-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32b5e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="32b5e-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="32b5e-120">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="32b5e-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="32b5e-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="32b5e-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32b5e-122"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="32b5e-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="32b5e-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32b5e-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32b5e-124"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="32b5e-125">IID</span><span class="sxs-lookup"><span data-stu-id="32b5e-125">IID</span></span><br/>                      | <span data-ttu-id="32b5e-126">IID \_ IMsRdpClientNonScriptable5 se define como 4f6996d5-d7b1-412C-b0ff-063718566907</span><span class="sxs-lookup"><span data-stu-id="32b5e-126">IID\_IMsRdpClientNonScriptable5 is defined as 4f6996d5-d7b1-412c-b0ff-063718566907</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="32b5e-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="32b5e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32b5e-128">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="32b5e-128">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





