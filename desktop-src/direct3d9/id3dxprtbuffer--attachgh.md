---
description: Asocia un objeto ID3DXTextureGutterHelper al objeto ID3DXPRTBuffer.
ms.assetid: 095fea82-ac7a-42fa-990a-084715c73823
title: 'ID3DXPRTBuffer:: AttachGH (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.AttachGH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1ba5afa238107d60620291b50b8f184eb4e5d361
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707964"
---
# <a name="id3dxprtbufferattachgh-method"></a><span data-ttu-id="629f8-103">ID3DXPRTBuffer:: AttachGH (método)</span><span class="sxs-lookup"><span data-stu-id="629f8-103">ID3DXPRTBuffer::AttachGH method</span></span>

<span data-ttu-id="629f8-104">Asocia un objeto [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) al objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="629f8-104">Associates an [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object with the [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="629f8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="629f8-105">Syntax</span></span>


```C++
HRESULT AttachGH(
  [in] LPD3DXTEXTUREGUTTERHELPER pGH
);
```



## <a name="parameters"></a><span data-ttu-id="629f8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="629f8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="629f8-107">*pGH* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="629f8-107">*pGH* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="629f8-108">Tipo: **[ **LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)**</span><span class="sxs-lookup"><span data-stu-id="629f8-108">Type: **[**LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)**</span></span>

<span data-ttu-id="629f8-109">Puntero a la interfaz [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) de un objeto que contiene los datos de medianil de textura.</span><span class="sxs-lookup"><span data-stu-id="629f8-109">Pointer to the [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) interface of an object that contains texture gutter data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="629f8-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="629f8-110">Return value</span></span>

<span data-ttu-id="629f8-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="629f8-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="629f8-112">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="629f8-112">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="629f8-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="629f8-113">Remarks</span></span>

<span data-ttu-id="629f8-114">El recuento de referencias del objeto [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) se incrementará automáticamente en uno.</span><span class="sxs-lookup"><span data-stu-id="629f8-114">The reference count of the [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object will automatically be incremented by one.</span></span> <span data-ttu-id="629f8-115">Se liberarán todos los punteros de **ID3DXTextureGutterHelper** existentes.</span><span class="sxs-lookup"><span data-stu-id="629f8-115">Any existing **ID3DXTextureGutterHelper** pointers will be released.</span></span>

<span data-ttu-id="629f8-116">Debe asegurarse de que el número de llamadas a **ID3DXPRTBuffer:: AttachGH** coincide con el número de llamadas [**ID3DXPRTBuffer:: ReleaseGH**](id3dxprtbuffer--releasegh.md) .</span><span class="sxs-lookup"><span data-stu-id="629f8-116">You must ensure that the number of **ID3DXPRTBuffer::AttachGH** calls matches the number of [**ID3DXPRTBuffer::ReleaseGH**](id3dxprtbuffer--releasegh.md) calls.</span></span> <span data-ttu-id="629f8-117">Después de llamar a **ID3DXPRTBuffer:: ReleaseGH**, ya no se debe usar el puntero pGH devuelto por **ID3DXPRTBuffer:: AttachGH** .</span><span class="sxs-lookup"><span data-stu-id="629f8-117">After calling **ID3DXPRTBuffer::ReleaseGH**, the pGH pointer returned by **ID3DXPRTBuffer::AttachGH** should no longer be used.</span></span>

## <a name="requirements"></a><span data-ttu-id="629f8-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="629f8-118">Requirements</span></span>



| <span data-ttu-id="629f8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="629f8-119">Requirement</span></span> | <span data-ttu-id="629f8-120">Value</span><span class="sxs-lookup"><span data-stu-id="629f8-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="629f8-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="629f8-121">Header</span></span><br/>  | <dl> <span data-ttu-id="629f8-122"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="629f8-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="629f8-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="629f8-123">Library</span></span><br/> | <dl> <span data-ttu-id="629f8-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="629f8-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="629f8-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="629f8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="629f8-126">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="629f8-126">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> <dt>

[<span data-ttu-id="629f8-127">**ID3DXPRTBuffer::ReleaseGH**</span><span class="sxs-lookup"><span data-stu-id="629f8-127">**ID3DXPRTBuffer::ReleaseGH**</span></span>](id3dxprtbuffer--releasegh.md)
</dt> </dl>

 

 




