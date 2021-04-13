---
description: Cargar un grafo desde un proceso externo
ms.assetid: 1c657c7f-46d7-4feb-88a7-4a3227c9070b
title: Cargar un grafo desde un proceso externo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eac42db3a87b00b1cb8f3a9ae5297215ae9bd3fa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104564421"
---
# <a name="loading-a-graph-from-an-external-process"></a>Cargar un grafo desde un proceso externo

GraphEdit puede cargar un gráfico de filtro creado por un proceso externo. Con esta característica, puede ver exactamente qué gráfico de filtro se compila en la aplicación, con solo una cantidad mínima de código adicional en la aplicación.

> [!Note]  
> Esta característica requiere Windows 2000, Windows XP o posterior.

 

> [!Note]  
> A partir de Windows Vista, debe registrar proppage.dll para habilitar esta característica. Proppage.dll se incluye en el Windows SDK.

 

La aplicación debe registrar la instancia del gráfico de filtro en la tabla de objetos en ejecución (ROT). La ROT es una tabla de búsqueda global accesible que realiza un seguimiento de los objetos en ejecución. Los objetos se registran en la tabla ROT por moniker. Para conectarse al gráfico, GraphEdit busca en la ROT los monikers cuyo nombre para mostrar coincida con un formato determinado:


```C++
!FilterGraph X pid Y
```



donde *X* es la dirección hexadecimal del administrador de gráficos de filtro e *y es el* identificador de proceso, también en formato hexadecimal.

Cuando la aplicación crea primero el gráfico de filtro, llame a la siguiente función:


```C++
HRESULT AddToRot(IUnknown *pUnkGraph, DWORD *pdwRegister) 
{
    IMoniker * pMoniker = NULL;
    IRunningObjectTable *pROT = NULL;

    if (FAILED(GetRunningObjectTable(0, &pROT))) 
    {
        return E_FAIL;
    }
    
    const size_t STRING_LENGTH = 256;

    WCHAR wsz[STRING_LENGTH];
 
   StringCchPrintfW(
        wsz, STRING_LENGTH, 
        L"FilterGraph %08x pid %08x", 
        (DWORD_PTR)pUnkGraph, 
        GetCurrentProcessId()
        );
    
    HRESULT hr = CreateItemMoniker(L"!", wsz, &pMoniker);
    if (SUCCEEDED(hr)) 
    {
        hr = pROT->Register(ROTFLAGS_REGISTRATIONKEEPSALIVE, pUnkGraph,
            pMoniker, pdwRegister);
        pMoniker->Release();
    }
    pROT->Release();
    
    return hr;
}
```



Esta función crea un moniker y una nueva entrada de tabla de texto para el gráfico de filtro. El primer parámetro es un puntero al gráfico de filtro. El segundo parámetro recibe un valor que identifica la nueva entrada de la tabla ROT. Antes de que la aplicación libere el gráfico de filtros, llame a la función siguiente para quitar la entrada de la tabla ROT. El parámetro *pdwRegister* es el identificador devuelto por la función AddToRot.


```C++
void RemoveFromRot(DWORD pdwRegister)
{
    IRunningObjectTable *pROT;
    if (SUCCEEDED(GetRunningObjectTable(0, &pROT))) {
        pROT->Revoke(pdwRegister);
        pROT->Release();
    }
}
```



En el ejemplo de código siguiente se muestra cómo llamar a estas funciones. En este ejemplo, el código que agrega y quita entradas de la tabla ROT se compila condicionalmente, de modo que solo se incluye en las compilaciones de depuración.


```C++
IGraphBuilder *pGraph;
DWORD dwRegister;
    
// Create the filter graph manager.
CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER,
                        IID_IGraphBuilder, (void **)&pGraph);
#ifdef _DEBUG
hr = AddToRot(pGraph, &dwRegister);
#endif

// Rest of the application (not shown).

#ifdef _DEBUG
RemoveFromRot(dwRegister);
#endif
pGraph->Release();
```



Para ver el gráfico de filtro en GraphEdit, ejecute la aplicación y GraphEdit al mismo tiempo. En el menú **archivo** GraphEdit, haga clic en **conectar a gráfico remoto...** En el cuadro de diálogo **conectar con el gráfico** , seleccione el ID. de proceso (PID) de la aplicación y haga clic en **Aceptar**. GraphEdit carga el gráfico de filtro y lo muestra. No use otras características de GraphEdit en este grafo; podría producir resultados inesperados. Por ejemplo, no agregue ni quite filtros, o detenga e inicie el gráfico. Cierre GraphEdit antes de salir de la aplicación.

> [!Note]  
> La aplicación podría alcanzar varias aserciones al salir. Puede pasarlos por alto.

 

En la ilustración siguiente se muestra el cuadro de diálogo **conectar con el gráfico** .

![conectar al grafo](images/gedit-spy.png)

Cuando GraphEdit carga el gráfico, se ejecuta en el contexto de la aplicación de destino. Por lo tanto, GraphEdit podría bloquearse porque está esperando el subproceso. Por ejemplo, esto puede ocurrir si está recorriendo el código en el depurador.

Esta característica solo debe usarse en las compilaciones de depuración de la aplicación, no en las compilaciones comerciales, ya que permite que otras aplicaciones vean o controlen el gráfico de filtro.

## <a name="connecting-to-a-remote-graph-from-the-command-line"></a>Conexión a un grafo remoto desde la línea de comandos

GraphEdit admite una opción de línea de comandos para cargar un grafo remoto automáticamente en el inicio. La sintaxis es la siguiente:


```C++
GraphEdt -a moniker
```



donde *moniker* es un moniker creado mediante la función AddToRot, descrito anteriormente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Simular la compilación de gráficos con GraphEdit](simulating-graph-building-with-graphedit.md)
</dt> </dl>

 

 



