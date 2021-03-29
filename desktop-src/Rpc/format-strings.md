---
title: Cadenas de formato
description: Una cadena de formato es un token interpretado que el motor NDR entiende. Las cadenas de formato se conocen a menudo como MOPs; en esta documentación se usa la cadena de formato de término en todo.
ms.assetid: 548283bd-023a-41dd-b1d0-661305d019e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 563dd9e4145a7d83b2e49f180329c05c1d55155d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776963"
---
# <a name="format-strings"></a><span data-ttu-id="ba753-104">Cadenas de formato</span><span class="sxs-lookup"><span data-stu-id="ba753-104">Format Strings</span></span>

<span data-ttu-id="ba753-105">Una cadena de formato es un token interpretado que el motor NDR entiende.</span><span class="sxs-lookup"><span data-stu-id="ba753-105">A format string is an interpreted token that the NDR engine understands.</span></span> <span data-ttu-id="ba753-106">Las cadenas de formato se conocen a menudo como MOPs; en esta documentación se usa la cadena de formato de término en todo.</span><span class="sxs-lookup"><span data-stu-id="ba753-106">Format strings are often referred to as MOPs; this documentation uses the term format string throughout.</span></span>

<span data-ttu-id="ba753-107">Para ser más precisos, un carácter de formato es un token interpretable individual (atómico).</span><span class="sxs-lookup"><span data-stu-id="ba753-107">To be more precise, a format character is an individual (atomic) interpretable token.</span></span> <span data-ttu-id="ba753-108">Cada carácter de formato tiene un byte de tamaño.</span><span class="sxs-lookup"><span data-stu-id="ba753-108">Each format character is one byte in size.</span></span> <span data-ttu-id="ba753-109">Una cadena de formato es una secuencia de caracteres de formato o caracteres de formato y datos numéricos.</span><span class="sxs-lookup"><span data-stu-id="ba753-109">A format string is a sequence of format characters or format characters and numerical data.</span></span> <span data-ttu-id="ba753-110">El descriptor de términos también se utiliza para asignar nombres a las secuencias comunes. por ejemplo, una cadena de formato de parámetro o un descriptor de parámetro es una cadena de formato que se usa para describir un parámetro de una rutina.</span><span class="sxs-lookup"><span data-stu-id="ba753-110">The term descriptor is also used for naming common sequences; for example, a parameter format string or a parameter descriptor is a format string used to describe a parameter of a routine.</span></span>

<span data-ttu-id="ba753-111">Los caracteres de formato tienen nombres simbólicos propuestos, como FC \_ Long o FC \_ struct.</span><span class="sxs-lookup"><span data-stu-id="ba753-111">Format characters have suggestive symbolic names like FC\_LONG or FC\_STRUCT.</span></span> <span data-ttu-id="ba753-112">Todos los caracteres de cadena de formato usados por MIDL y el motor NDR se definen en el archivo Ndrtypes. h.</span><span class="sxs-lookup"><span data-stu-id="ba753-112">All format string characters used by MIDL and the NDR engine are defined in the Ndrtypes.h file.</span></span>

## <a name="format-string-tables"></a><span data-ttu-id="ba753-113">Tablas de cadenas de formato</span><span class="sxs-lookup"><span data-stu-id="ba753-113">Format String Tables</span></span>

<span data-ttu-id="ba753-114">El motor utiliza dos tablas de cadenas de formato principal: la tabla de cadenas de formato de procedimiento, **\_ \_ MIDL \_ ProcFormatString**, que mantiene los descriptores de procedimiento y la tabla de cadenas de formato de tipo, **\_ \_ MIDL \_ TypeFormatString**, que mantiene los descriptores de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="ba753-114">Two primary format string tables are used by the engine: the procedure format string table, **\_\_MIDL\_ProcFormatString**, that keeps the procedure descriptors; and the type format string table, **\_\_MIDL\_TypeFormatString**, that keeps the data type descriptors.</span></span> <span data-ttu-id="ba753-115">El compilador genera ambos en los archivos de código auxiliar principales ( \* \_ c. c, \* \_ s. c, \* \_ p. c).</span><span class="sxs-lookup"><span data-stu-id="ba753-115">The compiler generates both into the main stub files (\*\_c.c, \*\_s.c, \*\_p.c).</span></span> <span data-ttu-id="ba753-116">La tabla de cadenas de formato de procedimiento la usan principalmente varios intérpretes, pero también se usa para la conversión de búfer, independientemente del modo del compilador.</span><span class="sxs-lookup"><span data-stu-id="ba753-116">The procedure format string table is used mostly by various interpreters but it is also used for the buffer conversion regardless of the compiler mode.</span></span> <span data-ttu-id="ba753-117">La tabla de cadenas de formato de tipo se usa al llamar al motor de NDR principal para indicar los tipos de datos específicos en los que se va a trabajar.</span><span class="sxs-lookup"><span data-stu-id="ba753-117">The type format string table is used when calling the core NDR engine to indicate specific data types to be worked on.</span></span>

