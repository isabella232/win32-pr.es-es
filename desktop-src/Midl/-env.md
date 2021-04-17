---
title: parámetro/env
description: El modificador/env selecciona el entorno en el que se ejecuta la aplicación.
ms.assetid: 70a548c8-fdc3-48f3-a865-14ba9b29fb02
keywords:
- /ENV (modificador) MIDL
topic_type:
- apiref
api_name:
- /env
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59da7185900d4b75781916bd6b4a9d70bf39dc85
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420582"
---
# <a name="env-switch"></a><span data-ttu-id="5937c-104">parámetro/env</span><span class="sxs-lookup"><span data-stu-id="5937c-104">/env switch</span></span>

<span data-ttu-id="5937c-105">El modificador **/env** selecciona el entorno en el que se ejecuta la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5937c-105">The **/env** switch selects the environment in which the application runs.</span></span>

``` syntax
midl /env { win32 | ia64 | amd64 | win64 }
```

## <a name="switch-options"></a><span data-ttu-id="5937c-106">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="5937c-106">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="win32"></span><span id="WIN32"></span>

<span data-ttu-id="5937c-107"><span id="win32"></span><span id="WIN32"></span>Win32 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="5937c-107"><span id="win32"></span><span id="WIN32"></span>\*\*\*\*win32\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="5937c-108">Indica al compilador de MIDL que genere archivos de código auxiliar, o un archivo de biblioteca de tipos, para un entorno de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="5937c-108">Directs the MIDL compiler to generate stub files, or a type library file, for a 32-bit environment.</span></span>

</dd> <dt>

<span id="ia64"></span><span id="IA64"></span>

<span data-ttu-id="5937c-109"><span id="ia64"></span><span id="IA64"></span>ia64 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="5937c-109"><span id="ia64"></span><span id="IA64"></span>\*\*\*\*ia64\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="5937c-110">Indica al compilador de MIDL que genere archivos de código auxiliar, o un archivo de biblioteca de tipos, para un entorno de arquitectura Intel 64 bits (IA64).</span><span class="sxs-lookup"><span data-stu-id="5937c-110">Directs the MIDL compiler to generate stub files, or a type library file, for a Intel Architecture 64-bit (IA64) environment.</span></span>

</dd> <dt>

<span id="amd64"></span><span id="AMD64"></span>

<span data-ttu-id="5937c-111"><span id="amd64"></span><span id="AMD64"></span>AMD64 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="5937c-111"><span id="amd64"></span><span id="AMD64"></span>\*\*\*\*amd64\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="5937c-112">Indica al compilador de MIDL que genere archivos de código auxiliar, o un archivo de biblioteca de tipos, para un entorno de micro de64 Vices (AMD64) avanzado.</span><span class="sxs-lookup"><span data-stu-id="5937c-112">Directs the MIDL compiler to generate stub files, or a type library file, for an Advanced Micro Devices 64-bit (AMD64) environment.</span></span>

</dd> <dt>

<span id="win64"></span><span id="WIN64"></span>

<span data-ttu-id="5937c-113"><span id="win64"></span><span id="WIN64"></span>Win64 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="5937c-113"><span id="win64"></span><span id="WIN64"></span>\*\*\*\*win64\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="5937c-114">Mismo comportamiento que *ia64*.</span><span class="sxs-lookup"><span data-stu-id="5937c-114">Same behavior as *ia64*.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5937c-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5937c-115">Remarks</span></span>

<span data-ttu-id="5937c-116">El modificador **/env** afecta principalmente al nivel de empaquetado utilizado para las estructuras de ese entorno.</span><span class="sxs-lookup"><span data-stu-id="5937c-116">The **/env** switch primarily affects the packing level used for structures in that environment.</span></span> <span data-ttu-id="5937c-117">Asegúrese de especificar la misma configuración de nivel de empaquetado para el compilador de MIDL y el compilador de C.</span><span class="sxs-lookup"><span data-stu-id="5937c-117">Be sure you specify the same packing-level setting for both the MIDL compiler and the C compiler.</span></span>

<span data-ttu-id="5937c-118">El modificador **/env** determina el nivel de empaquetado y otras opciones de configuración como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="5937c-118">The **/env** switch determines the packing level and other settings as follows:</span></span>

