---
description: La función de exportación FormatProperties da formato a los datos que se muestran en el panel de detalles de la interfaz de usuario de Monitor de red. Si desea mostrar los datos en el panel de detalles, debe implementar la función de exportación FormatProperties en todos los archivos dll de analizador.
ms.assetid: 78e0b4b9-f19e-41cb-8504-635f3f9ac1ee
title: Función de devolución de llamada FormatProperties (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FormatProperties
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 61707b49fa88490e1aa22ac89f33dfd97ec20cbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666287"
---
# <a name="formatproperties-callback-function"></a><span data-ttu-id="66d80-104">Función de devolución de llamada FormatProperties</span><span class="sxs-lookup"><span data-stu-id="66d80-104">FormatProperties callback function</span></span>

<span data-ttu-id="66d80-105">La función de exportación **FormatProperties** da formato a los datos que se muestran en el panel de detalles de la interfaz de usuario de monitor de red.</span><span class="sxs-lookup"><span data-stu-id="66d80-105">The **FormatProperties** export function formats the data that is displayed in the details pane of the Network Monitor UI.</span></span> <span data-ttu-id="66d80-106">Si desea mostrar los datos en el panel de detalles, debe implementar la función de exportación **FormatProperties** en todos los archivos dll de analizador.</span><span class="sxs-lookup"><span data-stu-id="66d80-106">If you want to display data in the details pane, you must implement the **FormatProperties** export function in all parser DLLs.</span></span>

## <a name="syntax"></a><span data-ttu-id="66d80-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="66d80-107">Syntax</span></span>


```C++
DWORD FormatProperties(
  _In_ HFRAME         hFrame,
  _In_ LPBYTE         lpFrame,
  _In_ LPBYTE         lpProtocol,
  _In_ DWORD          nPropertyInsts,
  _In_ LPPROPERTYINST lpPropInst
);
```



## <a name="parameters"></a><span data-ttu-id="66d80-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="66d80-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66d80-109">*hFrame* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="66d80-109">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66d80-110">Identificador del marco que se está analizando.</span><span class="sxs-lookup"><span data-stu-id="66d80-110">Handle to the frame that is being parsed.</span></span>

</dd> <dt>

<span data-ttu-id="66d80-111">*lpFrame* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="66d80-111">*lpFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66d80-112">Puntero al primer byte de un marco.</span><span class="sxs-lookup"><span data-stu-id="66d80-112">Pointer to the first byte of a frame.</span></span>

</dd> <dt>

<span data-ttu-id="66d80-113">*lpProtocol* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="66d80-113">*lpProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66d80-114">Puntero al principio de los datos de protocolo en un marco.</span><span class="sxs-lookup"><span data-stu-id="66d80-114">Pointer to the beginning of the protocol data in a frame.</span></span>

</dd> <dt>

<span data-ttu-id="66d80-115">*nPropertyInsts* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="66d80-115">*nPropertyInsts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66d80-116">Número de estructuras [PROPERTYINST](propertyinst.md) proporcionadas por *lpPropInst*.</span><span class="sxs-lookup"><span data-stu-id="66d80-116">Number of [PROPERTYINST](propertyinst.md) structures provided by *lpPropInst*.</span></span>

</dd> <dt>

<span data-ttu-id="66d80-117">*lpPropInst* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="66d80-117">*lpPropInst* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66d80-118">Puntero a una matriz de estructuras [PROPERTYINST](propertyinst.md) .</span><span class="sxs-lookup"><span data-stu-id="66d80-118">Pointer to an array of [PROPERTYINST](propertyinst.md) structures.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66d80-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="66d80-119">Return value</span></span>

<span data-ttu-id="66d80-120">Si la función se realiza correctamente, el valor devuelto es **true**.</span><span class="sxs-lookup"><span data-stu-id="66d80-120">If the function is successful, the return value is **TRUE**.</span></span>

<span data-ttu-id="66d80-121">Si la función no se realiza correctamente, el valor devuelto es **false**.</span><span class="sxs-lookup"><span data-stu-id="66d80-121">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="66d80-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="66d80-122">Remarks</span></span>

<span data-ttu-id="66d80-123">Monitor de red llama a la función **FormatProperties** para mostrar los datos en el panel de detalles de la interfaz de usuario de monitor de red.</span><span class="sxs-lookup"><span data-stu-id="66d80-123">Network Monitor calls the **FormatProperties** function to display data in the details pane of the Network Monitor UI.</span></span> <span data-ttu-id="66d80-124">Normalmente, se llama a **FormatProperties** para dar formato a la línea de Resumen de un protocolo y, a continuación, para dar formato a todas las instancias de propiedad del protocolo dentro de un marco.</span><span class="sxs-lookup"><span data-stu-id="66d80-124">Typically, **FormatProperties** is called to format the summary line for a protocol, and then to format all the property instances of the protocol within a frame.</span></span> <span data-ttu-id="66d80-125">Sin embargo, Monitor de red no garantiza el número de veces que llama a **FormatProperties** para un analizador específico.</span><span class="sxs-lookup"><span data-stu-id="66d80-125">However, Network Monitor does not guarantee the number of times it calls **FormatProperties** for a specific parser.</span></span>

<span data-ttu-id="66d80-126">Durante la implementación de la función **FormatProperties** , el analizador llama indirectamente a la función [FormatPropertyInstance](formatpropertyinstance.md) para usar el formateador genérico que proporciona monitor de red, o puede llamar a un procedimiento de formateador personalizado definido por el analizador.</span><span class="sxs-lookup"><span data-stu-id="66d80-126">During the implementation of the **FormatProperties** function, the parser indirectly calls the [FormatPropertyInstance](formatpropertyinstance.md) function to use the generic formatter that Network Monitor provides, or it can call a custom formatter procedure that is defined by the parser.</span></span> <span data-ttu-id="66d80-127">Se debe llamar a uno de los formateadores para cada estructura [PROPERTYINST](propertyinst.md) pasada a la dll del analizador en el parámetro *lpPropInst* .</span><span class="sxs-lookup"><span data-stu-id="66d80-127">One of the formatters must be called for each [PROPERTYINST](propertyinst.md) structure passed to the parser DLL in the *lpPropInst* parameter.</span></span>



| <span data-ttu-id="66d80-128">Para obtener información sobre</span><span class="sxs-lookup"><span data-stu-id="66d80-128">For Information on</span></span>                                          | <span data-ttu-id="66d80-129">Vea</span><span class="sxs-lookup"><span data-stu-id="66d80-129">See</span></span>                                                                |
|-------------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="66d80-130">Qué son los analizadores y cómo funcionan con Monitor de red.</span><span class="sxs-lookup"><span data-stu-id="66d80-130">What parsers are, and how they work with Network Monitor.</span></span>   | [<span data-ttu-id="66d80-131">Analizadores</span><span class="sxs-lookup"><span data-stu-id="66d80-131">Parsers</span></span>](parsers.md)                                             |
| <span data-ttu-id="66d80-132">Qué puntos de entrada se incluyen en el archivo DLL del analizador.</span><span class="sxs-lookup"><span data-stu-id="66d80-132">Which entry points are included in the parser DLL.</span></span>          | [<span data-ttu-id="66d80-133">Arquitectura de DLL de analizador</span><span class="sxs-lookup"><span data-stu-id="66d80-133">Parser DLL Architecture</span></span>](parser-dll-architecture.md)             |
| <span data-ttu-id="66d80-134">Cómo implementar **FormatProperties**  incluye un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="66d80-134">How to implement **FormatProperties**  includes an example.</span></span> | [<span data-ttu-id="66d80-135">Implementación de FormatProperties</span><span class="sxs-lookup"><span data-stu-id="66d80-135">Implementing FormatProperties</span></span>](implementing-formatproperties.md) |
| <span data-ttu-id="66d80-136">Cómo el formateador genérico da formato a distintos tipos de datos.</span><span class="sxs-lookup"><span data-stu-id="66d80-136">How the generic formatter formats different types of data.</span></span>  | [<span data-ttu-id="66d80-137">Salida del formateador genérico</span><span class="sxs-lookup"><span data-stu-id="66d80-137">Generic Formatter Output</span></span>](generic-formatter-output.md)           |



 

## <a name="requirements"></a><span data-ttu-id="66d80-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66d80-138">Requirements</span></span>



| <span data-ttu-id="66d80-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="66d80-139">Requirement</span></span> | <span data-ttu-id="66d80-140">Value</span><span class="sxs-lookup"><span data-stu-id="66d80-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="66d80-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66d80-141">Minimum supported client</span></span><br/> | <span data-ttu-id="66d80-142">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="66d80-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="66d80-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66d80-143">Minimum supported server</span></span><br/> | <span data-ttu-id="66d80-144">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="66d80-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="66d80-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="66d80-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="66d80-146"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="66d80-146"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66d80-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="66d80-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66d80-148">FormatPropertyInstance</span><span class="sxs-lookup"><span data-stu-id="66d80-148">FormatPropertyInstance</span></span>](formatpropertyinstance.md)
</dt> <dt>

[<span data-ttu-id="66d80-149">PROPERTYINFO</span><span class="sxs-lookup"><span data-stu-id="66d80-149">PROPERTYINFO</span></span>](propertyinfo.md)
</dt> <dt>

[<span data-ttu-id="66d80-150">PROPERTYINST</span><span class="sxs-lookup"><span data-stu-id="66d80-150">PROPERTYINST</span></span>](propertyinst.md)
</dt> </dl>

 

 