## <a name="format-string-notation"></a><span data-ttu-id="ba753-118">Notación de cadena de formato</span><span class="sxs-lookup"><span data-stu-id="ba753-118">Format String Notation</span></span>

<span data-ttu-id="ba753-119">La notación usada en este documento sigue las instrucciones de descripción de programación comunes, con una barra ( \| ) que se usa para indicar construcciones alternativas y corchetes ( \[ \] ) que se usan para indicar elementos opcionales.</span><span class="sxs-lookup"><span data-stu-id="ba753-119">The notation used in this document follows common programming description guidelines, with a bar ( \| ) used to denote alternative constructs and square brackets ( \[ \] ) used to indicate optional elements.</span></span> <span data-ttu-id="ba753-120">Las cadenas de formato suelen apilarse para mejorar la legibilidad (responsabilidad).</span><span class="sxs-lookup"><span data-stu-id="ba753-120">Format strings are frequently stacked up for readability (accountability).</span></span> <span data-ttu-id="ba753-121">En todo este documento, FC denota un solo carácter de formato.</span><span class="sxs-lookup"><span data-stu-id="ba753-121">Throughout this document, FC denotes a single format character.</span></span> <span data-ttu-id="ba753-122">Los caracteres de formato se presentan en MAYÚSCULAs, con sus nombres simbólicos reales.</span><span class="sxs-lookup"><span data-stu-id="ba753-122">Format characters are presented in all CAPS, using their actual symbolic names.</span></span> <span data-ttu-id="ba753-123">Otros campos arbitrarios se representan mediante un nombre y un tamaño.</span><span class="sxs-lookup"><span data-stu-id="ba753-123">Other arbitrary fields are represented by a name and a size.</span></span>

<span data-ttu-id="ba753-124">Los corchetes angulares ( <> ) se utilizan para indicar los tamaños de los descriptores.</span><span class="sxs-lookup"><span data-stu-id="ba753-124">Angle brackets ( <> ) are used to denote sizes of the descriptors.</span></span> <span data-ttu-id="ba753-125">Se emplean las convenciones que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="ba753-125">The conventions shown in the following table are employed.</span></span>



| <span data-ttu-id="ba753-126">Notación</span><span class="sxs-lookup"><span data-stu-id="ba753-126">Notation</span></span>     | <span data-ttu-id="ba753-127">Significado</span><span class="sxs-lookup"><span data-stu-id="ba753-127">Meaning</span></span>                                                   |
|--------------|-----------------------------------------------------------|
| <span data-ttu-id="ba753-128"><*n*></span><span class="sxs-lookup"><span data-stu-id="ba753-128"><*n*></span></span>  | <span data-ttu-id="ba753-129">El tamaño del descriptor es n bytes.</span><span class="sxs-lookup"><span data-stu-id="ba753-129">The size of descriptor is n bytes.</span></span>                        |
| <>     | <span data-ttu-id="ba753-130">El tamaño del descriptor varía.</span><span class="sxs-lookup"><span data-stu-id="ba753-130">The size of descriptor varies.</span></span>                            |
| <span data-ttu-id="ba753-131">{<>}\*</span><span class="sxs-lookup"><span data-stu-id="ba753-131">{<>}\*</span></span> | <span data-ttu-id="ba753-132">El descriptor se repite un número de veces (0, 1, 2...).</span><span class="sxs-lookup"><span data-stu-id="ba753-132">The descriptor is repeated any number of times (0,1,2 …).</span></span> |



 

<span data-ttu-id="ba753-133">Los siguientes caracteres de formato tienen un significado especial.</span><span class="sxs-lookup"><span data-stu-id="ba753-133">The following format characters have a special meaning.</span></span>



| <span data-ttu-id="ba753-134">Carácter</span><span class="sxs-lookup"><span data-stu-id="ba753-134">Character</span></span> | <span data-ttu-id="ba753-135">Significado</span><span class="sxs-lookup"><span data-stu-id="ba753-135">Meaning</span></span>                                   |
|-----------|-------------------------------------------|
| <span data-ttu-id="ba753-136">final de FC \_</span><span class="sxs-lookup"><span data-stu-id="ba753-136">FC\_END</span></span>   | <span data-ttu-id="ba753-137">Indica el final de algunas cadenas de formato.</span><span class="sxs-lookup"><span data-stu-id="ba753-137">Indicates the end of some format strings.</span></span> |
| <span data-ttu-id="ba753-138">Pad de FC \_</span><span class="sxs-lookup"><span data-stu-id="ba753-138">FC\_PAD</span></span>   | <span data-ttu-id="ba753-139">Carácter controlador no interpretado.</span><span class="sxs-lookup"><span data-stu-id="ba753-139">Uninterpreted pad character.</span></span>              |



 

 

 




