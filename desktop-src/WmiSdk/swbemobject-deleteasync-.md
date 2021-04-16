---
description: El \_ método DeleteAsync de SWbemObject elimina de forma asincrónica la clase actual o la instancia actual.
ms.assetid: b8d67fa5-5217-422b-acbe-5eea6028deeb
ms.tgt_platform: multiple
title: Método SWbemObject.DeleteAsync_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.DeleteAsync_
- ISWbemObject.DeleteAsync_
- ISWbemObject.DeleteAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 7951b84a2b5d9f06061f4cefb04c797ccfea3ecd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706053"
---
# <a name="swbemobjectdeleteasync_-method"></a><span data-ttu-id="d7124-103">SWbemObject. DeleteAsync, \_ método</span><span class="sxs-lookup"><span data-stu-id="d7124-103">SWbemObject.DeleteAsync\_ method</span></span>

<span data-ttu-id="d7124-104">El **método \_ DeleteAsync** de [**SWbemObject**](swbemobject.md) elimina de forma asincrónica la clase actual o la instancia actual.</span><span class="sxs-lookup"><span data-stu-id="d7124-104">The **DeleteAsync\_** method of [**SWbemObject**](swbemobject.md) asynchronously deletes either the current class or the current instance.</span></span> <span data-ttu-id="d7124-105">Si un proveedor dinámico proporciona la clase o la instancia, a veces no es posible eliminar este objeto a menos que el proveedor admita la eliminación de la clase o la instancia.</span><span class="sxs-lookup"><span data-stu-id="d7124-105">If a dynamic provider supplies the class or instance, sometimes it is not possible to delete this object unless the provider supports class or instance deletion.</span></span>

<span data-ttu-id="d7124-106">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="d7124-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d7124-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d7124-107">Syntax</span></span>


