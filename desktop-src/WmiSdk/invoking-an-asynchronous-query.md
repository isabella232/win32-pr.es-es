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
# <a name="invoking-an-asynchronous-query"></a><span data-ttu-id="ee907-103">Invocar una consulta asincrónica</span><span class="sxs-lookup"><span data-stu-id="ee907-103">Invoking an Asynchronous Query</span></span>

<span data-ttu-id="ee907-104">Una consulta asincrónica, aunque algo más compleja de escribir, es el tipo de consulta preferido cuando el rendimiento del sistema o de la red se verá afectado por la consulta de un grupo de datos grande.</span><span class="sxs-lookup"><span data-stu-id="ee907-104">An asynchronous query, while somewhat more complex to write, is the preferred type of query when system or network performance will be affected by querying a large group of data.</span></span> <span data-ttu-id="ee907-105">En el script, la creación de un objeto [**SWbemSink**](swbemsink.md) y subrutinas para controlar los eventos que el receptor podría recibir son las únicas tareas adicionales más allá de la consulta básica.</span><span class="sxs-lookup"><span data-stu-id="ee907-105">In script, creating an [**SWbemSink**](swbemsink.md) object and subroutines to handle the events that the sink could receive are the only additional tasks beyond the basic query.</span></span>

> [!Note]  
> <span data-ttu-id="ee907-106">Dado que la devolución de llamada al receptor podría no devolverse en el mismo nivel de autenticación que requiere el cliente, se recomienda usar semisincrónico en lugar de la comunicación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="ee907-106">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="ee907-107">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="ee907-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

<span data-ttu-id="ee907-108">El siguiente script abreviado consulta todos los archivos de datos en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="ee907-108">The following abbreviated script queries for all of the data files on the local machine.</span></span> <span data-ttu-id="ee907-109">Esta consulta puede tardar una cantidad excesiva de tiempo si se ejecutó para todas las máquinas de una red.</span><span class="sxs-lookup"><span data-stu-id="ee907-109">This query could take an excessive amount of time if it were executed for all of the machines on a network.</span></span> <span data-ttu-id="ee907-110">Se configura un objeto [**SWbemSink**](swbemsink.md) y el único evento que se controla es el evento alcompleted.</span><span class="sxs-lookup"><span data-stu-id="ee907-110">An [**SWbemSink**](swbemsink.md) object is set up and the only event that is handled is the OnCompleted event.</span></span>


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



<span data-ttu-id="ee907-111">Para obtener información detallada sobre cómo construir llamadas a métodos asincrónicos en scripts, vea [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="ee907-111">For detailed information about constructing asynchronous method calls in script, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="ee907-112">En las aplicaciones de C++, una consulta asincrónica genera un proceso independiente para recibir los datos de la consulta.</span><span class="sxs-lookup"><span data-stu-id="ee907-112">In C++ applications, an asynchronous query spawns a separate process to receive query data.</span></span> <span data-ttu-id="ee907-113">Una consulta asincrónica es más compleja que una consulta sincrónica, ya que debe codificar una aplicación multiproceso.</span><span class="sxs-lookup"><span data-stu-id="ee907-113">An asynchronous query is more complex than a synchronous query, as you must code a multithreaded application.</span></span> <span data-ttu-id="ee907-114">Sin embargo, una consulta asincrónica no monopoliza el subproceso principal de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ee907-114">However, an asynchronous query does not monopolize the main thread of your application.</span></span>

<span data-ttu-id="ee907-115">En el procedimiento siguiente se describe cómo realizar una consulta asincrónica en C++.</span><span class="sxs-lookup"><span data-stu-id="ee907-115">The following procedure describes how to perform an asynchronous query in C++.</span></span>

<span data-ttu-id="ee907-116">**Para realizar una consulta asincrónica en C++**</span><span class="sxs-lookup"><span data-stu-id="ee907-116">**To perform an asynchronous query in C++**</span></span>

1.  <span data-ttu-id="ee907-117">Implemente un objeto **IWbemSink** .</span><span class="sxs-lookup"><span data-stu-id="ee907-117">Implement an **IWbemSink** object.</span></span>

    <span data-ttu-id="ee907-118">Un objeto **IWbemSink** recibe información sobre una operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="ee907-118">An **IWbemSink** object receives information about an asynchronous operation.</span></span>

2.  <span data-ttu-id="ee907-119">Describa la consulta en una llamada a [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync).</span><span class="sxs-lookup"><span data-stu-id="ee907-119">Describe your query in a call to [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync).</span></span>

    <span data-ttu-id="ee907-120">WMI mueve inmediatamente el proceso que consulta el CIM a otro subproceso y libera el subproceso que ejecutó la consulta para otra tarea.</span><span class="sxs-lookup"><span data-stu-id="ee907-120">WMI immediately moves the process that queries the CIM to another thread and frees up the thread that executed the query for another task.</span></span>

3.  <span data-ttu-id="ee907-121">Espere a que WMI llame al método [**IWbemObjectSink:: indica**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) .</span><span class="sxs-lookup"><span data-stu-id="ee907-121">Wait for WMI to call the [**IWbemObjectSink::Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) method.</span></span>

    <span data-ttu-id="ee907-122">Una vez finalizado, las llamadas de WMI [**indican**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) a la aplicación que se ha completado la consulta.</span><span class="sxs-lookup"><span data-stu-id="ee907-122">When finished, WMI calls [**Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) to signal your application that the query is complete.</span></span> <span data-ttu-id="ee907-123">WMI también devuelve los resultados de la consulta al receptor como un puntero a un puntero de la interfaz [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) .</span><span class="sxs-lookup"><span data-stu-id="ee907-123">WMI also returns results of the query to the sink as a pointer to an [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) interface pointer.</span></span> <span data-ttu-id="ee907-124">Al igual que con una consulta sincrónica, utilice el puntero para tener acceso a los objetos que componen el resultado de la consulta.</span><span class="sxs-lookup"><span data-stu-id="ee907-124">As with a synchronous query, use the pointer to access the objects that make up the result of your query.</span></span>

<span data-ttu-id="ee907-125">El siguiente ejemplo de código no se compila sin un error porque no se ha definido la clase QuerySink.</span><span class="sxs-lookup"><span data-stu-id="ee907-125">The following code example does not compile without an error because the class QuerySink has not been defined.</span></span> <span data-ttu-id="ee907-126">Para la definición de la clase QuerySink, consulte [**IWbemObjectSink**](iwbemobjectsink.md).</span><span class="sxs-lookup"><span data-stu-id="ee907-126">For the definition of the QuerySink class, see [**IWbemObjectSink**](iwbemobjectsink.md).</span></span> <span data-ttu-id="ee907-127">El ejemplo de código también requiere las siguientes instrucciones de referencia e \# inclusión.</span><span class="sxs-lookup"><span data-stu-id="ee907-127">The code example also requires the following reference and \#include statements.</span></span>


```C++
#include <iostream>
using namespace std;
#include <wbemidl.h>
```



<span data-ttu-id="ee907-128">En el ejemplo de código siguiente se muestra cómo realizar una llamada asincrónica para emitir una consulta.</span><span class="sxs-lookup"><span data-stu-id="ee907-128">The following code example shows how to make an asynchronous call to issue a query.</span></span>


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



<span data-ttu-id="ee907-129">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="ee907-129">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

 



