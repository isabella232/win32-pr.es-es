---
description: El método GetBitMasks recupera las máscaras de color para un formato de videoinfo especificado.
ms.assetid: 72a9ba44-96de-4fff-a3fb-675d3dd080d8
title: Método CImageDisplay. GetBitMasks (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.GetBitMasks
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a2defe5e80a0d7311adcd19dca67119019623993
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661280"
---
# <a name="cimagedisplaygetbitmasks-method"></a><span data-ttu-id="77148-103">CImageDisplay. GetBitMasks, método</span><span class="sxs-lookup"><span data-stu-id="77148-103">CImageDisplay.GetBitMasks method</span></span>

<span data-ttu-id="77148-104">El `GetBitMasks` método recupera las máscaras de color para un formato de [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) especificado.</span><span class="sxs-lookup"><span data-stu-id="77148-104">The `GetBitMasks` method retrieves the color masks for a specified [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) format.</span></span>

## <a name="syntax"></a><span data-ttu-id="77148-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="77148-105">Syntax</span></span>


```C++
const DWORD* GetBitMasks(
   const VIDEOINFO *pVideoInfo
);
```



## <a name="parameters"></a><span data-ttu-id="77148-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="77148-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77148-107">*pVideoInfo*</span><span class="sxs-lookup"><span data-stu-id="77148-107">*pVideoInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="77148-108">Puntero a la estructura de **videoinfo** .</span><span class="sxs-lookup"><span data-stu-id="77148-108">Pointer to the **VIDEOINFO** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77148-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="77148-109">Return value</span></span>

<span data-ttu-id="77148-110">Devuelve una matriz de tres valores **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="77148-110">Returns an array of three **DWORD** values.</span></span>

## <a name="remarks"></a><span data-ttu-id="77148-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="77148-111">Remarks</span></span>

<span data-ttu-id="77148-112">Si el miembro de **bicompresión** son \_ campos de campos de BI, el método devuelve un puntero a las máscaras de color que se proporcionan en el miembro **dwBitMasks** .</span><span class="sxs-lookup"><span data-stu-id="77148-112">If the **biCompression** member is BI\_BITFIELDS, the method returns a pointer to the color masks that are supplied in the **dwBitMasks** member.</span></span> <span data-ttu-id="77148-113">Si el miembro de **bicompresión** es bi \_ RGB, el método devuelve las máscaras de color que corresponden a la profundidad de bits.</span><span class="sxs-lookup"><span data-stu-id="77148-113">If the **biCompression** member is BI\_RGB, the method returns the color masks that correspond to the bit depth.</span></span> <span data-ttu-id="77148-114">Si se produce un error en el método (por ejemplo, la profundidad de bits es menor que 16), el método devuelve la matriz {0,0,0} .</span><span class="sxs-lookup"><span data-stu-id="77148-114">If the method fails (for example, the bit depth is less than 16), the method returns the array {0,0,0}.</span></span>

## <a name="requirements"></a><span data-ttu-id="77148-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77148-115">Requirements</span></span>



| <span data-ttu-id="77148-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="77148-116">Requirement</span></span> | <span data-ttu-id="77148-117">Value</span><span class="sxs-lookup"><span data-stu-id="77148-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77148-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="77148-118">Header</span></span><br/>  | <dl> <span data-ttu-id="77148-119"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="77148-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="77148-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="77148-120">Library</span></span><br/> | <dl> <span data-ttu-id="77148-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="77148-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77148-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="77148-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77148-123">**Clase CImageDisplay**</span><span class="sxs-lookup"><span data-stu-id="77148-123">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




