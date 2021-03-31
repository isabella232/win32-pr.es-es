---
description: El \_ método ExecMethod del objeto SWbemObject ejecuta un método exportado por un proveedor de métodos.
ms.assetid: 39a8a6e7-b499-410a-8c27-d4a05d1a61b9
ms.tgt_platform: multiple
title: Método de cMethod_ de SWbemObject.Exe(Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.ExecMethod_
- ISWbemObject.ExecMethod_
- ISWbemObject.ExecMethod_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6b71d88a113e515d50ac01a23f070714fa467615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155829"
---
# <a name="swbemobjectexecmethod_-method"></a><span data-ttu-id="e52ad-103">SWbemObject.Exe\_ método cMethod</span><span class="sxs-lookup"><span data-stu-id="e52ad-103">SWbemObject.ExecMethod\_ method</span></span>

<span data-ttu-id="e52ad-104">El **método \_ ExecMethod** del objeto [**SWbemObject**](swbemobject.md) ejecuta un método exportado por un proveedor de métodos.</span><span class="sxs-lookup"><span data-stu-id="e52ad-104">The **ExecMethod\_** method of the [**SWbemObject**](swbemobject.md) object executes a method exported by a method provider.</span></span>

<span data-ttu-id="e52ad-105">Este método se pausa mientras se ejecuta el método que se reenvía al proveedor adecuado.</span><span class="sxs-lookup"><span data-stu-id="e52ad-105">This method pauses while the method that is forwarded to the appropriate provider executes.</span></span> <span data-ttu-id="e52ad-106">A continuación, se devuelven la información y el estado.</span><span class="sxs-lookup"><span data-stu-id="e52ad-106">The information and status are then returned.</span></span> <span data-ttu-id="e52ad-107">El proveedor en lugar de WMI implementa el método.</span><span class="sxs-lookup"><span data-stu-id="e52ad-107">The provider rather than WMI implements the method.</span></span>

<span data-ttu-id="e52ad-108">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="e52ad-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e52ad-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e52ad-109">Syntax</span></span>


```VB
objOutParams = .ExecMethod_( _
  ByVal strMethodName, _
  [ ByVal objwbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="e52ad-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e52ad-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e52ad-111">*strMethodName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e52ad-111">*strMethodName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e52ad-112">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e52ad-112">Required.</span></span> <span data-ttu-id="e52ad-113">Nombre del método para el objeto.</span><span class="sxs-lookup"><span data-stu-id="e52ad-113">Name of the method for the object.</span></span>

</dd> <dt>

<span data-ttu-id="e52ad-114">*objwbemInParams* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="e52ad-114">*objwbemInParams* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e52ad-115">Este es un objeto [**SWbemObject**](swbemobject.md) que contiene los parámetros de entrada para el método que se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="e52ad-115">This is an [**SWbemObject**](swbemobject.md) object that contains the input parameters for the method being executed.</span></span> <span data-ttu-id="e52ad-116">De forma predeterminada, este parámetro es indefinido.</span><span class="sxs-lookup"><span data-stu-id="e52ad-116">By default, this parameter is undefined.</span></span> <span data-ttu-id="e52ad-117">Para obtener más información, consulte [construir objetos Parameters y analizar objetos Parameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="e52ad-117">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="e52ad-118">*iFlags* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="e52ad-118">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e52ad-119">Reserved y debe establecerse en 0 (cero) si se especifica.</span><span class="sxs-lookup"><span data-stu-id="e52ad-119">Reserved and must be set to 0 (zero) if specified.</span></span>

</dd> <dt>

<span data-ttu-id="e52ad-120">*objwbemNamedValueSet* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="e52ad-120">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e52ad-121">Normalmente, es indefinido.</span><span class="sxs-lookup"><span data-stu-id="e52ad-121">Typically, it is undefined.</span></span> <span data-ttu-id="e52ad-122">De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que atiende la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e52ad-122">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="e52ad-123">Un proveedor que admite o requiere tal información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.</span><span class="sxs-lookup"><span data-stu-id="e52ad-123">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e52ad-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e52ad-124">Return value</span></span>

<span data-ttu-id="e52ad-125">Si este método se realiza correctamente, se devuelve un objeto [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="e52ad-125">If this method is successful, an [**SWbemObject**](swbemobject.md) object returns.</span></span> <span data-ttu-id="e52ad-126">El objeto devuelto contiene los parámetros de salida y el valor devuelto para el método que se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="e52ad-126">The returned object contains the out parameters and return value for the method being executed.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e52ad-127">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="e52ad-127">Error codes</span></span>

<span data-ttu-id="e52ad-128">Después de completar el método **ExecMethod \_** , el objeto **Err** puede contener uno de los códigos de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="e52ad-128">After the completion of the **ExecMethod\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="e52ad-129">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="e52ad-129">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="e52ad-130">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="e52ad-130">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="e52ad-131">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="e52ad-131">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="e52ad-132">La clase especificada no era válida.</span><span class="sxs-lookup"><span data-stu-id="e52ad-132">Specified class was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="e52ad-133">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="e52ad-133">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="e52ad-134">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="e52ad-134">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="e52ad-135">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="e52ad-135">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="e52ad-136">Memoria insuficiente para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="e52ad-136">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e52ad-137">**wbemErrInvalidMethod** -2147749934 (0x8004102E)</span><span class="sxs-lookup"><span data-stu-id="e52ad-137">**wbemErrInvalidMethod** - 2147749934 (0x8004102E)</span></span>
</dt> <dd>

<span data-ttu-id="e52ad-138">El método solicitado no estaba disponible.</span><span class="sxs-lookup"><span data-stu-id="e52ad-138">Requested method was not available.</span></span>

</dd> <dt>

<span data-ttu-id="e52ad-139">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="e52ad-139">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="e52ad-140">El usuario actual no está autorizado para ejecutar el método.</span><span class="sxs-lookup"><span data-stu-id="e52ad-140">Current user was not authorized to execute the method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e52ad-141">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e52ad-141">Remarks</span></span>

<span data-ttu-id="e52ad-142">Este método es similar a [**SWbemServices.ExecMethod**](swbemservices-execmethod.md), pero funciona directamente en el objeto cuyo método se va a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="e52ad-142">This method is similar to [**SWbemServices.ExecMethod**](swbemservices-execmethod.md), but it operates directly on the object whose method is to be executed.</span></span> <span data-ttu-id="e52ad-143">Por ejemplo, en el ejemplo de código siguiente se llama al método de proveedor de [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) en el [**\_ servicio de Win32**](/windows/desktop/CIMWin32Prov/win32-service) y se usa el [acceso directo](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="e52ad-143">For example, the following code example calls the [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) provider method in [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) and uses [direct access](manipulating-class-and-instance-information.md).</span></span>


```VB
oService = GetObject("winmgmts:Win32_Service=Alerter")
iStatus = oService.StartService()
```



<span data-ttu-id="e52ad-144">Esta versión llama a **SWbemObject.Exe\_ cMethod** para ejecutar el método [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) .</span><span class="sxs-lookup"><span data-stu-id="e52ad-144">This version calls **SWbemObject.ExecMethod\_** to execute the [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) method.</span></span>


```VB
oService = GetObject("winmgmts:Win32_Service=Alerter")
Set outParam = process.ExecMethod_("StartService")
```



<span data-ttu-id="e52ad-145">Use **SWbemObject.ExecMethod \_** como alternativa al acceso directo para ejecutar un método de [*proveedor*](gloss-p.md) en los casos en los que no es posible ejecutar un método directamente.</span><span class="sxs-lookup"><span data-stu-id="e52ad-145">Use **SWbemObject.ExecMethod\_** as an alternative to direct access for executing a [*provider method*](gloss-p.md) in cases where it is not possible to execute a method directly.</span></span> <span data-ttu-id="e52ad-146">Por ejemplo, usaría **SWbemObject.ExecMethod \_** con un lenguaje de scripting que no admita parámetros de salida si el método tiene parámetros out.</span><span class="sxs-lookup"><span data-stu-id="e52ad-146">For example, you would use **SWbemObject.ExecMethod\_** with a scripting language that does not support output parameters if your method has out parameters.</span></span> <span data-ttu-id="e52ad-147">De lo contrario, el medio recomendado para invocar un método es usar el acceso directo.</span><span class="sxs-lookup"><span data-stu-id="e52ad-147">Otherwise, the recommended means of invoking a method is to use direct access.</span></span>

-   <span data-ttu-id="e52ad-148">En el método **\_ cMethodSWbemObject.Exe** se supone que el objeto representado por [**SWbemObject**](swbemobject.md) contiene el método que se va a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="e52ad-148">The **SWbemObject.ExecMethod\_** method assumes the object represented by [**SWbemObject**](swbemobject.md) contains the method to execute.</span></span> <span data-ttu-id="e52ad-149">Por el contrario, [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) requiere una ruta de acceso de objeto.</span><span class="sxs-lookup"><span data-stu-id="e52ad-149">By contrast, [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) requires an object path.</span></span> <span data-ttu-id="e52ad-150">Use **SWbemObject.ExecMethod \_** si ya ha obtenido el objeto cuyo método desea ejecutar.</span><span class="sxs-lookup"><span data-stu-id="e52ad-150">Use **SWbemObject.ExecMethod\_** if you already have obtained the object whose method you want to execute.</span></span>

## <a name="examples"></a><span data-ttu-id="e52ad-151">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e52ad-151">Examples</span></span>

<span data-ttu-id="e52ad-152">En el siguiente ejemplo se muestra el método [**ExecMethod**](swbemservices-execmethod.md) . El script crea un objeto de [**\_ proceso de Win32**](/windows/desktop/CIMWin32Prov/win32-process) que representa un proceso que ejecuta el Bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="e52ad-152">The following example shows the [**ExecMethod**](swbemservices-execmethod.md) method.The script creates a [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) object representing a process running Notepad.</span></span> <span data-ttu-id="e52ad-153">Para obtener más información sobre un script que ilustra las mismas operaciones que se realizan de forma asincrónica, vea [**SWbemObject.ExecMethodAsync \_**](swbemobject-execmethodasync-.md).</span><span class="sxs-lookup"><span data-stu-id="e52ad-153">For more information about a script illustrating the same operations performed asynchronously, see [**SWbemObject.ExecMethodAsync\_**](swbemobject-execmethodasync-.md).</span></span> <span data-ttu-id="e52ad-154">Para obtener un ejemplo de uso de acceso directo, consulte [**Create method in Class Win32 \_ Process**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) .</span><span class="sxs-lookup"><span data-stu-id="e52ad-154">For an example using direct access, see [**Create Method in Class Win32\_Process**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) .</span></span> <span data-ttu-id="e52ad-155">Para obtener un ejemplo de la misma operación mediante un objeto [**SWbemServices**](swbemservices.md) , vea **SWbemServices.ExecMethod**.</span><span class="sxs-lookup"><span data-stu-id="e52ad-155">For an example of the same operation using an [**SWbemServices**](swbemservices.md) object, see **SWbemServices.ExecMethod**.</span></span>


```VB
' Connect to WMI and obtain a Win32_Process object.
' This is also an SWbemObject object.
Set oProcess = GetObject("winmgmts:Win32_Process")

' Create the SWbemMethod.InParameters
' object to hold the input parameter needed
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains a class object that defines
' the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object so SWbemObject.SpawnInstance_
' can be called to create it.
Set oInParams = oProcess.Methods_("Create"). _
    InParameters.SpawnInstance_

' Specify the name of the process to be run.
oInParams.CommandLine = "Notepad.exe"
Set oOutParams = oProcess.ExecMethod_("Create", oInParams)

If oOutParams.ReturnValue = 0 Then
    wscript.echo "Create method executed successfully"
Else
' If the Create method failed to execute,
' an empty OutParameters object is returned. 
    If IsNull(oOutParams.ReturnValue) Then
        wscript.echo "Create method failed to execute."  
    Else
        wscript.echo "Create method executed but had error" _
            & "0x" & hex(oOutParams.ReturnValue)
    End If
End If
```



## <a name="requirements"></a><span data-ttu-id="e52ad-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e52ad-156">Requirements</span></span>



| <span data-ttu-id="e52ad-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="e52ad-157">Requirement</span></span> | <span data-ttu-id="e52ad-158">Value</span><span class="sxs-lookup"><span data-stu-id="e52ad-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e52ad-159">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e52ad-159">Minimum supported client</span></span><br/> | <span data-ttu-id="e52ad-160">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e52ad-160">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e52ad-161">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e52ad-161">Minimum supported server</span></span><br/> | <span data-ttu-id="e52ad-162">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e52ad-162">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e52ad-163">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e52ad-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="e52ad-164"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e52ad-164"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e52ad-165">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e52ad-165">Type library</span></span><br/>             | <dl> <span data-ttu-id="e52ad-166"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e52ad-166"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e52ad-167">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e52ad-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e52ad-168"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e52ad-168"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e52ad-169">CLSID</span><span class="sxs-lookup"><span data-stu-id="e52ad-169">CLSID</span></span><br/>                    | <span data-ttu-id="e52ad-170">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="e52ad-170">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="e52ad-171">IID</span><span class="sxs-lookup"><span data-stu-id="e52ad-171">IID</span></span><br/>                      | <span data-ttu-id="e52ad-172">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="e52ad-172">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="e52ad-173">Vea también</span><span class="sxs-lookup"><span data-stu-id="e52ad-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e52ad-174">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="e52ad-174">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="e52ad-175">**SWbemObject.ExecMethodAsync\_**</span><span class="sxs-lookup"><span data-stu-id="e52ad-175">**SWbemObject.ExecMethodAsync\_**</span></span>](swbemobject-execmethodasync-.md)
</dt> <dt>

[<span data-ttu-id="e52ad-176">**SWbemServices.ExecMethod**</span><span class="sxs-lookup"><span data-stu-id="e52ad-176">**SWbemServices.ExecMethod**</span></span>](swbemservices-execmethod.md)
</dt> </dl>

 

