---
description: El método CheckPaletteHeader valida las entradas de la paleta en una estructura de videoinfo.
ms.assetid: bc18cbe6-0446-43a6-a50c-e587815b789d
title: Método CImageDisplay. CheckPaletteHeader (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckPaletteHeader
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54c4f401d2e75aeb35ffc19d26690fa04a769c27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680925"
---
# <a name="cimagedisplaycheckpaletteheader-method"></a><span data-ttu-id="fcb30-103">CImageDisplay. CheckPaletteHeader, método</span><span class="sxs-lookup"><span data-stu-id="fcb30-103">CImageDisplay.CheckPaletteHeader method</span></span>

<span data-ttu-id="fcb30-104">El `CheckPaletteHeader` método valida las entradas de la paleta en una estructura de [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="fcb30-104">The `CheckPaletteHeader` method validates the palette entries in a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcb30-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fcb30-105">Syntax</span></span>


```C++
BOOL CheckPaletteHeader(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a><span data-ttu-id="fcb30-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fcb30-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcb30-107">*pInput*</span><span class="sxs-lookup"><span data-stu-id="fcb30-107">*pInput*</span></span> 
</dt> <dd>

<span data-ttu-id="fcb30-108">Puntero a una estructura de **videoinfo** .</span><span class="sxs-lookup"><span data-stu-id="fcb30-108">Pointer to a **VIDEOINFO** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcb30-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fcb30-109">Return value</span></span>

<span data-ttu-id="fcb30-110">Devuelve **true** si las entradas de la paleta son válidas o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="fcb30-110">Returns **TRUE** if the palette entries are valid, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcb30-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fcb30-111">Remarks</span></span>

<span data-ttu-id="fcb30-112">Si el formato de la imagen no es de paleta, el método comprueba que **biClrUsed** sea igual a cero.</span><span class="sxs-lookup"><span data-stu-id="fcb30-112">If the image format is not palettized, the method verifies that **biClrUsed** equals zero.</span></span> <span data-ttu-id="fcb30-113">De lo contrario, el método comprueba que el marcador de **bicompresión** es de BI \_ RGB; **biClrImportant** no es mayor que **biClrUsed**; y el número de entradas de la paleta no supera el máximo, dada la profundidad de color.</span><span class="sxs-lookup"><span data-stu-id="fcb30-113">Otherwise, the method verifies that the **biCompression** flag is BI\_RGB; **biClrImportant** is not greater than **biClrUsed**; and the number of palette entries does not exceed the maximum, given the color depth.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcb30-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fcb30-114">Requirements</span></span>



| <span data-ttu-id="fcb30-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fcb30-115">Requirement</span></span> | <span data-ttu-id="fcb30-116">Value</span><span class="sxs-lookup"><span data-stu-id="fcb30-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcb30-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fcb30-117">Header</span></span><br/>  | <dl> <span data-ttu-id="fcb30-118"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fcb30-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fcb30-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fcb30-119">Library</span></span><br/> | <dl> <span data-ttu-id="fcb30-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="fcb30-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fcb30-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="fcb30-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcb30-122">**Clase CImageDisplay**</span><span class="sxs-lookup"><span data-stu-id="fcb30-122">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




