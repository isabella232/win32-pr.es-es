---
description: Una consulta asincrónica, aunque algo más compleja de escribir, es el tipo de consulta preferido cuando el rendimiento del sistema o de la red se verá afectado por la consulta de un grupo de datos grande.
ms.assetid: b382610a-dac9-4d31-b756-aa84d16f0234
ms.tgt_platform: multiple
title: Invocar una consulta asincrónica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a0e297c6a1955d0006d888fc95f5e827f5cb75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913365"
---
# <a name="invoking-an-asynchronous-query"></a>Invocar una consulta asincrónica

Una consulta asincrónica, aunque algo más compleja de escribir, es el tipo de consulta preferido cuando el rendimiento del sistema o de la red se verá afectado por la consulta de un grupo de datos grande. En el script, la creación de un objeto [**SWbemSink**](swbemsink.md) y subrutinas para controlar los eventos que el receptor podría recibir son las únicas tareas adicionales más allá de la consulta básica.

> [!Note]  
> Dado que la devolución de llamada al receptor podría no devolverse en el mismo nivel de autenticación que requiere el cliente, se recomienda usar semisincrónico en lugar de la comunicación asincrónica. Para obtener más información, consulte [llamar a un método](calling-a-method.md).

 

El siguiente script abreviado consulta todos los archivos de datos en el equipo local. Esta consulta puede tardar una cantidad excesiva de tiempo si se ejecutó para todas las máquinas de una red. Se configura un objeto [**SWbemSink**](swbemsink.md) y el único evento que se controla es el evento alcompleted.


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



Para obtener información detallada sobre cómo construir llamadas a métodos asincrónicos en scripts, vea [llamar a un método](calling-a-method.md).

En las aplicaciones de C++, una consulta asincrónica genera un proceso independiente para recibir los datos de la consulta. Una consulta asincrónica es más compleja que una consulta sincrónica, ya que debe codificar una aplicación multiproceso. Sin embargo, una consulta asincrónica no monopoliza el subproceso principal de la aplicación.

En el procedimiento siguiente se describe cómo realizar una consulta asincrónica en C++.

**Para realizar una consulta asincrónica en C++**

1.  Implemente un objeto **IWbemSink** .

    Un objeto **IWbemSink** recibe información sobre una operación asincrónica.

2.  Describa la consulta en una llamada a [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync).

    WMI mueve inmediatamente el proceso que consulta el CIM a otro subproceso y libera el subproceso que ejecutó la consulta para otra tarea.

3.  Espere a que WMI llame al método [**IWbemObjectSink:: indica**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) .

    Una vez finalizado, las llamadas de WMI [**indican**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) a la aplicación que se ha completado la consulta. WMI también devuelve los resultados de la consulta al receptor como un puntero a un puntero de la interfaz [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) . Al igual que con una consulta sincrónica, utilice el puntero para tener acceso a los objetos que componen el resultado de la consulta.

El siguiente ejemplo de código no se compila sin un error porque no se ha definido la clase QuerySink. Para la definición de la clase QuerySink, consulte [**IWbemObjectSink**](iwbemobjectsink.md). El ejemplo de código también requiere las siguientes instrucciones de referencia e \# inclusión.


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



Para obtener más información, consulte [llamar a un método](calling-a-method.md).

 

 



