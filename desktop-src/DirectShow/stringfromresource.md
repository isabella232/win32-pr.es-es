---
description: La función StringFromResource carga una cadena desde un archivo de recursos con el identificador de recursos especificado.
ms.assetid: 26b40905-db16-46d1-8621-9aa8cb8e7232
title: Función StringFromResource (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StringFromResource
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a9bb13944f281d528ff95a7856ebc8a0a2374c6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680944"
---
# <a name="stringfromresource-function"></a><span data-ttu-id="bbae9-103">StringFromResource función)</span><span class="sxs-lookup"><span data-stu-id="bbae9-103">StringFromResource function</span></span>

<span data-ttu-id="bbae9-104">La `StringFromResource` función carga una cadena de un archivo de recursos con el identificador de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="bbae9-104">The `StringFromResource` function loads a string from a resource file with the given resource identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbae9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bbae9-105">Syntax</span></span>


```C++
TCHAR* WINAPI StringFromResource(
   TCHAR *pBuffer,
   int   iResourceID
);
```



## <a name="parameters"></a><span data-ttu-id="bbae9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bbae9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbae9-107">*pBuffer*</span><span class="sxs-lookup"><span data-stu-id="bbae9-107">*pBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="bbae9-108">Puntero a la cadena que corresponde a *iResourceID*.</span><span class="sxs-lookup"><span data-stu-id="bbae9-108">Pointer to the string corresponding to *iResourceID*.</span></span>

</dd> <dt>

<span data-ttu-id="bbae9-109">*iResourceID*</span><span class="sxs-lookup"><span data-stu-id="bbae9-109">*iResourceID*</span></span> 
</dt> <dd>

<span data-ttu-id="bbae9-110">Identificador de recurso de la cadena que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="bbae9-110">Resource identifier of the string to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbae9-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bbae9-111">Return value</span></span>

<span data-ttu-id="bbae9-112">Devuelve la misma cadena que *pBuffer*.</span><span class="sxs-lookup"><span data-stu-id="bbae9-112">Returns the same string as *pBuffer*.</span></span> <span data-ttu-id="bbae9-113">Si la función no es correcta, devuelve una cadena nula.</span><span class="sxs-lookup"><span data-stu-id="bbae9-113">If the function is not successful, returns a null string.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbae9-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bbae9-114">Remarks</span></span>

<span data-ttu-id="bbae9-115">El búfer *pBuffer* debe ser al menos de \_ bytes de longitud máxima de Str \_ .</span><span class="sxs-lookup"><span data-stu-id="bbae9-115">The *pBuffer* buffer must be at least STR\_MAX\_LENGTH bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbae9-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bbae9-116">Requirements</span></span>



| <span data-ttu-id="bbae9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbae9-117">Requirement</span></span> | <span data-ttu-id="bbae9-118">Value</span><span class="sxs-lookup"><span data-stu-id="bbae9-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbae9-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bbae9-119">Header</span></span><br/>  | <dl> <span data-ttu-id="bbae9-120"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bbae9-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="bbae9-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bbae9-121">Library</span></span><br/> | <dl> <span data-ttu-id="bbae9-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="bbae9-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbae9-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="bbae9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbae9-124">Funciones auxiliares de páginas de propiedades</span><span class="sxs-lookup"><span data-stu-id="bbae9-124">Property Page Helper Functions</span></span>](property-page-helper-functions.md)
</dt> </dl>

 

 




