---
title: Método ID3DX11EffectMatrixVariable GetMatrixTransposeArray (D3dx11effect. h)
description: Transponer y obtener una matriz de matrices de punto flotante.
ms.assetid: cfcdbda0-b321-4e94-8d09-bb9d7ddfb4a5
keywords:
- Método GetMatrixTransposeArray Direct3D 11
- Método GetMatrixTransposeArray Direct3D 11, interfaz ID3DX11EffectMatrixVariable
- Interfaz ID3DX11EffectMatrixVariable Direct3D 11, método GetMatrixTransposeArray
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.GetMatrixTransposeArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80d0a43e69ccf88c15d8296c024535dec42b3f31
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986935"
---
# <a name="id3dx11effectmatrixvariablegetmatrixtransposearray-method"></a><span data-ttu-id="5dc11-106">ID3DX11EffectMatrixVariable:: GetMatrixTransposeArray (método)</span><span class="sxs-lookup"><span data-stu-id="5dc11-106">ID3DX11EffectMatrixVariable::GetMatrixTransposeArray method</span></span>

<span data-ttu-id="5dc11-107">Transponer y obtener una matriz de matrices de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="5dc11-107">Transpose and get an array of floating-point matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="5dc11-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5dc11-108">Syntax</span></span>


```C++
HRESULT GetMatrixTransposeArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a><span data-ttu-id="5dc11-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5dc11-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5dc11-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="5dc11-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="5dc11-111">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="5dc11-111">Type: **float\***</span></span>

<span data-ttu-id="5dc11-112">Puntero al primer elemento de una matriz de matrices de tranposed.</span><span class="sxs-lookup"><span data-stu-id="5dc11-112">A pointer to the first element of an array of tranposed matrices.</span></span>

</dd> <dt>

<span data-ttu-id="5dc11-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="5dc11-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="5dc11-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5dc11-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5dc11-115">Desplazamiento (en número de matrices) entre el inicio de la matriz y la primera matriz que se va a obtener.</span><span class="sxs-lookup"><span data-stu-id="5dc11-115">The offset (in number of matrices) between the start of the array and the first matrix to get.</span></span>

</dd> <dt>

<span data-ttu-id="5dc11-116">*Recuento*</span><span class="sxs-lookup"><span data-stu-id="5dc11-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="5dc11-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5dc11-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5dc11-118">Número de matrices de la matriz que se van a obtener.</span><span class="sxs-lookup"><span data-stu-id="5dc11-118">The number of matrices in the array to get.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5dc11-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5dc11-119">Return value</span></span>

<span data-ttu-id="5dc11-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5dc11-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5dc11-121">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="5dc11-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5dc11-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5dc11-122">Remarks</span></span>

<span data-ttu-id="5dc11-123">Transponer una matriz reorganizará el orden de los datos del orden de las columnas de fila al orden de las filas de columnas (o viceversa).</span><span class="sxs-lookup"><span data-stu-id="5dc11-123">Transposing a matrix will rearrange the data order from row-column order to column-row order (or vice versa).</span></span>

> [!Note]  
> <span data-ttu-id="5dc11-124">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="5dc11-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="5dc11-125">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="5dc11-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="5dc11-126">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="5dc11-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5dc11-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5dc11-127">Requirements</span></span>



| <span data-ttu-id="5dc11-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="5dc11-128">Requirement</span></span> | <span data-ttu-id="5dc11-129">Value</span><span class="sxs-lookup"><span data-stu-id="5dc11-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5dc11-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5dc11-130">Header</span></span><br/>  | <dl> <span data-ttu-id="5dc11-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="5dc11-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="5dc11-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5dc11-132">Library</span></span><br/> | <dl> <span data-ttu-id="5dc11-133"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="5dc11-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5dc11-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="5dc11-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dc11-135">ID3DX11EffectMatrixVariable</span><span class="sxs-lookup"><span data-stu-id="5dc11-135">ID3DX11EffectMatrixVariable</span></span>](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

