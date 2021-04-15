---
description: La función FilterAddObject agrega un solo objeto a un filtro de presentación.
ms.assetid: 796216f4-a407-4a8c-98b3-8c3761d91913
title: Función FilterAddObject (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FilterAddObject
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 7fc6c41a675bfe560c060e271e4f9f48f88cd58c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497002"
---
# <a name="filteraddobject-function"></a><span data-ttu-id="0998e-103">FilterAddObject función)</span><span class="sxs-lookup"><span data-stu-id="0998e-103">FilterAddObject function</span></span>

<span data-ttu-id="0998e-104">La función **FilterAddObject** agrega un solo objeto a un [*filtro de presentación*](d.md).</span><span class="sxs-lookup"><span data-stu-id="0998e-104">The **FilterAddObject** function adds a single object to a [*display filter*](d.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0998e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0998e-105">Syntax</span></span>


```C++
DWORD WINAPI FilterAddObject(
  _In_  HFILTER        hFilter,
  _Out_ LPFILTEROBJECT lpFilterObject
);
```



## <a name="parameters"></a><span data-ttu-id="0998e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0998e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0998e-107">*hFilter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0998e-107">*hFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0998e-108">Identificador del filtro de presentación.</span><span class="sxs-lookup"><span data-stu-id="0998e-108">Handle to the display filter.</span></span>

</dd> <dt>

<span data-ttu-id="0998e-109">*lpFilterObject* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0998e-109">*lpFilterObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0998e-110">Puntero a una estructura [FILTEROBJECT](filterobject.md) que define el objeto que se va a agregar al filtro.</span><span class="sxs-lookup"><span data-stu-id="0998e-110">Pointer to a [FILTEROBJECT](filterobject.md) structure that defines the object to be added to the filter.</span></span> <span data-ttu-id="0998e-111">Cada objeto puede ser un operador, un valor o una propiedad.</span><span class="sxs-lookup"><span data-stu-id="0998e-111">Each object can be an operator, value, or property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0998e-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0998e-112">Return value</span></span>

<span data-ttu-id="0998e-113">Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="0998e-113">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="0998e-114">Si la función no es correcta, el valor devuelto es un código de error.</span><span class="sxs-lookup"><span data-stu-id="0998e-114">If the function is unsuccessful, the return value is an error code.</span></span>



| <span data-ttu-id="0998e-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="0998e-115">Return code</span></span>                                                                                              | <span data-ttu-id="0998e-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="0998e-116">Description</span></span>                                                                  |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0998e-117"><dt>**NMERR \_ parámetro no válido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0998e-117"><dt>**NMERR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="0998e-118">El parámetro *hFilter* tiene un valor no válido.</span><span class="sxs-lookup"><span data-stu-id="0998e-118">The *hFilter* parameter has an invalid value.</span></span><br/>                     |
| <dl> <span data-ttu-id="0998e-119"><dt>**NMERR \_ \_ de \_ memoria insuficiente**</dt></span><span class="sxs-lookup"><span data-stu-id="0998e-119"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl>    | <span data-ttu-id="0998e-120">Monitor de red no tiene suficiente memoria para crear el objeto.</span><span class="sxs-lookup"><span data-stu-id="0998e-120">Network Monitor does not have enough memory to create the object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0998e-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0998e-121">Remarks</span></span>

<span data-ttu-id="0998e-122">Los [*expertos*](e.md) y [*analizadores*](p.md) pueden llamar a la función **FilterAddObject** .</span><span class="sxs-lookup"><span data-stu-id="0998e-122">[*Experts*](e.md) and [*parsers*](p.md) can call the **FilterAddObject** function.</span></span>

<span data-ttu-id="0998e-123">Se llama a la función **FilterAddObject** cada vez que se agrega un objeto de filtro al filtro de presentación.</span><span class="sxs-lookup"><span data-stu-id="0998e-123">The **FilterAddObject** function is called each time a filter object is added to the display filter.</span></span> <span data-ttu-id="0998e-124">El filtro de visualización es una pila de objetos postfijo que puede ser un operador, un valor o una propiedad.</span><span class="sxs-lookup"><span data-stu-id="0998e-124">The display filter is a postfix stack of objects that can be an operator, value, or property.</span></span>

## <a name="requirements"></a><span data-ttu-id="0998e-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0998e-125">Requirements</span></span>



| <span data-ttu-id="0998e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="0998e-126">Requirement</span></span> | <span data-ttu-id="0998e-127">Value</span><span class="sxs-lookup"><span data-stu-id="0998e-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0998e-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0998e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0998e-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0998e-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="0998e-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0998e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0998e-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0998e-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0998e-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0998e-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="0998e-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0998e-133"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="0998e-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0998e-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="0998e-135"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0998e-135"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="0998e-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0998e-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0998e-137"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0998e-137"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0998e-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="0998e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0998e-139">FILTEROBJECT</span><span class="sxs-lookup"><span data-stu-id="0998e-139">FILTEROBJECT</span></span>](filterobject.md)
</dt> </dl>

 

 




