---
description: El método GetColourMask recupera las máscaras de color para el formato de presentación actual.
ms.assetid: 386d0439-8502-411d-935c-3c2153a8b5b4
title: Método CImageDisplay. GetColourMask (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.GetColourMask
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 499b3677cd68444b58514d692d87cd4f631350b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681133"
---
# <a name="cimagedisplaygetcolourmask-method"></a><span data-ttu-id="71f1e-103">CImageDisplay. GetColourMask, método</span><span class="sxs-lookup"><span data-stu-id="71f1e-103">CImageDisplay.GetColourMask method</span></span>

<span data-ttu-id="71f1e-104">El `GetColourMask` método recupera las máscaras de color para el formato de presentación actual.</span><span class="sxs-lookup"><span data-stu-id="71f1e-104">The `GetColourMask` method retrieves the color masks for the current display format.</span></span>

## <a name="syntax"></a><span data-ttu-id="71f1e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="71f1e-105">Syntax</span></span>


```C++
BOOL GetColourMask(
   DWORD *pMaskRed,
   DWORD *pMaskGreen,
   DWORD *pMaskBlue
);
```



## <a name="parameters"></a><span data-ttu-id="71f1e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="71f1e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71f1e-107">*pMaskRed*</span><span class="sxs-lookup"><span data-stu-id="71f1e-107">*pMaskRed*</span></span> 
</dt> <dd>

<span data-ttu-id="71f1e-108">Puntero a una variable que recibe la máscara de componente rojo.</span><span class="sxs-lookup"><span data-stu-id="71f1e-108">Pointer to a variable that receives the red-component mask.</span></span>

</dd> <dt>

<span data-ttu-id="71f1e-109">*pMaskGreen*</span><span class="sxs-lookup"><span data-stu-id="71f1e-109">*pMaskGreen*</span></span> 
</dt> <dd>

<span data-ttu-id="71f1e-110">Puntero a una variable que recibe la máscara del componente verde.</span><span class="sxs-lookup"><span data-stu-id="71f1e-110">Pointer to a variable that receives the green-component mask.</span></span>

</dd> <dt>

<span data-ttu-id="71f1e-111">*pMaskBlue*</span><span class="sxs-lookup"><span data-stu-id="71f1e-111">*pMaskBlue*</span></span> 
</dt> <dd>

<span data-ttu-id="71f1e-112">Puntero a una variable que recibe la máscara de componente azul.</span><span class="sxs-lookup"><span data-stu-id="71f1e-112">Pointer to a variable that receives the blue-component mask.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71f1e-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="71f1e-113">Return value</span></span>

<span data-ttu-id="71f1e-114">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="71f1e-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="71f1e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71f1e-115">Requirements</span></span>



| <span data-ttu-id="71f1e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="71f1e-116">Requirement</span></span> | <span data-ttu-id="71f1e-117">Value</span><span class="sxs-lookup"><span data-stu-id="71f1e-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71f1e-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="71f1e-118">Header</span></span><br/>  | <dl> <span data-ttu-id="71f1e-119"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="71f1e-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="71f1e-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="71f1e-120">Library</span></span><br/> | <dl> <span data-ttu-id="71f1e-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="71f1e-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71f1e-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="71f1e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71f1e-123">**Clase CImageDisplay**</span><span class="sxs-lookup"><span data-stu-id="71f1e-123">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




