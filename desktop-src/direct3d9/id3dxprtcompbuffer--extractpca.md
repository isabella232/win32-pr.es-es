---
description: Extrae los coeficientes de proyección de análisis de componentes principales por ejemplo (PCA) de un búfer de datos comprimidos ID3DXPRTCompBuffer.
ms.assetid: 149098c2-35ca-46e9-a13a-94906c95cfd9
title: 'ID3DXPRTCompBuffer:: ExtractPCA (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractPCA
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6ef949e9f88a843f4636643dadd7d00ffd94d98b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717641"
---
# <a name="id3dxprtcompbufferextractpca-method"></a><span data-ttu-id="7f273-103">ID3DXPRTCompBuffer:: ExtractPCA (método)</span><span class="sxs-lookup"><span data-stu-id="7f273-103">ID3DXPRTCompBuffer::ExtractPCA method</span></span>

<span data-ttu-id="7f273-104">Extrae los coeficientes de proyección de análisis de componentes principales por ejemplo (PCA) de un búfer de datos comprimidos [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="7f273-104">Extracts the per-sample principal component analysis (PCA) projection coefficients from an [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) compressed data buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f273-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7f273-105">Syntax</span></span>


```C++
HRESULT ExtractPCA(
  [in] UINT  StartPCA,
  [in] UINT  NumExtract,
  [in] FLOAT *pPCACoefficients
);
```



## <a name="parameters"></a><span data-ttu-id="7f273-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7f273-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f273-107">*StartPCA* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7f273-107">*StartPCA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f273-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7f273-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7f273-109">Índice inicial de los coeficientes de proyección de PCA que se va a extraer del búfer.</span><span class="sxs-lookup"><span data-stu-id="7f273-109">Starting index for PCA projection coefficients to extract from the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="7f273-110">*NumExtract* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7f273-110">*NumExtract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f273-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7f273-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7f273-112">Número de coeficientes de proyección de PCA que se van a extraer del búfer.</span><span class="sxs-lookup"><span data-stu-id="7f273-112">Number of PCA projection coefficients to extract from the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="7f273-113">*pPCACoefficients* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7f273-113">*pPCACoefficients* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f273-114">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="7f273-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7f273-115">Puntero a la ubicación donde se escriben los coeficientes de análisis de componentes principales en clúster (CPCA).</span><span class="sxs-lookup"><span data-stu-id="7f273-115">Pointer to the location where clustered principal component analysis (CPCA) coefficients are written.</span></span> <span data-ttu-id="7f273-116">El tamaño de los datos escritos es (número de muestras) \* (número de coeficientes de PCA).</span><span class="sxs-lookup"><span data-stu-id="7f273-116">The size of the data written is (Number of Samples) \* (Number of PCA Coefficients).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f273-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7f273-117">Return value</span></span>

<span data-ttu-id="7f273-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7f273-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7f273-119">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7f273-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="7f273-120">Si se produce un error en el método, se devolverá el valor siguiente.</span><span class="sxs-lookup"><span data-stu-id="7f273-120">If the method fails, the following value will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f273-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f273-121">Requirements</span></span>



| <span data-ttu-id="7f273-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f273-122">Requirement</span></span> | <span data-ttu-id="7f273-123">Value</span><span class="sxs-lookup"><span data-stu-id="7f273-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f273-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7f273-124">Header</span></span><br/>  | <dl> <span data-ttu-id="7f273-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f273-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="7f273-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7f273-126">Library</span></span><br/> | <dl> <span data-ttu-id="7f273-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7f273-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7f273-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="7f273-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f273-129">ID3DXPRTCompBuffer</span><span class="sxs-lookup"><span data-stu-id="7f273-129">ID3DXPRTCompBuffer</span></span>](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
