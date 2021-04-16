---
description: Una aplicación usa los métodos de esta interfaz para implementar un conjunto de animaciones de fotogramas clave almacenado en un formato de datos comprimido.
ms.assetid: 858f09b7-c3b6-4e22-8017-ce2d6188ba80
title: Interfaz ID3DXCompressedAnimationSet (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXCompressedAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 33dd1017859be14924d8d40265696cfb552754ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105678797"
---
# <a name="id3dxcompressedanimationset-interface"></a><span data-ttu-id="a6d35-103">Interfaz ID3DXCompressedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="a6d35-103">ID3DXCompressedAnimationSet interface</span></span>

<span data-ttu-id="a6d35-104">Una aplicación usa los métodos de esta interfaz para implementar un conjunto de animaciones de fotogramas clave almacenado en un formato de datos comprimido.</span><span class="sxs-lookup"><span data-stu-id="a6d35-104">An application uses the methods of this interface to implement a key frame animation set stored in a compressed data format.</span></span>

## <a name="members"></a><span data-ttu-id="a6d35-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="a6d35-105">Members</span></span>

<span data-ttu-id="a6d35-106">La interfaz **ID3DXCompressedAnimationSet** hereda de [**ID3DXAnimationSet**](id3dxanimationset.md).</span><span class="sxs-lookup"><span data-stu-id="a6d35-106">The **ID3DXCompressedAnimationSet** interface inherits from [**ID3DXAnimationSet**](id3dxanimationset.md).</span></span> <span data-ttu-id="a6d35-107">**ID3DXCompressedAnimationSet** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a6d35-107">**ID3DXCompressedAnimationSet** also has these types of members:</span></span>

-   [<span data-ttu-id="a6d35-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="a6d35-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a6d35-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="a6d35-109">Methods</span></span>

<span data-ttu-id="a6d35-110">La interfaz **ID3DXCompressedAnimationSet** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="a6d35-110">The **ID3DXCompressedAnimationSet** interface has these methods.</span></span>



| <span data-ttu-id="a6d35-111">Método</span><span class="sxs-lookup"><span data-stu-id="a6d35-111">Method</span></span>                                                                                  | <span data-ttu-id="a6d35-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="a6d35-112">Description</span></span>                                                                      |
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="a6d35-113">**GetCallbackKeys**</span><span class="sxs-lookup"><span data-stu-id="a6d35-113">**GetCallbackKeys**</span></span>](id3dxcompressedanimationset--getcallbackkeys.md)                 | <span data-ttu-id="a6d35-114">Rellena una matriz con los datos de clave de devolución de llamada utilizados para la animación de fotogramas clave.</span><span class="sxs-lookup"><span data-stu-id="a6d35-114">Fills an array with callback key data used for key frame animation.</span></span><br/>   |
| [<span data-ttu-id="a6d35-115">**GetCompressedData**</span><span class="sxs-lookup"><span data-stu-id="a6d35-115">**GetCompressedData**</span></span>](id3dxcompressedanimationset--getcompresseddata.md)             | <span data-ttu-id="a6d35-116">Obtiene el búfer de datos que almacena los datos de animación de fotogramas clave comprimidos.</span><span class="sxs-lookup"><span data-stu-id="a6d35-116">Gets the data buffer that stores compressed key frame animation data.</span></span><br/> |
| [<span data-ttu-id="a6d35-117">**GetNumCallbackKeys**</span><span class="sxs-lookup"><span data-stu-id="a6d35-117">**GetNumCallbackKeys**</span></span>](id3dxcompressedanimationset--getnumcallbackkeys.md)           | <span data-ttu-id="a6d35-118">Obtiene el número de claves de devolución de llamada del conjunto de animaciones.</span><span class="sxs-lookup"><span data-stu-id="a6d35-118">Gets the number of callback keys in the animation set.</span></span><br/>                |
| [<span data-ttu-id="a6d35-119">**GetPlaybackType**</span><span class="sxs-lookup"><span data-stu-id="a6d35-119">**GetPlaybackType**</span></span>](id3dxcompressedanimationset--getplaybacktype.md)                 | <span data-ttu-id="a6d35-120">Obtiene el tipo del bucle de reproducción establecido de la animación.</span><span class="sxs-lookup"><span data-stu-id="a6d35-120">Gets the type of the animation set playback loop.</span></span><br/>                     |
| [<span data-ttu-id="a6d35-121">**GetSourceTicksPerSecond**</span><span class="sxs-lookup"><span data-stu-id="a6d35-121">**GetSourceTicksPerSecond**</span></span>](id3dxcompressedanimationset--getsourcetickspersecond.md) | <span data-ttu-id="a6d35-122">Obtiene el número de TICs de fotogramas clave de animación que se producen por segundo.</span><span class="sxs-lookup"><span data-stu-id="a6d35-122">Gets the number of animation key frame ticks that occur per second.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="a6d35-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a6d35-123">Remarks</span></span>

<span data-ttu-id="a6d35-124">Cree un conjunto de animaciones de fotogramas clave con formato comprimido con [**D3DXCreateCompressedAnimationSet**](d3dxcreatecompressedanimationset.md).</span><span class="sxs-lookup"><span data-stu-id="a6d35-124">Create a compressed-format key frame animation set with [**D3DXCreateCompressedAnimationSet**](d3dxcreatecompressedanimationset.md).</span></span>

<span data-ttu-id="a6d35-125">El tipo LPD3DXCOMPRESSEDANIMATIONSET se define como un puntero a esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="a6d35-125">The LPD3DXCOMPRESSEDANIMATIONSET type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXCompressedAnimationSet ID3DXCompressedAnimationSet;
typedef interface ID3DXCompressedAnimationSet *LPD3DXCOMPRESSEDANIMATIONSET;
```



## <a name="requirements"></a><span data-ttu-id="a6d35-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6d35-126">Requirements</span></span>



| <span data-ttu-id="a6d35-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6d35-127">Requirement</span></span> | <span data-ttu-id="a6d35-128">Value</span><span class="sxs-lookup"><span data-stu-id="a6d35-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6d35-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a6d35-129">Header</span></span><br/>  | <dl> <span data-ttu-id="a6d35-130"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6d35-130"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="a6d35-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a6d35-131">Library</span></span><br/> | <dl> <span data-ttu-id="a6d35-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a6d35-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a6d35-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="a6d35-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6d35-134">**ID3DXAnimationSet**</span><span class="sxs-lookup"><span data-stu-id="a6d35-134">**ID3DXAnimationSet**</span></span>](id3dxanimationset.md)
</dt> <dt>

[<span data-ttu-id="a6d35-135">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="a6d35-135">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 




