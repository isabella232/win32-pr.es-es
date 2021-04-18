---
title: VISTA. redimensionable
description: El atributo de tamaño variable recupera un valor que indica si se puede cambiar el tamaño de la vista.
ms.assetid: 4f0e4f31-cf16-498f-823f-da43566043b1
keywords:
- VISTA. redimensionable de Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.resizable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed4d61973e34891d336ea5729ea40478c6c32808
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718607"
---
# <a name="viewresizable"></a><span data-ttu-id="0b6b0-104">VISTA. redimensionable</span><span class="sxs-lookup"><span data-stu-id="0b6b0-104">VIEW.resizable</span></span>

<span data-ttu-id="0b6b0-105">El atributo de tamaño **variable** recupera un valor que indica si se puede cambiar el tamaño de la **vista** .</span><span class="sxs-lookup"><span data-stu-id="0b6b0-105">The **resizable** attribute retrieves a value indicating whether the **VIEW** can be resized.</span></span>

``` syntax
        elementID.resizable
```

## <a name="possible-values"></a><span data-ttu-id="0b6b0-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="0b6b0-106">Possible Values</span></span>

<span data-ttu-id="0b6b0-107">Este atributo es un **booleano** de solo lectura con un valor predeterminado igual al atributo **TitleBar** .</span><span class="sxs-lookup"><span data-stu-id="0b6b0-107">This attribute is a read-only **Boolean** with a default value equal to the **titlebar** attribute.</span></span>



| <span data-ttu-id="0b6b0-108">Valores</span><span class="sxs-lookup"><span data-stu-id="0b6b0-108">Values</span></span> | <span data-ttu-id="0b6b0-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="0b6b0-109">Description</span></span>             |
|--------|-------------------------|
| <span data-ttu-id="0b6b0-110">true</span><span class="sxs-lookup"><span data-stu-id="0b6b0-110">true</span></span>   | <span data-ttu-id="0b6b0-111">Se puede cambiar el tamaño de la vista.</span><span class="sxs-lookup"><span data-stu-id="0b6b0-111">View can be resized.</span></span>    |
| <span data-ttu-id="0b6b0-112">false</span><span class="sxs-lookup"><span data-stu-id="0b6b0-112">false</span></span>  | <span data-ttu-id="0b6b0-113">No se puede cambiar el tamaño de la vista.</span><span class="sxs-lookup"><span data-stu-id="0b6b0-113">View cannot be resized.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="0b6b0-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0b6b0-114">Remarks</span></span>

<span data-ttu-id="0b6b0-115">Si no hay ninguna **TitleBar** y, por tanto, no hay ninguna ventana o borde, debe utilizar el método **size** para cambiar el tamaño del elemento de **vista** .</span><span class="sxs-lookup"><span data-stu-id="0b6b0-115">If there is no **titlebar**, and therefore no window or border, you must use the **size** method to resize the **VIEW** element.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b6b0-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b6b0-116">Requirements</span></span>



| <span data-ttu-id="0b6b0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b6b0-117">Requirement</span></span> | <span data-ttu-id="0b6b0-118">Value</span><span class="sxs-lookup"><span data-stu-id="0b6b0-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="0b6b0-119">Versión</span><span class="sxs-lookup"><span data-stu-id="0b6b0-119">Version</span></span><br/> | <span data-ttu-id="0b6b0-120">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="0b6b0-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0b6b0-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b6b0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b6b0-122">**Elemento de vista**</span><span class="sxs-lookup"><span data-stu-id="0b6b0-122">**VIEW Element**</span></span>](view-element.md)
</dt> </dl>

 

 





