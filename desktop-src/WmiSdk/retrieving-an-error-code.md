---
description: Al igual que con todas las aplicaciones, WMI recibe códigos de error del Windows operativo.
ms.assetid: f54b8e7c-c531-47d5-bab8-780652b94555
ms.tgt_platform: multiple
title: Recuperar un código de error
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f16bb7af3c5c2b17d3a99ac00c9122a2ddfa6c075f463819e182fe44193613a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640635"
---
# <a name="retrieving-an-error-code"></a>Recuperar un código de error

Al igual que con todas las aplicaciones, WMI recibe códigos de error del Windows operativo.

Cuando reciba un código de error, tendrá las siguientes opciones:

-   Mire el registro de eventos.

    WMI envía mensajes de error al servicio registro de eventos que comprueba los registros de eventos para ayudar a determinar la causa de un error. Puede usar las clases que admite el proveedor de [registro](/previous-versions/windows/desktop/eventlogprov/event-log-provider) de eventos para acceder a los registros de eventos mediante programación.

-   Recupere el código de error normalmente.

    WMI admite las técnicas estándar para recuperar códigos de error, que son códigos de error COM para C++, y objetos de error nativos, como [Err Object (VBScript)](/previous-versions//sbf5ze0e(v=vs.85))o [**SWbemLastError**](swbemlasterror.md) si el proveedor proporciona información de error.

Para obtener más información, vea [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).

En este tema se de abordan las secciones siguientes:

-   [Control de un error con VBScript](#handling-an-error-with-vbscript)
-   [Controlar un error mediante C++](#handling-an-error-using-c)

## <a name="handling-an-error-with-vbscript"></a>Control de un error con VBScript

Si una llamada a WMI a través de scripting API para WMI produce un error, tiene las siguientes opciones para acceder a la información de error:

-   Use mecanismos de error nativos del lenguaje de scripting, por ejemplo, en VBScript, use [Err Object (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)) para admitir el control de errores.
-   Cree un [**objeto SWbemLastError**](swbemlasterror.md) para obtener un informe de errores.

El siguiente script muestra el uso del [objeto Err nativo (VBScript).](/previous-versions//sbf5ze0e(v=vs.85)) Cuando se da un valor incorrecto para el identificador de proceso, se genera un error.


```VB
On Error Resume Next
Set objProcess = GetObject( _
    "winmgmts:root\cimv2:Win32_Process.Handle='one'")
Wscript.Echo Err.Number
```



> [!Note]
>
> La **propiedad Description** del objeto Err [(VBScript)](/previous-versions//sbf5ze0e(v=vs.85)) está vacía al conectarse a WMI mediante el moniker "winmgmts:". Sin embargo, si se conecta mediante [**SWbemLocator,**](swbemlocator.md)la descripción está disponible.
>
> En la tabla siguiente se enumeran las propiedades de [Err Object (VBScript).](/previous-versions//sbf5ze0e(v=vs.85))
>
> 
>
> | Propiedad                   | Contiene                                                       |
> |----------------------------|----------------------------------------------------------------|
> | **Descripción**<br/> | Descripción localizada y legible del error.<br/> |
> | **Number**<br/>      | **HRESULT devuelto** por scripting API para WMI.<br/>  |
> | **Origen**<br/>      | Identifica el objeto que produjo el error.<br/>        |
>
> 
>
>  

 

El siguiente script muestra el uso de [**un objeto SWbemLastError**](swbemlasterror.md) para obtener información detallada del error. Tenga en cuenta que no todos los proveedores suministran **información a SWbemLastError**. Para obtener más información sobre los códigos de error en el script, [vea WbemErrorEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).


```VB
On Error Resume Next
Set obj = GetObject("winmgmts:root\cimv2:Win32_Process.Handle='one'")
Set LastError = createobject("wbemscripting.swbemlasterror")
Wscript.Echo "Operation = " & LastError.operation & VBCRLF & "ParameterInfo = " _
            & LastError.ParameterInfo & VBCRLF & "ProviderName = " & LastError.ProviderName
```



## <a name="handling-an-error-using-c"></a>Controlar un error mediante C++

Una aplicación cliente WMI puede recibir errores específicos de COM o específicos de WMI. Los errores COM se ajustan a la estructura de los códigos de error COM. Todas las interfaces WMI pueden devolver un error específico de COM, excepto las interfaces [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext), [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject)e [**IWbemQualifierSet.**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) Para obtener más información sobre los códigos de error COM, vea [Control de errores.](../com/error-handling-in-com.md) Las páginas de referencia de las interfaces WMI enumera los códigos de error wmi adecuados en la sección Códigos de error.

Una aplicación cliente debe seguir los estándares COM para comprobar el estado y los códigos de retorno de error. La principal diferencia que debe elegir es si desea recuperar el código de error de una llamada sincrónica, semisincronosa o asincrónica.

**Para acceder a mensajes de error sincrónicos y semisincronosos mediante C++**

1.  Recupere la información de error con una llamada a la función COM [GetErrorInfo.]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo)

    Asegúrese de llamar a [GetErrorInfo inmediatamente]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) después de que un método de interfaz indique un error. Esto incluye cualquiera de los métodos [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) a los que se llama al procesar un proceso semisincronoso.

2.  Examine el objeto de error COM devuelto con una llamada al [**método IErrorInterface::QueryInterface.**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))

    Asegúrese de especificar IID \_ WbemClassObject para el *parámetro riid* en la [**llamada a QueryInterface.**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) El **método QueryInterface** devuelve una instancia de una clase WMI, normalmente [**\_ \_ ExtendedStatus**](--extendedstatus.md).

WMI no entrega el objeto de error a través de [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) para una llamada asincrónica porque no hay ninguna manera de saber cuándo o en qué subproceso se produjo la llamada asincrónica. Por lo tanto, el código solo puede controlar errores específicos o pasar el error de llamada a través de COM.

> [!Note]  
> Dado que es posible que la devolución de llamada al receptor no se devuelva en el mismo nivel de autenticación que el cliente requiere, se recomienda usar la comunicación semisincronosa en lugar de la asincrónica. Para obtener más información, vea [Llamar a un método](calling-a-method.md).

 

**Para acceder a mensajes de error asincrónicos mediante C++**

-   Recupere el objeto de error COM de la implementación de [**IWbemObjectSink::SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus).

    El pseudocódigo siguiente muestra una implementación típica de control de errores para una aplicación cliente.

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

    

 

