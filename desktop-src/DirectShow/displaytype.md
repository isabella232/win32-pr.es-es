---
description: La función DisplayType envía información sobre un tipo de medio a la ubicación de salida de depuración. Se omite en las compilaciones comerciales.
ms.assetid: 63a88508-dff8-4869-97e5-0f75f4a9dca0
title: Función DisplayType (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DisplayType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f3d83bbe7a24463fc4cfaed4ace3adec9d6fcf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680270"
---
# <a name="displaytype-function"></a><span data-ttu-id="55207-104">Función DisplayType</span><span class="sxs-lookup"><span data-stu-id="55207-104">DisplayType function</span></span>

<span data-ttu-id="55207-105">La `DisplayType` función envía información sobre un tipo de medio a la ubicación de salida de depuración.</span><span class="sxs-lookup"><span data-stu-id="55207-105">The `DisplayType` function sends information about a media type to the debug output location.</span></span> <span data-ttu-id="55207-106">Se omite en las compilaciones comerciales.</span><span class="sxs-lookup"><span data-stu-id="55207-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="55207-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="55207-107">Syntax</span></span>


```C++
void DisplayType(
         LPTSTR        label,
   const AM_MEDIA_TYPE *pmtIn
);
```



## <a name="parameters"></a><span data-ttu-id="55207-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="55207-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55207-109">*label*</span><span class="sxs-lookup"><span data-stu-id="55207-109">*label*</span></span> 
</dt> <dd>

<span data-ttu-id="55207-110">Cadena que contiene un mensaje que se va a mostrar con la información del tipo de archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="55207-110">String that contains a message to display with the media type information.</span></span>

</dd> <dt>

<span data-ttu-id="55207-111">*pmtIn*</span><span class="sxs-lookup"><span data-stu-id="55207-111">*pmtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="55207-112">ointer a la estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) que contiene el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="55207-112">ointer to the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that contains the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55207-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="55207-113">Return value</span></span>

<span data-ttu-id="55207-114">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="55207-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="55207-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="55207-115">Remarks</span></span>

<span data-ttu-id="55207-116">Esta función genera varios mensajes de seguimiento de registro \_ .</span><span class="sxs-lookup"><span data-stu-id="55207-116">This function generates several LOG\_TRACE messages.</span></span> <span data-ttu-id="55207-117">En el nivel de registro 2 o superior, la función muestra el tipo principal, el subtipo y el tipo de formato, y los datos del bloque de formato.</span><span class="sxs-lookup"><span data-stu-id="55207-117">At logging level 2 or higher, the function displays the major type, subtype, and format type, and data from the format block.</span></span> <span data-ttu-id="55207-118">En el nivel de registro 5 o superior, la función muestra información adicional, como los rectángulos de origen y de destino para los tipos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="55207-118">At logging level 5 or higher, the function displays additional information, such as the source and target rectangles for video types.</span></span>

## <a name="requirements"></a><span data-ttu-id="55207-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55207-119">Requirements</span></span>



| <span data-ttu-id="55207-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="55207-120">Requirement</span></span> | <span data-ttu-id="55207-121">Value</span><span class="sxs-lookup"><span data-stu-id="55207-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55207-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="55207-122">Header</span></span><br/>  | <dl> <span data-ttu-id="55207-123"><dt>Wxdebug. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="55207-123"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="55207-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="55207-124">Library</span></span><br/> | <dl> <span data-ttu-id="55207-125"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="55207-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55207-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="55207-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55207-127">Funciones de salida de depuración</span><span class="sxs-lookup"><span data-stu-id="55207-127">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




