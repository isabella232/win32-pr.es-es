---
description: Al igual que con todas las aplicaciones, WMI recibe códigos de error del sistema operativo Windows.
ms.assetid: f54b8e7c-c531-47d5-bab8-780652b94555
ms.tgt_platform: multiple
title: Recuperar un código de error
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75c42dbd160ef6412c332e2da2c01f6590e10966
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715761"
---
# <a name="retrieving-an-error-code"></a><span data-ttu-id="94a3f-103">Recuperar un código de error</span><span class="sxs-lookup"><span data-stu-id="94a3f-103">Retrieving an Error Code</span></span>

<span data-ttu-id="94a3f-104">Al igual que con todas las aplicaciones, WMI recibe códigos de error del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="94a3f-104">As with all applications, WMI receives error codes from the Windows operating system.</span></span>

<span data-ttu-id="94a3f-105">Cuando recibe un código de error, tiene las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="94a3f-105">When you receive an error code, you have the following options:</span></span>

-   <span data-ttu-id="94a3f-106">Examine el registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="94a3f-106">Look at the event log.</span></span>

    <span data-ttu-id="94a3f-107">WMI envía mensajes de error al servicio registro de eventos que comprueba los registros de eventos para ayudar a determinar la causa de un error.</span><span class="sxs-lookup"><span data-stu-id="94a3f-107">WMI sends error messages to the Event Log service that checks the event logs to help determine the cause of an error.</span></span> <span data-ttu-id="94a3f-108">Puede utilizar las clases que admite el proveedor de [registro de eventos](/previous-versions/windows/desktop/eventlogprov/event-log-provider) para obtener acceso a los registros de eventos mediante programación.</span><span class="sxs-lookup"><span data-stu-id="94a3f-108">You can use the classes that the [Event Log](/previous-versions/windows/desktop/eventlogprov/event-log-provider) provider supports to access event logs programmatically.</span></span>

-   <span data-ttu-id="94a3f-109">Recupere el código de error normalmente.</span><span class="sxs-lookup"><span data-stu-id="94a3f-109">Retrieve the error code normally.</span></span>

    <span data-ttu-id="94a3f-110">WMI admite las técnicas estándar para recuperar códigos de error, que son códigos de error COM para C++, y objetos de error nativo, como el [objeto ERR (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)), o [**SWbemLastError**](swbemlasterror.md) si el proveedor proporciona información de errores.</span><span class="sxs-lookup"><span data-stu-id="94a3f-110">WMI supports the standard techniques to retrieve error codes, which are COM error codes for C++, and native error objects, such as [Err Object (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)), or [**SWbemLastError**](swbemlasterror.md) if the provider supplies error information.</span></span>

