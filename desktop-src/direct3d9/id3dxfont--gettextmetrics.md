---
description: Recupera las características de fuente que se identifican en una estructura TEXTMETRIC. Este método admite la configuración del compilador ANSI y Unicode.
ms.assetid: 37788281-5bb0-45bb-b6d4-bdc4d811e3af
title: 'ID3DXFont:: GetTextMetrics (método) (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetTextMetrics
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6ce6064804d2aac2846cbea6971f145fc07759f3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362552"
---
# <a name="id3dxfontgettextmetrics-method"></a><span data-ttu-id="6fe8f-104">ID3DXFont:: GetTextMetrics (método)</span><span class="sxs-lookup"><span data-stu-id="6fe8f-104">ID3DXFont::GetTextMetrics method</span></span>

<span data-ttu-id="6fe8f-105">Recupera las características de fuente que se identifican en una estructura [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) .</span><span class="sxs-lookup"><span data-stu-id="6fe8f-105">Retrieves font characteristics that are identified in a [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) structure.</span></span> <span data-ttu-id="6fe8f-106">Este método admite la configuración del compilador ANSI y Unicode.</span><span class="sxs-lookup"><span data-stu-id="6fe8f-106">This method supports ANSI and Unicode compiler settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fe8f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6fe8f-107">Syntax</span></span>


```C++
BOOL GetTextMetrics(
  [out] TEXTMETRIC *pTextMetrics
);
```



## <a name="parameters"></a><span data-ttu-id="6fe8f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6fe8f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fe8f-109">*pTextMetrics* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6fe8f-109">*pTextMetrics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6fe8f-110">Tipo: **[ **TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica)\***</span><span class="sxs-lookup"><span data-stu-id="6fe8f-110">Type: **[**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica)\***</span></span>

<span data-ttu-id="6fe8f-111">Puntero a una estructura [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) , que contiene las propiedades de fuente.</span><span class="sxs-lookup"><span data-stu-id="6fe8f-111">Pointer to a [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) structure, which contains font properties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fe8f-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6fe8f-112">Return value</span></span>

<span data-ttu-id="6fe8f-113">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6fe8f-113">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6fe8f-114">Es distinto de cero si la función se realiza correctamente; de lo contrario, es 0.</span><span class="sxs-lookup"><span data-stu-id="6fe8f-114">Nonzero if the function is successful; otherwise 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="6fe8f-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6fe8f-115">Remarks</span></span>

<span data-ttu-id="6fe8f-116">La configuración del compilador también determina el tipo de estructura.</span><span class="sxs-lookup"><span data-stu-id="6fe8f-116">The compiler setting also determines the structure type.</span></span> <span data-ttu-id="6fe8f-117">Si se define Unicode, la función devuelve una estructura TEXTMETRICW.</span><span class="sxs-lookup"><span data-stu-id="6fe8f-117">If Unicode is defined, the function returns a TEXTMETRICW structure.</span></span> <span data-ttu-id="6fe8f-118">De lo contrario, la llamada de función devuelve una estructura TEXTMETRICA.</span><span class="sxs-lookup"><span data-stu-id="6fe8f-118">Otherwise, the function call returns a TEXTMETRICA structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fe8f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6fe8f-119">Requirements</span></span>



| <span data-ttu-id="6fe8f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fe8f-120">Requirement</span></span> | <span data-ttu-id="6fe8f-121">Value</span><span class="sxs-lookup"><span data-stu-id="6fe8f-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6fe8f-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6fe8f-122">Header</span></span><br/>  | <dl> <span data-ttu-id="6fe8f-123"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fe8f-123"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="6fe8f-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6fe8f-124">Library</span></span><br/> | <dl> <span data-ttu-id="6fe8f-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6fe8f-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6fe8f-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="6fe8f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fe8f-127">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="6fe8f-127">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
