---
title: COLUMN. columnResizeMode
description: El atributo columnResizeMode especifica o recupera el modo de cambiar el tamaño de esta columna.
ms.assetid: 95ece2a3-20a6-4b9d-a2eb-fc69fc612f29
keywords:
- COLUMN. columnResizeMode Windows Media Player
topic_type:
- apiref
api_name:
- COLUMN.columnResizeMode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52d17b1a2edd878fb15e69c595e3c061c1963a5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699669"
---
# <a name="columncolumnresizemode"></a><span data-ttu-id="97488-104">COLUMN. columnResizeMode</span><span class="sxs-lookup"><span data-stu-id="97488-104">COLUMN.columnResizeMode</span></span>

<span data-ttu-id="97488-105">El atributo **columnResizeMode** especifica o recupera el modo de cambiar el tamaño de esta columna.</span><span class="sxs-lookup"><span data-stu-id="97488-105">The **columnResizeMode** attribute specifies or retrieves the resize mode for this column.</span></span>

``` syntax
        elementID.columnResizeMode
```

## <a name="possible-values"></a><span data-ttu-id="97488-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="97488-106">Possible Values</span></span>

<span data-ttu-id="97488-107">Este atributo es una **cadena** de lectura/escritura que contiene uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="97488-107">This attribute is a read/write **String** containing one of the following values.</span></span>



| <span data-ttu-id="97488-108">Value</span><span class="sxs-lookup"><span data-stu-id="97488-108">Value</span></span>          | <span data-ttu-id="97488-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="97488-109">Description</span></span>                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97488-110">AutosizeHeader</span><span class="sxs-lookup"><span data-stu-id="97488-110">AutosizeHeader</span></span> | <span data-ttu-id="97488-111">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="97488-111">Default.</span></span> <span data-ttu-id="97488-112">La columna cambia de tamaño para dar cabida a todos los datos de la columna y del encabezado.</span><span class="sxs-lookup"><span data-stu-id="97488-112">The column resizes to accommodate all data in both the column and the header.</span></span>                         |
| <span data-ttu-id="97488-113">AutosizeData</span><span class="sxs-lookup"><span data-stu-id="97488-113">AutosizeData</span></span>   | <span data-ttu-id="97488-114">La columna cambia de tamaño para alojar solo todos los datos de la columna.</span><span class="sxs-lookup"><span data-stu-id="97488-114">The column resizes to accommodate all data in the column only.</span></span>                                                 |
| <span data-ttu-id="97488-115">Fijo</span><span class="sxs-lookup"><span data-stu-id="97488-115">Fixed</span></span>          | <span data-ttu-id="97488-116">La columna tiene un tamaño fijo.</span><span class="sxs-lookup"><span data-stu-id="97488-116">The column is a fixed size.</span></span>                                                                                    |
| <span data-ttu-id="97488-117">Se expande</span><span class="sxs-lookup"><span data-stu-id="97488-117">Stretches</span></span>      | <span data-ttu-id="97488-118">La columna cambia de tamaño para usar el espacio restante en el control de la **lista de reproducción** después de cambiar el tamaño de todas las demás columnas.</span><span class="sxs-lookup"><span data-stu-id="97488-118">The column resizes to use the remaining space in the **PLAYLIST** control after all other columns are resized.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="97488-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97488-119">Requirements</span></span>



| <span data-ttu-id="97488-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="97488-120">Requirement</span></span> | <span data-ttu-id="97488-121">Value</span><span class="sxs-lookup"><span data-stu-id="97488-121">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="97488-122">Versión</span><span class="sxs-lookup"><span data-stu-id="97488-122">Version</span></span><br/> | <span data-ttu-id="97488-123">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="97488-123">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="97488-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="97488-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97488-125">**COLUMN, elemento**</span><span class="sxs-lookup"><span data-stu-id="97488-125">**COLUMN Element**</span></span>](column-element.md)
</dt> </dl>

 

 





