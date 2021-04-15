---
description: Agrega otro búfer a ID3DXPRTBuffer y almacena los resultados en ID3DXPRTBuffer.
ms.assetid: 345412f4-30c5-4c1d-b0ef-6e3e18c4e5ab
title: 'ID3DXPRTBuffer:: AddBuffer (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.AddBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 90b86ad3d5d9fe5aa65db722757bdb34574a1006
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708119"
---
# <a name="id3dxprtbufferaddbuffer-method"></a><span data-ttu-id="69bd6-103">ID3DXPRTBuffer:: AddBuffer (método)</span><span class="sxs-lookup"><span data-stu-id="69bd6-103">ID3DXPRTBuffer::AddBuffer method</span></span>

<span data-ttu-id="69bd6-104">Agrega otro búfer a [**ID3DXPRTBuffer**](id3dxprtbuffer.md) y almacena los resultados en **ID3DXPRTBuffer**.</span><span class="sxs-lookup"><span data-stu-id="69bd6-104">Adds another buffer to the [**ID3DXPRTBuffer**](id3dxprtbuffer.md) and stores the results in **ID3DXPRTBuffer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="69bd6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="69bd6-105">Syntax</span></span>


```C++
HRESULT AddBuffer(
  [in] LPD3DXPRTBUFFER pBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="69bd6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="69bd6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69bd6-107">*pBuffer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="69bd6-107">*pBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69bd6-108">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="69bd6-108">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="69bd6-109">Puntero a un búfer que contiene los miembros que se van a agregar a los miembros respectivos del búfer [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="69bd6-109">Pointer to a buffer that contains members to be added to the respective members of the [**ID3DXPRTBuffer**](id3dxprtbuffer.md) buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69bd6-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="69bd6-110">Return value</span></span>

<span data-ttu-id="69bd6-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="69bd6-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="69bd6-112">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="69bd6-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="69bd6-113">Si se produce un error en el método, se devolverá el valor siguiente.</span><span class="sxs-lookup"><span data-stu-id="69bd6-113">If the method fails, the following value will be returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="69bd6-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="69bd6-114">Remarks</span></span>

<span data-ttu-id="69bd6-115">pBuffer y [**ID3DXPRTBuffer**](id3dxprtbuffer.md) deben tener el mismo número de muestras, coeficientes y canales de color; de lo contrario, se producirá un error en el método.</span><span class="sxs-lookup"><span data-stu-id="69bd6-115">pBuffer and [**ID3DXPRTBuffer**](id3dxprtbuffer.md) must have the same number of samples, coefficients, and color channels; the method will fail otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="69bd6-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69bd6-116">Requirements</span></span>



| <span data-ttu-id="69bd6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="69bd6-117">Requirement</span></span> | <span data-ttu-id="69bd6-118">Value</span><span class="sxs-lookup"><span data-stu-id="69bd6-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="69bd6-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="69bd6-119">Header</span></span><br/>  | <dl> <span data-ttu-id="69bd6-120"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="69bd6-120"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="69bd6-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="69bd6-121">Library</span></span><br/> | <dl> <span data-ttu-id="69bd6-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="69bd6-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="69bd6-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="69bd6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69bd6-124">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="69bd6-124">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> </dl>

 

 




