---
description: 'El método Show muestra u oculta el cuadro de diálogo. Este método implementa el método IPropertyPage:: show.'
ms.assetid: 03796779-ed41-4b68-852d-6b1849a9dc10
title: Método CBasePropertyPage. Show (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Show
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1dadd1c187773df3ca41ac0e1e4daf06fb54761b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671267"
---
# <a name="cbasepropertypageshow-method"></a><span data-ttu-id="c848d-104">CBasePropertyPage. Show (método)</span><span class="sxs-lookup"><span data-stu-id="c848d-104">CBasePropertyPage.Show method</span></span>

<span data-ttu-id="c848d-105">El `Show` método muestra u oculta el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c848d-105">The `Show` method shows or hides the dialog box.</span></span> <span data-ttu-id="c848d-106">Este método implementa el método [IPropertyPage:: show](/windows/win32/api/ocidl/nf-ocidl-ipropertypage-show) .</span><span class="sxs-lookup"><span data-stu-id="c848d-106">This method implements the [IPropertyPage::Show](/windows/win32/api/ocidl/nf-ocidl-ipropertypage-show) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c848d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c848d-107">Syntax</span></span>

```C++
HRESULT Show(
   UINT nCmdShow
);
```
## <a name="parameters"></a><span data-ttu-id="c848d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c848d-108">Parameters</span></span>

<span data-ttu-id="c848d-109">*nCmdShow*</span><span class="sxs-lookup"><span data-stu-id="c848d-109">*nCmdShow*</span></span>

<span data-ttu-id="c848d-110">Tipo: **[uint](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c848d-110">Type: **[UINT](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c848d-111">Valor que especifica si se debe mostrar u ocultar la ventana.</span><span class="sxs-lookup"><span data-stu-id="c848d-111">Value that specifies whether to show or hide the window.</span></span> <span data-ttu-id="c848d-112">Para obtener más información, vea el método [IPropertyPage:: show](/windows/win32/api/ocidl/nf-ocidl-ipropertypage-show) .</span><span class="sxs-lookup"><span data-stu-id="c848d-112">For more information, see the [IPropertyPage::Show](/windows/win32/api/ocidl/nf-ocidl-ipropertypage-show) method.</span></span>

## <a name="return-value"></a><span data-ttu-id="c848d-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c848d-113">Return value</span></span>

<span data-ttu-id="c848d-114">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c848d-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="c848d-115">Estos son algunos de los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="c848d-115">Possible values include the following.</span></span>

| <span data-ttu-id="c848d-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c848d-116">Return code</span></span>                                                                                  | <span data-ttu-id="c848d-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="c848d-117">Description</span></span>                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="c848d-118"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="c848d-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="c848d-119">Correcto.</span><span class="sxs-lookup"><span data-stu-id="c848d-119">Success.</span></span><br/>            |
| <dl> <span data-ttu-id="c848d-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c848d-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="c848d-121">Argumento no válido.</span><span class="sxs-lookup"><span data-stu-id="c848d-121">Invalid argument.</span></span><br/>   |
| <dl> <span data-ttu-id="c848d-122"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="c848d-122"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="c848d-123">Error inesperado.</span><span class="sxs-lookup"><span data-stu-id="c848d-123">Unexpected failure.</span></span><br/> |

## <a name="requirements"></a><span data-ttu-id="c848d-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c848d-124">Requirements</span></span>

| <span data-ttu-id="c848d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c848d-125">Requirement</span></span> | <span data-ttu-id="c848d-126">Value</span><span class="sxs-lookup"><span data-stu-id="c848d-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c848d-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c848d-127">Header</span></span>  | <dl> <span data-ttu-id="c848d-128"><dt>Cprop. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c848d-128"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="c848d-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c848d-129">Library</span></span> | <dl> <span data-ttu-id="c848d-130"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="c848d-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="c848d-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="c848d-131">See also</span></span>

[<span data-ttu-id="c848d-132">Clase CBasePropertyPage</span><span class="sxs-lookup"><span data-stu-id="c848d-132">CBasePropertyPage Class</span></span>](cbasepropertypage.md)
