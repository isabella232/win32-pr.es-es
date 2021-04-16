---
description: Realizar una llamada asincrónica a un método WMI o a un método de proveedor permite que un script continúe ejecutándose mientras los objetos vuelven a un objeto SWbemSink y se controlan mediante métodos como SWbemSink. OnObjectReady.
ms.assetid: 61f401d9-c874-472d-8dd3-7cf9d7f20a12
ms.tgt_platform: multiple
title: Realización de una llamada asincrónica con VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c2b3ec0c1bd771f59a4e456cb8e57c3bb3e9e394
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706392"
---
# <a name="making-an-asynchronous-call-with-vbscript"></a><span data-ttu-id="29a04-103">Realización de una llamada asincrónica con VBScript</span><span class="sxs-lookup"><span data-stu-id="29a04-103">Making an Asynchronous Call with VBScript</span></span>

<span data-ttu-id="29a04-104">Realizar una llamada asincrónica a un [*método WMI*](gloss-w.md) o a un [*método de proveedor*](gloss-p.md) permite que un script continúe ejecutándose mientras los objetos vuelven a un objeto [**SWbemSink**](swbemsink.md) y se controlan mediante métodos como [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md).</span><span class="sxs-lookup"><span data-stu-id="29a04-104">Making an asynchronous call to a [*WMI method*](gloss-w.md) or a [*provider method*](gloss-p.md) allows a script to continue executing while objects return to an [**SWbemSink**](swbemsink.md) object, and are handled by methods such as [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md).</span></span> <span data-ttu-id="29a04-105">Sin embargo, no se recomiendan las llamadas asincrónicas porque es posible que los datos no se devuelvan en el mismo nivel de seguridad que se realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="29a04-105">However, asynchronous calls are not recommended because the data may not be returned at the same level of security as the call is made.</span></span>

<span data-ttu-id="29a04-106">Al utilizar llamadas de receptor asincrónicas como [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md) para obtener los datos devueltos, puede establecer el siguiente valor del registro.</span><span class="sxs-lookup"><span data-stu-id="29a04-106">When using asynchronous sink calls like [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) to get returned data, you can set the following registry value.</span></span>

<span data-ttu-id="29a04-107">**HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **UnsecAppAccessControlDefault**</span><span class="sxs-lookup"><span data-stu-id="29a04-107">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**UnsecAppAccessControlDefault**</span></span>

