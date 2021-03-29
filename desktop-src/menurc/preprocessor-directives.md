---
title: Directivas de preprocesador (menús y otros recursos)
description: Puede usar las directivas descritas en la siguiente tabla según sea necesario en el script de recursos. Indican a RC que realice acciones o asigne valores a los nombres.
ms.assetid: 162f946e-54d8-4e23-9aa7-8e91eda4ee68
keywords:
- compilador de recursos, directivas de preprocesador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43e8c32f1d32dab784d5d947fdf64b7018451a5a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104359646"
---
# <a name="preprocessor-directives-menus-and-other-resources"></a><span data-ttu-id="8f721-105">Directivas de preprocesador (menús y otros recursos)</span><span class="sxs-lookup"><span data-stu-id="8f721-105">Preprocessor Directives (Menus and Other Resources)</span></span>

<span data-ttu-id="8f721-106">Puede usar las directivas descritas en la siguiente tabla según sea necesario en el script de recursos.</span><span class="sxs-lookup"><span data-stu-id="8f721-106">You can use the directives described in the following table as needed in your resource script.</span></span> <span data-ttu-id="8f721-107">Indican a RC que realice acciones o asigne valores a los nombres.</span><span class="sxs-lookup"><span data-stu-id="8f721-107">They instruct RC to perform actions or to assign values to names.</span></span>



| <span data-ttu-id="8f721-108">Directiva</span><span class="sxs-lookup"><span data-stu-id="8f721-108">Directive</span></span>                     | <span data-ttu-id="8f721-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="8f721-109">Description</span></span>                                                           |
|-------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="8f721-110">**\#Defina**</span><span class="sxs-lookup"><span data-stu-id="8f721-110">**\#define**</span></span>](-define.md)   | <span data-ttu-id="8f721-111">Define un nombre especificado asignándole un valor determinado.</span><span class="sxs-lookup"><span data-stu-id="8f721-111">Defines a specified name by assigning it a given value.</span></span>               |
| [<span data-ttu-id="8f721-112">**\#elif**</span><span class="sxs-lookup"><span data-stu-id="8f721-112">**\#elif**</span></span>](-elif.md)       | <span data-ttu-id="8f721-113">Marca una cláusula opcional de un bloque de compilación condicional.</span><span class="sxs-lookup"><span data-stu-id="8f721-113">Marks an optional clause of a conditional-compilation block.</span></span>          |
| [<span data-ttu-id="8f721-114">**\#else**</span><span class="sxs-lookup"><span data-stu-id="8f721-114">**\#else**</span></span>](-else.md)       | <span data-ttu-id="8f721-115">Marca la última cláusula opcional de un bloque de compilación condicional.</span><span class="sxs-lookup"><span data-stu-id="8f721-115">Marks the last optional clause of a conditional-compilation block.</span></span>    |
| [<span data-ttu-id="8f721-116">**\#endif**</span><span class="sxs-lookup"><span data-stu-id="8f721-116">**\#endif**</span></span>](-endif.md)     | <span data-ttu-id="8f721-117">Marca el final de un bloque de compilación condicional.</span><span class="sxs-lookup"><span data-stu-id="8f721-117">Marks the end of a conditional-compilation block.</span></span>                     |
| [<span data-ttu-id="8f721-118">**\#if**</span><span class="sxs-lookup"><span data-stu-id="8f721-118">**\#if**</span></span>](-if.md)           | <span data-ttu-id="8f721-119">Compila condicionalmente el script si una expresión especificada es true.</span><span class="sxs-lookup"><span data-stu-id="8f721-119">Conditionally compiles the script if a specified expression is true.</span></span>  |
| [<span data-ttu-id="8f721-120">**\#ifdef**</span><span class="sxs-lookup"><span data-stu-id="8f721-120">**\#ifdef**</span></span>](-ifdef.md)     | <span data-ttu-id="8f721-121">Compila condicionalmente el script si se define un nombre especificado.</span><span class="sxs-lookup"><span data-stu-id="8f721-121">Conditionally compiles the script if a specified name is defined.</span></span>     |
| [<span data-ttu-id="8f721-122">**\#ifndef**</span><span class="sxs-lookup"><span data-stu-id="8f721-122">**\#ifndef**</span></span>](-ifndef.md)   | <span data-ttu-id="8f721-123">Compila condicionalmente el script si no se ha definido un nombre especificado.</span><span class="sxs-lookup"><span data-stu-id="8f721-123">Conditionally compiles the script if a specified name is not defined.</span></span> |
| [<span data-ttu-id="8f721-124">**\#inclui**</span><span class="sxs-lookup"><span data-stu-id="8f721-124">**\#include**</span></span>](-include.md) | <span data-ttu-id="8f721-125">Copia el contenido de un archivo en el archivo de definición de recursos.</span><span class="sxs-lookup"><span data-stu-id="8f721-125">Copies the contents of a file into the resource-definition file.</span></span>      |
| [<span data-ttu-id="8f721-126">**\#undef**</span><span class="sxs-lookup"><span data-stu-id="8f721-126">**\#undef**</span></span>](-undef.md)     | <span data-ttu-id="8f721-127">Quita la definición del nombre especificado.</span><span class="sxs-lookup"><span data-stu-id="8f721-127">Removes the definition of the specified name.</span></span>                         |



 

<span data-ttu-id="8f721-128">Para definir símbolos para los identificadores de recursos, use la directiva **\# define** para definirlos en un archivo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="8f721-128">To define symbols for your resource identifiers, use the **\#define** directive to define them in a header file.</span></span> <span data-ttu-id="8f721-129">Incluya este encabezado tanto en el script de recursos como en el código fuente de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8f721-129">Include this header both in the resource script and your application source code.</span></span> <span data-ttu-id="8f721-130">Del mismo modo, los valores de atributos y estilos de recursos se definen mediante la inclusión de Windows. h en el script de recursos.</span><span class="sxs-lookup"><span data-stu-id="8f721-130">Similarly, you define the values for resource attributes and styles by including Windows.h in the resource script.</span></span>

<span data-ttu-id="8f721-131">RC trata los archivos con las extensiones. c y. h de una manera especial.</span><span class="sxs-lookup"><span data-stu-id="8f721-131">RC treats files with the .c and .h extensions in a special manner.</span></span> <span data-ttu-id="8f721-132">Se supone que un archivo con una de estas extensiones no contiene recursos.</span><span class="sxs-lookup"><span data-stu-id="8f721-132">It assumes that a file with one of these extensions does not contain resources.</span></span> <span data-ttu-id="8f721-133">Si un archivo tiene la extensión de nombre de archivo. c o. h, RC omite todas las líneas del archivo excepto las directivas de preprocesador.</span><span class="sxs-lookup"><span data-stu-id="8f721-133">If a file has the .c or .h file name extension, RC ignores all lines in the file except the preprocessor directives.</span></span> <span data-ttu-id="8f721-134">Por lo tanto, para incluir un archivo que contenga recursos en otro script de recursos, asigne al archivo una extensión distinta de. c o. h.</span><span class="sxs-lookup"><span data-stu-id="8f721-134">Therefore, to include a file that contains resources in another resource script, give the file to be included an extension other than .c or .h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8f721-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8f721-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f721-136">Directivas pragma</span><span class="sxs-lookup"><span data-stu-id="8f721-136">Pragma Directives</span></span>](pragma-directives.md)
</dt> </dl>

 

 




