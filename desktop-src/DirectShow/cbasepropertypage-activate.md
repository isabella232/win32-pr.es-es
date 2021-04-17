---
description: 'El método Activate crea la ventana de cuadro de diálogo. Este método implementa el método IPropertyPage:: Activate.'
ms.assetid: 8f030dc5-1d14-46b5-9d40-7f07a1177dbe
title: Método CBasePropertyPage. Activate (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Activate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4b851cfc4490d25e7e30dfd2cf0e7c33b0e76224
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670843"
---
# <a name="cbasepropertypageactivate-method"></a><span data-ttu-id="1e9f3-104">CBasePropertyPage. Activate (método)</span><span class="sxs-lookup"><span data-stu-id="1e9f3-104">CBasePropertyPage.Activate method</span></span>

<span data-ttu-id="1e9f3-105">El `Activate` método crea la ventana de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="1e9f3-105">The `Activate` method creates the dialog box window.</span></span> <span data-ttu-id="1e9f3-106">Este método implementa el método **IPropertyPage:: Activate** .</span><span class="sxs-lookup"><span data-stu-id="1e9f3-106">This method implements the **IPropertyPage::Activate** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e9f3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1e9f3-107">Syntax</span></span>


```C++
HRESULT Activate(
   HWND    hwndParent,
   LPCRECT prect,
   BOOL    fModal
);
```



## <a name="parameters"></a><span data-ttu-id="1e9f3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1e9f3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e9f3-109">*hwndParent*</span><span class="sxs-lookup"><span data-stu-id="1e9f3-109">*hwndParent*</span></span> 
</dt> <dd>

<span data-ttu-id="1e9f3-110">Identificador de la ventana primaria del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="1e9f3-110">Handle to the parent window of the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="1e9f3-111">*prect*</span><span class="sxs-lookup"><span data-stu-id="1e9f3-111">*prect*</span></span> 
</dt> <dd>

<span data-ttu-id="1e9f3-112">Puntero a una estructura **Rect** que contiene información de posición del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="1e9f3-112">Pointer to a **RECT** structure that contains positioning information for the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="1e9f3-113">*fModal*</span><span class="sxs-lookup"><span data-stu-id="1e9f3-113">*fModal*</span></span> 
</dt> <dd>

<span data-ttu-id="1e9f3-114">Valor booleano que indica si el marco del cuadro de diálogo es modal (**true**) o no modal (**false**).</span><span class="sxs-lookup"><span data-stu-id="1e9f3-114">Boolean value indicating whether the dialog box frame is modal (**TRUE**) or modeless (**FALSE**).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e9f3-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1e9f3-115">Return value</span></span>

<span data-ttu-id="1e9f3-116">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1e9f3-116">Returns an **HRESULT** value.</span></span> <span data-ttu-id="1e9f3-117">Estos son algunos de los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="1e9f3-117">Possible values include the following.</span></span>



| <span data-ttu-id="1e9f3-118">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="1e9f3-118">Return code</span></span>                                                                                   | <span data-ttu-id="1e9f3-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="1e9f3-119">Description</span></span>                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="1e9f3-120"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="1e9f3-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1e9f3-121">Correcto.</span><span class="sxs-lookup"><span data-stu-id="1e9f3-121">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="1e9f3-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1e9f3-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="1e9f3-123">Memoria insuficiente.</span><span class="sxs-lookup"><span data-stu-id="1e9f3-123">Insufficient memory.</span></span><br/>       |
| <dl> <span data-ttu-id="1e9f3-124"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="1e9f3-124"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="1e9f3-125">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="1e9f3-125">**NULL** pointer argument.</span></span><br/> |
| <dl> <span data-ttu-id="1e9f3-126"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="1e9f3-126"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>  | <span data-ttu-id="1e9f3-127">Error inesperado.</span><span class="sxs-lookup"><span data-stu-id="1e9f3-127">Unexpected failure.</span></span><br/>        |



 

## <a name="requirements"></a><span data-ttu-id="1e9f3-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e9f3-128">Requirements</span></span>



| <span data-ttu-id="1e9f3-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e9f3-129">Requirement</span></span> | <span data-ttu-id="1e9f3-130">Value</span><span class="sxs-lookup"><span data-stu-id="1e9f3-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e9f3-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1e9f3-131">Header</span></span><br/>  | <dl> <span data-ttu-id="1e9f3-132"><dt>Cprop. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1e9f3-132"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="1e9f3-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1e9f3-133">Library</span></span><br/> | <dl> <span data-ttu-id="1e9f3-134"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="1e9f3-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e9f3-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="1e9f3-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e9f3-136">**Clase CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="1e9f3-136">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> <dt>

[<span data-ttu-id="1e9f3-137">**CBasePropertyPage:: OnActivate**</span><span class="sxs-lookup"><span data-stu-id="1e9f3-137">**CBasePropertyPage::OnActivate**</span></span>](cbasepropertypage-onactivate.md)
</dt> </dl>

 

 




