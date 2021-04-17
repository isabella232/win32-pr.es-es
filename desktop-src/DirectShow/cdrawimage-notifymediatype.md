---
description: El método NotifyMediaType notifica al objeto CDrawImage del tipo de medio actual.
ms.assetid: 419d516f-4b96-47aa-80cc-ac785e65af8b
title: Método CDrawImage. NotifyMediaType (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.NotifyMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e3af4d926bd0ca8db5ef11839dd0ca84523c374
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680946"
---
# <a name="cdrawimagenotifymediatype-method"></a><span data-ttu-id="59eaa-103">CDrawImage. NotifyMediaType, método</span><span class="sxs-lookup"><span data-stu-id="59eaa-103">CDrawImage.NotifyMediaType method</span></span>

<span data-ttu-id="59eaa-104">El `NotifyMediaType` método notifica al objeto **CDrawImage** del tipo de medio actual.</span><span class="sxs-lookup"><span data-stu-id="59eaa-104">The `NotifyMediaType` method notifies the **CDrawImage** object of the current media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="59eaa-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="59eaa-105">Syntax</span></span>


```C++
void NotifyMediaType(
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="59eaa-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="59eaa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59eaa-107">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="59eaa-107">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="59eaa-108">Puntero a un objeto [**CMediaType**](cmediatype.md) o **null** para borrar el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="59eaa-108">Pointer to a [**CMediaType**](cmediatype.md) object, or **NULL** to clear the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59eaa-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="59eaa-109">Return value</span></span>

<span data-ttu-id="59eaa-110">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="59eaa-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="59eaa-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="59eaa-111">Remarks</span></span>

<span data-ttu-id="59eaa-112">El filtro propietario debe llamar a este método cada vez que cambie el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="59eaa-112">The owning filter should call this method whenever the media type changes.</span></span> <span data-ttu-id="59eaa-113">Normalmente esto se produce cuando el PIN se conecta por primera vez y después de un cambio de formato dinámico.</span><span class="sxs-lookup"><span data-stu-id="59eaa-113">Typically this occurs when the pin first connects, and after a dynamic format change.</span></span>

<span data-ttu-id="59eaa-114">El objeto **CDrawImage** almacena el puntero *pMediaType* en la variable miembro **m \_ pMediaType** .</span><span class="sxs-lookup"><span data-stu-id="59eaa-114">The **CDrawImage** object stores the *pMediaType* pointer in the **m\_pMediaType** member variable.</span></span> <span data-ttu-id="59eaa-115">Por consiguiente, si el autor de la llamada necesita liberar el objeto **CMediaType** , debe actualizar el objeto **CDrawImage** llamando de nuevo a este método, ya sea con un puntero nuevo o con un valor **null** .</span><span class="sxs-lookup"><span data-stu-id="59eaa-115">Therefore, if the caller needs to release the **CMediaType** object, it should update the **CDrawImage** object by calling this method again, either with a new pointer or with a **NULL** value.</span></span> <span data-ttu-id="59eaa-116">De lo contrario, se puede producir un error cuando el objeto **CDrawImage** intenta hacer referencia al puntero anterior.</span><span class="sxs-lookup"><span data-stu-id="59eaa-116">Otherwise, an error can occur when the **CDrawImage** object attempts to reference the old pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="59eaa-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59eaa-117">Requirements</span></span>



| <span data-ttu-id="59eaa-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="59eaa-118">Requirement</span></span> | <span data-ttu-id="59eaa-119">Value</span><span class="sxs-lookup"><span data-stu-id="59eaa-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59eaa-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="59eaa-120">Header</span></span><br/>  | <dl> <span data-ttu-id="59eaa-121"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="59eaa-121"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="59eaa-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="59eaa-122">Library</span></span><br/> | <dl> <span data-ttu-id="59eaa-123"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="59eaa-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59eaa-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="59eaa-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59eaa-125">**Clase CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="59eaa-125">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




