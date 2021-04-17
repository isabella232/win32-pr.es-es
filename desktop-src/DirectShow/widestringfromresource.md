---
description: La función WideStringFromResource carga una cadena de caracteres anchos de un archivo de recursos con el identificador de recursos especificado.
ms.assetid: c5fac767-20c4-4342-9d4d-e1b916854b95
title: Función WideStringFromResource (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WideStringFromResource
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9c7cbdccc76fc57e660109851ae5b8f141704d04
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671066"
---
# <a name="widestringfromresource-function"></a><span data-ttu-id="534ba-103">WideStringFromResource función)</span><span class="sxs-lookup"><span data-stu-id="534ba-103">WideStringFromResource function</span></span>

<span data-ttu-id="534ba-104">La `WideStringFromResource` función carga una cadena de caracteres anchos de un archivo de recursos con el identificador de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="534ba-104">The `WideStringFromResource` function loads a wide-character string from a resource file with the given resource identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="534ba-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="534ba-105">Syntax</span></span>


```C++
WCHAR* WINAPI WideStringFromResource(
   pBuffer *pBuffer,
   int     iResourceID
);
```



## <a name="parameters"></a><span data-ttu-id="534ba-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="534ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="534ba-107">*pBuffer*</span><span class="sxs-lookup"><span data-stu-id="534ba-107">*pBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="534ba-108">Puntero a la cadena que corresponde a *iResourceID*.</span><span class="sxs-lookup"><span data-stu-id="534ba-108">Pointer to the string corresponding to *iResourceID*.</span></span>

</dd> <dt>

<span data-ttu-id="534ba-109">*iResourceID*</span><span class="sxs-lookup"><span data-stu-id="534ba-109">*iResourceID*</span></span> 
</dt> <dd>

<span data-ttu-id="534ba-110">Identificador de recurso de la cadena que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="534ba-110">Resource identifier of the string to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="534ba-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="534ba-111">Return value</span></span>

<span data-ttu-id="534ba-112">Devuelve la misma cadena que *pBuffer*.</span><span class="sxs-lookup"><span data-stu-id="534ba-112">Returns the same string as *pBuffer*.</span></span> <span data-ttu-id="534ba-113">Si la función no es correcta, devuelve una cadena nula.</span><span class="sxs-lookup"><span data-stu-id="534ba-113">If the function is not successful, returns a null string.</span></span>

## <a name="remarks"></a><span data-ttu-id="534ba-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="534ba-114">Remarks</span></span>

<span data-ttu-id="534ba-115">Normalmente, se llama a las páginas de propiedades a través de sus interfaces COM, que usan cadenas de caracteres anchos independientemente de cómo se compile el binario.</span><span class="sxs-lookup"><span data-stu-id="534ba-115">Property pages are typically called through their COM interfaces, which use wide-character strings regardless of how the binary is built.</span></span> <span data-ttu-id="534ba-116">Esta función permite convertir una cadena de recursos en una cadena de caracteres anchos.</span><span class="sxs-lookup"><span data-stu-id="534ba-116">This function allows you to convert a resource string to a wide-character string.</span></span> <span data-ttu-id="534ba-117">La función convierte el recurso en una cadena de caracteres anchos (si aún no es uno) después de cargarlo.</span><span class="sxs-lookup"><span data-stu-id="534ba-117">The function converts the resource to a wide-character string (if it is not already one) after loading it.</span></span>

## <a name="requirements"></a><span data-ttu-id="534ba-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="534ba-118">Requirements</span></span>



| <span data-ttu-id="534ba-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="534ba-119">Requirement</span></span> | <span data-ttu-id="534ba-120">Value</span><span class="sxs-lookup"><span data-stu-id="534ba-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="534ba-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="534ba-121">Header</span></span><br/>  | <dl> <span data-ttu-id="534ba-122"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="534ba-122"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="534ba-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="534ba-123">Library</span></span><br/> | <dl> <span data-ttu-id="534ba-124"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="534ba-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="534ba-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="534ba-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="534ba-126">Funciones auxiliares de páginas de propiedades</span><span class="sxs-lookup"><span data-stu-id="534ba-126">Property Page Helper Functions</span></span>](property-page-helper-functions.md)
</dt> </dl>

 

 