<span data-ttu-id="94a3f-111">Para obtener más información, vea [manipular la información de clase e instancia](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="94a3f-111">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

<span data-ttu-id="94a3f-112">En este tema se describen las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="94a3f-112">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="94a3f-113">Controlar un error con VBScript</span><span class="sxs-lookup"><span data-stu-id="94a3f-113">Handling an Error with VBScript</span></span>](#handling-an-error-with-vbscript)
-   [<span data-ttu-id="94a3f-114">Controlar un error con C++</span><span class="sxs-lookup"><span data-stu-id="94a3f-114">Handling an Error Using C++</span></span>](#handling-an-error-using-c)

## <a name="handling-an-error-with-vbscript"></a><span data-ttu-id="94a3f-115">Controlar un error con VBScript</span><span class="sxs-lookup"><span data-stu-id="94a3f-115">Handling an Error with VBScript</span></span>

<span data-ttu-id="94a3f-116">Si una llamada a WMI a través de la API de scripting para WMI produce un error, tiene las siguientes opciones para obtener acceso a la información de error:</span><span class="sxs-lookup"><span data-stu-id="94a3f-116">If a call to WMI through the Scripting API for WMI causes an error, you have the following options to access the error information:</span></span>

-   <span data-ttu-id="94a3f-117">Use los mecanismos de error nativos del lenguaje de scripting, por ejemplo, en VBScript use el [objeto ERR (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)) para admitir el control de errores.</span><span class="sxs-lookup"><span data-stu-id="94a3f-117">Use native error mechanisms of the scripting language, for example, in VBScript use [Err Object (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)) to support error handling.</span></span>
-   <span data-ttu-id="94a3f-118">Cree un objeto [**SWbemLastError**](swbemlasterror.md) para obtener un informe de errores.</span><span class="sxs-lookup"><span data-stu-id="94a3f-118">Create an [**SWbemLastError**](swbemlasterror.md) object to get an error report.</span></span>

<span data-ttu-id="94a3f-119">El siguiente script muestra el uso del [objeto Err nativo (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="94a3f-119">The following script shows use of the native [Err Object (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)).</span></span> <span data-ttu-id="94a3f-120">Cuando se proporciona un valor incorrecto para el identificador de proceso, se genera un error.</span><span class="sxs-lookup"><span data-stu-id="94a3f-120">When an incorrect value for the process handle is given, an error is generated.</span></span>


```VB
On Error Resume Next
Set objProcess = GetObject( _
    "winmgmts:root\cimv2:Win32_Process.Handle='one'")
Wscript.Echo Err.Number
```



> [!Note]
>
> <span data-ttu-id="94a3f-121">La propiedad **Description** del [objeto ERR (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)) está vacía al conectarse a WMI a través del moniker "winmgmts:".</span><span class="sxs-lookup"><span data-stu-id="94a3f-121">The **Description** property of [Err Object (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)) is empty when connecting to WMI through the "winmgmts:" moniker.</span></span> <span data-ttu-id="94a3f-122">Sin embargo, si se conecta mediante [**SWbemLocator**](swbemlocator.md), la descripción está disponible.</span><span class="sxs-lookup"><span data-stu-id="94a3f-122">However, if you connect using [**SWbemLocator**](swbemlocator.md), the description is available.</span></span>
>
> <span data-ttu-id="94a3f-123">En la tabla siguiente se enumeran las propiedades del [objeto ERR (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="94a3f-123">The following table lists the properties of [Err Object (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)).</span></span>
>
> 
>
> | <span data-ttu-id="94a3f-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="94a3f-124">Property</span></span>                   | <span data-ttu-id="94a3f-125">Contiene</span><span class="sxs-lookup"><span data-stu-id="94a3f-125">Contains</span></span>                                                       |
> |----------------------------|----------------------------------------------------------------|
> | <span data-ttu-id="94a3f-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="94a3f-126">**Description**</span></span><br/> | <span data-ttu-id="94a3f-127">Descripción localizada y legible del error.</span><span class="sxs-lookup"><span data-stu-id="94a3f-127">Localized, human-readable description of the error.</span></span><br/> |
> | <span data-ttu-id="94a3f-128">**Number**</span><span class="sxs-lookup"><span data-stu-id="94a3f-128">**Number**</span></span><br/>      | <span data-ttu-id="94a3f-129">**HRESULT** devuelto por la API de scripting para WMI.</span><span class="sxs-lookup"><span data-stu-id="94a3f-129">**HRESULT** returned by the Scripting API for WMI.</span></span><br/>  |
> | <span data-ttu-id="94a3f-130">**Origen**</span><span class="sxs-lookup"><span data-stu-id="94a3f-130">**Source**</span></span><br/>      | <span data-ttu-id="94a3f-131">Identifica el objeto que ha generado el error.</span><span class="sxs-lookup"><span data-stu-id="94a3f-131">Identifies the object that raised the error.</span></span><br/>        |
>
> 
>
>  

 

<span data-ttu-id="94a3f-132">El siguiente script muestra el uso de un objeto [**SWbemLastError**](swbemlasterror.md) para obtener información detallada del error.</span><span class="sxs-lookup"><span data-stu-id="94a3f-132">The following script shows use of an [**SWbemLastError**](swbemlasterror.md) object to obtain detailed error information.</span></span> <span data-ttu-id="94a3f-133">Tenga en cuenta que no todos los proveedores proporcionan información a **SWbemLastError**.</span><span class="sxs-lookup"><span data-stu-id="94a3f-133">Note that not all providers supply information to **SWbemLastError**.</span></span> <span data-ttu-id="94a3f-134">Para obtener más información sobre los códigos de error en el script, vea [WbemErrorEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="94a3f-134">For more information about error codes in script, see [WbemErrorEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>


```VB
On Error Resume Next
Set obj = GetObject("winmgmts:root\cimv2:Win32_Process.Handle='one'")
Set LastError = createobject("wbemscripting.swbemlasterror")
Wscript.Echo "Operation = " & LastError.operation & VBCRLF & "ParameterInfo = " _
            & LastError.ParameterInfo & VBCRLF & "ProviderName = " & LastError.ProviderName
```



## <a name="handling-an-error-using-c"></a><span data-ttu-id="94a3f-135">Controlar un error con C++</span><span class="sxs-lookup"><span data-stu-id="94a3f-135">Handling an Error Using C++</span></span>

<span data-ttu-id="94a3f-136">Una aplicación cliente de WMI puede recibir errores específicos de COM o específicos de WMI.</span><span class="sxs-lookup"><span data-stu-id="94a3f-136">A WMI client application can receive either COM-specific or WMI-specific errors.</span></span> <span data-ttu-id="94a3f-137">Los errores COM se ajustan a la estructura de los códigos de error COM.</span><span class="sxs-lookup"><span data-stu-id="94a3f-137">The COM errors conform to the structure of COM error codes.</span></span> <span data-ttu-id="94a3f-138">Todas las interfaces WMI pueden devolver un error específico de COM excepto las interfaces [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext), [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject)y [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) .</span><span class="sxs-lookup"><span data-stu-id="94a3f-138">All WMI interfaces can return a COM-specific error except the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext), [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject), and [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) interfaces.</span></span> <span data-ttu-id="94a3f-139">Para obtener más información sobre los códigos de error COM, vea [control de errores](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="94a3f-139">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span> <span data-ttu-id="94a3f-140">Las páginas de referencia de las interfaces WMI enumeran los códigos de error de WMI correspondientes en la sección códigos de error.</span><span class="sxs-lookup"><span data-stu-id="94a3f-140">The reference pages of the WMI interfaces list the appropriate WMI error codes in the Error Codes section.</span></span>

<span data-ttu-id="94a3f-141">Una aplicación cliente debe cumplir los estándares COM para comprobar el estado y los códigos de retorno de error.</span><span class="sxs-lookup"><span data-stu-id="94a3f-141">A client application must follow the COM standards for checking status and error return codes.</span></span> <span data-ttu-id="94a3f-142">La principal diferencia que debe elegir es si desea recuperar el código de error de una llamada sincrónica, semisincrónica o asincrónica.</span><span class="sxs-lookup"><span data-stu-id="94a3f-142">The main difference you must choose is whether you wish to retrieve the error code from a synchronous, semisynchronous, or asynchronous call.</span></span>

<span data-ttu-id="94a3f-143">**Para obtener acceso a mensajes de error sincrónicos y semisincrónicos mediante C++**</span><span class="sxs-lookup"><span data-stu-id="94a3f-143">**To access synchronous and semisynchronous error messages using C++**</span></span>

1.  <span data-ttu-id="94a3f-144">Recupere la información de error con una llamada a la función com [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) .</span><span class="sxs-lookup"><span data-stu-id="94a3f-144">Retrieve the error information with a call to the [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) COM function.</span></span>

    <span data-ttu-id="94a3f-145">Asegúrese de llamar a [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) inmediatamente después de que un método de interfaz indique un error.</span><span class="sxs-lookup"><span data-stu-id="94a3f-145">Make sure to call [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) immediately after an interface method indicates an error.</span></span> <span data-ttu-id="94a3f-146">Esto incluye cualquiera de los métodos [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) a los que se llama mientras se procesa un proceso semisincrónico.</span><span class="sxs-lookup"><span data-stu-id="94a3f-146">This includes any of the [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) methods you call while processing a semisynchronous process.</span></span>

2.  <span data-ttu-id="94a3f-147">Examine el objeto de error COM devuelto con una llamada al método [**IErrorInterface:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) .</span><span class="sxs-lookup"><span data-stu-id="94a3f-147">Examine the returned COM error object with a call to the [**IErrorInterface::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method.</span></span>

    <span data-ttu-id="94a3f-148">Asegúrese de especificar IID \_ WbemClassObject para el parámetro *riid* en la llamada [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) .</span><span class="sxs-lookup"><span data-stu-id="94a3f-148">Make sure to specify IID\_WbemClassObject for the *riid* parameter in the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) call.</span></span> <span data-ttu-id="94a3f-149">El método **QueryInterface** devuelve una instancia de una clase WMI, normalmente [**\_ \_ ExtendedStatus**](--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="94a3f-149">The **QueryInterface** method returns an instance of a WMI class, typically [**\_\_ExtendedStatus**](--extendedstatus.md).</span></span>

<span data-ttu-id="94a3f-150">WMI no entrega el objeto de error a través de [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) para una llamada asincrónica porque no hay ninguna manera de saber cuándo, o en qué subproceso se produjo la llamada asincrónica.</span><span class="sxs-lookup"><span data-stu-id="94a3f-150">WMI does not deliver the error object through [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) for an asynchronous call because there is no way to know when, or on which thread the asynchronous call occurred.</span></span> <span data-ttu-id="94a3f-151">Por lo tanto, el código solo puede controlar errores específicos o pasar el error de llamada a través de COM.</span><span class="sxs-lookup"><span data-stu-id="94a3f-151">Therefore, your code can only handle specific errors or pass the call failure through COM.</span></span>

> [!Note]  
> <span data-ttu-id="94a3f-152">Dado que la devolución de llamada al receptor podría no devolverse en el mismo nivel de autenticación que requiere el cliente, se recomienda usar semisincrónico en lugar de la comunicación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="94a3f-152">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="94a3f-153">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="94a3f-153">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

<span data-ttu-id="94a3f-154">**Para obtener acceso a mensajes de error asincrónicos mediante C++**</span><span class="sxs-lookup"><span data-stu-id="94a3f-154">**To access asynchronous error messages using C++**</span></span>

-   <span data-ttu-id="94a3f-155">Recupere el objeto de error COM de la implementación de [**IWbemObjectSink:: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus).</span><span class="sxs-lookup"><span data-stu-id="94a3f-155">Retrieve the COM error object from your implementation of [**IWbemObjectSink::SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus).</span></span>

    <span data-ttu-id="94a3f-156">En el siguiente pseudocódigo se muestra una implementación de control de errores típica para una aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="94a3f-156">The following pseudocode shows a typical error handling implementation for a client application.</span></span>

    ```C++
    HRESULT hRes = SomeMethod;

    // Check for specific error and status codes.
    if (hRes == WBEM_E_NOT_FOUND)
    {
    // Processing to handle specific error code
    }
    else if hRes == WBEM_S_DUPLICATE_OBJECTS
    {
    // All other cases, including errors specific to COM
    }
    else if (FAILED(hRes))
    {

    }
    ```

    

 

