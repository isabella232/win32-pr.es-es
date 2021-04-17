---
description: El método GetClassWindowStyles recupera los estilos de clase y los estilos de ventana de la ventana.
ms.assetid: 6eec7912-c654-4e4f-b6f1-ec94c7284575
title: Método CBaseWindow. GetClassWindowStyles (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.GetClassWindowStyles
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a34332f84a91ee88d61ee5f29f0b6a0b0cc44714
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679570"
---
# <a name="cbasewindowgetclasswindowstyles-method"></a><span data-ttu-id="50add-103">CBaseWindow. GetClassWindowStyles, método</span><span class="sxs-lookup"><span data-stu-id="50add-103">CBaseWindow.GetClassWindowStyles method</span></span>

<span data-ttu-id="50add-104">El `GetClassWindowStyles` método recupera los estilos de clase y los estilos de ventana de la ventana.</span><span class="sxs-lookup"><span data-stu-id="50add-104">The `GetClassWindowStyles` method retrieves the window's class styles and window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="50add-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="50add-105">Syntax</span></span>


```C++
virtual LPTSTR GetClassWindowStyles(
   DWORD *pClassStyles,
   DWORD *pWindowStyles,
   DWORD *pWindowStylesEx
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="50add-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="50add-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50add-107">*pClassStyles*</span><span class="sxs-lookup"><span data-stu-id="50add-107">*pClassStyles*</span></span> 
</dt> <dd>

<span data-ttu-id="50add-108">Puntero a una variable que recibe los estilos de clase.</span><span class="sxs-lookup"><span data-stu-id="50add-108">Pointer to a variable that receives the class styles.</span></span>

</dd> <dt>

<span data-ttu-id="50add-109">*pWindowStyles*</span><span class="sxs-lookup"><span data-stu-id="50add-109">*pWindowStyles*</span></span> 
</dt> <dd>

<span data-ttu-id="50add-110">Puntero a una variable que recibe los estilos de ventana.</span><span class="sxs-lookup"><span data-stu-id="50add-110">Pointer to a variable that receives the window styles.</span></span>

</dd> <dt>

<span data-ttu-id="50add-111">*pWindowStylesEx*</span><span class="sxs-lookup"><span data-stu-id="50add-111">*pWindowStylesEx*</span></span> 
</dt> <dd>

<span data-ttu-id="50add-112">Puntero a una variable que recibe los estilos extendidos de ventana.</span><span class="sxs-lookup"><span data-stu-id="50add-112">Pointer to a variable that receives the extended window styles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50add-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="50add-113">Return value</span></span>

<span data-ttu-id="50add-114">Devuelve una cadena de texto estático que contiene el nombre de clase.</span><span class="sxs-lookup"><span data-stu-id="50add-114">Returns a static text string that contains the class name.</span></span>

## <a name="remarks"></a><span data-ttu-id="50add-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="50add-115">Remarks</span></span>

<span data-ttu-id="50add-116">El método [**CBaseWindow::P reparewindow**](cbasewindow-preparewindow.md) llama a este método para recuperar los estilos de clase y los estilos de ventana de la ventana.</span><span class="sxs-lookup"><span data-stu-id="50add-116">The [**CBaseWindow::PrepareWindow**](cbasewindow-preparewindow.md) method calls this method to retrieve the window's class styles and window styles.</span></span>

<span data-ttu-id="50add-117">Este método es virtual puro; la clase derivada debe implementarla.</span><span class="sxs-lookup"><span data-stu-id="50add-117">This method is pure virtual; the derived class must implement it.</span></span> <span data-ttu-id="50add-118">En el ejemplo siguiente se muestra una posible implementación:</span><span class="sxs-lookup"><span data-stu-id="50add-118">The following example shows a possible implementation:</span></span>


```C++
LPTSTR CMyWindowClass::GetClassWindowStyles(DWORD *pClassStyles,
                                            DWORD *pWindowStyles,
                                            DWORD *pWindowStylesEx)
{
    *pClassStyles = CS_HREDRAW | CS_VREDRAW;
    *pWindowStyles = WS_OVERLAPPEDWINDOW | WS_CLIPCHILDREN;
    *pWindowStylesEx = WS_EX_WINDOWEDGE;
    return TEXT("MyWindowClass");
}
```



<span data-ttu-id="50add-119">El objeto usa el estilo de clase para el miembro **lpszClassName** de una estructura WNDCLASS, que pasa a la función **RegisterClass** .</span><span class="sxs-lookup"><span data-stu-id="50add-119">The object uses the class style for the **lpszClassName** member of a WNDCLASS structure, which it passes to the **RegisterClass** function.</span></span> <span data-ttu-id="50add-120">El objeto usa los estilos de ventana para los parámetros *dwExStyle* y *dwStyle* de la función **CreateWindowEx** .</span><span class="sxs-lookup"><span data-stu-id="50add-120">The object uses the window styles for the *dwExStyle* and *dwStyle* parameters of the **CreateWindowEx** function.</span></span> <span data-ttu-id="50add-121">Para obtener más información, vea el SDK de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="50add-121">For more information, see the Platform SDK.</span></span>

## <a name="requirements"></a><span data-ttu-id="50add-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50add-122">Requirements</span></span>



| <span data-ttu-id="50add-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="50add-123">Requirement</span></span> | <span data-ttu-id="50add-124">Value</span><span class="sxs-lookup"><span data-stu-id="50add-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50add-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="50add-125">Header</span></span><br/>  | <dl> <span data-ttu-id="50add-126"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="50add-126"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="50add-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="50add-127">Library</span></span><br/> | <dl> <span data-ttu-id="50add-128"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="50add-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50add-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="50add-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50add-130">**Clase CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="50add-130">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




