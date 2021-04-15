---
title: IDWriteTextLayout3 SetLineSpacing, método
description: Establezca el interlineado. | IDWriteTextLayout3 SetLineSpacing, método
ms.assetid: 1bfca257-189c-4d18-628c-aff8217d2775
keywords:
- Método SetLineSpacing de escritura directa
- Método SetLineSpacing de escritura directa, interfaz IDWriteTextLayout3
- Interfaz IDWriteTextLayout3 Direct Write, Método SetLineSpacing
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.SetLineSpacing
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 794df5b0dc993688c8bab15c927ae2c03bc18d69
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105670118"
---
# <a name="idwritetextlayout3setlinespacing-method"></a><span data-ttu-id="2b7c5-107">IDWriteTextLayout3:: SetLineSpacing (método)</span><span class="sxs-lookup"><span data-stu-id="2b7c5-107">IDWriteTextLayout3::SetLineSpacing method</span></span>

<span data-ttu-id="2b7c5-108">Establezca el interlineado.</span><span class="sxs-lookup"><span data-stu-id="2b7c5-108">Set line spacing.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b7c5-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2b7c5-109">Syntax</span></span>


```C++
HRESULT SetLineSpacing(
  [in] const DWRITE_LINE_SPACING *lineSpacingOptions
);
```



## <a name="parameters"></a><span data-ttu-id="2b7c5-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2b7c5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b7c5-111">*lineSpacingOptions* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2b7c5-111">*lineSpacingOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b7c5-112">Cómo administrar el espacio entre las líneas.</span><span class="sxs-lookup"><span data-stu-id="2b7c5-112">How to manage space between lines.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b7c5-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2b7c5-113">Return value</span></span>

<span data-ttu-id="2b7c5-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="2b7c5-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2b7c5-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2b7c5-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b7c5-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b7c5-116">Requirements</span></span>



| <span data-ttu-id="2b7c5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b7c5-117">Requirement</span></span> | <span data-ttu-id="2b7c5-118">Value</span><span class="sxs-lookup"><span data-stu-id="2b7c5-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b7c5-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b7c5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2b7c5-120">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="2b7c5-120">Windows 8.1 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="2b7c5-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b7c5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2b7c5-122">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="2b7c5-122">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2b7c5-123">Teléfono mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b7c5-123">Minimum supported phone</span></span><br/>  | <span data-ttu-id="2b7c5-124">Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]</span><span class="sxs-lookup"><span data-stu-id="2b7c5-124">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="2b7c5-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2b7c5-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="2b7c5-126"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2b7c5-126"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="2b7c5-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2b7c5-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b7c5-128"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b7c5-128"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2b7c5-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="2b7c5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b7c5-130">**IDWriteTextLayout3**</span><span class="sxs-lookup"><span data-stu-id="2b7c5-130">**IDWriteTextLayout3**</span></span>](idwritetextlayout3.md)
</dt> </dl>

 

 





