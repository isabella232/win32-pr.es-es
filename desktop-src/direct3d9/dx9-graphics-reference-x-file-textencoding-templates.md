---
description: 'Las plantillas definen cómo se interpreta el flujo de datos: los datos se modulan mediante la definición de plantilla. En esta sección se describen los siguientes aspectos de una plantilla y se proporciona una plantilla de ejemplo.'
ms.assetid: f84978a8-8315-4626-be68-f00f3a72e5ac
title: Plantillas (formato de archivo X, codificación de texto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fccec46e72a73bb5ed4434fd252595e1b072ad4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805192"
---
# <a name="templates-x-file-format-text-encoding"></a><span data-ttu-id="bc3fe-104">Plantillas (formato de archivo X, codificación de texto)</span><span class="sxs-lookup"><span data-stu-id="bc3fe-104">Templates (X file format, text encoding)</span></span>

<span data-ttu-id="bc3fe-105">Las plantillas definen cómo se interpreta el flujo de datos: los datos se modulan mediante la definición de plantilla.</span><span class="sxs-lookup"><span data-stu-id="bc3fe-105">Templates define how the data stream is interpreted - the data is modulated by the template definition.</span></span> <span data-ttu-id="bc3fe-106">En esta sección se describen los siguientes aspectos de una plantilla y se proporciona una plantilla de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="bc3fe-106">This section discusses the following aspects of a template and provides an example template.</span></span>

<span data-ttu-id="bc3fe-107">Hay una plantilla especial: la plantilla de encabezado.</span><span class="sxs-lookup"><span data-stu-id="bc3fe-107">There is one special template - the header template.</span></span> <span data-ttu-id="bc3fe-108">Se recomienda que cada aplicación defina una plantilla de encabezado y la use para definir información específica de la aplicación, como la información de versión.</span><span class="sxs-lookup"><span data-stu-id="bc3fe-108">It is recommended that each application define a header template and use it to define application-specific information, such as version information.</span></span> <span data-ttu-id="bc3fe-109">Si está presente, la API de formato de archivo. x Lee este encabezado.</span><span class="sxs-lookup"><span data-stu-id="bc3fe-109">If present, this header is read by the .x file format API.</span></span> <span data-ttu-id="bc3fe-110">Si un miembro de marcas está disponible, se utiliza para determinar cómo se interpretan los datos siguientes.</span><span class="sxs-lookup"><span data-stu-id="bc3fe-110">If a flags member is available, it is used to determine how the following data is interpreted.</span></span> <span data-ttu-id="bc3fe-111">El miembro Flags, si está definido, debe ser un valor DWORD.</span><span class="sxs-lookup"><span data-stu-id="bc3fe-111">The flags member, if defined, should be a DWORD.</span></span> <span data-ttu-id="bc3fe-112">Un bit está definido actualmente como bit 0.</span><span class="sxs-lookup"><span data-stu-id="bc3fe-112">One bit is currently defined - bit 0.</span></span> <span data-ttu-id="bc3fe-113">Si este bit está claro, los siguientes datos del archivo son binarios.</span><span class="sxs-lookup"><span data-stu-id="bc3fe-113">If this bit is clear, the following data in the file is binary.</span></span> <span data-ttu-id="bc3fe-114">Si se establece, los datos siguientes son texto.</span><span class="sxs-lookup"><span data-stu-id="bc3fe-114">If set, the following data is text.</span></span> <span data-ttu-id="bc3fe-115">Puede usar varios objetos de datos de encabezado para cambiar entre el texto binario y el texto dentro del archivo.</span><span class="sxs-lookup"><span data-stu-id="bc3fe-115">You can use multiple header data objects to switch between binary and text within the file.</span></span>

## <a name="template-form-name-and-uuid"></a><span data-ttu-id="bc3fe-116">Formulario de plantilla, nombre y UUID</span><span class="sxs-lookup"><span data-stu-id="bc3fe-116">Template Form, Name, and UUID</span></span>

<span data-ttu-id="bc3fe-117">Una plantilla tiene el formato siguiente.</span><span class="sxs-lookup"><span data-stu-id="bc3fe-117">A template has the following form.</span></span>


```
template <template-name> {
<UUID>
    <member 1>;
...
    <member n>;
[restrictions]
}
```



<span data-ttu-id="bc3fe-118">El nombre de la plantilla es un nombre alfanumérico que puede incluir el carácter de subrayado ( \_ ).</span><span class="sxs-lookup"><span data-stu-id="bc3fe-118">The template name is an alphanumeric name that can include the underscore character (\_).</span></span> <span data-ttu-id="bc3fe-119">No debe comenzar con un dígito.</span><span class="sxs-lookup"><span data-stu-id="bc3fe-119">It must not begin with a digit.</span></span> <span data-ttu-id="bc3fe-120">El UUID es un identificador único universal formateado con el estándar de entorno de informática distribuida de Open Software Foundation y entre corchetes angulares (< >).</span><span class="sxs-lookup"><span data-stu-id="bc3fe-120">The UUID is a universally unique identifier formatted to the Open Software Foundation's Distributed Computing Environment standard and enclosed by angle brackets (< >).</span></span> <span data-ttu-id="bc3fe-121">Por ejemplo: <3D82AB43-62DA-11cf-AB39-0020AF71E433>.</span><span class="sxs-lookup"><span data-stu-id="bc3fe-121">For example: <3D82AB43-62DA-11cf-AB39-0020AF71E433>.</span></span>

## <a name="template-members"></a><span data-ttu-id="bc3fe-122">Miembros de plantilla</span><span class="sxs-lookup"><span data-stu-id="bc3fe-122">Template Members</span></span>

<span data-ttu-id="bc3fe-123">Los miembros de plantilla se componen de un tipo de datos con nombre seguido de un nombre opcional o una matriz de un tipo de datos con nombre.</span><span class="sxs-lookup"><span data-stu-id="bc3fe-123">Template members consist of a named data type followed by an optional name or an array of a named data type.</span></span> <span data-ttu-id="bc3fe-124">En la tabla siguiente se definen los tipos de datos primitivos válidos.</span><span class="sxs-lookup"><span data-stu-id="bc3fe-124">Valid primitive data types are defined in the following table.</span></span>



| <span data-ttu-id="bc3fe-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="bc3fe-125">Type</span></span>    | <span data-ttu-id="bc3fe-126">Size</span><span class="sxs-lookup"><span data-stu-id="bc3fe-126">Size</span></span>                               |
|---------|------------------------------------|
| <span data-ttu-id="bc3fe-127">WORD</span><span class="sxs-lookup"><span data-stu-id="bc3fe-127">WORD</span></span>    | <span data-ttu-id="bc3fe-128">16 bits</span><span class="sxs-lookup"><span data-stu-id="bc3fe-128">16 bits</span></span>                            |
| <span data-ttu-id="bc3fe-129">DWORD</span><span class="sxs-lookup"><span data-stu-id="bc3fe-129">DWORD</span></span>   | <span data-ttu-id="bc3fe-130">32 bits</span><span class="sxs-lookup"><span data-stu-id="bc3fe-130">32 bits</span></span>                            |
| <span data-ttu-id="bc3fe-131">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bc3fe-131">FLOAT</span></span>   | <span data-ttu-id="bc3fe-132">Float de IEEE</span><span class="sxs-lookup"><span data-stu-id="bc3fe-132">IEEE float</span></span>                         |
| <span data-ttu-id="bc3fe-133">DOUBLE</span><span class="sxs-lookup"><span data-stu-id="bc3fe-133">DOUBLE</span></span>  | <span data-ttu-id="bc3fe-134">64 bits</span><span class="sxs-lookup"><span data-stu-id="bc3fe-134">64 bits</span></span>                            |
| <span data-ttu-id="bc3fe-135">CHAR</span><span class="sxs-lookup"><span data-stu-id="bc3fe-135">CHAR</span></span>    | <span data-ttu-id="bc3fe-136">8 bits</span><span class="sxs-lookup"><span data-stu-id="bc3fe-136">8 bits</span></span>                             |
| <span data-ttu-id="bc3fe-137">UCHAR</span><span class="sxs-lookup"><span data-stu-id="bc3fe-137">UCHAR</span></span>   | <span data-ttu-id="bc3fe-138">8 bits</span><span class="sxs-lookup"><span data-stu-id="bc3fe-138">8 bits</span></span>                             |
| <span data-ttu-id="bc3fe-139">BYTE</span><span class="sxs-lookup"><span data-stu-id="bc3fe-139">BYTE</span></span>    | <span data-ttu-id="bc3fe-140">8 bits</span><span class="sxs-lookup"><span data-stu-id="bc3fe-140">8 bits</span></span>                             |
| <span data-ttu-id="bc3fe-141">STRING</span><span class="sxs-lookup"><span data-stu-id="bc3fe-141">STRING</span></span>  | <span data-ttu-id="bc3fe-142">Cadena terminada en NULL</span><span class="sxs-lookup"><span data-stu-id="bc3fe-142">NULL terminated string</span></span>             |
| <span data-ttu-id="bc3fe-143">CSTRING</span><span class="sxs-lookup"><span data-stu-id="bc3fe-143">CSTRING</span></span> | <span data-ttu-id="bc3fe-144">Cadena de C con formato (no se admite)</span><span class="sxs-lookup"><span data-stu-id="bc3fe-144">Formatted C string (not supported)</span></span> |
| <span data-ttu-id="bc3fe-145">UNICODE</span><span class="sxs-lookup"><span data-stu-id="bc3fe-145">UNICODE</span></span> | <span data-ttu-id="bc3fe-146">Cadena Unicode (no se admite)</span><span class="sxs-lookup"><span data-stu-id="bc3fe-146">Unicode string (not supported)</span></span>     |



 

<span data-ttu-id="bc3fe-147">También se puede hacer referencia a tipos de datos adicionales definidos por plantillas encontradas anteriormente en el flujo de datos dentro de una definición de plantilla.</span><span class="sxs-lookup"><span data-stu-id="bc3fe-147">Additional data types defined by templates encountered earlier in the data stream can also be referenced within a template definition.</span></span> <span data-ttu-id="bc3fe-148">No se permiten referencias adelantadas.</span><span class="sxs-lookup"><span data-stu-id="bc3fe-148">No forward references are allowed.</span></span>

<span data-ttu-id="bc3fe-149">Cualquier tipo de datos válido se puede expresar como una matriz en la definición de plantilla.</span><span class="sxs-lookup"><span data-stu-id="bc3fe-149">Any valid data type can be expressed as an array in the template definition.</span></span> <span data-ttu-id="bc3fe-150">En el ejemplo siguiente se muestra la sintaxis básica.</span><span class="sxs-lookup"><span data-stu-id="bc3fe-150">The basic syntax is shown in the following example.</span></span>


```
array <data-type> <name>[<dimension-size>];
```



<span data-ttu-id="bc3fe-151"><> de tamaño de dimensión puede ser un entero o una referencia con nombre a otro miembro de plantilla cuyo valor se sustituirá.</span><span class="sxs-lookup"><span data-stu-id="bc3fe-151"><dimension-size> can either be an integer or a named reference to another template member whose value is then substituted.</span></span> <span data-ttu-id="bc3fe-152">Las matrices pueden ser de n dimensiones, donde n viene determinado por el número de corchetes emparejados al final de la instrucción, como en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="bc3fe-152">Arrays can be n-dimensional, where n is determined by the number of paired square brackets trailing the statement, as in the following example.</span></span>


```
array DWORD FixedHerd[24];
array DWORD Herd[nCows];
array FLOAT Matrix4x4[4][4];
```



## <a name="template-restrictions"></a><span data-ttu-id="bc3fe-153">Restricciones de plantilla</span><span class="sxs-lookup"><span data-stu-id="bc3fe-153">Template Restrictions</span></span>

<span data-ttu-id="bc3fe-154">Las plantillas pueden ser abiertas, cerradas o restringidas.</span><span class="sxs-lookup"><span data-stu-id="bc3fe-154">Templates can be open, closed, or restricted.</span></span> <span data-ttu-id="bc3fe-155">Estas restricciones determinan qué tipos de datos pueden aparecer en la jerarquía inmediata de un objeto de datos definido por la plantilla.</span><span class="sxs-lookup"><span data-stu-id="bc3fe-155">These restrictions determine which data types can appear in the immediate hierarchy of a data object defined by the template.</span></span> <span data-ttu-id="bc3fe-156">Una plantilla abierta no tiene restricciones, una plantilla cerrada rechaza todos los tipos de datos y una plantilla restringida permite una lista con nombre de tipos de datos.</span><span class="sxs-lookup"><span data-stu-id="bc3fe-156">An open template has no restrictions, a closed template rejects all data types, and a restricted template allows a named list of data types.</span></span>

<span data-ttu-id="bc3fe-157">La sintaxis para indicar una plantilla abierta es de tres puntos entre corchetes.</span><span class="sxs-lookup"><span data-stu-id="bc3fe-157">The syntax for indicating an open template is three periods enclosed by square brackets.</span></span>


```
[ ... ]
```



<span data-ttu-id="bc3fe-158">Una lista separada por comas de tipos de datos con nombre seguido opcionalmente por su UUID entre corchetes indica una plantilla restringida.</span><span class="sxs-lookup"><span data-stu-id="bc3fe-158">A comma-separated list of named data types followed optionally by their UUIDs enclosed by square brackets indicates a restricted template.</span></span>


```
[ { data-type [ UUID ] , } ... ]
```



<span data-ttu-id="bc3fe-159">La ausencia de una de las anteriores indica una plantilla cerrada.</span><span class="sxs-lookup"><span data-stu-id="bc3fe-159">The absence of either of the above indicates a closed template.</span></span>

## <a name="template-example"></a><span data-ttu-id="bc3fe-160">Ejemplo de plantilla</span><span class="sxs-lookup"><span data-stu-id="bc3fe-160">Template Example</span></span>

<span data-ttu-id="bc3fe-161">A continuación se muestra una plantilla de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="bc3fe-161">The following shows an example template.</span></span>


```
template Mesh {
<3D82AB44-62DA-11cf-AB39-0020AF71E433>
DWORD nVertices;
array Vector vertices[nVertices];
DWORD nFaces;
array MeshFace faces[nFaces];
 [ ... ]                // An open template
}
template Vector {
<3D82AB5E-62DA-11cf-AB39-0020AF71E433>
FLOAT x;
FLOAT y;
FLOAT z;
}                        // A closed template
template FileSystem {
<UUID>
STRING name;
[ Directory <UUID>, File <UUID> ]    // A restricted template
}
```



## <a name="related-topics"></a><span data-ttu-id="bc3fe-162">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bc3fe-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc3fe-163">Codificación de texto</span><span class="sxs-lookup"><span data-stu-id="bc3fe-163">Text Encoding</span></span>](text-encoding.md)
</dt> </dl>

 

 



