---
description: 'SWbemServices.Exemétodo cMethod: ejecuta un método exportado por un proveedor de métodos.'
ms.assetid: 2637efdc-fde5-4a44-a41f-67e0fb0df19d
ms.tgt_platform: multiple
title: SWbemServices.Exemétodo cMethod (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecMethod
- ISWbemServices.ExecMethod
- ISWbemServices.ExecMethod
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 452c42c37e8dcb9f2b37b660b1f8899e587b5579
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103643"
---
# <a name="swbemservicesexecmethod-method"></a><span data-ttu-id="7dd45-103">SWbemServices.Exemétodo cMethod</span><span class="sxs-lookup"><span data-stu-id="7dd45-103">SWbemServices.ExecMethod method</span></span>

<span data-ttu-id="7dd45-104">El **método ExecMethod** del objeto [**SWbemServices**](swbemservices.md) ejecuta un método exportado por un proveedor de métodos.</span><span class="sxs-lookup"><span data-stu-id="7dd45-104">The **ExecMethod** method of the [**SWbemServices**](swbemservices.md) object executes a method that is exported by a method provider.</span></span> <span data-ttu-id="7dd45-105">Este método se bloquea mientras se ejecuta el método que se reenvía al proveedor adecuado.</span><span class="sxs-lookup"><span data-stu-id="7dd45-105">This method blocks while the method that is forwarded to the appropriate provider executes.</span></span> <span data-ttu-id="7dd45-106">A continuación, se devuelve la información y el estado.</span><span class="sxs-lookup"><span data-stu-id="7dd45-106">The information and status are then returned.</span></span> <span data-ttu-id="7dd45-107">El proveedor, en lugar de WMI, implementa el método .</span><span class="sxs-lookup"><span data-stu-id="7dd45-107">The provider, rather than WMI, implements the method.</span></span>

<span data-ttu-id="7dd45-108">Se llama a este método en modo sincrónico.</span><span class="sxs-lookup"><span data-stu-id="7dd45-108">This method is called in the synchronous mode.</span></span> <span data-ttu-id="7dd45-109">Para obtener más información, vea [Llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="7dd45-109">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="7dd45-110">Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="7dd45-110">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7dd45-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7dd45-111">Syntax</span></span>


```VB
objOutParams = .ExecMethod( _
  ByVal strObjectPath, _
  ByVal strMethodName, _
  [ ByVal objWbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="7dd45-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7dd45-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7dd45-113">*strObjectPath*</span><span class="sxs-lookup"><span data-stu-id="7dd45-113">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="7dd45-114">Necesario.</span><span class="sxs-lookup"><span data-stu-id="7dd45-114">Required.</span></span> <span data-ttu-id="7dd45-115">Cadena que contiene la ruta de acceso del objeto para el que se ejecuta el método.</span><span class="sxs-lookup"><span data-stu-id="7dd45-115">String that contains the object path of the object for which the method is executed.</span></span> <span data-ttu-id="7dd45-116">Para obtener más información, [vea Describir la ubicación de un objeto WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="7dd45-116">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="7dd45-117">*strMethodName*</span><span class="sxs-lookup"><span data-stu-id="7dd45-117">*strMethodName*</span></span> 
</dt> <dd>

<span data-ttu-id="7dd45-118">Necesario.</span><span class="sxs-lookup"><span data-stu-id="7dd45-118">Required.</span></span> <span data-ttu-id="7dd45-119">Nombre del método para el objeto .</span><span class="sxs-lookup"><span data-stu-id="7dd45-119">Name of the method for the object.</span></span>

</dd> <dt>

<span data-ttu-id="7dd45-120">*objWbemInParams* \[ Opcional\]</span><span class="sxs-lookup"><span data-stu-id="7dd45-120">*objWbemInParams* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7dd45-121">Objeto [**SWbemObject**](swbemobject.md) que contiene los parámetros de entrada para el método que se ejecuta.</span><span class="sxs-lookup"><span data-stu-id="7dd45-121">An [**SWbemObject**](swbemobject.md) object that contains the input parameters for the method being executed.</span></span> <span data-ttu-id="7dd45-122">De forma predeterminada, este parámetro no está definido.</span><span class="sxs-lookup"><span data-stu-id="7dd45-122">By default, this parameter is undefined.</span></span> <span data-ttu-id="7dd45-123">Para obtener más información, [vea Construir objetos InParameters y Analizar objetos OutParameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="7dd45-123">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="7dd45-124">*iFlags* \[ Opcional\]</span><span class="sxs-lookup"><span data-stu-id="7dd45-124">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7dd45-125">Reservado.</span><span class="sxs-lookup"><span data-stu-id="7dd45-125">Reserved.</span></span> <span data-ttu-id="7dd45-126">Este valor debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="7dd45-126">This value must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="7dd45-127">*objWbemNamedValueSet* \[ Opcional\]</span><span class="sxs-lookup"><span data-stu-id="7dd45-127">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7dd45-128">Normalmente, esto no está definido.</span><span class="sxs-lookup"><span data-stu-id="7dd45-128">Typically, this is undefined.</span></span> <span data-ttu-id="7dd45-129">De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que está atendiendo la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7dd45-129">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="7dd45-130">Un proveedor que admita o requiera dicha información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.</span><span class="sxs-lookup"><span data-stu-id="7dd45-130">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7dd45-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7dd45-131">Return value</span></span>

<span data-ttu-id="7dd45-132">Si el método es correcto, se [**devuelve un objeto SWbemObject.**](swbemobject.md)</span><span class="sxs-lookup"><span data-stu-id="7dd45-132">If the method is successful, an [**SWbemObject**](swbemobject.md) object is returned.</span></span> <span data-ttu-id="7dd45-133">El objeto devuelto contiene los parámetros out y el valor devuelto para el método que se ejecuta.</span><span class="sxs-lookup"><span data-stu-id="7dd45-133">The returned object contains the out parameters and return value for the method that is being executed.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7dd45-134">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="7dd45-134">Error codes</span></span>

<span data-ttu-id="7dd45-135">Después de completar el método **ExecMethod,** el **objeto Err** puede contener uno de los códigos de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="7dd45-135">After the completion of the **ExecMethod** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="7dd45-136">**wbemErrFailed:** 2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="7dd45-136">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="7dd45-137">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="7dd45-137">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="7dd45-138">**wbemErrInvalidClass:** 2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="7dd45-138">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="7dd45-139">La clase especificada no era válida.</span><span class="sxs-lookup"><span data-stu-id="7dd45-139">Specified class was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="7dd45-140">**wbemErrInvalidParameter:** 2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="7dd45-140">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="7dd45-141">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="7dd45-141">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="7dd45-142">**wbemErrOutOfMemory:** 2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="7dd45-142">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="7dd45-143">No hay suficiente memoria para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="7dd45-143">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="7dd45-144">**wbemErrInvalidMethod:** 2147749934 (0x8004102E)</span><span class="sxs-lookup"><span data-stu-id="7dd45-144">**wbemErrInvalidMethod** - 2147749934 (0x8004102E)</span></span>
</dt> <dd>

<span data-ttu-id="7dd45-145">El método solicitado no estaba disponible.</span><span class="sxs-lookup"><span data-stu-id="7dd45-145">Requested method was not available.</span></span>

</dd> <dt>

<span data-ttu-id="7dd45-146">**wbemErrAccessDenied:** 2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="7dd45-146">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="7dd45-147">El usuario actual no estaba autorizado para ejecutar el método .</span><span class="sxs-lookup"><span data-stu-id="7dd45-147">Current user was not authorized to execute the method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7dd45-148">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7dd45-148">Remarks</span></span>

<span data-ttu-id="7dd45-149">Use **SWbemServices.ExecMethod** como alternativa al acceso directo [](gloss-p.md) para ejecutar un método de proveedor en casos en los que no sea posible ejecutar un método directamente.</span><span class="sxs-lookup"><span data-stu-id="7dd45-149">Use **SWbemServices.ExecMethod** as an alternative to direct access for executing a [*provider method*](gloss-p.md) in cases where it is not possible to execute a method directly.</span></span> <span data-ttu-id="7dd45-150">El **método ExecMethod** permite obtener parámetros de salida, si el proveedor los proporciona, con un lenguaje de scripting que no admite parámetros de salida.</span><span class="sxs-lookup"><span data-stu-id="7dd45-150">The **ExecMethod** method allows you to obtain output parameters, if the provider supplies them, with a scripting language that does not support output parameters.</span></span> <span data-ttu-id="7dd45-151">De lo contrario, el medio recomendado para invocar un método es usar el acceso directo.</span><span class="sxs-lookup"><span data-stu-id="7dd45-151">Otherwise, the recommended means of invoking a method is to use direct access.</span></span> <span data-ttu-id="7dd45-152">Para obtener más información, vea [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="7dd45-152">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

<span data-ttu-id="7dd45-153">Por ejemplo, el siguiente ejemplo de código que llama al [**método de proveedor StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) en el servicio [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-service) usa acceso directo.</span><span class="sxs-lookup"><span data-stu-id="7dd45-153">For example, the following code example that calls the [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) provider method in [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) uses direct access.</span></span>


```VB
oService = GetObject("winmgmts:Win32_Service=Alerter")
iStatus = oService.StartService()
```



<span data-ttu-id="7dd45-154">En este ejemplo **seSWbemServices.ExecMethod para** ejecutar el método [**StartService.**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service)</span><span class="sxs-lookup"><span data-stu-id="7dd45-154">This example calls **SWbemServices.ExecMethod** to execute the [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) method.</span></span> <span data-ttu-id="7dd45-155">Tenga en cuenta que se requiere una ruta de acceso de objeto **porqueSWbemServices.ExecMethod** no funciona en el objeto, a diferencia [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md).</span><span class="sxs-lookup"><span data-stu-id="7dd45-155">Note that an object path is required because **SWbemServices.ExecMethod** is not operating on the object already, unlike [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md).</span></span>


```VB
Set WbemServices = GetObject("winmgmts:")
Set oService = GetObject("winmgmts:Win32_Service='Alerter'")
Set oPath = GetObject("winmgmts:Win32_Service='Alerter'").Path_
WbemServices.ExecMethod oPath, "StartService"
```



<span data-ttu-id="7dd45-156">El **SWbemServices.Exemétodo cMethod** requiere una ruta de acceso de objeto.</span><span class="sxs-lookup"><span data-stu-id="7dd45-156">The **SWbemServices.ExecMethod** method requires an object path.</span></span> <span data-ttu-id="7dd45-157">Si el script ya contiene un [**objeto SWbemObject,**](swbemobject.md) use elSWbemObject.Exe [**método cMethod.**](swbemobject-execmethod-.md)</span><span class="sxs-lookup"><span data-stu-id="7dd45-157">If the script already holds an [**SWbemObject**](swbemobject.md) object, use the [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="7dd45-158">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="7dd45-158">Examples</span></span>

<span data-ttu-id="7dd45-159">En el ejemplo siguiente se muestra **el método ExecMethod.**</span><span class="sxs-lookup"><span data-stu-id="7dd45-159">The following example shows the **ExecMethod** method.</span></span> <span data-ttu-id="7dd45-160">El script crea un [**objeto Process \_ de Win32**](/windows/desktop/CIMWin32Prov/win32-process) que representa un proceso que ejecuta el Bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="7dd45-160">The script creates a [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) object that represents a process that is running Notepad.</span></span> <span data-ttu-id="7dd45-161">Muestra la configuración de un objeto [**InParameters**](swbemmethod-inparameters.md) y cómo obtener resultados de un [**objeto OutParameters.**](swbemmethod-outparameters.md)</span><span class="sxs-lookup"><span data-stu-id="7dd45-161">It shows the setting up of an [**InParameters**](swbemmethod-inparameters.md) object and how to obtain results from an [**OutParameters**](swbemmethod-outparameters.md) object.</span></span> <span data-ttu-id="7dd45-162">Para obtener un script que muestre las mismas operaciones realizadas de forma asincrónica, [**veaSWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md).</span><span class="sxs-lookup"><span data-stu-id="7dd45-162">For a script that shows the same operations performed asynchronously, see [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md).</span></span> <span data-ttu-id="7dd45-163">Para obtener un ejemplo del uso del acceso directo, vea [Create Method in Class Win32 \_ Process](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process).</span><span class="sxs-lookup"><span data-stu-id="7dd45-163">For an example of using direct access, see [Create Method in Class Win32\_Process](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process).</span></span> <span data-ttu-id="7dd45-164">Para obtener un ejemplo de la misma operación mediante [**un SWbemObject**](swbemobject.md), [**veaSWbemObject.ExecMethod**](swbemobject-execmethod-.md).</span><span class="sxs-lookup"><span data-stu-id="7dd45-164">For an example of the same operation using an [**SWbemObject**](swbemobject.md), see [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md).</span></span>


```VB
' Connect to WMI
set Services = getobject("winmgmts:root\cimv2")

' Obtain the class definition object of a Win32_Process object.
Set oProcess = Services.Get("Win32_Process")

' Create the SWbemMethod.InParameters object
' to hold the input parameter needed
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains obtains a class object that
' defines the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object so SWbemObject.SpawnInstance_ 
'can be called to create it.

Set oInParams = _
    oProcess.Methods_("Create").InParameters.SpawnInstance_
oInParams.CommandLine = "Notepad.exe"

'Call SWbemServices.ExecMethod with the WMI path Win32_Process
Set oOutParams = _
    Services.ExecMethod( "Win32_Process", "Create", oInParams)

If oOutParams.ReturnValue = 0 Then
    wscript.echo "Create method executed successfully."
Else
' If the Create method failed to execute,
' an empty OutParameters object is returned. 
    If IsNull(oOutParams.ReturnValue) Then
        wscript.echo "Create method failed to execute."  
    Else
        wscript.echo "Create method executed" _
            & " but had error " _
            & "0x" & hex(oOutParams.ReturnValue)
    End If
End If
```



## <a name="requirements"></a><span data-ttu-id="7dd45-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7dd45-165">Requirements</span></span>



| <span data-ttu-id="7dd45-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="7dd45-166">Requirement</span></span> | <span data-ttu-id="7dd45-167">Valor</span><span class="sxs-lookup"><span data-stu-id="7dd45-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7dd45-168">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7dd45-168">Minimum supported client</span></span><br/> | <span data-ttu-id="7dd45-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7dd45-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7dd45-170">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7dd45-170">Minimum supported server</span></span><br/> | <span data-ttu-id="7dd45-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7dd45-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7dd45-172">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7dd45-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="7dd45-173"><dt>Wbemdisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="7dd45-173"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7dd45-174">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="7dd45-174">Type library</span></span><br/>             | <dl> <span data-ttu-id="7dd45-175"><dt>Wbemdisp.tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7dd45-175"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7dd45-176">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7dd45-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7dd45-177"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7dd45-177"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7dd45-178">CLSID</span><span class="sxs-lookup"><span data-stu-id="7dd45-178">CLSID</span></span><br/>                    | <span data-ttu-id="7dd45-179">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="7dd45-179">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="7dd45-180">IID</span><span class="sxs-lookup"><span data-stu-id="7dd45-180">IID</span></span><br/>                      | <span data-ttu-id="7dd45-181">IID \_ ISWbemServices</span><span class="sxs-lookup"><span data-stu-id="7dd45-181">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="7dd45-182">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7dd45-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dd45-183">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="7dd45-183">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="7dd45-184">**SWbemObject.ExecMethod\_**</span><span class="sxs-lookup"><span data-stu-id="7dd45-184">**SWbemObject.ExecMethod\_**</span></span>](swbemobject-execmethod-.md)
</dt> <dt>

[<span data-ttu-id="7dd45-185">Llamar a un método provider</span><span class="sxs-lookup"><span data-stu-id="7dd45-185">Calling a Provider Method</span></span>](calling-a-provider-method.md)
</dt> <dt>

[<span data-ttu-id="7dd45-186">Manipulación de información de clase e instancia</span><span class="sxs-lookup"><span data-stu-id="7dd45-186">Manipulating Class and Instance Information</span></span>](manipulating-class-and-instance-information.md)
</dt> </dl>

 

