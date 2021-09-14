---
description: Cargar un Graph desde un proceso externo
ms.assetid: 1c657c7f-46d7-4feb-88a7-4a3227c9070b
title: Cargar un Graph desde un proceso externo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eac42db3a87b00b1cb8f3a9ae5297215ae9bd3fa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063209"
---
# <a name="loading-a-graph-from-an-external-process"></a>Cargar un Graph desde un proceso externo

GraphEdit puede cargar un gráfico de filtro creado por un proceso externo. Con esta característica, puede ver exactamente qué gráfico de filtro compila la aplicación, con solo una cantidad mínima de código adicional en la aplicación.

> [!Note]  
> Esta característica requiere Windows 2000, Windows XP o posterior.

 

> [!Note]  
> A partir Windows Vista, debe registrar proppage.dll para habilitar esta característica. Proppage.dll se incluye en el SDK de Windows.

 

La aplicación debe registrar la instancia del gráfico de filtros en la tabla de objetos en ejecución (ROT). ROT es una tabla de consulta accesible globalmente que realiza un seguimiento de los objetos en ejecución. Los objetos se registran en rot mediante moniker. Para conectarse al gráfico, GraphEdit busca monikers en ROT cuyo nombre para mostrar coincide con un formato determinado:


```C++
!FilterGraph X pid Y
```



donde *X* es la dirección hexadecimal del Administrador de Graph filtros e *Y* es el identificador de proceso, también en hexadecimal.

Cuando la aplicación cree por primera vez el gráfico de filtro, llame a la siguiente función:


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



Esta función crea un moniker y una nueva entrada ROT para el gráfico de filtro. El primer parámetro es un puntero al gráfico de filtro. El segundo parámetro recibe un valor que identifica la nueva entrada ROT. Antes de que la aplicación libere el gráfico de filtro, llame a la siguiente función para quitar la entrada ROT. El *parámetro pdwRegister* es el identificador devuelto por la función AddToRot.


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



En el ejemplo de código siguiente se muestra cómo llamar a estas funciones. En este ejemplo, el código que agrega y quita entradas ROT se compila condicionalmente, de modo que solo se incluye en las compilaciones de depuración.


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



Para ver el gráfico de filtros en GraphEdit, ejecute la aplicación y GraphEdit al mismo tiempo. En el menú GraphEdit **File (Editar** archivo), **haga clic Conectar en Remote Graph...** En el **Conectar de diálogo Graph,** seleccione el identificador de proceso (pid) de la aplicación y haga clic en **Aceptar.** GraphEdit carga el gráfico de filtros y lo muestra. No use ninguna otra función de GraphEdit en este grafo, ya que podría provocar resultados inesperados. Por ejemplo, no agregue ni quite filtros, ni detenga e inicie el gráfico. Cierre GraphEdit antes de salir de la aplicación.

> [!Note]  
> La aplicación puede alcanzar varias aserciones cuando se cierra. Puede pasarlos por alto.

 

En la ilustración siguiente se muestra **Conectar cuadro de diálogo Graph** de diálogo.

![conectarse al grafo](images/gedit-spy.png)

Cuando GraphEdit carga el gráfico, se ejecuta en el contexto de la aplicación de destino. Por lo tanto, GraphEdit podría bloquearse porque está esperando el subproceso. Por ejemplo, esto puede ocurrir si está avanzando por el código en el depurador.

Esta característica solo debe usarse en compilaciones de depuración de la aplicación, no en compilaciones comerciales, porque permite que otras aplicaciones puedan ver o controlar el gráfico de filtros.

## <a name="connecting-to-a-remote-graph-from-the-command-line"></a>Conectarse a un Graph remoto desde la línea de comandos

GraphEdit admite una opción de línea de comandos para cargar un gráfico remoto automáticamente al iniciarse. La sintaxis es:


```C++
GraphEdt -a moniker
```



donde *moniker* es un moniker creado mediante la función AddToRot, descrita anteriormente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Simulación de Graph compilar con GraphEdit](simulating-graph-building-with-graphedit.md)
</dt> </dl>

 

 



