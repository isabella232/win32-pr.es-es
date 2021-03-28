---
title: D3DX_R16G16_FLOAT_to_FLOAT2 función)
description: Desempaqueta los \_ \_ \_ \_ datos de sombreador B8G8R8X8 UNORM sRGB Format en XMFLOAT2.
ms.assetid: 6c57dc86-d034-4b54-8572-44ac3738beb9
keywords:
- D3DX_R16G16_FLOAT_to_FLOAT2 de la función HLSL
topic_type:
- apiref
api_name:
- D3DX_R16G16_FLOAT_to_FLOAT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e6fb721e59a63415f98216b6e3f81a92e7598f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157240"
---
# <a name="d3dx_r16g16_float_to_float2-function"></a><span data-ttu-id="3aaf1-104">D3DX \_ R16G16 \_ float \_ a \_ FLOAT2 función)</span><span class="sxs-lookup"><span data-stu-id="3aaf1-104">D3DX\_R16G16\_FLOAT\_to\_FLOAT2 function</span></span>

<span data-ttu-id="3aaf1-105">Desempaqueta los \_ \_ \_ \_ datos de sombreador B8G8R8X8 UNORM sRGB Format en XMFLOAT2.</span><span class="sxs-lookup"><span data-stu-id="3aaf1-105">Unpacks DXGI\_FORMAT\_B8G8R8X8\_UNORM\_SRGB shader data to an XMFLOAT2.</span></span>

## <a name="syntax"></a><span data-ttu-id="3aaf1-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3aaf1-106">Syntax</span></span>

``` syntax
XMFLOAT2 D3DX_R16G16_FLOAT_to_FLOAT2(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="3aaf1-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3aaf1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3aaf1-108">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="3aaf1-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="3aaf1-109">Datos del sombreador empaquetado.</span><span class="sxs-lookup"><span data-stu-id="3aaf1-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3aaf1-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3aaf1-110">Return value</span></span>

<span data-ttu-id="3aaf1-111">Datos del sombreador desempaquetado.</span><span class="sxs-lookup"><span data-stu-id="3aaf1-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="3aaf1-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3aaf1-112">Requirements</span></span>



| <span data-ttu-id="3aaf1-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="3aaf1-113">Requirement</span></span> | <span data-ttu-id="3aaf1-114">Value</span><span class="sxs-lookup"><span data-stu-id="3aaf1-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3aaf1-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3aaf1-115">Header</span></span><br/> | <dl> <span data-ttu-id="3aaf1-116"><dt>D3DX \_ DXGIFormatConvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="3aaf1-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3aaf1-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="3aaf1-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3aaf1-118">Funciones</span><span class="sxs-lookup"><span data-stu-id="3aaf1-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="3aaf1-119">Desempaquetar y empaquetar el \_ formato de DXGI para la edición de In-Place imagen</span><span class="sxs-lookup"><span data-stu-id="3aaf1-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





