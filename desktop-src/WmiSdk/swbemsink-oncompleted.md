---
description: El evento alcompleto de un objeto SWbemSink se desencadena cuando se completa una llamada asincrónica. Este evento indica a la aplicación cliente, el resultado de una operación asincrónica y proporciona información de error cuando se produce un error en la llamada asincrónica.
ms.assetid: 2723185d-5b8b-4cc7-ada3-51c3275272a9
ms.tgt_platform: multiple
title: 'Evento ISWbemSinkEvents:: alcompleted (Wbemdisp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnCompleted
- ISWbemSinkEvents.OnCompleted
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 16cb0362b5c1b1d432d72bb959103adbb7315069
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155812"
---
# <a name="iswbemsinkeventsoncompleted-event"></a><span data-ttu-id="df9b8-104">Evento ISWbemSinkEvents:: alcompleted</span><span class="sxs-lookup"><span data-stu-id="df9b8-104">ISWbemSinkEvents::OnCompleted event</span></span>

<span data-ttu-id="df9b8-105">El evento **alcompleto** de un objeto [**SWbemSink**](swbemsink.md) se desencadena cuando se completa una llamada asincrónica.</span><span class="sxs-lookup"><span data-stu-id="df9b8-105">The **OnCompleted** event of an [**SWbemSink**](swbemsink.md) object is triggered when an asynchronous call is complete.</span></span> <span data-ttu-id="df9b8-106">Este evento indica a la aplicación cliente, el resultado de una operación asincrónica y proporciona información de error cuando se produce un error en la llamada asincrónica.</span><span class="sxs-lookup"><span data-stu-id="df9b8-106">This event indicates to the client application, the result of an asynchronous operation, and provides error information when the asynchronous call fails.</span></span>

<span data-ttu-id="df9b8-107">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="df9b8-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="df9b8-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="df9b8-108">Syntax</span></span>


