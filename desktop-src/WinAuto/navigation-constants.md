---
title: Constantes de navegación (oleacc. h)
description: En este tema se describen los valores constantes, definidos en oleacc. h, que indican la dirección espacial (arriba, abajo, izquierda y derecha) o lógica (primer elemento secundario, último, siguiente y anterior) observada cuando los clientes usan IAccessible accNavigate para desplazarse de un elemento de la interfaz de usuario a otro dentro del mismo contenedor.
ms.assetid: 5859a7a3-bcd3-443e-8ff0-4952f4639517
topic_type:
- apiref
api_name:
- NAVDIR_DOWN
- NAVDIR_FIRSTCHILD
- NAVDIR_LASTCHILD
- NAVDIR_LEFT
- NAVDIR_NEXT
- NAVDIR_PREVIOUS
- NAVDIR_RIGHT
- NAVDIR_UP
api_location:
- oleacc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8de5f4eaa3fc7fb24583e49bdd14acb9633b2bd4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660497"
---
# <a name="navigation-constants"></a><span data-ttu-id="c79ad-103">Constantes de navegación</span><span class="sxs-lookup"><span data-stu-id="c79ad-103">Navigation Constants</span></span>

<span data-ttu-id="c79ad-104">En este tema se describen los valores constantes, definidos en oleacc. h, que indican la dirección *espacial* (arriba, abajo, izquierda y derecha) o *lógica* (primera parte secundaria, última, siguiente y anterior) observada cuando los clientes usan [**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) para desplazarse de un elemento de la interfaz de usuario a otro dentro del mismo contenedor.</span><span class="sxs-lookup"><span data-stu-id="c79ad-104">This topic describes the constant values, defined in oleacc.h, that indicate the *spatial* (up, down, left, and right) or *logical* (first child, last, next, and previous) direction observed when clients use [**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) to navigate from one user interface element to another within the same container.</span></span> <span data-ttu-id="c79ad-105">Para obtener más información, vea [métodos y propiedades de navegación de objetos](object-navigation-properties-and-methods.md).</span><span class="sxs-lookup"><span data-stu-id="c79ad-105">For more information, see [Object Navigation Properties and Methods](object-navigation-properties-and-methods.md).</span></span>

<span data-ttu-id="c79ad-106">Las constantes de navegación de Microsoft Active Accessibility son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="c79ad-106">The Microsoft Active Accessibility navigation constants are as follows:</span></span>



