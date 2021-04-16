---
description: Asigna índices en el intervalo de 0 a 255 a los Estados de transformación correspondientes.
ms.assetid: b0a1548c-de5d-4eff-baf9-4aecb5e13443
title: Macro D3DTS_WORLDMATRIX (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTS_WORLDMATRIX
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: f80996a37e2fb48bf8ca7ea73f714b04e711b263
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547859"
---
# <a name="d3dts_worldmatrix-macro"></a><span data-ttu-id="b0e3a-103">D3DTS \_ WORLDMATRIX (macro)</span><span class="sxs-lookup"><span data-stu-id="b0e3a-103">D3DTS\_WORLDMATRIX macro</span></span>

<span data-ttu-id="b0e3a-104">Asigna índices en el intervalo de 0 a 255 a los Estados de transformación correspondientes.</span><span class="sxs-lookup"><span data-stu-id="b0e3a-104">Maps indices in the range 0 through 255 to the corresponding transform states.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0e3a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b0e3a-105">Syntax</span></span>


```C++
D3DTRANSFORMSTATETYPE D3DTS_WORLDMATRIX(
   int index
);
```



## <a name="parameters"></a><span data-ttu-id="b0e3a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b0e3a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0e3a-107">*índice*</span><span class="sxs-lookup"><span data-stu-id="b0e3a-107">*index*</span></span> 
</dt> <dd>

<span data-ttu-id="b0e3a-108">Un valor de índice en el intervalo comprendido entre 0 y 255.</span><span class="sxs-lookup"><span data-stu-id="b0e3a-108">An index value in the range 0 through 255.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0e3a-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b0e3a-109">Return value</span></span>

<span data-ttu-id="b0e3a-110">[**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) que se asigna al *Índice* especificado.</span><span class="sxs-lookup"><span data-stu-id="b0e3a-110">The [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) that maps to the given *index*.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0e3a-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b0e3a-111">Remarks</span></span>

<span data-ttu-id="b0e3a-112">Los Estados de transformación en el intervalo de 256 a 511 se reservan para almacenar hasta 256 matrices que se pueden indexar con índices de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="b0e3a-112">Transform states in the range 256 through 511 are reserved to store up to 256 matrices that can be indexed using 8-bit indices.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0e3a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0e3a-113">Requirements</span></span>



| <span data-ttu-id="b0e3a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0e3a-114">Requirement</span></span> | <span data-ttu-id="b0e3a-115">Value</span><span class="sxs-lookup"><span data-stu-id="b0e3a-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0e3a-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b0e3a-116">Header</span></span><br/> | <dl> <span data-ttu-id="b0e3a-117"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0e3a-117"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0e3a-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="b0e3a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0e3a-119">Macros</span><span class="sxs-lookup"><span data-stu-id="b0e3a-119">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="b0e3a-120">**SetTransform**</span><span class="sxs-lookup"><span data-stu-id="b0e3a-120">**SetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> </dl>

 

 
