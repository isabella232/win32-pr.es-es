---
description: Busca la siguiente instancia de la propiedad especificada por el parámetro hProperty.
ms.assetid: f77cb92b-5936-4349-bf66-643c16e9e0df
title: Función FindPropertyInstanceRestart (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindPropertyInstanceRestart
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: d1e731bb00b28bb62862dd18fbd6031fa973fe38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666288"
---
# <a name="findpropertyinstancerestart-function"></a><span data-ttu-id="51393-103">FindPropertyInstanceRestart función)</span><span class="sxs-lookup"><span data-stu-id="51393-103">FindPropertyInstanceRestart function</span></span>

<span data-ttu-id="51393-104">La función **FindPropertyInstanceRestart** busca la siguiente instancia de la propiedad especificada por el parámetro *hProperty* .</span><span class="sxs-lookup"><span data-stu-id="51393-104">The **FindPropertyInstanceRestart** function finds the next instance of the property specified by the *hProperty* parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="51393-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="51393-105">Syntax</span></span>


```C++
LPPROPERTYINST WINAPI FindPropertyInstanceRestart(
  _In_ HFRAME         hFrame,
  _In_ HPROPERTY      hProperty,
  _In_ LPPROPERTYINST *lpRestartKey,
  _In_ BOOL           DirForward
);
```



## <a name="parameters"></a><span data-ttu-id="51393-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="51393-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51393-107">*hFrame* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="51393-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51393-108">Identificador del marco.</span><span class="sxs-lookup"><span data-stu-id="51393-108">A handle to the frame.</span></span> <span data-ttu-id="51393-109">El identificador del marco se puede recuperar mediante una llamada a la función [GetFrame](getframe.md) .</span><span class="sxs-lookup"><span data-stu-id="51393-109">The frame handle can be retrieved by a call to the [GetFrame](getframe.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="51393-110">*hProperty* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="51393-110">*hProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51393-111">Identificador de la propiedad que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="51393-111">A handle to the property to find.</span></span> <span data-ttu-id="51393-112">El identificador de propiedad se puede recuperar mediante una llamada a la función [GetProperty](getproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="51393-112">The property handle can be retrieved by a call to the [GetProperty](getproperty.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="51393-113">*lpRestartKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="51393-113">*lpRestartKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51393-114">Puntero a la instancia de propiedad que se usa como punto inicial de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="51393-114">A pointer to the property instance used as the starting point of the search.</span></span> <span data-ttu-id="51393-115">Si el parámetro *lpRestartKey* se establece en **null**, la búsqueda comienza al principio del marco o al final del marco, dependiendo del valor del parámetro *DirForward* .</span><span class="sxs-lookup"><span data-stu-id="51393-115">If the *lpRestartKey* parameter is set to **NULL**, the search begins at beginning of the frame, or the end of the frame, depending on the value of the *DirForward* parameter.</span></span>

<span data-ttu-id="51393-116">Si *lpRestartKey* apunta a **null**, la búsqueda comienza al principio del marco si *DirForward* es **true** o al final del marco si el parámetro es **false**.</span><span class="sxs-lookup"><span data-stu-id="51393-116">If *lpRestartKey* points to **NULL**, the search begins at the beginning of the frame if *DirForward* is **TRUE** or the at end of the frame if the parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="51393-117">*DirForward* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="51393-117">*DirForward* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51393-118">Indicador de la dirección de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="51393-118">An indicator of the search direction.</span></span> <span data-ttu-id="51393-119">Si el valor es **true**, la búsqueda se desplaza desde la ubicación actual hasta el final del marco.</span><span class="sxs-lookup"><span data-stu-id="51393-119">If the value is **TRUE**, the search moves from the current location to the end of the frame.</span></span> <span data-ttu-id="51393-120">Si el valor es **false**, la búsqueda se desplaza desde la ubicación actual hasta el principio del marco.</span><span class="sxs-lookup"><span data-stu-id="51393-120">If the value is **FALSE**, the search moves from the current location to the beginning of the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51393-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="51393-121">Return value</span></span>

<span data-ttu-id="51393-122">Si la función se realiza correctamente, el valor devuelto es el siguiente **LPPROPERTYINST** válido.</span><span class="sxs-lookup"><span data-stu-id="51393-122">If the function is successful, the return value is the next valid **LPPROPERTYINST**.</span></span>

<span data-ttu-id="51393-123">Si la función no se realiza correctamente, el valor devuelto es **null**.</span><span class="sxs-lookup"><span data-stu-id="51393-123">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="51393-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="51393-124">Remarks</span></span>

<span data-ttu-id="51393-125">Los [*expertos*](e.md) y [*analizadores*](p.md) pueden llamar a la función **FindPropertyInstanceRestart** .</span><span class="sxs-lookup"><span data-stu-id="51393-125">[*Experts*](e.md) and [*parsers*](p.md) can call the **FindPropertyInstanceRestart** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="51393-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51393-126">Requirements</span></span>



| <span data-ttu-id="51393-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="51393-127">Requirement</span></span> | <span data-ttu-id="51393-128">Value</span><span class="sxs-lookup"><span data-stu-id="51393-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="51393-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="51393-129">Minimum supported client</span></span><br/> | <span data-ttu-id="51393-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="51393-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="51393-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="51393-131">Minimum supported server</span></span><br/> | <span data-ttu-id="51393-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="51393-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="51393-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="51393-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="51393-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="51393-134"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="51393-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="51393-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="51393-136"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="51393-136"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="51393-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="51393-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51393-138"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51393-138"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51393-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="51393-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51393-140">GetFrame</span><span class="sxs-lookup"><span data-stu-id="51393-140">GetFrame</span></span>](getframe.md)
</dt> <dt>

[<span data-ttu-id="51393-141">GetProperty</span><span class="sxs-lookup"><span data-stu-id="51393-141">GetProperty</span></span>](getproperty.md)
</dt> </dl>

 

 




