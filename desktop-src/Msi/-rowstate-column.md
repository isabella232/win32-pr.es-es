---
description: El nombre de la columna reservada \_ RowState representa el estado no persistente asociado a cada fila de la tabla en una tabla de base de datos del instalador.
ms.assetid: ff570b47-7c16-47ae-b1c2-2ecad9266372
title: _RowState columna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e61a2964d7d11c1c2429ad95e9de2b8bdb148954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082552"
---
# <a name="_rowstate-column"></a><span data-ttu-id="59cdf-103">\_Columna RowState</span><span class="sxs-lookup"><span data-stu-id="59cdf-103">\_RowState Column</span></span>

<span data-ttu-id="59cdf-104">El nombre de la columna reservada \_ RowState representa el estado no persistente asociado a cada fila de la tabla en una tabla de base de datos del instalador.</span><span class="sxs-lookup"><span data-stu-id="59cdf-104">The reserved column name \_RowState represents the non-persistent state associated with each table row in an installer database table.</span></span> <span data-ttu-id="59cdf-105">La pseudocolumna es de tipo [entero](integer.md)y el valor está compuesto de un conjunto de marcadores de bits.</span><span class="sxs-lookup"><span data-stu-id="59cdf-105">The pseudo-column is of type [Integer](integer.md), and the value consists of a set of bit flags.</span></span> <span data-ttu-id="59cdf-106">Todos los bits son legibles, pero solo se pueden establecer los bits de UserInfo y temporales.</span><span class="sxs-lookup"><span data-stu-id="59cdf-106">All the bits are readable, but only the UserInfo and Temporary bits can be set.</span></span> <span data-ttu-id="59cdf-107">Estos datos solo están disponibles siempre que las tablas estén bloqueadas o en uso (es decir, mientras exista una vista que contenga las tablas).</span><span class="sxs-lookup"><span data-stu-id="59cdf-107">This data is available only as long as the tables are locked or in use (that is, while a view containing the tables exists).</span></span> <span data-ttu-id="59cdf-108">En la tabla siguiente se muestran los atributos que puede tener una fila.</span><span class="sxs-lookup"><span data-stu-id="59cdf-108">The following table shows the attributes a row can have.</span></span>



| <span data-ttu-id="59cdf-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="59cdf-109">Name</span></span>           | <span data-ttu-id="59cdf-110">Value</span><span class="sxs-lookup"><span data-stu-id="59cdf-110">Value</span></span> | <span data-ttu-id="59cdf-111">Significado</span><span class="sxs-lookup"><span data-stu-id="59cdf-111">Meaning</span></span>                                                        |
|----------------|-------|----------------------------------------------------------------|
| <span data-ttu-id="59cdf-112">iraUserInfo</span><span class="sxs-lookup"><span data-stu-id="59cdf-112">iraUserInfo</span></span>    | <span data-ttu-id="59cdf-113">0x01</span><span class="sxs-lookup"><span data-stu-id="59cdf-113">0x01</span></span>  | <span data-ttu-id="59cdf-114">El atributo es para uso externo.</span><span class="sxs-lookup"><span data-stu-id="59cdf-114">The attribute is for external use.</span></span> <span data-ttu-id="59cdf-115">Este valor se puede actualizar.</span><span class="sxs-lookup"><span data-stu-id="59cdf-115">This value can be updated.</span></span>  |
| <span data-ttu-id="59cdf-116">iraTemporary</span><span class="sxs-lookup"><span data-stu-id="59cdf-116">iraTemporary</span></span>   | <span data-ttu-id="59cdf-117">0x02</span><span class="sxs-lookup"><span data-stu-id="59cdf-117">0x02</span></span>  | <span data-ttu-id="59cdf-118">La fila no es persistente.</span><span class="sxs-lookup"><span data-stu-id="59cdf-118">The row is not persistent.</span></span> <span data-ttu-id="59cdf-119">Este valor se puede actualizar.</span><span class="sxs-lookup"><span data-stu-id="59cdf-119">This value can be updated.</span></span>          |
| <span data-ttu-id="59cdf-120">iraModified</span><span class="sxs-lookup"><span data-stu-id="59cdf-120">iraModified</span></span>    | <span data-ttu-id="59cdf-121">0x04</span><span class="sxs-lookup"><span data-stu-id="59cdf-121">0x04</span></span>  | <span data-ttu-id="59cdf-122">Se ha actualizado una fila.</span><span class="sxs-lookup"><span data-stu-id="59cdf-122">A row has been updated.</span></span>                                        |
| <span data-ttu-id="59cdf-123">iraInserted</span><span class="sxs-lookup"><span data-stu-id="59cdf-123">iraInserted</span></span>    | <span data-ttu-id="59cdf-124">0x08</span><span class="sxs-lookup"><span data-stu-id="59cdf-124">0x08</span></span>  | <span data-ttu-id="59cdf-125">Se ha insertado una fila.</span><span class="sxs-lookup"><span data-stu-id="59cdf-125">A row has been inserted.</span></span>                                       |
| <span data-ttu-id="59cdf-126">iraMergeFailed</span><span class="sxs-lookup"><span data-stu-id="59cdf-126">iraMergeFailed</span></span> | <span data-ttu-id="59cdf-127">0x0F</span><span class="sxs-lookup"><span data-stu-id="59cdf-127">0x0F</span></span>  | <span data-ttu-id="59cdf-128">Se intentó fusionar mediante combinación con datos no idénticos que no son de clave.</span><span class="sxs-lookup"><span data-stu-id="59cdf-128">An attempt was made to merge with non-identical, non-key data.</span></span> |



 

<span data-ttu-id="59cdf-129">Los bits 6 a 8 están reservados.</span><span class="sxs-lookup"><span data-stu-id="59cdf-129">Bits 6 through 8 are reserved.</span></span>

 

 



