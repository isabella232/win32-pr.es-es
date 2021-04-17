---
description: La función PdhVbAddCounter crea una entrada de contador en el objeto de consulta especificado y devuelve un identificador a ese contador después de la finalización correcta.
ms.assetid: 20a9e6cd-bf0d-497d-b660-88e786e2f004
title: PdhVbAddCounter función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbAddCounter
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 19f97abeec74af0d08f340b70aa139e1bec7bf1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667315"
---
# <a name="pdhvbaddcounter-function"></a><span data-ttu-id="72665-103">PdhVbAddCounter función)</span><span class="sxs-lookup"><span data-stu-id="72665-103">PdhVbAddCounter function</span></span>

<span data-ttu-id="72665-104">La función **PdhVbAddCounter** crea una entrada de contador en el objeto de consulta especificado y devuelve un identificador a ese contador después de la finalización correcta.</span><span class="sxs-lookup"><span data-stu-id="72665-104">The **PdhVbAddCounter** function creates a counter entry in the specified query object, and returns a handle to that counter upon successful completion.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="72665-105">La función que se describe en este tema puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="72665-105">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="72665-106">En su lugar, Microsoft recomienda que use las funciones descritas en [funciones de contadores de rendimiento](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="72665-106">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="72665-107">Función PdhVbAddCounter ( \_ ByVal QueryHandle as Long, \_ ByVal Perpath As String, \_ ByVal contrahandle as Long \_ ) as Long</span><span class="sxs-lookup"><span data-stu-id="72665-107">Function PdhVbAddCounter( \_ ByVal QueryHandle As Long, \_ ByVal CounterPath As String, \_ ByVal CounterHandle As Long \_ ) As Long</span></span>

## <a name="parameters"></a><span data-ttu-id="72665-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="72665-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72665-109">*QueryHandle*</span><span class="sxs-lookup"><span data-stu-id="72665-109">*QueryHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="72665-110">IDENTIFICADOR de la consulta a la que se va a asignar este contador.</span><span class="sxs-lookup"><span data-stu-id="72665-110">ID of the query to which this counter is to be assigned.</span></span> <span data-ttu-id="72665-111">La función [**PdhVbOpenQuery**](pdhvbopenquery.md) devuelve este valor.</span><span class="sxs-lookup"><span data-stu-id="72665-111">This value is returned by the [**PdhVbOpenQuery**](pdhvbopenquery.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="72665-112">*CounterPath*</span><span class="sxs-lookup"><span data-stu-id="72665-112">*CounterPath*</span></span> 
</dt> <dd>

<span data-ttu-id="72665-113">Cadena de texto que especifica el nombre de la ruta de acceso del contador que se va a agregar a la consulta.</span><span class="sxs-lookup"><span data-stu-id="72665-113">Text string that specifies the name of the counter path to add to the query.</span></span> <span data-ttu-id="72665-114">El contenido de esta cadena debe ser una ruta de acceso de contador válida, como se obtiene del explorador de contadores u otro origen.</span><span class="sxs-lookup"><span data-stu-id="72665-114">The contents of this string must be a valid counter path, as obtained from the counter browser or other source.</span></span>

</dd> <dt>

<span data-ttu-id="72665-115">*Control de contracargo*</span><span class="sxs-lookup"><span data-stu-id="72665-115">*CounterHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="72665-116">Referencia única que identifica este contador en la consulta.</span><span class="sxs-lookup"><span data-stu-id="72665-116">Unique reference that identifies this counter in the query.</span></span> <span data-ttu-id="72665-117">Esta variable se debe inicializar en cero antes de que se llame a la función.</span><span class="sxs-lookup"><span data-stu-id="72665-117">This variable must be initialized to zero before the function is called.</span></span> <span data-ttu-id="72665-118">Contiene un valor válido en la devolución solo si la función se completa correctamente.</span><span class="sxs-lookup"><span data-stu-id="72665-118">It contains a valid value on return only if the function completes successfully.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72665-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="72665-119">Return value</span></span>

<span data-ttu-id="72665-120">Si la función se ejecuta correctamente, devuelve un entero **largo** igual a error \_ correcto y un nuevo identificador en la variable de control de *supercontrolador* .</span><span class="sxs-lookup"><span data-stu-id="72665-120">If the function succeeds, it returns a **Long** integer equal to ERROR\_SUCCESS and a new handle in the *CounterHandle* variable.</span></span>

<span data-ttu-id="72665-121">Si se produce un error en la función, el valor devuelto es un [código de error del sistema](/windows/desktop/Debug/system-error-codes) o un [código de error de PDH](pdh-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="72665-121">If the function fails, the return value is a [system error code](/windows/desktop/Debug/system-error-codes) or a [PDH error code](pdh-error-codes.md).</span></span> <span data-ttu-id="72665-122">Los valores posibles son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="72665-122">The following are possible values.</span></span>



| <span data-ttu-id="72665-123">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="72665-123">Return code</span></span>                                                                                                     | <span data-ttu-id="72665-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="72665-124">Description</span></span>                                                                   |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="72665-125"><dt>**PDH \_ argumento no válido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="72665-125"><dt>**PDH\_INVALID\_ARGUMENT**</dt></span></span> </dl>           | <span data-ttu-id="72665-126">Uno o varios argumentos no son válidos o son incorrectos.</span><span class="sxs-lookup"><span data-stu-id="72665-126">One or more of the arguments is invalid or incorrect.</span></span><br/>              |
| <dl> <span data-ttu-id="72665-127"><dt>**\_error de \_ asignación de memoria de PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="72665-127"><dt>**PDH\_MEMORY\_ALLOCATION\_FAILURE**</dt></span></span> </dl> | <span data-ttu-id="72665-128">No se pudo asignar un búfer de memoria.</span><span class="sxs-lookup"><span data-stu-id="72665-128">A memory buffer could not be allocated.</span></span><br/>                            |
| <dl> <span data-ttu-id="72665-129"><dt>**\_identificador no válido de PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="72665-129"><dt>**PDH\_INVALID\_HANDLE**</dt></span></span> </dl>             | <span data-ttu-id="72665-130">El identificador de consulta no es válido.</span><span class="sxs-lookup"><span data-stu-id="72665-130">The query handle is not valid.</span></span><br/>                                     |
| <dl> <span data-ttu-id="72665-131"><dt>**\_CSTATUS \_ no \_ contador de PDH**</dt></span><span class="sxs-lookup"><span data-stu-id="72665-131"><dt>**PDH\_CSTATUS\_NO\_COUNTER**</dt></span></span> </dl>        | <span data-ttu-id="72665-132">No se encontró el contador especificado.</span><span class="sxs-lookup"><span data-stu-id="72665-132">The specified counter was not found.</span></span><br/>                               |
| <dl> <span data-ttu-id="72665-133"><dt>**PDH \_ CSTATUS \_ ningún \_ objeto**</dt></span><span class="sxs-lookup"><span data-stu-id="72665-133"><dt>**PDH\_CSTATUS\_NO\_OBJECT**</dt></span></span> </dl>         | <span data-ttu-id="72665-134">No se encontró el objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="72665-134">The specified object could not be found.</span></span><br/>                           |
| <dl> <span data-ttu-id="72665-135"><dt>**PDH \_ CSTATUS \_ sin \_ equipo**</dt></span><span class="sxs-lookup"><span data-stu-id="72665-135"><dt>**PDH\_CSTATUS\_NO\_MACHINE**</dt></span></span> </dl>        | <span data-ttu-id="72665-136">No se pudo crear una entrada de equipo.</span><span class="sxs-lookup"><span data-stu-id="72665-136">A computer entry could not be created.</span></span><br/>                             |
| <dl> <span data-ttu-id="72665-137"><dt>**\_ \_ nombre incorrecto de PDH CSTATUS \_**</dt></span><span class="sxs-lookup"><span data-stu-id="72665-137"><dt>**PDH\_CSTATUS\_BAD\_COUNTERNAME**</dt></span></span> </dl>   | <span data-ttu-id="72665-138">Se pasó una cadena de ruta de acceso de nombre de contador vacía.</span><span class="sxs-lookup"><span data-stu-id="72665-138">An empty counter name path string was passed in.</span></span><br/>                   |
| <dl> <span data-ttu-id="72665-139"><dt>**\_ \_ no \_ se encontró la función PDH**</dt></span><span class="sxs-lookup"><span data-stu-id="72665-139"><dt>**PDH\_FUNCTION\_NOT\_FOUND**</dt></span></span> </dl>        | <span data-ttu-id="72665-140">No se pudo determinar la función de cálculo para este contador.</span><span class="sxs-lookup"><span data-stu-id="72665-140">The calculation function for this counter could not be determined.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="72665-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72665-141">Requirements</span></span>



| <span data-ttu-id="72665-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="72665-142">Requirement</span></span> | <span data-ttu-id="72665-143">Value</span><span class="sxs-lookup"><span data-stu-id="72665-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="72665-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="72665-144">Minimum supported client</span></span><br/> | <span data-ttu-id="72665-145">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="72665-145">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="72665-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="72665-146">Minimum supported server</span></span><br/> | <span data-ttu-id="72665-147">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="72665-147">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="72665-148">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="72665-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="72665-149"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="72665-149"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="72665-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="72665-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72665-151"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72665-151"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72665-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="72665-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72665-153">**PdhVbOpenQuery**</span><span class="sxs-lookup"><span data-stu-id="72665-153">**PdhVbOpenQuery**</span></span>](pdhvbopenquery.md)
</dt> </dl>

 

