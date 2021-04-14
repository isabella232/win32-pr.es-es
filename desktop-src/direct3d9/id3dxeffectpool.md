---
description: Las aplicaciones usan la interfaz ID3DXEffectPool para identificar los parámetros que se van a compartir entre los efectos. Consulte uso compartido de parámetros en la clonación y el uso compartido (Direct3D 9). Esta interfaz no tiene métodos.
ms.assetid: dd5e55eb-9436-422d-9743-38be44d05962
title: Interfaz ID3DXEffectPool (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectPool
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 893116d7e99bd720f098a8b536f1ad4fd02563ab
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424339"
---
# <a name="id3dxeffectpool-interface"></a><span data-ttu-id="d7a9c-105">Interfaz ID3DXEffectPool</span><span class="sxs-lookup"><span data-stu-id="d7a9c-105">ID3DXEffectPool interface</span></span>

<span data-ttu-id="d7a9c-106">Las aplicaciones usan la interfaz **ID3DXEffectPool** para identificar los parámetros que se van a compartir entre los efectos.</span><span class="sxs-lookup"><span data-stu-id="d7a9c-106">Applications use the **ID3DXEffectPool** interface to identify parameters that are going to be shared across effects.</span></span> <span data-ttu-id="d7a9c-107">Consulte uso compartido de parámetros en la [clonación y el uso compartido (Direct3D 9)](cloning-and-sharing.md).</span><span class="sxs-lookup"><span data-stu-id="d7a9c-107">See parameter sharing in [Cloning and Sharing (Direct3D 9)](cloning-and-sharing.md).</span></span> <span data-ttu-id="d7a9c-108">Esta interfaz no tiene métodos.</span><span class="sxs-lookup"><span data-stu-id="d7a9c-108">This interface has no methods.</span></span>

## <a name="members"></a><span data-ttu-id="d7a9c-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="d7a9c-109">Members</span></span>

<span data-ttu-id="d7a9c-110">La interfaz **ID3DXEffectPool** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) , pero no tiene miembros adicionales.</span><span class="sxs-lookup"><span data-stu-id="d7a9c-110">The **ID3DXEffectPool** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7a9c-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d7a9c-111">Remarks</span></span>

<span data-ttu-id="d7a9c-112">La interfaz ID3DXEffectPool se obtiene llamando a [**D3DXCreateEffectPool**](d3dxcreateeffectpool.md).</span><span class="sxs-lookup"><span data-stu-id="d7a9c-112">The ID3DXEffectPool interface is obtained by calling [**D3DXCreateEffectPool**](d3dxcreateeffectpool.md).</span></span>

<span data-ttu-id="d7a9c-113">El tipo LPD3DXEFFECTPOOL se define como un puntero a esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="d7a9c-113">The LPD3DXEFFECTPOOL type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXEffectPool ID3DXEffectPool;
typedef interface ID3DXEffectPool *LPD3DXEFFECTPOOL;
```



## <a name="requirements"></a><span data-ttu-id="d7a9c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7a9c-114">Requirements</span></span>



| <span data-ttu-id="d7a9c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7a9c-115">Requirement</span></span> | <span data-ttu-id="d7a9c-116">Value</span><span class="sxs-lookup"><span data-stu-id="d7a9c-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7a9c-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d7a9c-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d7a9c-118"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7a9c-118"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="d7a9c-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d7a9c-119">Library</span></span><br/> | <dl> <span data-ttu-id="d7a9c-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d7a9c-120"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d7a9c-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7a9c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7a9c-122">Interfaces de efectos</span><span class="sxs-lookup"><span data-stu-id="d7a9c-122">Effect Interfaces</span></span>](dx9-graphics-reference-effects-interfaces.md)
</dt> </dl>

 

 
