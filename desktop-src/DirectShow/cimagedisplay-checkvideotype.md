---
description: El método CheckVideoType comprueba si un formato de videoinfo especificado es compatible con el formato de presentación.
ms.assetid: a8593c7d-bde0-4c44-b450-10c129dd0007
title: Método CImageDisplay. CheckVideoType (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckVideoType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7db198270804053993352c4969b924fa7edc891f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661095"
---
# <a name="cimagedisplaycheckvideotype-method"></a><span data-ttu-id="efb81-103">CImageDisplay. CheckVideoType, método</span><span class="sxs-lookup"><span data-stu-id="efb81-103">CImageDisplay.CheckVideoType method</span></span>

<span data-ttu-id="efb81-104">El `CheckVideoType` método comprueba si un formato de [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) especificado es compatible con el formato de presentación.</span><span class="sxs-lookup"><span data-stu-id="efb81-104">The `CheckVideoType` method checks whether a specified [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) format is compatible with the display format.</span></span>

## <a name="syntax"></a><span data-ttu-id="efb81-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="efb81-105">Syntax</span></span>


```C++
HRESULT CheckVideoType(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a><span data-ttu-id="efb81-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="efb81-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efb81-107">*pInput*</span><span class="sxs-lookup"><span data-stu-id="efb81-107">*pInput*</span></span> 
</dt> <dd>

<span data-ttu-id="efb81-108">Puntero a una estructura de **videoinfo** .</span><span class="sxs-lookup"><span data-stu-id="efb81-108">Pointer to a **VIDEOINFO** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efb81-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="efb81-109">Return value</span></span>

<span data-ttu-id="efb81-110">Devuelve S \_ OK si el formato es compatible o E \_ INVALIDARG en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="efb81-110">Returns S\_OK if the format is compatible, or E\_INVALIDARG otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="efb81-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="efb81-111">Remarks</span></span>

<span data-ttu-id="efb81-112">Este método devuelve S \_ OK si el tipo propuesto se puede mostrar fácilmente bajo la configuración de pantalla actual.</span><span class="sxs-lookup"><span data-stu-id="efb81-112">This method returns S\_OK if the proposed type can be displayed easily under the current display settings.</span></span>

## <a name="requirements"></a><span data-ttu-id="efb81-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="efb81-113">Requirements</span></span>



| <span data-ttu-id="efb81-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="efb81-114">Requirement</span></span> | <span data-ttu-id="efb81-115">Value</span><span class="sxs-lookup"><span data-stu-id="efb81-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efb81-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="efb81-116">Header</span></span><br/>  | <dl> <span data-ttu-id="efb81-117"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="efb81-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="efb81-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="efb81-118">Library</span></span><br/> | <dl> <span data-ttu-id="efb81-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="efb81-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efb81-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="efb81-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efb81-121">**Clase CImageDisplay**</span><span class="sxs-lookup"><span data-stu-id="efb81-121">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




