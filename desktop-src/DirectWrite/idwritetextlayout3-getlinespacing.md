---
title: IDWriteTextLayout3 GetLineSpacing, método
description: Obtiene la información de espaciado de línea.
ms.assetid: 6b93a3ec-c8ea-2e64-45b5-51565d6de173
keywords:
- Método GetLineSpacing de escritura directa
- Método GetLineSpacing de escritura directa, interfaz IDWriteTextLayout3
- Interfaz IDWriteTextLayout3 Direct Write, método GetLineSpacing
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.GetLineSpacing
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303030a5674f39c160804ae2dad5b91050d82f37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996626"
---
# <a name="idwritetextlayout3getlinespacing-method"></a><span data-ttu-id="0add5-106">IDWriteTextLayout3:: GetLineSpacing (método)</span><span class="sxs-lookup"><span data-stu-id="0add5-106">IDWriteTextLayout3::GetLineSpacing method</span></span>

<span data-ttu-id="0add5-107">Obtiene la información de espaciado de línea.</span><span class="sxs-lookup"><span data-stu-id="0add5-107">Gets line spacing information.</span></span>

## <a name="syntax"></a><span data-ttu-id="0add5-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0add5-108">Syntax</span></span>


```C++
HRESULT GetLineSpacing(
  [out] DWRITE_LINE_SPACING *lineSpacingOptions
);
```



## <a name="parameters"></a><span data-ttu-id="0add5-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0add5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0add5-110">*lineSpacingOptions* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0add5-110">*lineSpacingOptions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0add5-111">Cómo administrar el espacio entre las líneas.</span><span class="sxs-lookup"><span data-stu-id="0add5-111">How to manage space between lines.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0add5-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0add5-112">Return value</span></span>

<span data-ttu-id="0add5-113">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="0add5-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0add5-114">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0add5-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0add5-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0add5-115">Requirements</span></span>



| <span data-ttu-id="0add5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0add5-116">Requirement</span></span> | <span data-ttu-id="0add5-117">Value</span><span class="sxs-lookup"><span data-stu-id="0add5-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0add5-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0add5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0add5-119">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="0add5-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="0add5-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0add5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0add5-121">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="0add5-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0add5-122">Teléfono mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0add5-122">Minimum supported phone</span></span><br/>  | <span data-ttu-id="0add5-123">Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]</span><span class="sxs-lookup"><span data-stu-id="0add5-123">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="0add5-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0add5-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="0add5-125"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0add5-125"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="0add5-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0add5-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0add5-127"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0add5-127"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0add5-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="0add5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0add5-129">**IDWriteTextLayout3**</span><span class="sxs-lookup"><span data-stu-id="0add5-129">**IDWriteTextLayout3**</span></span>](idwritetextlayout3.md)
</dt> </dl>

 

 





