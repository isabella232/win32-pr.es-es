---
description: La \_ estructura de filtro AMOVIESETUP contiene información para registrar un filtro.
ms.assetid: 72e58f33-e480-4b32-b3d5-8f6c8eb2d5a3
title: Estructura de AMOVIESETUP_FILTER (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMOVIESETUP_FILTER
api_type:
- HeaderDef
api_location:
- combase.h
ms.openlocfilehash: 55a225185733a822591d8f93c2eca3674d51a340
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661116"
---
# <a name="amoviesetup_filter-structure"></a><span data-ttu-id="3ac94-103">AMOVIESETUP \_ estructura de filtro</span><span class="sxs-lookup"><span data-stu-id="3ac94-103">AMOVIESETUP\_FILTER structure</span></span>

<span data-ttu-id="3ac94-104">La estructura de **\_ filtro AMOVIESETUP** contiene información para registrar un filtro.</span><span class="sxs-lookup"><span data-stu-id="3ac94-104">The **AMOVIESETUP\_FILTER** structure contains information for registering a filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ac94-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3ac94-105">Syntax</span></span>


```C++
typedef struct _AMOVIESETUP_FILTER {
  const  CLSID           *clsID;
  const  WCHAR           *strName;
  DWORD                  dwMerit;
  UINT                   nPins;
  const  AMOVIESETUP_PIN *lpPin;
} AMOVIESETUP_FILTER, *PAMOVIESETUP_FILTER, *FAR LPAMOVIESETUP_FILTER;
```



## <a name="members"></a><span data-ttu-id="3ac94-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="3ac94-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="3ac94-107">**clsID**</span><span class="sxs-lookup"><span data-stu-id="3ac94-107">**clsID**</span></span>
</dt> <dd>

<span data-ttu-id="3ac94-108">Identificador de clase del filtro.</span><span class="sxs-lookup"><span data-stu-id="3ac94-108">Class identifier of the filter.</span></span>

</dd> <dt>

<span data-ttu-id="3ac94-109">**strName**</span><span class="sxs-lookup"><span data-stu-id="3ac94-109">**strName**</span></span>
</dt> <dd>

<span data-ttu-id="3ac94-110">Nombre del filtro.</span><span class="sxs-lookup"><span data-stu-id="3ac94-110">Name of the filter.</span></span>

</dd> <dt>

<span data-ttu-id="3ac94-111">**dwMerit**</span><span class="sxs-lookup"><span data-stu-id="3ac94-111">**dwMerit**</span></span>
</dt> <dd>

<span data-ttu-id="3ac94-112">Mérito del filtro.</span><span class="sxs-lookup"><span data-stu-id="3ac94-112">Filter merit.</span></span> <span data-ttu-id="3ac94-113">Lo usa la interfaz [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) al construir un gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="3ac94-113">Used by the [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) interface when constructing a filter graph.</span></span> <span data-ttu-id="3ac94-114">Para obtener una lista de los valores de méritos, vea [mérito](merit.md).</span><span class="sxs-lookup"><span data-stu-id="3ac94-114">For a list of merit values, see [Merit](merit.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ac94-115">**nPins**</span><span class="sxs-lookup"><span data-stu-id="3ac94-115">**nPins**</span></span>
</dt> <dd>

<span data-ttu-id="3ac94-116">Número de elementos de la matriz *lpPin* .</span><span class="sxs-lookup"><span data-stu-id="3ac94-116">Number of elements in the *lpPin* array.</span></span> <span data-ttu-id="3ac94-117">Si *lpPin* es **null**, establezca este miembro en cero.</span><span class="sxs-lookup"><span data-stu-id="3ac94-117">If *lpPin* is **NULL**, set this member to zero.</span></span>

</dd> <dt>

<span data-ttu-id="3ac94-118">**lpPin**</span><span class="sxs-lookup"><span data-stu-id="3ac94-118">**lpPin**</span></span>
</dt> <dd>

<span data-ttu-id="3ac94-119">Puntero a una matriz de estructuras [**AMOVIESETUP \_ PIN**](amoviesetup-pin.md) , de tamaño *nPins*.</span><span class="sxs-lookup"><span data-stu-id="3ac94-119">Pointer to an array of [**AMOVIESETUP\_PIN**](amoviesetup-pin.md) structures, of size *nPins*.</span></span> <span data-ttu-id="3ac94-120">Cada miembro de esta matriz describe un PIN en el filtro.</span><span class="sxs-lookup"><span data-stu-id="3ac94-120">Each member of this array describes a pin on the filter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3ac94-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3ac94-121">Remarks</span></span>

<span data-ttu-id="3ac94-122">Para obtener información acerca del uso de esta estructura, consulte [How to Register DirectShow filters](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="3ac94-122">For information about using this structure, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span> <span data-ttu-id="3ac94-123">Use esta estructura solo para los filtros que se registran en la categoría de filtro predeterminada (CLSID \_ LegacyAmFilterCategory).</span><span class="sxs-lookup"><span data-stu-id="3ac94-123">Use this structure only for filters that are registered in the default filter category (CLSID\_LegacyAmFilterCategory).</span></span> <span data-ttu-id="3ac94-124">Para registrar un filtro en una categoría diferente, use el método [**IFilterMapper2:: RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) , como se describe en [implementación de DllRegisterServer](implementing-dllregisterserver.md).</span><span class="sxs-lookup"><span data-stu-id="3ac94-124">To register a filter in a different category, use the [**IFilterMapper2::RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) method, as described in [Implementing DllRegisterServer](implementing-dllregisterserver.md).</span></span>

> [!Note]  
> <span data-ttu-id="3ac94-125">El archivo de encabezado ComBase. h se proporciona con las [clases base de DirectShow](directshow-base-classes.md).</span><span class="sxs-lookup"><span data-stu-id="3ac94-125">The header file combase.h is provided with the [DirectShow Base Classes](directshow-base-classes.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3ac94-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ac94-126">Requirements</span></span>



| <span data-ttu-id="3ac94-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ac94-127">Requirement</span></span> | <span data-ttu-id="3ac94-128">Value</span><span class="sxs-lookup"><span data-stu-id="3ac94-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ac94-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3ac94-129">Header</span></span><br/> | <dl> <span data-ttu-id="3ac94-130"><dt>ComBase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3ac94-130"><dt>Combase.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ac94-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="3ac94-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ac94-132">Estructuras de DirectShow</span><span class="sxs-lookup"><span data-stu-id="3ac94-132">DirectShow Structures</span></span>](directshow-structures.md)
</dt> </dl>

 

 




