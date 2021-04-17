---
description: 'El método TranslateAccelerator indica a la página de propiedades que procese una pulsación de tecla. Este método implementa el método IPropertyPage:: TranslateAccelerator.'
ms.assetid: 2da214c9-35dc-470c-9b7f-2f4ef6bcd40a
title: Método CBasePropertyPage. TranslateAccelerator (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.TranslateAccelerator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3116e85eec8fbf3a00bf434a1f88c8cac662ed0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660175"
---
# <a name="cbasepropertypagetranslateaccelerator-method"></a><span data-ttu-id="480a3-104">CBasePropertyPage. TranslateAccelerator (método)</span><span class="sxs-lookup"><span data-stu-id="480a3-104">CBasePropertyPage.TranslateAccelerator method</span></span>

<span data-ttu-id="480a3-105">El `TranslateAccelerator` método indica a la página de propiedades que procese una pulsación de tecla.</span><span class="sxs-lookup"><span data-stu-id="480a3-105">The `TranslateAccelerator` method instructs the property page to process a keystroke.</span></span> <span data-ttu-id="480a3-106">Este método implementa el método **IPropertyPage:: TranslateAccelerator** .</span><span class="sxs-lookup"><span data-stu-id="480a3-106">This method implements the **IPropertyPage::TranslateAccelerator** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="480a3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="480a3-107">Syntax</span></span>


```C++
HRESULT TranslateAccelerator(
   LPMSG lpMsg
);
```



## <a name="parameters"></a><span data-ttu-id="480a3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="480a3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="480a3-109">*lpMsg*</span><span class="sxs-lookup"><span data-stu-id="480a3-109">*lpMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="480a3-110">Puntero a una estructura **MSG** que describe la pulsación de tecla que se va a procesar.</span><span class="sxs-lookup"><span data-stu-id="480a3-110">Pointer to a **MSG** structure describing the keystroke to process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="480a3-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="480a3-111">Return value</span></span>

<span data-ttu-id="480a3-112">Devuelve E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="480a3-112">Returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="480a3-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="480a3-113">Remarks</span></span>

<span data-ttu-id="480a3-114">Invalide este método si desea proporcionar aceleradores de teclado para la página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="480a3-114">Override this method if you want to provide keyboard accelerators for the property page.</span></span>

## <a name="requirements"></a><span data-ttu-id="480a3-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="480a3-115">Requirements</span></span>



| <span data-ttu-id="480a3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="480a3-116">Requirement</span></span> | <span data-ttu-id="480a3-117">Value</span><span class="sxs-lookup"><span data-stu-id="480a3-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="480a3-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="480a3-118">Header</span></span><br/>  | <dl> <span data-ttu-id="480a3-119"><dt>Cprop. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="480a3-119"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="480a3-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="480a3-120">Library</span></span><br/> | <dl> <span data-ttu-id="480a3-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="480a3-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="480a3-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="480a3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="480a3-123">**Clase CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="480a3-123">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




