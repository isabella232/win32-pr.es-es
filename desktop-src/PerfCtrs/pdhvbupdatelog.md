---
description: La función PdhVbUpdateLog actualiza la consulta actual y escribe nuevos datos en el archivo de registro. Esta función llama a PdhUpdateLog.
ms.assetid: a7a3ad18-2d61-448e-9764-ba363398e804
title: PdhVbUpdateLog función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbUpdateLog
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: c02e533f57481004b0a7de9f779399b20bddc0af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667303"
---
# <a name="pdhvbupdatelog-function"></a><span data-ttu-id="c2174-104">PdhVbUpdateLog función)</span><span class="sxs-lookup"><span data-stu-id="c2174-104">PdhVbUpdateLog function</span></span>

<span data-ttu-id="c2174-105">La función **PdhVbUpdateLog** actualiza la consulta actual y escribe nuevos datos en el archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="c2174-105">The **PdhVbUpdateLog** function function updates the current query and writes new data to the log file.</span></span> <span data-ttu-id="c2174-106">Esta función llama a [**PdhUpdateLog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga).</span><span class="sxs-lookup"><span data-stu-id="c2174-106">This function calls [**PdhUpdateLog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c2174-107">La función que se describe en este tema puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="c2174-107">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="c2174-108">En su lugar, Microsoft recomienda que use las funciones descritas en [funciones de contadores de rendimiento](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="c2174-108">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="c2174-109">Function PdhVbUpdateLog ( \_ ByVal HLog as PDH \_ hLog, \_ BYVAL szUserString as LPCTSTR \_ )</span><span class="sxs-lookup"><span data-stu-id="c2174-109">Function PdhVbUpdateLog( \_ ByVal hLog As PDH\_HLOG, \_ ByVal szUserString As LPCTSTR \_ )</span></span>

## <a name="parameters"></a><span data-ttu-id="c2174-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c2174-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2174-111">*hLog* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c2174-111">*hLog* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2174-112">Identificador del archivo de registro que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="c2174-112">Handle to the log file to be updated.</span></span> <span data-ttu-id="c2174-113">La función [**PdhVbOpenLog**](pdhvbopenlog.md) devuelve este identificador.</span><span class="sxs-lookup"><span data-stu-id="c2174-113">This handle is returned by the [**PdhVbOpenLog**](pdhvbopenlog.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="c2174-114">*szUserString* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c2174-114">*szUserString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2174-115">Puntero a una cadena que especifica los datos que se van a agregar al archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="c2174-115">Pointer to a string that specifies the data to be added to the log file.</span></span> <span data-ttu-id="c2174-116">Normalmente se utiliza para los comentarios dentro del archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="c2174-116">This is generally used for comments within the log file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2174-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c2174-117">Return value</span></span>

<span data-ttu-id="c2174-118">Si la función se ejecuta correctamente, devuelve 0.</span><span class="sxs-lookup"><span data-stu-id="c2174-118">If the function succeeds, it returns 0.</span></span>

<span data-ttu-id="c2174-119">Si se produce un error en la función, el valor devuelto es un [código de error del sistema](/windows/desktop/Debug/system-error-codes) o un [código de error de PDH](pdh-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="c2174-119">If the function fails, the return value is a [system error code](/windows/desktop/Debug/system-error-codes) or a [PDH error code](pdh-error-codes.md).</span></span> <span data-ttu-id="c2174-120">Los valores posibles son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="c2174-120">The following are possible values.</span></span>



| <span data-ttu-id="c2174-121">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c2174-121">Return code</span></span>                                                                                                | <span data-ttu-id="c2174-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2174-122">Description</span></span>                                                                                            |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c2174-123"><dt>**\_búfer insuficiente de PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c2174-123"><dt>**PDH\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl>   | <span data-ttu-id="c2174-124">Los datos solicitados son mayores que el búfer proporcionado.</span><span class="sxs-lookup"><span data-stu-id="c2174-124">The requested data is larger than the buffer supplied.</span></span> <span data-ttu-id="c2174-125">No se pueden devolver los datos solicitados.</span><span class="sxs-lookup"><span data-stu-id="c2174-125">Unable to return the requested data.</span></span><br/> |
| <dl> <span data-ttu-id="c2174-126"><dt>**PDH \_ argumento no válido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c2174-126"><dt>**PDH\_INVALID\_ARGUMENT**</dt></span></span> </dl>      | <span data-ttu-id="c2174-127">Uno o varios de los búferes de cadena no tienen el tamaño correcto.</span><span class="sxs-lookup"><span data-stu-id="c2174-127">One or more of the string buffers is not the correct size.</span></span><br/>                                  |
| <dl> <span data-ttu-id="c2174-128"><dt>**\_identificador no válido de PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c2174-128"><dt>**PDH\_INVALID\_HANDLE**</dt></span></span> </dl>        | <span data-ttu-id="c2174-129">El identificador no es un objeto PDH válido.</span><span class="sxs-lookup"><span data-stu-id="c2174-129">The handle is not a valid PDH object.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="c2174-130"><dt>**\_ \_ \_ error al abrir el archivo de registro de PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c2174-130"><dt>**PDH\_LOG\_FILE\_OPEN\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="c2174-131">No se puede abrir el archivo de registro especificado.</span><span class="sxs-lookup"><span data-stu-id="c2174-131">Unable to open the specified log file.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="c2174-132"><dt>**\_ \_ no \_ se encontró el archivo PDH**</dt></span><span class="sxs-lookup"><span data-stu-id="c2174-132"><dt>**PDH\_FILE\_NOT\_FOUND**</dt></span></span> </dl>       | <span data-ttu-id="c2174-133">No se puede encontrar el archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="c2174-133">Unable to find the specified file.</span></span><br/>                                                          |



 

## <a name="remarks"></a><span data-ttu-id="c2174-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c2174-134">Remarks</span></span>

<span data-ttu-id="c2174-135">Debe haber una consulta abierta actualmente y deben agregarse los contadores deseados antes de llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="c2174-135">There must be a currently opened query, and the desired counters must be added to it before this function is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2174-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2174-136">Requirements</span></span>



| <span data-ttu-id="c2174-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2174-137">Requirement</span></span> | <span data-ttu-id="c2174-138">Value</span><span class="sxs-lookup"><span data-stu-id="c2174-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c2174-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2174-139">Minimum supported client</span></span><br/> | <span data-ttu-id="c2174-140">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="c2174-140">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c2174-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2174-141">Minimum supported server</span></span><br/> | <span data-ttu-id="c2174-142">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c2174-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c2174-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c2174-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="c2174-144"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c2174-144"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="c2174-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c2174-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2174-146"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2174-146"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2174-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="c2174-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2174-148">**PdhUpdateLog**</span><span class="sxs-lookup"><span data-stu-id="c2174-148">**PdhUpdateLog**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga)
</dt> <dt>

[<span data-ttu-id="c2174-149">**PdhVbGetLogFileSize**</span><span class="sxs-lookup"><span data-stu-id="c2174-149">**PdhVbGetLogFileSize**</span></span>](pdhvbgetlogfilesize.md)
</dt> <dt>

[<span data-ttu-id="c2174-150">**PdhVbOpenLog**</span><span class="sxs-lookup"><span data-stu-id="c2174-150">**PdhVbOpenLog**</span></span>](pdhvbopenlog.md)
</dt> </dl>

 

