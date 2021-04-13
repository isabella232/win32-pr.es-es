---
title: /error (modificador)
description: El modificador/error determina los tipos de comprobación de errores que realizará el código auxiliar generado en tiempo de ejecución.
ms.assetid: abd3616a-2d2c-4a7d-bf3a-c84a43387894
keywords:
- /error switch MIDL
topic_type:
- apiref
api_name:
- /error
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f84a56c1ae3d57ab1931ec175aa8dc9010ea6b8a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419652"
---
# <a name="error-switch"></a><span data-ttu-id="8d91d-104">/error (modificador)</span><span class="sxs-lookup"><span data-stu-id="8d91d-104">/error switch</span></span>

<span data-ttu-id="8d91d-105">El modificador **/error** determina los tipos de comprobación de errores que realizará el código auxiliar generado en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="8d91d-105">The **/error** switch determines the types of error checking that the generated stubs will perform at run time.</span></span>

> [!Note]  
> <span data-ttu-id="8d91d-106">Esta característica está obsoleta y ya no se admite.</span><span class="sxs-lookup"><span data-stu-id="8d91d-106">This feature is obsolete and no longer supported.</span></span> <span data-ttu-id="8d91d-107">Se recomienda el uso del modificador [**/Robust**](-robust.md) .</span><span class="sxs-lookup"><span data-stu-id="8d91d-107">The use of the [**/robust**](-robust.md) switch is recommended.</span></span>

 

``` syntax
midl /error { allocation | stub_data | ref | bounds_check | none | all }
```

## <a name="switch-options"></a><span data-ttu-id="8d91d-108">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="8d91d-108">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="allocation"></span><span id="ALLOCATION"></span>

<span data-ttu-id="8d91d-109"><span id="allocation"></span><span id="ALLOCATION"></span>asignación \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="8d91d-109"><span id="allocation"></span><span id="ALLOCATION"></span>\*\*\*\*allocation\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="8d91d-110">Comprueba si el usuario de la [**\_ \_ asignación de MIDL**](midl-user-allocate-1.md) devuelve un valor **null** , lo que indica un error de memoria insuficiente.</span><span class="sxs-lookup"><span data-stu-id="8d91d-110">Checks whether [**midl\_user\_allocate**](midl-user-allocate-1.md) returns a **NULL** value, indicating an out-of-memory error.</span></span>

</dd> <dt>

<span id="stub_data"></span><span id="STUB_DATA"></span>

<span data-ttu-id="8d91d-111"><span id="stub_data"></span><span id="STUB_DATA"></span>datos de código auxiliar \* \* \* \* \_</span><span class="sxs-lookup"><span data-stu-id="8d91d-111"><span id="stub_data"></span><span id="STUB_DATA"></span>\*\*\*\*stub\_data\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="8d91d-112">Genera un código auxiliar que detecta las excepciones de cálculo de referencias en el lado del servidor y los propaga de nuevo al cliente.</span><span class="sxs-lookup"><span data-stu-id="8d91d-112">Generates a stub that catches unmarshaling exceptions on the server side and propagates them back to the client.</span></span>

</dd> <dt>

<span id="ref"></span><span id="REF"></span>

<span data-ttu-id="8d91d-113"><span id="ref"></span><span id="REF"></span>Ref \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="8d91d-113"><span id="ref"></span><span id="REF"></span>\*\*\*\*ref\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="8d91d-114">Genera código que ejecuta una comprobación en tiempo de ejecución para garantizar que no se pasen punteros de referencia **nulos** al código auxiliar del cliente y genere una excepción de puntero de referencia null de RPC \_ X \_ \_ \_ si encuentra alguna.</span><span class="sxs-lookup"><span data-stu-id="8d91d-114">Generates code that runs a check at run time to ensure that no **NULL** reference pointers are being passed to the client stubs and raises an RPC\_X\_NULL\_REF\_POINTER exception if it finds any.</span></span>

</dd> <dt>

<span id="bounds_check"></span><span id="BOUNDS_CHECK"></span>

<span data-ttu-id="8d91d-115"><span id="bounds_check"></span><span id="BOUNDS_CHECK"></span>comprobación de límites \* \* \* \* \_</span><span class="sxs-lookup"><span data-stu-id="8d91d-115"><span id="bounds_check"></span><span id="BOUNDS_CHECK"></span>\*\*\*\*bounds\_check\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="8d91d-116">Comprueba el tamaño de las matrices variables y variables conformes con la especificación de longitud de transmisión.</span><span class="sxs-lookup"><span data-stu-id="8d91d-116">Checks size of conformant-varying and varying arrays against transmission length specification.</span></span>

</dd> <dt>

<span id="none"></span><span id="NONE"></span>

<span data-ttu-id="8d91d-117"><span id="none"></span><span id="NONE"></span>ninguno \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="8d91d-117"><span id="none"></span><span id="NONE"></span>\*\*\*\*none\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="8d91d-118">No realiza ninguna comprobación de errores.</span><span class="sxs-lookup"><span data-stu-id="8d91d-118">Performs no error checking.</span></span>

</dd> <dt>

<span id="all"></span><span id="ALL"></span>

