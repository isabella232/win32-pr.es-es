---
title: IDWriteTextLayout2 GetMetrics, método
description: Recupera las métricas generales de la cadena con formato.
ms.assetid: EADCD83A-9FF5-44AB-8AB5-35FCB3A84889
keywords:
- Método GetMetrics de escritura directa
- Método GetMetrics de escritura directa, interfaz IDWriteTextLayout2
- Interfaz IDWriteTextLayout2 Direct Write, método GetMetrics
topic_type:
- apiref
api_name:
- IDWriteTextLayout2.GetMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e393dfabb632641125d915e85f275977b20f0326
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686046"
---
# <a name="idwritetextlayout2getmetrics-method"></a><span data-ttu-id="48eb7-106">IDWriteTextLayout2:: GetMetrics (método)</span><span class="sxs-lookup"><span data-stu-id="48eb7-106">IDWriteTextLayout2::GetMetrics method</span></span>

<span data-ttu-id="48eb7-107">Recupera las métricas generales de la cadena con formato.</span><span class="sxs-lookup"><span data-stu-id="48eb7-107">Retrieves overall metrics for the formatted string.</span></span>

## <a name="syntax"></a><span data-ttu-id="48eb7-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="48eb7-108">Syntax</span></span>


```C++
virtual HRESULT GetMetrics(
  [out] DWRITE_TEXT_METRICS1 * textMetrics
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="48eb7-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="48eb7-109">Parameters</span></span>

<dl> <dt>

 <span data-ttu-id="48eb7-110">*textMetrics* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="48eb7-110">*textMetrics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="48eb7-111">Escriba: \**[**DWRITE \_ Text \_ METRICS1**](/windows/win32/api/dwrite_2/ns-dwrite_2-dwrite_text_metrics1) \** _</span><span class="sxs-lookup"><span data-stu-id="48eb7-111">Type: \**[**DWRITE\_TEXT\_METRICS1**](/windows/win32/api/dwrite_2/ns-dwrite_2-dwrite_text_metrics1)\** _</span></span>

<span data-ttu-id="48eb7-112">Cuando este método realiza la devolución, contiene las distancias de texto y el contenido asociado medidos después de dar formato.</span><span class="sxs-lookup"><span data-stu-id="48eb7-112">When this method returns, contains the measured distances of text and associated content after being formatted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48eb7-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="48eb7-113">Return value</span></span>

<span data-ttu-id="48eb7-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="48eb7-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="48eb7-115">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="48eb7-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="48eb7-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="48eb7-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="48eb7-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48eb7-117">Requirements</span></span>



| <span data-ttu-id="48eb7-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="48eb7-118">Requirement</span></span> | <span data-ttu-id="48eb7-119">Value</span><span class="sxs-lookup"><span data-stu-id="48eb7-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="48eb7-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48eb7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="48eb7-121">Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="48eb7-121">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="48eb7-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48eb7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="48eb7-123">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="48eb7-123">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="48eb7-124">Teléfono mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48eb7-124">Minimum supported phone</span></span><br/>  | <span data-ttu-id="48eb7-125">Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]</span><span class="sxs-lookup"><span data-stu-id="48eb7-125">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="48eb7-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="48eb7-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="48eb7-127"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="48eb7-127"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="48eb7-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="48eb7-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48eb7-129"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48eb7-129"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="48eb7-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="48eb7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48eb7-131">**IDWriteTextLayout2**</span><span class="sxs-lookup"><span data-stu-id="48eb7-131">**IDWriteTextLayout2**</span></span>](idwritetextlayout2.md)
</dt> </dl>

 

 





