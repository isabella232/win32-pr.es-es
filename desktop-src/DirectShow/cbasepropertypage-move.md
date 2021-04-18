---
description: 'El método move coloca y cambia el tamaño del cuadro de diálogo. Este método implementa el método IPropertyPage:: Move.'
ms.assetid: b6cabb5c-196d-489b-9dd4-194d26f4de83
title: Método CBasePropertyPage. Move (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Move
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4d293f6ccb6a1bcd730ce997367c179f1747f66e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671090"
---
# <a name="cbasepropertypagemove-method"></a><span data-ttu-id="25831-104">CBasePropertyPage. Move (método)</span><span class="sxs-lookup"><span data-stu-id="25831-104">CBasePropertyPage.Move method</span></span>

<span data-ttu-id="25831-105">El `Move` método coloca y cambia el tamaño del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="25831-105">The `Move` method positions and resizes the dialog box.</span></span> <span data-ttu-id="25831-106">Este método implementa el método **IPropertyPage:: Move** .</span><span class="sxs-lookup"><span data-stu-id="25831-106">This method implements the **IPropertyPage::Move** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="25831-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="25831-107">Syntax</span></span>


```C++
HRESULT Move(
   LPCRECT prect
);
```



## <a name="parameters"></a><span data-ttu-id="25831-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="25831-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25831-109">*prect*</span><span class="sxs-lookup"><span data-stu-id="25831-109">*prect*</span></span> 
</dt> <dd>

<span data-ttu-id="25831-110">Puntero a una estructura **Rect** que contiene la información de posición.</span><span class="sxs-lookup"><span data-stu-id="25831-110">Pointer to a **RECT** structure containing the positioning information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25831-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="25831-111">Return value</span></span>

<span data-ttu-id="25831-112">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="25831-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="25831-113">Estos son algunos de los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="25831-113">Possible values include the following.</span></span>



| <span data-ttu-id="25831-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="25831-114">Return code</span></span>                                                                                  | <span data-ttu-id="25831-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="25831-115">Description</span></span>                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="25831-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="25831-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="25831-117">Correcto.</span><span class="sxs-lookup"><span data-stu-id="25831-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="25831-118"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="25831-118"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="25831-119">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="25831-119">**NULL** pointer argument.</span></span><br/> |
| <dl> <span data-ttu-id="25831-120"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="25831-120"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="25831-121">Error inesperado.</span><span class="sxs-lookup"><span data-stu-id="25831-121">Unexpected failure.</span></span><br/>        |



 

## <a name="requirements"></a><span data-ttu-id="25831-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25831-122">Requirements</span></span>



| <span data-ttu-id="25831-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="25831-123">Requirement</span></span> | <span data-ttu-id="25831-124">Value</span><span class="sxs-lookup"><span data-stu-id="25831-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25831-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="25831-125">Header</span></span><br/>  | <dl> <span data-ttu-id="25831-126"><dt>Cprop. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="25831-126"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="25831-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="25831-127">Library</span></span><br/> | <dl> <span data-ttu-id="25831-128"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="25831-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25831-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="25831-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25831-130">**Clase CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="25831-130">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




