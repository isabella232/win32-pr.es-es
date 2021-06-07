---
title: El comando de archivo de respuesta
description: Un archivo de respuesta es un archivo de texto que contiene una o varias opciones de línea de comandos del compilador MIDL.
ms.assetid: ad47ea1a-fe7a-4354-be2f-599ba77685ee
keywords:
- referencia de línea de comandos MIDL, comando de archivo de respuesta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26cf4d07ce8465239874ff666537646da2c4c564
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387671"
---
# <a name="the-response-file-command"></a><span data-ttu-id="a1460-104">El comando de archivo de respuesta</span><span class="sxs-lookup"><span data-stu-id="a1460-104">The Response File Command</span></span>

<span data-ttu-id="a1460-105">Un archivo de respuesta es un archivo de texto que contiene una o varias opciones de línea de comandos del compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="a1460-105">A response file is a text file containing one or more MIDL compiler command-line options.</span></span> <span data-ttu-id="a1460-106">A diferencia de una línea de comandos, un archivo de respuesta permite varias líneas de opciones y nombres de archivo.</span><span class="sxs-lookup"><span data-stu-id="a1460-106">Unlike a command line, a response file allows multiple lines of options and file names.</span></span> <span data-ttu-id="a1460-107">Esto puede ser útil debido a las limitaciones del entorno de compilación o para su proceso de compilación.</span><span class="sxs-lookup"><span data-stu-id="a1460-107">This may be useful due to limitations of your build environment, or as a convenience for your build process.</span></span>

## <a name="switch-options"></a><span data-ttu-id="a1460-108">Cambiar opciones</span><span class="sxs-lookup"><span data-stu-id="a1460-108">Switch Options</span></span>

``` syntax
midl @response_file
```

<dl> <dt>

<span data-ttu-id="a1460-109"><span id="response_file"></span><span id="RESPONSE_FILE"></span>*archivo \_ de respuesta*</span><span class="sxs-lookup"><span data-stu-id="a1460-109"><span id="response_file"></span><span id="RESPONSE_FILE"></span>*response\_file*</span></span>
</dt> <dd>

<span data-ttu-id="a1460-110">Especifica el nombre de un archivo de respuesta.</span><span class="sxs-lookup"><span data-stu-id="a1460-110">Specifies the name of a response file.</span></span> <span data-ttu-id="a1460-111">El nombre del archivo de respuesta debe seguir inmediatamente el carácter @.</span><span class="sxs-lookup"><span data-stu-id="a1460-111">The response file name must immediately follow the @ character.</span></span> <span data-ttu-id="a1460-112">No se permite ningún espacio en blanco entre el carácter @ y el nombre del archivo de respuesta.</span><span class="sxs-lookup"><span data-stu-id="a1460-112">No white space is allowed between the @ character and the response file name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a1460-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a1460-113">Remarks</span></span>

<span data-ttu-id="a1460-114">Como alternativa a colocar todas las opciones asociadas a un modificador en la línea de comandos, el compilador midl acepta archivos de respuesta que contienen modificadores y argumentos.</span><span class="sxs-lookup"><span data-stu-id="a1460-114">As an alternative to placing all options associated with a switch on the command line, the MIDL compiler accepts response files that contain switches and arguments.</span></span> <span data-ttu-id="a1460-115">Las opciones de un archivo de respuesta se interpretan como si se encuentran en esa ubicación en la línea de comandos de MIDL.</span><span class="sxs-lookup"><span data-stu-id="a1460-115">Options in a response file are interpreted as if they are present in that location in the MIDL command line.</span></span>

<span data-ttu-id="a1460-116">Cada argumento de un archivo de respuesta debe comenzar y terminar en la misma línea.</span><span class="sxs-lookup"><span data-stu-id="a1460-116">Each argument in a response file must begin and end on the same line.</span></span> <span data-ttu-id="a1460-117">El carácter de barra diagonal inversa ( \\ ) no se puede usar para concatenar líneas.</span><span class="sxs-lookup"><span data-stu-id="a1460-117">The backslash character (\\) cannot be used to concatenate lines.</span></span> <span data-ttu-id="a1460-118">Cuando forma parte de una cadena entrecomillada en el archivo de respuesta, el carácter de barra diagonal inversa solo se puede usar antes de otra barra diagonal inversa o antes de un carácter de comilla doble (").</span><span class="sxs-lookup"><span data-stu-id="a1460-118">When it is part of a quoted string in the response file, the backslash character can only be used before another backslash or before a double quotation mark character (").</span></span> <span data-ttu-id="a1460-119">Cuando no forma parte de una cadena entre comillas, el carácter de barra diagonal inversa solo se puede usar antes de un carácter de comilla doble.</span><span class="sxs-lookup"><span data-stu-id="a1460-119">When it is not part of a quoted string, the backslash character can only be used before a double quotation mark character.</span></span>

<span data-ttu-id="a1460-120">MIDL admite argumentos de línea de comandos que incluyen uno o varios archivos de respuesta combinados con otros modificadores de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="a1460-120">MIDL supports command-line arguments that include one or more response files combined with other command-line switches.</span></span>

<span data-ttu-id="a1460-121">El compilador MIDL no admite archivos de respuesta anidados.</span><span class="sxs-lookup"><span data-stu-id="a1460-121">The MIDL compiler does not support nested response files.</span></span>

## <a name="examples"></a><span data-ttu-id="a1460-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a1460-122">Examples</span></span>

<span data-ttu-id="a1460-123">**Midl @midl.rsp**</span><span class="sxs-lookup"><span data-stu-id="a1460-123">**midl @midl.rsp**</span></span>

<span data-ttu-id="a1460-124">**midl -Oicf @midl1.rsp -env win32 @midl2.rsp itf.idl**</span><span class="sxs-lookup"><span data-stu-id="a1460-124">**midl -Oicf @midl1.rsp -env win32 @midl2.rsp itf.idl**</span></span>

## <a name="related-topics"></a><span data-ttu-id="a1460-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a1460-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1460-126">Sintaxis general de la línea de comandos de MIDL</span><span class="sxs-lookup"><span data-stu-id="a1460-126">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




