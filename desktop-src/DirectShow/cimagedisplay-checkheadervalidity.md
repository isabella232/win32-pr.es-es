---
description: El método CheckHeaderValidity valida una estructura BITMAPINFOHEADER. Este método solo es útil para los tipos RGB sin comprimir, no para los tipos comprimidos ni los tipos YUV.
ms.assetid: 24b547b6-b730-48b2-9a1b-6e77f9cb1ce1
title: Método CImageDisplay. CheckHeaderValidity (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckHeaderValidity
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 803e8cd1a70c68f3e20c320978e9a350bdf23bdb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679086"
---
# <a name="cimagedisplaycheckheadervalidity-method"></a><span data-ttu-id="85077-104">CImageDisplay. CheckHeaderValidity, método</span><span class="sxs-lookup"><span data-stu-id="85077-104">CImageDisplay.CheckHeaderValidity method</span></span>

<span data-ttu-id="85077-105">El `CheckHeaderValidity` método valida una estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="85077-105">The `CheckHeaderValidity` method validates a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span> <span data-ttu-id="85077-106">Este método solo es útil para los tipos RGB sin comprimir, no para los tipos comprimidos ni los tipos YUV.</span><span class="sxs-lookup"><span data-stu-id="85077-106">This method is useful only for uncompressed RGB types, not for compressed types or YUV types.</span></span>

## <a name="syntax"></a><span data-ttu-id="85077-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="85077-107">Syntax</span></span>


```C++
BOOL CheckHeaderValidity(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a><span data-ttu-id="85077-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="85077-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85077-109">*pInput*</span><span class="sxs-lookup"><span data-stu-id="85077-109">*pInput*</span></span> 
</dt> <dd>

<span data-ttu-id="85077-110">Puntero a una estructura de [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) que contiene la estructura **BITMAPINFOHEADER** .</span><span class="sxs-lookup"><span data-stu-id="85077-110">Pointer to a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure containing the **BITMAPINFOHEADER** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85077-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="85077-111">Return value</span></span>

<span data-ttu-id="85077-112">Devuelve **true** si **BITMAPINFOHEADER** es válido o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="85077-112">Returns **TRUE** if the **BITMAPINFOHEADER** is valid, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="85077-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="85077-113">Remarks</span></span>

<span data-ttu-id="85077-114">Este método comprueba que las dimensiones de la imagen no son negativas; el tipo de compresión es de BI RGB o de campos de tipos de \_ BI \_ ; la profundidad de color y las máscaras de color son válidas, el miembro **biplaners** es igual a uno; y los miembros **bisize** y **biSizeImage** son correctos.</span><span class="sxs-lookup"><span data-stu-id="85077-114">This method checks that the image dimensions are non-negative; the compression type is BI\_RGB or BI\_BITFIELDS; the color depth and color masks are valid; the **biPlanes** member equals one; and the **biSize** and **biSizeImage** members are correct.</span></span> <span data-ttu-id="85077-115">También comprueba si hay errores comunes en las entradas de la paleta, si existen.</span><span class="sxs-lookup"><span data-stu-id="85077-115">It also checks for common errors in the palette entries, if any.</span></span>

## <a name="requirements"></a><span data-ttu-id="85077-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85077-116">Requirements</span></span>



| <span data-ttu-id="85077-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="85077-117">Requirement</span></span> | <span data-ttu-id="85077-118">Value</span><span class="sxs-lookup"><span data-stu-id="85077-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85077-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="85077-119">Header</span></span><br/>  | <dl> <span data-ttu-id="85077-120"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="85077-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="85077-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="85077-121">Library</span></span><br/> | <dl> <span data-ttu-id="85077-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="85077-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85077-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="85077-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85077-124">**Clase CImageDisplay**</span><span class="sxs-lookup"><span data-stu-id="85077-124">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




