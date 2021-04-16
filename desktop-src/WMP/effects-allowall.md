---
title: EFFECTs. allowAll
description: El atributo allowAll especifica o recupera un valor que indica si se deben incluir todas las visualizaciones que se encuentran en el registro.
ms.assetid: 8552cc06-05b2-4049-ba7d-f6bd770449e0
keywords:
- EFFECTs. allowAll Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.allowAll
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56760021fe34522072677e9524fe6636e519e20f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699384"
---
# <a name="effectsallowall"></a><span data-ttu-id="5cb30-104">EFFECTs. allowAll</span><span class="sxs-lookup"><span data-stu-id="5cb30-104">EFFECTS.allowAll</span></span>

<span data-ttu-id="5cb30-105">El atributo **allowAll** especifica o recupera un valor que indica si se deben incluir todas las visualizaciones que se encuentran en el registro.</span><span class="sxs-lookup"><span data-stu-id="5cb30-105">The **allowAll** attribute specifies or retrieves a value indicating whether to include all the visualizations that are in the registry.</span></span>

``` syntax
        elementID.allowAll
```

## <a name="possible-values"></a><span data-ttu-id="5cb30-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="5cb30-106">Possible Values</span></span>

<span data-ttu-id="5cb30-107">Este atributo es un **valor booleano** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="5cb30-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="5cb30-108">Value</span><span class="sxs-lookup"><span data-stu-id="5cb30-108">Value</span></span> | <span data-ttu-id="5cb30-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="5cb30-109">Description</span></span>                                                         |
|-------|---------------------------------------------------------------------|
| <span data-ttu-id="5cb30-110">true</span><span class="sxs-lookup"><span data-stu-id="5cb30-110">true</span></span>  | <span data-ttu-id="5cb30-111">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="5cb30-111">Default.</span></span> <span data-ttu-id="5cb30-112">Permite el ciclo de todas las visualizaciones en el sistema del usuario.</span><span class="sxs-lookup"><span data-stu-id="5cb30-112">Allows cycling of all visualizations on the user's system.</span></span> |
| <span data-ttu-id="5cb30-113">false</span><span class="sxs-lookup"><span data-stu-id="5cb30-113">false</span></span> | <span data-ttu-id="5cb30-114">Limita el ciclo a las visualizaciones que aparecen dentro de las etiquetas de **efectos** .</span><span class="sxs-lookup"><span data-stu-id="5cb30-114">Limits cycling to visualizations appearing within **EFFECTS** tags.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="5cb30-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5cb30-115">Remarks</span></span>

<span data-ttu-id="5cb30-116">Si este atributo se establece en false, solo las visualizaciones que aparecen dentro de las etiquetas **Effects** se pueden recorrer en iteración mediante PREVIOUS/NEXT.</span><span class="sxs-lookup"><span data-stu-id="5cb30-116">If this attribute is set to false, only the visualizations appearing within **EFFECTS** tags can be cycled through using previous/next.</span></span> <span data-ttu-id="5cb30-117">Si se establece en true, todas las visualizaciones que se registran en el sistema del usuario se pueden recorrer.</span><span class="sxs-lookup"><span data-stu-id="5cb30-117">If it is set to true, then all visualizations that are registered on the user's system can be cycled through.</span></span> <span data-ttu-id="5cb30-118">Si se establece en true y se especifican las visualizaciones dentro de las etiquetas **Effects** , los atributos especificados en estas etiquetas se aplican a todas las visualizaciones del sistema del usuario.</span><span class="sxs-lookup"><span data-stu-id="5cb30-118">If it is set to true and you specify any visualizations within **EFFECTS** tags, then the attributes specified in these tags are applied to all visualizations on the user's system.</span></span>

## <a name="requirements"></a><span data-ttu-id="5cb30-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5cb30-119">Requirements</span></span>



| <span data-ttu-id="5cb30-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5cb30-120">Requirement</span></span> | <span data-ttu-id="5cb30-121">Value</span><span class="sxs-lookup"><span data-stu-id="5cb30-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="5cb30-122">Versión</span><span class="sxs-lookup"><span data-stu-id="5cb30-122">Version</span></span><br/> | <span data-ttu-id="5cb30-123">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="5cb30-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5cb30-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="5cb30-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cb30-125">**EFFECTs, elemento**</span><span class="sxs-lookup"><span data-stu-id="5cb30-125">**EFFECTS Element**</span></span>](effects-element.md)
</dt> </dl>

 

 





