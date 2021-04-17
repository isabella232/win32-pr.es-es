---
description: El evento OnProgress de SWbemSink se desencadena cuando una llamada asincrónica devuelve el estado de una llamada en curso.
ms.assetid: abb43916-f952-41fe-a5ba-0428864c0685
ms.tgt_platform: multiple
title: 'Evento ISWbemSinkEvents:: OnProgress (Wbemdisp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnProgress
- ISWbemSinkEvents.OnProgress
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 0d322309adcfad33b1c303d7efd6af28db1cac80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717124"
---
# <a name="iswbemsinkeventsonprogress-event"></a><span data-ttu-id="7d59c-103">ISWbemSinkEvents:: OnProgress (evento)</span><span class="sxs-lookup"><span data-stu-id="7d59c-103">ISWbemSinkEvents::OnProgress event</span></span>

<span data-ttu-id="7d59c-104">El evento **OnProgress** de [**SWbemSink**](swbemsink.md) se desencadena cuando una llamada asincrónica devuelve el estado de una llamada en curso.</span><span class="sxs-lookup"><span data-stu-id="7d59c-104">The **OnProgress** event of [**SWbemSink**](swbemsink.md) is triggered when an asynchronous call returns the status of a call that is in progress.</span></span> <span data-ttu-id="7d59c-105">Si los eventos, instancias o clases se generan a partir de un proveedor que admite actualizaciones de estado, puede colocar código en este evento para proporcionar a los usuarios comentarios sobre el estado de una operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="7d59c-105">If the events, instances, or classes are produced from a provider that supports status updates, you can place code in this event to provide users with feedback about the status of an asynchronous operation.</span></span> <span data-ttu-id="7d59c-106">Debe establecer el parámetro *iFlags* de la llamada asincrónica a **wbemFlagSendStatus** (128/0x80) Si desea recibir actualizaciones de estado, de lo contrario, este evento no se desencadena.</span><span class="sxs-lookup"><span data-stu-id="7d59c-106">You must set the *iFlags* parameter of the asynchronous call to **wbemFlagSendStatus** (128/0x80) if you want to receive status updates, otherwise this event is not triggered.</span></span>

<span data-ttu-id="7d59c-107">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="7d59c-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7d59c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7d59c-108">Syntax</span></span>


