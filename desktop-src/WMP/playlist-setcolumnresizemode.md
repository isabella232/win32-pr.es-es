---
title: Lista de reproducción. setColumnResizeMode
description: El método setColumnResizeMode especifica cómo se ajusta el tamaño de las columnas indizadas.
ms.assetid: 84ca0e60-ca24-4058-ae08-5b9cf3d7c38f
keywords:
- Windows Media Player de lista de reproducción. setColumnResizeMode
topic_type:
- apiref
api_name:
- PLAYLIST.setColumnResizeMode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a1b83020f4400f4f1095c84e281fe498f2b67da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709266"
---
# <a name="playlistsetcolumnresizemode"></a><span data-ttu-id="b91cd-104">Lista de reproducción. setColumnResizeMode</span><span class="sxs-lookup"><span data-stu-id="b91cd-104">PLAYLIST.setColumnResizeMode</span></span>

<span data-ttu-id="b91cd-105">El método **setColumnResizeMode** especifica cómo se ajusta el tamaño de las columnas indizadas.</span><span class="sxs-lookup"><span data-stu-id="b91cd-105">The **setColumnResizeMode** method specifies how the indexed column sizes itself.</span></span>

``` syntax
        elementID.setColumnResizeMode(column, mode)
```

## <a name="parameters"></a><span data-ttu-id="b91cd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b91cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b91cd-107"><span id="column"></span><span id="COLUMN"></span>*artículo*</span><span class="sxs-lookup"><span data-stu-id="b91cd-107"><span id="column"></span><span id="COLUMN"></span>*column*</span></span>
</dt> <dd>

<span data-ttu-id="b91cd-108">**Número** (**largo**) que indica el índice de la columna que se va a cambiar.</span><span class="sxs-lookup"><span data-stu-id="b91cd-108">**Number** (**long**) indicating the index of the column to be changed.</span></span>

</dd> <dt>

<span data-ttu-id="b91cd-109"><span id="mode"></span><span id="MODE"></span>*modo*</span><span class="sxs-lookup"><span data-stu-id="b91cd-109"><span id="mode"></span><span id="MODE"></span>*mode*</span></span>
</dt> <dd>

<span data-ttu-id="b91cd-110">**Cadena** que indica el modo de ajuste de tamaño.</span><span class="sxs-lookup"><span data-stu-id="b91cd-110">**String** indicating the sizing mode.</span></span> <span data-ttu-id="b91cd-111">Contiene uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="b91cd-111">Contains one of the following values.</span></span>



| <span data-ttu-id="b91cd-112">Value</span><span class="sxs-lookup"><span data-stu-id="b91cd-112">Value</span></span>          | <span data-ttu-id="b91cd-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="b91cd-113">Description</span></span>                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b91cd-114">AutosizeHeader</span><span class="sxs-lookup"><span data-stu-id="b91cd-114">AutosizeHeader</span></span> | <span data-ttu-id="b91cd-115">La columna cambia de tamaño para dar cabida a todos los datos de la columna y del encabezado.</span><span class="sxs-lookup"><span data-stu-id="b91cd-115">The column resizes to accommodate all data in both the column and the header.</span></span>                                  |
| <span data-ttu-id="b91cd-116">AutosizeData</span><span class="sxs-lookup"><span data-stu-id="b91cd-116">AutosizeData</span></span>   | <span data-ttu-id="b91cd-117">La columna cambia de tamaño para alojar solo todos los datos de la columna.</span><span class="sxs-lookup"><span data-stu-id="b91cd-117">The column resizes to accommodate all data in the column only.</span></span>                                                 |
| <span data-ttu-id="b91cd-118">Fijo</span><span class="sxs-lookup"><span data-stu-id="b91cd-118">Fixed</span></span>          | <span data-ttu-id="b91cd-119">La columna tiene un tamaño fijo.</span><span class="sxs-lookup"><span data-stu-id="b91cd-119">The column is a fixed size.</span></span>                                                                                    |
| <span data-ttu-id="b91cd-120">Se expande</span><span class="sxs-lookup"><span data-stu-id="b91cd-120">Stretches</span></span>      | <span data-ttu-id="b91cd-121">La columna cambia de tamaño para usar el espacio restante en el elemento de **lista de reproducción** después de cambiar el tamaño de todas las demás columnas.</span><span class="sxs-lookup"><span data-stu-id="b91cd-121">The column resizes to use the remaining space in the **PLAYLIST** element after all other columns are resized.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b91cd-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b91cd-122">Return Value</span></span>

<span data-ttu-id="b91cd-123">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="b91cd-123">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b91cd-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b91cd-124">Requirements</span></span>



| <span data-ttu-id="b91cd-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b91cd-125">Requirement</span></span> | <span data-ttu-id="b91cd-126">Value</span><span class="sxs-lookup"><span data-stu-id="b91cd-126">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="b91cd-127">Versión</span><span class="sxs-lookup"><span data-stu-id="b91cd-127">Version</span></span><br/> | <span data-ttu-id="b91cd-128">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="b91cd-128">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b91cd-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="b91cd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b91cd-130">**Elemento PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="b91cd-130">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> </dl>

 

 





