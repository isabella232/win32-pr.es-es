---
description: Si este bit se establece para un control de texto estático, el control intenta dar formato automáticamente al texto mostrado como un número que representa un recuento de bytes.
ms.assetid: acf76fff-b7a4-456b-91b9-eb3087879d7b
title: Formatear atributo de control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d7fa656b81272b8ac60985d3dac0416c0f81bef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275927"
---
# <a name="formatsize-control-attribute"></a><span data-ttu-id="48b5a-103">Formatear atributo de control</span><span class="sxs-lookup"><span data-stu-id="48b5a-103">FormatSize Control Attribute</span></span>

<span data-ttu-id="48b5a-104">Si este bit se establece para un control de texto estático, el control intenta dar formato automáticamente al texto mostrado como un número que representa un recuento de bytes.</span><span class="sxs-lookup"><span data-stu-id="48b5a-104">If this bit is set for a static text control, the control automatically attempts to format the displayed text as a number that represents a count of bytes.</span></span> <span data-ttu-id="48b5a-105">Para que el formato sea correcto, el texto del control debe establecerse en una cadena que represente un número expresado en unidades de 512 bytes.</span><span class="sxs-lookup"><span data-stu-id="48b5a-105">For proper formatting, the control's text must be set to a string that represents a number expressed in units of 512 bytes.</span></span> <span data-ttu-id="48b5a-106">A continuación, se da formato al valor mostrado en kilobytes (KB), megabytes (MB) o gigabytes (GB) y se muestra con la cadena adecuada que representa las unidades.</span><span class="sxs-lookup"><span data-stu-id="48b5a-106">The displayed value is then formatted in kilobytes (KB), megabytes (MB), or gigabytes (GB), and displayed with the appropriate string that represents the units.</span></span> <span data-ttu-id="48b5a-107">Para obtener más información, vea [control de texto](text-control.md).</span><span class="sxs-lookup"><span data-stu-id="48b5a-107">For more information, see [Text Control](text-control.md).</span></span>



| <span data-ttu-id="48b5a-108">Valor numérico del texto original</span><span class="sxs-lookup"><span data-stu-id="48b5a-108">Numerical value of original text</span></span> | <span data-ttu-id="48b5a-109">Cadena de unidad usada</span><span class="sxs-lookup"><span data-stu-id="48b5a-109">Unit string used</span></span> |
|----------------------------------|------------------|
| <span data-ttu-id="48b5a-110">Menor que 20480</span><span class="sxs-lookup"><span data-stu-id="48b5a-110">Less than 20480</span></span>                  | <span data-ttu-id="48b5a-111">KB</span><span class="sxs-lookup"><span data-stu-id="48b5a-111">KB</span></span>               |
| <span data-ttu-id="48b5a-112">Menor que 20971520</span><span class="sxs-lookup"><span data-stu-id="48b5a-112">Less than 20971520</span></span>               | <span data-ttu-id="48b5a-113">MB</span><span class="sxs-lookup"><span data-stu-id="48b5a-113">MB</span></span>               |
| <span data-ttu-id="48b5a-114">Menor que 10737418240</span><span class="sxs-lookup"><span data-stu-id="48b5a-114">Less than 10737418240</span></span>            | <span data-ttu-id="48b5a-115">GB</span><span class="sxs-lookup"><span data-stu-id="48b5a-115">GB</span></span>               |



 

## <a name="valid-controls"></a><span data-ttu-id="48b5a-116">Controles válidos</span><span class="sxs-lookup"><span data-stu-id="48b5a-116">Valid Controls</span></span>



| <span data-ttu-id="48b5a-117">Decimal</span><span class="sxs-lookup"><span data-stu-id="48b5a-117">Decimal</span></span> | <span data-ttu-id="48b5a-118">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="48b5a-118">Hexadecimal</span></span> | <span data-ttu-id="48b5a-119">Control</span><span class="sxs-lookup"><span data-stu-id="48b5a-119">Control</span></span>                          |
|---------|-------------|----------------------------------|
| <span data-ttu-id="48b5a-120">524 288</span><span class="sxs-lookup"><span data-stu-id="48b5a-120">524288</span></span>  | <span data-ttu-id="48b5a-121">0x00080000</span><span class="sxs-lookup"><span data-stu-id="48b5a-121">0x00080000</span></span>  | <span data-ttu-id="48b5a-122">msidbControlAttributesFormatSize</span><span class="sxs-lookup"><span data-stu-id="48b5a-122">msidbControlAttributesFormatSize</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="48b5a-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="48b5a-123">Remarks</span></span>