<span data-ttu-id="8d91d-119"><span id="all"></span><span id="ALL"></span>todo \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="8d91d-119"><span id="all"></span><span id="ALL"></span>\*\*\*\*all\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="8d91d-120">Realiza todas las comprobaciones de errores.</span><span class="sxs-lookup"><span data-stu-id="8d91d-120">Performs all error checking.</span></span> <span data-ttu-id="8d91d-121">A partir de la versión 5,0 de MIDL, se trata de un modificador de compilador predeterminado.</span><span class="sxs-lookup"><span data-stu-id="8d91d-121">Effective with MIDL version 5.0, this is a default compiler switch.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8d91d-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8d91d-122">Remarks</span></span>

<span data-ttu-id="8d91d-123">El modificador **/error** selecciona el número de comprobaciones de errores que realizarán los archivos stub generados.</span><span class="sxs-lookup"><span data-stu-id="8d91d-123">The **/error** switch selects the number of error checks that the generated stub files will perform.</span></span> <span data-ttu-id="8d91d-124">A partir de la versión 5,0 de MIDL, el valor predeterminado es **/error All**.</span><span class="sxs-lookup"><span data-stu-id="8d91d-124">Effective with MIDL version 5.0, the default setting is **/error all**.</span></span>

<span data-ttu-id="8d91d-125">Los errores de enumeración que se comprueban (de forma predeterminada en todas las versiones de MIDL) son errores de truncamiento producidos al convertir entre tipos de **enumeración largos** (enteros de 32 bits) y tipos de **enumeración cortos** (la representación de datos de red de [**enum**](enum.md)) y el número de identificadores en una enumeración que supera 32.767.</span><span class="sxs-lookup"><span data-stu-id="8d91d-125">The enum errors that are checked (by default in all versions of MIDL) are truncation errors caused when converting between **long enum** types (32-bit integers) and **short enum** types (the network-data representation of [**enum**](enum.md)), and the number of identifiers in an enumeration exceeding 32,767.</span></span>

<span data-ttu-id="8d91d-126">La comprobación de errores de acceso a memoria (también de forma predeterminada en todas las versiones de MIDL) es para punteros que superan el final del búfer en el cálculo de referencias de código y para matrices compatibles cuyo tamaño es menor que cero.</span><span class="sxs-lookup"><span data-stu-id="8d91d-126">The memory-access error checking (also by default in all versions of MIDL) is for pointers that exceed the end of the buffer in marshaling code and for conformant arrays whose size is less than zero.</span></span> <span data-ttu-id="8d91d-127">Use la marca de **\_ comprobación** de los límites de/error para buscar otros límites de matriz no válidos.</span><span class="sxs-lookup"><span data-stu-id="8d91d-127">Use the **/error bounds\_check** flag to check for other invalid array bounds.</span></span>

<span data-ttu-id="8d91d-128">Cuando se especifica **/error Allocation**, los códigos auxiliares incluyen código que genera una excepción cuando el usuario de la [**\_ \_ asignación de MIDL**](midl-user-allocate-1.md) devuelve 0.</span><span class="sxs-lookup"><span data-stu-id="8d91d-128">When you specify **/error allocation**, the stubs include code that raises an exception when [**midl\_user\_allocate**](midl-user-allocate-1.md) returns 0.</span></span>

<span data-ttu-id="8d91d-129">La opción **/error stub \_ Data** evita que los datos del cliente bloqueen el servidor durante la desserialización, lo que proporciona eficazmente un método más eficaz para controlar la operación de desserialización.</span><span class="sxs-lookup"><span data-stu-id="8d91d-129">The **/error stub\_data** option prevents client data from crashing the server during unmarshaling, effectively providing a more robust method of handling the unmarshaling operation.</span></span>

<span data-ttu-id="8d91d-130">En vigor con Windows 2000, el motor de serialización de NDR en tiempo de ejecución subyacente realiza la mayoría de estas comprobaciones.</span><span class="sxs-lookup"><span data-stu-id="8d91d-130">Effective with WindowsÂ 2000, the underlying run-time NDR marshaling engine performs most of these checks.</span></span> <span data-ttu-id="8d91d-131">Esto significa que, si usa uno de los modos que se interpretan totalmente ([**/OI**](-oi.md), **/OIF**) de la generación de código auxiliar, la elección de distintas opciones de comprobación de errores no tendrá ningún efecto marcado en el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="8d91d-131">This means that if you are using one of the fully-interpreted modes ([**/Oi**](-oi.md), **/Oif**) of stub generation, choosing different error checking options will not have a marked effect on performance.</span></span>

## <a name="examples"></a><span data-ttu-id="8d91d-132">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8d91d-132">Examples</span></span>

<span data-ttu-id="8d91d-133">**MIDL/error enasignación FILENAME. idl**</span><span class="sxs-lookup"><span data-stu-id="8d91d-133">**midl /error allocation filename.idl**</span></span>

<span data-ttu-id="8d91d-134">**MIDL/error None nombreDeArchivo. idl**</span><span class="sxs-lookup"><span data-stu-id="8d91d-134">**midl /error none filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="8d91d-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="8d91d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d91d-136">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="8d91d-136">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="8d91d-137">**/Robust**</span><span class="sxs-lookup"><span data-stu-id="8d91d-137">**/robust**</span></span>](-robust.md)
</dt> </dl>

 

 