-   <span data-ttu-id="5937c-119">Cuando se especifica **Win32**, el código auxiliar generado usa el nivel de empaquetado del compilador de C para todos los tipos implicados en las operaciones remotas.</span><span class="sxs-lookup"><span data-stu-id="5937c-119">When you specify **win32**, generated stubs use C-compiler packing-level 8 for all types involved in remote operations.</span></span> <span data-ttu-id="5937c-120">Los tipos de datos [**int**](int.md) son de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="5937c-120">The [**int**](int.md) data types are both 32 bits.</span></span> <span data-ttu-id="5937c-121">Los punteros son de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="5937c-121">Pointers are 32 bits.</span></span>
-   <span data-ttu-id="5937c-122">Cuando se especifica **ia64** o **AMD64**, el compilador MIDL se ejecuta en modo de compilador cruzado para la plataforma indicada (Intel o AMD) 64 bits.</span><span class="sxs-lookup"><span data-stu-id="5937c-122">When you specify **ia64** or **amd64**, the MIDL compiler runs in a cross-compiler mode for the indicated (Intel or AMD) 64-bit platform.</span></span> <span data-ttu-id="5937c-123">El código auxiliar generado usa el nivel de empaquetado del compilador C 8 para todos los tipos implicados en las operaciones remotas.</span><span class="sxs-lookup"><span data-stu-id="5937c-123">The generated stubs use C-compiler packing-level 8 for all types involved in remote operations.</span></span> <span data-ttu-id="5937c-124">Los tipos de datos [**Long**](long.md) e [**int**](int.md) son de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="5937c-124">The [**long**](long.md) and [**int**](int.md) data types are 32 bits.</span></span> <span data-ttu-id="5937c-125">Los punteros son de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="5937c-125">Pointers are 64 bits.</span></span>

<span data-ttu-id="5937c-126">Los modificadores [**/align**](-align.md), [**/Pack**](-pack.md)y [**/ZP**](-zp.md) tienen prioridad sobre la configuración de **/env** .</span><span class="sxs-lookup"><span data-stu-id="5937c-126">The [**/align**](-align.md), [**/pack**](-pack.md), and [**/Zp**](-zp.md) switches take precedence over the **/env** settings.</span></span>

<span data-ttu-id="5937c-127">Para obtener más información sobre la compatibilidad con 64 bits para MIDL y RPC, vea [diseñar interfaces compatibles con 64 bits](/windows/desktop/WinProg64/designing-64-bit-compatible-interfaces).</span><span class="sxs-lookup"><span data-stu-id="5937c-127">For more information on 64 bit support for MIDL and RPC see [Designing 64-bit-Compatible Interfaces](/windows/desktop/WinProg64/designing-64-bit-compatible-interfaces).</span></span>

## <a name="examples"></a><span data-ttu-id="5937c-128">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="5937c-128">Examples</span></span>

<span data-ttu-id="5937c-129">**MIDL/env Win32 FILENAME. idl**</span><span class="sxs-lookup"><span data-stu-id="5937c-129">**midl /env win32 filename.idl**</span></span>

<span data-ttu-id="5937c-130">**MIDL/env ia64 nombreDeArchivo. idl**</span><span class="sxs-lookup"><span data-stu-id="5937c-130">**midl /env ia64 filename.idl**</span></span>

<span data-ttu-id="5937c-131">**MIDL/env AMD64 nombreDeArchivo. idl**</span><span class="sxs-lookup"><span data-stu-id="5937c-131">**midl /env amd64 filename.idl**</span></span>

<span data-ttu-id="5937c-132">**MIDL/env Win64 nombreDeArchivo. idl**</span><span class="sxs-lookup"><span data-stu-id="5937c-132">**midl /env win64 filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="5937c-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="5937c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5937c-134">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="5937c-134">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="5937c-135">**/Pack**</span><span class="sxs-lookup"><span data-stu-id="5937c-135">**/pack**</span></span>](-pack.md)
</dt> <dt>

[<span data-ttu-id="5937c-136">**/ZP**</span><span class="sxs-lookup"><span data-stu-id="5937c-136">**/Zp**</span></span>](-zp.md)
</dt> </dl>

 

 