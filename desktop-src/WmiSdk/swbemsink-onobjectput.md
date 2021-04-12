---
description: El evento OnObjectPut de un objeto SWbemSink se desencadena cuando se completa una operación PUT asincrónica. Este evento devuelve la ruta de acceso del objeto de la instancia o la clase guardada.
ms.assetid: 2046dd03-ac2c-49fa-b1ad-a458967709e5
ms.tgt_platform: multiple
title: 'Evento ISWbemSinkEvents:: OnObjectPut (Wbemdisp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnObjectPut
- ISWbemSinkEvents.OnObjectPut
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c6ed42105efe407558d80cd108e657e396e88763
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279286"
---
# <a name="iswbemsinkeventsonobjectput-event"></a><span data-ttu-id="5e28a-104">Evento ISWbemSinkEvents:: OnObjectPut</span><span class="sxs-lookup"><span data-stu-id="5e28a-104">ISWbemSinkEvents::OnObjectPut event</span></span>

<span data-ttu-id="5e28a-105">El evento **OnObjectPut** de un objeto [**SWbemSink**](swbemsink.md) se desencadena cuando se completa una operación PUT asincrónica.</span><span class="sxs-lookup"><span data-stu-id="5e28a-105">The **OnObjectPut** event of an [**SWbemSink**](swbemsink.md) object is triggered when an asynchronous Put operation is complete.</span></span> <span data-ttu-id="5e28a-106">Este evento devuelve la ruta de acceso del objeto de la instancia o la clase guardada.</span><span class="sxs-lookup"><span data-stu-id="5e28a-106">This event returns the object path of the instance or the saved class.</span></span>

<span data-ttu-id="5e28a-107">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="5e28a-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5e28a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5e28a-108">Syntax</span></span>


```VB
SWbemSink.OnObjectPut( _
  ByVal objWbemObjectPath, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a><span data-ttu-id="5e28a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5e28a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e28a-110">*objWbemObjectPath*</span><span class="sxs-lookup"><span data-stu-id="5e28a-110">*objWbemObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="5e28a-111">Objeto [**SWbemObjectPath**](swbemobjectpath.md) que contiene la ruta de acceso del objeto de la instancia o clase que la operación PUT escribe en WMI.</span><span class="sxs-lookup"><span data-stu-id="5e28a-111">An [**SWbemObjectPath**](swbemobjectpath.md) object, that contains the object path of the instance or class that the put operation writes to WMI.</span></span>

</dd> <dt>

<span data-ttu-id="5e28a-112">*objWbemAsyncContext*</span><span class="sxs-lookup"><span data-stu-id="5e28a-112">*objWbemAsyncContext*</span></span> 
</dt> <dd>

<span data-ttu-id="5e28a-113">Un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que se pasa a la llamada asincrónica original.</span><span class="sxs-lookup"><span data-stu-id="5e28a-113">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that is passed to the original asynchronous call.</span></span> <span data-ttu-id="5e28a-114">Use este parámetro para identificar el origen de la llamada asincrónica que desencadena este evento cuando se realizan varias llamadas asincrónicas con este receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="5e28a-114">Use this parameter to identify the origin of the asynchronous call that triggers this event when multiple asynchronous calls are made using this object sink.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e28a-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5e28a-115">Return value</span></span>

<span data-ttu-id="5e28a-116">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="5e28a-116">This event does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5e28a-117">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="5e28a-117">Error codes</span></span>

<span data-ttu-id="5e28a-118">Después de la finalización del evento **OnObjectPut** , el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener uno de los códigos de error siguientes.</span><span class="sxs-lookup"><span data-stu-id="5e28a-118">After the completion of the **OnObjectPut** event, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="5e28a-119">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="5e28a-119">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="5e28a-120">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="5e28a-120">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="5e28a-121">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="5e28a-121">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="5e28a-122">Memoria insuficiente para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="5e28a-122">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="5e28a-123">**wbemErrTransportFailure** -2147749909 (0x80041015)</span><span class="sxs-lookup"><span data-stu-id="5e28a-123">**wbemErrTransportFailure** - 2147749909 (0x80041015)</span></span>
</dt> <dd>

<span data-ttu-id="5e28a-124">Se produjo un error de red, evitando el funcionamiento normal.</span><span class="sxs-lookup"><span data-stu-id="5e28a-124">Networking error occurred, preventing normal operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5e28a-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5e28a-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5e28a-126">Una devolución de llamada asincrónica permite que un usuario no autenticado proporcione datos al receptor.</span><span class="sxs-lookup"><span data-stu-id="5e28a-126">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="5e28a-127">Esto supone riesgos de seguridad para los scripts y las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="5e28a-127">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="5e28a-128">Para eliminar los riesgos, utilice la comunicación sincrónica o la comunicación sincrónica.</span><span class="sxs-lookup"><span data-stu-id="5e28a-128">To eliminate the risks, use either semi-synchronous communication or synchronous communication.</span></span> <span data-ttu-id="5e28a-129">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="5e28a-129">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5e28a-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e28a-130">Requirements</span></span>



| <span data-ttu-id="5e28a-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e28a-131">Requirement</span></span> | <span data-ttu-id="5e28a-132">Value</span><span class="sxs-lookup"><span data-stu-id="5e28a-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e28a-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e28a-133">Minimum supported client</span></span><br/> | <span data-ttu-id="5e28a-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5e28a-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5e28a-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e28a-135">Minimum supported server</span></span><br/> | <span data-ttu-id="5e28a-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5e28a-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5e28a-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5e28a-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e28a-138"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e28a-138"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5e28a-139">IDL</span><span class="sxs-lookup"><span data-stu-id="5e28a-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5e28a-140"><dt>Wbemdisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5e28a-140"><dt>Wbemdisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="5e28a-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5e28a-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e28a-142"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e28a-142"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5e28a-143">CLSID</span><span class="sxs-lookup"><span data-stu-id="5e28a-143">CLSID</span></span><br/>                    | <span data-ttu-id="5e28a-144">CLSID \_ SWbemSink</span><span class="sxs-lookup"><span data-stu-id="5e28a-144">CLSID\_SWbemSink</span></span><br/>                                                             |
| <span data-ttu-id="5e28a-145">IID</span><span class="sxs-lookup"><span data-stu-id="5e28a-145">IID</span></span><br/>                      | <span data-ttu-id="5e28a-146">\_ISWBEMSINKEVENTS IID</span><span class="sxs-lookup"><span data-stu-id="5e28a-146">IID\_ISWbemSinkEvents</span></span><br/>                                                        |



## <a name="see-also"></a><span data-ttu-id="5e28a-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="5e28a-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e28a-148">**SWbemSink**</span><span class="sxs-lookup"><span data-stu-id="5e28a-148">**SWbemSink**</span></span>](swbemsink.md)
</dt> </dl>

 

