---
description: La función PdhVbGetCounterPathFromList copia la ruta de acceso del contador a la que hace referencia el parámetro de índice de una lista de rutas de acceso de contador creada por el usuario a partir de la llamada más reciente a la función PdhVbCreateCounterPathList.
ms.assetid: e77a022d-42f2-4c48-acb7-36cb013730dd
title: PdhVbGetCounterPathFromList función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetCounterPathFromList
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 4c5ae4632ede898b7cd323723037ea68d53455b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667311"
---
# <a name="pdhvbgetcounterpathfromlist-function"></a><span data-ttu-id="95bf4-103">PdhVbGetCounterPathFromList función)</span><span class="sxs-lookup"><span data-stu-id="95bf4-103">PdhVbGetCounterPathFromList function</span></span>

<span data-ttu-id="95bf4-104">La función **PdhVbGetCounterPathFromList** copia la ruta de acceso del contador a la que hace referencia el parámetro de *Índice* de una lista de rutas de acceso de contador creada por el usuario a partir de la llamada más reciente a la función [**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md) .</span><span class="sxs-lookup"><span data-stu-id="95bf4-104">The **PdhVbGetCounterPathFromList** function copies the counter path referenced by the *Index* parameter from a counter path list created by the user from the most recent call to the [**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md) function.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="95bf4-105">La función que se describe en este tema puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="95bf4-105">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="95bf4-106">En su lugar, Microsoft recomienda que use las funciones descritas en [funciones de contadores de rendimiento](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="95bf4-106">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="95bf4-107">Función PdhVbGetCounterPathFromList ( \_ ByVal index as Long, \_ ByVal buffer As String, \_ ByVal BufferLength as Long \_ ) as Long</span><span class="sxs-lookup"><span data-stu-id="95bf4-107">Function PdhVbGetCounterPathFromList( \_ ByVal Index As Long, \_ ByVal Buffer As String, \_ ByVal BufferLength As Long \_ ) As Long</span></span>

## <a name="parameters"></a><span data-ttu-id="95bf4-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="95bf4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95bf4-109">*Index*</span><span class="sxs-lookup"><span data-stu-id="95bf4-109">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="95bf4-110">Índice de la ruta de acceso del contador que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="95bf4-110">Index of the counter path to retrieve.</span></span> <span data-ttu-id="95bf4-111">Debe ser un valor mayor o igual que 1 y menor o igual que el valor devuelto por la función [**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md) .</span><span class="sxs-lookup"><span data-stu-id="95bf4-111">This must be a value that is greater than or equal to 1, and less than or equal to the value returned by the [**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="95bf4-112">*Buffer*</span><span class="sxs-lookup"><span data-stu-id="95bf4-112">*Buffer*</span></span> 
</dt> <dd>

<span data-ttu-id="95bf4-113">Cadena dimensionada e inicializada que recibirá la ruta de acceso del contador que corresponde al valor del parámetro de índice.</span><span class="sxs-lookup"><span data-stu-id="95bf4-113">Dimensioned and initialized string that will receive the counter path that corresponds to the value of the Index parameter.</span></span>

</dd> <dt>

<span data-ttu-id="95bf4-114">*BufferLength*</span><span class="sxs-lookup"><span data-stu-id="95bf4-114">*BufferLength*</span></span> 
</dt> <dd>

<span data-ttu-id="95bf4-115">Número máximo de caracteres que caben en la cadena a la que hace referencia el búfer.</span><span class="sxs-lookup"><span data-stu-id="95bf4-115">Maximum number of characters that will fit in the string referenced by Buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95bf4-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="95bf4-116">Return value</span></span>

<span data-ttu-id="95bf4-117">La función devuelve el número de caracteres copiados en el búfer.</span><span class="sxs-lookup"><span data-stu-id="95bf4-117">The function returns the number of characters copied to Buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="95bf4-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95bf4-118">Requirements</span></span>



| <span data-ttu-id="95bf4-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="95bf4-119">Requirement</span></span> | <span data-ttu-id="95bf4-120">Value</span><span class="sxs-lookup"><span data-stu-id="95bf4-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="95bf4-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="95bf4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="95bf4-122">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="95bf4-122">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="95bf4-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="95bf4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="95bf4-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="95bf4-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="95bf4-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="95bf4-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="95bf4-126"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="95bf4-126"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="95bf4-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="95bf4-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95bf4-128"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95bf4-128"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95bf4-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="95bf4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95bf4-130">**PdhVbCreateCounterPathList**</span><span class="sxs-lookup"><span data-stu-id="95bf4-130">**PdhVbCreateCounterPathList**</span></span>](pdhvbcreatecounterpathlist.md)
</dt> <dt>

[<span data-ttu-id="95bf4-131">**PdhVbGetCounterPathElements**</span><span class="sxs-lookup"><span data-stu-id="95bf4-131">**PdhVbGetCounterPathElements**</span></span>](pdhvbgetcounterpathelements.md)
</dt> <dt>

[<span data-ttu-id="95bf4-132">**PdhVbGetOneCounterPath**</span><span class="sxs-lookup"><span data-stu-id="95bf4-132">**PdhVbGetOneCounterPath**</span></span>](pdhvbgetonecounterpath.md)
</dt> </dl>

 

 




