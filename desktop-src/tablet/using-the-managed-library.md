---
description: Información general de la biblioteca administrada y notas sobre el uso de la biblioteca administrada de la plataforma de Tablet PC.
ms.assetid: d283ea1c-faf3-4222-a9a7-c67087636b86
title: Uso de la biblioteca administrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d1241787b680045d6c84b440717ced5426e4352d8c280ef58c1bb7f75c9fc66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449258"
---
# <a name="using-the-managed-library"></a>Uso de la biblioteca administrada

Common Language Runtime es la base de microsoft .NET Framework. Puede pensar en Common Language Runtime como un agente que administra el código en tiempo de ejecución, proporcionando servicios básicos como la administración de memoria, la administración de subprocesos y la comunicación remota, a la vez que se fuerza una seguridad de código estricta. De hecho, el concepto de administración de código es un principio fundamental de Common Language Runtime. El código que tiene como destino Common Language Runtime se conoce como código administrado. El código que no tiene como destino Common Language Runtime se conoce como código nativo.

La biblioteca de clases Framework es una colección completa orientada a objetos de clases reutilizables que puede usar para desarrollar aplicaciones que abarcan desde aplicaciones tradicionales de la línea de comandos o de la interfaz gráfica de usuario (GUI) hasta aplicaciones basadas en las últimas innovaciones proporcionadas por ASP.NET y servicios web.

La biblioteca administrada de Tablet PC contiene un conjunto de objetos administrados que amplía el marco de trabajo para proporcionar compatibilidad con la entrada y salida de escritura a mano en Tablet PC, así como el intercambio de datos con otros equipos.

## <a name="exceptions"></a>Excepciones

Los objetos de biblioteca administrada de Tablet PC API encapsulan las implementaciones de la biblioteca COM. Cuando el objeto o control de la biblioteca COM subyacente devuelve un error, la API administrada producirá una excepción Marshal.ThrowExceptionForHR que proporciona los detalles sobre la excepción COM interna. Puede consultar los valores HRESULT en la Referencia de la biblioteca COM para obtener más información sobre los posibles errores que se pueden devolver.

## <a name="object-comparison"></a>Comparación de objetos

Para todos los objetos de la biblioteca administrada de la plataforma de Tablet PC, [**Equals**](/previous-versions/windows/) no se invalida para comparar correctamente dos objetos que son iguales. La interfaz de programación de aplicaciones administradas (API) no admite la comparación de objetos para la igualdad, ya sea a través de la función **Equals** o mediante el operador equals (==).

## <a name="binding-to-the-latest-microsoftinkdll"></a>Enlace al último Microsoft.Ink.dll

El ensamblado Microsoft.Ink.dll más reciente es un reemplazo compatible para Microsoft.Ink.dll versión 1.0 y Microsoft.Ink.15.dll. En la mayoría de los casos, no es necesario realizar ningún cambio en las aplicaciones que se distribuyen con los ensamblados anteriores. Sin embargo, en algunos casos debe indicar al cargador de Common Language Runtime que use la biblioteca de vínculos dinámicos (DLL) más reciente siempre que se haga referencia a los archivos DLL anteriores.

La única vez que necesita enlazar explícitamente al nuevo ensamblado mediante la técnica siguiente es si la aplicación usa un componente que hace referencia al ensamblado de la versión 1.0 o 1.5 en combinación con un componente que hace referencia a un ensamblado de versión más reciente, como 1.7, y si esos componentes pueden intercambiar datos.

La mejor manera de indicar al cargador de Common Language Runtime que use el archivo DLL más reciente es redirigir las versiones de ensamblado en el nivel de aplicación. Puede especificar que la aplicación use la versión más reciente del ensamblado colocando información de enlace de ensamblado en el archivo de configuración de la aplicación. Para obtener más información sobre cómo redirigir las versiones de ensamblado en el nivel de aplicación, vea Redirigir versiones de ensamblado [,](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconassemblyversionredirection.asp%3fframe%3dtrue)en concreto la sección "Especificar el enlace de ensamblado en archivos de configuración".

Deberá crear un archivo de configuración en el mismo directorio que el archivo ejecutable. El archivo de configuración debe tener el mismo nombre que el ejecutable, seguido de la extensión .config archivo. Por ejemplo, para una aplicación, MyApp.exe, el archivo de configuración debe ser MyApp.exe.config archivo. El archivo de configuración usa un [elemento bindingRedirect](/previous-versions/dotnet/netframework-1.1/eftw1fys(v=vs.71)) para forzar que todas las versiones anteriores se asignen a la versión más reciente, como se muestra en el ejemplo siguiente:

`<bindingRedirect oldVersion="0.0.0.0-1.7.2600.xxxx" newVersion="1.7.2600.xxxx" />`

Para obtener más información sobre los archivos de configuración, incluidos ejemplos de cómo construir el lenguaje de marcado extensible (XML) para el archivo de configuración, vea [bindingRedirect](/previous-versions/dotnet/netframework-1.1/eftw1fys(v=vs.71)) y [Redirecting Assembly Versions](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconassemblyversionredirection.asp%3fframe%3dtrue).

Las aplicaciones creadas con Microsoft Windows XP Tablet PC Edition Development Kit 1.7 y versiones posteriores se enlazan automáticamente a la nueva versión del ensamblado Microsoft.Ink. Para obtener más información sobre el enlace de ensamblados, [vea How the Runtime Locates Assemblies](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconHowRuntimeLocatesAssemblies.asp).

> [!Note]  
> El uso de la directiva de aplicación para enlazar al ensamblado actualizado no funciona para las aplicaciones que usan la clase [Divider](/previous-versions/ms583616(v=vs.100)) o [la clase PenInputPanel.](/previous-versions/aa514041(v=msdn.10)) Las aplicaciones que usan cualquiera de esas clases deben seguir usando Microsoft.Ink.15.dll o volver a compilarse después de hacer referencia al ensamblado actualizado.

 

