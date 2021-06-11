---
description: Obtenga información sobre la interfaz IAMFilterData, que convierte la información de filtro en datos binarios empaquetados. Esta interfaz está desusada.
ms.assetid: d9800850-b0ee-44f7-bcb4-f2bac8d17693
title: Interfaz IAMFilterData (Fil \_ data.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMFilterData
api_type:
- COM
api_location:
- fil_data.h
ms.openlocfilehash: 1e43e0f16ddfdee596f0dc6bd736ed86fc6fa37d
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989440"
---
# <a name="iamfilterdata-interface"></a><span data-ttu-id="4f3c9-104">Interfaz IAMFilterData</span><span class="sxs-lookup"><span data-stu-id="4f3c9-104">IAMFilterData interface</span></span>

> [!Note]  
> <span data-ttu-id="4f3c9-105">Esta interfaz está desusada.</span><span class="sxs-lookup"><span data-stu-id="4f3c9-105">This interface has been deprecated.</span></span> <span data-ttu-id="4f3c9-106">Las nuevas aplicaciones deben usar la [**interfaz IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="4f3c9-106">New applications should use the [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) interface instead.</span></span>

 

<span data-ttu-id="4f3c9-107">La `IAMFilterData` interfaz convierte la información de filtro en datos binarios empaquetados, que se pueden almacenar en el Registro.</span><span class="sxs-lookup"><span data-stu-id="4f3c9-107">The `IAMFilterData` interface converts filter information to packed binary data, which can be stored in the registry.</span></span> <span data-ttu-id="4f3c9-108">El objeto Filter Mapper expone esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="4f3c9-108">The Filter Mapper object exposes this interface.</span></span>

## <a name="members"></a><span data-ttu-id="4f3c9-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="4f3c9-109">Members</span></span>

<span data-ttu-id="4f3c9-110">La **interfaz IAMFilterData** hereda de [**la interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown)</span><span class="sxs-lookup"><span data-stu-id="4f3c9-110">The **IAMFilterData** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4f3c9-111">**IAMFilterData** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4f3c9-111">**IAMFilterData** also has these types of members:</span></span>

-   [<span data-ttu-id="4f3c9-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="4f3c9-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4f3c9-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="4f3c9-113">Methods</span></span>

<span data-ttu-id="4f3c9-114">La **interfaz IAMFilterData** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="4f3c9-114">The **IAMFilterData** interface has these methods.</span></span>



| <span data-ttu-id="4f3c9-115">Método</span><span class="sxs-lookup"><span data-stu-id="4f3c9-115">Method</span></span>                                                     | <span data-ttu-id="4f3c9-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="4f3c9-116">Description</span></span>                                               |
|:-----------------------------------------------------------|:----------------------------------------------------------|
| [<span data-ttu-id="4f3c9-117">**CreateFilterData**</span><span class="sxs-lookup"><span data-stu-id="4f3c9-117">**CreateFilterData**</span></span>](iamfilterdata-createfilterdata.md) | <span data-ttu-id="4f3c9-118">Crea datos binarios del Registro para un filtro.</span><span class="sxs-lookup"><span data-stu-id="4f3c9-118">Creates binary registry data for a filter.</span></span><br/>     |
| [<span data-ttu-id="4f3c9-119">**ParseFilterData**</span><span class="sxs-lookup"><span data-stu-id="4f3c9-119">**ParseFilterData**</span></span>](iamfilterdata-parsefilterdata.md)   | <span data-ttu-id="4f3c9-120">Desempaquete los datos binarios del Registro para un filtro.</span><span class="sxs-lookup"><span data-stu-id="4f3c9-120">Unpacks the binary registry data for a filter.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4f3c9-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4f3c9-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4f3c9-122">El encabezado Fil \_ data.h se encuentra en el directorio [Mapper Sample](mapper-sample.md) del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="4f3c9-122">The header Fil\_data.h is located in the [Mapper Sample](mapper-sample.md) directory in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4f3c9-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f3c9-123">Requirements</span></span>



| <span data-ttu-id="4f3c9-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f3c9-124">Requirement</span></span> | <span data-ttu-id="4f3c9-125">Value</span><span class="sxs-lookup"><span data-stu-id="4f3c9-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f3c9-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4f3c9-126">Header</span></span><br/> | <dl> <span data-ttu-id="4f3c9-127"><dt>Fil \_ data.h</dt></span><span class="sxs-lookup"><span data-stu-id="4f3c9-127"><dt>Fil\_data.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f3c9-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="4f3c9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f3c9-129">Interfaces en desuso</span><span class="sxs-lookup"><span data-stu-id="4f3c9-129">Deprecated Interfaces</span></span>](deprecated-interfaces.md)
</dt> </dl>

 

 
