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
# <a name="retrieving-an-error-code"></a>Recuperar un código de error

Al igual que con todas las aplicaciones, WMI recibe códigos de error del sistema operativo Windows.

Cuando recibe un código de error, tiene las siguientes opciones:

-   Examine el registro de eventos.

    WMI envía mensajes de error al servicio registro de eventos que comprueba los registros de eventos para ayudar a determinar la causa de un error. Puede utilizar las clases que admite el proveedor de [registro de eventos](/previous-versions/windows/desktop/eventlogprov/event-log-provider) para obtener acceso a los registros de eventos mediante programación.

-   Recupere el código de error normalmente.

    WMI admite las técnicas estándar para recuperar códigos de error, que son códigos de error COM para C++, y objetos de error nativo, como el [objeto ERR (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)), o [**SWbemLastError**](swbemlasterror.md) si el proveedor proporciona información de errores.

Para obtener más información, vea [manipular la información de clase e instancia](manipulating-class-and-instance-information.md).

En este tema se describen las siguientes secciones:

-   [Controlar un error con VBScript](#handling-an-error-with-vbscript)
-   [Controlar un error con C++](#handling-an-error-using-c)

## <a name="handling-an-error-with-vbscript"></a>Controlar un error con VBScript

Si una llamada a WMI a través de la API de scripting para WMI produce un error, tiene las siguientes opciones para obtener acceso a la información de error:

-   Use los mecanismos de error nativos del lenguaje de scripting, por ejemplo, en VBScript use el [objeto ERR (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)) para admitir el control de errores.
-   Cree un objeto [**SWbemLastError**](swbemlasterror.md) para obtener un informe de errores.

El siguiente script muestra el uso del [objeto Err nativo (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)). Cuando se proporciona un valor incorrecto para el identificador de proceso, se genera un error.


```VB
On Error Resume Next
Set objProcess = GetObject( _
    "winmgmts:root\cimv2:Win32_Process.Handle='one'")
Wscript.Echo Err.Number
```



> [!Note]
>
> La propiedad **Description** del [objeto ERR (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)) está vacía al conectarse a WMI a través del moniker "winmgmts:". Sin embargo, si se conecta mediante [**SWbemLocator**](swbemlocator.md), la descripción está disponible.
>
> En la tabla siguiente se enumeran las propiedades del [objeto ERR (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)).
>
> 
>
> | Propiedad                   | Contiene                                                       |
> |----------------------------|----------------------------------------------------------------|
> | **Descripción**<br/> | Descripción localizada y legible del error.<br/> |
> | **Number**<br/>      | **HRESULT** devuelto por la API de scripting para WMI.<br/>  |
> | **Origen**<br/>      | Identifica el objeto que ha generado el error.<br/>        |
>
> 
>
>  

 

El siguiente script muestra el uso de un objeto [**SWbemLastError**](swbemlasterror.md) para obtener información detallada del error. Tenga en cuenta que no todos los proveedores proporcionan información a **SWbemLastError**. Para obtener más información sobre los códigos de error en el script, vea [WbemErrorEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).


```VB
On Error Resume Next
Set obj = GetObject("winmgmts:root\cimv2:Win32_Process.Handle='one'")
Set LastError = createobject("wbemscripting.swbemlasterror")
Wscript.Echo "Operation = " & LastError.operation & VBCRLF & "ParameterInfo = " _
            & LastError.ParameterInfo & VBCRLF & "ProviderName = " & LastError.ProviderName
```



## <a name="handling-an-error-using-c"></a>Controlar un error con C++

Una aplicación cliente de WMI puede recibir errores específicos de COM o específicos de WMI. Los errores COM se ajustan a la estructura de los códigos de error COM. Todas las interfaces WMI pueden devolver un error específico de COM excepto las interfaces [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext), [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject)y [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) . Para obtener más información sobre los códigos de error COM, vea [control de errores](../com/error-handling-in-com.md). Las páginas de referencia de las interfaces WMI enumeran los códigos de error de WMI correspondientes en la sección códigos de error.

Una aplicación cliente debe cumplir los estándares COM para comprobar el estado y los códigos de retorno de error. La principal diferencia que debe elegir es si desea recuperar el código de error de una llamada sincrónica, semisincrónica o asincrónica.

**Para obtener acceso a mensajes de error sincrónicos y semisincrónicos mediante C++**

1.  Recupere la información de error con una llamada a la función com [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) .

    Asegúrese de llamar a [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) inmediatamente después de que un método de interfaz indique un error. Esto incluye cualquiera de los métodos [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) a los que se llama mientras se procesa un proceso semisincrónico.

2.  Examine el objeto de error COM devuelto con una llamada al método [**IErrorInterface:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) .

    Asegúrese de especificar IID \_ WbemClassObject para el parámetro *riid* en la llamada [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) . El método **QueryInterface** devuelve una instancia de una clase WMI, normalmente [**\_ \_ ExtendedStatus**](--extendedstatus.md).

WMI no entrega el objeto de error a través de [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) para una llamada asincrónica porque no hay ninguna manera de saber cuándo, o en qué subproceso se produjo la llamada asincrónica. Por lo tanto, el código solo puede controlar errores específicos o pasar el error de llamada a través de COM.

> [!Note]  
> Dado que la devolución de llamada al receptor podría no devolverse en el mismo nivel de autenticación que requiere el cliente, se recomienda usar semisincrónico en lugar de la comunicación asincrónica. Para obtener más información, consulte [llamar a un método](calling-a-method.md).

 

**Para obtener acceso a mensajes de error asincrónicos mediante C++**

-   Recupere el objeto de error COM de la implementación de [**IWbemObjectSink:: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus).

    En el siguiente pseudocódigo se muestra una implementación de control de errores típica para una aplicación cliente.

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

    

 

