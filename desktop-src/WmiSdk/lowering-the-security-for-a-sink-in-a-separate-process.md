---
description: Instrumental de administración de Windows (WMI) puede crear el receptor para recibir devoluciones de llamada asincrónicas para una aplicación cliente en un proceso independiente.
ms.assetid: 3d3111ac-7d83-48d6-94e4-36cb46a506fa
ms.tgt_platform: multiple
title: Reducir la seguridad de un receptor en un proceso independiente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63aec8bcb451d254961acae8278cb45cb4454f37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697366"
---
# <a name="lowering-the-security-for-a-sink-in-a-separate-process"></a>Reducir la seguridad de un receptor en un proceso independiente

Instrumental de administración de Windows (WMI) puede crear el receptor para recibir devoluciones de llamada asincrónicas para una aplicación cliente en un proceso independiente. El proceso independiente se Unsecapp.exe. Use la interfaz [**IWbemUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment) . **IWbemUnsecuredApartment** permite controlar si Unsecapp.exe autentica las devoluciones de llamada en el receptor. Para obtener más información, vea [establecer la seguridad en una llamada asincrónica](setting-security-on-an-asynchronous-call.md).

Después, puede reducir la seguridad en ese proceso y WMI puede tener acceso al receptor sin restricciones. Para ayudar a esta técnica, WMI proporciona el proceso de Unsecapp.exe para que funcione como proceso independiente. Puede hospedar Unsecapp.exe con una llamada a la interfaz [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment) .

La interfaz [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment) permite a una aplicación cliente crear un proceso dedicado independiente que ejecute Unsecapp.exe para hospedar una implementación de [**IWbemObjectSink**](iwbemobjectsink.md) . El proceso dedicado puede llamar a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) para conceder acceso a WMI al proceso dedicado sin poner en peligro la seguridad del proceso principal. Después de la inicialización, el proceso dedicado actúa como intermediario entre el proceso principal y WMI.

En el procedimiento siguiente se describe cómo realizar una llamada asincrónica con [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment).

**Para realizar una llamada asincrónica con IUnsecuredApartment**

1.  Cree un proceso dedicado con una llamada a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

    En el ejemplo de código siguiente se llama a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para crear un proceso dedicado.

    ```C++
    IUnsecuredApartment* pUnsecApp = NULL;

    CoCreateInstance(CLSID_UnsecuredApartment, NULL, 
      CLSCTX_LOCAL_SERVER, IID_IUnsecuredApartment, 
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

    En el ejemplo de código siguiente se llama a [**CreateObjectStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iunsecuredapartment-createobjectstub) para crear un código auxiliar para el receptor.

    ```C++
    IUnknown* pStubUnk = NULL; 
    pUnsecApp->CreateObjectStub(pSink, &pStubUnk);
    ```

    

4.  Llame a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para el contenedor y solicite un puntero a la interfaz [**IWbemObjectSink**](iwbemobjectsink.md) .

    En el ejemplo de código siguiente se llama a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) y se solicita un puntero a la interfaz [**IWbemObjectSink**](iwbemobjectsink.md) .

    ```C++
    IWbemObjectSink* pStubSink = NULL;
    pStubUnk->QueryInterface(IID_IWbemObjectSink, (void **)&pStubSink); pStubUnk->Release();
    ```

    

5.  Libere el puntero del objeto receptor.

    Puede liberar el puntero de objeto porque el código auxiliar posee ahora el puntero.

    En el ejemplo de código siguiente se libera el puntero del objeto receptor.

    ```C++
    pSink->Release();
    ```

    

6.  Use el código auxiliar en cualquier llamada asincrónica.

    Cuando termine con la llamada, libere el recuento de referencias local.

    En el ejemplo de código siguiente se usa el código auxiliar en una llamada asincrónica.

    ```C++
    // pServices is an IWbemServices* object
    pServices->CreateInstanceEnumAsync(strClassName, 0, NULL, pStubSink);
    ```

    

    En ocasiones, puede que tenga que cancelar una llamada asincrónica después de realizar la llamada. Si tiene que cancelar la llamada, cancele la llamada con el mismo puntero que originalmente realizó la llamada.

    En el ejemplo de código siguiente se muestra cómo cancelar una llamada asincrónica.

    ```C++
    pServices->CancelAsyncCall(pStubSink);
    ```

    

7.  Libere el recuento de referencias local cuando haya terminado de usar la llamada asincrónica.

    Asegúrese de liberar el puntero *pStubSink* solo después de confirmar que no es necesario cancelar la llamada asincrónica. Además, no libere *pStubSink* después de que WMI libere el puntero de receptor *pSink* . Al liberar *pStubSink* después de *pSink* , se crea un recuento de referencias circulares en el que tanto el receptor como el código auxiliar permanecen en memoria indefinidamente. En su lugar, una ubicación posible para liberar el puntero está en la llamada a [**IWbemObjectSink:: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) , realizada por WMI para informar de que se ha completado la llamada asincrónica original.

8.  Cuando termine, desinicialice COM con una llamada a [**Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).

    En el ejemplo de código siguiente se muestra cómo llamar a [**Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en el puntero *pUnsecApp* .

    ```C++
    pUnsecApp->Release();
    ```

    

    Los ejemplos de código de este tema requieren la siguiente referencia e \# instrucción include para compilar correctamente.

    ```C++
    #include <wbemidl.h>
    #pragma comment(lib, "wbemuuid.lib")
    ```

    

Para obtener más información sobre la función [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) y los parámetros, consulte la documentación de [com](../cossdk/component-services-portal.md) en el kit de desarrollo de software (SDK) de la plataforma.

 

 
