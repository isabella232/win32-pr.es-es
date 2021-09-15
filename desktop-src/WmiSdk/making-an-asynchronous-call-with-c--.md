---
description: Las aplicaciones WMI escritas en C++ pueden realizar llamadas asincrónicas mediante muchos de los métodos de la interfaz COM IWbemServices.
ms.assetid: 5179969f-bc7d-4408-84ef-7b003950a59f
ms.tgt_platform: multiple
title: Realizar una llamada asincrónica con C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7f093aef4b1a1b4dbede53333e77d737f8efd69
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566837"
---
# <a name="making-an-asynchronous-call-with-c"></a>Realizar una llamada asincrónica con C++

Las aplicaciones WMI escritas en C++ pueden realizar llamadas asincrónicas mediante muchos de los métodos de la interfaz COM [**IWbemServices.**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) Sin embargo, el procedimiento recomendado para llamar [*a*](gloss-p.md) un método [*WMI*](gloss-w.md) o a un método de proveedor es mediante llamadas semisincronosas porque las llamadas semisincronosas son más seguras que las llamadas asincrónicas. Para obtener más información, vea [Realizar una llamada semisincronosa](making-a-semisynchronous-call-with-c--.md) con C++ y Establecer la seguridad en una llamada [asincrónica.](setting-security-on-an-asynchronous-call.md)

En el procedimiento siguiente se describe cómo realizar una llamada asincrónica mediante el receptor en el proceso.

**Para realizar una llamada asincrónica mediante C++**

1.  Implemente [**la interfaz IWbemObjectSink.**](iwbemobjectsink.md)

    Todas las aplicaciones que realicen llamadas asincrónicas deben implementar [**IWbemObjectSink**](iwbemobjectsink.md). Los consumidores de eventos temporales también **implementan IWbemObjectSink para** recibir notificaciones de eventos.

2.  Inicie sesión en el espacio de nombres WMI de destino.

    Las aplicaciones siempre tienen que llamar a la función COM [**CoInitializeSecurity durante**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) la fase de inicialización. Si no lo hacen antes de realizar una llamada asincrónica, WMI libera el receptor de la aplicación sin completar la llamada asincrónica. Para obtener más información, [vea Inicializar COM para una aplicación WMI.](initializing-com-for-a-wmi-application.md)

3.  Establezca la seguridad del receptor.

    Las llamadas asincrónicas crean diversos problemas de seguridad con los que puede que tenga que tratar, por ejemplo, permitiendo el acceso wmi a la aplicación. Para obtener más información, vea [Establecer la seguridad en una llamada asincrónica.](setting-security-on-an-asynchronous-call.md)

4.  Realice la llamada asincrónica.

    El método devuelve inmediatamente con el código **de acierto WBEM \_ S NO \_ \_ ERROR.** La aplicación puede continuar con otras tareas mientras espera a que se complete la operación. WMI informa a la aplicación mediante una llamada a métodos en la [**implementación de IWbemObjectSink**](iwbemobjectsink.md) de la aplicación.

5.  Si es necesario, compruebe periódicamente la implementación para ver si hay actualizaciones.

    Las aplicaciones pueden recibir una notificación del estado intermedio estableciendo el parámetro *lFlags* en la llamada asincrónica a **WBEM \_ FLAG SEND \_ \_ STATUS**. WMI notifica el estado de la llamada estableciendo el parámetro *lFlags* de [**IWbemObjectSink**](iwbemobjectsink.md) en **WBEM \_ STATUS \_ PROGRESS**.

6.  Si es necesario, puede cancelar la llamada antes de que WMI finalice el procesamiento llamando al [**método IWbemServices::CancelCallAsync.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall)

    El [**método CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) cancela el procesamiento asincrónico al liberar inmediatamente el puntero a la [**interfaz IWbemObjectSink**](iwbemobjectsink.md) y garantiza que el puntero se libera antes de que **cancelAsyncCall vuelva.**

    Si usa un objeto contenedor que implementa la interfaz **IUnsecured** para hospedar [**IWbemObjectSink,**](iwbemobjectsink.md)puede encontrar algunas complicaciones adicionales. Dado que la aplicación debe pasar el mismo puntero a [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) que se pasó en la llamada asincrónica original, la aplicación debe mantener en el objeto contenedor hasta que se aclare que no se requiere cancelación. Para obtener más información, vea [Establecer la seguridad en una llamada asincrónica.](setting-security-on-an-asynchronous-call.md)

7.  Cuando termine, limpie los punteros y apague la aplicación.

    WMI proporciona la llamada de estado final a través del [**método SetStatus.**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus)

    > [!Note]  
    > Después de enviar la actualización de estado final, WMI libera el receptor del objeto llamando al **método Release** para la clase que implementa la [**interfaz IWbemObjectSink.**](iwbemobjectsink.md) En el ejemplo anterior, este es el **método QuerySink::Release.** Si desea tener control sobre la duración del objeto receptor, puede implementar el receptor con un recuento de referencias inicial de uno (1).

     

    Si una aplicación cliente pasa la misma interfaz receptora en dos llamadas asincrónicas superpuestas diferentes, WMI no garantiza el orden de la devolución de llamada. Una aplicación cliente que realiza llamadas asincrónicas superpuestas debe pasar objetos receptores diferentes o serializar las llamadas.

En el ejemplo siguiente se requieren las siguientes instrucciones reference \# e include.


```C++
#include <iostream>
using namespace std;
#pragma comment(lib, "wbemuuid.lib")
#include <wbemidl.h>
```



En el ejemplo siguiente se describe cómo realizar una consulta asincrónica mediante el método [**ExecQueryAsync,**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) pero no crea la configuración de seguridad ni libera el objeto [**IWbemObjectSink.**](iwbemobjectsink.md) Para obtener más información, vea [Establecer la seguridad en una llamada asincrónica.](setting-security-on-an-asynchronous-call.md)


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
> El código anterior no se compila sin error porque no se ha definido la clase **QuerySink.** Para obtener más información sobre **QuerySink,** vea [**IWbemObjectSink.**](iwbemobjectsink.md)

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Llamar a un método](calling-a-method.md)
</dt> </dl>

 

 
