---
description: Clona un objeto de información de máscara.
ms.assetid: 82d0a78a-95f3-4b09-bc1a-b4bc663e0850
title: 'ID3DXSkinInfo:: Clone (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.Clone
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: edd9776b75d027a32b32b58c59fc82daaebfa3ad
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280289"
---
# <a name="id3dxskininfoclone-method"></a><span data-ttu-id="b0130-103">ID3DXSkinInfo:: Clone (método)</span><span class="sxs-lookup"><span data-stu-id="b0130-103">ID3DXSkinInfo::Clone method</span></span>

<span data-ttu-id="b0130-104">Clona un objeto de información de máscara.</span><span class="sxs-lookup"><span data-stu-id="b0130-104">Clones a skin info object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0130-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b0130-105">Syntax</span></span>


```C++
HRESULT Clone(
  [in, out] LPD3DXSKININFO *ppSkinInfo
);
```



## <a name="parameters"></a><span data-ttu-id="b0130-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b0130-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0130-107">*ppSkinInfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b0130-107">*ppSkinInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0130-108">Tipo: **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***</span><span class="sxs-lookup"><span data-stu-id="b0130-108">Type: **[**LPD3DXSKININFO**](id3dxskininfo.md)\***</span></span>

<span data-ttu-id="b0130-109">Dirección de un puntero a un objeto [**ID3DXSkinInfo**](id3dxskininfo.md) , que contendrá el objeto clonado si el método se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="b0130-109">Address of a pointer to an [**ID3DXSkinInfo**](id3dxskininfo.md) object, which will contain the cloned object if the method is successful.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0130-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b0130-110">Return value</span></span>

<span data-ttu-id="b0130-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b0130-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b0130-112">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b0130-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b0130-113">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="b0130-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0130-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0130-114">Requirements</span></span>



| <span data-ttu-id="b0130-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0130-115">Requirement</span></span> | <span data-ttu-id="b0130-116">Value</span><span class="sxs-lookup"><span data-stu-id="b0130-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0130-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b0130-117">Header</span></span><br/>  | <dl> <span data-ttu-id="b0130-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0130-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="b0130-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b0130-119">Library</span></span><br/> | <dl> <span data-ttu-id="b0130-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b0130-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b0130-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="b0130-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0130-122">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="b0130-122">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 