<span data-ttu-id="29a04-108">Al establecer este valor del registro se garantiza la autenticación de los objetos de datos que se devuelven al receptor.</span><span class="sxs-lookup"><span data-stu-id="29a04-108">Setting this registry value ensures authentication of the data objects returned to the sink.</span></span> <span data-ttu-id="29a04-109">Si **UnsecAppAccessControlDefault** se establece en One (1), WMI realiza la comprobación de acceso de la devolución de datos.</span><span class="sxs-lookup"><span data-stu-id="29a04-109">If **UnsecAppAccessControlDefault** is set to one (1), then WMI performs access checking of the data return.</span></span> <span data-ttu-id="29a04-110">Las comprobaciones de acceso comprueban que los datos proceden del origen correcto.</span><span class="sxs-lookup"><span data-stu-id="29a04-110">Access checks verify that the data comes from the correct source.</span></span> <span data-ttu-id="29a04-111">Para obtener más información, vea [establecer la seguridad en una llamada asincrónica](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="29a04-111">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="29a04-112">Los métodos asincrónicos con nombres que terminan en "Async \_ " siempre devuelven inmediatamente después de que se llame a para que un programa pueda seguir ejecutándose.</span><span class="sxs-lookup"><span data-stu-id="29a04-112">Asynchronous methods with names that end in "Async\_" always return immediately after being called so that a program can continue executing.</span></span> <span data-ttu-id="29a04-113">Por ejemplo, [**SWbemServices.ExecQuery**](swbemservices-execquery.md) es sincrónico y bloquea la ejecución hasta que se devuelven todos los objetos.</span><span class="sxs-lookup"><span data-stu-id="29a04-113">For example, [**SWbemServices.ExecQuery**](swbemservices-execquery.md) is synchronous and blocks execution until all of the objects are returned.</span></span> <span data-ttu-id="29a04-114">El método [**cQueryAsyncSWbemServices.Exe**](swbemservices-execqueryasync.md) es la versión asincrónica sin bloqueos.</span><span class="sxs-lookup"><span data-stu-id="29a04-114">The [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md) method is the nonblocking asynchronous version.</span></span> <span data-ttu-id="29a04-115">Una manera más segura de hacer la llamada a **SWbemServices.ExecQuery** no se bloquea es hacer que la llamada sea [*semisincrónica*](gloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="29a04-115">A more secure way to make the call to **SWbemServices.ExecQuery** nonblocking is by making the call [*semisynchronously*](gloss-s.md).</span></span> <span data-ttu-id="29a04-116">Para obtener más información, vea [establecer la seguridad en una llamada asincrónica](setting-security-on-an-asynchronous-call.md) y [crear una llamada semisincrónica con VBScript](making-a-semisynchronous-call-with-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="29a04-116">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md) and [Making a Semisynchronous Call with VBScript](making-a-semisynchronous-call-with-vbscript.md).</span></span>

<span data-ttu-id="29a04-117">El parámetro *iFlags* para llamadas asincrónicas siempre tiene como valor predeterminado cero (0).</span><span class="sxs-lookup"><span data-stu-id="29a04-117">The *iFlags* parameter for asynchronous calls always defaults to zero (0).</span></span> <span data-ttu-id="29a04-118">Los métodos asincrónicos no proporcionan una colección [**SWbemObjectSet**](swbemobjectset.md) a la subrutina del receptor.</span><span class="sxs-lookup"><span data-stu-id="29a04-118">Asynchronous methods do not supply an [**SWbemObjectSet**](swbemobjectset.md) collection to the sink subroutine.</span></span> <span data-ttu-id="29a04-119">En su lugar, la subrutina del evento [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md) del script o la aplicación recibe cada objeto a medida que se proporciona.</span><span class="sxs-lookup"><span data-stu-id="29a04-119">Instead, the [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) event subroutine in your script or application receives each object as it is provided.</span></span>

<span data-ttu-id="29a04-120">Cuando se completa la llamada asincrónica original, llama al evento [**SWbemSink.**](swbemsink-oncompleted.md) onexecute del receptor de objetos y ejecuta el código que se coloca allí para procesar el resultado de la llamada.</span><span class="sxs-lookup"><span data-stu-id="29a04-120">When the original asynchronous call is complete, it calls the [**SWbemSink.OnCompleted**](swbemsink-oncompleted.md) event of the object sink, and executes the code you place there to process the result of the call.</span></span>

> [!Note]  
> <span data-ttu-id="29a04-121">Una página Active Server (ASP) como un host de script no admite una llamada asincrónica.</span><span class="sxs-lookup"><span data-stu-id="29a04-121">An Active Server Page (ASP) as a script host does not support an asynchronous call.</span></span>

 

<span data-ttu-id="29a04-122">En el procedimiento siguiente se describe cómo hacer una llamada asincrónica mediante VBScript.</span><span class="sxs-lookup"><span data-stu-id="29a04-122">The following procedure describes how to make an asynchronous call by using VBScript.</span></span>

<span data-ttu-id="29a04-123">**Para hacer una llamada asincrónica con VBScript**</span><span class="sxs-lookup"><span data-stu-id="29a04-123">**To make an asynchronous call using VBScript**</span></span>

1.  <span data-ttu-id="29a04-124">Conéctese a WMI y obtenga un objeto [**SWbemServices**](swbemservices.md) .</span><span class="sxs-lookup"><span data-stu-id="29a04-124">Connect to WMI and get an [**SWbemServices**](swbemservices.md) object.</span></span>

    ```VB
    Set Service = GetObject("Winmgmts:")
    ```

    

2.  <span data-ttu-id="29a04-125">Cree el receptor de objetos mediante [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) o (solo para Windows Script Host 2,0) la etiqueta de objeto con un atributo Events establecido en **true**.</span><span class="sxs-lookup"><span data-stu-id="29a04-125">Create the object sink using either [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) or (for Windows Script Host 2.0 only) the OBJECT tag with an events attribute set to **TRUE**.</span></span>

    ```VB
    Set sink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")
    ```

    

    <span data-ttu-id="29a04-126">O bien</span><span class="sxs-lookup"><span data-stu-id="29a04-126">-or-</span></span>

    ```VB
    <OBJECT progid="WbemScripting.SWbemSink" ID="SINK" events="true"/>
    ```

    

3.  <span data-ttu-id="29a04-127">Cree una subrutina para cada evento que un evento asincrónico pueda desencadenar.</span><span class="sxs-lookup"><span data-stu-id="29a04-127">Create a subroutine for each event an asynchronous event can trigger.</span></span> <span data-ttu-id="29a04-128">Estos eventos se definen como métodos en [**SWbemObject**](swbemobject.md).</span><span class="sxs-lookup"><span data-stu-id="29a04-128">These events are defined as methods on [**SWbemObject**](swbemobject.md).</span></span> <span data-ttu-id="29a04-129">Por ejemplo, WMI realiza una devolución de llamada a [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md) cuando cada instancia devuelve.</span><span class="sxs-lookup"><span data-stu-id="29a04-129">For example, WMI makes a callback to [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) as each instance returns.</span></span>

    <span data-ttu-id="29a04-130">Al crear la subrutina, coloque el código en la subrutina para controlar cada evento cuando se reciba.</span><span class="sxs-lookup"><span data-stu-id="29a04-130">When you create the subroutine, place code in the subroutine to handle each event when it is received.</span></span>

    ```VB
    Sub SINK_OnCompleted(
          iHResult, 
          objErrorObject, 
          objAsyncContext
          )
        WScript.Echo "Asynchronous operation is done."
    End Sub

    Sub SINK_OnObjectReady(objObject, objAsyncContext)
        WScript.Echo (objObject.Name)
    End Sub
    ```

    

    <span data-ttu-id="29a04-131">Examine el parámetro *iHresult* que devuelve el evento [**alcompleted**](swbemsink-oncompleted.md) para determinar si la llamada asincrónica se realiza correctamente o no, o si se produjo un error.</span><span class="sxs-lookup"><span data-stu-id="29a04-131">Examine the *iHresult* parameter returned by the [**OnCompleted**](swbemsink-oncompleted.md) event to determine whether or not the asynchronous call is successful, or if an error occurred.</span></span> <span data-ttu-id="29a04-132">Si es correcto, el valor pasado en el parámetro *iHresult* es igual a cero (0).</span><span class="sxs-lookup"><span data-stu-id="29a04-132">If successful, the value passed in the *iHresult* parameter is equal to zero (0).</span></span> <span data-ttu-id="29a04-133">Cualquier otro valor puede indicar un error y debe comprobar los valores del objeto de error que se devuelve en el parámetro *objErrorObject* .</span><span class="sxs-lookup"><span data-stu-id="29a04-133">Any other value may indicate an error, and you should check the values in the error object that is returned in the *objErrorObject* parameter.</span></span>

4.  <span data-ttu-id="29a04-134">Realice una llamada asincrónica y pase el nombre del receptor en el parámetro *objWbemSink* .</span><span class="sxs-lookup"><span data-stu-id="29a04-134">Make an asynchronous call and pass the name of your sink in the *objWbemSink* parameter.</span></span>

    ```VB
    Service.InstancesOfAsync sink, "Win32_process"
    ```

    

5.  <span data-ttu-id="29a04-135">Realice una llamada que impida que el script finalice antes de que se reciban todos los eventos.</span><span class="sxs-lookup"><span data-stu-id="29a04-135">Make a call that prevents the script from ending before all of the events are received.</span></span> <span data-ttu-id="29a04-136">Si el script se puede ejecutar con una interfaz de pantalla, una manera sencilla de hacerlo es usar un comando de Windows Script Host (WSH) `Echo` , que se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="29a04-136">If your script can run with a screen interface, a simple way to do this is to use a Windows Script Host (WSH) `Echo` command, which is shown in the following example.</span></span>

    ```VB
    WScript.Echo "Waiting for instances."
    ```

    

    <span data-ttu-id="29a04-137">Al ejecutar este script, es posible que vea que la primera instancia vuelve antes del mensaje **en espera de instancias** o puede que la vea después de.</span><span class="sxs-lookup"><span data-stu-id="29a04-137">When you execute this script you may see the first instance return before the **Waiting for instances** message or you may see it after.</span></span> <span data-ttu-id="29a04-138">Esta es la naturaleza del procesamiento asincrónico.</span><span class="sxs-lookup"><span data-stu-id="29a04-138">This is the nature of asynchronous processing.</span></span> <span data-ttu-id="29a04-139">Si cierra el cuadro **de mensaje en espera** demasiado pronto, es posible que no vea todas las instancias.</span><span class="sxs-lookup"><span data-stu-id="29a04-139">If you close the **Waiting for instances** message box too soon, you may not see all of the instances.</span></span>

6.  <span data-ttu-id="29a04-140">Si tiene resultados de varias llamadas asincrónicas diferentes que devuelven al mismo receptor, almacene los datos distintivos necesarios en el parámetro de contexto *objWbemAsyncContext* .</span><span class="sxs-lookup"><span data-stu-id="29a04-140">If you have results from several different asynchronous calls returning to the same sink, store any necessary distinguishing data in the *objWbemAsyncContext* context parameter.</span></span>

7.  <span data-ttu-id="29a04-141">Cuando termine con el receptor, cancele la llamada asincrónica con el método [**Cancel**](swbemsink-cancel.md) .</span><span class="sxs-lookup"><span data-stu-id="29a04-141">When finished with the sink, cancel your asynchronous call with the [**Cancel**](swbemsink-cancel.md) method.</span></span>

    ```VB
    objwbemsink.Cancel()
    ```

    

    <span data-ttu-id="29a04-142">El método [**Cancel**](swbemsink-cancel.md) indica a WSH que cancele todas las llamadas asincrónicas asociadas a un objeto receptor determinado.</span><span class="sxs-lookup"><span data-stu-id="29a04-142">The [**Cancel**](swbemsink-cancel.md) method instructs WSH to cancel all of the asynchronous calls associated with a given sink object.</span></span> <span data-ttu-id="29a04-143">Por lo tanto, puede que desee usar receptores independientes para las operaciones asincrónicas que deben ser independientes.</span><span class="sxs-lookup"><span data-stu-id="29a04-143">Thus, you may want to use separate sinks for asynchronous operations that must be independent.</span></span>

8.  <span data-ttu-id="29a04-144">Libere el objeto de receptor mediante la asignación del objeto de receptor a `Nothing` .</span><span class="sxs-lookup"><span data-stu-id="29a04-144">Release the sink object by assigning the sink object to `Nothing`.</span></span>

    ```VB
    set objwbemsink= Nothing
    ```

    

<span data-ttu-id="29a04-145">En el ejemplo de código siguiente se muestra una consulta asincrónica para todas las instancias del [**\_ proceso de Win32**](/windows/desktop/CIMWin32Prov/win32-process) en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="29a04-145">The following code example shows an asynchronous query for all the instances of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) on the local machine.</span></span> <span data-ttu-id="29a04-146">Para obtener una versión semisincrónica del mismo método, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="29a04-146">For a semisynchronous version of the same method, see [Calling a Method](calling-a-method.md).</span></span>


```VB
' Create an object sink
set oSink = WScript.CreateObject("wbemscripting.swbemsink","sink_")
' Connect to WMI and the cimv2 namespace, and obtain
' an SWbemServices object
set oSvc = GetObject("winmgmts:root\cimv2")

bdone = false
' Query for all Win32_Process objects
osvc.ExecQueryAsync oSink, "SELECT Name FROM Win32_Process"
' Wait until all instances are returned. 
' The bdone flag prevents the script from exiting until
' the sink.OnCompleted subroutine is executed when
' all the objects are returned.
while not bdone    
    wscript.sleep 1000
wend

' The sink subroutine to handle the OnObjectReady 
' event. This is called as each object returns.
sub sink_OnObjectReady(oInst, octx)
    WScript.Echo "Got Instance: " & oInst.Name
end sub
' The sink subroutine to handle the OnCompleted event.
' This is called when all the objects are returned. 
' The oErr parameter obtains an SWbemLastError object,
' if available from the provider.
sub sink_OnCompleted(HResult, oErr, oCtx)
    WScript.Echo "ExecQueryAsync completed"
    bdone = true
end sub
```



## <a name="related-topics"></a><span data-ttu-id="29a04-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="29a04-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29a04-148">Llamar a un método</span><span class="sxs-lookup"><span data-stu-id="29a04-148">Calling a Method</span></span>](calling-a-method.md)
</dt> <dt>

[<span data-ttu-id="29a04-149">Mantenimiento de la seguridad de WMI</span><span class="sxs-lookup"><span data-stu-id="29a04-149">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> </dl>

 

 
