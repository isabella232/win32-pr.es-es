---
description: Devuelve información sobre la posición y la orientación de un glifo en una celda de carácter.
ms.assetid: 1114b06a-c0f0-4c2a-86ad-2ed72bee4049
title: 'ID3DX10Font:: GetGlyphData (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetGlyphData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 530206c4f351cb1ef073639a21dfa37e43af5bae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707995"
---
# <a name="id3dx10fontgetglyphdata-method"></a><span data-ttu-id="ccf89-103">ID3DX10Font:: GetGlyphData (método)</span><span class="sxs-lookup"><span data-stu-id="ccf89-103">ID3DX10Font::GetGlyphData method</span></span>

<span data-ttu-id="ccf89-104">Devuelve información sobre la posición y la orientación de un glifo en una celda de carácter.</span><span class="sxs-lookup"><span data-stu-id="ccf89-104">Return information about the placement and orientation of a glyph in a character cell.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccf89-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ccf89-105">Syntax</span></span>


```C++
HRESULT GetGlyphData(
  [in]  UINT                     Glyph,
  [out] ID3D10ShaderResourceView **ppTexture,
  [in]  RECT                     *pBlackBox,
  [in]  POINT                    *pCellInc
);
```



## <a name="parameters"></a><span data-ttu-id="ccf89-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ccf89-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccf89-107">*Glifo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ccf89-107">*Glyph* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccf89-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ccf89-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ccf89-109">Identificador del glifo.</span><span class="sxs-lookup"><span data-stu-id="ccf89-109">Glyph identifier.</span></span>

</dd> <dt>

<span data-ttu-id="ccf89-110">*ppTexture* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ccf89-110">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ccf89-111">Tipo: **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="ccf89-111">Type: **[**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span></span>

<span data-ttu-id="ccf89-112">Dirección de un puntero a un objeto ID3D10Texture que contiene el glifo.</span><span class="sxs-lookup"><span data-stu-id="ccf89-112">Address of a pointer to a ID3D10Texture object that contains the glyph.</span></span>

</dd> <dt>

<span data-ttu-id="ccf89-113">*pBlackBox* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ccf89-113">*pBlackBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccf89-114">Tipo: **[ **Rect**](/previous-versions//dd162897(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="ccf89-114">Type: **[**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="ccf89-115">Puntero al objeto de rectángulo más pequeño que incluye completamente el glifo.</span><span class="sxs-lookup"><span data-stu-id="ccf89-115">Pointer to the smallest rectangle object that completely encloses the glyph.</span></span> <span data-ttu-id="ccf89-116">Vea [Rect](/previous-versions//ms536136(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ccf89-116">See [RECT](/previous-versions//ms536136(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ccf89-117">*pCellInc* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ccf89-117">*pCellInc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccf89-118">Tipo: **Point \***</span><span class="sxs-lookup"><span data-stu-id="ccf89-118">Type: **POINT\***</span></span>

<span data-ttu-id="ccf89-119">Puntero al vector bidimensional que conecta el origen de la celda de carácter actual con el origen de la celda de carácter siguiente.</span><span class="sxs-lookup"><span data-stu-id="ccf89-119">Pointer to the two-dimensional vector that connects the origin of the current character cell to the origin of the next character cell.</span></span> <span data-ttu-id="ccf89-120">Vea [Point](/previous-versions//ms536119(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ccf89-120">See [POINT](/previous-versions//ms536119(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccf89-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ccf89-121">Return value</span></span>

<span data-ttu-id="ccf89-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ccf89-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ccf89-123">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ccf89-123">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ccf89-124">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="ccf89-124">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccf89-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ccf89-125">Requirements</span></span>



| <span data-ttu-id="ccf89-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccf89-126">Requirement</span></span> | <span data-ttu-id="ccf89-127">Value</span><span class="sxs-lookup"><span data-stu-id="ccf89-127">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ccf89-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ccf89-128">Header</span></span><br/>  | <dl> <span data-ttu-id="ccf89-129"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="ccf89-129"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="ccf89-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ccf89-130">Library</span></span><br/> | <dl> <span data-ttu-id="ccf89-131"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ccf89-131"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccf89-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="ccf89-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccf89-133">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="ccf89-133">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="ccf89-134">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="ccf89-134">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
