---
description: La función PdhVbGetCounterPathElements analiza una cadena de ruta de acceso de contador de rendimiento completa en sus elementos individuales.
ms.assetid: 5459c7dd-e8b6-48cd-a33f-cafdc64dd9ee
title: PdhVbGetCounterPathElements función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetCounterPathElements
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 003374141b0454d730ba4b844715bd6f00b544da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667313"
---
# <a name="pdhvbgetcounterpathelements-function"></a><span data-ttu-id="5645b-103">PdhVbGetCounterPathElements función)</span><span class="sxs-lookup"><span data-stu-id="5645b-103">PdhVbGetCounterPathElements function</span></span>

<span data-ttu-id="5645b-104">La función **PdhVbGetCounterPathElements** analiza una cadena de ruta de acceso de contador de rendimiento completa en sus elementos individuales.</span><span class="sxs-lookup"><span data-stu-id="5645b-104">The **PdhVbGetCounterPathElements** function parses a fully qualified performance counter path string into its individual elements.</span></span> <span data-ttu-id="5645b-105">Cada una de las variables de cadena debe tener el mismo tamaño (*BufferSize*) y estar dimensionada e inicializada antes de que se use en esta función.</span><span class="sxs-lookup"><span data-stu-id="5645b-105">Each of the string variables must be the same size (*BufferSize*) and dimensioned and initialized before it is used in this function.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5645b-106">La función que se describe en este tema puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="5645b-106">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="5645b-107">En su lugar, Microsoft recomienda que use las funciones descritas en [funciones de contadores de rendimiento](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="5645b-107">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="5645b-108">Function PdhVbGetCounterPathElements ( \_ ByVal PathString As String, \_ ByVal MachineName As String, \_ ByVal objectname As String, \_ ByVal nombreDeInstancia As String, \_ ByVal ParentInstance As String, \_ ByVal Contraname As String, \_ ByVal BufferSize as Long \_ ) as Long</span><span class="sxs-lookup"><span data-stu-id="5645b-108">Function PdhVbGetCounterPathElements( \_ ByVal PathString As String, \_ ByVal MachineName As String, \_ ByVal ObjectName As String, \_ ByVal InstanceName As String, \_ ByVal ParentInstance As String, \_ ByVal CounterName As String, \_ ByVal BufferSize As Long \_ ) As Long</span></span>

## <a name="parameters"></a><span data-ttu-id="5645b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5645b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5645b-110">*PathString*</span><span class="sxs-lookup"><span data-stu-id="5645b-110">*PathString*</span></span> 
</dt> <dd>

<span data-ttu-id="5645b-111">Cadena de ruta de acceso de contador que se va a dividir en sus elementos individuales.</span><span class="sxs-lookup"><span data-stu-id="5645b-111">Counter path string that is to be broken up into its individual elements.</span></span>

</dd> <dt>

<span data-ttu-id="5645b-112">*MachineName*</span><span class="sxs-lookup"><span data-stu-id="5645b-112">*MachineName*</span></span> 
</dt> <dd>

<span data-ttu-id="5645b-113">Cadena que recibirá el nombre del equipo.</span><span class="sxs-lookup"><span data-stu-id="5645b-113">String to receive the computer name.</span></span>

</dd> <dt>

<span data-ttu-id="5645b-114">*ObjectName*</span><span class="sxs-lookup"><span data-stu-id="5645b-114">*ObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="5645b-115">Cadena que va a recibir el nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="5645b-115">String to receive the object name.</span></span>

</dd> <dt>

<span data-ttu-id="5645b-116">*InstanceName*</span><span class="sxs-lookup"><span data-stu-id="5645b-116">*InstanceName*</span></span> 
</dt> <dd>

<span data-ttu-id="5645b-117">Cadena que recibirá el nombre de instancia, si se utiliza.</span><span class="sxs-lookup"><span data-stu-id="5645b-117">String to receive the instance name, if used.</span></span>

</dd> <dt>

<span data-ttu-id="5645b-118">*ParentInstance*</span><span class="sxs-lookup"><span data-stu-id="5645b-118">*ParentInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="5645b-119">Cadena que recibirá la instancia primaria, si se utiliza.</span><span class="sxs-lookup"><span data-stu-id="5645b-119">String to receive the parent instance, if used.</span></span>

</dd> <dt>

<span data-ttu-id="5645b-120">*CounterName*</span><span class="sxs-lookup"><span data-stu-id="5645b-120">*CounterName*</span></span> 
</dt> <dd>

