---
description: La tabla UIText contiene las versiones localizadas de algunas de las cadenas usadas en la interfaz de usuario. Estas cadenas no forman parte de ninguna otra tabla. La tabla UIText es para las cadenas que no tienen ninguna posición lógica en ninguna otra tabla.
ms.assetid: 2965e3a8-2cbf-4445-963b-ec2040692106
title: Tabla UIText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5fe8bbdec694511103636508d229ab0d2e40afc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153737"
---
# <a name="uitext-table"></a><span data-ttu-id="f8f80-105">Tabla UIText</span><span class="sxs-lookup"><span data-stu-id="f8f80-105">UIText Table</span></span>

<span data-ttu-id="f8f80-106">La tabla UIText contiene las versiones localizadas de algunas de las cadenas usadas en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="f8f80-106">The UIText table contains the localized versions of some of the strings used in the user interface.</span></span> <span data-ttu-id="f8f80-107">Estas cadenas no forman parte de ninguna otra tabla.</span><span class="sxs-lookup"><span data-stu-id="f8f80-107">These strings are not part of any other table.</span></span> <span data-ttu-id="f8f80-108">La tabla UIText es para las cadenas que no tienen ninguna posición lógica en ninguna otra tabla.</span><span class="sxs-lookup"><span data-stu-id="f8f80-108">The UIText table is for strings that have no logical place in any other table.</span></span>

<span data-ttu-id="f8f80-109">La tabla UIText tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="f8f80-109">The UIText table has the following columns.</span></span>



| <span data-ttu-id="f8f80-110">Columna</span><span class="sxs-lookup"><span data-stu-id="f8f80-110">Column</span></span> | <span data-ttu-id="f8f80-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="f8f80-111">Type</span></span>                         | <span data-ttu-id="f8f80-112">Clave</span><span class="sxs-lookup"><span data-stu-id="f8f80-112">Key</span></span> | <span data-ttu-id="f8f80-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="f8f80-113">Nullable</span></span> |
|--------|------------------------------|-----|----------|
| <span data-ttu-id="f8f80-114">Clave</span><span class="sxs-lookup"><span data-stu-id="f8f80-114">Key</span></span>    | [<span data-ttu-id="f8f80-115">Identificador</span><span class="sxs-lookup"><span data-stu-id="f8f80-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="f8f80-116">Y</span><span class="sxs-lookup"><span data-stu-id="f8f80-116">Y</span></span>   | <span data-ttu-id="f8f80-117">N</span><span class="sxs-lookup"><span data-stu-id="f8f80-117">N</span></span>        |
| <span data-ttu-id="f8f80-118">Texto</span><span class="sxs-lookup"><span data-stu-id="f8f80-118">Text</span></span>   | [<span data-ttu-id="f8f80-119">Texto</span><span class="sxs-lookup"><span data-stu-id="f8f80-119">Text</span></span>](text.md)             | <span data-ttu-id="f8f80-120">N</span><span class="sxs-lookup"><span data-stu-id="f8f80-120">N</span></span>   | <span data-ttu-id="f8f80-121">Y</span><span class="sxs-lookup"><span data-stu-id="f8f80-121">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="f8f80-122">Columnas</span><span class="sxs-lookup"><span data-stu-id="f8f80-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="f8f80-123"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Clave</span><span class="sxs-lookup"><span data-stu-id="f8f80-123"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Key</span></span>
</dt> <dd>

<span data-ttu-id="f8f80-124">Una clave única que identifica la cadena determinada.</span><span class="sxs-lookup"><span data-stu-id="f8f80-124">A unique key that identifies the particular string.</span></span>

</dd> <dt>

<span data-ttu-id="f8f80-125"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Negrita</span><span class="sxs-lookup"><span data-stu-id="f8f80-125"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text</span></span>
</dt> <dd>

<span data-ttu-id="f8f80-126">Versión localizada de la cadena.</span><span class="sxs-lookup"><span data-stu-id="f8f80-126">The localized version of the string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f8f80-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f8f80-127">Remarks</span></span>

<span data-ttu-id="f8f80-128">Algunos controles usan la tabla UIText como origen de cadenas.</span><span class="sxs-lookup"><span data-stu-id="f8f80-128">Some controls use the UIText table as a source of strings.</span></span> <span data-ttu-id="f8f80-129">Para obtener información sobre qué cadenas son necesarias en esta tabla para cada control concreto, vea los controles individuales en la referencia de la [interfaz de usuario](user-interface-reference.md).</span><span class="sxs-lookup"><span data-stu-id="f8f80-129">For information about which strings are required in this table for each particular control, see the individual controls in the [User Interface Reference](user-interface-reference.md).</span></span>

## <a name="validation"></a><span data-ttu-id="f8f80-130">Validación</span><span class="sxs-lookup"><span data-stu-id="f8f80-130">Validation</span></span>

<dl>

[<span data-ttu-id="f8f80-131">ICE03</span><span class="sxs-lookup"><span data-stu-id="f8f80-131">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="f8f80-132">ICE06</span><span class="sxs-lookup"><span data-stu-id="f8f80-132">ICE06</span></span>](ice06.md)  
</dl>

 

 



