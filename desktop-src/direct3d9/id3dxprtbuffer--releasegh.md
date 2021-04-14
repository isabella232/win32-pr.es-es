---
description: Desasocia un objeto ID3DXTextureGutterHelper asociado con el objeto ID3DXPRTBuffer.
ms.assetid: 0bd8322a-8af1-4173-bbe3-9134c831cf3a
title: 'ID3DXPRTBuffer:: ReleaseGH (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ReleaseGH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e9fb7a68f11d21065d6b4911b9ee7f58920aeb25
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424527"
---
# <a name="id3dxprtbufferreleasegh-method"></a><span data-ttu-id="75cdd-103">ID3DXPRTBuffer:: ReleaseGH (método)</span><span class="sxs-lookup"><span data-stu-id="75cdd-103">ID3DXPRTBuffer::ReleaseGH method</span></span>

<span data-ttu-id="75cdd-104">Desasocia un objeto [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) asociado con el objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="75cdd-104">Unassociates an attached [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object with the [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="75cdd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="75cdd-105">Syntax</span></span>


```C++
HRESULT ReleaseGH();
```



## <a name="parameters"></a><span data-ttu-id="75cdd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="75cdd-106">Parameters</span></span>

<span data-ttu-id="75cdd-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="75cdd-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="75cdd-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="75cdd-108">Return value</span></span>

<span data-ttu-id="75cdd-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="75cdd-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="75cdd-110">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="75cdd-110">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="75cdd-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="75cdd-111">Remarks</span></span>

<span data-ttu-id="75cdd-112">Este método libera el puntero a la interfaz [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) .</span><span class="sxs-lookup"><span data-stu-id="75cdd-112">This method releases the pointer to the [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) interface.</span></span>

<span data-ttu-id="75cdd-113">Debe asegurarse de que el número de llamadas a [**ID3DXPRTBuffer:: AttachGH**](id3dxprtbuffer--attachgh.md) coincide con el número de llamadas **ID3DXPRTBuffer:: ReleaseGH** .</span><span class="sxs-lookup"><span data-stu-id="75cdd-113">You must ensure that the number of [**ID3DXPRTBuffer::AttachGH**](id3dxprtbuffer--attachgh.md) calls matches the number of **ID3DXPRTBuffer::ReleaseGH** calls.</span></span> <span data-ttu-id="75cdd-114">Después de llamar a **ID3DXPRTBuffer:: ReleaseGH**, ya no se debe usar el puntero pGH devuelto por **ID3DXPRTBuffer:: AttachGH** .</span><span class="sxs-lookup"><span data-stu-id="75cdd-114">After calling **ID3DXPRTBuffer::ReleaseGH**, the pGH pointer returned by **ID3DXPRTBuffer::AttachGH** should no longer be used.</span></span>

## <a name="requirements"></a><span data-ttu-id="75cdd-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75cdd-115">Requirements</span></span>



| <span data-ttu-id="75cdd-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="75cdd-116">Requirement</span></span> | <span data-ttu-id="75cdd-117">Value</span><span class="sxs-lookup"><span data-stu-id="75cdd-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="75cdd-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="75cdd-118">Header</span></span><br/>  | <dl> <span data-ttu-id="75cdd-119"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="75cdd-119"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="75cdd-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="75cdd-120">Library</span></span><br/> | <dl> <span data-ttu-id="75cdd-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="75cdd-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="75cdd-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="75cdd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75cdd-123">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="75cdd-123">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> <dt>

[<span data-ttu-id="75cdd-124">**ID3DXPRTBuffer::AttachGH**</span><span class="sxs-lookup"><span data-stu-id="75cdd-124">**ID3DXPRTBuffer::AttachGH**</span></span>](id3dxprtbuffer--attachgh.md)
</dt> </dl>

 

 




