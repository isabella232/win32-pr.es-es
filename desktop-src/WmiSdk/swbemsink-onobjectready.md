---
description: El evento OnObjectReady de un objeto SWbemSink se desencadena cuando una operación asincrónica devuelve un objeto.
ms.assetid: 14110ee7-a808-4786-b695-2ce54189d826
ms.tgt_platform: multiple
title: 'Evento ISWbemSinkEvents:: OnObjectReady (Wbemdisp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnObjectReady
- ISWbemSinkEvents.OnObjectReady
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1fa803339e7007a030881c3d5b47d67f354b5661
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155808"
---
# <a name="iswbemsinkeventsonobjectready-event"></a><span data-ttu-id="5a3aa-103">Evento ISWbemSinkEvents:: OnObjectReady</span><span class="sxs-lookup"><span data-stu-id="5a3aa-103">ISWbemSinkEvents::OnObjectReady event</span></span>

<span data-ttu-id="5a3aa-104">El evento **OnObjectReady** de un objeto [**SWbemSink**](swbemsink.md) se desencadena cuando una operación asincrónica devuelve un objeto.</span><span class="sxs-lookup"><span data-stu-id="5a3aa-104">The **OnObjectReady** event of an [**SWbemSink**](swbemsink.md) object is triggered when an asynchronous operation returns an object.</span></span> <span data-ttu-id="5a3aa-105">Utilice este evento para procesar objetos de llamadas asincrónicas como [**SWbemObject. InstancesAsync \_**](swbemobject-instancesasync-.md) o [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md).</span><span class="sxs-lookup"><span data-stu-id="5a3aa-105">Use this event to process objects from asynchronous calls such as [**SWbemObject.InstancesAsync\_**](swbemobject-instancesasync-.md) or [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md).</span></span> <span data-ttu-id="5a3aa-106">**OnObjectReady** devuelve un [**SWbemObject**](swbemobject.md) cada vez hasta que se completa la enumeración.</span><span class="sxs-lookup"><span data-stu-id="5a3aa-106">**OnObjectReady** returns one [**SWbemObject**](swbemobject.md) each time until the enumeration is complete.</span></span>

<span data-ttu-id="5a3aa-107">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="5a3aa-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5a3aa-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5a3aa-108">Syntax</span></span>


