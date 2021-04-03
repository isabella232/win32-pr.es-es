---
description: En este tema se describen los tipos de formato de las cadenas que se usan para crear la imagen de formato para una cadena de hora. Cada imagen de formato consta de una combinación de una cadena de cada uno de los tipos de formato.
ms.assetid: a5e87d88-4037-4302-99b7-179bfb03fac3
title: Imágenes con formato de hora, minuto y segundo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 589c04fea0d6ce2f522436c30c39c873e3a7165e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083478"
---
# <a name="hour-minute-and-second-format-pictures"></a><span data-ttu-id="55ff2-104">Imágenes con formato de hora, minuto y segundo</span><span class="sxs-lookup"><span data-stu-id="55ff2-104">Hour, Minute, and Second Format Pictures</span></span>

<span data-ttu-id="55ff2-105">En este tema se describen los tipos de formato de las cadenas que se usan para crear la imagen de formato para una cadena de hora.</span><span class="sxs-lookup"><span data-stu-id="55ff2-105">This topic describes the format types for strings used to compose the format picture for a time string.</span></span> <span data-ttu-id="55ff2-106">Cada imagen de formato consta de una combinación de una cadena de cada uno de los tipos de formato.</span><span class="sxs-lookup"><span data-stu-id="55ff2-106">Each format picture consists of a combination of one string of each of the format types.</span></span>

> [!Note]  
> <span data-ttu-id="55ff2-107">En los tipos de formato, las letras "m", "s" y "t" deben estar en minúsculas, y la letra "h" debe estar en minúsculas para indicar el reloj de 12 horas o mayúsculas ("H") para indicar el reloj de 24 horas.</span><span class="sxs-lookup"><span data-stu-id="55ff2-107">In the format types, the letters "m", "s", and "t" must be lowercase, and the letter "h" must be lowercase to denote the 12-hour clock or uppercase ("H") to denote the 24-hour clock.</span></span>

<span data-ttu-id="55ff2-108">Las comillas simples se pueden usar para marcar los caracteres que se deben mostrar exactamente como se especifican.</span><span class="sxs-lookup"><span data-stu-id="55ff2-108">Single quotation marks can be used to mark characters that should be displayed exactly as specified.</span></span> <span data-ttu-id="55ff2-109">Si la aplicación debe mostrar una comilla simple, debe colocar dos comillas simples en una fila.</span><span class="sxs-lookup"><span data-stu-id="55ff2-109">If the application must display a single quotation mark, it should place two single quotation marks in a row.</span></span> <span data-ttu-id="55ff2-110">Por ejemplo, "ABC", "bar", se muestra como "abc'bar".</span><span class="sxs-lookup"><span data-stu-id="55ff2-110">For example, 'abc''bar', is displayed as "abc'bar".</span></span>

<span data-ttu-id="55ff2-111">En la tabla siguiente se definen los tipos de formato que se usan para representar las horas.</span><span class="sxs-lookup"><span data-stu-id="55ff2-111">The following table defines the format types used to represent hours.</span></span>

| <span data-ttu-id="55ff2-112">String</span><span class="sxs-lookup"><span data-stu-id="55ff2-112">String</span></span> | <span data-ttu-id="55ff2-113">Significado</span><span class="sxs-lookup"><span data-stu-id="55ff2-113">Meaning</span></span>                                                             |
|--------|---------------------------------------------------------------------|
| <span data-ttu-id="55ff2-114">h</span><span class="sxs-lookup"><span data-stu-id="55ff2-114">h</span></span>      | <span data-ttu-id="55ff2-115">Horas sin ceros a la izquierda para las horas de un solo dígito (reloj de 12 horas).</span><span class="sxs-lookup"><span data-stu-id="55ff2-115">Hours without leading zeros for single-digit hours (12-hour clock).</span></span> |
| <span data-ttu-id="55ff2-116">hh</span><span class="sxs-lookup"><span data-stu-id="55ff2-116">hh</span></span>     | <span data-ttu-id="55ff2-117">Horas con ceros a la izquierda para las horas de un solo dígito (reloj de 12 horas).</span><span class="sxs-lookup"><span data-stu-id="55ff2-117">Hours with leading zeros for single-digit hours (12-hour clock).</span></span>    |
| <span data-ttu-id="55ff2-118">H</span><span class="sxs-lookup"><span data-stu-id="55ff2-118">H</span></span>      | <span data-ttu-id="55ff2-119">Horas sin ceros a la izquierda para las horas de un solo dígito (reloj de 24 horas).</span><span class="sxs-lookup"><span data-stu-id="55ff2-119">Hours without leading zeros for single-digit hours (24-hour clock).</span></span> |
| <span data-ttu-id="55ff2-120">HH</span><span class="sxs-lookup"><span data-stu-id="55ff2-120">HH</span></span>     | <span data-ttu-id="55ff2-121">Horas con ceros a la izquierda para las horas de un solo dígito (reloj de 24 horas).</span><span class="sxs-lookup"><span data-stu-id="55ff2-121">Hours with leading zeros for single-digit hours (24-hour clock).</span></span>    |