## <a name="working-with-events"></a>Trabajar con eventos

Si el código de un controlador de eventos para cualquiera de los objetos administrados produce una excepción, la excepción no se entrega al usuario. Para asegurarse de que se entregan excepciones, use bloques try-catch en los controladores de eventos para eventos administrados.

## <a name="managing-forms"></a>Administrar formularios

La [clase Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) y sus clases base no definen un finalizador. Para limpiar los recursos en un formulario, escriba una subclase que proporciona un finalizador (por ejemplo, el destructor de C mediante ~) que llama a \# [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1). Para realizar la limpieza, el finalizador invalida Dispose y, a continuación, llama a la clase base Dispose. No haga referencia a otros objetos que requieran el método [Finalize](/previous-versions/windows/) en el método Dispose cuando el parámetro booleano sea **FALSE**, porque es posible que esos objetos ya se hayan finalizado. Para obtener más información sobre cómo liberar recursos, [vea Finalizar métodos y destructores.](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconfinalizemethodscdestructors.asp)

## <a name="forms-and-the-recognizercontext"></a>Forms y RecognizerContext

[Los eventos recognizerContext](/previous-versions/ms552546(v=vs.100)) se ejecutan en un subproceso diferente al subproceso en el que se encuentra el formulario. Los controles de Windows forms están enlazados a un subproceso específico y no son seguros para subprocesos. Por lo tanto, debe usar uno de los métodos de invocación del control para serializar la llamada al subproceso adecuado. Cuatro métodos de un control son seguros para subprocesos: [los](/dotnet/api/system.windows.forms.control.invoke?view=netcore-3.1)métodos Invoke , [BeginInvoke](/dotnet/api/system.windows.forms.control.begininvoke?view=netcore-3.1), [EndInvoke](/dotnet/api/system.windows.forms.control.endinvoke?view=netcore-3.1)y [CreateGraphics.](/dotnet/api/system.windows.forms.control.creategraphics?view=netcore-3.1) Para todas las demás llamadas a métodos, use uno de estos métodos de invocación al llamar desde un subproceso diferente. Para obtener más información sobre el uso de estos métodos, vea [Manipular controles de subprocesos.](/previous-versions/757y83z4(v=vs.140))

## <a name="waiting-for-events"></a>Esperando eventos

El entorno de Tablet PC es multiproceso. Use la función [**CoWaitForMultipleHandles**](/windows/win32/api/combaseapi/nf-combaseapi-cowaitformultiplehandles) en lugar de otros métodos de espera para permitir que las llamadas del Modelo de objetos componentes (COM) vuelvan a entrar en el apartamento multiproceso (MTA) mientras la aplicación espera un evento.

## <a name="using-ink-strokes-collections"></a>Uso de colecciones de trazos de lápiz

Las instancias de [colecciones de trazos](/previous-versions/ms552701(v=vs.100)) que se obtienen de un objeto [Ink](/previous-versions/aa515768(v=msdn.10)) no se recopilan como elementos no utilizados. Para evitar una pérdida de memoria, siempre que trabaje con una de estas colecciones, use la instrucción "using", como se muestra a continuación.


```C++
using (Strokes strokes = myInk.Strokes)
{
    int i = strokes.Count;
}
```



## <a name="disposing-managed-objects-and-controls"></a>Eliminación de objetos y controles administrados

Para evitar una pérdida de memoria, debe llamar explícitamente al método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) en cualquier objeto o control de Tablet PC al que se haya asociado un controlador de eventos antes de que el objeto o control salga del ámbito.

Para mejorar el rendimiento de la aplicación, elimine manualmente los siguientes objetos, controles y recopilación cuando ya no sean necesarios.

-   [Divisor](/previous-versions/ms583616(v=vs.100))
-   [Entrada de lápiz](/previous-versions/aa515768(v=msdn.10))
-   [InkCollector](/previous-versions/ms583683(v=vs.100))
-   [InkEdit](/previous-versions/ms552265(v=vs.100))
-   [InkOverlay](/previous-versions/ms552322(v=vs.100))
-   [InkPicture](/previous-versions/aa514604(v=msdn.10))
-   [PenInputPanel](/previous-versions/aa514041(v=msdn.10))
-   [RecognizerContext](/previous-versions/ms552546(v=vs.100))
-   [Trazos](/previous-versions/ms552701(v=vs.100))

En el siguiente ejemplo de C \# se muestran algunos escenarios en los que se usa el método [Dispose.](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1)


```C++
// A field for a Divider object
private Microsoft.Ink.Divider theDivider;

// A method that creates a Divider object
public void CreateDivider()
{
    // Make sure any previous Divider object was disposed of.
    if (null != theDivider)
    {
        theDivider.Dispose();
        theDivider = null;
    }
    // Create the Divider object.
    theDivider = new Microsoft.Ink.Divider();

    // The remainder of the method
}

// A method that disposes of the Divider object
public void DisposeDivider()
{
    // The remainder of the method

    // Dispose of the Divider object.
    if (null != theDivider)
    {
        theDivider.Dispose();
        theDivider = null;
    }
}

// A method that uses a local PenInputPanel object.
public void UsePenInputPanel()
{
    // Create the PenInputPanel object.
    Microsoft.Ink.PenInputPanel thePenInputPanel =
        new Microsoft.Ink.PenInputPanel();

    // The remainder of the method

    // Dispose of the PenInputPanel object before exiting.
    thePenInputPanel.Dispose();
    thePenInputPanel = null;
}
```



 

 