---
title: Generando interfaz UUID
description: Generando identificadores únicos universales (UUID) de interfaz y usando Uuidgen.
ms.assetid: a973b7f9-71c5-46a0-aa0c-51f150560dbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68c5f727ed3e37139d4da50f84c3929bff333156
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775739"
---
# <a name="generating-interface-uuids"></a><span data-ttu-id="d29b4-103">Generando interfaz UUID</span><span class="sxs-lookup"><span data-stu-id="d29b4-103">Generating Interface UUIDs</span></span>

<span data-ttu-id="d29b4-104">En esta sección se ofrece información sobre los identificadores únicos universales (UUID) y la utilidad uuidgen en los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="d29b4-104">This section presents information on Universal Unique Identifiers (UUIDs) and the Uuidgen utility in the following topics:</span></span>

-   [<span data-ttu-id="d29b4-105">¿Qué es un UUID?</span><span class="sxs-lookup"><span data-stu-id="d29b4-105">What is a UUID?</span></span>](#what-is-a-uuid)
-   [<span data-ttu-id="d29b4-106">Usar uuidgen</span><span class="sxs-lookup"><span data-stu-id="d29b4-106">Using Uuidgen</span></span>](#using-uuidgen)

## <a name="what-is-a-uuid"></a><span data-ttu-id="d29b4-107">¿Qué es un UUID?</span><span class="sxs-lookup"><span data-stu-id="d29b4-107">What is a UUID?</span></span>

<span data-ttu-id="d29b4-108">Todas las interfaces se deben identificar de forma única en una red para que los clientes puedan encontrarlas.</span><span class="sxs-lookup"><span data-stu-id="d29b4-108">All interfaces must be uniquely identified on a network so that clients can find them.</span></span> <span data-ttu-id="d29b4-109">En redes pequeñas, el nombre de la interfaz solo puede ser suficiente para identificarla.</span><span class="sxs-lookup"><span data-stu-id="d29b4-109">On small networks, the interface's name alone may be sufficient to identify it.</span></span> <span data-ttu-id="d29b4-110">Sin embargo, esto no suele ser factible en redes de gran tamaño.</span><span class="sxs-lookup"><span data-stu-id="d29b4-110">However, that is usually not feasible on large networks.</span></span> <span data-ttu-id="d29b4-111">Por lo tanto, los desarrolladores suelen asignar un identificador único universal (UUID, intercambiable con el término GUID o un identificador único global) a cada interfaz.</span><span class="sxs-lookup"><span data-stu-id="d29b4-111">Therefore, developers typically assign a Universal Unique Identifier (UUID, interchangeable with the term GUID, or Globally Unique Identifier) to each interface.</span></span> <span data-ttu-id="d29b4-112">Un UUID es una cadena que contiene un conjunto de dígitos hexadecimales.</span><span class="sxs-lookup"><span data-stu-id="d29b4-112">A UUID is a string that contains a set of hexadecimal digits.</span></span> <span data-ttu-id="d29b4-113">Cada interfaz tiene un UUID diferente.</span><span class="sxs-lookup"><span data-stu-id="d29b4-113">Each interface has a different UUID.</span></span> <span data-ttu-id="d29b4-114">Para obtener más información, consulte [UUID de cadena](string-uuid.md).</span><span class="sxs-lookup"><span data-stu-id="d29b4-114">For details, see [String UUID](string-uuid.md).</span></span>

<span data-ttu-id="d29b4-115">La representación textual de un UUID es una cadena que consta de 8 dígitos hexadecimales seguidos de un guión, seguido de tres grupos separados por guiones de 4 dígitos hexadecimales, seguidos de un guión, seguido de 12 dígitos hexadecimales.</span><span class="sxs-lookup"><span data-stu-id="d29b4-115">The textual representation of a UUID is a string consisting of 8 hexadecimal digits followed by a hyphen, followed by three hyphen-separated groups of 4 hexadecimal digits, followed by a hyphen, followed by 12 hexadecimal digits.</span></span> <span data-ttu-id="d29b4-116">El ejemplo siguiente es una cadena de UUID válida:</span><span class="sxs-lookup"><span data-stu-id="d29b4-116">The following example is a valid UUID string:</span></span>

<span data-ttu-id="d29b4-117">ba209999-0c6c-11d2-97cf-00c04f8eea45</span><span class="sxs-lookup"><span data-stu-id="d29b4-117">ba209999-0c6c-11d2-97cf-00c04f8eea45</span></span>

<span data-ttu-id="d29b4-118">Los UUID vacíos se denominan un UUID nulo en lugar de un UUID **nulo** .</span><span class="sxs-lookup"><span data-stu-id="d29b4-118">Empty UUIDs are referred to as nil UUIDs rather than **NULL** UUIDs.</span></span> <span data-ttu-id="d29b4-119">El término Nil indica cualquier elemento que sea cero, en blanco, vacío o no inicializado.</span><span class="sxs-lookup"><span data-stu-id="d29b4-119">The term nil indicates anything that is zero, blank, empty, or uninitialized.</span></span> <span data-ttu-id="d29b4-120">Una cadena vacía, un registro de base de datos vacío o un UUID no inicializado son ejemplos de valores nulos.</span><span class="sxs-lookup"><span data-stu-id="d29b4-120">An empty string, an empty database record, or an uninitialized UUID are all examples of nil values.</span></span>

> [!Note]  
> <span data-ttu-id="d29b4-121">El valor **null** es el valor específico de cero.</span><span class="sxs-lookup"><span data-stu-id="d29b4-121">The value **NULL** is the specific value zero.</span></span> <span data-ttu-id="d29b4-122">A menudo se usa en la programación de C y C++ junto con punteros.</span><span class="sxs-lookup"><span data-stu-id="d29b4-122">It is often used in C and C++ programming in conjunction with pointers.</span></span> <span data-ttu-id="d29b4-123">Nil es un término más general que **null**.</span><span class="sxs-lookup"><span data-stu-id="d29b4-123">Nil is a more general term than **NULL**.</span></span> <span data-ttu-id="d29b4-124">La interfaz de objeto no inicializada UUID siempre se debe denominar UUID nulo en lugar de UUID **nulo** .</span><span class="sxs-lookup"><span data-stu-id="d29b4-124">Uninitialized object interface UUIDs should always be referred to as nil UUIDs rather than **NULL** UUIDs.</span></span>

 

## <a name="using-uuidgen"></a><span data-ttu-id="d29b4-125">Usar uuidgen</span><span class="sxs-lookup"><span data-stu-id="d29b4-125">Using Uuidgen</span></span>

<span data-ttu-id="d29b4-126">Microsoft proporciona un programa de utilidad denominado uuidgen para generar el UUID.</span><span class="sxs-lookup"><span data-stu-id="d29b4-126">Microsoft provides a utility program called Uuidgen to generate your UUIDs.</span></span> <span data-ttu-id="d29b4-127">La utilidad uuidgen genera el UUID en formato de archivo IDL o en formato de lenguaje C.</span><span class="sxs-lookup"><span data-stu-id="d29b4-127">The Uuidgen utility generates the UUID in IDL file format or C-language format.</span></span>

<span data-ttu-id="d29b4-128">Al ejecutar la utilidad uuidgen desde la línea de comandos, puede usar los siguientes modificadores de comando.</span><span class="sxs-lookup"><span data-stu-id="d29b4-128">When you run the Uuidgen utility from the command line, you can use the following command switches.</span></span>



| <span data-ttu-id="d29b4-129">Uuidgen (conmutador)</span><span class="sxs-lookup"><span data-stu-id="d29b4-129">Uuidgen switch</span></span>           | <span data-ttu-id="d29b4-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="d29b4-130">Description</span></span>                                                                |
|--------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="d29b4-131">**/I**</span><span class="sxs-lookup"><span data-stu-id="d29b4-131">**/I**</span></span>                   | <span data-ttu-id="d29b4-132">Genera UUID en una plantilla de interfaz IDL.</span><span class="sxs-lookup"><span data-stu-id="d29b4-132">Outputs UUID to an IDL interface template.</span></span>                                 |
| <span data-ttu-id="d29b4-133">**/s**</span><span class="sxs-lookup"><span data-stu-id="d29b4-133">**/s**</span></span>                   | <span data-ttu-id="d29b4-134">Genera UUID como una estructura de C inicializada.</span><span class="sxs-lookup"><span data-stu-id="d29b4-134">Outputs UUID as an initialized C structure.</span></span>                                |
| <span data-ttu-id="d29b4-135">**/o** < *nombre de archivo*></span><span class="sxs-lookup"><span data-stu-id="d29b4-135">**/o**<*filename*></span></span> | <span data-ttu-id="d29b4-136">Redirige la salida a un archivo; se especifica inmediatamente después del modificador **/o** .</span><span class="sxs-lookup"><span data-stu-id="d29b4-136">Redirects output to a file; specified immediately after the **/o** switch.</span></span> |
| <span data-ttu-id="d29b4-137">**/n** < *número* de></span><span class="sxs-lookup"><span data-stu-id="d29b4-137">**/n**<*number*></span></span>   | <span data-ttu-id="d29b4-138">Especifica el número de UUID que se va a generar.</span><span class="sxs-lookup"><span data-stu-id="d29b4-138">Specifies the number of UUIDs to generate.</span></span>                                 |
| <span data-ttu-id="d29b4-139">**/v**</span><span class="sxs-lookup"><span data-stu-id="d29b4-139">**/v**</span></span>                   | <span data-ttu-id="d29b4-140">Muestra información de versión sobre Uuidgen.</span><span class="sxs-lookup"><span data-stu-id="d29b4-140">Displays version information about Uuidgen.</span></span>                                |
| <span data-ttu-id="d29b4-141">**/h** o **?**</span><span class="sxs-lookup"><span data-stu-id="d29b4-141">**/h** or **?**</span></span>          | <span data-ttu-id="d29b4-142">Muestra el Resumen de la opción de comando.</span><span class="sxs-lookup"><span data-stu-id="d29b4-142">Displays command-option summary.</span></span>                                           |



 

<span data-ttu-id="d29b4-143">Normalmente, utilizará la utilidad uuidgen, tal como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="d29b4-143">Typically, you will use the Uuidgen utility as shown in the following example.</span></span>

<span data-ttu-id="d29b4-144">**uuidgen-i-oMyApp. idl**</span><span class="sxs-lookup"><span data-stu-id="d29b4-144">**uuidgen -i -oMyApp.idl**</span></span>

<span data-ttu-id="d29b4-145">Este comando genera un UUID y lo almacena en un archivo MIDL que se puede utilizar como plantilla.</span><span class="sxs-lookup"><span data-stu-id="d29b4-145">This command generates a UUID and stores it in a MIDL file that you can use as a template.</span></span> <span data-ttu-id="d29b4-146">Cuando se ejecuta el comando anterior, el contenido de MyApp. idl es similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="d29b4-146">When the preceding command is executed, the contents of MyApp.idl are similar to the following:</span></span>

``` syntax
[
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface INTERFACENAME
{

}
```

<span data-ttu-id="d29b4-147">El siguiente paso sería reemplazar el nombre del marcador de posición, INTERFACENAME, por el nombre real de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="d29b4-147">The next step would be to replace the placeholder name, INTERFACENAME, with the actual name of your interface.</span></span>

 

 