<span data-ttu-id="5645b-121">Cadena que va a recibir el nombre del contador.</span><span class="sxs-lookup"><span data-stu-id="5645b-121">String to receive the counter name.</span></span>

</dd> <dt>

<span data-ttu-id="5645b-122">*BufferSize*</span><span class="sxs-lookup"><span data-stu-id="5645b-122">*BufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="5645b-123">Tamaño máximo de cada variable de cadena utilizada como parámetro para esta llamada de función.</span><span class="sxs-lookup"><span data-stu-id="5645b-123">Maximum size of each string variable used as a parameter to this function call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5645b-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5645b-124">Return value</span></span>

<span data-ttu-id="5645b-125">Si la función se ejecuta correctamente, devuelve un entero **largo** igual a error de \_ éxito.</span><span class="sxs-lookup"><span data-stu-id="5645b-125">If the function succeeds, it returns a **Long** integer equal to ERROR\_SUCCESS.</span></span>

<span data-ttu-id="5645b-126">Si se produce un error en la función, el valor devuelto es un [código de error del sistema](/windows/desktop/Debug/system-error-codes) o un [código de error de PDH](pdh-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="5645b-126">If the function fails, the return value is a [system error code](/windows/desktop/Debug/system-error-codes) or a [PDH error code](pdh-error-codes.md).</span></span> <span data-ttu-id="5645b-127">Los valores posibles son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="5645b-127">The following are possible values.</span></span>



| <span data-ttu-id="5645b-128">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="5645b-128">Return code</span></span>                                                                                                     | <span data-ttu-id="5645b-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="5645b-129">Description</span></span>                                                                                    |
|-----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5645b-130"><dt>**PDH \_ argumento no válido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5645b-130"><dt>**PDH\_INVALID\_ARGUMENT**</dt></span></span> </dl>           | <span data-ttu-id="5645b-131">Uno o varios de los búferes de cadena no tienen el tamaño correcto.</span><span class="sxs-lookup"><span data-stu-id="5645b-131">One or more of the string buffers is not the correct size.</span></span><br/>                          |
| <dl> <span data-ttu-id="5645b-132"><dt>**PDH \_ más \_ datos**</dt></span><span class="sxs-lookup"><span data-stu-id="5645b-132"><dt>**PDH\_MORE\_DATA**</dt></span></span> </dl>                  | <span data-ttu-id="5645b-133">Uno o varios de los elementos de la ruta de acceso del contador son demasiado grandes para la longitud del búfer de retorno.</span><span class="sxs-lookup"><span data-stu-id="5645b-133">One or more of the counter path elements is too large for the return buffer length.</span></span><br/> |
| <dl> <span data-ttu-id="5645b-134"><dt>**\_error de \_ asignación de memoria de PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5645b-134"><dt>**PDH\_MEMORY\_ALLOCATION\_FAILURE**</dt></span></span> </dl> | <span data-ttu-id="5645b-135">No se pudo asignar un búfer de memoria temporal.</span><span class="sxs-lookup"><span data-stu-id="5645b-135">A temporary memory buffer could not be allocated.</span></span><br/>                                   |



 

## <a name="requirements"></a><span data-ttu-id="5645b-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5645b-136">Requirements</span></span>



| <span data-ttu-id="5645b-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="5645b-137">Requirement</span></span> | <span data-ttu-id="5645b-138">Value</span><span class="sxs-lookup"><span data-stu-id="5645b-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5645b-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5645b-139">Minimum supported client</span></span><br/> | <span data-ttu-id="5645b-140">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="5645b-140">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5645b-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5645b-141">Minimum supported server</span></span><br/> | <span data-ttu-id="5645b-142">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5645b-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5645b-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5645b-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="5645b-144"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5645b-144"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="5645b-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5645b-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5645b-146"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5645b-146"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5645b-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="5645b-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5645b-148">**PdhVbCreateCounterPathList**</span><span class="sxs-lookup"><span data-stu-id="5645b-148">**PdhVbCreateCounterPathList**</span></span>](pdhvbcreatecounterpathlist.md)
</dt> <dt>

[<span data-ttu-id="5645b-149">**PdhVbGetCounterPathFromList**</span><span class="sxs-lookup"><span data-stu-id="5645b-149">**PdhVbGetCounterPathFromList**</span></span>](pdhvbgetcounterpathfromlist.md)
</dt> <dt>

[<span data-ttu-id="5645b-150">**PdhVbGetOneCounterPath**</span><span class="sxs-lookup"><span data-stu-id="5645b-150">**PdhVbGetOneCounterPath**</span></span>](pdhvbgetonecounterpath.md)
</dt> </dl>

 