<span data-ttu-id="55ff2-122">En la tabla siguiente se definen los tipos de formato que se usan para representar los minutos.</span><span class="sxs-lookup"><span data-stu-id="55ff2-122">The following table defines the format types used to represent minutes.</span></span>

| <span data-ttu-id="55ff2-123">String</span><span class="sxs-lookup"><span data-stu-id="55ff2-123">String</span></span> | <span data-ttu-id="55ff2-124">Significado</span><span class="sxs-lookup"><span data-stu-id="55ff2-124">Meaning</span></span>                                                 |
|--------|---------------------------------------------------------|
| <span data-ttu-id="55ff2-125">m</span><span class="sxs-lookup"><span data-stu-id="55ff2-125">m</span></span>      | <span data-ttu-id="55ff2-126">Minutos sin ceros a la izquierda para los minutos con un solo dígito.</span><span class="sxs-lookup"><span data-stu-id="55ff2-126">Minutes without leading zeros for single-digit minutes.</span></span> |
| <span data-ttu-id="55ff2-127">MM</span><span class="sxs-lookup"><span data-stu-id="55ff2-127">mm</span></span>     | <span data-ttu-id="55ff2-128">Minutos con ceros a la izquierda para los minutos con un solo dígito.</span><span class="sxs-lookup"><span data-stu-id="55ff2-128">Minutes with leading zeros for single-digit minutes.</span></span>    |

<span data-ttu-id="55ff2-129">En la tabla siguiente se definen los tipos de formato que se usan para representar los segundos.</span><span class="sxs-lookup"><span data-stu-id="55ff2-129">The following table defines the format types used to represent seconds.</span></span>

| <span data-ttu-id="55ff2-130">String</span><span class="sxs-lookup"><span data-stu-id="55ff2-130">String</span></span> | <span data-ttu-id="55ff2-131">Significado</span><span class="sxs-lookup"><span data-stu-id="55ff2-131">Meaning</span></span>                                                 |
|--------|---------------------------------------------------------|
| <span data-ttu-id="55ff2-132">s</span><span class="sxs-lookup"><span data-stu-id="55ff2-132">s</span></span>      | <span data-ttu-id="55ff2-133">Segundos sin ceros a la izquierda para los segundos de un solo dígito.</span><span class="sxs-lookup"><span data-stu-id="55ff2-133">Seconds without leading zeros for single-digit seconds.</span></span> |
| <span data-ttu-id="55ff2-134">ss</span><span class="sxs-lookup"><span data-stu-id="55ff2-134">ss</span></span>     | <span data-ttu-id="55ff2-135">Segundos con ceros a la izquierda para los segundos de un solo dígito.</span><span class="sxs-lookup"><span data-stu-id="55ff2-135">Seconds with leading zeros for single-digit seconds.</span></span>    |

<span data-ttu-id="55ff2-136">En la tabla siguiente se definen los tipos de formato que se usan para representar un marcador de tiempo.</span><span class="sxs-lookup"><span data-stu-id="55ff2-136">The following table defines the format types used to represent a time marker.</span></span>

| <span data-ttu-id="55ff2-137">String</span><span class="sxs-lookup"><span data-stu-id="55ff2-137">String</span></span> | <span data-ttu-id="55ff2-138">Significado</span><span class="sxs-lookup"><span data-stu-id="55ff2-138">Meaning</span></span>|
| ---    | ---    |
| <span data-ttu-id="55ff2-139">t</span><span class="sxs-lookup"><span data-stu-id="55ff2-139">t</span></span>      | <span data-ttu-id="55ff2-140">Cadena de marcador de tiempo de un carácter.</span><span class="sxs-lookup"><span data-stu-id="55ff2-140">One-character time marker string.</span></span><br /><span data-ttu-id="55ff2-141">**Nota:** No se recomienda usar este formato con determinados idiomas, como japonés (Japón).</span><span class="sxs-lookup"><span data-stu-id="55ff2-141">**Note:** This format is not recommended for use with certain languages, such as Japanese (Japan).</span></span> <span data-ttu-id="55ff2-142">Con este formato, una aplicación siempre toma el primer carácter de la cadena de marcador de hora, definida por [LOCALE_S1159](locale-s1159.md) (AM) y [LOCALE_S2359](locale-s2359.md) (PM).</span><span class="sxs-lookup"><span data-stu-id="55ff2-142">With this format, an application always takes the first character from the time marker string, defined by [LOCALE_S1159](locale-s1159.md) (AM) and [LOCALE_S2359](locale-s2359.md) (PM).</span></span> <span data-ttu-id="55ff2-143">Por esta razón, la aplicación puede crear un formato incorrecto con la misma cadena que se usa para AM y PM.</span><span class="sxs-lookup"><span data-stu-id="55ff2-143">Because of this, the application can create incorrect formatting with the same string used for both AM and PM.</span></span>|
| <span data-ttu-id="55ff2-144">tt</span><span class="sxs-lookup"><span data-stu-id="55ff2-144">tt</span></span>     | <span data-ttu-id="55ff2-145">Cadena de marcador de tiempo de varios caracteres.</span><span class="sxs-lookup"><span data-stu-id="55ff2-145">Multi-character time marker string.</span></span> |
