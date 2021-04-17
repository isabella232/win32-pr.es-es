---
description: Obtiene una descripción del objeto de fuente actual. GetDescW y GetDescA son idénticos a este método, salvo que se devuelve un puntero a una \_ estructura D3DXFONT DESCW o D3DXFONT \_ Desca, respectivamente.
ms.assetid: 21bcd3e0-3659-4d64-959a-0f2d65850cb1
title: 'ID3DXFont:: GetDesc (método) (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3310971e360fb9994a30d62349d3e7e4b764c7d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717747"
---
# <a name="id3dxfontgetdesc-method"></a><span data-ttu-id="3f6d5-104">ID3DXFont:: GetDesc (método)</span><span class="sxs-lookup"><span data-stu-id="3f6d5-104">ID3DXFont::GetDesc method</span></span>

<span data-ttu-id="3f6d5-105">Obtiene una descripción del objeto de fuente actual.</span><span class="sxs-lookup"><span data-stu-id="3f6d5-105">Gets a description of the current font object.</span></span> <span data-ttu-id="3f6d5-106">GetDescW y GetDescA son idénticos a este método, salvo que se devuelve un puntero a una estructura [**D3DXFONT \_ DESCW**](d3dxfont-desc.md) o **D3DXFONT \_ Desca** , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="3f6d5-106">GetDescW and GetDescA are identical to this method, except that a pointer is returned to a [**D3DXFONT\_DESCW**](d3dxfont-desc.md) or **D3DXFONT\_DESCA** structure, respectively.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f6d5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3f6d5-107">Syntax</span></span>


```C++
HRESULT GetDesc(
  [out] D3DXFONT_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="3f6d5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3f6d5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f6d5-109">*pDesc* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3f6d5-109">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f6d5-110">Tipo: **[ **D3DXFONT \_ DESC**](d3dxfont-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="3f6d5-110">Type: **[**D3DXFONT\_DESC**](d3dxfont-desc.md)\***</span></span>

<span data-ttu-id="3f6d5-111">Puntero a una [**estructura \_ DESC de D3DXFONT**](d3dxfont-desc.md) que describe el objeto de fuente.</span><span class="sxs-lookup"><span data-stu-id="3f6d5-111">Pointer to a [**D3DXFONT\_DESC**](d3dxfont-desc.md) structure that describes the font object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f6d5-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3f6d5-112">Return value</span></span>

<span data-ttu-id="3f6d5-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3f6d5-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3f6d5-114">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3f6d5-114">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="3f6d5-115">Si se produce un error en el método, se devolverá el valor siguiente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="3f6d5-115">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f6d5-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3f6d5-116">Remarks</span></span>

<span data-ttu-id="3f6d5-117">Este método describe los objetos de fuente Unicode si se define Unicode.</span><span class="sxs-lookup"><span data-stu-id="3f6d5-117">This method describes Unicode font objects if UNICODE is defined.</span></span> <span data-ttu-id="3f6d5-118">De lo contrario, se llama a GetDescA, que devuelve un puntero a la estructura [**\_ Desca de D3DXFONT**](d3dxfont-desc.md) .</span><span class="sxs-lookup"><span data-stu-id="3f6d5-118">Otherwise GetDescA is called, which returns a pointer to the [**D3DXFONT\_DESCA**](d3dxfont-desc.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f6d5-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f6d5-119">Requirements</span></span>



| <span data-ttu-id="3f6d5-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f6d5-120">Requirement</span></span> | <span data-ttu-id="3f6d5-121">Value</span><span class="sxs-lookup"><span data-stu-id="3f6d5-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f6d5-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3f6d5-122">Header</span></span><br/>  | <dl> <span data-ttu-id="3f6d5-123"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f6d5-123"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="3f6d5-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3f6d5-124">Library</span></span><br/> | <dl> <span data-ttu-id="3f6d5-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3f6d5-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3f6d5-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="3f6d5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f6d5-127">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="3f6d5-127">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 




