---
description: GuidNames es una matriz global de la biblioteca de clases base de DirectShow que contiene cadenas que representan los GUID definidos en UUID. h. Esta matriz es útil para generar la salida de depuración.
ms.assetid: 6d72ad1e-588a-4a82-a1c1-e1e7b49df572
title: GuidNames (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GuidNames
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 359294d0cf3ab4e2074db5935cbbd604dcc1b250
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680200"
---
# <a name="guidnames"></a><span data-ttu-id="8617c-104">GuidNames</span><span class="sxs-lookup"><span data-stu-id="8617c-104">GuidNames</span></span>

<span data-ttu-id="8617c-105">`GuidNames` es una matriz global de la biblioteca de clases base de DirectShow que contiene cadenas que representan los GUID definidos en UUID. h.</span><span class="sxs-lookup"><span data-stu-id="8617c-105">`GuidNames` is a global array in the DirectShow base class library that contains strings representing the GUIDs defined in Uuids.h.</span></span> <span data-ttu-id="8617c-106">Esta matriz es útil para generar la salida de depuración.</span><span class="sxs-lookup"><span data-stu-id="8617c-106">This array is useful for generating debug output.</span></span>

``` syntax
char* GuidNames[guid]
```

## <a name="parameters"></a><span data-ttu-id="8617c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8617c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8617c-108"><span id="guid"></span><span id="GUID"></span>*volumen*</span><span class="sxs-lookup"><span data-stu-id="8617c-108"><span id="guid"></span><span id="GUID"></span>*guid*</span></span>
</dt> <dd>

<span data-ttu-id="8617c-109">Especifica cualquier valor GUID definido en el archivo de encabezado UUID. h.</span><span class="sxs-lookup"><span data-stu-id="8617c-109">Specifies any GUID value defined in the header file Uuids.h.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8617c-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8617c-110">Remarks</span></span>

<span data-ttu-id="8617c-111">Use esta matriz global para generar constantes GUID como cadenas.</span><span class="sxs-lookup"><span data-stu-id="8617c-111">Use this global array to output GUID constants as strings.</span></span> <span data-ttu-id="8617c-112">Por ejemplo, el código siguiente imprime la cadena "MEDIATYPE \_ video" en la consola:</span><span class="sxs-lookup"><span data-stu-id="8617c-112">For example, the following code prints the string "MEDIATYPE\_Video" to the console:</span></span>


```C++
puts(GuidNames[MEDIATYPE_Video]);
```



<span data-ttu-id="8617c-113">Si no se encuentra ninguna coincidencia con el GUID, se devuelve la cadena "nombre del GUID desconocido".</span><span class="sxs-lookup"><span data-stu-id="8617c-113">If the GUID is not matched, the string "Unknown GUID Name" is returned.</span></span> <span data-ttu-id="8617c-114">No todos los GUID de DirectShow se definen en UUID. h.</span><span class="sxs-lookup"><span data-stu-id="8617c-114">Not all DirectShow GUIDs are defined in uuids.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="8617c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8617c-115">Requirements</span></span>



| <span data-ttu-id="8617c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8617c-116">Requirement</span></span> | <span data-ttu-id="8617c-117">Value</span><span class="sxs-lookup"><span data-stu-id="8617c-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8617c-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8617c-118">Header</span></span><br/>  | <dl> <span data-ttu-id="8617c-119"><dt>Wxdebug. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8617c-119"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8617c-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8617c-120">Library</span></span><br/> | <dl> <span data-ttu-id="8617c-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="8617c-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8617c-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="8617c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8617c-123">Funciones de salida de depuración</span><span class="sxs-lookup"><span data-stu-id="8617c-123">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




