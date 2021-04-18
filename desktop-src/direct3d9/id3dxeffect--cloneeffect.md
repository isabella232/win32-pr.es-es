---
description: Crea una copia de un efecto.
ms.assetid: 6272bce0-b712-4a61-afe2-8f572993b03e
title: 'ID3DXEffect:: CloneEffect (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.CloneEffect
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: eba2f6248bd1373ebf0aae55cf94103e2c269be7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718240"
---
# <a name="id3dxeffectcloneeffect-method"></a><span data-ttu-id="2250a-103">ID3DXEffect:: CloneEffect (método)</span><span class="sxs-lookup"><span data-stu-id="2250a-103">ID3DXEffect::CloneEffect method</span></span>

<span data-ttu-id="2250a-104">Crea una copia de un efecto.</span><span class="sxs-lookup"><span data-stu-id="2250a-104">Creates a copy of an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="2250a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2250a-105">Syntax</span></span>


```C++
HRESULT CloneEffect(
  [in]  LPDIRECT3DDEVICE9 pDevice,
  [out] LPD3DXEFFECT      *ppEffect
);
```



## <a name="parameters"></a><span data-ttu-id="2250a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2250a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2250a-107">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2250a-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2250a-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="2250a-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="2250a-109">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo asociado al efecto.</span><span class="sxs-lookup"><span data-stu-id="2250a-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the effect.</span></span>

</dd> <dt>

<span data-ttu-id="2250a-110">*ppEffect* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2250a-110">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2250a-111">Tipo: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="2250a-111">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="2250a-112">Puntero a una interfaz [**ID3DXEffect**](id3dxeffect.md) que contiene el efecto clonado.</span><span class="sxs-lookup"><span data-stu-id="2250a-112">Pointer to an [**ID3DXEffect**](id3dxeffect.md) interface, containing the cloned effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2250a-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2250a-113">Return value</span></span>

<span data-ttu-id="2250a-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2250a-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2250a-115">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2250a-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="2250a-116">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="2250a-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="2250a-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2250a-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2250a-118">Esta función no clonará ningún efecto si el usuario especifica que [D3DXFX no se podrá \_ \_ clonar](d3dxfx.md) durante la creación del efecto.</span><span class="sxs-lookup"><span data-stu-id="2250a-118">This function will not clone an effect if the user specifies [D3DXFX\_NOT\_CLONEABLE](d3dxfx.md) during effect creation.</span></span>

 

<span data-ttu-id="2250a-119">Para actualizar los parámetros compartidos y no compartidos en una técnica activa de un efecto clonado, vea [**ID3DXEffect:: commitChanges**](id3dxeffect--commitchanges.md).</span><span class="sxs-lookup"><span data-stu-id="2250a-119">To update shared and non-shared parameters in an active technique of a cloned effect, see [**ID3DXEffect::CommitChanges**](id3dxeffect--commitchanges.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2250a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2250a-120">Requirements</span></span>



| <span data-ttu-id="2250a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="2250a-121">Requirement</span></span> | <span data-ttu-id="2250a-122">Value</span><span class="sxs-lookup"><span data-stu-id="2250a-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2250a-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2250a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="2250a-124"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="2250a-124"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="2250a-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2250a-125">Library</span></span><br/> | <dl> <span data-ttu-id="2250a-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2250a-126"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2250a-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="2250a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2250a-128">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="2250a-128">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 
