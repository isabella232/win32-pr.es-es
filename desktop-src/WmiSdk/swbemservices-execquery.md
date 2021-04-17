---
description: Ejecuta una consulta para recuperar objetos.
ms.assetid: 06b9d4c9-cd72-49b2-92b0-d18d94dfbd9f
ms.tgt_platform: multiple
title: SWbemServices.Exemétodo cQuery (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecQuery
- ISWbemServices.ExecQuery
- ISWbemServices.ExecQuery
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2f3a894681bafc71de34ae7722b985494ef80b4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716195"
---
# <a name="swbemservicesexecquery-method"></a><span data-ttu-id="cbda8-103">SWbemServices.Exemétodo cQuery</span><span class="sxs-lookup"><span data-stu-id="cbda8-103">SWbemServices.ExecQuery method</span></span>

<span data-ttu-id="cbda8-104">El método **ExecQuery** del objeto [**SWbemServices**](swbemservices.md) ejecuta una consulta para recuperar objetos.</span><span class="sxs-lookup"><span data-stu-id="cbda8-104">The **ExecQuery** method of the [**SWbemServices**](swbemservices.md) object executes a query to retrieve objects.</span></span> <span data-ttu-id="cbda8-105">Estos objetos están disponibles a través de la colección [**SWbemObjectSet**](swbemobjectset.md) devuelta.</span><span class="sxs-lookup"><span data-stu-id="cbda8-105">These objects are available through the returned [**SWbemObjectSet**](swbemobjectset.md) collection.</span></span>

<span data-ttu-id="cbda8-106">Se llama a este método en el modo semisincrónico.</span><span class="sxs-lookup"><span data-stu-id="cbda8-106">This method is called in the semisynchronous mode.</span></span> <span data-ttu-id="cbda8-107">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="cbda8-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="cbda8-108">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="cbda8-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="cbda8-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cbda8-109">Syntax</span></span>


```VB
objWbemObjectSet = .ExecQuery( _
  ByVal strQuery, _
  [ ByVal strQueryLanguage ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="cbda8-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cbda8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbda8-111">*strQuery*</span><span class="sxs-lookup"><span data-stu-id="cbda8-111">*strQuery*</span></span> 
</dt> <dd>

<span data-ttu-id="cbda8-112">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="cbda8-112">Required.</span></span> <span data-ttu-id="cbda8-113">Cadena que contiene el texto de la consulta.</span><span class="sxs-lookup"><span data-stu-id="cbda8-113">String that contains the text of the query.</span></span> <span data-ttu-id="cbda8-114">Este parámetro no puede estar en blanco.</span><span class="sxs-lookup"><span data-stu-id="cbda8-114">This parameter cannot be blank.</span></span> <span data-ttu-id="cbda8-115">Para obtener más información sobre la creación de cadenas de consulta de WMI, vea [consultas con WQL](querying-with-wql.md) y la referencia de [WQL](wql-sql-for-wmi.md) .</span><span class="sxs-lookup"><span data-stu-id="cbda8-115">For more information on building WMI query strings, see [Querying with WQL](querying-with-wql.md) and the [WQL](wql-sql-for-wmi.md) reference.</span></span>

</dd> <dt>

<span data-ttu-id="cbda8-116">*strQueryLanguage* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="cbda8-116">*strQueryLanguage* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cbda8-117">Cadena que contiene el lenguaje de consulta que se va a utilizar.</span><span class="sxs-lookup"><span data-stu-id="cbda8-117">String that contains the query language to be used.</span></span> <span data-ttu-id="cbda8-118">Si se especifica, este valor debe ser "WQL".</span><span class="sxs-lookup"><span data-stu-id="cbda8-118">If specified, this value must be "WQL".</span></span>

</dd> <dt>

<span data-ttu-id="cbda8-119">*iFlags* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="cbda8-119">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cbda8-120">Entero que determina el comportamiento de la consulta y determina si esta llamada se devuelve inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="cbda8-120">Integer that determines the behavior of the query and determines whether this call returns immediately.</span></span> <span data-ttu-id="cbda8-121">El valor predeterminado de este parámetro es **wbemFlagReturnImmediately**.</span><span class="sxs-lookup"><span data-stu-id="cbda8-121">The default value for this parameter is **wbemFlagReturnImmediately**.</span></span> <span data-ttu-id="cbda8-122">Este parámetro puede aceptar los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="cbda8-122">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="cbda8-123"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="cbda8-123"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="cbda8-124">Hace que se devuelva un enumerador de solo avance.</span><span class="sxs-lookup"><span data-stu-id="cbda8-124">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="cbda8-125">Los enumeradores de solo avance suelen ser mucho más rápidos y usan menos memoria que los enumeradores convencionales, pero no permiten llamadas a [**SWbemObject. \_ Clone**](swbemobject-clone-.md).</span><span class="sxs-lookup"><span data-stu-id="cbda8-125">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span data-ttu-id="cbda8-126"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional \* \* \* \* (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="cbda8-126"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>\*\*\*\*wbemFlagBidirectional\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="cbda8-127">Hace que WMI conserve punteros a objetos de la enumeración hasta que el cliente libere el enumerador.</span><span class="sxs-lookup"><span data-stu-id="cbda8-127">Causes WMI to retain pointers to objects of the enumeration until the client releases the enumerator.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="cbda8-128"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="cbda8-128"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="cbda8-129">Hace que la llamada se devuelva inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="cbda8-129">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="cbda8-130"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* \* (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="cbda8-130"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="cbda8-131">Hace que esta llamada se bloquee hasta que se complete la consulta.</span><span class="sxs-lookup"><span data-stu-id="cbda8-131">Causes this call to block until the query is complete.</span></span> <span data-ttu-id="cbda8-132">Esta marca llama al método en el modo sincrónico.</span><span class="sxs-lookup"><span data-stu-id="cbda8-132">This flag calls the method in the synchronous mode.</span></span>

</dd> <dt>

<span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>

<span data-ttu-id="cbda8-133"><span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>wbemQueryFlagPrototype \* \* \* \* (2 (0X2))</span><span class="sxs-lookup"><span data-stu-id="cbda8-133"><span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>\*\*\*\*wbemQueryFlagPrototype\*\*\*\* (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="cbda8-134">Se usa para la prototipo.</span><span class="sxs-lookup"><span data-stu-id="cbda8-134">Used for prototyping.</span></span> <span data-ttu-id="cbda8-135">Esta marca evita que se produzca la consulta y devuelve un objeto que parece un objeto de resultado típico.</span><span class="sxs-lookup"><span data-stu-id="cbda8-135">This flag stops the query from happening and returns an object that looks like a typical result object.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="cbda8-136"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="cbda8-136"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="cbda8-137">Hace que WMI devuelva datos de modificación de clase con la definición de clase base.</span><span class="sxs-lookup"><span data-stu-id="cbda8-137">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="cbda8-138">Para obtener más información, consulte [localizar información de clase WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="cbda8-138">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="cbda8-139">*objWbemNamedValueSet* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="cbda8-139">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cbda8-140">Normalmente, esto no está definido.</span><span class="sxs-lookup"><span data-stu-id="cbda8-140">Typically, this is undefined.</span></span> <span data-ttu-id="cbda8-141">De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que atiende la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cbda8-141">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="cbda8-142">Un proveedor que admite o requiere tal información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.</span><span class="sxs-lookup"><span data-stu-id="cbda8-142">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbda8-143">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cbda8-143">Return value</span></span>

<span data-ttu-id="cbda8-144">Si no se produce ningún error, este método devuelve un objeto [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="cbda8-144">If no error occurs, this method returns an [**SWbemObjectSet**](swbemobjectset.md) object.</span></span> <span data-ttu-id="cbda8-145">Se trata de una colección de objetos que contiene el conjunto de resultados de la consulta.</span><span class="sxs-lookup"><span data-stu-id="cbda8-145">This is an object collection that contains the result set of the query.</span></span> <span data-ttu-id="cbda8-146">El autor de la llamada puede examinar la colección utilizando la implementación de colecciones para el lenguaje de programación que está usando.</span><span class="sxs-lookup"><span data-stu-id="cbda8-146">The caller can examine the collection using the implementation of collections for the programming language you are using.</span></span> <span data-ttu-id="cbda8-147">Para obtener más información, vea [obtener acceso a una colección](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="cbda8-147">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="cbda8-148">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="cbda8-148">Error codes</span></span>

<span data-ttu-id="cbda8-149">Después de completar el método **ExecQuery** , el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener uno de los códigos de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="cbda8-149">After the completion of the **ExecQuery** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object can contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="cbda8-150">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="cbda8-150">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="cbda8-151">El usuario actual no tiene permiso para ver el conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="cbda8-151">Current user does not have the permission to view the result set.</span></span>

</dd> <dt>

<span data-ttu-id="cbda8-152">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="cbda8-152">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="cbda8-153">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="cbda8-153">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="cbda8-154">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="cbda8-154">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="cbda8-155">Se especificó un parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="cbda8-155">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="cbda8-156">**wbemErrInvalidQuery** -2147749911 (0x80041017)</span><span class="sxs-lookup"><span data-stu-id="cbda8-156">**wbemErrInvalidQuery** - 2147749911 (0x80041017)</span></span>
</dt> <dd>

<span data-ttu-id="cbda8-157">La sintaxis de la consulta no es válida.</span><span class="sxs-lookup"><span data-stu-id="cbda8-157">Query syntax is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="cbda8-158">**wbemErrInvalidQueryType** -2147749912 (0x80041018)</span><span class="sxs-lookup"><span data-stu-id="cbda8-158">**wbemErrInvalidQueryType** - 2147749912 (0x80041018)</span></span>
</dt> <dd>

<span data-ttu-id="cbda8-159">No se admite el lenguaje de consulta solicitado.</span><span class="sxs-lookup"><span data-stu-id="cbda8-159">Requested query language is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="cbda8-160">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="cbda8-160">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="cbda8-161">Memoria insuficiente para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="cbda8-161">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cbda8-162">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cbda8-162">Remarks</span></span>

<span data-ttu-id="cbda8-163">**ExecQuery** es una de las llamadas más utilizadas para recuperar información de WMI.</span><span class="sxs-lookup"><span data-stu-id="cbda8-163">**ExecQuery** is one of the most commonly-used calls to retrieve WMI information.</span></span> <span data-ttu-id="cbda8-164">Una llamada estándar a **ExecQuery** es similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="cbda8-164">A standard call to **ExecQuery** looks like the following:</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colServices = objWMIService.ExecQuery ("Select * from Win32_Service where Name='Alerter'")
For Each objService in colServices
    Return = objService.StopService()
    If Return <> 0 Then
        Wscript.Echo "Failed " &VBNewLine & "Error code = " & Return 
    Else
       WScript.Echo "Succeeded"
    End If
Next
```



<span data-ttu-id="cbda8-165">Tenga en cuenta que crea el objeto [**SWbemServices**](swbemservices.md) con un moniker que representa el espacio de nombres y la seguridad adecuados y, a continuación, realiza la llamada **ExecQuery** a través del servicio.</span><span class="sxs-lookup"><span data-stu-id="cbda8-165">Note that you create the [**SWbemServices**](swbemservices.md) object with a moniker that represents the appropriate namespace and security, then make the **ExecQuery** call through the service.</span></span> <span data-ttu-id="cbda8-166">Para obtener una explicación más completa, consulte [creación de un script de WMI](creating-a-wmi-script.md) y [enumeración de WMI](enumerating-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="cbda8-166">For a more complete discussion, see [Creating a WMI Script](creating-a-wmi-script.md) and [Enumerating WMI](enumerating-wmi.md).</span></span>

<span data-ttu-id="cbda8-167">Al igual que el método [**instances**](swbemservices-instancesof.md) , el método **ExecQuery** siempre devuelve una colección [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="cbda8-167">Like the [**InstancesOf**](swbemservices-instancesof.md) method, the **ExecQuery** method always returns an [**SWbemObjectSet**](swbemobjectset.md) collection.</span></span> <span data-ttu-id="cbda8-168">Por lo tanto, el script de WMI debe enumerar la colección ExecQuery devuelve para tener acceso a cada instancia de recurso administrada en la colección, como se muestra aquí:</span><span class="sxs-lookup"><span data-stu-id="cbda8-168">Thus your WMI script must enumerate the collection ExecQuery returns in order to access each managed resource instance in the collection, as shown here:</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.ExecQuery _
   ("SELECT * FROM Win32_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Name: " & objSWbemObject.Name
Next
```



<span data-ttu-id="cbda8-169">Otros métodos de [**SWbemServices**](swbemservices.md) que devuelven [**SWbemObjectSet**](swbemobjectset.md) incluyen [**AssociatorsOf**](swbemservices-associatorsof.md), [**References**](swbemservices-referencesto.md)y [**subclasses**](swbemservices-subclassesof.md).</span><span class="sxs-lookup"><span data-stu-id="cbda8-169">Other [**SWbemServices**](swbemservices.md) methods that return an [**SWbemObjectSet**](swbemobjectset.md) include [**AssociatorsOf**](swbemservices-associatorsof.md), [**ReferencesTo**](swbemservices-referencesto.md), and [**SubclassesOf**](swbemservices-subclassesof.md).</span></span>

<span data-ttu-id="cbda8-170">No es un error que la consulta devuelva un conjunto de resultados vacío.</span><span class="sxs-lookup"><span data-stu-id="cbda8-170">It is not an error for the query to return an empty result set.</span></span> <span data-ttu-id="cbda8-171">El método **ExecQuery** devuelve propiedades de clave tanto si se solicita la propiedad de clave como si no en el argumento *strQuery* .</span><span class="sxs-lookup"><span data-stu-id="cbda8-171">The **ExecQuery** method returns key properties whether or not the key property is requested in the *strQuery* argument.</span></span> <span data-ttu-id="cbda8-172">Si se produce un error al ejecutar este método y no se usa la marca **wbemFlagReturnImmediately** , el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) no se establece hasta que se intenta obtener acceso al conjunto de objetos devueltos.</span><span class="sxs-lookup"><span data-stu-id="cbda8-172">If an error occurs when executing this method and you do not use the **wbemFlagReturnImmediately** flag, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object is not set until you attempt to access the returned object set.</span></span> <span data-ttu-id="cbda8-173">Sin embargo, si usa la marca **wbemFlagReturnWhenComplete** , el objeto Err se establece cuando se llama al método **ExecQuery** .</span><span class="sxs-lookup"><span data-stu-id="cbda8-173">However, if you use the **wbemFlagReturnWhenComplete** flag, the Err object is set when the **ExecQuery** method is called.</span></span>

<span data-ttu-id="cbda8-174">Hay límites en el número de palabras clave **and** y **or** que se pueden usar en las consultas WQL.</span><span class="sxs-lookup"><span data-stu-id="cbda8-174">There are limits to the number of **AND** and **OR** keywords that can be used in WQL queries.</span></span> <span data-ttu-id="cbda8-175">Un gran número de palabras clave WQL que se usan en una consulta compleja puede hacer que WMI devuelva el código de error de **\_ \_ \_ infracción de la cuota de WBEM E** como un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cbda8-175">Large numbers of WQL keywords that are used in a complex query can cause WMI to return the **WBEM\_E\_QUOTA\_VIOLATION** error code as an **HRESULT** value.</span></span> <span data-ttu-id="cbda8-176">El límite de palabras clave de WQL depende de la complejidad de la consulta.</span><span class="sxs-lookup"><span data-stu-id="cbda8-176">The limit of WQL keywords depends on how complex the query is.</span></span>

## <a name="examples"></a><span data-ttu-id="cbda8-177">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="cbda8-177">Examples</span></span>

<span data-ttu-id="cbda8-178">En el siguiente ejemplo de código de VBScript se buscan todas las unidades de disco en el equipo local y se muestra el identificador de dispositivo y el tipo de la unidad de disco.</span><span class="sxs-lookup"><span data-stu-id="cbda8-178">The following VBScript code example locates all the disk drives on the local computer and displays the device ID and the type of the disk drive.</span></span>


```VB
Set colDisks = GetObject( _
    "Winmgmts:").ExecQuery("Select * from Win32_LogicalDisk")
For Each objDisk in colDisks
 
    Select Case objDisk.DriveType
        Case 1
            Wscript.Echo "No root directory. Drive type could not be determined."
        Case 2
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Removable drive" 
        Case 3
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Local hard disk" 
        Case 4
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Network disk" 
        Case 5
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Compact disk" 
        Case 6
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = RAM disk" 
        Case Else
            Wscript.Echo "Drive type could not be determined."
    End Select
Next
```



## <a name="requirements"></a><span data-ttu-id="cbda8-179">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cbda8-179">Requirements</span></span>



| <span data-ttu-id="cbda8-180">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbda8-180">Requirement</span></span> | <span data-ttu-id="cbda8-181">Value</span><span class="sxs-lookup"><span data-stu-id="cbda8-181">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cbda8-182">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cbda8-182">Minimum supported client</span></span><br/> | <span data-ttu-id="cbda8-183">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cbda8-183">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cbda8-184">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cbda8-184">Minimum supported server</span></span><br/> | <span data-ttu-id="cbda8-185">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cbda8-185">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cbda8-186">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cbda8-186">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbda8-187"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbda8-187"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="cbda8-188">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="cbda8-188">Type library</span></span><br/>             | <dl> <span data-ttu-id="cbda8-189"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="cbda8-189"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="cbda8-190">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cbda8-190">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cbda8-191"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cbda8-191"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="cbda8-192">CLSID</span><span class="sxs-lookup"><span data-stu-id="cbda8-192">CLSID</span></span><br/>                    | <span data-ttu-id="cbda8-193">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="cbda8-193">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="cbda8-194">IID</span><span class="sxs-lookup"><span data-stu-id="cbda8-194">IID</span></span><br/>                      | <span data-ttu-id="cbda8-195">\_ISWBEMSERVICES IID</span><span class="sxs-lookup"><span data-stu-id="cbda8-195">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="cbda8-196">Vea también</span><span class="sxs-lookup"><span data-stu-id="cbda8-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbda8-197">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="cbda8-197">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="cbda8-198">**SWbemServices. get**</span><span class="sxs-lookup"><span data-stu-id="cbda8-198">**SWbemServices.Get**</span></span>](swbemservices-get.md)
</dt> <dt>

[<span data-ttu-id="cbda8-199">Realizar consultas con WQL</span><span class="sxs-lookup"><span data-stu-id="cbda8-199">Querying with WQL</span></span>](querying-with-wql.md)
</dt> <dt>

[<span data-ttu-id="cbda8-200">Creación de un script de WMI</span><span class="sxs-lookup"><span data-stu-id="cbda8-200">Creating a WMI Script</span></span>](creating-a-wmi-script.md)
</dt> <dt>

[<span data-ttu-id="cbda8-201">Enumerar WMI</span><span class="sxs-lookup"><span data-stu-id="cbda8-201">Enumerating WMI</span></span>](enumerating-wmi.md)
</dt> </dl>

 

