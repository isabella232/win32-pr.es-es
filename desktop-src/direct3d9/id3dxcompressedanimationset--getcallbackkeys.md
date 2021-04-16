---
description: Rellena una matriz con los datos de clave de devolución de llamada utilizados para la animación de fotogramas clave.
ms.assetid: 0dc30c1f-9ffb-42ec-8074-84293f16c344
title: 'ID3DXCompressedAnimationSet:: GetCallbackKeys (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXCompressedAnimationSet.GetCallbackKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fe56a3dbdd7d019deb5d7111fa592470bffd244d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105678802"
---
# <a name="id3dxcompressedanimationsetgetcallbackkeys-method"></a><span data-ttu-id="1fa27-103">ID3DXCompressedAnimationSet:: GetCallbackKeys (método)</span><span class="sxs-lookup"><span data-stu-id="1fa27-103">ID3DXCompressedAnimationSet::GetCallbackKeys method</span></span>

<span data-ttu-id="1fa27-104">Rellena una matriz con los datos de clave de devolución de llamada utilizados para la animación de fotogramas clave.</span><span class="sxs-lookup"><span data-stu-id="1fa27-104">Fills an array with callback key data used for key frame animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fa27-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1fa27-105">Syntax</span></span>


```C++
HRESULT GetCallbackKeys(
  [out] LPD3DXKEY_CALLBACK pCallbackKeys
);
```



## <a name="parameters"></a><span data-ttu-id="1fa27-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1fa27-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fa27-107">*pCallbackKeys* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1fa27-107">*pCallbackKeys* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1fa27-108">Tipo: **[ **\_ devolución de llamada LPD3DXKEY**](d3dxkey-callback.md)**</span><span class="sxs-lookup"><span data-stu-id="1fa27-108">Type: **[**LPD3DXKEY\_CALLBACK**](d3dxkey-callback.md)**</span></span>

<span data-ttu-id="1fa27-109">Puntero a una matriz asignada por el usuario de estructuras de [**\_ devolución de llamada de D3DXKEY**](d3dxkey-callback.md) que el método va a rellenar con los datos de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="1fa27-109">Pointer to a user-allocated array of [**D3DXKEY\_CALLBACK**](d3dxkey-callback.md) structures that the method is to fill with callback data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fa27-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1fa27-110">Return value</span></span>

<span data-ttu-id="1fa27-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1fa27-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1fa27-112">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1fa27-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="1fa27-113">Si se produce un error en el método, se devolverá el valor siguiente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="1fa27-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fa27-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fa27-114">Requirements</span></span>



| <span data-ttu-id="1fa27-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fa27-115">Requirement</span></span> | <span data-ttu-id="1fa27-116">Value</span><span class="sxs-lookup"><span data-stu-id="1fa27-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1fa27-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1fa27-117">Header</span></span><br/>  | <dl> <span data-ttu-id="1fa27-118"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="1fa27-118"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="1fa27-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1fa27-119">Library</span></span><br/> | <dl> <span data-ttu-id="1fa27-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1fa27-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1fa27-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="1fa27-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fa27-122">ID3DXCompressedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="1fa27-122">ID3DXCompressedAnimationSet</span></span>](id3dxcompressedanimationset.md)
</dt> <dt>

[<span data-ttu-id="1fa27-123">**ID3DXCompressedAnimationSet::GetNumCallbackKeys**</span><span class="sxs-lookup"><span data-stu-id="1fa27-123">**ID3DXCompressedAnimationSet::GetNumCallbackKeys**</span></span>](id3dxcompressedanimationset--getnumcallbackkeys.md)
</dt> </dl>

 

 




