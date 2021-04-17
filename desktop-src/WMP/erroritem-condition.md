---
title: ErrorItem. Condition
description: La propiedad Condition recupera un valor que indica la condición del error.
ms.assetid: efb54b48-cfaa-479f-9ee6-ce6724dca24c
keywords:
- ErrorItem. Condition Windows Media Player
topic_type:
- apiref
api_name:
- ErrorItem.condition
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c498e7479a7a3e067dea2d8a562800351effd672
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700106"
---
# <a name="erroritemcondition"></a><span data-ttu-id="6759e-104">ErrorItem. Condition</span><span class="sxs-lookup"><span data-stu-id="6759e-104">ErrorItem.condition</span></span>

<span data-ttu-id="6759e-105">La propiedad **Condition** recupera un valor que indica la condición del error.</span><span class="sxs-lookup"><span data-stu-id="6759e-105">The **condition** property retrieves a value indicating the condition for the error.</span></span>

``` syntax
player.error.item(
        index
        ).condition
      
```

## <a name="possible-values"></a><span data-ttu-id="6759e-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="6759e-106">Possible Values</span></span>

<span data-ttu-id="6759e-107">Esta propiedad es un **número** de solo lectura (**Long**) que representa el código de condición.</span><span class="sxs-lookup"><span data-stu-id="6759e-107">This property is a read-only **Number** (**long**) that represents the condition code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6759e-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6759e-108">Remarks</span></span>

<span data-ttu-id="6759e-109">El código de condición es un valor que usa Microsoft para proporcionar información adicional al personal de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="6759e-109">The condition code is a value that is used by Microsoft to provide additional information for technical support personnel.</span></span>

<span data-ttu-id="6759e-110">**Windows Media Player 10 Mobile:** Esta propiedad siempre devuelve 0.</span><span class="sxs-lookup"><span data-stu-id="6759e-110">**Windows Media Player 10 Mobile:** This property always returns 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="6759e-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6759e-111">Requirements</span></span>



| <span data-ttu-id="6759e-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="6759e-112">Requirement</span></span> | <span data-ttu-id="6759e-113">Value</span><span class="sxs-lookup"><span data-stu-id="6759e-113">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6759e-114">Versión</span><span class="sxs-lookup"><span data-stu-id="6759e-114">Version</span></span><br/> | <span data-ttu-id="6759e-115">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="6759e-115">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="6759e-116">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6759e-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="6759e-117"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6759e-117"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6759e-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="6759e-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6759e-119">**Objeto ErrorItem**</span><span class="sxs-lookup"><span data-stu-id="6759e-119">**ErrorItem Object**</span></span>](erroritem-object.md)
</dt> </dl>

 

 





