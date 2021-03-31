---
description: Devuelve el marco solicitado desde una captura cargada.
ms.assetid: efd1cff5-a3a1-4910-b003-25b6e10dad6e
title: Función ExpertGetFrame (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertGetFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2bd02bde8caf157b6df6b1dd772a8f7574df0e57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907676"
---
# <a name="expertgetframe-function"></a><span data-ttu-id="e3352-103">ExpertGetFrame función)</span><span class="sxs-lookup"><span data-stu-id="e3352-103">ExpertGetFrame function</span></span>

<span data-ttu-id="e3352-104">La función **ExpertGetFrame** devuelve el fotograma solicitado desde una captura cargada.</span><span class="sxs-lookup"><span data-stu-id="e3352-104">The **ExpertGetFrame** function returns the requested frame from a loaded capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3352-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e3352-105">Syntax</span></span>


```C++
DWORD WINAPI ExpertGetFrame(
  _In_  HEXPERTKEY              hExpertKey,
  _In_  DWORD                   Direction,
  _In_  DWORD                   RequestFlags,
  _In_  DWORD                   RequestedFrameNumber,
  _In_  HFILTER                 hFilter,
  _Out_ LPEXPERTFRAMEDESCRIPTOR pEFrameDescriptor
);
```



## <a name="parameters"></a><span data-ttu-id="e3352-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e3352-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3352-107">*hExpertKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e3352-107">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3352-108">Identificador de experto único.</span><span class="sxs-lookup"><span data-stu-id="e3352-108">A unique expert identifier.</span></span> <span data-ttu-id="e3352-109">Monitor de red pasa el identificador *hExpertKey* al experto cuando llama a la función [**Run**](run.md) .</span><span class="sxs-lookup"><span data-stu-id="e3352-109">Network Monitor passes the *hExpertKey* identifier to the expert when it calls the [**Run**](run.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="e3352-110">*Dirección* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e3352-110">*Direction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3352-111">Valor que identifica cómo Monitor de red busca el marco.</span><span class="sxs-lookup"><span data-stu-id="e3352-111">A value that identifies how Network Monitor searches for the frame.</span></span>



| <span data-ttu-id="e3352-112">Value</span><span class="sxs-lookup"><span data-stu-id="e3352-112">Value</span></span>                                                                                                                                                                                         | <span data-ttu-id="e3352-113">Significado</span><span class="sxs-lookup"><span data-stu-id="e3352-113">Meaning</span></span>                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="GET_SPECIFIED_FRAME"></span><span id="get_specified_frame"></span><dl> <span data-ttu-id="e3352-114"><dt>**OBTENER \_ el \_ marco especificado**</dt></span><span class="sxs-lookup"><span data-stu-id="e3352-114"><dt>**GET\_SPECIFIED\_FRAME**</dt></span></span> </dl>              | <span data-ttu-id="e3352-115">Devuelve el marco solicitado.</span><span class="sxs-lookup"><span data-stu-id="e3352-115">Return the requested frame.</span></span><br/> |
| <span id="GET_FRAME_NEXT_FORWARD"></span><span id="get_frame_next_forward"></span><dl> <span data-ttu-id="e3352-116"><dt>**OBTENER \_ fotograma \_ siguiente \_ hacia delante**</dt></span><span class="sxs-lookup"><span data-stu-id="e3352-116"><dt>**GET\_FRAME\_NEXT\_FORWARD**</dt></span></span> </dl>    | <span data-ttu-id="e3352-117">Devolver el siguiente fotograma.</span><span class="sxs-lookup"><span data-stu-id="e3352-117">Return the next frame.</span></span><br/>      |
| <span id="GET_FRAME_NEXT_BACKWARD"></span><span id="get_frame_next_backward"></span><dl> <span data-ttu-id="e3352-118"><dt>**OBTENER \_ fotograma \_ siguiente \_ hacia atrás**</dt></span><span class="sxs-lookup"><span data-stu-id="e3352-118"><dt>**GET\_FRAME\_NEXT\_BACKWARD**</dt></span></span> </dl> | <span data-ttu-id="e3352-119">Devuelve el fotograma anterior.</span><span class="sxs-lookup"><span data-stu-id="e3352-119">Return the previous frame.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="e3352-120">*RequestFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e3352-120">*RequestFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3352-121">Marcas que especifican cómo debe administrar Monitor de red la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e3352-121">The flags that specify how Network Monitor should handle the request.</span></span> <span data-ttu-id="e3352-122">Especifique una o varias de las marcas siguientes.</span><span class="sxs-lookup"><span data-stu-id="e3352-122">Specify one or more of the following flags.</span></span>



| <span data-ttu-id="e3352-123">Value</span><span class="sxs-lookup"><span data-stu-id="e3352-123">Value</span></span>                                                                                                                                                                                             | <span data-ttu-id="e3352-124">Significado</span><span class="sxs-lookup"><span data-stu-id="e3352-124">Meaning</span></span>                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLAGS_DEFER_TO_UI_FILTER"></span><span id="flags_defer_to_ui_filter"></span><dl> <span data-ttu-id="e3352-125"><dt>**MARCAS \_ \_ de aplazamiento \_ a \_ filtro de interfaz de usuario**</dt></span><span class="sxs-lookup"><span data-stu-id="e3352-125"><dt>**FLAGS\_DEFER\_TO\_UI\_FILTER**</dt></span></span> </dl> | <span data-ttu-id="e3352-126">Antes de aplicar el parámetro de filtro para mostrar del experto que se especifica en *hFilter*, aplique el filtro de visualización que monitor de red esté usando cuando se inicie el experto.</span><span class="sxs-lookup"><span data-stu-id="e3352-126">Before applying the display filter parameter of the expert which is specified in *hFilter*, apply the display filter that Network Monitor is using when the expert starts.</span></span><br/>                                                                                                                              |
| <span id="FLAGS_ATTACH_PROPERTIES"></span><span id="flags_attach_properties"></span><dl> <span data-ttu-id="e3352-127"><dt>**\_propiedades de adjuntar marcas \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e3352-127"><dt>**FLAGS\_ATTACH\_PROPERTIES**</dt></span></span> </dl>      | <span data-ttu-id="e3352-128">Las propiedades que todos los analizadores de protocolos encuentran con las secciones reclamadas de este marco se adjuntan al marco.</span><span class="sxs-lookup"><span data-stu-id="e3352-128">The properties that all protocol parsers find with claimed sections of this frame are attached to the frame.</span></span> <span data-ttu-id="e3352-129">Si no se establece la marca, el campo **lpPropertyTable** de la estructura [**EXPERTFRAMEDESCRIPTOR**](expertframedescriptor.md) (devuelto por **pEFrameDescriptor**) se establecerá en **null**.</span><span class="sxs-lookup"><span data-stu-id="e3352-129">If the flag is not set, the **lpPropertyTable** field of the [**EXPERTFRAMEDESCRIPTOR**](expertframedescriptor.md) structure (returned by **pEFrameDescriptor**) will be set to **NULL**.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e3352-130">*RequestedFrameNumber* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e3352-130">*RequestedFrameNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3352-131">Número de la trama solicitada.</span><span class="sxs-lookup"><span data-stu-id="e3352-131">The number of the requested frame.</span></span>

</dd> <dt>

<span data-ttu-id="e3352-132">*hFilter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e3352-132">*hFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3352-133">Identificador del filtro de visualización del experto.</span><span class="sxs-lookup"><span data-stu-id="e3352-133">A handle to the expert display filter.</span></span> <span data-ttu-id="e3352-134">Si el experto no tiene un filtro de visualización, establezca el parámetro en **null**.</span><span class="sxs-lookup"><span data-stu-id="e3352-134">If the expert does not have a display filter, set the parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e3352-135">*pEFrameDescriptor* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e3352-135">*pEFrameDescriptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3352-136">La estructura [**EXPERTFRAMEDESCRIPTOR**](expertframedescriptor.md) que, en la devolución, describe el marco.</span><span class="sxs-lookup"><span data-stu-id="e3352-136">The [**EXPERTFRAMEDESCRIPTOR**](expertframedescriptor.md) structure that, on return, describes the frame.</span></span> <span data-ttu-id="e3352-137">El experto debe asignar y liberar la memoria que usa esta estructura.</span><span class="sxs-lookup"><span data-stu-id="e3352-137">The expert must allocate and free the memory that this structure uses.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3352-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e3352-138">Return value</span></span>

<span data-ttu-id="e3352-139">Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="e3352-139">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="e3352-140">Si la función no se realiza correctamente, el valor devuelto indica la razón del error.</span><span class="sxs-lookup"><span data-stu-id="e3352-140">If the function is unsuccessful, the return value indicates the reason for the failure.</span></span> <span data-ttu-id="e3352-141">Si el valor devuelto es NMERR \_ Expert \_ Terminate, el experto debe limpiarse y devolverse inmediatamente; el usuario ha anulado la ejecución del experto.</span><span class="sxs-lookup"><span data-stu-id="e3352-141">If the return value is NMERR\_EXPERT\_TERMINATE, the expert must immediately clean up and return; the user has aborted the expert run.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3352-142">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e3352-142">Remarks</span></span>

<span data-ttu-id="e3352-143">Si establece \_ las propiedades de adjuntar marcas \_ , la llamada requiere más recursos que si no se establece la marca.</span><span class="sxs-lookup"><span data-stu-id="e3352-143">If you set FLAGS\_ATTACH\_PROPERTIES, the call requires more resources than if you do not set the flag.</span></span> <span data-ttu-id="e3352-144">Si no se establece la marca, un puntero apunta al fotograma sin formato y a los datos sobre el marco.</span><span class="sxs-lookup"><span data-stu-id="e3352-144">If the flag is not set, a pointer points to the raw frame and to data about the frame.</span></span> <span data-ttu-id="e3352-145">Si se establece esta marca, Monitor de red asocia todas las propiedades al marco llamando a cada analizador que notifica una parte del marco.</span><span class="sxs-lookup"><span data-stu-id="e3352-145">If this flag is set, Network Monitor attaches all properties to the frame by calling every parser that claims a portion of the frame.</span></span> <span data-ttu-id="e3352-146">Esto puede ser un proceso lento.</span><span class="sxs-lookup"><span data-stu-id="e3352-146">This can be a slow process.</span></span>

<span data-ttu-id="e3352-147">Los expertos no deben establecer la \_ marca propiedades de adjuntar marcas a \_ menos que los expertos requieran las propiedades que los analizadores adjuntan al marco.</span><span class="sxs-lookup"><span data-stu-id="e3352-147">Experts should not set the FLAGS\_ATTACH\_PROPERTIES flag unless the experts require the properties that parsers attach to the frame.</span></span> <span data-ttu-id="e3352-148">Si es posible, los expertos deben llamar a la función **ExpertGetFrame** sin la marca y, a continuación, extraer los datos necesarios directamente del marco.</span><span class="sxs-lookup"><span data-stu-id="e3352-148">If possible, experts should call the **ExpertGetFrame** function without the flag, and then extract the required data directly from the frame.</span></span>

<span data-ttu-id="e3352-149">Si el experto llama a **ExpertGetFrame** sin el \_ marcador Flags Attach \_ Properties y requiere las propiedades asociadas a ese marco (un evento, por ejemplo), el experto llama a **ExpertGetFrame** con los mismos parámetros, excepto los siguientes:</span><span class="sxs-lookup"><span data-stu-id="e3352-149">If the expert calls **ExpertGetFrame** without the FLAGS\_ATTACH\_PROPERTIES flag and requires the properties associated with that frame (an event, for example), the expert calls **ExpertGetFrame** with the same parameters except for the following:</span></span>

``` syntax
Direction = EXPERT_GET_SPECIFIED_FRAME;
RequestFlags &= (~EXPERT_DEFER_TO_UI_FILTER) | EXPERT_ATTACH_PROPERTIES;
RequestedFrameNumber= (The actual frame number you want);
hFilter = NULL;
pEFrameDescriptor = (The same one as last time);
```

<span data-ttu-id="e3352-150">El uso del código anterior garantiza que el experto obtiene el marco necesario sin tener que volver a llamar al código de filtro.</span><span class="sxs-lookup"><span data-stu-id="e3352-150">Using the preceding code ensures that the expert gets the required frame without having to call filter code again.</span></span>

<span data-ttu-id="e3352-151">Puede establecer el parámetro *hFilter* como **LPVOID**.</span><span class="sxs-lookup"><span data-stu-id="e3352-151">You can set the *hFilter* parameter as an **LPVOID**.</span></span> <span data-ttu-id="e3352-152">Si existe, el fotograma devuelto pasa este filtro.</span><span class="sxs-lookup"><span data-stu-id="e3352-152">If it exists, the returned frame passes this filter.</span></span> <span data-ttu-id="e3352-153">Si el experto no tiene un filtro de visualización para pasar a la función (si *hFilter* es **null** ), el fotograma devuelto no se filtra.</span><span class="sxs-lookup"><span data-stu-id="e3352-153">If the expert does not have a display filter to pass to the function (if *hFilter* is **NULL** ), then the frame returned is not filtered.</span></span>

<span data-ttu-id="e3352-154">La función **ExpertGetFrame** solo puede ser llamada por expertos que implementan la función de exportación [**Ejecutar**](run.md) o [**configurar**](configure.md) .</span><span class="sxs-lookup"><span data-stu-id="e3352-154">The **ExpertGetFrame** function can only be called by experts that implement the [**Run**](run.md) or [**Configure**](configure.md) export function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3352-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3352-155">Requirements</span></span>



| <span data-ttu-id="e3352-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3352-156">Requirement</span></span> | <span data-ttu-id="e3352-157">Value</span><span class="sxs-lookup"><span data-stu-id="e3352-157">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e3352-158">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3352-158">Minimum supported client</span></span><br/> | <span data-ttu-id="e3352-159">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e3352-159">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="e3352-160">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3352-160">Minimum supported server</span></span><br/> | <span data-ttu-id="e3352-161">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e3352-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e3352-162">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e3352-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3352-163"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3352-163"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="e3352-164">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e3352-164">Library</span></span><br/>                  | <dl> <span data-ttu-id="e3352-165"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e3352-165"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="e3352-166">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e3352-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3352-167"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3352-167"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