```VB
SWbemObject.DeleteAsync_( _
  ByVal objWbemSink, _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="d7124-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d7124-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7124-109">*objWbemSink* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d7124-109">*objWbemSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7124-110">Receptor de objeto que devuelve el resultado de la operación de eliminación.</span><span class="sxs-lookup"><span data-stu-id="d7124-110">Object sink that returns the outcome of the delete operation.</span></span>

</dd> <dt>

<span data-ttu-id="d7124-111">*iFlags* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="d7124-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d7124-112">Entero que determina el comportamiento de la llamada.</span><span class="sxs-lookup"><span data-stu-id="d7124-112">Integer that determines the behavior of the call.</span></span> <span data-ttu-id="d7124-113">Este parámetro puede aceptar los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="d7124-113">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="d7124-114"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="d7124-114"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="d7124-115">Hace que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**SWbemSink. OnProgress**](swbemsink-onprogress.md) para el receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="d7124-115">Causes asynchronous calls to send status updates to the [**SWbemSink.OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="d7124-116"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="d7124-116"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* ( 0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="d7124-117">Impide que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**OnProgress**](swbemsink-onprogress.md) para el receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="d7124-117">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d7124-118">*objwbemNamedValueSet* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="d7124-118">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d7124-119">Normalmente, este parámetro no está definido.</span><span class="sxs-lookup"><span data-stu-id="d7124-119">This parameter is typically undefined.</span></span> <span data-ttu-id="d7124-120">De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que atiende la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d7124-120">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="d7124-121">Un proveedor que admite o requiere tal información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.</span><span class="sxs-lookup"><span data-stu-id="d7124-121">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="d7124-122">*objWbemAsyncContext* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="d7124-122">*objWbemAsyncContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d7124-123">Se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que devuelve al receptor del objeto para identificar el origen de la llamada asincrónica original.</span><span class="sxs-lookup"><span data-stu-id="d7124-123">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="d7124-124">Utilice este parámetro si va a realizar varias llamadas asincrónicas mediante el mismo receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="d7124-124">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="d7124-125">Para usar este parámetro, cree un objeto **SWbemNamedValueSet** y use el método [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) para agregar un valor que identifique la llamada asincrónica que está realizando.</span><span class="sxs-lookup"><span data-stu-id="d7124-125">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="d7124-126">Este objeto **SWbemNamedValueSet** se devuelve al receptor del objeto y el origen de la llamada se puede extraer mediante el método [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="d7124-126">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="d7124-127">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="d7124-127">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7124-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d7124-128">Return value</span></span>

<span data-ttu-id="d7124-129">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="d7124-129">This method does not return a value.</span></span> <span data-ttu-id="d7124-130">Si esta llamada es correcta, el resultado de la operación de eliminación se proporciona a través del receptor de objeto proporcionado.</span><span class="sxs-lookup"><span data-stu-id="d7124-130">If this call is successful, the result of the delete operation is provided through the supplied object sink.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d7124-131">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="d7124-131">Error codes</span></span>

<span data-ttu-id="d7124-132">Después de completar el método **DeleteAsync \_** , el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener uno de los códigos de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="d7124-132">After the completion of the **DeleteAsync\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="d7124-133">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="d7124-133">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="d7124-134">El contexto actual no tiene los derechos de seguridad adecuados para eliminar el objeto.</span><span class="sxs-lookup"><span data-stu-id="d7124-134">Current context does not have adequate security rights to delete the object.</span></span>

</dd> <dt>

<span data-ttu-id="d7124-135">**wbemErrFailed** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="d7124-135">**wbemErrFailed** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="d7124-136">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="d7124-136">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="d7124-137">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="d7124-137">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="d7124-138">La clase especificada no existe.</span><span class="sxs-lookup"><span data-stu-id="d7124-138">Specified class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="d7124-139">**wbemErrInvalidOperation** -2147749910 (0x80041016)</span><span class="sxs-lookup"><span data-stu-id="d7124-139">**wbemErrInvalidOperation** - 2147749910 (0x80041016)</span></span>
</dt> <dd>

<span data-ttu-id="d7124-140">No se puede eliminar el objeto.</span><span class="sxs-lookup"><span data-stu-id="d7124-140">Object cannot be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="d7124-141">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="d7124-141">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="d7124-142">El objeto no existía.</span><span class="sxs-lookup"><span data-stu-id="d7124-142">Object did not exist.</span></span>

</dd> <dt>

<span data-ttu-id="d7124-143">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="d7124-143">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="d7124-144">Memoria insuficiente para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="d7124-144">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d7124-145">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d7124-145">Remarks</span></span>

<span data-ttu-id="d7124-146">Esta llamada se devuelve inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="d7124-146">This call returns immediately.</span></span> <span data-ttu-id="d7124-147">El estado se devuelve al autor de la llamada a través de una devolución de llamada que se entrega al receptor que se especifica en *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="d7124-147">The status is returned to the caller through a callback delivered to the sink that is specified in *objWbemSink*.</span></span>

<span data-ttu-id="d7124-148">Una devolución de llamada asincrónica permite que un usuario no autenticado proporcione datos al receptor.</span><span class="sxs-lookup"><span data-stu-id="d7124-148">An asynchronous callback allows a nonauthenticated user to provide data to the sink.</span></span> <span data-ttu-id="d7124-149">Esto supone riesgos de seguridad para los scripts y las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="d7124-149">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="d7124-150">Para eliminar los riesgos, utilice la comunicación semisincrónica o la comunicación sincrónica.</span><span class="sxs-lookup"><span data-stu-id="d7124-150">To eliminate the risks, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="d7124-151">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="d7124-151">For more information, see [Calling a Method](calling-a-method.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d7124-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7124-152">Requirements</span></span>



| <span data-ttu-id="d7124-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7124-153">Requirement</span></span> | <span data-ttu-id="d7124-154">Value</span><span class="sxs-lookup"><span data-stu-id="d7124-154">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7124-155">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7124-155">Minimum supported client</span></span><br/> | <span data-ttu-id="d7124-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d7124-156">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d7124-157">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7124-157">Minimum supported server</span></span><br/> | <span data-ttu-id="d7124-158">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d7124-158">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d7124-159">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d7124-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7124-160"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7124-160"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d7124-161">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d7124-161">Type library</span></span><br/>             | <dl> <span data-ttu-id="d7124-162"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d7124-162"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d7124-163">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d7124-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7124-164"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7124-164"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d7124-165">CLSID</span><span class="sxs-lookup"><span data-stu-id="d7124-165">CLSID</span></span><br/>                    | <span data-ttu-id="d7124-166">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="d7124-166">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="d7124-167">IID</span><span class="sxs-lookup"><span data-stu-id="d7124-167">IID</span></span><br/>                      | <span data-ttu-id="d7124-168">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="d7124-168">IID\_ISWbemObject</span></span><br/>                                                            |



 

