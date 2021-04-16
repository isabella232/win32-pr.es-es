---
title: CD3DX12_DEFAULT estructura (D3dx12. h)
description: Pasa \_ el valor predeterminado de D3D12 en un constructor para cada estructura de aplicación auxiliar. Esta estructura simplemente se usa como mecanismo para establecer los parámetros predeterminados en las otras estructuras auxiliares.
ms.assetid: AD41FD7B-9172-400E-9292-374FFAEDE145
keywords:
- Estructura de CD3DX12_DEFAULT
topic_type:
- apiref
api_name:
- CD3DX12_DEFAULT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b010e8f0fdce67f16750d0f66d1cf272c8ddb849
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649387"
---
# <a name="cd3dx12_default-structure"></a><span data-ttu-id="7e245-105">\_Estructura predeterminada de CD3DX12</span><span class="sxs-lookup"><span data-stu-id="7e245-105">CD3DX12\_DEFAULT structure</span></span>

<span data-ttu-id="7e245-106">Pasa \_ el valor predeterminado de D3D12 en un constructor para cada estructura de aplicación auxiliar.</span><span class="sxs-lookup"><span data-stu-id="7e245-106">Passes D3D12\_DEFAULT into a constructor for each helper structure.</span></span> <span data-ttu-id="7e245-107">Esta estructura simplemente se usa como mecanismo para establecer los parámetros predeterminados en las otras estructuras auxiliares.</span><span class="sxs-lookup"><span data-stu-id="7e245-107">This structure is simply used as a mechanism to set default parameters on the other helper structures.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e245-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7e245-108">Remarks</span></span>

<span data-ttu-id="7e245-109">Este struct se declara de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="7e245-109">This struct is declared as follows:</span></span>

``` syntax
struct CD3DX12_DEFAULT {};
extern const DECLSPEC_SELECTANY CD3DX12_DEFAULT D3D12_DEFAULT;
```

<span data-ttu-id="7e245-110">Pasa \_ el valor predeterminado de D3D12 en un constructor para cada struct de la aplicación auxiliar.</span><span class="sxs-lookup"><span data-stu-id="7e245-110">Passes D3D12\_DEFAULT into a constructor for each helper struct.</span></span> <span data-ttu-id="7e245-111">Por ejemplo, el siguiente constructor se declara en d3dx12. h:</span><span class="sxs-lookup"><span data-stu-id="7e245-111">For example, the following constructor is declared in d3dx12.h:</span></span>

<span data-ttu-id="7e245-112">\_Identificador de \_ descriptor de CPU de CD3DX12 \_ ( \_ valor predeterminado de CD3DX12) {PTR = 0;}</span><span class="sxs-lookup"><span data-stu-id="7e245-112">CD3DX12\_CPU\_DESCRIPTOR\_HANDLE(CD3DX12\_DEFAULT) { ptr = 0; }</span></span>

## <a name="requirements"></a><span data-ttu-id="7e245-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e245-113">Requirements</span></span>



| <span data-ttu-id="7e245-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e245-114">Requirement</span></span> | <span data-ttu-id="7e245-115">Value</span><span class="sxs-lookup"><span data-stu-id="7e245-115">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7e245-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7e245-116">Header</span></span><br/> | <dl> <span data-ttu-id="7e245-117"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e245-117"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e245-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="7e245-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e245-119">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="7e245-119">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





