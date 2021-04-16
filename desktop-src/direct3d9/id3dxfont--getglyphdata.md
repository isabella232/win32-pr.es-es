---
description: Devuelve información sobre la posición y la orientación de un glifo en una celda de carácter.
ms.assetid: 80a78e68-6f88-4cd2-bb7b-0c608ae700aa
title: 'ID3DXFont:: GetGlyphData (método) (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetGlyphData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 31f8d2e9d61cd7a8d6bd96fbdd3f6f6a7d895568
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105689884"
---
# <a name="id3dxfontgetglyphdata-method"></a><span data-ttu-id="25160-103">ID3DXFont:: GetGlyphData (método)</span><span class="sxs-lookup"><span data-stu-id="25160-103">ID3DXFont::GetGlyphData method</span></span>

<span data-ttu-id="25160-104">Devuelve información sobre la posición y la orientación de un glifo en una celda de carácter.</span><span class="sxs-lookup"><span data-stu-id="25160-104">Returns information about the placement and orientation of a glyph in a character cell.</span></span>

## <a name="syntax"></a><span data-ttu-id="25160-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="25160-105">Syntax</span></span>


```C++
HRESULT GetGlyphData(
  [in]  UINT               Glyph,
  [out] LPDIRECT3DTEXTURE9 *ppTexture,
  [out] RECT               *pBlackBox,
  [out] POINT              *pCellInc
);
```



## <a name="parameters"></a><span data-ttu-id="25160-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="25160-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25160-107">*Glifo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="25160-107">*Glyph* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25160-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="25160-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="25160-109">Identificador del glifo.</span><span class="sxs-lookup"><span data-stu-id="25160-109">Glyph identifier.</span></span>

</dd> <dt>

<span data-ttu-id="25160-110">*ppTexture* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="25160-110">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="25160-111">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="25160-111">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="25160-112">Dirección de un puntero a un objeto [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que contiene el glifo.</span><span class="sxs-lookup"><span data-stu-id="25160-112">Address of a pointer to a [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) object that contains the glyph.</span></span>

</dd> <dt>

<span data-ttu-id="25160-113">*pBlackBox* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="25160-113">*pBlackBox* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="25160-114">Tipo: **[ **Rect**](/previous-versions//dd162897(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="25160-114">Type: **[**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="25160-115">Puntero al objeto de rectángulo más pequeño que incluye completamente el glifo.</span><span class="sxs-lookup"><span data-stu-id="25160-115">Pointer to the smallest rectangle object that completely encloses the glyph.</span></span>

</dd> <dt>

<span data-ttu-id="25160-116">*pCellInc* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="25160-116">*pCellInc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="25160-117">Tipo: **[ **Point**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="25160-117">Type: **[**POINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="25160-118">Puntero al vector bidimensional que conecta el origen de la celda de carácter actual con el origen de la celda de carácter siguiente.</span><span class="sxs-lookup"><span data-stu-id="25160-118">Pointer to the two-dimensional vector that connects the origin of the current character cell to the origin of the next character cell.</span></span> <span data-ttu-id="25160-119">Vea [**Point**](../winprog/windows-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="25160-119">See [**POINT**](../winprog/windows-data-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25160-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="25160-120">Return value</span></span>

<span data-ttu-id="25160-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="25160-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="25160-122">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="25160-122">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="25160-123">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="25160-123">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="25160-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25160-124">Requirements</span></span>



| <span data-ttu-id="25160-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="25160-125">Requirement</span></span> | <span data-ttu-id="25160-126">Value</span><span class="sxs-lookup"><span data-stu-id="25160-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="25160-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="25160-127">Header</span></span><br/>  | <dl> <span data-ttu-id="25160-128"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="25160-128"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="25160-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="25160-129">Library</span></span><br/> | <dl> <span data-ttu-id="25160-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="25160-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="25160-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="25160-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25160-132">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="25160-132">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
