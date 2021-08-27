---
description: Las llamadas asincrónicas presentan riesgos de seguridad graves porque una devolución de llamada al receptor puede no ser el resultado de la llamada asincrónica por parte de la aplicación o script original.
ms.assetid: 2b839ea9-e1e6-4123-a98a-04ebee907b3b
ms.tgt_platform: multiple
title: Establecer la seguridad en una llamada asincrónica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 228dbf5d84a85f28d5d57afb12823c93c95f9b259ebe95a15e949eec10543d84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992335"
---
# <a name="setting-security-on-an-asynchronous-call"></a>Establecer la seguridad en una llamada asincrónica

Las llamadas asincrónicas presentan riesgos de [](gloss-s.md) seguridad graves porque una devolución de llamada al receptor puede no ser el resultado de la llamada asincrónica por parte de la aplicación o script original. La seguridad en las conexiones remotas se basa en el cifrado de la comunicación entre el cliente y el proveedor en el equipo remoto. En C++ puede establecer el cifrado a través del parámetro de nivel de autenticación en la llamada a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). En scripting, establezca *AuthenticationLevel en* la conexión del moniker o en un [**objeto SWbemSecurity.**](swbemsecurity.md) Para obtener más información, vea [Establecer el nivel de seguridad de proceso predeterminado mediante VBScript.](setting-the-default-process-security-level-using-vbscript.md)

Los riesgos de seguridad para las llamadas asincrónicas existen porque WMI reduce el nivel de autenticación en una devolución de llamada hasta que la devolución de llamada se realiza correctamente. En una llamada asincrónica saliente, el cliente puede establecer el nivel de autenticación en la conexión a WMI. WMI recupera la configuración de seguridad en la llamada de cliente e intenta volver a llamar a con el mismo nivel de autenticación. La devolución de llamada siempre se inicia en el nivel DE PRIVACIDAD PKT DE **RPC \_ C \_ \_ AUTHN LEVEL. \_ \_** Si se produce un error en la devolución de llamada, WMI reduce el nivel de autenticación a un nivel en el que la devolución de llamada puede realizarse correctamente, si es necesario, a **RPC \_ C \_ AUTHN \_ LEVEL \_ NONE**. En el contexto de las llamadas dentro del sistema local donde el servicio de autenticación no es Kerberos, la devolución de llamada siempre se devuelve en **RPC \_ C \_ AUTHN \_ LEVEL \_ NONE**.

El nivel de autenticación mínimo **es RPC \_ C \_ AUTHN \_ LEVEL \_ PKT** **(wbemAuthenticationLevelPkt** para scripting). Sin embargo, puede especificar un nivel superior, como **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY** (**wbemAuthenticationLevelPktPrivacy**). Se recomienda que los scripts o aplicaciones cliente establezcan el nivel de autenticación en **RPC \_ C \_ AUTHN \_ LEVEL \_ DEFAULT** (**wbemAuthenticationLevelDefault**), lo que permite negociar el nivel de autenticación al nivel especificado por el servidor.

El valor del Registro **HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **UnsecAppAccessControlDefault** controla si WMI busca un nivel de autenticación aceptable en las devoluciones de llamada. Este es el único mecanismo para proteger la seguridad del receptor para las llamadas asincrónicas realizadas en scripts o Visual Basic. De forma predeterminada, esta clave del Registro se establece en cero. Si la clave del Registro es cero, WMI no comprueba los niveles de autenticación. Para proteger las llamadas asincrónicas en scripting, establezca la clave del Registro en 1. Los clientes de C++ pueden llamar [**a IWbemUnsecuredControl::CreateSinkStub para**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemunsecuredapartment-createsinkstub) controlar el acceso al receptor. El valor se crea en cualquier lugar de forma predeterminada.

En los temas siguientes se proporcionan ejemplos de configuración de la seguridad de llamadas asincrónicas:

-   [Establecer la seguridad en una llamada asincrónica en VBScript](setting-security-on-an-asynchronous-call-in-vbscript.md)
-   Establecer la seguridad de llamadas asincrónicas en C++

## <a name="setting-asynchronous-call-security-in-c"></a>Establecer la seguridad de llamadas asincrónicas en C++

