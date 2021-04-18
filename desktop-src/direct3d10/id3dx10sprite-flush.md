---
description: 'Forzar el envío de todos los sprites por lotes al dispositivo. Los Estados de los dispositivos permanecen tal como estaban después de la última llamada a ID3DX10Sprite:: Begin. A continuación, se borra la lista de sprites por lotes.'
ms.assetid: ae03e17c-1a14-4a41-a9a9-8757d2f7a81d
title: 'ID3DX10Sprite:: Flush (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.Flush
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 748be56a7b89223db1957b9c0144143edd90ee4c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718560"
---
# <a name="id3dx10spriteflush-method"></a><span data-ttu-id="0b349-105">ID3DX10Sprite:: Flush (método)</span><span class="sxs-lookup"><span data-stu-id="0b349-105">ID3DX10Sprite::Flush method</span></span>

<span data-ttu-id="0b349-106">Forzar el envío de todos los sprites por lotes al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0b349-106">Force all batched sprites to be submitted to the device.</span></span> <span data-ttu-id="0b349-107">Los Estados de los dispositivos permanecen tal como estaban después de la última llamada a ID3DX10Sprite:: Begin.</span><span class="sxs-lookup"><span data-stu-id="0b349-107">Device states remain as they were after the last call to ID3DX10Sprite::Begin.</span></span> <span data-ttu-id="0b349-108">A continuación, se borra la lista de sprites por lotes.</span><span class="sxs-lookup"><span data-stu-id="0b349-108">The list of batched sprites is then cleared.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b349-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0b349-109">Syntax</span></span>


```C++
HRESULT Flush();
```



## <a name="parameters"></a><span data-ttu-id="0b349-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0b349-110">Parameters</span></span>

<span data-ttu-id="0b349-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="0b349-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0b349-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0b349-112">Return value</span></span>

<span data-ttu-id="0b349-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0b349-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0b349-114">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0b349-114">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="0b349-115">Si se produce un error en el método, se devolverá el valor siguiente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="0b349-115">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b349-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b349-116">Requirements</span></span>



| <span data-ttu-id="0b349-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b349-117">Requirement</span></span> | <span data-ttu-id="0b349-118">Value</span><span class="sxs-lookup"><span data-stu-id="0b349-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0b349-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0b349-119">Header</span></span><br/>  | <dl> <span data-ttu-id="0b349-120"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b349-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="0b349-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0b349-121">Library</span></span><br/> | <dl> <span data-ttu-id="0b349-122"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0b349-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b349-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b349-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b349-124">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="0b349-124">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="0b349-125">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="0b349-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




