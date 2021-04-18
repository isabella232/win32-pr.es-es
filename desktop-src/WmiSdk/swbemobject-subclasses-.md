---
description: El método subclasses \_ del objeto SWbemObject devuelve un objeto SWbemObjectSet.
ms.assetid: c17e5d4a-016f-42ae-bc11-e21a44772ce5
ms.tgt_platform: multiple
title: Método SWbemObject.Subclasses_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Subclasses_
- ISWbemObject.Subclasses_
- ISWbemObject.Subclasses_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: efae27b26235cbf1c298c7b45de69e1cf49c8570
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696790"
---
# <a name="swbemobjectsubclasses_-method"></a><span data-ttu-id="3e9b3-103">SWbemObject. subclasses ( \_ método)</span><span class="sxs-lookup"><span data-stu-id="3e9b3-103">SWbemObject.Subclasses\_ method</span></span>

<span data-ttu-id="3e9b3-104">El método **subclasses \_** del objeto [**SWbemObject**](swbemobject.md) devuelve un objeto [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="3e9b3-104">The **Subclasses\_** method of the [**SWbemObject**](swbemobject.md) object returns an [**SWbemObjectSet**](swbemobjectset.md) object.</span></span> <span data-ttu-id="3e9b3-105">Este objeto es una colección de subclases del objeto actual, que debe ser una clase.</span><span class="sxs-lookup"><span data-stu-id="3e9b3-105">This object is a collection of subclasses of the current object, which must be a class.</span></span> <span data-ttu-id="3e9b3-106">Los elementos de la colección devuelta se pueden obtener mediante métodos de colección estándar.</span><span class="sxs-lookup"><span data-stu-id="3e9b3-106">Items in the returned collection can be obtained using standard collection methods.</span></span> <span data-ttu-id="3e9b3-107">Para obtener más información, vea [obtener acceso a una colección](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="3e9b3-107">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

<span data-ttu-id="3e9b3-108">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="3e9b3-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3e9b3-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3e9b3-109">Syntax</span></span>


```VB
objWbemObjectSet = .Subclasses_( _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="3e9b3-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3e9b3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e9b3-111">*iFlags* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="3e9b3-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3e9b3-112">Entero que determina la información detallada que enumera la llamada.</span><span class="sxs-lookup"><span data-stu-id="3e9b3-112">Integer that determines how detailed the call enumerates.</span></span> <span data-ttu-id="3e9b3-113">Este parámetro puede aceptar los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="3e9b3-113">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span data-ttu-id="3e9b3-114"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemQueryFlagDeep \* \* \* \* (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="3e9b3-114"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>\*\*\*\*wbemQueryFlagDeep\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="3e9b3-115">Fuerza la enumeración recursiva en todas las subclases derivadas de la clase primaria especificada.</span><span class="sxs-lookup"><span data-stu-id="3e9b3-115">Forces recursive enumeration into all subclasses derived from the specified parent class.</span></span> <span data-ttu-id="3e9b3-116">La propia clase primaria no se devuelve en la enumeración.</span><span class="sxs-lookup"><span data-stu-id="3e9b3-116">The parent class itself is not returned in the enumeration.</span></span>

</dd> <dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span data-ttu-id="3e9b3-117"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemQueryFlagShallow \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="3e9b3-117"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>\*\*\*\*wbemQueryFlagShallow\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="3e9b3-118">Valor predeterminado para este parámetro.</span><span class="sxs-lookup"><span data-stu-id="3e9b3-118">Default value for this parameter.</span></span> <span data-ttu-id="3e9b3-119">Obliga a la enumeración a incluir solo las subclases inmediatas de la clase primaria especificada.</span><span class="sxs-lookup"><span data-stu-id="3e9b3-119">It forces the enumeration to include only immediate subclasses of the specified parent class.</span></span>

</dd> <dt>

<span id="WbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="3e9b3-120"><span id="WbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>WbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="3e9b3-120"><span id="WbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*WbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="3e9b3-121">Hace que la llamada se devuelva inmediatamente</span><span class="sxs-lookup"><span data-stu-id="3e9b3-121">Causes the call to return immediately</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="3e9b3-122"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* \* (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="3e9b3-122"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="3e9b3-123">Hace que esta llamada se bloquee hasta que se complete la llamada.</span><span class="sxs-lookup"><span data-stu-id="3e9b3-123">Causes this call to block until the call has completed.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="3e9b3-124"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="3e9b3-124"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="3e9b3-125">Hace que WMI devuelva datos de modificación de clase junto con la definición de clase base.</span><span class="sxs-lookup"><span data-stu-id="3e9b3-125">Causes WMI to return class amendment data along with the base class definition.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="3e9b3-126">*objwbemNamedValueSet* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="3e9b3-126">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3e9b3-127">Normalmente, esto no está definido.</span><span class="sxs-lookup"><span data-stu-id="3e9b3-127">Typically, this is undefined.</span></span> <span data-ttu-id="3e9b3-128">De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que atiende la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3e9b3-128">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="3e9b3-129">Un proveedor que admite o requiere tal información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.</span><span class="sxs-lookup"><span data-stu-id="3e9b3-129">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e9b3-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3e9b3-130">Return value</span></span>

<span data-ttu-id="3e9b3-131">Si la llamada se realiza correctamente, se devuelve un objeto [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="3e9b3-131">If the call is successful, an [**SWbemObjectSet**](swbemobjectset.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3e9b3-132">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="3e9b3-132">Error codes</span></span>

<span data-ttu-id="3e9b3-133">Después de completar el método de **subclases \_** , el objeto **Err** puede contener uno de los códigos de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="3e9b3-133">After the completion of the **Subclasses\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="3e9b3-134">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="3e9b3-134">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="3e9b3-135">El usuario actual no tiene permiso para ver una o varias de las clases devueltas por la llamada.</span><span class="sxs-lookup"><span data-stu-id="3e9b3-135">Current user does not have permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="3e9b3-136">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="3e9b3-136">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="3e9b3-137">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="3e9b3-137">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="3e9b3-138">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="3e9b3-138">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="3e9b3-139">La clase especificada no existía.</span><span class="sxs-lookup"><span data-stu-id="3e9b3-139">Specified class did not exist.</span></span>

</dd> <dt>

<span data-ttu-id="3e9b3-140">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="3e9b3-140">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="3e9b3-141">Se especificó un parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="3e9b3-141">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="3e9b3-142">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="3e9b3-142">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="3e9b3-143">Memoria insuficiente para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="3e9b3-143">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3e9b3-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3e9b3-144">Remarks</span></span>

<span data-ttu-id="3e9b3-145">No es un error que la colección devuelta tenga cero elementos si no hay ninguna subclase del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="3e9b3-145">It is not an error for the returned collection to have zero elements if there are no subclasses of the current object.</span></span> <span data-ttu-id="3e9b3-146">El método **subclases \_** solo funciona con objetos de clase.</span><span class="sxs-lookup"><span data-stu-id="3e9b3-146">The **Subclasses\_** method only works for class objects.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e9b3-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e9b3-147">Requirements</span></span>



| <span data-ttu-id="3e9b3-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e9b3-148">Requirement</span></span> | <span data-ttu-id="3e9b3-149">Value</span><span class="sxs-lookup"><span data-stu-id="3e9b3-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e9b3-150">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e9b3-150">Minimum supported client</span></span><br/> | <span data-ttu-id="3e9b3-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3e9b3-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3e9b3-152">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e9b3-152">Minimum supported server</span></span><br/> | <span data-ttu-id="3e9b3-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3e9b3-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3e9b3-154">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3e9b3-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e9b3-155"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e9b3-155"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="3e9b3-156">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="3e9b3-156">Type library</span></span><br/>             | <dl> <span data-ttu-id="3e9b3-157"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3e9b3-157"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3e9b3-158">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3e9b3-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e9b3-159"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e9b3-159"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="3e9b3-160">CLSID</span><span class="sxs-lookup"><span data-stu-id="3e9b3-160">CLSID</span></span><br/>                    | <span data-ttu-id="3e9b3-161">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="3e9b3-161">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="3e9b3-162">IID</span><span class="sxs-lookup"><span data-stu-id="3e9b3-162">IID</span></span><br/>                      | <span data-ttu-id="3e9b3-163">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="3e9b3-163">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="3e9b3-164">Vea también</span><span class="sxs-lookup"><span data-stu-id="3e9b3-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e9b3-165">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="3e9b3-165">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="3e9b3-166">**SWbemObjectSet**</span><span class="sxs-lookup"><span data-stu-id="3e9b3-166">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> </dl>

 

 




