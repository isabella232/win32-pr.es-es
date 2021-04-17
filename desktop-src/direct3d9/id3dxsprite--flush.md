---
description: 'Obliga a que todos los sprites por lotes se envíen al dispositivo. Los Estados de los dispositivos permanecen tal como estaban después de la última llamada a ID3DXSprite:: Begin. A continuación, se borra la lista de sprites por lotes.'
ms.assetid: e5717bde-e339-4344-8ce7-b0c3fe118887
title: 'ID3DXSprite:: Flush (método) (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.Flush
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3bcd89984672f0dcfa2df120ede1abdfee23d171
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718290"
---
# <a name="id3dxspriteflush-method"></a><span data-ttu-id="17251-105">ID3DXSprite:: Flush (método)</span><span class="sxs-lookup"><span data-stu-id="17251-105">ID3DXSprite::Flush method</span></span>

<span data-ttu-id="17251-106">Obliga a que todos los sprites por lotes se envíen al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="17251-106">Forces all batched sprites to be submitted to the device.</span></span> <span data-ttu-id="17251-107">Los Estados de los dispositivos permanecen tal como estaban después de la última llamada a [**ID3DXSprite:: Begin**](id3dxsprite--begin.md).</span><span class="sxs-lookup"><span data-stu-id="17251-107">Device states remain as they were after the last call to [**ID3DXSprite::Begin**](id3dxsprite--begin.md).</span></span> <span data-ttu-id="17251-108">A continuación, se borra la lista de sprites por lotes.</span><span class="sxs-lookup"><span data-stu-id="17251-108">The list of batched sprites is then cleared.</span></span>

## <a name="syntax"></a><span data-ttu-id="17251-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="17251-109">Syntax</span></span>


```C++
HRESULT Flush();
```



## <a name="parameters"></a><span data-ttu-id="17251-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="17251-110">Parameters</span></span>

<span data-ttu-id="17251-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="17251-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="17251-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="17251-112">Return value</span></span>

<span data-ttu-id="17251-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="17251-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="17251-114">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="17251-114">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="17251-115">Si se produce un error en el método, se devolverá el valor siguiente. D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="17251-115">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="17251-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17251-116">Requirements</span></span>



| <span data-ttu-id="17251-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="17251-117">Requirement</span></span> | <span data-ttu-id="17251-118">Value</span><span class="sxs-lookup"><span data-stu-id="17251-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="17251-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="17251-119">Header</span></span><br/>  | <dl> <span data-ttu-id="17251-120"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="17251-120"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="17251-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="17251-121">Library</span></span><br/> | <dl> <span data-ttu-id="17251-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="17251-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="17251-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="17251-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17251-124">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="17251-124">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> <dt>

[<span data-ttu-id="17251-125">**ID3DXSprite:: end**</span><span class="sxs-lookup"><span data-stu-id="17251-125">**ID3DXSprite::End**</span></span>](id3dxsprite--end.md)
</dt> </dl>

 

 