El [**método IWbemUnsecuredChev::CreateSinkStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemunsecuredapartment-createsinkstub) es similar al método [**IUnsecuredChev::CreateObjectStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iunsecuredapartment-createobjectstub) y crea un receptor en un proceso independiente, Unsecapp.exe, para recibir devoluciones de llamada. Sin embargo, **el método CreateSinkStub** tiene un *parámetro dwFlag* que especifica cómo controla el control de acceso el proceso independiente.

El *parámetro dwFlag* especifica una de las siguientes acciones para Unsecapp.exe:

-   Use la configuración de clave del Registro para determinar si se debe comprobar o no el acceso.
-   Ignore la clave del Registro y compruebe siempre el acceso.
-   Ignore la clave del Registro y nunca compruebe el acceso.

El ejemplo de código de este tema requiere que la \# siguiente instrucción include se compile correctamente.


```C++
#include <wbemidl.h>
```



En el procedimiento siguiente se describe cómo realizar una llamada asincrónica con [**IWbemUnsecuredWb**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment).

**Para realizar una llamada asincrónica con IWbemUnsecuredWb**

1.  Cree un proceso dedicado con una llamada a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

    En el ejemplo de código siguiente se llama a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para crear un proceso dedicado.

    ```C++
    CLSID                    CLSID_WbemUnsecuredApartment;
    IWbemUnsecuredApartment* pUnsecApp = NULL;

    CoCreateInstance(CLSID_WbemUnsecuredApartment, 
                     NULL, 
                     CLSCTX_LOCAL_SERVER, 
                     IID_IWbemUnsecuredApartment, 
                     (void**)&pUnsecApp);
    ```

    

2.  Cree una instancia del objeto receptor.

    En el ejemplo de código siguiente se crea un nuevo objeto receptor.

    ```C++
    CMySink* pSink = new CMySink;
    pSink->AddRef();
    ```

    

3.  Cree un código auxiliar para el receptor.

    Un código auxiliar es una función contenedora producida a partir del receptor.

    En el ejemplo de código siguiente se crea un código auxiliar para el receptor.

    ```C++
    LPCWSTR          wszReserved = NULL;           
    IWbemObjectSink* pStubSink   = NULL;
    IUnknown*        pStubUnk    = NULL; 

    pUnsecApp->CreateSinkStub(pSink,
                              WBEM_FLAG_UNSECAPP_CHECK_ACCESS,  //Authenticate callbacks regardless of registry key
                              wszReserved,
                              &pStubSink);
    ```

    

4.  Suelte el puntero de objeto receptor.

    Puede liberar el puntero de objeto porque el código auxiliar ahora posee el puntero.

    En el ejemplo de código siguiente se libera el puntero de objeto.

    ```C++
    pSink->Release();
    ```

    

5.  Use el código auxiliar en cualquier llamada asincrónica.

    Cuando termine con la llamada, libere el recuento de referencias local.

    En el ejemplo de código siguiente se usa el código auxiliar en una llamada asincrónica.

    ```C++
    // pServices is an IWbemServices* object
    pServices->CreateInstanceEnumAsync(strClassName, 0, NULL, pStubSink);
    ```

    

    En ocasiones, es posible que tenga que cancelar una llamada asincrónica después de realizar la llamada. Si necesita cancelar la llamada, cancele la llamada con el mismo puntero que realizó originalmente la llamada.

    En el ejemplo de código siguiente se describe cómo cancelar una llamada asincrónica.

    ```C++
    pServices->CancelAsyncCall(pStubSink);
    ```

    

6.  Libere el recuento de referencias locales cuando haya terminado con la llamada asincrónica.

    Asegúrese de liberar el puntero *pStubSink* solo después de confirmar que no se debe cancelar la llamada asincrónica. Además, no libere *pStubSink después* de que WMI libere el puntero de receptor *pSink.* Al liberar *pStubSink después* de *pSink,* se crea un recuento circular de referencias en el que tanto el receptor como el código auxiliar permanecen en memoria para siempre. En su lugar, una posible ubicación para liberar el puntero se encuentra en la llamada [**IWbemObjectSink::SetStatus,**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) realizada por WMI para informar de que la llamada asincrónica original se ha completado.

7.  Cuando termine, desinicialice COM con una llamada a [**Release().**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)

    En el ejemplo de código siguiente se muestra cómo llamar [**a Release()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en el *puntero pUnsecApp.*

    ```C++
    pUnsecApp->Release();
    ```

    

Para obtener más información sobre la [**función CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) y los parámetros, consulte la [documentación de COM.](../cossdk/component-services-portal.md)

 

 
