---
description: La tabla CheckBox muestra los valores de las casillas.
ms.assetid: 6881f358-74af-4160-ac69-36e848865ac0
title: Tabla CheckBox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3600b741543a88e7ded71cd385a56b499c8ef516
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666999"
---
# <a name="checkbox-table"></a><span data-ttu-id="cb292-103">Tabla CheckBox</span><span class="sxs-lookup"><span data-stu-id="cb292-103">CheckBox Table</span></span>

<span data-ttu-id="cb292-104">La tabla CheckBox muestra los valores de las casillas.</span><span class="sxs-lookup"><span data-stu-id="cb292-104">The CheckBox table lists the values for the check boxes.</span></span>

<span data-ttu-id="cb292-105">La tabla CheckBox tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="cb292-105">The CheckBox table has the following columns.</span></span>



| <span data-ttu-id="cb292-106">Columna</span><span class="sxs-lookup"><span data-stu-id="cb292-106">Column</span></span>   | <span data-ttu-id="cb292-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="cb292-107">Type</span></span>                         | <span data-ttu-id="cb292-108">Clave</span><span class="sxs-lookup"><span data-stu-id="cb292-108">Key</span></span> | <span data-ttu-id="cb292-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="cb292-109">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="cb292-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cb292-110">Property</span></span> | [<span data-ttu-id="cb292-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="cb292-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="cb292-112">Y</span><span class="sxs-lookup"><span data-stu-id="cb292-112">Y</span></span>   | <span data-ttu-id="cb292-113">N</span><span class="sxs-lookup"><span data-stu-id="cb292-113">N</span></span>        |
| <span data-ttu-id="cb292-114">Value</span><span class="sxs-lookup"><span data-stu-id="cb292-114">Value</span></span>    | [<span data-ttu-id="cb292-115">Formatea</span><span class="sxs-lookup"><span data-stu-id="cb292-115">Formatted</span></span>](formatted.md)   | <span data-ttu-id="cb292-116">N</span><span class="sxs-lookup"><span data-stu-id="cb292-116">N</span></span>   | <span data-ttu-id="cb292-117">Y</span><span class="sxs-lookup"><span data-stu-id="cb292-117">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="cb292-118">Columnas</span><span class="sxs-lookup"><span data-stu-id="cb292-118">Columns</span></span>

<dl> <dt>

<span data-ttu-id="cb292-119"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propiedad</span><span class="sxs-lookup"><span data-stu-id="cb292-119"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="cb292-120">Propiedad con nombre que se va a asociar a este elemento.</span><span class="sxs-lookup"><span data-stu-id="cb292-120">A named property to be tied to this item.</span></span>

</dd> <dt>

<span data-ttu-id="cb292-121"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor</span><span class="sxs-lookup"><span data-stu-id="cb292-121"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="cb292-122">Cadena de valor asociada a este elemento.</span><span class="sxs-lookup"><span data-stu-id="cb292-122">The value string associated with this item.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cb292-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cb292-123">Remarks</span></span>

<span data-ttu-id="cb292-124">Si la casilla está activada, la propiedad correspondiente se establece en el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="cb292-124">If the check box is selected, then the corresponding property is set to the specified value.</span></span> <span data-ttu-id="cb292-125">Si no hay ningún valor especificado o esta tabla no existe, la propiedad se establece en su valor original cuando la casilla está activada.</span><span class="sxs-lookup"><span data-stu-id="cb292-125">If there is no value specified or this table does not exist, then the property is set to its original value when the check box is selected.</span></span> <span data-ttu-id="cb292-126">Si el valor original es null, la propiedad se establece en "1".</span><span class="sxs-lookup"><span data-stu-id="cb292-126">If the original value is null, the property is set to "1".</span></span>

<span data-ttu-id="cb292-127">La función [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) da formato al contenido de la columna de valor cuando se crea el control.</span><span class="sxs-lookup"><span data-stu-id="cb292-127">The contents of the Value column are formatted by the [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) function when the control is created.</span></span> <span data-ttu-id="cb292-128">Por lo tanto, puede contener cualquier expresión que la función **MsiFormatRecord** pueda interpretar.</span><span class="sxs-lookup"><span data-stu-id="cb292-128">Therefore, it can contain any expression that the **MsiFormatRecord** function can interpret.</span></span> <span data-ttu-id="cb292-129">Solo se da formato a la columna valor cuando se crea el control y no se actualiza si una propiedad implicada en una expresión se modifica durante la vida del control.</span><span class="sxs-lookup"><span data-stu-id="cb292-129">The Value column is formatted only when the control is created, and it is not updated if a property involved in an expression is modified during the life of the control.</span></span>

## <a name="validation"></a><span data-ttu-id="cb292-130">Validación</span><span class="sxs-lookup"><span data-stu-id="cb292-130">Validation</span></span>

<dl>

[<span data-ttu-id="cb292-131">ICE03</span><span class="sxs-lookup"><span data-stu-id="cb292-131">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="cb292-132">ICE06</span><span class="sxs-lookup"><span data-stu-id="cb292-132">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="cb292-133">ICE46</span><span class="sxs-lookup"><span data-stu-id="cb292-133">ICE46</span></span>](ice46.md)  
</dl>

 

 