```VB
SWbemSink.OnCompleted( _
  ByVal iHResult, _
  ByVal objWbemErrorObject, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a><span data-ttu-id="df9b8-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="df9b8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df9b8-110">*iHResult*</span><span class="sxs-lookup"><span data-stu-id="df9b8-110">*iHResult*</span></span> 
</dt> <dd>

<span data-ttu-id="df9b8-111">HRESULT del método asincrónico completado.</span><span class="sxs-lookup"><span data-stu-id="df9b8-111">The HRESULT of the completed asynchronous method.</span></span> <span data-ttu-id="df9b8-112">HRESULT es el mismo que el valor devuelto de una [API com equivalente para](com-api-for-wmi.md) la llamada al método WMI.</span><span class="sxs-lookup"><span data-stu-id="df9b8-112">The HRESULT is the same as the value that is returned from an equivalent [COM API for WMI](com-api-for-wmi.md) method call.</span></span> <span data-ttu-id="df9b8-113">Compruebe este valor para determinar si la llamada asincrónica se realiza correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="df9b8-113">Check this value to determine whether or not the asynchronous call is successful.</span></span> <span data-ttu-id="df9b8-114">Si la llamada asincrónica se realiza correctamente, este parámetro contiene WBEM \_ S \_ no \_ error (0).</span><span class="sxs-lookup"><span data-stu-id="df9b8-114">If the asynchronous call is successful, this parameter contains WBEM\_S\_NO\_ERROR (0).</span></span> <span data-ttu-id="df9b8-115">Si se produce un error en la llamada asincrónica, este parámetro contiene un código de error.</span><span class="sxs-lookup"><span data-stu-id="df9b8-115">If the asynchronous call fails, this parameter contains an error code.</span></span>

</dd> <dt>

<span data-ttu-id="df9b8-116">*objWbemErrorObject*</span><span class="sxs-lookup"><span data-stu-id="df9b8-116">*objWbemErrorObject*</span></span> 
</dt> <dd>

<span data-ttu-id="df9b8-117">Contiene un objeto [**SWbemLastError**](swbemlasterror.md) cuando se produce un error en el método asincrónico.</span><span class="sxs-lookup"><span data-stu-id="df9b8-117">Contains an [**SWbemLastError**](swbemlasterror.md) object when the asynchronous method fails.</span></span>

</dd> <dt>

<span data-ttu-id="df9b8-118">*objWbemAsyncContext*</span><span class="sxs-lookup"><span data-stu-id="df9b8-118">*objWbemAsyncContext*</span></span> 
</dt> <dd>

<span data-ttu-id="df9b8-119">Se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que se pasa a la llamada asincrónica original.</span><span class="sxs-lookup"><span data-stu-id="df9b8-119">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that is passed to the original asynchronous call.</span></span> <span data-ttu-id="df9b8-120">Use este parámetro para identificar el origen de la llamada asincrónica que desencadena este evento cuando se realizan varias llamadas asincrónicas con este receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="df9b8-120">Use this parameter to identify the origin of the asynchronous call that triggers this event when multiple asynchronous calls are made using this object sink.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df9b8-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="df9b8-121">Return value</span></span>

<span data-ttu-id="df9b8-122">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="df9b8-122">This event does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="df9b8-123">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="df9b8-123">Error codes</span></span>

<span data-ttu-id="df9b8-124">Después de completar el evento **Alcompleted** , el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener uno de los códigos de error siguientes.</span><span class="sxs-lookup"><span data-stu-id="df9b8-124">After completion of the **OnCompleted** event, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="df9b8-125">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="df9b8-125">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="df9b8-126">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="df9b8-126">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="df9b8-127">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="df9b8-127">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="df9b8-128">Memoria insuficiente para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="df9b8-128">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="df9b8-129">**wbemErrTransportFailure** -2147749909 (0x80041015)</span><span class="sxs-lookup"><span data-stu-id="df9b8-129">**wbemErrTransportFailure** - 2147749909 (0x80041015)</span></span>
</dt> <dd>

<span data-ttu-id="df9b8-130">Se produjo un error de red, evitando el funcionamiento normal.</span><span class="sxs-lookup"><span data-stu-id="df9b8-130">Networking error occurred, preventing normal operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="df9b8-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="df9b8-131">Remarks</span></span>

<span data-ttu-id="df9b8-132">Una devolución de llamada asincrónica permite que un usuario no autenticado proporcione datos al receptor.</span><span class="sxs-lookup"><span data-stu-id="df9b8-132">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="df9b8-133">Esto supone riesgos de seguridad para los scripts y las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="df9b8-133">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="df9b8-134">Para eliminar los riesgos, utilice la comunicación sincrónica o semisincrónica.</span><span class="sxs-lookup"><span data-stu-id="df9b8-134">To eliminate the risks, use semisynchronous or synchronous communication.</span></span> <span data-ttu-id="df9b8-135">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="df9b8-135">For more information, see [Calling a Method](calling-a-method.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="df9b8-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df9b8-136">Requirements</span></span>



| <span data-ttu-id="df9b8-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="df9b8-137">Requirement</span></span> | <span data-ttu-id="df9b8-138">Value</span><span class="sxs-lookup"><span data-stu-id="df9b8-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="df9b8-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="df9b8-139">Minimum supported client</span></span><br/> | <span data-ttu-id="df9b8-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="df9b8-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="df9b8-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="df9b8-141">Minimum supported server</span></span><br/> | <span data-ttu-id="df9b8-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="df9b8-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="df9b8-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="df9b8-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="df9b8-144"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="df9b8-144"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="df9b8-145">IDL</span><span class="sxs-lookup"><span data-stu-id="df9b8-145">IDL</span></span><br/>                      | <dl> <span data-ttu-id="df9b8-146"><dt>Wbemdisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="df9b8-146"><dt>Wbemdisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="df9b8-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="df9b8-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df9b8-148"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df9b8-148"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="df9b8-149">CLSID</span><span class="sxs-lookup"><span data-stu-id="df9b8-149">CLSID</span></span><br/>                    | <span data-ttu-id="df9b8-150">CLSID \_ SWbemSink</span><span class="sxs-lookup"><span data-stu-id="df9b8-150">CLSID\_SWbemSink</span></span><br/>                                                             |
| <span data-ttu-id="df9b8-151">IID</span><span class="sxs-lookup"><span data-stu-id="df9b8-151">IID</span></span><br/>                      | <span data-ttu-id="df9b8-152">\_ISWBEMSINKEVENTS IID</span><span class="sxs-lookup"><span data-stu-id="df9b8-152">IID\_ISWbemSinkEvents</span></span><br/>                                                        |



 

