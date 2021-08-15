---
description: Una consulta asincrónica, aunque algo más compleja de escribir, es el tipo preferido de consulta cuando el rendimiento del sistema o de la red se verá afectado al consultar un gran grupo de datos.
ms.assetid: b382610a-dac9-4d31-b756-aa84d16f0234
ms.tgt_platform: multiple
title: Invocación de una consulta asincrónica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52ae188e3826562b1de68357db34dca6cea60a40e4be07c16946b13ed3eb3007
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993075"
---
# <a name="invoking-an-asynchronous-query"></a>Invocación de una consulta asincrónica

Una consulta asincrónica, aunque algo más compleja de escribir, es el tipo preferido de consulta cuando el rendimiento del sistema o de la red se verá afectado al consultar un gran grupo de datos. En el script, la creación de un [**objeto SWbemSink**](swbemsink.md) y subrutinas para controlar los eventos que el receptor podría recibir son las únicas tareas adicionales más allá de la consulta básica.

> [!Note]  
> Dado que es posible que la devolución de llamada al receptor no se devuelva en el mismo nivel de autenticación que el cliente requiere, se recomienda usar la comunicación semisincronosa en lugar de la asincrónica. Para obtener más información, vea [Llamar a un método](calling-a-method.md).

 

El siguiente script abreviado consulta todos los archivos de datos del equipo local. Esta consulta podría tardar una cantidad excesiva de tiempo si se ejecutara para todas las máquinas de una red. Se [**configura un objeto SWbemSink**](swbemsink.md) y el único evento que se controla es el evento OnCompleted.


```VB
Sub SINK_OnCompleted(iHResult, objErrorObject, objAsyncContext)
    WScript.Echo "Asynchronous operation is done."
End Sub

Set service = GetObject("winmgmts:")
Set sink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")
service.ExecQueryAsync sink, "SELECT * FROM Win32_DataFile"
WScript.Echo "Waiting for instances."
sink.Cancel()
set sink= Nothing
```



Para obtener información detallada sobre cómo construir llamadas a métodos asincrónicos en el script, vea [Llamar a un método](calling-a-method.md).

En las aplicaciones de C++, una consulta asincrónica genera un proceso independiente para recibir datos de consulta. Una consulta asincrónica es más compleja que una consulta sincrónica, ya que debe codificar una aplicación multiproceso. Sin embargo, una consulta asincrónica no contrae el subproceso principal de la aplicación.

En el procedimiento siguiente se describe cómo realizar una consulta asincrónica en C++.

**Para realizar una consulta asincrónica en C++**

1.  Implemente **un objeto IWbemSink.**

    Un **objeto IWbemSink** recibe información sobre una operación asincrónica.

2.  Describa la consulta en una llamada a [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync).

    WMI mueve inmediatamente el proceso que consulta cim a otro subproceso y libera el subproceso que ejecutó la consulta para otra tarea.

3.  Espere a que WMI llame al [**método IWbemObjectSink::Indicate.**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate)

    Cuando termine, wmi llama a [**Indica**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) para indicar a la aplicación que la consulta está completa. WMI también devuelve los resultados de la consulta al receptor como un puntero a un puntero de [**interfaz IEnumWbemClassObject.**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) Al igual que con una consulta sincrónica, use el puntero para acceder a los objetos que son el resultado de la consulta.

El ejemplo de código siguiente no se compila sin un error porque no se ha definido la clase QuerySink. Para obtener la definición de la clase QuerySink, vea [**IWbemObjectSink**](iwbemobjectsink.md). El ejemplo de código también requiere las siguientes instrucciones reference \# e include.


```C++
#include <iostream>
using namespace std;
#include <wbemidl.h>
```



En el ejemplo de código siguiente se muestra cómo realizar una llamada asincrónica para emitir una consulta.


```C++
void ExecQuery(IWbemServices *pSvc)
{
    // Create a new sink object.
    QuerySink *pSink = new QuerySink;

    // Initialize the query and query language.
    BSTR strQuery = SysAllocString(L"SELECT * FROM ClassName");
    BSTR strQueryLang = SysAllocString(L"WQL");
    
    // Issue the query.
    HRESULT hRes = pSvc->ExecQueryAsync(strQueryLang, strQuery, 0,
        NULL, pSink);

    // Clean up.
    SysFreeString(strQuery);
    SysFreeString(strQueryLang);
    
    if (hRes)
    {
        printf("ExecQueryAsync failed with = 0x%X\n", hRes);
        return;
    }
    
    printf("Completed.\n");
}
```



Para obtener más información, vea [Llamar a un método](calling-a-method.md).

 

 



