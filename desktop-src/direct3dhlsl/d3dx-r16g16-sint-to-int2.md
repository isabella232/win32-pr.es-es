---
title: D3DX_R16G16_SINT_to_INT2 función)
description: Desempaqueta los \_ datos del \_ \_ sombreador R16G16 de los formatos de DXGI en un XMINT2.
ms.assetid: 0aad1581-5fd8-43c0-828d-51ef9eb82a74
keywords:
- D3DX_R16G16_SINT_to_INT2 de la función HLSL
topic_type:
- apiref
api_name:
- D3DX_R16G16_SINT_to_INT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9e14e935b49e1fa0c982551696e8d38a076a5bf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998653"
---
# <a name="d3dx_r16g16_sint_to_int2-function"></a><span data-ttu-id="50471-104">D3DX \_ R16G16 \_ Sint \_ a la \_ función INT2</span><span class="sxs-lookup"><span data-stu-id="50471-104">D3DX\_R16G16\_SINT\_to\_INT2 function</span></span>

<span data-ttu-id="50471-105">Desempaqueta los \_ datos del \_ \_ sombreador R16G16 de los formatos de DXGI en un XMINT2.</span><span class="sxs-lookup"><span data-stu-id="50471-105">Unpacks DXGI\_FORMAT\_R16G16\_SINT shader data to an XMINT2.</span></span>

## <a name="syntax"></a><span data-ttu-id="50471-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="50471-106">Syntax</span></span>

``` syntax
XMINT2 D3DX_R16G16_SINT_to_INT2(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="50471-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="50471-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50471-108">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="50471-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="50471-109">Datos del sombreador empaquetado.</span><span class="sxs-lookup"><span data-stu-id="50471-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50471-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="50471-110">Return value</span></span>

<span data-ttu-id="50471-111">Datos del sombreador desempaquetado.</span><span class="sxs-lookup"><span data-stu-id="50471-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="50471-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50471-112">Requirements</span></span>



| <span data-ttu-id="50471-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="50471-113">Requirement</span></span> | <span data-ttu-id="50471-114">Value</span><span class="sxs-lookup"><span data-stu-id="50471-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50471-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="50471-115">Header</span></span><br/> | <dl> <span data-ttu-id="50471-116"><dt>D3DX \_ DXGIFormatConvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="50471-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50471-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="50471-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50471-118">Funciones</span><span class="sxs-lookup"><span data-stu-id="50471-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="50471-119">Desempaquetar y empaquetar el \_ formato de DXGI para la edición de In-Place imagen</span><span class="sxs-lookup"><span data-stu-id="50471-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





