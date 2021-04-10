---
description: La función PdhVbOpenQuery crea e inicializa una estructura de consulta única que se utiliza para administrar la colección de datos de rendimiento.
ms.assetid: 9cf535ef-76ad-4773-8414-8e289f3c52f6
title: PdhVbOpenQuery función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbOpenQuery
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: c657f033e2e972473218f2b283e03b11659d9f2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156524"
---
# <a name="pdhvbopenquery-function"></a><span data-ttu-id="37cca-103">PdhVbOpenQuery función)</span><span class="sxs-lookup"><span data-stu-id="37cca-103">PdhVbOpenQuery function</span></span>

<span data-ttu-id="37cca-104">La función **PdhVbOpenQuery** crea e inicializa una estructura de consulta única que se utiliza para administrar la colección de datos de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="37cca-104">The **PdhVbOpenQuery** function creates and initializes a unique query structure that is used to manage the collection of performance data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="37cca-105">La función que se describe en este tema puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="37cca-105">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="37cca-106">En su lugar, Microsoft recomienda que use las funciones descritas en [funciones de contadores de rendimiento](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="37cca-106">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="37cca-107">Función PdhVbOpenQuery ( \_ ByVal QueryHandle as Long \_ ) as Long</span><span class="sxs-lookup"><span data-stu-id="37cca-107">Function PdhVbOpenQuery( \_ ByVal QueryHandle As Long \_ ) As Long</span></span>

## <a name="parameters"></a><span data-ttu-id="37cca-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="37cca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37cca-109">*QueryHandle*</span><span class="sxs-lookup"><span data-stu-id="37cca-109">*QueryHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="37cca-110">Variable que está desactivada (es igual a 0) antes de que se llame a la función y, si la función es correcta, contiene el identificador único de la consulta que se crea y se abre.</span><span class="sxs-lookup"><span data-stu-id="37cca-110">Variable that is cleared (equals 0) before the function is called and, if the function is successful, contains the unique ID of the query that is created and opened.</span></span> <span data-ttu-id="37cca-111">Este identificador se utiliza en las llamadas subsiguientes a otras funciones de PDH para identificar la consulta.</span><span class="sxs-lookup"><span data-stu-id="37cca-111">This handle is used in the subsequent calls to other PDH functions to identify the query.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37cca-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="37cca-112">Return value</span></span>

<span data-ttu-id="37cca-113">Si la función se ejecuta correctamente, devuelve un entero **largo** igual a error \_ correcto y un nuevo identificador en la variable *QueryHandle* .</span><span class="sxs-lookup"><span data-stu-id="37cca-113">If the function succeeds, it returns a **Long** integer equal to ERROR\_SUCCESS and a new handle in the *QueryHandle* variable.</span></span>

<span data-ttu-id="37cca-114">Si se produce un error en la función, el valor devuelto es un [código de error del sistema](/windows/desktop/Debug/system-error-codes) o un [código de error de PDH](pdh-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="37cca-114">If the function fails, the return value is a [system error code](/windows/desktop/Debug/system-error-codes) or a [PDH error code](pdh-error-codes.md).</span></span> <span data-ttu-id="37cca-115">Los valores posibles son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="37cca-115">The following are possible values.</span></span>



| <span data-ttu-id="37cca-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="37cca-116">Return code</span></span>                                                                                                     | <span data-ttu-id="37cca-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="37cca-117">Description</span></span>                                                  |
|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <span data-ttu-id="37cca-118"><dt>**PDH \_ argumento no válido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="37cca-118"><dt>**PDH\_INVALID\_ARGUMENT**</dt></span></span> </dl>           | <span data-ttu-id="37cca-119">El argumento no es válido o es incorrecto.</span><span class="sxs-lookup"><span data-stu-id="37cca-119">The argument is invalid or incorrect.</span></span><br/>             |
| <dl> <span data-ttu-id="37cca-120"><dt>**\_error de \_ asignación de memoria de PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="37cca-120"><dt>**PDH\_MEMORY\_ALLOCATION\_FAILURE**</dt></span></span> </dl> | <span data-ttu-id="37cca-121">No se pudo asignar un búfer de memoria temporal.</span><span class="sxs-lookup"><span data-stu-id="37cca-121">A temporary memory buffer could not be allocated.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="37cca-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37cca-122">Requirements</span></span>



| <span data-ttu-id="37cca-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="37cca-123">Requirement</span></span> | <span data-ttu-id="37cca-124">Value</span><span class="sxs-lookup"><span data-stu-id="37cca-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="37cca-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37cca-125">Minimum supported client</span></span><br/> | <span data-ttu-id="37cca-126">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="37cca-126">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="37cca-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37cca-127">Minimum supported server</span></span><br/> | <span data-ttu-id="37cca-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="37cca-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="37cca-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="37cca-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="37cca-130"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="37cca-130"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="37cca-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="37cca-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37cca-132"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37cca-132"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37cca-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="37cca-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37cca-134">**PdhCloseQuery**</span><span class="sxs-lookup"><span data-stu-id="37cca-134">**PdhCloseQuery**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery)
</dt> </dl>

 

