---
title: Función CommandListCast (D3dx12. h)
description: Esta plantilla de función convierte un puntero constante en cualquier lista de comandos en un puntero const a un ID3D12CommandList.
ms.assetid: 63719AA1-2119-456C-9D23-13933D38AFA9
keywords:
- CommandListCast función)
topic_type:
- apiref
api_name:
- CommandListCast
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81a740258f74975fecac3e1a4df2412f1fae92f3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718447"
---
# <a name="commandlistcast-function"></a><span data-ttu-id="329da-104">CommandListCast función)</span><span class="sxs-lookup"><span data-stu-id="329da-104">CommandListCast function</span></span>

<span data-ttu-id="329da-105">Esta plantilla de función convierte un puntero constante en cualquier lista de comandos en un puntero const a un ID3D12CommandList.</span><span class="sxs-lookup"><span data-stu-id="329da-105">This function template casts a constant pointer to any command list into a const pointer to an ID3D12CommandList.</span></span>

<span data-ttu-id="329da-106">Esta conversión es útil para pasar punteros de lista de comandos fuertemente tipados a [**ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).</span><span class="sxs-lookup"><span data-stu-id="329da-106">This cast is useful for passing strongly-typed command list pointers into [**ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).</span></span>

## <a name="syntax"></a><span data-ttu-id="329da-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="329da-107">Syntax</span></span>


```C++
ID3D12CommandList * const * inline CommandListCast(
   t_CommandListType * const * pp
);
```



## <a name="parameters"></a><span data-ttu-id="329da-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="329da-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="329da-109">*páginas*</span><span class="sxs-lookup"><span data-stu-id="329da-109">*pp*</span></span> 
</dt> <dd>

<span data-ttu-id="329da-110">Tipo: **t \_ CommandListType \* const \***</span><span class="sxs-lookup"><span data-stu-id="329da-110">Type: **t\_CommandListType \* const \***</span></span>

<span data-ttu-id="329da-111">Lista de comandos fuertemente tipados que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="329da-111">The strongly-typed command list to cast.</span></span>

<span data-ttu-id="329da-112">El argumento de plantilla **t \_ CommandListType** especifica cualquier objeto de lista de comandos fuertemente tipado.</span><span class="sxs-lookup"><span data-stu-id="329da-112">The template argument **t\_CommandListType** specifies any strongly-typed command list object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="329da-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="329da-113">Return value</span></span>

<span data-ttu-id="329da-114">Tipo: **ID3D12CommandList \* const \***</span><span class="sxs-lookup"><span data-stu-id="329da-114">Type: **ID3D12CommandList \* const \***</span></span>

<span data-ttu-id="329da-115">La lista de comandos fuertemente tipados, reinterpretada como [**ID3D12CommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandlist).</span><span class="sxs-lookup"><span data-stu-id="329da-115">The strongly-typed command list, reinterpreted as an [**ID3D12CommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandlist).</span></span>

## <a name="remarks"></a><span data-ttu-id="329da-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="329da-116">Remarks</span></span>

<span data-ttu-id="329da-117">CommandListCast realiza una **\_ conversión de reinterpretación**.</span><span class="sxs-lookup"><span data-stu-id="329da-117">CommandListCast performs a **reinterpret\_cast**.</span></span> <span data-ttu-id="329da-118">La conversión es válida siempre y cuando se respete la constante de la lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="329da-118">The cast is valid as long as the const-ness of the command list is respected.</span></span>

<span data-ttu-id="329da-119">La función CommandListCast se define como la siguiente:</span><span class="sxs-lookup"><span data-stu-id="329da-119">The CommandListCast function is defined as the following:</span></span>


```C++
template <typename t_CommandListType>
inline ID3D12CommandList * const * CommandListCast(t_CommandListType * const * pp)
{
    return reinterpret_cast<ID3D12CommandList * const *>(pp);
}
          
```



## <a name="requirements"></a><span data-ttu-id="329da-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="329da-120">Requirements</span></span>



| <span data-ttu-id="329da-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="329da-121">Requirement</span></span> | <span data-ttu-id="329da-122">Value</span><span class="sxs-lookup"><span data-stu-id="329da-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="329da-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="329da-123">Header</span></span><br/>  | <dl> <span data-ttu-id="329da-124"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="329da-124"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="329da-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="329da-125">Library</span></span><br/> | <dl> <span data-ttu-id="329da-126"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="329da-126"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="329da-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="329da-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="329da-128"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="329da-128"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="329da-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="329da-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="329da-130">Funciones auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="329da-130">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





