---
description: 'Constructor CBaseWindow.CBaseWindow: método constructor.'
ms.assetid: 9f0b91c4-0364-4c73-b97f-86703ca3ef74
title: Constructor CBaseWindow.CBaseWindow (Winutil.h)
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
ms.openlocfilehash: 05205750810294076bf005d0e5b73fda6b2143d5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095823"
---
# <a name="cbasewindowcbasewindow-constructor"></a><span data-ttu-id="cef16-103">Constructor CBaseWindow.CBaseWindow</span><span class="sxs-lookup"><span data-stu-id="cef16-103">CBaseWindow.CBaseWindow constructor</span></span>

<span data-ttu-id="cef16-104">Método constructor.</span><span class="sxs-lookup"><span data-stu-id="cef16-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cef16-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cef16-105">Syntax</span></span>


```C++
CBaseWindow(
   BOOL bDoGetDC = TRUE,
   BOOL bPostToDestroy = FALSE
);
```



## <a name="parameters"></a><span data-ttu-id="cef16-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cef16-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cef16-107">*bDoGetDC*</span><span class="sxs-lookup"><span data-stu-id="cef16-107">*bDoGetDC*</span></span> 
</dt> <dd>

<span data-ttu-id="cef16-108">Valor booleano que especifica si se debe recuperar el contexto del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cef16-108">Boolean value that specifies whether to retrieve the device context.</span></span>

</dd> <dt>

<span data-ttu-id="cef16-109">*bPostToDestroy*</span><span class="sxs-lookup"><span data-stu-id="cef16-109">*bPostToDestroy*</span></span> 
</dt> <dd>

<span data-ttu-id="cef16-110">Valor booleano que especifica la variable [**miembro CBaseWindow::m \_ bDoPostToDestroy.**](cbasewindow-m-bdoposttodestroy.md)</span><span class="sxs-lookup"><span data-stu-id="cef16-110">Boolean value that specifies the [**CBaseWindow::m\_bDoPostToDestroy**](cbasewindow-m-bdoposttodestroy.md) member variable.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cef16-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cef16-111">Remarks</span></span>

<span data-ttu-id="cef16-112">Después de crear el objeto , llame al [**método CBaseWindow::P repareWindow**](cbasewindow-preparewindow.md) para crear la ventana.</span><span class="sxs-lookup"><span data-stu-id="cef16-112">After you create the object, call the [**CBaseWindow::PrepareWindow**](cbasewindow-preparewindow.md) method to create the window.</span></span> <span data-ttu-id="cef16-113">**PrepareWindow** es un método virtual.</span><span class="sxs-lookup"><span data-stu-id="cef16-113">**PrepareWindow** is a virtual method.</span></span> <span data-ttu-id="cef16-114">Llama a [**CBaseWindow::InitialiseWindow,**](cbasewindow-initialisewindow.md)también un método virtual.</span><span class="sxs-lookup"><span data-stu-id="cef16-114">It calls [**CBaseWindow::InitialiseWindow**](cbasewindow-initialisewindow.md), also a virtual method.</span></span> <span data-ttu-id="cef16-115">Estos métodos están separados del constructor para que las clases derivadas puedan invalidarlos, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="cef16-115">These methods are separated from the constructor so that derived classes can override them, if necessary.</span></span>

<span data-ttu-id="cef16-116">Si el valor del *parámetro bDoGetDC* es **TRUE,** el objeto recupera un identificador en el contexto de dispositivo (DC) de la ventana y lo almacena en la variable miembro `CBaseWindow` [**\_ hdc CBaseWindow::m.**](cbasewindow-m-hdc.md)</span><span class="sxs-lookup"><span data-stu-id="cef16-116">If the value of the *bDoGetDC* parameter is **TRUE**, the `CBaseWindow` object retrieves a handle to the window's device context (DC) and stores it in the [**CBaseWindow::m\_hdc**](cbasewindow-m-hdc.md) member variable.</span></span> <span data-ttu-id="cef16-117">El objeto también crea un controlador de dominio de memoria compatible, que almacena en la variable miembro [**CBaseWindow::m \_ MemoryDC.**](cbasewindow-m-memorydc.md)</span><span class="sxs-lookup"><span data-stu-id="cef16-117">The object also creates a compatible memory DC, which it stores in the [**CBaseWindow::m\_MemoryDC**](cbasewindow-m-memorydc.md) member variable.</span></span> <span data-ttu-id="cef16-118">Estas acciones se producen en el **método InitialiseWindow.**</span><span class="sxs-lookup"><span data-stu-id="cef16-118">These actions occur in the **InitialiseWindow** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="cef16-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cef16-119">Requirements</span></span>



| <span data-ttu-id="cef16-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="cef16-120">Requirement</span></span> | <span data-ttu-id="cef16-121">Value</span><span class="sxs-lookup"><span data-stu-id="cef16-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cef16-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cef16-122">Header</span></span><br/>  | <dl> <span data-ttu-id="cef16-123"><dt>Winutil.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="cef16-123"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cef16-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cef16-124">Library</span></span><br/> | <dl> <span data-ttu-id="cef16-125"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="cef16-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cef16-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="cef16-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cef16-127">**CBaseWindow (clase)**</span><span class="sxs-lookup"><span data-stu-id="cef16-127">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




