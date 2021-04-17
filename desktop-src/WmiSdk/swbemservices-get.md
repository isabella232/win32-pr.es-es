---
description: Recupera un objeto, que es una definición de clase o una instancia de, en función de la ruta de acceso del objeto.
ms.assetid: 3071aeb2-adab-47aa-a10c-9796766bb630
ms.tgt_platform: multiple
title: Método SWbemServices. get (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.Get
- ISWbemServices.Get
- ISWbemServices.Get
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c8998a1ca04206362fcc0e7405fccf8c923d74d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716194"
---
# <a name="swbemservicesget-method"></a><span data-ttu-id="df44e-103">SWbemServices. get (método)</span><span class="sxs-lookup"><span data-stu-id="df44e-103">SWbemServices.Get method</span></span>

<span data-ttu-id="df44e-104">El método **Get** del objeto [**SWbemServices**](swbemservices.md) recupera un objeto, que es una definición de clase o una instancia, en función de la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="df44e-104">The **Get** method of the [**SWbemServices**](swbemservices.md) object retrieves an object, that is either a class definition or an instance, based on the object path.</span></span> <span data-ttu-id="df44e-105">Este método solo recupera los objetos del espacio de nombres que está asociado al objeto **SWbemServices** actual.</span><span class="sxs-lookup"><span data-stu-id="df44e-105">This method retrieves only objects from the namespace that is associated with the current **SWbemServices** object.</span></span>

<span data-ttu-id="df44e-106">Se llama al método en el modo sincrónico.</span><span class="sxs-lookup"><span data-stu-id="df44e-106">The method is called in the synchronous mode.</span></span> <span data-ttu-id="df44e-107">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="df44e-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="df44e-108">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="df44e-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="df44e-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="df44e-109">Syntax</span></span>


```VB
objWbemObject = .Get( _
  [ ByVal strObjectPath ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="df44e-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="df44e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df44e-111">*strObjectPath* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="df44e-111">*strObjectPath* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="df44e-112">Cadena que contiene la ruta de acceso del objeto que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="df44e-112">String that contains the object path of the object to retrieve.</span></span> <span data-ttu-id="df44e-113">Si este valor está vacío, el objeto vacío que se devuelve puede convertirse en una nueva clase.</span><span class="sxs-lookup"><span data-stu-id="df44e-113">If this value is empty, the empty object that is returned can become a new class.</span></span> <span data-ttu-id="df44e-114">Para obtener más información, vea [Descripción de la ubicación de un objeto WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="df44e-114">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="df44e-115">*iFlags* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="df44e-115">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="df44e-116">Entero que determina el comportamiento de la consulta.</span><span class="sxs-lookup"><span data-stu-id="df44e-116">Integer that determines the behavior of the query.</span></span> <span data-ttu-id="df44e-117">Este parámetro puede aceptar los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="df44e-117">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="df44e-118"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="df44e-118"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="df44e-119">Hace que WMI devuelva datos de modificación de clase con la definición de clase base.</span><span class="sxs-lookup"><span data-stu-id="df44e-119">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="df44e-120">Para obtener más información acerca de los calificadores modificados, consulte [localizar información de clase WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="df44e-120">For more information about amended qualifiers, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="df44e-121">*objWbemNamedValueSet* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="df44e-121">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="df44e-122">Normalmente, esto no está definido.</span><span class="sxs-lookup"><span data-stu-id="df44e-122">Typically, this is undefined.</span></span> <span data-ttu-id="df44e-123">De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que atiende la solicitud.</span><span class="sxs-lookup"><span data-stu-id="df44e-123">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="df44e-124">Un proveedor que admite o requiere tal información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.</span><span class="sxs-lookup"><span data-stu-id="df44e-124">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df44e-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="df44e-125">Return value</span></span>

<span data-ttu-id="df44e-126">Si es correcto, este método devuelve un objeto [**SWbemObject**](swbemobject.md) que representa el objeto solicitado.</span><span class="sxs-lookup"><span data-stu-id="df44e-126">If successful, this method returns an [**SWbemObject**](swbemobject.md) object that represents the requested object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="df44e-127">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="df44e-127">Error codes</span></span>

<span data-ttu-id="df44e-128">Una vez finalizado el método **Get** , el objeto **Err** puede contener uno de los códigos de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="df44e-128">Upon the completion of the **Get** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="df44e-129">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="df44e-129">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="df44e-130">El usuario actual no tiene permiso para obtener acceso al objeto.</span><span class="sxs-lookup"><span data-stu-id="df44e-130">Current user does not have the permission to access the object.</span></span>

</dd> <dt>

<span data-ttu-id="df44e-131">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="df44e-131">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="df44e-132">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="df44e-132">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="df44e-133">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="df44e-133">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="df44e-134">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="df44e-134">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="df44e-135">**wbemErrInvalidObjectPath** -2147749946 (0x8004103A)</span><span class="sxs-lookup"><span data-stu-id="df44e-135">**wbemErrInvalidObjectPath** - 2147749946 (0x8004103A)</span></span>
</dt> <dd>

<span data-ttu-id="df44e-136">La ruta de acceso especificada no era válida.</span><span class="sxs-lookup"><span data-stu-id="df44e-136">Specified path was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="df44e-137">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="df44e-137">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="df44e-138">No se encontró el objeto solicitado.</span><span class="sxs-lookup"><span data-stu-id="df44e-138">Requested object could not be found.</span></span>

</dd> <dt>

<span data-ttu-id="df44e-139">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="df44e-139">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="df44e-140">Memoria insuficiente para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="df44e-140">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="df44e-141">Observaciones</span><span class="sxs-lookup"><span data-stu-id="df44e-141">Remarks</span></span>

<span data-ttu-id="df44e-142">A diferencia de [**los métodos**](swbemservices-instancesof.md) [**ExecQuery**](/windows/desktop/api/Provider/nf-provider-provider-execquery) e instanceof, el método get siempre devuelve un [**SWbemObject**](swbemobject.md) que representa una instancia específica de un recurso administrado por WMI.</span><span class="sxs-lookup"><span data-stu-id="df44e-142">Unlike the [**ExecQuery**](/windows/desktop/api/Provider/nf-provider-provider-execquery) and [**InstancesOf**](swbemservices-instancesof.md) methods, the Get method always returns an [**SWbemObject**](swbemobject.md) representing a specific instance of a WMI-managed resource.</span></span> <span data-ttu-id="df44e-143">Para obtener una instancia específica de un recurso administrado por WMI mediante el método get, debe indicar a get la instancia que se va a recuperar pasando el método a la ruta de acceso del objeto, tal como se muestra en el script siguiente.</span><span class="sxs-lookup"><span data-stu-id="df44e-143">To obtain a specific instance of a WMI-managed resource using the Get method, you must tell Get the instance to retrieve by passing the method the object path, as shown in the following script.</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set objSWbemObject = objSWbemServices.Get("Win32_Service.Name='Messenger'")
Wscript.Echo "Name:         " & objSWbemObject.Name        & vbCrLf & _
             "Display Name: " & objSWbemObject.DisplayName & vbCrLf & _
             "Start Mode:   " & objSWbemObject.StartMode   & vbCrLf & _
             "State:        " & objSWbemObject.State
```



<span data-ttu-id="df44e-144">Puede utilizar este método para obtener objetos [*Singleton*](gloss-s.md) , como [**\_ \_ CIMOMIdentification**](--cimomidentification.md), que contiene información de versión sobre la instalación de WMI que se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="df44e-144">You can use this method to obtain [*singleton*](gloss-s.md) objects, such as [**\_\_CIMOMIdentification**](--cimomidentification.md), which contains version information about the WMI installation that is running.</span></span>

<span data-ttu-id="df44e-145">Puede examinar el repositorio con una herramienta de visualización como [CIM Studio](further-information.md) para comprobar que aparece la nueva clase e instancia.</span><span class="sxs-lookup"><span data-stu-id="df44e-145">You can examine the repository with a viewing tool such as [CIM Studio](further-information.md) to verify that the new class and instance appear.</span></span> <span data-ttu-id="df44e-146">Para obtener un ejemplo de cómo quitar una clase y una instancia del repositorio, vea [**SWbemServices. Delete**](swbemservices-delete.md) o [**SWbemObject \_ . Delete**](swbemobject-delete-.md).</span><span class="sxs-lookup"><span data-stu-id="df44e-146">For an example of removing a class and instance from the repository, see [**SWbemServices.Delete**](swbemservices-delete.md) or [**SWbemObject.Delete\_**](swbemobject-delete-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="df44e-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df44e-147">Requirements</span></span>



| <span data-ttu-id="df44e-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="df44e-148">Requirement</span></span> | <span data-ttu-id="df44e-149">Value</span><span class="sxs-lookup"><span data-stu-id="df44e-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="df44e-150">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="df44e-150">Minimum supported client</span></span><br/> | <span data-ttu-id="df44e-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="df44e-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="df44e-152">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="df44e-152">Minimum supported server</span></span><br/> | <span data-ttu-id="df44e-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="df44e-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="df44e-154">Encabezado</span><span class="sxs-lookup"><span data-stu-id="df44e-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="df44e-155"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="df44e-155"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="df44e-156">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="df44e-156">Type library</span></span><br/>             | <dl> <span data-ttu-id="df44e-157"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="df44e-157"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="df44e-158">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="df44e-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df44e-159"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df44e-159"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="df44e-160">CLSID</span><span class="sxs-lookup"><span data-stu-id="df44e-160">CLSID</span></span><br/>                    | <span data-ttu-id="df44e-161">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="df44e-161">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="df44e-162">IID</span><span class="sxs-lookup"><span data-stu-id="df44e-162">IID</span></span><br/>                      | <span data-ttu-id="df44e-163">\_ISWBEMSERVICES IID</span><span class="sxs-lookup"><span data-stu-id="df44e-163">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="df44e-164">Vea también</span><span class="sxs-lookup"><span data-stu-id="df44e-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df44e-165">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="df44e-165">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="df44e-166">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="df44e-166">**SWbemObject**</span></span>](swbemobject.md)
</dt> </dl>

 

 




