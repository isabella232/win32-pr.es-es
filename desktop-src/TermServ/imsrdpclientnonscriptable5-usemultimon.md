---
title: Propiedad UseMultimon de IMsRdpClientNonScriptable5
description: Especifica si el control ActiveX Escritorio remoto debe usar varios monitores.
ms.assetid: 7832E025-80F6-4B4B-9829-C2D2EF2D8C37
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad UseMultimon
- Propiedad UseMultimon Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad UseMultimon
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.UseMultimon
- IMsRdpClientNonScriptable5.get_UseMultimon
- IMsRdpClientNonScriptable5.put_UseMultimon
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 941a2991ef5591176cd2508bbb6a097fecabebf0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996680"
---
# <a name="imsrdpclientnonscriptable5usemultimon-property"></a><span data-ttu-id="099a4-106">IMsRdpClientNonScriptable5:: UseMultimon (propiedad)</span><span class="sxs-lookup"><span data-stu-id="099a4-106">IMsRdpClientNonScriptable5::UseMultimon property</span></span>

<span data-ttu-id="099a4-107">Especifica si el control ActiveX Escritorio remoto debe usar varios monitores.</span><span class="sxs-lookup"><span data-stu-id="099a4-107">Specifies whether the Remote Desktop ActiveX control should use multiple monitors.</span></span> <span data-ttu-id="099a4-108">Si esta propiedad contiene **Variant \_ true**, el control utilizará varios monitores.</span><span class="sxs-lookup"><span data-stu-id="099a4-108">If this property contains **VARIANT\_TRUE**, the control will use multiple monitors.</span></span> <span data-ttu-id="099a4-109">Si esta propiedad contiene **Variant \_ false**, el control no usará varios monitores.</span><span class="sxs-lookup"><span data-stu-id="099a4-109">If this property contains **VARIANT\_FALSE**, the control will not use multiple monitors.</span></span>

<span data-ttu-id="099a4-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="099a4-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="099a4-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="099a4-111">Syntax</span></span>


```C++
HRESULT put_UseMultimon(
  [in]          VARIANT_BOOL fUseMultimon
);

HRESULT get_UseMultimon(
  [out, retval] VARIANT_BOOL *pfUseMultimon
);
```



## <a name="property-value"></a><span data-ttu-id="099a4-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="099a4-112">Property value</span></span>

<span data-ttu-id="099a4-113">Especifica el nuevo valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="099a4-113">Specifies the new property value.</span></span>

## <a name="requirements"></a><span data-ttu-id="099a4-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="099a4-114">Requirements</span></span>



| <span data-ttu-id="099a4-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="099a4-115">Requirement</span></span> | <span data-ttu-id="099a4-116">Value</span><span class="sxs-lookup"><span data-stu-id="099a4-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="099a4-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="099a4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="099a4-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="099a4-118">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="099a4-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="099a4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="099a4-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="099a4-120">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="099a4-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="099a4-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="099a4-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="099a4-122"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="099a4-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="099a4-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="099a4-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="099a4-124"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="099a4-125">IID</span><span class="sxs-lookup"><span data-stu-id="099a4-125">IID</span></span><br/>                      | <span data-ttu-id="099a4-126">IID \_ IMsRdpClientNonScriptable5 se define como 4f6996d5-d7b1-412C-b0ff-063718566907</span><span class="sxs-lookup"><span data-stu-id="099a4-126">IID\_IMsRdpClientNonScriptable5 is defined as 4f6996d5-d7b1-412c-b0ff-063718566907</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="099a4-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="099a4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="099a4-128">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="099a4-128">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





