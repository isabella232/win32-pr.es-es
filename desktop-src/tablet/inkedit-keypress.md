---
description: Se produce cuando el usuario presiona y suelta una tecla mientras el control InkEdit tiene el foco.
ms.assetid: 8284ab41-dfac-4da2-b101-6968a43b15d7
title: Evento InkEdit. KeyPress (autodibujado. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e49264f82b2cfe3c6998666339f08340a540791
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716313"
---
# <a name="inkeditkeypress-event"></a><span data-ttu-id="7c79b-103">Evento InkEdit. KeyPress</span><span class="sxs-lookup"><span data-stu-id="7c79b-103">InkEdit.KeyPress event</span></span>

<span data-ttu-id="7c79b-104">Se produce cuando el usuario presiona y suelta una tecla mientras el control [InkEdit](inkedit-control-reference.md) tiene el foco.</span><span class="sxs-lookup"><span data-stu-id="7c79b-104">Occurs when the user presses and releases a key while the [InkEdit](inkedit-control-reference.md) control has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c79b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7c79b-105">Syntax</span></span>


```C++
HRESULT KeyPress(
   Long *Char
);
```



## <a name="parameters"></a><span data-ttu-id="7c79b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7c79b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c79b-107">*Char*</span><span class="sxs-lookup"><span data-stu-id="7c79b-107">*Char*</span></span> 
</dt> <dd>

<span data-ttu-id="7c79b-108">Un entero que devuelve un valor de KeyCode ANSI estándar numérico.</span><span class="sxs-lookup"><span data-stu-id="7c79b-108">An integer that returns a standard numeric ANSI keycode.</span></span> <span data-ttu-id="7c79b-109">El parámetro *Char* se pasa por referencia; al cambiarlo, se envía un carácter diferente al control.</span><span class="sxs-lookup"><span data-stu-id="7c79b-109">The *Char* parameter is passed by reference; changing it sends a different character to the control.</span></span> <span data-ttu-id="7c79b-110">Al cambiar el parámetro *Char* a 0 se cancela el evento.</span><span class="sxs-lookup"><span data-stu-id="7c79b-110">Changing the *Char* parameter to 0 cancels the event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c79b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7c79b-111">Return value</span></span>

<span data-ttu-id="7c79b-112">Si este evento se realiza correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="7c79b-112">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7c79b-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7c79b-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c79b-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7c79b-114">Remarks</span></span>

<span data-ttu-id="7c79b-115">Este método de evento se define en la interfaz **\_ IInkEditEvents** .</span><span class="sxs-lookup"><span data-stu-id="7c79b-115">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="7c79b-116">La interfaz **\_ IInkEditEvents** implementa la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de DISPID \_ IeeKeyPress.</span><span class="sxs-lookup"><span data-stu-id="7c79b-116">The **\_IInkEditEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IeeKeyPress.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c79b-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c79b-117">Requirements</span></span>



| <span data-ttu-id="7c79b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c79b-118">Requirement</span></span> | <span data-ttu-id="7c79b-119">Value</span><span class="sxs-lookup"><span data-stu-id="7c79b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c79b-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c79b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7c79b-121">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="7c79b-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7c79b-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c79b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7c79b-123">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="7c79b-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="7c79b-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7c79b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c79b-125"><dt>Autodibujado. h (también requiere la intermano \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7c79b-125"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7c79b-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7c79b-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="7c79b-127"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c79b-127"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="7c79b-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="7c79b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c79b-129">InkEdit</span><span class="sxs-lookup"><span data-stu-id="7c79b-129">InkEdit</span></span>](inkedit-control-reference.md)
</dt> <dt>

<span data-ttu-id="7c79b-130">[**Control InkEdit de evento KeyDown \[\]**](inkedit-keydown.md)</span><span class="sxs-lookup"><span data-stu-id="7c79b-130">[**KeyDown Event \[InkEdit Control\]**](inkedit-keydown.md)</span></span>
</dt> <dt>

<span data-ttu-id="7c79b-131">[**Control InkEdit de evento KeyUp \[\]**](inkedit-keyup.md)</span><span class="sxs-lookup"><span data-stu-id="7c79b-131">[**KeyUp Event \[InkEdit Control\]**](inkedit-keyup.md)</span></span>
</dt> </dl>

 

