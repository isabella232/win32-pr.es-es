---
description: Los tipos de formato entero de los datos configurables se pueden usar en campos de base de datos de texto o enteros. El atributo msmConfigItemNonNullable está implícito en este formato de datos y no es necesario establecerlo. Null nunca es un valor válido para este tipo.
ms.assetid: 63fb9c0d-e7f1-4c1d-bb83-2833c5fff18d
title: Tipos de formato entero
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 184ef6380f25474a9e2ad07be7a4eb6d00706aee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814403"
---
# <a name="integer-format-types"></a><span data-ttu-id="12cb6-105">Tipos de formato entero</span><span class="sxs-lookup"><span data-stu-id="12cb6-105">Integer Format Types</span></span>

<span data-ttu-id="12cb6-106">Los tipos de formato entero de los datos configurables se pueden usar en campos de base de datos de texto o enteros.</span><span class="sxs-lookup"><span data-stu-id="12cb6-106">The Integer Format Types of configurable data may be used in either text or integer database fields.</span></span> <span data-ttu-id="12cb6-107">El atributo msmConfigItemNonNullable está implícito en este formato de datos y no es necesario establecerlo.</span><span class="sxs-lookup"><span data-stu-id="12cb6-107">The msmConfigItemNonNullable attribute is implicit in this data format and does not need to be set.</span></span> <span data-ttu-id="12cb6-108">Null nunca es un valor válido para este tipo.</span><span class="sxs-lookup"><span data-stu-id="12cb6-108">Null is never a valid value for this type.</span></span>

<span data-ttu-id="12cb6-109">Existe el siguiente tipo de formato entero.</span><span class="sxs-lookup"><span data-stu-id="12cb6-109">The following Integer Format type exists.</span></span>

[<span data-ttu-id="12cb6-110">Tipo de entero arbitrario</span><span class="sxs-lookup"><span data-stu-id="12cb6-110">Arbitrary Integer Type</span></span>](arbitrary-integer-type.md)

<span data-ttu-id="12cb6-111">Los elementos configurables del tipo de formato entero se utilizan en columnas de texto o de enteros y, en general, se pueden reemplazar por cualquier entero positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="12cb6-111">Configurable items of the Integer Format Type are used in either text or integer columns and in general could be replaced by any positive or negative integer.</span></span> <span data-ttu-id="12cb6-112">Sin embargo, los elementos configurables concretos también pueden tener restricciones semánticas característicos.</span><span class="sxs-lookup"><span data-stu-id="12cb6-112">However, particular configurable items may also have characteristic semantic restrictions.</span></span> <span data-ttu-id="12cb6-113">Por ejemplo, un determinado elemento configurable debe ser un entero entre 0 y 100 y una restricción semántica adicional.</span><span class="sxs-lookup"><span data-stu-id="12cb6-113">For example, a particular configurable item required to be an integer between 0 and 100 has and additional semantic restriction.</span></span> <span data-ttu-id="12cb6-114">Estas restricciones no se aplican mediante Mergemod.dll y, por tanto, los autores de módulos deben estar preparados para controlar cualquier cadena que satisfaga el tipo de formato entero especificado.</span><span class="sxs-lookup"><span data-stu-id="12cb6-114">Such restrictions are not enforced by Mergemod.dll and therefore module authors should be prepared to handle any string that satisfies the specified Integer Format type.</span></span>

 

 



