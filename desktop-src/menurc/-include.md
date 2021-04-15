---
title: " include"
description: La Directiva \ include hace que el compilador de recursos procese el archivo especificado en el parámetro FILENAME.
ms.assetid: 9a3505c6-c19f-4c4f-85a4-94fbcfc0f9c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8d36f1d0ae24f3dc21d67eec57056872aabdbd
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104421867"
---
# <a name="-include"></a><span data-ttu-id="b009e-103">inclui</span><span class="sxs-lookup"><span data-stu-id="b009e-103">' include'</span></span>

<span data-ttu-id="b009e-104">La directiva **\# include** hace que el compilador de recursos procese el archivo especificado en el parámetro *filename* .</span><span class="sxs-lookup"><span data-stu-id="b009e-104">The **\#include** directive causes the resource compiler to process the file specified in the *filename* parameter.</span></span> <span data-ttu-id="b009e-105">Este archivo debe ser un archivo de encabezado que defina las constantes que se usan en el archivo de definición de recursos.</span><span class="sxs-lookup"><span data-stu-id="b009e-105">This file should be a header file that defines the constants used in the resource-definition file.</span></span> <span data-ttu-id="b009e-106">El archivo puede utilizar caracteres de un solo byte, de doble byte o Unicode.</span><span class="sxs-lookup"><span data-stu-id="b009e-106">The file can use single-byte, double-byte, or Unicode characters.</span></span>

``` syntax
#include filename
```

<dl> <dt>

<span data-ttu-id="b009e-107"><span id="filename"></span><span id="FILENAME"></span>*extensión*</span><span class="sxs-lookup"><span data-stu-id="b009e-107"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="b009e-108">Nombre del archivo que se va a incluir.</span><span class="sxs-lookup"><span data-stu-id="b009e-108">Name of the file to be included.</span></span> <span data-ttu-id="b009e-109">Si el archivo está en el directorio actual, la cadena debe ir entre comillas dobles. Si el archivo se encuentra en el directorio especificado por la variable de entorno INCLUDE, la cadena se debe incluir entre caracteres de menor que y mayor que (<>).</span><span class="sxs-lookup"><span data-stu-id="b009e-109">If the file is in the current directory, the string must be enclosed in double quotation marks; if the file is in the directory specified by the INCLUDE environment variable, the string must be enclosed in less-than and greater-than characters (<>).</span></span> <span data-ttu-id="b009e-110">Debe proporcionar una ruta de acceso completa entre comillas dobles (") si el archivo no está en el directorio actual o en el directorio especificado por la variable de entorno INCLUDE.</span><span class="sxs-lookup"><span data-stu-id="b009e-110">You must give a full path enclosed in double quotation marks (") if the file is not in the current directory or in the directory specified by the INCLUDE environment variable.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b009e-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b009e-111">Remarks</span></span>

<span data-ttu-id="b009e-112">Use la siguiente instrucción en el archivo de encabezado para envolver las instrucciones que puede compilar un compilador de C pero no RC:</span><span class="sxs-lookup"><span data-stu-id="b009e-112">Use the following statement in your header file to surround statements that can be compiled by a C compiler but not RC:</span></span>

``` syntax
#ifndef RC_INVOKED
```

<span data-ttu-id="b009e-113">De este modo, puede usar los mismos archivos de inclusión en los archivos. c y. rc.</span><span class="sxs-lookup"><span data-stu-id="b009e-113">This way, you can use the same include files in your .c and .rc files.</span></span>

## <a name="example"></a><span data-ttu-id="b009e-114">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b009e-114">Example</span></span>

<span data-ttu-id="b009e-115">En este ejemplo se procesan los archivos de encabezado Windows. h y MyDefs. h mientras se compila el archivo de definición de recursos:</span><span class="sxs-lookup"><span data-stu-id="b009e-115">This example processes the header files Windows.h and MyDefs.h while compiling the resource-definition file:</span></span>

``` syntax
#include <windows.h>
#include "headers\mydefs.h"
```

## <a name="related-topics"></a><span data-ttu-id="b009e-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b009e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b009e-117">Directivas de preprocesador</span><span class="sxs-lookup"><span data-stu-id="b009e-117">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




