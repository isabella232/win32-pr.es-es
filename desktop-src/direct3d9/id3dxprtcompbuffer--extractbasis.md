---
description: Extrae los vectores de referencia media y de análisis de componentes principales (PCA) para un clúster determinado a partir de un búfer de datos comprimidos ID3DXPRTCompBuffer.
ms.assetid: dcb1372f-2c8f-4d18-9840-5982b2ed0d6e
title: 'ID3DXPRTCompBuffer:: ExtractBasis (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractBasis
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ebedef91c9f3d1e277a099ffd295903e9ba77ba8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718317"
---
# <a name="id3dxprtcompbufferextractbasis-method"></a><span data-ttu-id="f66c6-103">ID3DXPRTCompBuffer:: ExtractBasis (método)</span><span class="sxs-lookup"><span data-stu-id="f66c6-103">ID3DXPRTCompBuffer::ExtractBasis method</span></span>

<span data-ttu-id="f66c6-104">Extrae los vectores de referencia media y de análisis de componentes principales (PCA) para un clúster determinado a partir de un búfer de datos comprimidos [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="f66c6-104">Extracts the mean and principal component analysis (PCA) basis vectors for a given cluster from an [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) compressed data buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="f66c6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f66c6-105">Syntax</span></span>


```C++
HRESULT ExtractBasis(
  [in]      UINT  Cluster,
  [in, out] FLOAT *pClusterBasis
);
```



## <a name="parameters"></a><span data-ttu-id="f66c6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f66c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f66c6-107">*Clúster* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="f66c6-107">*Cluster* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f66c6-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f66c6-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f66c6-109">Clúster para el que se extraerá la base.</span><span class="sxs-lookup"><span data-stu-id="f66c6-109">Cluster for which the basis will be extracted.</span></span>

</dd> <dt>

<span data-ttu-id="f66c6-110">*pClusterBasis* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f66c6-110">*pClusterBasis* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f66c6-111">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f66c6-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f66c6-112">Puntero a una matriz de datos vectoriales básicos del clúster.</span><span class="sxs-lookup"><span data-stu-id="f66c6-112">Pointer to an array of basis vector data for Cluster.</span></span> <span data-ttu-id="f66c6-113">El tamaño de los datos FLOAT almacenados será: (1 + número de vectores PCA por clúster) \* (número de coeficientes) \* (número de canales de color)</span><span class="sxs-lookup"><span data-stu-id="f66c6-113">The size of the FLOAT data stored will be: (1 + Number of PCA vectors per cluster) \* (Number of coefficients) \* (Number of color channels)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f66c6-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f66c6-114">Return value</span></span>

<span data-ttu-id="f66c6-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f66c6-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f66c6-116">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f66c6-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="f66c6-117">Si se produce un error en el método, se devolverá el valor siguiente.</span><span class="sxs-lookup"><span data-stu-id="f66c6-117">If the method fails, the following value will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="f66c6-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f66c6-118">Requirements</span></span>



| <span data-ttu-id="f66c6-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f66c6-119">Requirement</span></span> | <span data-ttu-id="f66c6-120">Value</span><span class="sxs-lookup"><span data-stu-id="f66c6-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f66c6-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f66c6-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f66c6-122"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="f66c6-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="f66c6-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f66c6-123">Library</span></span><br/> | <dl> <span data-ttu-id="f66c6-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f66c6-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f66c6-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="f66c6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f66c6-126">ID3DXPRTCompBuffer</span><span class="sxs-lookup"><span data-stu-id="f66c6-126">ID3DXPRTCompBuffer</span></span>](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
