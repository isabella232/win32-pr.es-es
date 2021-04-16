---
title: Lista de reproducción. sortColumn
description: El método sortColumn ordena los datos de la columna especificada.
ms.assetid: 1563fee8-044a-4cb4-a9c2-11d4533536da
keywords:
- Media Player de listas de reproducción. sortColumn de Windows
topic_type:
- apiref
api_name:
- PLAYLIST.sortColumn
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f21f0032ee4db4c7af46b5dda814bb11db551330
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105719019"
---
# <a name="playlistsortcolumn"></a><span data-ttu-id="c5ffd-104">Lista de reproducción. sortColumn</span><span class="sxs-lookup"><span data-stu-id="c5ffd-104">PLAYLIST.sortColumn</span></span>

<span data-ttu-id="c5ffd-105">El método **sortColumn** ordena los datos de la columna especificada.</span><span class="sxs-lookup"><span data-stu-id="c5ffd-105">The **sortColumn** method sorts the data in the specified column.</span></span>

``` syntax
        elementID.sortColumn(column)
```

## <a name="parameters"></a><span data-ttu-id="c5ffd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c5ffd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5ffd-107"><span id="column"></span><span id="COLUMN"></span>*artículo*</span><span class="sxs-lookup"><span data-stu-id="c5ffd-107"><span id="column"></span><span id="COLUMN"></span>*column*</span></span>
</dt> <dd>

<span data-ttu-id="c5ffd-108">**Número** (**largo**) que indica el índice de la columna que se va a ordenar.</span><span class="sxs-lookup"><span data-stu-id="c5ffd-108">**Number** (**long**) indicating the index of the column to sort.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5ffd-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c5ffd-109">Return Value</span></span>

<span data-ttu-id="c5ffd-110">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="c5ffd-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5ffd-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c5ffd-111">Remarks</span></span>

<span data-ttu-id="c5ffd-112">Este método ordena la columna especificada de la misma manera que los botones de encabezado de columna del elemento de **lista de reproducción** .</span><span class="sxs-lookup"><span data-stu-id="c5ffd-112">This method sorts the specified column in the same way as the column header buttons in the **PLAYLIST** element.</span></span> <span data-ttu-id="c5ffd-113">Si la columna no se ha ordenado todavía, se ordena en orden alfanumérico.</span><span class="sxs-lookup"><span data-stu-id="c5ffd-113">If the column has not yet been sorted, it is sorted in alphanumeric order.</span></span> <span data-ttu-id="c5ffd-114">Si se ha ordenado, se invierte su orden.</span><span class="sxs-lookup"><span data-stu-id="c5ffd-114">If it has been sorted, its order is reversed.</span></span>

<span data-ttu-id="c5ffd-115">Para que este método funcione, el atributo **allowColumnSorting** debe establecerse en true.</span><span class="sxs-lookup"><span data-stu-id="c5ffd-115">For this method to work, the **allowColumnSorting** attribute must be set to true.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5ffd-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5ffd-116">Requirements</span></span>



| <span data-ttu-id="c5ffd-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5ffd-117">Requirement</span></span> | <span data-ttu-id="c5ffd-118">Value</span><span class="sxs-lookup"><span data-stu-id="c5ffd-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="c5ffd-119">Versión</span><span class="sxs-lookup"><span data-stu-id="c5ffd-119">Version</span></span><br/> | <span data-ttu-id="c5ffd-120">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="c5ffd-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c5ffd-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="c5ffd-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5ffd-122">**Elemento PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="c5ffd-122">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="c5ffd-123">**Lista de reproducción. allowColumnSorting**</span><span class="sxs-lookup"><span data-stu-id="c5ffd-123">**PLAYLIST.allowColumnSorting**</span></span>](playlist-allowcolumnsorting.md)
</dt> </dl>

 

 





