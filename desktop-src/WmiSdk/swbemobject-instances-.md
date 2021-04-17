---
description: El método instances \_ del objeto SWbemObject crea un enumerador que devuelve las instancias del objeto de clase actual. Este método implementa una consulta simple. Las consultas más complejas pueden requerir el uso de SWbemServices.ExecQuery.
ms.assetid: 30402d7d-f7cb-43b5-96b5-a8a76144e32d
ms.tgt_platform: multiple
title: Método SWbemObject.Instances_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Instances_
- ISWbemObject.Instances_
- ISWbemObject.Instances_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c573c1e94cd473d22483c7b6a2c801c3e6bcb9dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716990"
---
# <a name="swbemobjectinstances_-method"></a><span data-ttu-id="2157a-105">SWbemObject. Instances ( \_ método)</span><span class="sxs-lookup"><span data-stu-id="2157a-105">SWbemObject.Instances\_ method</span></span>

<span data-ttu-id="2157a-106">El **método \_ instances** del objeto [**SWbemObject**](swbemobject.md) crea un enumerador que devuelve las instancias del objeto de clase actual.</span><span class="sxs-lookup"><span data-stu-id="2157a-106">The **Instances\_** method of the [**SWbemObject**](swbemobject.md) object creates an enumerator that returns the instances of the current class object.</span></span> <span data-ttu-id="2157a-107">Este método implementa una consulta simple.</span><span class="sxs-lookup"><span data-stu-id="2157a-107">This method implements a simple query.</span></span> <span data-ttu-id="2157a-108">Las consultas más complejas pueden requerir el uso de [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span><span class="sxs-lookup"><span data-stu-id="2157a-108">More complex queries may require the use of [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span></span>

<span data-ttu-id="2157a-109">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="2157a-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2157a-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2157a-110">Syntax</span></span>


```VB
objWbemObjectSet = .Instances_( _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="2157a-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2157a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2157a-112">*iFlags* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="2157a-112">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2157a-113">Entero que determina el comportamiento de la llamada.</span><span class="sxs-lookup"><span data-stu-id="2157a-113">Integer that determines the behavior of the call.</span></span> <span data-ttu-id="2157a-114">Este parámetro puede aceptar los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="2157a-114">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="2157a-115"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="2157a-115"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="2157a-116">Hace que se devuelva un enumerador de solo avance.</span><span class="sxs-lookup"><span data-stu-id="2157a-116">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="2157a-117">Los enumeradores de solo avance suelen ser mucho más rápidos y usan menos memoria que los enumeradores convencionales, pero no permiten llamadas a [**SWbemObject. \_ Clone**](swbemobject-clone-.md).</span><span class="sxs-lookup"><span data-stu-id="2157a-117">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span data-ttu-id="2157a-118"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional \* \* \* \* (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="2157a-118"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>\*\*\*\*wbemFlagBidirectional\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="2157a-119">Hace que WMI conserve punteros a objetos de la enumeración hasta que el cliente libere el enumerador.</span><span class="sxs-lookup"><span data-stu-id="2157a-119">Causes WMI to retain pointers to objects of the enumeration until the client releases the enumerator.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="2157a-120"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="2157a-120"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="2157a-121">Valor predeterminado para este parámetro.</span><span class="sxs-lookup"><span data-stu-id="2157a-121">Default value for this parameter.</span></span> <span data-ttu-id="2157a-122">Esta marca hace que la llamada se devuelva inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="2157a-122">This flag causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="2157a-123"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* \* (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="2157a-123"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* ( 0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="2157a-124">Hace que esta llamada se bloquee hasta que se complete la consulta.</span><span class="sxs-lookup"><span data-stu-id="2157a-124">Causes this call to block until the query has completed.</span></span>

</dd> <dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span data-ttu-id="2157a-125"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemQueryFlagShallow \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="2157a-125"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>\*\*\*\*wbemQueryFlagShallow\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="2157a-126">Fuerza a la enumeración a incluir solo las subclases inmediatas de la clase primaria especificada.</span><span class="sxs-lookup"><span data-stu-id="2157a-126">Forces the enumeration to include only immediate subclasses of the specified parent class.</span></span>

</dd> <dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span data-ttu-id="2157a-127"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemQueryFlagDeep \* \* \* \* (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="2157a-127"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>\*\*\*\*wbemQueryFlagDeep\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="2157a-128">Valor predeterminado para este parámetro.</span><span class="sxs-lookup"><span data-stu-id="2157a-128">Default for this parameter.</span></span> <span data-ttu-id="2157a-129">Este valor fuerza a la enumeración a incluir todas las clases de la jerarquía.</span><span class="sxs-lookup"><span data-stu-id="2157a-129">This value forces the enumeration to include all classes in the hierarchy.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="2157a-130"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="2157a-130"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="2157a-131">Hace que WMI devuelva datos de modificación de clase con la definición de clase base.</span><span class="sxs-lookup"><span data-stu-id="2157a-131">Causes WMI to return class amendment data with the base class definition.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="2157a-132">*objwbemNamedValueSet* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="2157a-132">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2157a-133">Normalmente, esto no está definido.</span><span class="sxs-lookup"><span data-stu-id="2157a-133">Typically, this is undefined.</span></span> <span data-ttu-id="2157a-134">De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que atiende la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2157a-134">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="2157a-135">Un proveedor que admite o requiere tal información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.</span><span class="sxs-lookup"><span data-stu-id="2157a-135">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2157a-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2157a-136">Return value</span></span>

<span data-ttu-id="2157a-137">Si el método se realiza correctamente, se devuelve un objeto [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="2157a-137">If the method is successful, an [**SWbemObjectSet**](swbemobjectset.md) object returns.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2157a-138">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="2157a-138">Error codes</span></span>

<span data-ttu-id="2157a-139">Después de completar el método **instances \_** , el objeto **Err** puede contener uno de los códigos de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="2157a-139">After the completion of the **Instances\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="2157a-140">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="2157a-140">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="2157a-141">El usuario actual no tiene permiso para ver las instancias de la clase especificada.</span><span class="sxs-lookup"><span data-stu-id="2157a-141">Current user does not have permission to view instances of the specified class.</span></span>

</dd> <dt>

<span data-ttu-id="2157a-142">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="2157a-142">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="2157a-143">Se produjo un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="2157a-143">Unspecified error occurred.</span></span>

</dd> <dt>

<span data-ttu-id="2157a-144">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="2157a-144">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="2157a-145">La clase especificada no es válida.</span><span class="sxs-lookup"><span data-stu-id="2157a-145">Specified class is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="2157a-146">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="2157a-146">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="2157a-147">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="2157a-147">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="2157a-148">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="2157a-148">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="2157a-149">Memoria insuficiente para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="2157a-149">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2157a-150">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2157a-150">Remarks</span></span>

<span data-ttu-id="2157a-151">El **método \_ instances** solo funciona con objetos de clase.</span><span class="sxs-lookup"><span data-stu-id="2157a-151">The **Instances\_** method only works for class objects.</span></span> <span data-ttu-id="2157a-152">No es un error que la colección devuelta tenga cero elementos.</span><span class="sxs-lookup"><span data-stu-id="2157a-152">It is not an error for the returned collection to have zero elements.</span></span> <span data-ttu-id="2157a-153">El comportamiento predeterminado de este método es [*semisincrónico*](gloss-s.md) debido al valor predeterminado de *IFlags* **wbemFlagReturnImmediately**.</span><span class="sxs-lookup"><span data-stu-id="2157a-153">The default behavior for this method is [*semisynchronous*](gloss-s.md) because of the default *IFlags* value **wbemFlagReturnImmediately**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2157a-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2157a-154">Requirements</span></span>



| <span data-ttu-id="2157a-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="2157a-155">Requirement</span></span> | <span data-ttu-id="2157a-156">Value</span><span class="sxs-lookup"><span data-stu-id="2157a-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2157a-157">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2157a-157">Minimum supported client</span></span><br/> | <span data-ttu-id="2157a-158">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2157a-158">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2157a-159">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2157a-159">Minimum supported server</span></span><br/> | <span data-ttu-id="2157a-160">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2157a-160">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2157a-161">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2157a-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="2157a-162"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2157a-162"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2157a-163">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="2157a-163">Type library</span></span><br/>             | <dl> <span data-ttu-id="2157a-164"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2157a-164"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2157a-165">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2157a-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2157a-166"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2157a-166"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2157a-167">CLSID</span><span class="sxs-lookup"><span data-stu-id="2157a-167">CLSID</span></span><br/>                    | <span data-ttu-id="2157a-168">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="2157a-168">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="2157a-169">IID</span><span class="sxs-lookup"><span data-stu-id="2157a-169">IID</span></span><br/>                      | <span data-ttu-id="2157a-170">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="2157a-170">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="2157a-171">Vea también</span><span class="sxs-lookup"><span data-stu-id="2157a-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2157a-172">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="2157a-172">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="2157a-173">**SWbemObjectSet**</span><span class="sxs-lookup"><span data-stu-id="2157a-173">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> </dl>

 

 




