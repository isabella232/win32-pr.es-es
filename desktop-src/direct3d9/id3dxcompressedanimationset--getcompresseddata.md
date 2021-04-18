---
description: Obtiene el búfer de datos que almacena los datos de animación de fotogramas clave comprimidos.
ms.assetid: cb42a4c8-6420-4694-9921-0d36cfe960e5
title: 'ID3DXCompressedAnimationSet:: GetCompressedData (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXCompressedAnimationSet.GetCompressedData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7907daf5db2d03afca310a630f6aeb2dc16c4f22
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105678800"
---
# <a name="id3dxcompressedanimationsetgetcompresseddata-method"></a><span data-ttu-id="659d9-103">ID3DXCompressedAnimationSet:: GetCompressedData (método)</span><span class="sxs-lookup"><span data-stu-id="659d9-103">ID3DXCompressedAnimationSet::GetCompressedData method</span></span>

<span data-ttu-id="659d9-104">Obtiene el búfer de datos que almacena los datos de animación de fotogramas clave comprimidos.</span><span class="sxs-lookup"><span data-stu-id="659d9-104">Gets the data buffer that stores compressed key frame animation data.</span></span>

## <a name="syntax"></a><span data-ttu-id="659d9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="659d9-105">Syntax</span></span>


```C++
HRESULT GetCompressedData(
  [out] LPD3DXBUFFER *ppCompressedData
);
```



## <a name="parameters"></a><span data-ttu-id="659d9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="659d9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="659d9-107">*ppCompressedData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="659d9-107">*ppCompressedData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="659d9-108">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="659d9-108">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="659d9-109">Dirección de un puntero al búfer de datos [**ID3DXBuffer**](id3dxbuffer.md) que recibe los datos de animación de fotogramas clave comprimidos.</span><span class="sxs-lookup"><span data-stu-id="659d9-109">Address of a pointer to the [**ID3DXBuffer**](id3dxbuffer.md) data buffer that receives compressed key frame animation data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="659d9-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="659d9-110">Return value</span></span>

<span data-ttu-id="659d9-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="659d9-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="659d9-112">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="659d9-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="659d9-113">Si se produce un error en el método, se devolverá el valor siguiente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="659d9-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="659d9-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="659d9-114">Requirements</span></span>



| <span data-ttu-id="659d9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="659d9-115">Requirement</span></span> | <span data-ttu-id="659d9-116">Value</span><span class="sxs-lookup"><span data-stu-id="659d9-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="659d9-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="659d9-117">Header</span></span><br/>  | <dl> <span data-ttu-id="659d9-118"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="659d9-118"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="659d9-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="659d9-119">Library</span></span><br/> | <dl> <span data-ttu-id="659d9-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="659d9-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="659d9-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="659d9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="659d9-122">ID3DXCompressedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="659d9-122">ID3DXCompressedAnimationSet</span></span>](id3dxcompressedanimationset.md)
</dt> </dl>

 

 