```VB
SWbemSink.OnProgress( _
  ByVal iUpperBound, _
  ByVal iCurrent, _
  ByVal strMessage, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a><span data-ttu-id="7d59c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7d59c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d59c-110">*iUpperBound*</span><span class="sxs-lookup"><span data-stu-id="7d59c-110">*iUpperBound*</span></span> 
</dt> <dd>

<span data-ttu-id="7d59c-111">Entero que describe el número total de tareas que se van a completar.</span><span class="sxs-lookup"><span data-stu-id="7d59c-111">Integer that describes the total number of tasks to complete.</span></span>

</dd> <dt>

<span data-ttu-id="7d59c-112">*iCurrent*</span><span class="sxs-lookup"><span data-stu-id="7d59c-112">*iCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="7d59c-113">Elemento actual que se está procesando.</span><span class="sxs-lookup"><span data-stu-id="7d59c-113">Current item that is being processed.</span></span>

</dd> <dt>

<span data-ttu-id="7d59c-114">*strMessage*</span><span class="sxs-lookup"><span data-stu-id="7d59c-114">*strMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="7d59c-115">Mensaje que describe el estado de la tarea actual.</span><span class="sxs-lookup"><span data-stu-id="7d59c-115">Message that describes the status of the current task.</span></span>

</dd> <dt>

<span data-ttu-id="7d59c-116">*objWbemAsyncContext*</span><span class="sxs-lookup"><span data-stu-id="7d59c-116">*objWbemAsyncContext*</span></span> 
</dt> <dd>

<span data-ttu-id="7d59c-117">Un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que se pasa a la llamada asincrónica original.</span><span class="sxs-lookup"><span data-stu-id="7d59c-117">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that is passed to the original asynchronous call.</span></span> <span data-ttu-id="7d59c-118">Use este parámetro para identificar el origen de la llamada asincrónica que desencadena este evento cuando se realizan varias llamadas asincrónicas con este receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="7d59c-118">Use this parameter to identify the origin of the asynchronous call that triggers this event when multiple asynchronous calls are made using this object sink.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d59c-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7d59c-119">Return value</span></span>

<span data-ttu-id="7d59c-120">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="7d59c-120">This event does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7d59c-121">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="7d59c-121">Error codes</span></span>

<span data-ttu-id="7d59c-122">Después de completar el evento **OnProgress** , el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener uno de los códigos de error siguientes.</span><span class="sxs-lookup"><span data-stu-id="7d59c-122">After the completion of the **OnProgress** event, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="7d59c-123">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="7d59c-123">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="7d59c-124">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="7d59c-124">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="7d59c-125">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="7d59c-125">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="7d59c-126">Memoria insuficiente para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="7d59c-126">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="7d59c-127">**wbemErrTransportFailure** -2147749909 (0x80041015)</span><span class="sxs-lookup"><span data-stu-id="7d59c-127">**wbemErrTransportFailure** - 2147749909 (0x80041015)</span></span>
</dt> <dd>

<span data-ttu-id="7d59c-128">Se produjo un error de red, evitando el funcionamiento normal.</span><span class="sxs-lookup"><span data-stu-id="7d59c-128">Networking error occurred, preventing normal operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7d59c-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7d59c-129">Remarks</span></span>

<span data-ttu-id="7d59c-130">El evento **OnProgress** se desencadena cuando una llamada asincrónica devuelve el estado de una llamada en curso.</span><span class="sxs-lookup"><span data-stu-id="7d59c-130">The **OnProgress** event is triggered when an asynchronous call returns the status of a call that is in progress.</span></span> <span data-ttu-id="7d59c-131">Si los eventos, instancias o clases se generan a partir de un proveedor que admite actualizaciones de estado, puede colocar código en este evento para proporcionar a los usuarios comentarios sobre el estado de una operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="7d59c-131">If the events, instances, or classes are produced from a provider that supports status updates, you can place code in this event to give users feedback about the status of an asynchronous operation.</span></span>

> [!Note]  
> <span data-ttu-id="7d59c-132">Una devolución de llamada asincrónica permite que un usuario no autenticado proporcione datos al receptor.</span><span class="sxs-lookup"><span data-stu-id="7d59c-132">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="7d59c-133">Esto supone riesgos de seguridad para los scripts y las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="7d59c-133">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="7d59c-134">Para eliminar los riesgos, utilice la comunicación sincrónica o semisincrónica.</span><span class="sxs-lookup"><span data-stu-id="7d59c-134">To eliminate the risks, use semi-synchronous or synchronous communication.</span></span> <span data-ttu-id="7d59c-135">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="7d59c-135">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7d59c-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d59c-136">Requirements</span></span>



| <span data-ttu-id="7d59c-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d59c-137">Requirement</span></span> | <span data-ttu-id="7d59c-138">Value</span><span class="sxs-lookup"><span data-stu-id="7d59c-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d59c-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7d59c-139">Minimum supported client</span></span><br/> | <span data-ttu-id="7d59c-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7d59c-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7d59c-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7d59c-141">Minimum supported server</span></span><br/> | <span data-ttu-id="7d59c-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7d59c-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7d59c-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7d59c-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d59c-144"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d59c-144"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7d59c-145">IDL</span><span class="sxs-lookup"><span data-stu-id="7d59c-145">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7d59c-146"><dt>Wbemdisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7d59c-146"><dt>Wbemdisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="7d59c-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7d59c-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d59c-148"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d59c-148"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7d59c-149">CLSID</span><span class="sxs-lookup"><span data-stu-id="7d59c-149">CLSID</span></span><br/>                    | <span data-ttu-id="7d59c-150">CLSID \_ SWbemSink</span><span class="sxs-lookup"><span data-stu-id="7d59c-150">CLSID\_SWbemSink</span></span><br/>                                                             |
| <span data-ttu-id="7d59c-151">IID</span><span class="sxs-lookup"><span data-stu-id="7d59c-151">IID</span></span><br/>                      | <span data-ttu-id="7d59c-152">\_ISWBEMSINKEVENTS IID</span><span class="sxs-lookup"><span data-stu-id="7d59c-152">IID\_ISWbemSinkEvents</span></span><br/>                                                        |



## <a name="see-also"></a><span data-ttu-id="7d59c-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="7d59c-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d59c-154">**SWbemSink**</span><span class="sxs-lookup"><span data-stu-id="7d59c-154">**SWbemSink**</span></span>](swbemsink.md)
</dt> </dl>

 

