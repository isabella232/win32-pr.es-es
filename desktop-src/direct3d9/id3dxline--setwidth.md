---
description: Especifica el grosor de la línea.
ms.assetid: cedf9217-2b47-40c3-a64c-9872c1083d71
title: 'ID3DXLine:: SetWidth (método) (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.SetWidth
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d357d7516233caf6ef9206aa2aecc2a98a435cde
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083792"
---
# <a name="id3dxlinesetwidth-method"></a><span data-ttu-id="b0a09-103">ID3DXLine:: SetWidth (método)</span><span class="sxs-lookup"><span data-stu-id="b0a09-103">ID3DXLine::SetWidth method</span></span>

<span data-ttu-id="b0a09-104">Especifica el grosor de la línea.</span><span class="sxs-lookup"><span data-stu-id="b0a09-104">Specifies the thickness of the line.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0a09-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b0a09-105">Syntax</span></span>


```C++
HRESULT SetWidth(
  [in] FLOAT fWidth
);
```



## <a name="parameters"></a><span data-ttu-id="b0a09-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b0a09-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0a09-107">*fWidth* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b0a09-107">*fWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0a09-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b0a09-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b0a09-109">Describe el ancho de línea.</span><span class="sxs-lookup"><span data-stu-id="b0a09-109">Describes the line width.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0a09-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b0a09-110">Return value</span></span>

<span data-ttu-id="b0a09-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b0a09-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b0a09-112">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b0a09-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b0a09-113">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="b0a09-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0a09-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0a09-114">Requirements</span></span>



| <span data-ttu-id="b0a09-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0a09-115">Requirement</span></span> | <span data-ttu-id="b0a09-116">Value</span><span class="sxs-lookup"><span data-stu-id="b0a09-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0a09-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b0a09-117">Header</span></span><br/>  | <dl> <span data-ttu-id="b0a09-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0a09-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="b0a09-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b0a09-119">Library</span></span><br/> | <dl> <span data-ttu-id="b0a09-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b0a09-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b0a09-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="b0a09-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0a09-122">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="b0a09-122">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
