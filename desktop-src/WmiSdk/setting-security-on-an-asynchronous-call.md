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
# <a name="setting-security-on-an-asynchronous-call"></a>Establecer la seguridad en una llamada asincrónica

Las llamadas asincrónicas presentan riesgos de seguridad graves porque es posible que una devolución de llamada al [*receptor*](gloss-s.md) no sea el resultado de la llamada asincrónica del script o la aplicación original. La seguridad en las conexiones remotas se basa en el cifrado de la comunicación entre el cliente y el proveedor en el equipo remoto. En C++, puede establecer el cifrado mediante el parámetro de nivel de autenticación en la llamada a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). En scripting, establezca *AuthenticationLevel* en la conexión de moniker o en un objeto [**SWbemSecurity**](swbemsecurity.md) . Para obtener más información, vea [establecer el nivel de seguridad de proceso predeterminado con VBScript](setting-the-default-process-security-level-using-vbscript.md).

Los riesgos de seguridad para las llamadas asincrónicas existen porque WMI reduce el nivel de autenticación en una devolución de llamada hasta que la devolución de llamada se realiza correctamente. En una llamada asincrónica saliente, el cliente puede establecer el nivel de autenticación en la conexión a WMI. WMI recupera la configuración de seguridad en la llamada de cliente e intenta volver a llamar con el mismo nivel de autenticación. La devolución de llamada siempre se inicia en el nivel de **\_ \_ \_ \_ \_ privacidad de nivel de autenticación de RPC C** . Si se produce un error en la devolución de llamada, WMI baja el nivel de autenticación a un nivel en el que la devolución de llamada puede realizarse correctamente, si es necesario, a la **autenticación de RPC \_ C \_ \_ nivel \_ ninguno**. En el contexto de las llamadas dentro del sistema local en las que el servicio de autenticación no es Kerberos, la devolución de llamada siempre se devuelve en el **\_ \_ \_ nivel \_ None de autenticación de RPC C**.

El nivel de autenticación mínimo es el **\_ \_ \_ nivel \_ de autenticación RPC C** (**wbemAuthenticationLevelPkt** para scripting). Sin embargo, puede especificar un nivel superior, como **\_ \_ \_ \_ \_ privacidad de nivel de autenticación de RPC C** (**wbemAuthenticationLevelPktPrivacy**). Se recomienda que las aplicaciones cliente o los scripts establezcan el nivel de autenticación en el nivel **\_ \_ \_ \_ predeterminado** de autenticación de RPC C (**wbemAuthenticationLevelDefault**), lo que permite negociar el nivel de autenticación con el nivel especificado por el servidor.

El valor del registro **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **UnsecAppAccessControlDefault** controla si WMI comprueba un nivel de autenticación aceptable en las devoluciones de llamada. Este es el único mecanismo para proteger la seguridad del receptor de llamadas asincrónicas realizadas en scripting o Visual Basic. De forma predeterminada, esta clave del registro se establece en cero. Si la clave del registro es cero, WMI no comprueba los niveles de autenticación. Para proteger las llamadas asincrónicas en scripting, establezca la clave del registro en 1. Los clientes de C++ pueden llamar a [**IWbemUnsecuredApartment:: CreateSinkStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemunsecuredapartment-createsinkstub) para controlar el acceso al receptor. El valor se crea en cualquier parte de forma predeterminada.

En los temas siguientes se proporcionan ejemplos de configuración de la seguridad de llamada asincrónica:

-   [Establecer la seguridad en una llamada asincrónica en VBScript](setting-security-on-an-asynchronous-call-in-vbscript.md)
-   Establecer la seguridad de llamadas asincrónicas en C++

## <a name="setting-asynchronous-call-security-in-c"></a>Establecer la seguridad de llamadas asincrónicas en C++

El método [**IWbemUnsecuredApartment:: CreateSinkStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemunsecuredapartment-createsinkstub) es similar al método [**IUnsecuredApartment:: CreateObjectStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iunsecuredapartment-createobjectstub) y crea un receptor en un proceso independiente, Unsecapp.exe, para recibir devoluciones de llamada. Sin embargo, el método **CreateSinkStub** tiene un parámetro *dwFlag* que especifica cómo controla el proceso independiente el control de acceso.

El parámetro *dwFlag* especifica una de las siguientes acciones para Unsecapp.exe:

-   Utilice la configuración de la clave del registro para determinar si se debe comprobar o no el acceso.
-   Omita la clave del registro y compruebe siempre el acceso.
-   Omita la clave del registro y no compruebe nunca el acceso.

El ejemplo de código de este tema requiere la siguiente \# instrucción include para compilar correctamente.


```C++
#include <wbemidl.h>
```



En el procedimiento siguiente se describe cómo realizar una llamada asincrónica con [**IWbemUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment).

**Para realizar una llamada asincrónica con IWbemUnsecuredApartment**

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

    Un código auxiliar es una función contenedora generada a partir del receptor.

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

    

4.  Libere el puntero del objeto receptor.

    Puede liberar el puntero de objeto porque el código auxiliar posee ahora el puntero.

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

    

    En ocasiones, puede que tenga que cancelar una llamada asincrónica después de realizar la llamada. Si tiene que cancelar la llamada, cancele la llamada con el mismo puntero que originalmente realizó la llamada.

    En el ejemplo de código siguiente se describe cómo cancelar una llamada asincrónica.

    ```C++
    pServices->CancelAsyncCall(pStubSink);
    ```

    

6.  Libere el recuento de referencias local cuando haya terminado de usar la llamada asincrónica.

    Asegúrese de liberar el puntero *pStubSink* solo después de confirmar que no se debe cancelar la llamada asincrónica. Además, no libere *pStubSink* después de que WMI libere el puntero de receptor *pSink* . Al liberar *pStubSink* después de *pSink* , se crea un recuento de referencias circulares en el que tanto el receptor como el código auxiliar permanecen en memoria indefinidamente. En su lugar, una ubicación posible para liberar el puntero está en la llamada a [**IWbemObjectSink:: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) , realizada por WMI para informar de que se ha completado la llamada asincrónica original.

7.  Cuando termine, desinicialice COM con una llamada a [**Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).

    En el ejemplo de código siguiente se muestra cómo llamar a [**Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en el puntero *pUnsecApp* .

    ```C++
    pUnsecApp->Release();
    ```

    

Para obtener más información acerca de la función [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) y los parámetros, consulte la documentación de [com](../cossdk/component-services-portal.md) .

 

 
