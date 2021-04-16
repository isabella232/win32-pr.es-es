---
description: La función FindPropertyInstance busca la primera instancia de la propiedad especificada por el parámetro hProperty.
ms.assetid: e994503d-2f32-4fa2-bba9-ff66c9d558dc
title: Función FindPropertyInstance (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindPropertyInstance
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 21f94a3e4a1eb9619b39cff534a778235980a278
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666289"
---
# <a name="findpropertyinstance-function"></a><span data-ttu-id="180b4-103">FindPropertyInstance función)</span><span class="sxs-lookup"><span data-stu-id="180b4-103">FindPropertyInstance function</span></span>

<span data-ttu-id="180b4-104">La función **FindPropertyInstance** busca la primera instancia de la propiedad especificada por el parámetro *hProperty* .</span><span class="sxs-lookup"><span data-stu-id="180b4-104">The **FindPropertyInstance** function finds the first instance of the property specified by the *hProperty* parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="180b4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="180b4-105">Syntax</span></span>


```C++
LPPROPERTYINST WINAPI FindPropertyInstance(
  _In_ HFRAME    hFrame,
  _In_ HPROPERTY hProperty
);
```



## <a name="parameters"></a><span data-ttu-id="180b4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="180b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="180b4-107">*hFrame* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="180b4-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="180b4-108">Identificador del marco.</span><span class="sxs-lookup"><span data-stu-id="180b4-108">Handle to the frame.</span></span> <span data-ttu-id="180b4-109">El identificador del marco se puede recuperar mediante una llamada a la función [GetFrame](getframe.md) .</span><span class="sxs-lookup"><span data-stu-id="180b4-109">The frame handle can be retrieved by a call to the [GetFrame](getframe.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="180b4-110">*hProperty* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="180b4-110">*hProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="180b4-111">Identificador de la propiedad que se desea buscar.</span><span class="sxs-lookup"><span data-stu-id="180b4-111">Handle to the property you want to find.</span></span> <span data-ttu-id="180b4-112">El identificador de propiedad se puede recuperar mediante una llamada a la función [GetProperty](getproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="180b4-112">The property handle can be retrieved by a call to the [GetProperty](getproperty.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="180b4-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="180b4-113">Return value</span></span>

<span data-ttu-id="180b4-114">Si la función es correcta (es decir, si se encuentra la propiedad), el valor devuelto es un puntero a la primera instancia de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="180b4-114">If the function is successful (that is, if the property is found), the return value is a pointer to the first instance of the property.</span></span>

<span data-ttu-id="180b4-115">Si la función no se realiza correctamente, el valor devuelto es **null**.</span><span class="sxs-lookup"><span data-stu-id="180b4-115">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="180b4-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="180b4-116">Remarks</span></span>

<span data-ttu-id="180b4-117">Para recuperar la siguiente instancia de la propiedad, llame a [FindPropertyInstanceRestart](findpropertyinstancerestart.md).</span><span class="sxs-lookup"><span data-stu-id="180b4-117">To retrieve the next instance of the property, call [FindPropertyInstanceRestart](findpropertyinstancerestart.md).</span></span>

<span data-ttu-id="180b4-118">Los [*expertos*](e.md) y [*analizadores*](p.md)pueden llamar a la función **FindPropertyInstance** .</span><span class="sxs-lookup"><span data-stu-id="180b4-118">[*Experts*](e.md) and [*parsers*](p.md)can call the **FindPropertyInstance** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="180b4-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="180b4-119">Requirements</span></span>



| <span data-ttu-id="180b4-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="180b4-120">Requirement</span></span> | <span data-ttu-id="180b4-121">Value</span><span class="sxs-lookup"><span data-stu-id="180b4-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="180b4-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="180b4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="180b4-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="180b4-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="180b4-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="180b4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="180b4-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="180b4-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="180b4-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="180b4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="180b4-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="180b4-127"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="180b4-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="180b4-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="180b4-129"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="180b4-129"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="180b4-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="180b4-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="180b4-131"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="180b4-131"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="180b4-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="180b4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="180b4-133">FindPropertyInstanceRestart</span><span class="sxs-lookup"><span data-stu-id="180b4-133">FindPropertyInstanceRestart</span></span>](findpropertyinstancerestart.md)
</dt> </dl>

 

 




