---
description: 'Método ID3DXKeyframedAnimationSet::GetCallbackKeys: rellena una matriz con datos de clave de devolución de llamada usados para la animación de fotogramas clave.'
ms.assetid: 2a2aa04a-a889-415b-8aa2-cc5f2bed1f9a
title: Método ID3DXKeyframedAnimationSet::GetCallbackKeys (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetCallbackKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5f3bdb7049de3b5d6aad10b5ff5100d01d05e3ee
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093723"
---
# <a name="id3dxkeyframedanimationsetgetcallbackkeys-method"></a><span data-ttu-id="230b8-103">Método ID3DXKeyframedAnimationSet::GetCallbackKeys</span><span class="sxs-lookup"><span data-stu-id="230b8-103">ID3DXKeyframedAnimationSet::GetCallbackKeys method</span></span>

<span data-ttu-id="230b8-104">Rellena una matriz con datos de clave de devolución de llamada usados para la animación de fotogramas clave.</span><span class="sxs-lookup"><span data-stu-id="230b8-104">Fills an array with callback key data used for key frame animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="230b8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="230b8-105">Syntax</span></span>


```C++
HRESULT GetCallbackKeys(
  [out] LPD3DXKEY_CALLBACK pCallbackKeys
);
```



## <a name="parameters"></a><span data-ttu-id="230b8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="230b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="230b8-107">*pCallbackKeys* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="230b8-107">*pCallbackKeys* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="230b8-108">Tipo: **[ **LPD3DXKEY \_ CALLBACK**](d3dxkey-callback.md)**</span><span class="sxs-lookup"><span data-stu-id="230b8-108">Type: **[**LPD3DXKEY\_CALLBACK**](d3dxkey-callback.md)**</span></span>

<span data-ttu-id="230b8-109">Puntero a una matriz asignada por el usuario de estructuras [**D3DXKEY \_ CALLBACK**](d3dxkey-callback.md) que el método va a rellenar con datos de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="230b8-109">Pointer to a user-allocated array of [**D3DXKEY\_CALLBACK**](d3dxkey-callback.md) structures that the method is to fill with callback data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="230b8-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="230b8-110">Return value</span></span>

<span data-ttu-id="230b8-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="230b8-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="230b8-112">Si el método se realiza correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="230b8-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="230b8-113">Si se produce un error en el método, se devolverá el siguiente valor: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="230b8-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="230b8-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="230b8-114">Requirements</span></span>



| <span data-ttu-id="230b8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="230b8-115">Requirement</span></span> | <span data-ttu-id="230b8-116">Value</span><span class="sxs-lookup"><span data-stu-id="230b8-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="230b8-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="230b8-117">Header</span></span><br/>  | <dl> <span data-ttu-id="230b8-118"><dt>D3dx9anim.h</dt></span><span class="sxs-lookup"><span data-stu-id="230b8-118"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="230b8-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="230b8-119">Library</span></span><br/> | <dl> <span data-ttu-id="230b8-120"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="230b8-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="230b8-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="230b8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="230b8-122">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="230b8-122">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> <dt>

[<span data-ttu-id="230b8-123">**ID3DXKeyframedAnimationSet::GetNumCallbackKeys**</span><span class="sxs-lookup"><span data-stu-id="230b8-123">**ID3DXKeyframedAnimationSet::GetNumCallbackKeys**</span></span>](id3dxkeyframedanimationset--getnumcallbackkeys.md)
</dt> </dl>

 

 