<span data-ttu-id="48b5a-124">Para establecer este atributo en un control, incluya los bits de formato en la columna Attributes del registro del control en la [tabla de control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="48b5a-124">To set this attribute on a control, include the FormatSize bits in the Attributes column of the control's record in the [Control Table](control-table.md).</span></span> <span data-ttu-id="48b5a-125">El texto del control debe establecerse en una cadena que represente un número expresado en unidades de 512 bytes.</span><span class="sxs-lookup"><span data-stu-id="48b5a-125">The control's text must be set to a string representing a number expressed in units of 512 bytes.</span></span> <span data-ttu-id="48b5a-126">El texto de las cadenas de unidad se define en la [tabla UIText](uitext-table.md).</span><span class="sxs-lookup"><span data-stu-id="48b5a-126">The text of the unit strings are defined in the [UIText Table](uitext-table.md).</span></span> <span data-ttu-id="48b5a-127">La posición de la cadena de unidad se controla mediante la propiedad [**LeftUnit**](leftunit.md) .</span><span class="sxs-lookup"><span data-stu-id="48b5a-127">The positioning of the unit string is controlled by the [**LeftUnit**](leftunit.md) Property.</span></span> <span data-ttu-id="48b5a-128">Si la propiedad **LeftUnit** se define como cualquier valor, la cadena de unidad aparece delante del valor numérico.</span><span class="sxs-lookup"><span data-stu-id="48b5a-128">If the **LeftUnit** Property is defined to be any value, the unit string appears before the numerical value.</span></span> <span data-ttu-id="48b5a-129">Si en el texto asociado al control aparece algo que no sea un carácter numérico, el valor mostrado es indefinido.</span><span class="sxs-lookup"><span data-stu-id="48b5a-129">If anything other than numerical characters appears in the text associated with the control, the displayed value is undefined.</span></span>

<span data-ttu-id="48b5a-130">En tiempo de ejecución, el instalador resuelve la propiedad [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md) en el número total de bytes necesarios para la instalación en unidades de 512.</span><span class="sxs-lookup"><span data-stu-id="48b5a-130">At run time, the installer resolves the [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md) Property to the total number of bytes required for the installation in units of 512.</span></span> <span data-ttu-id="48b5a-131">Se puede usar un control de texto estático con el bit Formatme para dar formato y etiquetar automáticamente el número total de bytes necesarios para la instalación en KB, MB o GB, según corresponda.</span><span class="sxs-lookup"><span data-stu-id="48b5a-131">A static text control with FormatSize bit can be used to automatically format and label the total number of bytes required for the installation in KB, MB, or GB as appropriate.</span></span> <span data-ttu-id="48b5a-132">Para los fines de este ejemplo, suponga que el número total de bytes es 18.336.768.</span><span class="sxs-lookup"><span data-stu-id="48b5a-132">For the purposes of this example, assume the total number of bytes is 18,336,768.</span></span> <span data-ttu-id="48b5a-133">El instalador establece el valor de la propiedad PrimaryVolumeSpaceRequired en 18.336.768 dividido entre 512 o 35.814.</span><span class="sxs-lookup"><span data-stu-id="48b5a-133">The installer sets the value of the PrimaryVolumeSpaceRequired property to 18,336,768 divided by 512, or 35,814.</span></span> <span data-ttu-id="48b5a-134">El número que muestra el control de texto con Formatme sería 17MB.</span><span class="sxs-lookup"><span data-stu-id="48b5a-134">The number displayed by the text control with FormatSize would be 17MB.</span></span>

<span data-ttu-id="48b5a-135">Los valores numéricos del texto original se proporcionan en unidades de 512.</span><span class="sxs-lookup"><span data-stu-id="48b5a-135">The numerical values of the original text are given in units of 512.</span></span> <span data-ttu-id="48b5a-136">En la tabla anterior, la cadena 20.480 corresponde a la cadena de KB porque 20.480 veces 512 produce un resultado de 10.485.760 bytes o de 10.240 KB.</span><span class="sxs-lookup"><span data-stu-id="48b5a-136">In the table above, the string 20,480 corresponds to the KB string because 20,480 times 512 yields a result of 10,485,760 bytes or 10,240 KB.</span></span>

<span data-ttu-id="48b5a-137">Las cadenas de unidad enumeradas en la tabla anterior hacen referencia a las claves de la [tabla UIText](uitext-table.md), donde se define el texto de la cadena de unidad.</span><span class="sxs-lookup"><span data-stu-id="48b5a-137">The unit strings listed in the previous table refer to keys in the [UIText Table](uitext-table.md), where the text of the unit string is defined.</span></span>

<span data-ttu-id="48b5a-138">La posición de la cadena de unidad se controla mediante la propiedad [**LeftUnit**](leftunit.md) .</span><span class="sxs-lookup"><span data-stu-id="48b5a-138">The positioning of the unit string is controlled by the [**LeftUnit**](leftunit.md) Property.</span></span> <span data-ttu-id="48b5a-139">Si la propiedad **LeftUnit** se define como cualquier valor, la cadena de unidad aparece delante del valor numérico.</span><span class="sxs-lookup"><span data-stu-id="48b5a-139">If the **LeftUnit** Property is defined to be any value, the unit string appears before the numerical value.</span></span>

<span data-ttu-id="48b5a-140">Si en el texto asociado al control aparece algo que no sea un carácter numérico, el valor mostrado es indefinido.</span><span class="sxs-lookup"><span data-stu-id="48b5a-140">If anything other than numerical characters appears in the text associated with the control, the displayed value is undefined.</span></span>

<span data-ttu-id="48b5a-141">Para obtener más información, vea [controles](controls.md)y [atributos de control](control-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="48b5a-141">For more information, see [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



