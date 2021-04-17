---
description: Obtiene una descripción del objeto de fuente actual.
ms.assetid: f08beb35-351f-4087-a2db-097843463291
title: 'ID3DX10Font:: GetDesc (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetDesc
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 59a7e361ebb6254fcc49eab30ff44ab39c38fd76
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105670251"
---
# <a name="id3dx10fontgetdesc-method"></a><span data-ttu-id="b821b-103">ID3DX10Font:: GetDesc (método)</span><span class="sxs-lookup"><span data-stu-id="b821b-103">ID3DX10Font::GetDesc method</span></span>

<span data-ttu-id="b821b-104">Obtiene una descripción del objeto de fuente actual.</span><span class="sxs-lookup"><span data-stu-id="b821b-104">Get a description of the current font object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b821b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b821b-105">Syntax</span></span>


```C++
HRESULT GetDesc(
  [in] D3DX10_FONT_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="b821b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b821b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b821b-107">*pDesc* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b821b-107">*pDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b821b-108">Type: **[ **D3DX10 \_ Font \_ DESC**](d3dx10-font-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="b821b-108">Type: **[**D3DX10\_FONT\_DESC**](d3dx10-font-desc.md)\***</span></span>

<span data-ttu-id="b821b-109">Puntero a una estructura de [**\_ \_ DESC de fuente D3DX10**](d3dx10-font-desc.md) que describe el objeto de fuente.</span><span class="sxs-lookup"><span data-stu-id="b821b-109">Pointer to a [**D3DX10\_FONT\_DESC**](d3dx10-font-desc.md) structure that describes the font object.</span></span> <span data-ttu-id="b821b-110">Si se define Unicode, se devuelve un puntero a un DESCW de D3DX10FONT \_ ; de lo contrario, se devuelve un puntero a D3DX10FONT \_ Desca.</span><span class="sxs-lookup"><span data-stu-id="b821b-110">If UNICODE is defined, a pointer to a D3DX10FONT\_DESCW is returned; otherwise a pointer to a D3DX10FONT\_DESCA is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b821b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b821b-111">Return value</span></span>

<span data-ttu-id="b821b-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b821b-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b821b-113">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b821b-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="b821b-114">Si se produce un error en el método, se devolverá el valor siguiente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="b821b-114">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="b821b-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b821b-115">Remarks</span></span>

<span data-ttu-id="b821b-116">Este método describe los objetos de fuente Unicode si se define Unicode.</span><span class="sxs-lookup"><span data-stu-id="b821b-116">This method describes Unicode font objects if UNICODE is defined.</span></span> <span data-ttu-id="b821b-117">De lo contrario, se llama a GetDescA, que devuelve un puntero a la \_ estructura Desca de D3DX10FONT.</span><span class="sxs-lookup"><span data-stu-id="b821b-117">Otherwise GetDescA is called, which returns a pointer to the D3DX10FONT\_DESCA structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="b821b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b821b-118">Requirements</span></span>



| <span data-ttu-id="b821b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b821b-119">Requirement</span></span> | <span data-ttu-id="b821b-120">Value</span><span class="sxs-lookup"><span data-stu-id="b821b-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b821b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b821b-121">Header</span></span><br/>  | <dl> <span data-ttu-id="b821b-122"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="b821b-122"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="b821b-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b821b-123">Library</span></span><br/> | <dl> <span data-ttu-id="b821b-124"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b821b-124"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b821b-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="b821b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b821b-126">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="b821b-126">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="b821b-127">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="b821b-127">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




