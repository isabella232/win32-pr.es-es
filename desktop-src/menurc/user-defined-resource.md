---
title: User-Defined recurso
description: Una instrucción de definición de recursos definida por el usuario define un recurso que contiene datos específicos de la aplicación.
ms.assetid: b1cfec71-5733-4900-97f6-c1cbb350c728
keywords:
- recurso definido por el usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 909352c7f0643ed67b1d199fafba1ac8f15d2a9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268709"
---
# <a name="user-defined-resource"></a><span data-ttu-id="76a30-104">User-Defined recurso</span><span class="sxs-lookup"><span data-stu-id="76a30-104">User-Defined Resource</span></span>

<span data-ttu-id="76a30-105">Una instrucción de definición de recursos definida por el usuario define un recurso que contiene datos específicos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="76a30-105">A user-defined resource-definition statement defines a resource that contains application-specific data.</span></span> <span data-ttu-id="76a30-106">Los datos pueden tener cualquier formato y pueden definirse como el contenido de un archivo determinado (si se proporciona el parámetro *filename* ) o como una serie de números y cadenas (si se especifica el bloque de *datos sin formato* ).</span><span class="sxs-lookup"><span data-stu-id="76a30-106">The data can have any format and can be defined either as the content of a given file (if the *filename* parameter is given) or as a series of numbers and strings (if the *raw-data* block is specified).</span></span>

``` syntax
nameID typeID filename
```

<span data-ttu-id="76a30-107">El *nombre de archivo especifica el* nombre de un archivo que contiene los datos binarios del recurso.</span><span class="sxs-lookup"><span data-stu-id="76a30-107">The *filename* specifies the name of a file containing the binary data of the resource.</span></span> <span data-ttu-id="76a30-108">El contenido del archivo se incluye como el recurso.</span><span class="sxs-lookup"><span data-stu-id="76a30-108">The contents of the file are included as the resource.</span></span> <span data-ttu-id="76a30-109">RC no interpreta los datos binarios de ningún modo.</span><span class="sxs-lookup"><span data-stu-id="76a30-109">RC does not interpret the binary data in any way.</span></span> <span data-ttu-id="76a30-110">Es responsabilidad del programador garantizar que los datos se alineen correctamente para la arquitectura del equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="76a30-110">It is the programmer's responsibility to ensure that the data is properly aligned for the target computer architecture.</span></span>

<span data-ttu-id="76a30-111">También se puede definir un recurso definido por el usuario por completo en el script de recursos con la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="76a30-111">A user-defined resource can also be defined completely in the resource script using the following syntax:</span></span>

``` syntax
nameID typeID  {  raw-data  }
```

## <a name="parameters"></a><span data-ttu-id="76a30-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="76a30-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76a30-113"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="76a30-113"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="76a30-114">Nombre único o entero de 16 bits sin signo que identifica el recurso.</span><span class="sxs-lookup"><span data-stu-id="76a30-114">Unique name or a 16-bit unsigned integer that identifies the resource.</span></span>

</dd> <dt>

<span data-ttu-id="76a30-115"><span id="typeID"></span><span id="typeid"></span><span id="TYPEID"></span>*typeID*</span><span class="sxs-lookup"><span data-stu-id="76a30-115"><span id="typeID"></span><span id="typeid"></span><span id="TYPEID"></span>*typeID*</span></span>
</dt> <dd>

<span data-ttu-id="76a30-116">Nombre único o entero de 16 bits sin signo que identifica el tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="76a30-116">Unique name or a 16-bit unsigned integer that identifies the resource type.</span></span> <span data-ttu-id="76a30-117">Si se proporciona un número, debe ser mayor que 255.</span><span class="sxs-lookup"><span data-stu-id="76a30-117">If a number is given, it must be greater than 255.</span></span> <span data-ttu-id="76a30-118">Los números del 1 al 255 se reservan para los tipos de recursos redefinidos existentes y futuros.</span><span class="sxs-lookup"><span data-stu-id="76a30-118">The numbers 1 through 255 are reserved for existing and future redefined resource types.</span></span>

</dd> <dt>