| <span data-ttu-id="c79ad-107">Constante</span><span class="sxs-lookup"><span data-stu-id="c79ad-107">Constant</span></span>                                                                                                                                                                  | <span data-ttu-id="c79ad-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="c79ad-108">Description</span></span>                                                                                                                                           |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NAVDIR_DOWN"></span><span id="navdir_down"></span><dl> <span data-ttu-id="c79ad-109"><dt>**NAVDIR \_ abajo**</dt></span><span class="sxs-lookup"><span data-stu-id="c79ad-109"><dt>**NAVDIR\_DOWN**</dt></span></span> </dl>                   | <span data-ttu-id="c79ad-110">Navegue hasta el objeto relacionado que se encuentra debajo del objeto inicial.</span><span class="sxs-lookup"><span data-stu-id="c79ad-110">Navigate to the sibling object that is located below the starting object.</span></span><br/>                                                                  |
| <span id="NAVDIR_FIRSTCHILD"></span><span id="navdir_firstchild"></span><dl> <span data-ttu-id="c79ad-111"><dt>**NAVDIR \_ FIRSTCHILD**</dt></span><span class="sxs-lookup"><span data-stu-id="c79ad-111"><dt>**NAVDIR\_FIRSTCHILD**</dt></span></span> </dl> | <span data-ttu-id="c79ad-112">Navegue hasta el primer elemento secundario de este objeto.</span><span class="sxs-lookup"><span data-stu-id="c79ad-112">Navigate to the first child of this object.</span></span> <span data-ttu-id="c79ad-113">Cuando se usa esta marca, el miembro **lVal** del parámetro *VARSTART* debe ser CHILDID \_ Self.</span><span class="sxs-lookup"><span data-stu-id="c79ad-113">When this flag is used, the **lVal** member of the *varStart* parameter must be CHILDID\_SELF.</span></span><br/> |
| <span id="NAVDIR_LASTCHILD"></span><span id="navdir_lastchild"></span><dl> <span data-ttu-id="c79ad-114"><dt>**NAVDIR \_ LASTCHILD**</dt></span><span class="sxs-lookup"><span data-stu-id="c79ad-114"><dt>**NAVDIR\_LASTCHILD**</dt></span></span> </dl>    | <span data-ttu-id="c79ad-115">Navegue hasta el último elemento secundario de este objeto.</span><span class="sxs-lookup"><span data-stu-id="c79ad-115">Navigate to the last child of this object.</span></span> <span data-ttu-id="c79ad-116">Cuando se usa esta marca, el miembro **lVal** del parámetro *VARSTART* debe ser CHILDID \_ Self.</span><span class="sxs-lookup"><span data-stu-id="c79ad-116">When using this flag, the **lVal** member of the *varStart* parameter must be CHILDID\_SELF.</span></span><br/>    |
| <span id="NAVDIR_LEFT"></span><span id="navdir_left"></span><dl> <span data-ttu-id="c79ad-117"><dt>**NAVDIR a la \_ izquierda**</dt></span><span class="sxs-lookup"><span data-stu-id="c79ad-117"><dt>**NAVDIR\_LEFT**</dt></span></span> </dl>                   | <span data-ttu-id="c79ad-118">Navegue hasta el objeto relacionado situado a la izquierda del objeto inicial.</span><span class="sxs-lookup"><span data-stu-id="c79ad-118">Navigate to the sibling object located to the left of the starting object.</span></span><br/>                                                                 |
| <span id="NAVDIR_NEXT"></span><span id="navdir_next"></span><dl> <span data-ttu-id="c79ad-119"><dt>**NAVDIR \_ siguiente**</dt></span><span class="sxs-lookup"><span data-stu-id="c79ad-119"><dt>**NAVDIR\_NEXT**</dt></span></span> </dl>                   | <span data-ttu-id="c79ad-120">Navegue hasta el siguiente objeto lógico; por lo general, es un elemento relacionado del objeto inicial.</span><span class="sxs-lookup"><span data-stu-id="c79ad-120">Navigate to the next logical object; generally, it is a sibling of the starting object.</span></span><br/>                                                    |
| <span id="NAVDIR_PREVIOUS"></span><span id="navdir_previous"></span><dl> <span data-ttu-id="c79ad-121"><dt>**NAVDIR \_ anterior**</dt></span><span class="sxs-lookup"><span data-stu-id="c79ad-121"><dt>**NAVDIR\_PREVIOUS**</dt></span></span> </dl>       | <span data-ttu-id="c79ad-122">Navegue hasta el objeto lógico anterior; por lo general, es un elemento relacionado del objeto inicial.</span><span class="sxs-lookup"><span data-stu-id="c79ad-122">Navigate to the previous logical object; generally, it is a sibling of the starting object.</span></span><br/>                                                |
| <span id="NAVDIR_RIGHT"></span><span id="navdir_right"></span><dl> <span data-ttu-id="c79ad-123"><dt>**NAVDIR \_ derecha**</dt></span><span class="sxs-lookup"><span data-stu-id="c79ad-123"><dt>**NAVDIR\_RIGHT**</dt></span></span> </dl>                | <span data-ttu-id="c79ad-124">Navegue hasta el objeto relacionado que se encuentra a la derecha del objeto de inicio.</span><span class="sxs-lookup"><span data-stu-id="c79ad-124">Navigate to the sibling object that is located to the right of the starting object.</span></span><br/>                                                        |
| <span id="NAVDIR_UP"></span><span id="navdir_up"></span><dl> <span data-ttu-id="c79ad-125"><dt>**NAVDIR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c79ad-125"><dt>**NAVDIR\_UP**</dt></span></span> </dl>                         | <span data-ttu-id="c79ad-126">Navegue hasta el objeto relacionado que se encuentra encima del objeto inicial.</span><span class="sxs-lookup"><span data-stu-id="c79ad-126">Navigate to the sibling object that is located above the starting object.</span></span><br/>                                                                  |



## <a name="requirements"></a><span data-ttu-id="c79ad-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c79ad-127">Requirements</span></span>



| <span data-ttu-id="c79ad-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="c79ad-128">Requirement</span></span> | <span data-ttu-id="c79ad-129">Value</span><span class="sxs-lookup"><span data-stu-id="c79ad-129">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c79ad-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c79ad-130">Header</span></span><br/> | <dl> <span data-ttu-id="c79ad-131"><dt>Oleacc. h</dt></span><span class="sxs-lookup"><span data-stu-id="c79ad-131"><dt>Oleacc.h</dt></span></span> </dl> |



 

 





