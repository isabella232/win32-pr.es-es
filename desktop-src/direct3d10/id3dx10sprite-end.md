---
description: 'Llame a este método después de ID3DX10Sprite:: flush. Si \_ \_ \_ se especificó el estado de guardado de Sprite de D3DX10 cuando se llamó a ID3DX10Sprite:: Begin, esta API restaurará el estado del dispositivo al modo en que se encontraba antes de que se llamara a ID3DX10Sprite:: Begin.'
ms.assetid: 71645edb-be4a-4d87-9fb0-557cf5cf10e5
title: 'ID3DX10Sprite:: end (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.End
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 02d25e41916bd5d7605f3c0e1bc6e7998ea06e86
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718561"
---
# <a name="id3dx10spriteend-method"></a><span data-ttu-id="06f04-104">ID3DX10Sprite:: end (método)</span><span class="sxs-lookup"><span data-stu-id="06f04-104">ID3DX10Sprite::End method</span></span>

<span data-ttu-id="06f04-105">Llame a este método después de ID3DX10Sprite:: flush.</span><span class="sxs-lookup"><span data-stu-id="06f04-105">Call this after ID3DX10Sprite::Flush.</span></span> <span data-ttu-id="06f04-106">Si \_ \_ \_ se especificó el estado de guardado de Sprite de D3DX10 cuando se llamó a ID3DX10Sprite:: Begin, esta API restaurará el estado del dispositivo al modo en que se encontraba antes de que se llamara a ID3DX10Sprite:: Begin.</span><span class="sxs-lookup"><span data-stu-id="06f04-106">If D3DX10\_SPRITE\_SAVE\_STATE was specified when ID3DX10Sprite::Begin was called, this API will restore the device state to how it was before ID3DX10Sprite::Begin was called.</span></span>

## <a name="syntax"></a><span data-ttu-id="06f04-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="06f04-107">Syntax</span></span>


```C++
HRESULT End();
```



## <a name="parameters"></a><span data-ttu-id="06f04-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="06f04-108">Parameters</span></span>

<span data-ttu-id="06f04-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="06f04-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="06f04-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="06f04-110">Return value</span></span>

<span data-ttu-id="06f04-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="06f04-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="06f04-112">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="06f04-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="06f04-113">Si se produce un error en el método, se devolverá el valor siguiente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="06f04-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="06f04-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06f04-114">Requirements</span></span>



| <span data-ttu-id="06f04-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="06f04-115">Requirement</span></span> | <span data-ttu-id="06f04-116">Value</span><span class="sxs-lookup"><span data-stu-id="06f04-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="06f04-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="06f04-117">Header</span></span><br/>  | <dl> <span data-ttu-id="06f04-118"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="06f04-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="06f04-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="06f04-119">Library</span></span><br/> | <dl> <span data-ttu-id="06f04-120"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="06f04-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06f04-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="06f04-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06f04-122">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="06f04-122">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="06f04-123">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="06f04-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




