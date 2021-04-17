---
description: Multiplica cada valor del búfer por un valor constante.
ms.assetid: 3d7ef530-b83a-4123-a2ed-fff2b21378ee
title: 'ID3DXPRTBuffer:: ScaleBuffer (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ScaleBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 05bdd066f4b7c33ad06f089551f16f0489608c83
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698429"
---
# <a name="id3dxprtbufferscalebuffer-method"></a><span data-ttu-id="c67a3-103">ID3DXPRTBuffer:: ScaleBuffer (método)</span><span class="sxs-lookup"><span data-stu-id="c67a3-103">ID3DXPRTBuffer::ScaleBuffer method</span></span>

<span data-ttu-id="c67a3-104">Multiplica cada valor del búfer por un valor constante.</span><span class="sxs-lookup"><span data-stu-id="c67a3-104">Multiplies every value in the buffer by a constant value.</span></span>

## <a name="syntax"></a><span data-ttu-id="c67a3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c67a3-105">Syntax</span></span>


```C++
HRESULT ScaleBuffer(
  [in] FLOAT Scale
);
```



## <a name="parameters"></a><span data-ttu-id="c67a3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c67a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c67a3-107">*Escala* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c67a3-107">*Scale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c67a3-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c67a3-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c67a3-109">Valor constante que se usa para escalar el búfer.</span><span class="sxs-lookup"><span data-stu-id="c67a3-109">Constant value used to scale the buffer.</span></span> <span data-ttu-id="c67a3-110">Cada valor del búfer se sustituye por el producto de este valor y el valor de búfer original.</span><span class="sxs-lookup"><span data-stu-id="c67a3-110">Every value in the buffer is replaced by the product of this value and the original buffer value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c67a3-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c67a3-111">Return value</span></span>

<span data-ttu-id="c67a3-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c67a3-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c67a3-113">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c67a3-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="c67a3-114">Si se produce un error en el método, se devolverá el valor siguiente.</span><span class="sxs-lookup"><span data-stu-id="c67a3-114">If the method fails, the following value will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="c67a3-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c67a3-115">Requirements</span></span>



| <span data-ttu-id="c67a3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c67a3-116">Requirement</span></span> | <span data-ttu-id="c67a3-117">Value</span><span class="sxs-lookup"><span data-stu-id="c67a3-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c67a3-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c67a3-118">Header</span></span><br/>  | <dl> <span data-ttu-id="c67a3-119"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="c67a3-119"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="c67a3-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c67a3-120">Library</span></span><br/> | <dl> <span data-ttu-id="c67a3-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c67a3-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c67a3-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="c67a3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c67a3-123">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="c67a3-123">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> </dl>

 

 
