---
description: Extrae los identificadores de clúster por ejemplo de un búfer de datos comprimidos de ID3DXPRTCompBuffer.
ms.assetid: d78d82ab-58bc-4b73-9ca0-8b7f06867618
title: 'ID3DXPRTCompBuffer:: ExtractClusterIDs (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractClusterIDs
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ef68a972109e89e318adb83ab388c653c6a3deed
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718553"
---
# <a name="id3dxprtcompbufferextractclusterids-method"></a><span data-ttu-id="6beab-103">ID3DXPRTCompBuffer:: ExtractClusterIDs (método)</span><span class="sxs-lookup"><span data-stu-id="6beab-103">ID3DXPRTCompBuffer::ExtractClusterIDs method</span></span>

<span data-ttu-id="6beab-104">Extrae los identificadores de clúster por ejemplo de un búfer de datos comprimidos de [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="6beab-104">Extracts the per-sample cluster IDs from an [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) compressed data buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="6beab-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6beab-105">Syntax</span></span>


```C++
HRESULT ExtractClusterIDs(
  [in, out] UINT *pClusterIDs
);
```



## <a name="parameters"></a><span data-ttu-id="6beab-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6beab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6beab-107">*pClusterIDs* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6beab-107">*pClusterIDs* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6beab-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="6beab-108">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6beab-109">Puntero a la ubicación en memoria donde se escriben los identificadores.</span><span class="sxs-lookup"><span data-stu-id="6beab-109">Pointer to the location in memory where IDs are written.</span></span> <span data-ttu-id="6beab-110">La longitud de memoria necesaria es el valor devuelto por [**ID3DXPRTCompBuffer:: GetNumSamples**](id3dxprtcompbuffer--getnumsamples.md).</span><span class="sxs-lookup"><span data-stu-id="6beab-110">The length of memory required is the value returned by [**ID3DXPRTCompBuffer::GetNumSamples**](id3dxprtcompbuffer--getnumsamples.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6beab-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6beab-111">Return value</span></span>

<span data-ttu-id="6beab-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6beab-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6beab-113">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6beab-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="6beab-114">Si se produce un error en el método, se devolverá el valor siguiente.</span><span class="sxs-lookup"><span data-stu-id="6beab-114">If the method fails, the following value will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="6beab-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6beab-115">Requirements</span></span>



| <span data-ttu-id="6beab-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6beab-116">Requirement</span></span> | <span data-ttu-id="6beab-117">Value</span><span class="sxs-lookup"><span data-stu-id="6beab-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6beab-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6beab-118">Header</span></span><br/>  | <dl> <span data-ttu-id="6beab-119"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="6beab-119"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="6beab-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6beab-120">Library</span></span><br/> | <dl> <span data-ttu-id="6beab-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6beab-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6beab-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="6beab-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6beab-123">ID3DXPRTCompBuffer</span><span class="sxs-lookup"><span data-stu-id="6beab-123">ID3DXPRTCompBuffer</span></span>](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