```VB
SWbemSink.OnObjectReady( _
  ByVal objWbemObject, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a><span data-ttu-id="5a3aa-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5a3aa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a3aa-110">*objWbemObject*</span><span class="sxs-lookup"><span data-stu-id="5a3aa-110">*objWbemObject*</span></span> 
</dt> <dd>

<span data-ttu-id="5a3aa-111">Objeto [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="5a3aa-111">An [**SWbemObject**](swbemobject.md) object.</span></span> <span data-ttu-id="5a3aa-112">Esto es similar a lo que devuelve el equivalente sincrónico de la llamada asincrónica que desencadena este evento.</span><span class="sxs-lookup"><span data-stu-id="5a3aa-112">This is similar to what is returned by the synchronous equivalent of the asynchronous call that triggers this event.</span></span> <span data-ttu-id="5a3aa-113">Por ejemplo, una llamada al método [**SWbemServices. GetAsync**](swbemservices-getasync.md) devuelve un **SWbemObject** en el parámetro *objWbemObject* del evento **OnObjectReady** del objeto [**SWbemSink**](swbemsink.md) , que se pasa como parámetro *objWbemObject* de la llamada original.</span><span class="sxs-lookup"><span data-stu-id="5a3aa-113">For example, a call to the [**SWbemServices.GetAsync**](swbemservices-getasync.md) method returns an **SWbemObject** in the *objWbemObject* parameter of the **OnObjectReady** event of the [**SWbemSink**](swbemsink.md) object, which is passed as the *objWbemObject* parameter of the original call.</span></span> <span data-ttu-id="5a3aa-114">El mismo objeto **SWbemObject** se puede obtener mediante una llamada sincrónica equivalente a [**SWbemServices. Get**](swbemservices-get.md).</span><span class="sxs-lookup"><span data-stu-id="5a3aa-114">The same **SWbemObject** object can be obtained by using an equivalent synchronous call to [**SWbemServices.Get**](swbemservices-get.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a3aa-115">*objWbemAsyncContext*</span><span class="sxs-lookup"><span data-stu-id="5a3aa-115">*objWbemAsyncContext*</span></span> 
</dt> <dd>

<span data-ttu-id="5a3aa-116">Un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que se pasa a la llamada asincrónica original.</span><span class="sxs-lookup"><span data-stu-id="5a3aa-116">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that is passed to the original asynchronous call.</span></span> <span data-ttu-id="5a3aa-117">Use este parámetro para identificar el origen de la llamada asincrónica que desencadena este evento cuando se realizan varias llamadas asincrónicas con este receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="5a3aa-117">Use this parameter to identify the origin of the asynchronous call that triggers this event when multiple asynchronous calls are made using this object sink.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a3aa-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5a3aa-118">Return value</span></span>

<span data-ttu-id="5a3aa-119">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="5a3aa-119">This event does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5a3aa-120">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="5a3aa-120">Error codes</span></span>

<span data-ttu-id="5a3aa-121">Después de la finalización del evento **OnObjectReady** , el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener uno de los códigos de error siguientes.</span><span class="sxs-lookup"><span data-stu-id="5a3aa-121">After the completion of the **OnObjectReady** event, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="5a3aa-122">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="5a3aa-122">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="5a3aa-123">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="5a3aa-123">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="5a3aa-124">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="5a3aa-124">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="5a3aa-125">Memoria insuficiente para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="5a3aa-125">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="5a3aa-126">**wbemErrTransportFailure** -2147749909 (0x80041015)</span><span class="sxs-lookup"><span data-stu-id="5a3aa-126">**wbemErrTransportFailure** - 2147749909 (0x80041015)</span></span>
</dt> <dd>

<span data-ttu-id="5a3aa-127">Se produjo un error de red, evitando el funcionamiento normal.</span><span class="sxs-lookup"><span data-stu-id="5a3aa-127">Networking error occurred, preventing normal operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5a3aa-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5a3aa-128">Remarks</span></span>

<span data-ttu-id="5a3aa-129">Una devolución de llamada asincrónica permite que un usuario no autenticado proporcione datos al receptor.</span><span class="sxs-lookup"><span data-stu-id="5a3aa-129">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="5a3aa-130">Esto supone riesgos de seguridad para los scripts y las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="5a3aa-130">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="5a3aa-131">Para eliminar los riesgos, utilice la comunicación sincrónica o la comunicación sincrónica.</span><span class="sxs-lookup"><span data-stu-id="5a3aa-131">To eliminate the risks, use either semi-synchronous communication or synchronous communication.</span></span> <span data-ttu-id="5a3aa-132">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="5a3aa-132">For more information, see [Calling a Method](calling-a-method.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5a3aa-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a3aa-133">Requirements</span></span>



| <span data-ttu-id="5a3aa-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a3aa-134">Requirement</span></span> | <span data-ttu-id="5a3aa-135">Value</span><span class="sxs-lookup"><span data-stu-id="5a3aa-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a3aa-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a3aa-136">Minimum supported client</span></span><br/> | <span data-ttu-id="5a3aa-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5a3aa-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5a3aa-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a3aa-138">Minimum supported server</span></span><br/> | <span data-ttu-id="5a3aa-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5a3aa-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5a3aa-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5a3aa-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a3aa-141"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a3aa-141"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5a3aa-142">IDL</span><span class="sxs-lookup"><span data-stu-id="5a3aa-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5a3aa-143"><dt>Wbemdisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5a3aa-143"><dt>Wbemdisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="5a3aa-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5a3aa-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a3aa-145"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a3aa-145"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5a3aa-146">CLSID</span><span class="sxs-lookup"><span data-stu-id="5a3aa-146">CLSID</span></span><br/>                    | <span data-ttu-id="5a3aa-147">CLSID \_ SWbemSink</span><span class="sxs-lookup"><span data-stu-id="5a3aa-147">CLSID\_SWbemSink</span></span><br/>                                                             |
| <span data-ttu-id="5a3aa-148">IID</span><span class="sxs-lookup"><span data-stu-id="5a3aa-148">IID</span></span><br/>                      | <span data-ttu-id="5a3aa-149">\_ISWBEMSINKEVENTS IID</span><span class="sxs-lookup"><span data-stu-id="5a3aa-149">IID\_ISWbemSinkEvents</span></span><br/>                                                        |



## <a name="see-also"></a><span data-ttu-id="5a3aa-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="5a3aa-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a3aa-151">**SWbemSink**</span><span class="sxs-lookup"><span data-stu-id="5a3aa-151">**SWbemSink**</span></span>](swbemsink.md)
</dt> </dl>

 

