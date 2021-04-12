---
description: Recupere el dispositivo asociado al objeto Sprite.
ms.assetid: 9119b232-22c8-4b05-b584-ce176370ca97
title: 'ID3DX10Sprite:: GetDevice (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.GetDevice
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d4e7a3c6ebfcbcb83aaaed6273ea321b33a44ce1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362822"
---
# <a name="id3dx10spritegetdevice-method"></a><span data-ttu-id="b8bb5-103">ID3DX10Sprite:: GetDevice (método)</span><span class="sxs-lookup"><span data-stu-id="b8bb5-103">ID3DX10Sprite::GetDevice method</span></span>

<span data-ttu-id="b8bb5-104">Recupere el dispositivo asociado al objeto Sprite.</span><span class="sxs-lookup"><span data-stu-id="b8bb5-104">Retrieve the device associated with the sprite object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8bb5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b8bb5-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out] ID3D10Device **ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="b8bb5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b8bb5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8bb5-107">*ppDevice* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b8bb5-107">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b8bb5-108">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span><span class="sxs-lookup"><span data-stu-id="b8bb5-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span></span>

<span data-ttu-id="b8bb5-109">Dirección de un puntero a una interfaz ID3D10Device que representa el objeto de dispositivo Direct3D asociado al objeto Sprite.</span><span class="sxs-lookup"><span data-stu-id="b8bb5-109">Address of a pointer to an ID3D10Device interface, representing the Direct3D device object associated with the sprite object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8bb5-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b8bb5-110">Return value</span></span>

<span data-ttu-id="b8bb5-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b8bb5-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b8bb5-112">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b8bb5-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="b8bb5-113">Si se produce un error en el método, se devolverá el valor siguiente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="b8bb5-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8bb5-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b8bb5-114">Remarks</span></span>

<span data-ttu-id="b8bb5-115">Al llamar a este método, se aumentará el recuento de referencias interno en la interfaz ID3D10Device.</span><span class="sxs-lookup"><span data-stu-id="b8bb5-115">Calling this method will increase the internal reference count on the ID3D10Device interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8bb5-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8bb5-116">Requirements</span></span>



| <span data-ttu-id="b8bb5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8bb5-117">Requirement</span></span> | <span data-ttu-id="b8bb5-118">Value</span><span class="sxs-lookup"><span data-stu-id="b8bb5-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b8bb5-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b8bb5-119">Header</span></span><br/>  | <dl> <span data-ttu-id="b8bb5-120"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8bb5-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="b8bb5-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b8bb5-121">Library</span></span><br/> | <dl> <span data-ttu-id="b8bb5-122"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b8bb5-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8bb5-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="b8bb5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8bb5-124">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="b8bb5-124">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="b8bb5-125">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="b8bb5-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




