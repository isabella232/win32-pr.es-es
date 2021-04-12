---
description: Procesa algunos datos.
ms.assetid: c64f6a2d-4512-4028-8ed9-bfc5e9e86758
title: ID3DX10DataProcessor::P método rador (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataProcessor.Process
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2ddad2f6350f48f65bc82e094eccb92b1b8bf390
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280531"
---
# <a name="id3dx10dataprocessorprocess-method"></a><span data-ttu-id="9d158-103">ID3DX10DataProcessor::P método rador</span><span class="sxs-lookup"><span data-stu-id="9d158-103">ID3DX10DataProcessor::Process method</span></span>

<span data-ttu-id="9d158-104">Procesa algunos datos.</span><span class="sxs-lookup"><span data-stu-id="9d158-104">Process some data.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d158-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9d158-105">Syntax</span></span>


```C++
HRESULT Process(
  [in] void   *pData,
  [in] SIZE_T cBytes
);
```



## <a name="parameters"></a><span data-ttu-id="9d158-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9d158-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d158-107">*pdata* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9d158-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d158-108">Tipo: **void \***</span><span class="sxs-lookup"><span data-stu-id="9d158-108">Type: **void\***</span></span>

<span data-ttu-id="9d158-109">Puntero a los datos que se van a procesar.</span><span class="sxs-lookup"><span data-stu-id="9d158-109">Pointer to the data to be processed.</span></span>

</dd> <dt>

<span data-ttu-id="9d158-110">*cBytes* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9d158-110">*cBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d158-111">Tipo: **[ **tamaño \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9d158-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9d158-112">Tamaño de los datos que se van a procesar.</span><span class="sxs-lookup"><span data-stu-id="9d158-112">Size of the data to be processed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d158-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9d158-113">Return value</span></span>

<span data-ttu-id="9d158-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9d158-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9d158-115">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="9d158-115">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9d158-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d158-116">Requirements</span></span>



| <span data-ttu-id="9d158-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d158-117">Requirement</span></span> | <span data-ttu-id="9d158-118">Value</span><span class="sxs-lookup"><span data-stu-id="9d158-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9d158-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9d158-119">Header</span></span><br/>  | <dl> <span data-ttu-id="9d158-120"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d158-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="9d158-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9d158-121">Library</span></span><br/> | <dl> <span data-ttu-id="9d158-122"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9d158-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d158-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="9d158-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d158-124">ID3DX10DataProcessor</span><span class="sxs-lookup"><span data-stu-id="9d158-124">ID3DX10DataProcessor</span></span>](id3dx10dataprocessor.md)
</dt> <dt>

[<span data-ttu-id="9d158-125">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="9d158-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
