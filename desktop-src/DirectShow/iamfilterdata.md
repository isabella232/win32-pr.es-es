---
description: 'Nota: esta interfaz está en desuso.'
ms.assetid: d9800850-b0ee-44f7-bcb4-f2bac8d17693
title: Interfaz IAMFilterData (Fil \_ Data. h)
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
ms.openlocfilehash: 1ab5ea8e9c90c043c33cca4d9f8138dd7d9937ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679392"
---
# <a name="iamfilterdata-interface"></a><span data-ttu-id="b7ac1-103">Interfaz IAMFilterData</span><span class="sxs-lookup"><span data-stu-id="b7ac1-103">IAMFilterData interface</span></span>

> [!Note]  
> <span data-ttu-id="b7ac1-104">Esta interfaz está desusada.</span><span class="sxs-lookup"><span data-stu-id="b7ac1-104">This interface has been deprecated.</span></span> <span data-ttu-id="b7ac1-105">En su lugar, las nuevas aplicaciones deben usar la interfaz [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) .</span><span class="sxs-lookup"><span data-stu-id="b7ac1-105">New applications should use the [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) interface instead.</span></span>

 

<span data-ttu-id="b7ac1-106">La `IAMFilterData` interfaz convierte información de filtro en datos binarios empaquetados, que se pueden almacenar en el registro.</span><span class="sxs-lookup"><span data-stu-id="b7ac1-106">The `IAMFilterData` interface converts filter information to packed binary data, which can be stored in the registry.</span></span> <span data-ttu-id="b7ac1-107">El objeto de asignador de filtros expone esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="b7ac1-107">The Filter Mapper object exposes this interface.</span></span>

## <a name="members"></a><span data-ttu-id="b7ac1-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="b7ac1-108">Members</span></span>

<span data-ttu-id="b7ac1-109">La interfaz **IAMFilterData** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="b7ac1-109">The **IAMFilterData** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b7ac1-110">**IAMFilterData** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b7ac1-110">**IAMFilterData** also has these types of members:</span></span>

-   [<span data-ttu-id="b7ac1-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="b7ac1-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b7ac1-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="b7ac1-112">Methods</span></span>

<span data-ttu-id="b7ac1-113">La interfaz **IAMFilterData** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="b7ac1-113">The **IAMFilterData** interface has these methods.</span></span>



| <span data-ttu-id="b7ac1-114">Método</span><span class="sxs-lookup"><span data-stu-id="b7ac1-114">Method</span></span>                                                     | <span data-ttu-id="b7ac1-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="b7ac1-115">Description</span></span>                                               |
|:-----------------------------------------------------------|:----------------------------------------------------------|
| [<span data-ttu-id="b7ac1-116">**CreateFilterData**</span><span class="sxs-lookup"><span data-stu-id="b7ac1-116">**CreateFilterData**</span></span>](iamfilterdata-createfilterdata.md) | <span data-ttu-id="b7ac1-117">Crea datos de registro binarios para un filtro.</span><span class="sxs-lookup"><span data-stu-id="b7ac1-117">Creates binary registry data for a filter.</span></span><br/>     |
| [<span data-ttu-id="b7ac1-118">**ParseFilterData**</span><span class="sxs-lookup"><span data-stu-id="b7ac1-118">**ParseFilterData**</span></span>](iamfilterdata-parsefilterdata.md)   | <span data-ttu-id="b7ac1-119">Desempaqueta los datos de registro binarios para un filtro.</span><span class="sxs-lookup"><span data-stu-id="b7ac1-119">Unpacks the binary registry data for a filter.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b7ac1-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b7ac1-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b7ac1-121">El encabezado Fil \_ Data. h se encuentra en el directorio de [ejemplo del asignador](mapper-sample.md) en el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="b7ac1-121">The header Fil\_data.h is located in the [Mapper Sample](mapper-sample.md) directory in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b7ac1-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7ac1-122">Requirements</span></span>



| <span data-ttu-id="b7ac1-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7ac1-123">Requirement</span></span> | <span data-ttu-id="b7ac1-124">Value</span><span class="sxs-lookup"><span data-stu-id="b7ac1-124">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7ac1-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b7ac1-125">Header</span></span><br/> | <dl> <span data-ttu-id="b7ac1-126"><dt>Fil \_ Data. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7ac1-126"><dt>Fil\_data.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7ac1-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="b7ac1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7ac1-128">Interfaces desusadas</span><span class="sxs-lookup"><span data-stu-id="b7ac1-128">Deprecated Interfaces</span></span>](deprecated-interfaces.md)
</dt> </dl>

 

 