<span data-ttu-id="76a30-119"><span id="filename"></span><span id="FILENAME"></span>*extensión*</span><span class="sxs-lookup"><span data-stu-id="76a30-119"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="76a30-120">Nombre del archivo que contiene los datos de recursos.</span><span class="sxs-lookup"><span data-stu-id="76a30-120">Name of the file that contains the resource data.</span></span> <span data-ttu-id="76a30-121">El parámetro debe ser un nombre de archivo válido; debe ser una ruta de acceso completa si el archivo no está en el directorio de trabajo actual.</span><span class="sxs-lookup"><span data-stu-id="76a30-121">The parameter must be a valid file name; it must be a full path if the file is not in the current working directory.</span></span>

</dd> <dt>

<span data-ttu-id="76a30-122"><span id="raw-data"></span><span id="RAW-DATA"></span>*datos sin procesar*</span><span class="sxs-lookup"><span data-stu-id="76a30-122"><span id="raw-data"></span><span id="RAW-DATA"></span>*raw-data*</span></span>
</dt> <dd>

<span data-ttu-id="76a30-123">Datos sin procesar que se componen de uno o varios enteros o cadenas de caracteres.</span><span class="sxs-lookup"><span data-stu-id="76a30-123">Raw data consisting of one or more integers or strings of characters.</span></span> <span data-ttu-id="76a30-124">Los enteros se pueden especificar en formato decimal, octal o hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="76a30-124">Integers can be specified in decimal, octal, or hexadecimal format.</span></span> <span data-ttu-id="76a30-125">Para ser compatible con Windows de 16 bits, los enteros se almacenan como valores de WORD.</span><span class="sxs-lookup"><span data-stu-id="76a30-125">To be compatible with 16-bit Windows, integers are stored as WORD values.</span></span> <span data-ttu-id="76a30-126">Puede almacenar un entero como valor DWORD si califica el entero con el sufijo "L".</span><span class="sxs-lookup"><span data-stu-id="76a30-126">You can store an integer as a DWORD value by qualifying the integer with the "L" suffix.</span></span>

<span data-ttu-id="76a30-127">Las cadenas se incluyen entre comillas.</span><span class="sxs-lookup"><span data-stu-id="76a30-127">Strings are enclosed in quotation marks.</span></span> <span data-ttu-id="76a30-128">RC no anexa automáticamente un carácter nulo de terminación a una cadena.</span><span class="sxs-lookup"><span data-stu-id="76a30-128">RC does not automatically append a terminating null character to a string.</span></span> <span data-ttu-id="76a30-129">Cada cadena es una secuencia de los caracteres ANSI especificados, a menos que la califique como una cadena de caracteres anchos con el prefijo "L".</span><span class="sxs-lookup"><span data-stu-id="76a30-129">Each string is a sequence of the specified ANSI characters, unless you qualify it as a wide-character string with the "L" prefix.</span></span>

<span data-ttu-id="76a30-130">El bloque de datos comienza en un límite **DWORD** y RC no realiza ningún relleno ni alineación de los datos en el bloque de *datos sin procesar* .</span><span class="sxs-lookup"><span data-stu-id="76a30-130">The block of data begins on a **DWORD** boundary and RC performs no padding or alignment of data within the *raw-data* block.</span></span> <span data-ttu-id="76a30-131">Es responsabilidad del programador garantizar la correcta alineación de los datos dentro del bloque.</span><span class="sxs-lookup"><span data-stu-id="76a30-131">It is the programmer's responsibility to ensure the proper alignment of data within the block.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="76a30-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="76a30-132">Example</span></span>

<span data-ttu-id="76a30-133">En el ejemplo siguiente se muestran varias instrucciones definidas por el usuario:</span><span class="sxs-lookup"><span data-stu-id="76a30-133">The following example shows several user-defined statements:</span></span>

``` syntax
array   MYRES   data.res
14      300     custom.res
18 MYRES2
{
   "Here is an ANSI string\0",    // explicitly null-terminated 
   L"Here is a Unicode string\0", // explicitly null-terminated 
   1024,                          // integer, stored as WORD 
   7L,                            // integer, stored as DWORD 
   0x029a,                        // hex integer 
   0o733,                         // octal integer 
}
```

 

 




