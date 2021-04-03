---
description: Crea un enumerador que devuelve las instancias de una clase especificada de acuerdo con los criterios de selección especificados por el usuario.
ms.assetid: 6465a981-f98e-4ece-a9b6-9da8ae618bc6
ms.tgt_platform: multiple
title: Método SWbemServices. Instances (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.InstancesOf
- ISWbemServices.InstancesOf
- ISWbemServices.InstancesOf
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e2386b52160b1e2a08c5a345b67922ed24afc44c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913189"
---
# <a name="swbemservicesinstancesof-method"></a><span data-ttu-id="8a144-103">SWbemServices. Instances (método)</span><span class="sxs-lookup"><span data-stu-id="8a144-103">SWbemServices.InstancesOf method</span></span>

<span data-ttu-id="8a144-104">El método **instances** del objeto [**SWbemServices**](swbemservices.md) crea un enumerador que devuelve las instancias de una clase especificada de acuerdo con los criterios de selección especificados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="8a144-104">The **InstancesOf** method of the [**SWbemServices**](swbemservices.md) object creates an enumerator that returns the instances of a specified class according to the user-specified selection criteria.</span></span> <span data-ttu-id="8a144-105">Este método implementa una consulta simple.</span><span class="sxs-lookup"><span data-stu-id="8a144-105">This method implements a simple query.</span></span> <span data-ttu-id="8a144-106">Las consultas más complejas pueden requerir el uso de [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span><span class="sxs-lookup"><span data-stu-id="8a144-106">More complex queries may require the use of [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span></span>

<span data-ttu-id="8a144-107">Se llama al método en el modo semisincrónico.</span><span class="sxs-lookup"><span data-stu-id="8a144-107">The method is called in the semisynchronous mode.</span></span> <span data-ttu-id="8a144-108">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="8a144-108">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="8a144-109">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="8a144-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8a144-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8a144-110">Syntax</span></span>


```VB
objWbemObjectSet = .InstancesOf( _
  ByVal strClass, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="8a144-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8a144-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a144-112">*strClass*</span><span class="sxs-lookup"><span data-stu-id="8a144-112">*strClass*</span></span> 
</dt> <dd>

<span data-ttu-id="8a144-113">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8a144-113">Required.</span></span> <span data-ttu-id="8a144-114">Cadena que contiene el nombre de la clase para la que se desean instancias.</span><span class="sxs-lookup"><span data-stu-id="8a144-114">String that contains the name of the class for which instances are desired.</span></span> <span data-ttu-id="8a144-115">Este parámetro no puede estar en blanco.</span><span class="sxs-lookup"><span data-stu-id="8a144-115">This parameter cannot be blank.</span></span>

</dd> <dt>

<span data-ttu-id="8a144-116">*iFlags* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="8a144-116">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8a144-117">Este parámetro determina la información detallada que enumera la llamada y si esta llamada se devuelve inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="8a144-117">This parameter determines how detailed the call enumerates and if this call returns immediately.</span></span> <span data-ttu-id="8a144-118">El valor predeterminado de este parámetro es **wbemFlagReturnImmediately**.</span><span class="sxs-lookup"><span data-stu-id="8a144-118">The default value for this parameter is **wbemFlagReturnImmediately**.</span></span> <span data-ttu-id="8a144-119">Este parámetro puede aceptar los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="8a144-119">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="8a144-120"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="8a144-120"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="8a144-121">Hace que se devuelva un enumerador de solo avance.</span><span class="sxs-lookup"><span data-stu-id="8a144-121">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="8a144-122">Los enumeradores de solo avance suelen ser mucho más rápidos y usan menos memoria que los enumeradores convencionales, pero no permiten llamadas a [**SWbemObject. \_ Clone**](swbemobject-clone-.md).</span><span class="sxs-lookup"><span data-stu-id="8a144-122">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span data-ttu-id="8a144-123"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional \* \* \* \* (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="8a144-123"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>\*\*\*\*wbemFlagBidirectional\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="8a144-124">Hace que WMI conserve punteros a objetos de la enumeración hasta que el cliente libere el enumerador.</span><span class="sxs-lookup"><span data-stu-id="8a144-124">Causes WMI to retain pointers to objects of the enumeration until the client releases the enumerator.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="8a144-125"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="8a144-125"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="8a144-126">Valor predeterminado para este parámetro.</span><span class="sxs-lookup"><span data-stu-id="8a144-126">Default value for this parameter.</span></span> <span data-ttu-id="8a144-127">Esta marca hace que la llamada se devuelva inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="8a144-127">This flag causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="8a144-128"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* \* (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="8a144-128"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="8a144-129">Hace que esta llamada se bloquee hasta que se complete la consulta.</span><span class="sxs-lookup"><span data-stu-id="8a144-129">Causes this call to block until the query has completed.</span></span> <span data-ttu-id="8a144-130">Esta marca llama al método en el modo sincrónico.</span><span class="sxs-lookup"><span data-stu-id="8a144-130">This flag calls the method in the synchronous mode.</span></span>

</dd> <dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span data-ttu-id="8a144-131"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemQueryFlagShallow \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="8a144-131"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>\*\*\*\*wbemQueryFlagShallow\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="8a144-132">Fuerza a la enumeración a incluir solo las subclases inmediatas de la clase primaria especificada.</span><span class="sxs-lookup"><span data-stu-id="8a144-132">Forces the enumeration to include only immediate subclasses of the specified parent class.</span></span>

</dd> <dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span data-ttu-id="8a144-133"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemQueryFlagDeep \* \* \* \* (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="8a144-133"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>\*\*\*\*wbemQueryFlagDeep\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="8a144-134">Valor predeterminado para este parámetro.</span><span class="sxs-lookup"><span data-stu-id="8a144-134">Default value for this parameter.</span></span> <span data-ttu-id="8a144-135">Este valor fuerza a la enumeración a incluir todas las clases de la jerarquía.</span><span class="sxs-lookup"><span data-stu-id="8a144-135">This value forces the enumeration to include all classes in the hierarchy.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="8a144-136"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="8a144-136"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="8a144-137">Hace que WMI devuelva datos de modificación de clase con la definición de clase base.</span><span class="sxs-lookup"><span data-stu-id="8a144-137">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="8a144-138">Para obtener más información, consulte [localizar información de clase WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="8a144-138">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="8a144-139">*objWbemNamedValueSet* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="8a144-139">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8a144-140">Normalmente, esto no está definido.</span><span class="sxs-lookup"><span data-stu-id="8a144-140">Typically, this is undefined.</span></span> <span data-ttu-id="8a144-141">De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que atiende la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8a144-141">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="8a144-142">Un proveedor que admite o requiere tal información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.</span><span class="sxs-lookup"><span data-stu-id="8a144-142">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a144-143">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8a144-143">Return value</span></span>

<span data-ttu-id="8a144-144">Si se realiza correctamente, el método devuelve un [**SWbemObjectSet**](swbemobjectset.md).</span><span class="sxs-lookup"><span data-stu-id="8a144-144">If successful, the method returns an [**SWbemObjectSet**](swbemobjectset.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="8a144-145">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="8a144-145">Error codes</span></span>

<span data-ttu-id="8a144-146">Una vez finalizado el método **instances** , el objeto **Err** puede contener uno de los códigos de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="8a144-146">Upon the completion of the **InstancesOf** method, the **Err** object may contain one of the error codes in the following list.</span></span>

> [!Note]  
> <span data-ttu-id="8a144-147">Un enumerador devuelto con cero elementos no es un error.</span><span class="sxs-lookup"><span data-stu-id="8a144-147">A returned enumerator with zero elements is not an error.</span></span>

 

<dl> <dt>

<span data-ttu-id="8a144-148">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="8a144-148">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="8a144-149">El usuario actual no tiene permiso para ver las instancias de la clase especificada.</span><span class="sxs-lookup"><span data-stu-id="8a144-149">Current user does not have the permission to view instances of the specified class.</span></span>

</dd> <dt>

<span data-ttu-id="8a144-150">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="8a144-150">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="8a144-151">Se produjo un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="8a144-151">Unspecified error occurred.</span></span>

</dd> <dt>

<span data-ttu-id="8a144-152">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="8a144-152">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="8a144-153">La clase especificada no es válida.</span><span class="sxs-lookup"><span data-stu-id="8a144-153">Specified class is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="8a144-154">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="8a144-154">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="8a144-155">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="8a144-155">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="8a144-156">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="8a144-156">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="8a144-157">Memoria insuficiente para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="8a144-157">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8a144-158">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8a144-158">Remarks</span></span>

<span data-ttu-id="8a144-159">El método **instances** solo funciona con objetos de clase.</span><span class="sxs-lookup"><span data-stu-id="8a144-159">The **InstancesOf** method only works for class objects.</span></span>

<span data-ttu-id="8a144-160">De forma predeterminada, las instancias realizan una recuperación en profundidad.</span><span class="sxs-lookup"><span data-stu-id="8a144-160">By default, InstancesOf performs a deep retrieval.</span></span> <span data-ttu-id="8a144-161">Es decir, las instancias recuperan todas las instancias del recurso administrado que se identifican y todas las instancias de todas las subclases definidas bajo la clase de destino.</span><span class="sxs-lookup"><span data-stu-id="8a144-161">That is, InstancesOf retrieves all instances of the managed resource you identify and all instances of all the subclasses defined beneath the target class.</span></span> <span data-ttu-id="8a144-162">Por ejemplo, el siguiente script recupera todos los recursos modelados por todas las clases dinámicas definidas bajo la \_ clase abstracta del servicio CIM.</span><span class="sxs-lookup"><span data-stu-id="8a144-162">For example, the following script retrieves all of the resources modeled by all of the dynamic classes defined beneath the CIM\_Service abstract class.</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("CIM_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Object Path: " & objSWbemObject.Path_.Path
Next
```



<span data-ttu-id="8a144-163">Si ejecuta este script, volverá a obtener información.</span><span class="sxs-lookup"><span data-stu-id="8a144-163">If you run this script, you will get information back.</span></span> <span data-ttu-id="8a144-164">Sin embargo, esta información no se limitará a los servicios instalados en un equipo.</span><span class="sxs-lookup"><span data-stu-id="8a144-164">However, this information will not be limited to the services installed on a computer.</span></span> <span data-ttu-id="8a144-165">En su lugar, incluirá información de todas las clases secundarias del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service), incluido [**Win32 \_ SystemDriver**](/windows/desktop/CIMWin32Prov/win32-systemdriver) y [**Win32 \_ ApplicationService**](/previous-versions/windows/desktop/legacy/aa394068(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8a144-165">Instead, it will include information from all child classes of [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), including [**Win32\_SystemDriver**](/windows/desktop/CIMWin32Prov/win32-systemdriver) and [**Win32\_ApplicationService**](/previous-versions/windows/desktop/legacy/aa394068(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="8a144-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a144-166">Requirements</span></span>



| <span data-ttu-id="8a144-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a144-167">Requirement</span></span> | <span data-ttu-id="8a144-168">Value</span><span class="sxs-lookup"><span data-stu-id="8a144-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a144-169">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a144-169">Minimum supported client</span></span><br/> | <span data-ttu-id="8a144-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8a144-170">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8a144-171">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a144-171">Minimum supported server</span></span><br/> | <span data-ttu-id="8a144-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8a144-172">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8a144-173">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8a144-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a144-174"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a144-174"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8a144-175">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="8a144-175">Type library</span></span><br/>             | <dl> <span data-ttu-id="8a144-176"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8a144-176"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8a144-177">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8a144-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a144-178"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a144-178"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="8a144-179">CLSID</span><span class="sxs-lookup"><span data-stu-id="8a144-179">CLSID</span></span><br/>                    | <span data-ttu-id="8a144-180">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="8a144-180">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="8a144-181">IID</span><span class="sxs-lookup"><span data-stu-id="8a144-181">IID</span></span><br/>                      | <span data-ttu-id="8a144-182">\_ISWBEMSERVICES IID</span><span class="sxs-lookup"><span data-stu-id="8a144-182">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="8a144-183">Vea también</span><span class="sxs-lookup"><span data-stu-id="8a144-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a144-184">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="8a144-184">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="8a144-185">**SWbemObjectSet**</span><span class="sxs-lookup"><span data-stu-id="8a144-185">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> </dl>

 

