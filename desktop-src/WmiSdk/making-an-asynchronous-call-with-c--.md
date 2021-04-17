---
description: Las aplicaciones WMI escritas en C++ pueden realizar llamadas asincrónicas mediante muchos de los métodos de la interfaz COM IWbemServices.
ms.assetid: 5179969f-bc7d-4408-84ef-7b003950a59f
ms.tgt_platform: multiple
title: Realización de una llamada asincrónica con C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7f093aef4b1a1b4dbede53333e77d737f8efd69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717127"
---
# <a name="making-an-asynchronous-call-with-c"></a>Realización de una llamada asincrónica con C++

Las aplicaciones WMI escritas en C++ pueden realizar llamadas asincrónicas mediante muchos de los métodos de la interfaz com [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) . Sin embargo, el procedimiento recomendado para llamar a un [*método WMI*](gloss-w.md) o a un [*método de proveedor*](gloss-p.md) es mediante llamadas semisincrónicas, ya que las llamadas sincrónicas son más seguras que las llamadas asincrónicas. Para obtener más información, vea [crear una llamada semisincrónica con C++](making-a-semisynchronous-call-with-c--.md) y [establecer la seguridad en una llamada asincrónica](setting-security-on-an-asynchronous-call.md).

En el procedimiento siguiente se describe cómo hacer una llamada asincrónica mediante el uso del receptor en el proceso.

**Para hacer una llamada asincrónica con C++**

1.  Implemente la interfaz [**IWbemObjectSink**](iwbemobjectsink.md) .

    Todas las aplicaciones que realizan llamadas asincrónicas deben implementar [**IWbemObjectSink**](iwbemobjectsink.md). Los consumidores de eventos temporales también implementan **IWbemObjectSink** para recibir notificaciones de eventos.

2.  Inicie sesión en el espacio de nombres WMI de destino.

    Las aplicaciones siempre tienen que llamar a la función COM [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) durante la fase de inicialización. Si no lo hacen antes de realizar una llamada asincrónica, WMI libera el receptor de la aplicación sin completar la llamada asincrónica. Para obtener más información, vea [inicializar com para una aplicación WMI](initializing-com-for-a-wmi-application.md).

3.  Establezca la seguridad del receptor.

    Las llamadas asincrónicas crean una variedad de problemas de seguridad que es posible que tenga que tratar, por ejemplo, para permitir el acceso de WMI a la aplicación. Para obtener más información, vea [establecer la seguridad en una llamada asincrónica](setting-security-on-an-asynchronous-call.md).

4.  Realice la llamada asincrónica.

    El método se devuelve inmediatamente con el código de **\_ \_ \_ error de WBEM S** . La aplicación puede continuar con otras tareas mientras espera a que se complete la operación. WMI informa de nuevo a la aplicación llamando a métodos en la implementación de [**IWbemObjectSink**](iwbemobjectsink.md) de la aplicación.

5.  Si es necesario, Compruebe la implementación periódicamente en busca de actualizaciones.

    Las aplicaciones pueden recibir notificaciones de estado intermedio estableciendo el parámetro *lFlags* en la llamada asincrónica al **\_ \_ \_ Estado de envío de la marca WBEM**. WMI informa del estado de la llamada estableciendo el parámetro *lFlags* de [**IWbemObjectSink**](iwbemobjectsink.md) en el **\_ \_ progreso de estado de WBEM**.

6.  Si es necesario, puede cancelar la llamada antes de que WMI finalice el procesamiento llamando al método [**IWbemServices:: CancelCallAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) .

    El método [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) cancela el procesamiento asincrónico liberando inmediatamente el puntero a la interfaz [**IWbemObjectSink**](iwbemobjectsink.md) y garantiza que el puntero se libera antes de que **CancelAsyncCall** devuelva.

    Si usa un objeto contenedor que implementa la interfaz **IUnsecured** para hospedar [**IWbemObjectSink**](iwbemobjectsink.md), es posible que encuentre algunas complicaciones adicionales. Dado que la aplicación debe pasar el mismo puntero a [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) que se pasó en la llamada asincrónica original, la aplicación debe mantener el objeto contenedor hasta que quede claro que no se requiere la cancelación. Para obtener más información, vea [establecer la seguridad en una llamada asincrónica](setting-security-on-an-asynchronous-call.md).

7.  Cuando termine, limpie los punteros y apague la aplicación.

    WMI proporciona la llamada de estado final a través del método [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) .

    > [!Note]  
    > Después de enviar la actualización de estado final, WMI libera el receptor del objeto llamando al método **Release** para la clase que implementa la interfaz [**IWbemObjectSink**](iwbemobjectsink.md) . En el ejemplo anterior, este es el método **QuerySink:: Release** . Si desea tener control sobre la duración del objeto receptor, puede implementar el receptor con un recuento de referencias inicial de uno (1).

     

    Si una aplicación cliente pasa la misma interfaz de receptor en dos llamadas asincrónicas diferentes que se superponen, WMI no garantiza el orden de la devolución de llamada. Una aplicación cliente que realiza llamadas asincrónicas superpuestas debe pasar objetos receptores diferentes o serializar las llamadas.

El siguiente ejemplo requiere las siguientes instrucciones de referencia e \# inclusión.


```C++
#include <iostream>
using namespace std;
#pragma comment(lib, "wbemuuid.lib")
#include <wbemidl.h>
```



En el ejemplo siguiente se describe cómo realizar una consulta asincrónica mediante el método [**ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) , pero no se crea la configuración de seguridad ni se libera el objeto [**IWbemObjectSink**](iwbemobjectsink.md) . Para obtener más información, vea [establecer la seguridad en una llamada asincrónica](setting-security-on-an-asynchronous-call.md).


```C++
// Set input parameters to ExecQueryAsync.
BSTR QueryLang = SysAllocString(L"WQL");
BSTR Query = SysAllocString(L"SELECT * FROM MyClass");

// Create IWbemObjectSink object and set pointer.
QuerySink *pSink = new QuerySink;

IWbemServices* pSvc = 0;

// Call ExecQueryAsync.
HRESULT hRes = pSvc->ExecQueryAsync(QueryLang, 
                                    Query, 
                                    0, 
                                    NULL, 
                                    pSink);

// Check for errors.
if (hRes)
{
    printf("ExecQueryAsync failed with = 0x%X\n", hRes);
    SysFreeString(QueryLang);
    SysFreeString(Query);
    delete pSink;    
    return ERROR;
}
```



> [!Note]  
> El código anterior no se compila sin errores porque no se ha definido la clase **QuerySink** . Para obtener más información sobre **QuerySink**, consulte [**IWbemObjectSink**](iwbemobjectsink.md).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Llamar a un método](calling-a-method.md)
</dt> </dl>

 

 
