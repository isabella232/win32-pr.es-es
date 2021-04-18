---
description: Método de constructor.
ms.assetid: 9f0b91c4-0364-4c73-b97f-86703ca3ef74
title: Constructor CBaseWindow. CBaseWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.CBaseWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a1741f8596210afac676a7e81f57b46e18fbba9b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660236"
---
# <a name="cbasewindowcbasewindow-constructor"></a><span data-ttu-id="b9911-103">Constructor CBaseWindow. CBaseWindow</span><span class="sxs-lookup"><span data-stu-id="b9911-103">CBaseWindow.CBaseWindow constructor</span></span>

<span data-ttu-id="b9911-104">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="b9911-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9911-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b9911-105">Syntax</span></span>


```C++
CBaseWindow(
   BOOL bDoGetDC = TRUE,
   BOOL bPostToDestroy = FALSE
);
```



## <a name="parameters"></a><span data-ttu-id="b9911-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b9911-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9911-107">*bDoGetDC*</span><span class="sxs-lookup"><span data-stu-id="b9911-107">*bDoGetDC*</span></span> 
</dt> <dd>

<span data-ttu-id="b9911-108">Valor booleano que especifica si se debe recuperar el contexto del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b9911-108">Boolean value that specifies whether to retrieve the device context.</span></span>

</dd> <dt>

<span data-ttu-id="b9911-109">*bPostToDestroy*</span><span class="sxs-lookup"><span data-stu-id="b9911-109">*bPostToDestroy*</span></span> 
</dt> <dd>

<span data-ttu-id="b9911-110">Valor booleano que especifica la variable miembro [**CBaseWindow:: m \_ bDoPostToDestroy**](cbasewindow-m-bdoposttodestroy.md) .</span><span class="sxs-lookup"><span data-stu-id="b9911-110">Boolean value that specifies the [**CBaseWindow::m\_bDoPostToDestroy**](cbasewindow-m-bdoposttodestroy.md) member variable.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b9911-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b9911-111">Remarks</span></span>

<span data-ttu-id="b9911-112">Después de crear el objeto, llame al método [**CBaseWindow::P reparewindow**](cbasewindow-preparewindow.md) para crear la ventana.</span><span class="sxs-lookup"><span data-stu-id="b9911-112">After you create the object, call the [**CBaseWindow::PrepareWindow**](cbasewindow-preparewindow.md) method to create the window.</span></span> <span data-ttu-id="b9911-113">**PrepareWindow** es un método virtual.</span><span class="sxs-lookup"><span data-stu-id="b9911-113">**PrepareWindow** is a virtual method.</span></span> <span data-ttu-id="b9911-114">Llama a [**CBaseWindow:: InitialiseWindow**](cbasewindow-initialisewindow.md), también a un método virtual.</span><span class="sxs-lookup"><span data-stu-id="b9911-114">It calls [**CBaseWindow::InitialiseWindow**](cbasewindow-initialisewindow.md), also a virtual method.</span></span> <span data-ttu-id="b9911-115">Estos métodos se separan del constructor para que las clases derivadas puedan invalidarlos, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="b9911-115">These methods are separated from the constructor so that derived classes can override them, if necessary.</span></span>

<span data-ttu-id="b9911-116">Si el valor del parámetro *bDoGetDC* es **true**, el `CBaseWindow` objeto recupera un identificador para el contexto de dispositivo (DC) de la ventana y lo almacena en la variable miembro [**CBaseWindow:: m \_ HDC**](cbasewindow-m-hdc.md) .</span><span class="sxs-lookup"><span data-stu-id="b9911-116">If the value of the *bDoGetDC* parameter is **TRUE**, the `CBaseWindow` object retrieves a handle to the window's device context (DC) and stores it in the [**CBaseWindow::m\_hdc**](cbasewindow-m-hdc.md) member variable.</span></span> <span data-ttu-id="b9911-117">El objeto también crea un controlador de dominio de memoria compatible, que almacena en la variable miembro [**CBaseWindow:: m \_ MemoryDC**](cbasewindow-m-memorydc.md) .</span><span class="sxs-lookup"><span data-stu-id="b9911-117">The object also creates a compatible memory DC, which it stores in the [**CBaseWindow::m\_MemoryDC**](cbasewindow-m-memorydc.md) member variable.</span></span> <span data-ttu-id="b9911-118">Estas acciones se producen en el método **InitialiseWindow** .</span><span class="sxs-lookup"><span data-stu-id="b9911-118">These actions occur in the **InitialiseWindow** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9911-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9911-119">Requirements</span></span>



| <span data-ttu-id="b9911-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9911-120">Requirement</span></span> | <span data-ttu-id="b9911-121">Value</span><span class="sxs-lookup"><span data-stu-id="b9911-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9911-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b9911-122">Header</span></span><br/>  | <dl> <span data-ttu-id="b9911-123"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b9911-123"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b9911-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b9911-124">Library</span></span><br/> | <dl> <span data-ttu-id="b9911-125"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="b9911-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9911-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="b9911-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9911-127">**Clase CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="b9911-127">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




