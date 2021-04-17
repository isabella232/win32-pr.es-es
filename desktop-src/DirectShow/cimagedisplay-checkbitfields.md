---
description: El método CheckBitFields valida las máscaras de color en una estructura de videoinfo.
ms.assetid: b03455aa-8d90-4fab-999d-7408d8417021
title: Método CImageDisplay. CheckBitFields (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckBitFields
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ade581dad5e53c2454df52e387653e44d6d4ad2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660226"
---
# <a name="cimagedisplaycheckbitfields-method"></a><span data-ttu-id="cbc23-103">CImageDisplay. CheckBitFields, método</span><span class="sxs-lookup"><span data-stu-id="cbc23-103">CImageDisplay.CheckBitFields method</span></span>

<span data-ttu-id="cbc23-104">El `CheckBitFields` método valida las máscaras de color en una estructura de [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="cbc23-104">The `CheckBitFields` method validates the color masks in a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbc23-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cbc23-105">Syntax</span></span>


```C++
BOOL CheckBitFields(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a><span data-ttu-id="cbc23-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cbc23-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbc23-107">*pInput*</span><span class="sxs-lookup"><span data-stu-id="cbc23-107">*pInput*</span></span> 
</dt> <dd>

<span data-ttu-id="cbc23-108">Puntero a una estructura de **videoinfo** .</span><span class="sxs-lookup"><span data-stu-id="cbc23-108">Pointer to a **VIDEOINFO** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbc23-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cbc23-109">Return value</span></span>

<span data-ttu-id="cbc23-110">Devuelve **true** si las máscaras de color son válidas o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="cbc23-110">Returns **TRUE** if the color masks are valid, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbc23-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cbc23-111">Remarks</span></span>

<span data-ttu-id="cbc23-112">Este método comprueba que la máscara de color para cada componente de color está comprendida entre uno y ocho bits de longitud y que cada máscara de color es una secuencia contigua de bits.</span><span class="sxs-lookup"><span data-stu-id="cbc23-112">This method verifies that the color mask for each color component is between one and eight bits long, and that each color mask is a contiguous sequence of bits.</span></span> <span data-ttu-id="cbc23-113">Llame a este método solo cuando el miembro **bicompression** esté establecido en \_ campos de campos de BI.</span><span class="sxs-lookup"><span data-stu-id="cbc23-113">Call this method only when the **biCompression** member is set to BI\_BITFIELDS.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbc23-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cbc23-114">Requirements</span></span>



| <span data-ttu-id="cbc23-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbc23-115">Requirement</span></span> | <span data-ttu-id="cbc23-116">Value</span><span class="sxs-lookup"><span data-stu-id="cbc23-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbc23-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cbc23-117">Header</span></span><br/>  | <dl> <span data-ttu-id="cbc23-118"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cbc23-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cbc23-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cbc23-119">Library</span></span><br/> | <dl> <span data-ttu-id="cbc23-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="cbc23-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbc23-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="cbc23-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbc23-122">**Clase CImageDisplay**</span><span class="sxs-lookup"><span data-stu-id="cbc23-122">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




