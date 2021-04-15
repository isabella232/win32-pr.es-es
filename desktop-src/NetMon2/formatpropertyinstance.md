---
description: Da formato a los datos de instancia de la propiedad mediante el formateador genérico que proporciona Monitor de red.
ms.assetid: 36206601-7519-45c8-a14e-707b318c539d
title: Función FormatPropertyInstance (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FormatPropertyInstance
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 39d51df93a04efa8631fcfbd583075d7e3500bff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677293"
---
# <a name="formatpropertyinstance-function"></a><span data-ttu-id="8f26e-103">FormatPropertyInstance función)</span><span class="sxs-lookup"><span data-stu-id="8f26e-103">FormatPropertyInstance function</span></span>

<span data-ttu-id="8f26e-104">La función **FormatPropertyInstance** da formato a los datos de instancia de la propiedad mediante el formateador genérico que proporciona monitor de red.</span><span class="sxs-lookup"><span data-stu-id="8f26e-104">The **FormatPropertyInstance** function formats the property instance data using the generic formatter that Network Monitor provides.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f26e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8f26e-105">Syntax</span></span>


```C++
DWORD WINAPIV FormatPropertyInstance(
  _Inout_ LPPROPERTYINST lpPropertyInst
);
```



## <a name="parameters"></a><span data-ttu-id="8f26e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8f26e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f26e-107">*lpPropertyInst* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8f26e-107">*lpPropertyInst* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f26e-108">Puntero a una estructura [PROPERTYINST](propertyinst.md) que contiene los datos de instancia.</span><span class="sxs-lookup"><span data-stu-id="8f26e-108">A pointer to a [PROPERTYINST](propertyinst.md) structure that contains the instance data.</span></span>

<span data-ttu-id="8f26e-109">En la entrada, el formateador genérico toma los datos de la instancia de uno de los miembros de la Unión **PROPERTYINST** y convierte los datos en una cadena con formato predefinida.</span><span class="sxs-lookup"><span data-stu-id="8f26e-109">On input, the generic formatter takes the instance data from one of the **PROPERTYINST** union members and converts that data to a predefined formatted string.</span></span>

<span data-ttu-id="8f26e-110">En la salida, el formateador genérico establece el miembro **szPropertyText** de la estructura **PROPERTYINST** en un puntero a la cadena con formato.</span><span class="sxs-lookup"><span data-stu-id="8f26e-110">On output, the generic formatter sets the **szPropertyText** member of the **PROPERTYINST** structure to a pointer to the formatted string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f26e-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8f26e-111">Return value</span></span>

<span data-ttu-id="8f26e-112">Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="8f26e-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="8f26e-113">Si la función no es correcta, el valor devuelto es un código de error de NMerr. h.</span><span class="sxs-lookup"><span data-stu-id="8f26e-113">If the function is unsuccessful, the return value is an error code from NMerr.h.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f26e-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8f26e-114">Remarks</span></span>

<span data-ttu-id="8f26e-115">El archivo DLL del analizador llama indirectamente a la función **FormatPropertyInstance** cuando se requiere el formateador genérico para dar formato a los datos para su presentación en el panel de detalles de la interfaz de usuario de monitor de red.</span><span class="sxs-lookup"><span data-stu-id="8f26e-115">The parser DLL indirectly calls the **FormatPropertyInstance** function when the generic formatter is required to format data for display in the details pane of the Network Monitor UI.</span></span> <span data-ttu-id="8f26e-116">Para llamar a **FormatPropertyInstance** , especifíquelo en el miembro **InstanceData** de la estructura [PROPERTYINFO](propertyinfo.md) al definir la propiedad.</span><span class="sxs-lookup"><span data-stu-id="8f26e-116">To call **FormatPropertyInstance** specify it in the **InstanceData** member of the [PROPERTYINFO](propertyinfo.md) structure when you define the property.</span></span>

> [!Note]  
> <span data-ttu-id="8f26e-117">El analizador no reconoce la función a la que se llama cuando debe dar formato a una instancia de una propiedad.</span><span class="sxs-lookup"><span data-stu-id="8f26e-117">The parser does not recognize which function is called when it must format an instance of a property.</span></span> <span data-ttu-id="8f26e-118">La función puede ser **FormatPropertyInstance** o una función de formato personalizado definida por el analizador.</span><span class="sxs-lookup"><span data-stu-id="8f26e-118">The function can be **FormatPropertyInstance** or a custom format function defined by the parser.</span></span> <span data-ttu-id="8f26e-119">El analizador llama a la función de formato especificada por el miembro **InstanceData** de la estructura **PROPERTYINFO** para la propiedad.</span><span class="sxs-lookup"><span data-stu-id="8f26e-119">The parser calls whatever format function is specified by the **InstanceData** member of the **PROPERTYINFO** structure for the property.</span></span>

 

<span data-ttu-id="8f26e-120">Para obtener más información y un ejemplo de cómo implementar [formatproperties](formatproperties.md), vea [implementar formatproperties](implementing-formatproperties.md).</span><span class="sxs-lookup"><span data-stu-id="8f26e-120">For more information and an example of how to implement [formatproperties](formatproperties.md), see [Implementing FormatProperties](implementing-formatproperties.md).</span></span> <span data-ttu-id="8f26e-121">Para obtener más información sobre cómo el formateador genérico da formato a distintos tipos de datos, vea la [salida del formateador genérico](generic-formatter-output.md).</span><span class="sxs-lookup"><span data-stu-id="8f26e-121">For more information about how the generic formatter formats different types of data, see [Generic Formatter Output](generic-formatter-output.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8f26e-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f26e-122">Requirements</span></span>



| <span data-ttu-id="8f26e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f26e-123">Requirement</span></span> | <span data-ttu-id="8f26e-124">Value</span><span class="sxs-lookup"><span data-stu-id="8f26e-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8f26e-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f26e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8f26e-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8f26e-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="8f26e-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f26e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8f26e-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8f26e-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8f26e-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8f26e-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f26e-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f26e-130"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="8f26e-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8f26e-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="8f26e-132"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8f26e-132"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="8f26e-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8f26e-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f26e-134"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f26e-134"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f26e-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="8f26e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f26e-136">PROPERTYINFO</span><span class="sxs-lookup"><span data-stu-id="8f26e-136">PROPERTYINFO</span></span>](propertyinfo.md)
</dt> <dt>

[<span data-ttu-id="8f26e-137">PROPERTYINST</span><span class="sxs-lookup"><span data-stu-id="8f26e-137">PROPERTYINST</span></span>](propertyinst.md)
</dt> </dl>

 

 




