---
description: Guarda un búfer de Radiance Transfer (PRT) precalculado en el disco.
ms.assetid: 1fca69bd-6729-45af-981f-b7480c741bc2
title: Función D3DXSavePRTBufferToFile (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSavePRTBufferToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b796ee24be44bf65be7df938bdfe85d6784cc5f3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698228"
---
# <a name="d3dxsaveprtbuffertofile-function"></a><span data-ttu-id="b44b5-103">D3DXSavePRTBufferToFile función)</span><span class="sxs-lookup"><span data-stu-id="b44b5-103">D3DXSavePRTBufferToFile function</span></span>

<span data-ttu-id="b44b5-104">Guarda un búfer de Radiance Transfer (PRT) precalculado en el disco.</span><span class="sxs-lookup"><span data-stu-id="b44b5-104">Saves a precomputed radiance transfer (PRT) buffer to disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="b44b5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b44b5-105">Syntax</span></span>

```cpp
HRESULT D3DXSavePRTBufferToFile(
  _In_ LPCSTR          pFileName,
  _In_ LPD3DXPRTBUFFER pBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="b44b5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b44b5-106">Parameters</span></span>

<span data-ttu-id="b44b5-107">*pFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b44b5-107">*pFileName* \[in\]</span></span>

<span data-ttu-id="b44b5-108">Tipo: **[LPCSTR](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b44b5-108">Type: **[LPCSTR](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b44b5-109">Nombre del archivo en el que se va a guardar el búfer.</span><span class="sxs-lookup"><span data-stu-id="b44b5-109">Name of the file to which the buffer is to be saved.</span></span>

<span data-ttu-id="b44b5-110">*pBuffer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b44b5-110">*pBuffer* \[in\]</span></span>

<span data-ttu-id="b44b5-111">Tipo: **[LPD3DXPRTBUFFER](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="b44b5-111">Type: **[LPD3DXPRTBUFFER](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="b44b5-112">Dirección de un puntero al objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de entrada.</span><span class="sxs-lookup"><span data-stu-id="b44b5-112">Address of a pointer to the input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="b44b5-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b44b5-113">Return value</span></span>

<span data-ttu-id="b44b5-114">Tipo: **[HRESULT](../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="b44b5-114">Type: **[HRESULT](../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="b44b5-115">Si el método se ejecuta correctamente, el valor devuelto es **D3D \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b44b5-115">If the method succeeds, the return value is **D3D\_OK**.</span></span> <span data-ttu-id="b44b5-116">Si se produce un error en el método, el valor devuelto puede ser **D3DERR \_ INVALIDCALL**.</span><span class="sxs-lookup"><span data-stu-id="b44b5-116">If the method fails, the return value can be **D3DERR\_INVALIDCALL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b44b5-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b44b5-117">Remarks</span></span>

<span data-ttu-id="b44b5-118">La configuración del compilador también determina la versión de la función.</span><span class="sxs-lookup"><span data-stu-id="b44b5-118">The compiler setting also determines the function version.</span></span> <span data-ttu-id="b44b5-119">Si se define Unicode, la llamada de función se resuelve como [D3DXSavePRTBufferToFileW]().</span><span class="sxs-lookup"><span data-stu-id="b44b5-119">If Unicode is defined, then the function call resolves to [D3DXSavePRTBufferToFileW]().</span></span> <span data-ttu-id="b44b5-120">De lo contrario, la llamada de función se resuelve como **D3DXSavePRTBufferToFileA**.</span><span class="sxs-lookup"><span data-stu-id="b44b5-120">Otherwise, the function call resolves to **D3DXSavePRTBufferToFileA**.</span></span>

<span data-ttu-id="b44b5-121">El formato de archivo PRT es un archivo binario en forma de encabezado y, a continuación, un bloque de datos.</span><span class="sxs-lookup"><span data-stu-id="b44b5-121">The PRT file format is a binary file in the form of a header and then a data block.</span></span>

```cpp
struct PRTHeader
{
    UINT NumSamples;
    UINT NumCoeffs;
    UINT NumChannels;
    UINT TexWidth;
    UINT TexHeight;
    UINT bIsTex;
};
```

<span data-ttu-id="b44b5-122">En el caso de que *bIsTex* sea distinto de cero, *NumSamples* debe ser igual `TexWidth * TexHeight` .</span><span class="sxs-lookup"><span data-stu-id="b44b5-122">For the case of *bIsTex* being non-zero, *NumSamples* should equal `TexWidth * TexHeight`.</span></span>

<span data-ttu-id="b44b5-123">El bloque de datos que sigue al encabezado es `NumSamples * NumCoeffs * NumChannels * sizeof(float)` bytes.</span><span class="sxs-lookup"><span data-stu-id="b44b5-123">The data block that follows the header is `NumSamples * NumCoeffs * NumChannels * sizeof(float)` bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="b44b5-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b44b5-124">Requirements</span></span>

| <span data-ttu-id="b44b5-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b44b5-125">Requirement</span></span> | <span data-ttu-id="b44b5-126">Value</span><span class="sxs-lookup"><span data-stu-id="b44b5-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b44b5-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b44b5-127">Header</span></span><br/>  | <dl> <span data-ttu-id="b44b5-128"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="b44b5-128"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="b44b5-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b44b5-129">Library</span></span><br/> | <dl> <span data-ttu-id="b44b5-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b44b5-130"><dt>D3dx9.lib</dt></span></span> </dl>   |

## <a name="see-also"></a><span data-ttu-id="b44b5-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="b44b5-131">See also</span></span>

[<span data-ttu-id="b44b5-132">Funciones de transferencia Radiance precalculadas</span><span class="sxs-lookup"><span data-stu-id="b44b5-132">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
