---
title: Método ID3DX11EffectMatrixVariable SetMatrixTransposeArray (D3dx11effect. h)
description: Transponer y establecer una matriz de matrices de punto flotante.
ms.assetid: 08223022-5e77-4a84-9b68-b9b0c9a02270
keywords:
- Método SetMatrixTransposeArray Direct3D 11
- Método SetMatrixTransposeArray Direct3D 11, interfaz ID3DX11EffectMatrixVariable
- Interfaz ID3DX11EffectMatrixVariable Direct3D 11, método SetMatrixTransposeArray
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.SetMatrixTransposeArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f70676b76658b5732c1a2ee15858f83694272b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003928"
---
# <a name="id3dx11effectmatrixvariablesetmatrixtransposearray-method"></a><span data-ttu-id="db0e9-106">ID3DX11EffectMatrixVariable:: SetMatrixTransposeArray (método)</span><span class="sxs-lookup"><span data-stu-id="db0e9-106">ID3DX11EffectMatrixVariable::SetMatrixTransposeArray method</span></span>

<span data-ttu-id="db0e9-107">Transponer y establecer una matriz de matrices de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="db0e9-107">Transpose and set an array of floating-point matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="db0e9-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="db0e9-108">Syntax</span></span>


```C++
HRESULT SetMatrixTransposeArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a><span data-ttu-id="db0e9-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="db0e9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db0e9-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="db0e9-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="db0e9-111">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="db0e9-111">Type: **float\***</span></span>

<span data-ttu-id="db0e9-112">Puntero a una matriz de matrices.</span><span class="sxs-lookup"><span data-stu-id="db0e9-112">A pointer to an array of matrices.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="db0e9-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="db0e9-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="db0e9-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="db0e9-115">Desplazamiento (en número de matrices) entre el inicio de la matriz y la primera matriz que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="db0e9-115">The offset (in number of matrices) between the start of the array and the first matrix to set.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-116">*Recuento*</span><span class="sxs-lookup"><span data-stu-id="db0e9-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="db0e9-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="db0e9-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="db0e9-118">Número de matrices de la matriz que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="db0e9-118">The number of matrices in the array to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db0e9-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="db0e9-119">Return value</span></span>

<span data-ttu-id="db0e9-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="db0e9-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="db0e9-121">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="db0e9-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="db0e9-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="db0e9-122">Remarks</span></span>

<span data-ttu-id="db0e9-123">Transponer una matriz reorganizará el orden de los datos del orden de las columnas de fila al orden de las filas de columnas (o viceversa).</span><span class="sxs-lookup"><span data-stu-id="db0e9-123">Transposing a matrix will rearrange the data order from row-column order to column-row order (or vice versa).</span></span>

> [!Note]  
> <span data-ttu-id="db0e9-124">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="db0e9-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="db0e9-125">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="db0e9-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="db0e9-126">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="db0e9-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="db0e9-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db0e9-127">Requirements</span></span>



| <span data-ttu-id="db0e9-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="db0e9-128">Requirement</span></span> | <span data-ttu-id="db0e9-129">Value</span><span class="sxs-lookup"><span data-stu-id="db0e9-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db0e9-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="db0e9-130">Header</span></span><br/>  | <dl> <span data-ttu-id="db0e9-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="db0e9-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="db0e9-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="db0e9-132">Library</span></span><br/> | <dl> <span data-ttu-id="db0e9-133"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="db0e9-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db0e9-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="db0e9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db0e9-135">ID3DX11EffectMatrixVariable</span><span class="sxs-lookup"><span data-stu-id="db0e9-135">ID3DX11EffectMatrixVariable</span></span>](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

