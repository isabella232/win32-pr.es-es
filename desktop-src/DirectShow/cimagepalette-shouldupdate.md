---
description: El método ShouldUpdate determina si es necesario crear una nueva paleta.
ms.assetid: 50886277-189b-4102-ade9-0366f64fdbcb
title: Método CImagePalette. ShouldUpdate (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.ShouldUpdate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f8cf27548487ad0338f0c4773c66df8f7d03c2f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670491"
---
# <a name="cimagepaletteshouldupdate-method"></a><span data-ttu-id="de949-103">CImagePalette. ShouldUpdate, método</span><span class="sxs-lookup"><span data-stu-id="de949-103">CImagePalette.ShouldUpdate method</span></span>

<span data-ttu-id="de949-104">El `ShouldUpdate` método determina si es necesario crear una nueva paleta.</span><span class="sxs-lookup"><span data-stu-id="de949-104">The `ShouldUpdate` method determines whether it is necessary to create a new palette.</span></span>

## <a name="syntax"></a><span data-ttu-id="de949-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="de949-105">Syntax</span></span>


```C++
BOOL ShouldUpdate(
   const VIDEOINFOHEADER *pNewInfo,
   const VIDEOINFOHEADER *pOldInfo
);
```



## <a name="parameters"></a><span data-ttu-id="de949-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="de949-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de949-107">*pNewInfo*</span><span class="sxs-lookup"><span data-stu-id="de949-107">*pNewInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="de949-108">Puntero a una estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) que contiene la nueva tabla de colores.</span><span class="sxs-lookup"><span data-stu-id="de949-108">Pointer to a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure containing the new color table.</span></span>

</dd> <dt>

<span data-ttu-id="de949-109">*pOldInfo*</span><span class="sxs-lookup"><span data-stu-id="de949-109">*pOldInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="de949-110">Puntero a una estructura **VIDEOINFOHEADER** que contiene la tabla de colores antigua.</span><span class="sxs-lookup"><span data-stu-id="de949-110">Pointer to a **VIDEOINFOHEADER** structure containing the old color table.</span></span> <span data-ttu-id="de949-111">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="de949-111">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de949-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="de949-112">Return value</span></span>

<span data-ttu-id="de949-113">Devuelve **true** si la paleta debe actualizarse o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="de949-113">Returns **TRUE** if the palette needs to be updated, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="de949-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="de949-114">Remarks</span></span>

-   <span data-ttu-id="de949-115">Si ninguna de las estructuras **VIDEOINFOHEADER** contiene una tabla de colores, el método devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="de949-115">If neither **VIDEOINFOHEADER** structure contains a color table, the method returns **FALSE**.</span></span>
-   <span data-ttu-id="de949-116">Si solo una estructura contiene una tabla de colores, o si *pOldInfo* es **null**, el método devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="de949-116">If only one structure contains a color table, or if *pOldInfo* is **NULL**, the method returns **TRUE**.</span></span>
-   <span data-ttu-id="de949-117">Si ambas estructuras contienen tablas de color y las entradas de color coinciden, el método devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="de949-117">If both structures contain color tables, and the color entries match, the method returns **FALSE**.</span></span>
-   <span data-ttu-id="de949-118">Si ambas estructuras contienen tablas de color, pero las entradas de color no coinciden, el método devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="de949-118">If both structures contain color tables, but the color entries do not match, the method returns **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="de949-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de949-119">Requirements</span></span>



| <span data-ttu-id="de949-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="de949-120">Requirement</span></span> | <span data-ttu-id="de949-121">Value</span><span class="sxs-lookup"><span data-stu-id="de949-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de949-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="de949-122">Header</span></span><br/>  | <dl> <span data-ttu-id="de949-123"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="de949-123"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="de949-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="de949-124">Library</span></span><br/> | <dl> <span data-ttu-id="de949-125"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="de949-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de949-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="de949-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de949-127">**Clase CImagePalette**</span><span class="sxs-lookup"><span data-stu-id="de949-127">**CImagePalette Class**</span></span>](cimagepalette.md)
</dt> </dl>

 

 




