---
description: Guarda en el disco un búfer comprimido de Radiance (PRT) comprimido previamente.
ms.assetid: cc94a83e-f755-411d-a993-4529c5d53cd5
title: Función D3DXSavePRTCompBufferToFile (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSavePRTCompBufferToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d06629185637ce6fa0d7d33d5454282d2bbb8ec2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003806"
---
# <a name="d3dxsaveprtcompbuffertofile-function"></a><span data-ttu-id="0683e-103">D3DXSavePRTCompBufferToFile función)</span><span class="sxs-lookup"><span data-stu-id="0683e-103">D3DXSavePRTCompBufferToFile function</span></span>

<span data-ttu-id="0683e-104">Guarda en el disco un búfer comprimido de Radiance (PRT) comprimido previamente.</span><span class="sxs-lookup"><span data-stu-id="0683e-104">Saves a compressed precomputed radiance transfer (PRT) buffer to disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="0683e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0683e-105">Syntax</span></span>

```cpp
HRESULT D3DXSavePRTCompBufferToFile(
  _In_ LPCSTR              pFileName,
  _In_ LPD3DXPRTCOMPBUFFER pBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="0683e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0683e-106">Parameters</span></span>

<span data-ttu-id="0683e-107">*pFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0683e-107">*pFileName* \[in\]</span></span>

<span data-ttu-id="0683e-108">Tipo: **[LPCSTR](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0683e-108">Type: **[LPCSTR](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0683e-109">Nombre del archivo en el que se va a guardar el búfer comprimido.</span><span class="sxs-lookup"><span data-stu-id="0683e-109">Name of the file to which the compressed buffer is to be saved.</span></span>

<span data-ttu-id="0683e-110">*pBuffer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0683e-110">*pBuffer* \[in\]</span></span>

<span data-ttu-id="0683e-111">Tipo: **[LPD3DXPRTCOMPBUFFER](id3dxprtcompbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="0683e-111">Type: **[LPD3DXPRTCOMPBUFFER](id3dxprtcompbuffer.md)**</span></span>

<span data-ttu-id="0683e-112">Dirección de un puntero al objeto [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) de entrada.</span><span class="sxs-lookup"><span data-stu-id="0683e-112">Address of a pointer to the input [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="0683e-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0683e-113">Return value</span></span>

<span data-ttu-id="0683e-114">Tipo: **[HRESULT](../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="0683e-114">Type: **[HRESULT](../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="0683e-115">Si el método se ejecuta correctamente, el valor devuelto es **D3D \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0683e-115">If the method succeeds, then the return value is **D3D\_OK**.</span></span> <span data-ttu-id="0683e-116">Si se produce un error en el método, el valor devuelto puede ser **D3DERR \_ INVALIDCALL**.</span><span class="sxs-lookup"><span data-stu-id="0683e-116">If the method fails, then the return value can be **D3DERR\_INVALIDCALL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0683e-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0683e-117">Remarks</span></span>

<span data-ttu-id="0683e-118">La configuración del compilador también determina la versión de la función.</span><span class="sxs-lookup"><span data-stu-id="0683e-118">The compiler setting also determines the function version.</span></span> <span data-ttu-id="0683e-119">Si se define Unicode, la llamada de función se resuelve como [D3DXSavePRTCompBufferToFileW]().</span><span class="sxs-lookup"><span data-stu-id="0683e-119">If Unicode is defined, then the function call resolves to [D3DXSavePRTCompBufferToFileW]().</span></span> <span data-ttu-id="0683e-120">De lo contrario, la llamada de función se resuelve como **D3DXSavePRTCompBufferToFileA**.</span><span class="sxs-lookup"><span data-stu-id="0683e-120">Otherwise, the function call resolves to **D3DXSavePRTCompBufferToFileA**.</span></span>

<span data-ttu-id="0683e-121">El formato de archivo PCA es un archivo binario en forma de encabezado y, a continuación, dos o tres bloques de datos.</span><span class="sxs-lookup"><span data-stu-id="0683e-121">The PCA file format is a binary file in the form of a header and then two or three data blocks.</span></span>

```cpp
struct PRTCompressHeader
{
    UINT NumSamples;
    UINT NumCoeffs;
    UINT NumChannels;
    UINT TexWidth;
    UINT TexHeight;
    UINT bIsTex;
    UINT NumClusters;
    UINT NumPCA;
};
```

<span data-ttu-id="0683e-122">En el caso de que *bIsTex* sea distinto de cero, *NumSamples* debe ser igual `TexWidth * TexHeight` .</span><span class="sxs-lookup"><span data-stu-id="0683e-122">For the case of *bIsTex* being non-zero, *NumSamples* should equal `TexWidth * TexHeight`.</span></span>

<span data-ttu-id="0683e-123">El bloque de datos base que sigue al encabezado es `NumCoeffs * NumChannels * (NumPCA + 1) * NumClusters * sizeof(float)` bytes.</span><span class="sxs-lookup"><span data-stu-id="0683e-123">The basis data block that follows the header is `NumCoeffs * NumChannels * (NumPCA + 1) * NumClusters * sizeof(float)` bytes.</span></span>

<span data-ttu-id="0683e-124">A continuación se indican los bloques de datos de pesos del PCA, que son `NumPCA * NumSamples * sizeof(float)` bytes.</span><span class="sxs-lookup"><span data-stu-id="0683e-124">Following that is the PCA weights data block, which is `NumPCA * NumSamples * sizeof(float)` bytes.</span></span>

<span data-ttu-id="0683e-125">Si *NumClusters* es mayor que 1, el archivo finaliza con el bloque de datos de los identificadores de clúster de `NumSamples * sizeof(UINT)` bytes.</span><span class="sxs-lookup"><span data-stu-id="0683e-125">If *NumClusters* is greater than 1, then the file ends with the cluster IDs data block of `NumSamples * sizeof(UINT)` bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="0683e-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0683e-126">Requirements</span></span>

| <span data-ttu-id="0683e-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="0683e-127">Requirement</span></span> | <span data-ttu-id="0683e-128">Value</span><span class="sxs-lookup"><span data-stu-id="0683e-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0683e-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0683e-129">Header</span></span><br/>  | <dl> <span data-ttu-id="0683e-130"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="0683e-130"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="0683e-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0683e-131">Library</span></span><br/> | <dl> <span data-ttu-id="0683e-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0683e-132"><dt>D3dx9.lib</dt></span></span> </dl>   |

## <a name="see-also"></a><span data-ttu-id="0683e-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="0683e-133">See also</span></span>

[<span data-ttu-id="0683e-134">Funciones de transferencia Radiance precalculadas</span><span class="sxs-lookup"><span data-stu-id="0683e-134">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
