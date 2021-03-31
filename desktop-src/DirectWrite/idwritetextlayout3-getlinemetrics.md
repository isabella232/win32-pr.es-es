---
title: IDWriteTextLayout3 GetLineMetrics, método
description: Recupera las propiedades de cada línea.
ms.assetid: 352ca3e3-7b08-823c-0881-0b051d4ce574
keywords:
- Método GetLineMetrics de escritura directa
- Método GetLineMetrics de escritura directa, interfaz IDWriteTextLayout3
- Interfaz IDWriteTextLayout3 Direct Write, método GetLineMetrics
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.GetLineMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d10a06cbf123b71e1308b45c747ac8a840a5fe1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491410"
---
# <a name="idwritetextlayout3getlinemetrics-method"></a><span data-ttu-id="e80c8-106">IDWriteTextLayout3:: GetLineMetrics (método)</span><span class="sxs-lookup"><span data-stu-id="e80c8-106">IDWriteTextLayout3::GetLineMetrics method</span></span>

<span data-ttu-id="e80c8-107">Recupera las propiedades de cada línea.</span><span class="sxs-lookup"><span data-stu-id="e80c8-107">Retrieves properties of each line.</span></span>

## <a name="syntax"></a><span data-ttu-id="e80c8-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e80c8-108">Syntax</span></span>


```C++
HRESULT GetLineMetrics(
  [out] DWRITE_LINE_METRICS1 *lineMetrics,
        UINT32               maxLineCount,
  [out] UINT32               *actualLineCount
);
```



## <a name="parameters"></a><span data-ttu-id="e80c8-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e80c8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e80c8-110">*lineMetrics* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e80c8-110">*lineMetrics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e80c8-111">Matriz que se va a rellenar con información de línea.</span><span class="sxs-lookup"><span data-stu-id="e80c8-111">The array to fill with line information.</span></span>

</dd> <dt>

<span data-ttu-id="e80c8-112">*maxLineCount*</span><span class="sxs-lookup"><span data-stu-id="e80c8-112">*maxLineCount*</span></span> 
</dt> <dd>

<span data-ttu-id="e80c8-113">Tamaño máximo de la matriz lineMetrics.</span><span class="sxs-lookup"><span data-stu-id="e80c8-113">The maximum size of the lineMetrics array.</span></span>

</dd> <dt>

<span data-ttu-id="e80c8-114">*actualLineCount* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e80c8-114">*actualLineCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e80c8-115">Tamaño real de la matriz de lineMetrics que se necesita.</span><span class="sxs-lookup"><span data-stu-id="e80c8-115">The actual size of the lineMetrics array that is needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e80c8-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e80c8-116">Return value</span></span>

<span data-ttu-id="e80c8-117">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="e80c8-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e80c8-118">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e80c8-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e80c8-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e80c8-119">Remarks</span></span>

<span data-ttu-id="e80c8-120">Si maxLineCount no es suficientemente grande \_ y no hay suficiente \_ \_ búfer, que es equivalente a HRESULT \_ de \_ Win32 (error de \_ búfer insuficiente \_ ), se devuelve y actualLineCount se establece en el número de líneas necesarias.</span><span class="sxs-lookup"><span data-stu-id="e80c8-120">If maxLineCount is not large enough E\_NOT\_SUFFICIENT\_BUFFER, which is equivalent to HRESULT\_FROM\_WIN32(ERROR\_INSUFFICIENT\_BUFFER), is returned and actualLineCount is set to the number of lines needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="e80c8-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e80c8-121">Requirements</span></span>



| <span data-ttu-id="e80c8-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e80c8-122">Requirement</span></span> | <span data-ttu-id="e80c8-123">Value</span><span class="sxs-lookup"><span data-stu-id="e80c8-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e80c8-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e80c8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e80c8-125">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="e80c8-125">Windows 8.1 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="e80c8-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e80c8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e80c8-127">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e80c8-127">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e80c8-128">Teléfono mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e80c8-128">Minimum supported phone</span></span><br/>  | <span data-ttu-id="e80c8-129">Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]</span><span class="sxs-lookup"><span data-stu-id="e80c8-129">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="e80c8-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e80c8-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="e80c8-131"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e80c8-131"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="e80c8-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e80c8-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e80c8-133"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e80c8-133"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e80c8-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="e80c8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e80c8-135">**IDWriteTextLayout3**</span><span class="sxs-lookup"><span data-stu-id="e80c8-135">**IDWriteTextLayout3**</span></span>](idwritetextlayout3.md)
</dt> </dl>

 

 





