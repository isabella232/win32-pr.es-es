---
description: Las llamadas asincrónicas presentan riesgos de seguridad graves porque es posible que una devolución de llamada al receptor no sea el resultado de la llamada asincrónica del script o la aplicación original.
ms.assetid: 2b839ea9-e1e6-4123-a98a-04ebee907b3b
ms.tgt_platform: multiple
title: Establecer la seguridad en una llamada asincrónica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e39f78315814d3b66c97e60a6b8045d7ea9e7afe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717042"
---
# <a name="setting-security-on-an-asynchronous-call"></a><span data-ttu-id="ad24d-103">Establecer la seguridad en una llamada asincrónica</span><span class="sxs-lookup"><span data-stu-id="ad24d-103">Setting Security on an Asynchronous Call</span></span>

<span data-ttu-id="ad24d-104">Las llamadas asincrónicas presentan riesgos de seguridad graves porque es posible que una devolución de llamada al [*receptor*](gloss-s.md) no sea el resultado de la llamada asincrónica del script o la aplicación original.</span><span class="sxs-lookup"><span data-stu-id="ad24d-104">Asynchronous calls present serious security risks because a callback to the [*sink*](gloss-s.md) may not be a result of the asynchronous call by the original application or script.</span></span> <span data-ttu-id="ad24d-105">La seguridad en las conexiones remotas se basa en el cifrado de la comunicación entre el cliente y el proveedor en el equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="ad24d-105">Security in remote connections is based on encryption of the communication between the client and the provider on the remote computer.</span></span> <span data-ttu-id="ad24d-106">En C++, puede establecer el cifrado mediante el parámetro de nivel de autenticación en la llamada a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="ad24d-106">In C++ you can set encryption through the authentication level parameter in the call to [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="ad24d-107">En scripting, establezca *AuthenticationLevel* en la conexión de moniker o en un objeto [**SWbemSecurity**](swbemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="ad24d-107">In scripting, set the *AuthenticationLevel* in the moniker connection or on an [**SWbemSecurity**](swbemsecurity.md) object.</span></span> <span data-ttu-id="ad24d-108">Para obtener más información, vea [establecer el nivel de seguridad de proceso predeterminado con VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="ad24d-108">For more information, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

<span data-ttu-id="ad24d-109">Los riesgos de seguridad para las llamadas asincrónicas existen porque WMI reduce el nivel de autenticación en una devolución de llamada hasta que la devolución de llamada se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="ad24d-109">The security risks for asynchronous calls exist because WMI lowers the authentication level on a callback until the callback succeeds.</span></span> <span data-ttu-id="ad24d-110">En una llamada asincrónica saliente, el cliente puede establecer el nivel de autenticación en la conexión a WMI.</span><span class="sxs-lookup"><span data-stu-id="ad24d-110">On an outgoing asynchronous call, the client can set the authentication level on the connection to WMI.</span></span> <span data-ttu-id="ad24d-111">WMI recupera la configuración de seguridad en la llamada de cliente e intenta volver a llamar con el mismo nivel de autenticación.</span><span class="sxs-lookup"><span data-stu-id="ad24d-111">WMI retrieves the security settings on the client call and attempts to call back with the same authentication level.</span></span> <span data-ttu-id="ad24d-112">La devolución de llamada siempre se inicia en el nivel de **\_ \_ \_ \_ \_ privacidad de nivel de autenticación de RPC C** .</span><span class="sxs-lookup"><span data-stu-id="ad24d-112">The callback is always initiated at the **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** level.</span></span> <span data-ttu-id="ad24d-113">Si se produce un error en la devolución de llamada, WMI baja el nivel de autenticación a un nivel en el que la devolución de llamada puede realizarse correctamente, si es necesario, a la **autenticación de RPC \_ C \_ \_ nivel \_ ninguno**.</span><span class="sxs-lookup"><span data-stu-id="ad24d-113">If the callback fails, WMI lowers the authentication level to a level where the callback can succeed, if necessary, to **RPC\_C\_AUTHN\_LEVEL\_NONE**.</span></span> <span data-ttu-id="ad24d-114">En el contexto de las llamadas dentro del sistema local en las que el servicio de autenticación no es Kerberos, la devolución de llamada siempre se devuelve en el **\_ \_ \_ nivel \_ None de autenticación de RPC C**.</span><span class="sxs-lookup"><span data-stu-id="ad24d-114">In the context of calls within the local system where the authentication service is not Kerberos, the callback is always returned at **RPC\_C\_AUTHN\_LEVEL\_NONE**.</span></span>

<span data-ttu-id="ad24d-115">El nivel de autenticación mínimo es el **\_ \_ \_ nivel \_ de autenticación RPC C** (**wbemAuthenticationLevelPkt** para scripting).</span><span class="sxs-lookup"><span data-stu-id="ad24d-115">The minimum authentication level is **RPC\_C\_AUTHN\_LEVEL\_PKT** (**wbemAuthenticationLevelPkt** for scripting).</span></span> <span data-ttu-id="ad24d-116">Sin embargo, puede especificar un nivel superior, como **\_ \_ \_ \_ \_ privacidad de nivel de autenticación de RPC C** (**wbemAuthenticationLevelPktPrivacy**).</span><span class="sxs-lookup"><span data-stu-id="ad24d-116">However, you can specify a higher level, such as **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** (**wbemAuthenticationLevelPktPrivacy**).</span></span> <span data-ttu-id="ad24d-117">Se recomienda que las aplicaciones cliente o los scripts establezcan el nivel de autenticación en el nivel **\_ \_ \_ \_ predeterminado** de autenticación de RPC C (**wbemAuthenticationLevelDefault**), lo que permite negociar el nivel de autenticación con el nivel especificado por el servidor.</span><span class="sxs-lookup"><span data-stu-id="ad24d-117">It is recommended that client applications or scripts set the authentication level to **RPC\_C\_AUTHN\_LEVEL\_DEFAULT** (**wbemAuthenticationLevelDefault**) which allows the authentication level to be negotiated to the level specified by the server.</span></span>

<span data-ttu-id="ad24d-118">El valor del registro **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **UnsecAppAccessControlDefault** controla si WMI comprueba un nivel de autenticación aceptable en las devoluciones de llamada.</span><span class="sxs-lookup"><span data-stu-id="ad24d-118">The **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**UnsecAppAccessControlDefault** registry value controls whether WMI checks for an acceptable authentication level in callbacks.</span></span> <span data-ttu-id="ad24d-119">Este es el único mecanismo para proteger la seguridad del receptor de llamadas asincrónicas realizadas en scripting o Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="ad24d-119">This is the only mechanism for protecting sink security for asynchronous calls made in scripting or Visual Basic.</span></span> <span data-ttu-id="ad24d-120">De forma predeterminada, esta clave del registro se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="ad24d-120">By default, this registry key is set to zero.</span></span> <span data-ttu-id="ad24d-121">Si la clave del registro es cero, WMI no comprueba los niveles de autenticación.</span><span class="sxs-lookup"><span data-stu-id="ad24d-121">If the registry key is zero then WMI does not verify authentication levels.</span></span> <span data-ttu-id="ad24d-122">Para proteger las llamadas asincrónicas en scripting, establezca la clave del registro en 1.</span><span class="sxs-lookup"><span data-stu-id="ad24d-122">To secure asynchronous calls in scripting, set the registry key to 1.</span></span> <span data-ttu-id="ad24d-123">Los clientes de C++ pueden llamar a [**IWbemUnsecuredApartment:: CreateSinkStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemunsecuredapartment-createsinkstub) para controlar el acceso al receptor.</span><span class="sxs-lookup"><span data-stu-id="ad24d-123">C++ clients can call [**IWbemUnsecuredApartment::CreateSinkStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemunsecuredapartment-createsinkstub) to control access to the sink.</span></span> <span data-ttu-id="ad24d-124">El valor se crea en cualquier parte de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ad24d-124">The value is created anywhere by default.</span></span>

<span data-ttu-id="ad24d-125">En los temas siguientes se proporcionan ejemplos de configuración de la seguridad de llamada asincrónica:</span><span class="sxs-lookup"><span data-stu-id="ad24d-125">The following topics provide examples of setting asynchronous call security:</span></span>

-   [<span data-ttu-id="ad24d-126">Establecer la seguridad en una llamada asincrónica en VBScript</span><span class="sxs-lookup"><span data-stu-id="ad24d-126">Setting Security on an Asynchronous Call in VBScript</span></span>](setting-security-on-an-asynchronous-call-in-vbscript.md)
-   <span data-ttu-id="ad24d-127">Establecer la seguridad de llamadas asincrónicas en C++</span><span class="sxs-lookup"><span data-stu-id="ad24d-127">Setting Asynchronous Call Security in C++</span></span>

## <a name="setting-asynchronous-call-security-in-c"></a><span data-ttu-id="ad24d-128">Establecer la seguridad de llamadas asincrónicas en C++</span><span class="sxs-lookup"><span data-stu-id="ad24d-128">Setting Asynchronous Call Security in C++</span></span>

<span data-ttu-id="ad24d-129">El método [**IWbemUnsecuredApartment:: CreateSinkStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemunsecuredapartment-createsinkstub) es similar al método [**IUnsecuredApartment:: CreateObjectStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iunsecuredapartment-createobjectstub) y crea un receptor en un proceso independiente, Unsecapp.exe, para recibir devoluciones de llamada.</span><span class="sxs-lookup"><span data-stu-id="ad24d-129">The [**IWbemUnsecuredApartment::CreateSinkStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemunsecuredapartment-createsinkstub) method is similar to [**IUnsecuredApartment::CreateObjectStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iunsecuredapartment-createobjectstub) method and creates a sink in a separate process, Unsecapp.exe, to receive callbacks.</span></span> <span data-ttu-id="ad24d-130">Sin embargo, el método **CreateSinkStub** tiene un parámetro *dwFlag* que especifica cómo controla el proceso independiente el control de acceso.</span><span class="sxs-lookup"><span data-stu-id="ad24d-130">However, the **CreateSinkStub** method has a *dwFlag* parameter that specifies how the separate process handles access control.</span></span>

<span data-ttu-id="ad24d-131">El parámetro *dwFlag* especifica una de las siguientes acciones para Unsecapp.exe:</span><span class="sxs-lookup"><span data-stu-id="ad24d-131">The *dwFlag* parameter specifies one of the following actions for Unsecapp.exe:</span></span>

-   <span data-ttu-id="ad24d-132">Utilice la configuración de la clave del registro para determinar si se debe comprobar o no el acceso.</span><span class="sxs-lookup"><span data-stu-id="ad24d-132">Use the registry key setting to determine whether or not to check access.</span></span>
-   <span data-ttu-id="ad24d-133">Omita la clave del registro y compruebe siempre el acceso.</span><span class="sxs-lookup"><span data-stu-id="ad24d-133">Ignore the registry key and always check access.</span></span>
-   <span data-ttu-id="ad24d-134">Omita la clave del registro y no compruebe nunca el acceso.</span><span class="sxs-lookup"><span data-stu-id="ad24d-134">Ignore the registry key and never check access.</span></span>

<span data-ttu-id="ad24d-135">El ejemplo de código de este tema requiere la siguiente \# instrucción include para compilar correctamente.</span><span class="sxs-lookup"><span data-stu-id="ad24d-135">The code example in this topic requires the following \#include statement to correctly compile.</span></span>


```C++
#include <wbemidl.h>
```



<span data-ttu-id="ad24d-136">En el procedimiento siguiente se describe cómo realizar una llamada asincrónica con [**IWbemUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment).</span><span class="sxs-lookup"><span data-stu-id="ad24d-136">The following procedure describes how to perform an asynchronous call with [**IWbemUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment).</span></span>

<span data-ttu-id="ad24d-137">**Para realizar una llamada asincrónica con IWbemUnsecuredApartment**</span><span class="sxs-lookup"><span data-stu-id="ad24d-137">**To perform an asynchronous call with IWbemUnsecuredApartment**</span></span>

1.  <span data-ttu-id="ad24d-138">Cree un proceso dedicado con una llamada a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="ad24d-138">Create a dedicated process with a call to [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="ad24d-139">En el ejemplo de código siguiente se llama a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para crear un proceso dedicado.</span><span class="sxs-lookup"><span data-stu-id="ad24d-139">The following code example calls [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a dedicated process.</span></span>

    ```C++
    CLSID                    CLSID_WbemUnsecuredApartment;
    IWbemUnsecuredApartment* pUnsecApp = NULL;

    CoCreateInstance(CLSID_WbemUnsecuredApartment, 
                     NULL, 
                     CLSCTX_LOCAL_SERVER, 
                     IID_IWbemUnsecuredApartment, 
                     (void**)&pUnsecApp);
    ```

    

2.  <span data-ttu-id="ad24d-140">Cree una instancia del objeto receptor.</span><span class="sxs-lookup"><span data-stu-id="ad24d-140">Instantiate the sink object.</span></span>

    <span data-ttu-id="ad24d-141">En el ejemplo de código siguiente se crea un nuevo objeto receptor.</span><span class="sxs-lookup"><span data-stu-id="ad24d-141">The following code example creates a new sink object.</span></span>

    ```C++
    CMySink* pSink = new CMySink;
    pSink->AddRef();
    ```

    

3.  <span data-ttu-id="ad24d-142">Cree un código auxiliar para el receptor.</span><span class="sxs-lookup"><span data-stu-id="ad24d-142">Create a stub for the sink.</span></span>

    <span data-ttu-id="ad24d-143">Un código auxiliar es una función contenedora generada a partir del receptor.</span><span class="sxs-lookup"><span data-stu-id="ad24d-143">A stub is a wrapper function produced from the sink.</span></span>

    <span data-ttu-id="ad24d-144">En el ejemplo de código siguiente se crea un código auxiliar para el receptor.</span><span class="sxs-lookup"><span data-stu-id="ad24d-144">The following code example creates a stub for the sink.</span></span>

    ```C++
    LPCWSTR          wszReserved = NULL;           
    IWbemObjectSink* pStubSink   = NULL;
    IUnknown*        pStubUnk    = NULL; 

    pUnsecApp->CreateSinkStub(pSink,
                              WBEM_FLAG_UNSECAPP_CHECK_ACCESS,  //Authenticate callbacks regardless of registry key
                              wszReserved,
                              &pStubSink);
    ```

    

4.  <span data-ttu-id="ad24d-145">Libere el puntero del objeto receptor.</span><span class="sxs-lookup"><span data-stu-id="ad24d-145">Release the sink object pointer.</span></span>

    <span data-ttu-id="ad24d-146">Puede liberar el puntero de objeto porque el código auxiliar posee ahora el puntero.</span><span class="sxs-lookup"><span data-stu-id="ad24d-146">You can release the object pointer because the stub now owns the pointer.</span></span>

    <span data-ttu-id="ad24d-147">En el ejemplo de código siguiente se libera el puntero de objeto.</span><span class="sxs-lookup"><span data-stu-id="ad24d-147">The following code example releases the object pointer.</span></span>

    ```C++
    pSink->Release();
    ```

    

5.  <span data-ttu-id="ad24d-148">Use el código auxiliar en cualquier llamada asincrónica.</span><span class="sxs-lookup"><span data-stu-id="ad24d-148">Use the stub in any asynchronous call.</span></span>

    <span data-ttu-id="ad24d-149">Cuando termine con la llamada, libere el recuento de referencias local.</span><span class="sxs-lookup"><span data-stu-id="ad24d-149">When finished with the call, release the local reference count.</span></span>

    <span data-ttu-id="ad24d-150">En el ejemplo de código siguiente se usa el código auxiliar en una llamada asincrónica.</span><span class="sxs-lookup"><span data-stu-id="ad24d-150">The following code example uses the stub in an asynchronous call.</span></span>

    ```C++
    // pServices is an IWbemServices* object
    pServices->CreateInstanceEnumAsync(strClassName, 0, NULL, pStubSink);
    ```

    

    <span data-ttu-id="ad24d-151">En ocasiones, puede que tenga que cancelar una llamada asincrónica después de realizar la llamada.</span><span class="sxs-lookup"><span data-stu-id="ad24d-151">At times you may have to cancel an asynchronous call after you make the call.</span></span> <span data-ttu-id="ad24d-152">Si tiene que cancelar la llamada, cancele la llamada con el mismo puntero que originalmente realizó la llamada.</span><span class="sxs-lookup"><span data-stu-id="ad24d-152">If you need to cancel the call, cancel the call with the same pointer that originally made the call.</span></span>

    <span data-ttu-id="ad24d-153">En el ejemplo de código siguiente se describe cómo cancelar una llamada asincrónica.</span><span class="sxs-lookup"><span data-stu-id="ad24d-153">The following code example describes how to cancel an asynchronous call.</span></span>

    ```C++
    pServices->CancelAsyncCall(pStubSink);
    ```

    

6.  <span data-ttu-id="ad24d-154">Libere el recuento de referencias local cuando haya terminado de usar la llamada asincrónica.</span><span class="sxs-lookup"><span data-stu-id="ad24d-154">Release the local reference count when you are done using the asynchronous call.</span></span>

    <span data-ttu-id="ad24d-155">Asegúrese de liberar el puntero *pStubSink* solo después de confirmar que no se debe cancelar la llamada asincrónica.</span><span class="sxs-lookup"><span data-stu-id="ad24d-155">Make sure to release the *pStubSink* pointer only after you confirm that the asynchronous call does not must be canceled.</span></span> <span data-ttu-id="ad24d-156">Además, no libere *pStubSink* después de que WMI libere el puntero de receptor *pSink* .</span><span class="sxs-lookup"><span data-stu-id="ad24d-156">Further, do not release *pStubSink* after WMI releases the *pSink* sink pointer.</span></span> <span data-ttu-id="ad24d-157">Al liberar *pStubSink* después de *pSink* , se crea un recuento de referencias circulares en el que tanto el receptor como el código auxiliar permanecen en memoria indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="ad24d-157">Releasing *pStubSink* after *pSink* creates a circular reference count in which both the sink and the stub stay in memory forever.</span></span> <span data-ttu-id="ad24d-158">En su lugar, una ubicación posible para liberar el puntero está en la llamada a [**IWbemObjectSink:: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) , realizada por WMI para informar de que se ha completado la llamada asincrónica original.</span><span class="sxs-lookup"><span data-stu-id="ad24d-158">Instead, a possible location to release the pointer is in the [**IWbemObjectSink::SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) call, made by WMI to report that the original asynchronous call is complete.</span></span>

7.  <span data-ttu-id="ad24d-159">Cuando termine, desinicialice COM con una llamada a [**Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span><span class="sxs-lookup"><span data-stu-id="ad24d-159">When finished, uninitialize COM with a call to [**Release()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span></span>

    <span data-ttu-id="ad24d-160">En el ejemplo de código siguiente se muestra cómo llamar a [**Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en el puntero *pUnsecApp* .</span><span class="sxs-lookup"><span data-stu-id="ad24d-160">The following code example shows how to call [**Release()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on the *pUnsecApp* pointer.</span></span>

    ```C++
    pUnsecApp->Release();
    ```

    

<span data-ttu-id="ad24d-161">Para obtener más información acerca de la función [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) y los parámetros, consulte la documentación de [com](../cossdk/component-services-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="ad24d-161">For more information about the [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) function and parameters, see the [COM](../cossdk/component-services-portal.md) documentation.</span></span>

 

 
