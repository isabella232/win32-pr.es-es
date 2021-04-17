---
description: La función PdhVbGetLogFileSize devuelve el tamaño del archivo de registro especificado. Esta función llama a PdhGetLogFileSize.
ms.assetid: 8f4fbb68-b0f5-4163-ae6e-5b7139a35adf
title: PdhVbGetLogFileSize función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetLogFileSize
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 0b9f490477704086bd9aa8c53dd32456d486471e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667309"
---
# <a name="pdhvbgetlogfilesize-function"></a><span data-ttu-id="b5802-104">PdhVbGetLogFileSize función)</span><span class="sxs-lookup"><span data-stu-id="b5802-104">PdhVbGetLogFileSize function</span></span>

<span data-ttu-id="b5802-105">La función **PdhVbGetLogFileSize** devuelve el tamaño del archivo de registro especificado.</span><span class="sxs-lookup"><span data-stu-id="b5802-105">The **PdhVbGetLogFileSize** function returns the size of the specified log file.</span></span> <span data-ttu-id="b5802-106">Esta función llama a [**PdhGetLogFileSize**](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize).</span><span class="sxs-lookup"><span data-stu-id="b5802-106">This function calls [**PdhGetLogFileSize**](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b5802-107">La función que se describe en este tema puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="b5802-107">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="b5802-108">En su lugar, Microsoft recomienda que use las funciones descritas en [funciones de contadores de rendimiento](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="b5802-108">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="b5802-109">Function PdhVbGetLogFileSize ( \_ ByVal HLog as PDH \_ hLog, \_ BYREF llSize as Long \_ ) as DWORD</span><span class="sxs-lookup"><span data-stu-id="b5802-109">Function PdhVbGetLogFileSize( \_ ByVal hLog As PDH\_HLOG, \_ ByRef llSize As LONG \_ ) As DWORD</span></span>

## <a name="parameters"></a><span data-ttu-id="b5802-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b5802-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5802-111">*hLog* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b5802-111">*hLog* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5802-112">Identificador del archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="b5802-112">Handle to the log file.</span></span> <span data-ttu-id="b5802-113">La función [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga) devuelve este identificador.</span><span class="sxs-lookup"><span data-stu-id="b5802-113">This handle is returned by the [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga) function.</span></span>

</dd> <dt>

<span data-ttu-id="b5802-114">*llSize* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b5802-114">*llSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5802-115">Puntero a una variable que recibe el tamaño del archivo de registro, en bytes.</span><span class="sxs-lookup"><span data-stu-id="b5802-115">Pointer to a variable that receives the size of the log file, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5802-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b5802-116">Return value</span></span>

<span data-ttu-id="b5802-117">Si la función se ejecuta correctamente, devuelve 0.</span><span class="sxs-lookup"><span data-stu-id="b5802-117">If the function succeeds, it returns 0.</span></span>

<span data-ttu-id="b5802-118">Si se produce un error en la función, el valor devuelto es un [código de error del sistema](/windows/desktop/Debug/system-error-codes) o un [código de error de PDH](pdh-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="b5802-118">If the function fails, the return value is a [system error code](/windows/desktop/Debug/system-error-codes) or a [PDH error code](pdh-error-codes.md).</span></span> <span data-ttu-id="b5802-119">Los valores posibles son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="b5802-119">The following are possible values.</span></span>



| <span data-ttu-id="b5802-120">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="b5802-120">Return code</span></span>                                                                                                | <span data-ttu-id="b5802-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="b5802-121">Description</span></span>                                                                                            |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b5802-122"><dt>**\_búfer insuficiente de PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b5802-122"><dt>**PDH\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl>   | <span data-ttu-id="b5802-123">Los datos solicitados son mayores que el búfer proporcionado.</span><span class="sxs-lookup"><span data-stu-id="b5802-123">The requested data is larger than the buffer supplied.</span></span> <span data-ttu-id="b5802-124">No se pueden devolver los datos solicitados.</span><span class="sxs-lookup"><span data-stu-id="b5802-124">Unable to return the requested data.</span></span><br/> |
| <dl> <span data-ttu-id="b5802-125"><dt>**PDH \_ argumento no válido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b5802-125"><dt>**PDH\_INVALID\_ARGUMENT**</dt></span></span> </dl>      | <span data-ttu-id="b5802-126">Uno o varios de los búferes de cadena no tienen el tamaño correcto.</span><span class="sxs-lookup"><span data-stu-id="b5802-126">One or more of the string buffers is not the correct size.</span></span><br/>                                  |
| <dl> <span data-ttu-id="b5802-127"><dt>**\_identificador no válido de PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b5802-127"><dt>**PDH\_INVALID\_HANDLE**</dt></span></span> </dl>        | <span data-ttu-id="b5802-128">El identificador no es un objeto PDH válido.</span><span class="sxs-lookup"><span data-stu-id="b5802-128">The handle is not a valid PDH object.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="b5802-129"><dt>**\_ \_ \_ error al abrir el archivo de registro de PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b5802-129"><dt>**PDH\_LOG\_FILE\_OPEN\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="b5802-130">No se puede abrir el archivo de registro especificado.</span><span class="sxs-lookup"><span data-stu-id="b5802-130">Unable to open the specified log file.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="b5802-131"><dt>**\_ \_ no \_ se encontró el archivo PDH**</dt></span><span class="sxs-lookup"><span data-stu-id="b5802-131"><dt>**PDH\_FILE\_NOT\_FOUND**</dt></span></span> </dl>       | <span data-ttu-id="b5802-132">No se puede encontrar el archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="b5802-132">Unable to find the specified file.</span></span><br/>                                                          |



 

## <a name="requirements"></a><span data-ttu-id="b5802-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5802-133">Requirements</span></span>



| <span data-ttu-id="b5802-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5802-134">Requirement</span></span> | <span data-ttu-id="b5802-135">Value</span><span class="sxs-lookup"><span data-stu-id="b5802-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b5802-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5802-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b5802-137">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="b5802-137">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b5802-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5802-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b5802-139">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b5802-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b5802-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b5802-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="b5802-141"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5802-141"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="b5802-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b5802-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5802-143"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5802-143"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5802-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="b5802-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5802-145">**PdhGetLogFileSize**</span><span class="sxs-lookup"><span data-stu-id="b5802-145">**PdhGetLogFileSize**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize)
</dt> <dt>

[<span data-ttu-id="b5802-146">**PdhVbOpenLog**</span><span class="sxs-lookup"><span data-stu-id="b5802-146">**PdhVbOpenLog**</span></span>](pdhvbopenlog.md)
</dt> <dt>

[<span data-ttu-id="b5802-147">**PdhVbUpdateLog**</span><span class="sxs-lookup"><span data-stu-id="b5802-147">**PdhVbUpdateLog**</span></span>](pdhvbupdatelog.md)
</dt> </dl>

 

