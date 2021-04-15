---
title: IDWriteColorGlyphRunEnumerator MoveNext (método)
description: Desplácese a la siguiente ejecución del glifo en el enumerador.
ms.assetid: E6336C0E-F880-485C-9111-A102298257C1
keywords:
- MoveNext (método) de escritura directa
- MoveNext Method Direct Write, IDWriteColorGlyphRunEnumerator (interfaz)
- Interfaz IDWriteColorGlyphRunEnumerator Direct Write, método MoveNext
topic_type:
- apiref
api_name:
- IDWriteColorGlyphRunEnumerator.MoveNext
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15c9963916c07f1df8cf3cfedb49b9e3fd66d0df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534498"
---
# <a name="idwritecolorglyphrunenumeratormovenext-method"></a><span data-ttu-id="fb1d5-106">IDWriteColorGlyphRunEnumerator:: MoveNext (método)</span><span class="sxs-lookup"><span data-stu-id="fb1d5-106">IDWriteColorGlyphRunEnumerator::MoveNext method</span></span>

<span data-ttu-id="fb1d5-107">Desplácese a la siguiente ejecución del glifo en el enumerador.</span><span class="sxs-lookup"><span data-stu-id="fb1d5-107">Move to the next glyph run in the enumerator.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb1d5-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fb1d5-108">Syntax</span></span>


```C++
HRESULT MoveNext(
  [out] BOOL *haveRun
);
```



## <a name="parameters"></a><span data-ttu-id="fb1d5-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fb1d5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb1d5-110">*haveRun* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="fb1d5-110">*haveRun* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb1d5-111">Tipo: \**bool \** _</span><span class="sxs-lookup"><span data-stu-id="fb1d5-111">Type: \**BOOL\** _</span></span>

<span data-ttu-id="fb1d5-112">Devuelve _ *true*\* si hay una ejecución del siguiente glifo.</span><span class="sxs-lookup"><span data-stu-id="fb1d5-112">Returns _ *TRUE*\* if there is a next glyph run.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb1d5-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fb1d5-113">Return value</span></span>

<span data-ttu-id="fb1d5-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="fb1d5-114">Type: **HRESULT**</span></span>

<span data-ttu-id="fb1d5-115">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="fb1d5-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fb1d5-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fb1d5-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb1d5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb1d5-117">Requirements</span></span>



| <span data-ttu-id="fb1d5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb1d5-118">Requirement</span></span> | <span data-ttu-id="fb1d5-119">Value</span><span class="sxs-lookup"><span data-stu-id="fb1d5-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb1d5-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb1d5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fb1d5-121">Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="fb1d5-121">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="fb1d5-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb1d5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fb1d5-123">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="fb1d5-123">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="fb1d5-124">Teléfono mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb1d5-124">Minimum supported phone</span></span><br/>  | <span data-ttu-id="fb1d5-125">Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]</span><span class="sxs-lookup"><span data-stu-id="fb1d5-125">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="fb1d5-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fb1d5-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="fb1d5-127"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fb1d5-127"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="fb1d5-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fb1d5-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb1d5-129"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb1d5-129"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fb1d5-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="fb1d5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb1d5-131">**IDWriteColorGlyphRunEnumerator**</span><span class="sxs-lookup"><span data-stu-id="fb1d5-131">**IDWriteColorGlyphRunEnumerator**</span></span>](idwritecolorglyphrunenumerator.md)
</dt> </dl>

 

 





