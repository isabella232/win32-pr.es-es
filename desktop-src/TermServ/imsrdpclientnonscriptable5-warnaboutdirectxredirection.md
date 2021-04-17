---
title: Propiedad WarnAboutDirectXRedirection de IMsRdpClientNonScriptable5
description: No se usa esta propiedad. | Propiedad WarnAboutDirectXRedirection de IMsRdpClientNonScriptable5
ms.assetid: 005CA515-05B1-4B31-A83F-80E113F1BA7B
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad WarnAboutDirectXRedirection
- Propiedad WarnAboutDirectXRedirection Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad WarnAboutDirectXRedirection
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.WarnAboutDirectXRedirection
- IMsRdpClientNonScriptable5.get_WarnAboutDirectXRedirection
- IMsRdpClientNonScriptable5.put_WarnAboutDirectXRedirection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39bb49a79e319d848b12e4bbf50e191b21605f3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689714"
---
# <a name="imsrdpclientnonscriptable5warnaboutdirectxredirection-property"></a><span data-ttu-id="e0e35-107">IMsRdpClientNonScriptable5:: WarnAboutDirectXRedirection (propiedad)</span><span class="sxs-lookup"><span data-stu-id="e0e35-107">IMsRdpClientNonScriptable5::WarnAboutDirectXRedirection property</span></span>

<span data-ttu-id="e0e35-108">No se usa esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="e0e35-108">This property is not used.</span></span>

<span data-ttu-id="e0e35-109">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="e0e35-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0e35-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e0e35-110">Syntax</span></span>


```C++
HRESULT put_WarnAboutDirectXRedirection(
  [in]          VARIANT_BOOL fWarn
);

HRESULT get_WarnAboutDirectXRedirection(
  [out, retval] VARIANT_BOOL *pfWarn
);
```



## <a name="property-value"></a><span data-ttu-id="e0e35-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e0e35-111">Property value</span></span>

<span data-ttu-id="e0e35-112">Especifica el nuevo valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="e0e35-112">Specifies the new property value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0e35-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0e35-113">Requirements</span></span>



| <span data-ttu-id="e0e35-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0e35-114">Requirement</span></span> | <span data-ttu-id="e0e35-115">Value</span><span class="sxs-lookup"><span data-stu-id="e0e35-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0e35-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0e35-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e0e35-117">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e0e35-117">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e0e35-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0e35-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e0e35-119">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e0e35-119">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="e0e35-120">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e0e35-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="e0e35-121"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0e35-121"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="e0e35-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e0e35-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0e35-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0e35-123"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="e0e35-124">IID</span><span class="sxs-lookup"><span data-stu-id="e0e35-124">IID</span></span><br/>                      | <span data-ttu-id="e0e35-125">IID \_ IMsRdpClientNonScriptable5 se define como 4f6996d5-d7b1-412C-b0ff-063718566907</span><span class="sxs-lookup"><span data-stu-id="e0e35-125">IID\_IMsRdpClientNonScriptable5 is defined as 4f6996d5-d7b1-412c-b0ff-063718566907</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e0e35-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="e0e35-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0e35-127">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="e0e35-127">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





