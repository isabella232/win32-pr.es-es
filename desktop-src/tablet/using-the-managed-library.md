---
description: Información general de la biblioteca administrada y notas sobre el uso de la biblioteca administrada de la plataforma de Tablet PC.
ms.assetid: d283ea1c-faf3-4222-a9a7-c67087636b86
title: Uso de la biblioteca administrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b1a1050705a6d74e6b183d04ec1c8f82d3954f0
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105707507"
---
# <a name="using-the-managed-library"></a>Uso de la biblioteca administrada

La Common Language Runtime es la base de Microsoft .NET Framework. Puede pensar en el Common Language Runtime como un agente que administra el código en tiempo de ejecución, proporcionando servicios principales como la administración de memoria, la administración de subprocesos y la comunicación remota, al tiempo que aplica una seguridad estricta del código. De hecho, el concepto de administración de código es un principio fundamental del Common Language Runtime. El código que tiene como destino el Common Language Runtime se conoce como código administrado. El código que no tiene como destino el Common Language Runtime se denomina código nativo.

La biblioteca de clases de Framework es una completa colección orientada a objetos de clases reutilizables que puede usar para desarrollar aplicaciones que abarcan desde aplicaciones tradicionales de línea de comandos o de interfaz gráfica de usuario (GUI) hasta aplicaciones basadas en las innovaciones más recientes proporcionadas por ASP.NET y servicios Web.

La biblioteca administrada de Tablet PC contiene un conjunto de objetos administrados que extiende el marco de trabajo para proporcionar compatibilidad con la entrada y la salida de escritura a mano en Tablet PC, así como el intercambio de datos con otros equipos.

## <a name="exceptions"></a>Excepciones

Los objetos de biblioteca administrada de la API de Tablet PC encapsulan las implementaciones de la biblioteca COM. Cuando el objeto o el control de la biblioteca COM subyacente devuelve un error, la API administrada generará una excepción Marshal. ThrowExceptionForHR que proporciona los detalles sobre la excepción COM interna. Puede hacer referencia a los valores HRESULT en la referencia de la biblioteca COM para obtener más información sobre los posibles errores que se pueden devolver.

## <a name="object-comparison"></a>Comparación de objetos

En el caso de todos los objetos de la biblioteca administrada de la plataforma de Tablet PC, [**Equals**](/previous-versions/windows/) no se invalida para comparar correctamente dos objetos que son iguales. La interfaz de programación de aplicaciones (API) administrada no admite la comparación de igualdad de objetos, ya sea a través de la función **Equals** o a través del operador Equals (= =).

## <a name="binding-to-the-latest-microsoftinkdll"></a>Enlazar a la Microsoft.Ink.dll más reciente

El ensamblado de Microsoft.Ink.dll más reciente es un reemplazo compatible de Microsoft.Ink.dll versión 1,0 y Microsoft.Ink.15.dll. En la mayoría de los casos, no es necesario realizar ningún cambio en las aplicaciones que se distribuyen con los ensamblados anteriores. Sin embargo, en algunos casos debe indicar al cargador de Common Language Runtime que utilice la biblioteca de vínculos dinámicos (DLL) más reciente donde se hace referencia a los archivos dll más antiguos.

La única vez que necesita enlazar explícitamente al nuevo ensamblado mediante el uso de la técnica siguiente es si la aplicación usa un componente que hace referencia al ensamblado de la versión 1,0 o 1,5 en combinación con un componente que hace referencia a un ensamblado de versión más reciente, como 1,7, y si esos componentes pueden intercambiar datos.

La mejor manera de indicar al cargador de Common Language Runtime que use el archivo DLL más reciente es redirigir las versiones de ensamblado en el nivel de aplicación. Puede especificar que la aplicación use la versión más reciente del ensamblado colocando la información de enlace del ensamblado en el archivo de configuración de la aplicación. Para obtener más información acerca de la redirección de versiones de ensamblado en el nivel de aplicación, consulte [redirección de versiones de ensamblado](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconassemblyversionredirection.asp%3fframe%3dtrue), concretamente la sección "especificar el enlace de ensamblados en archivos de configuración".

Tendrá que crear un archivo de configuración en el mismo directorio que el archivo ejecutable. El archivo de configuración debe tener el mismo nombre que el ejecutable, seguido de la extensión del archivo. config. Por ejemplo, para una aplicación, MyApp.exe, el archivo de configuración debe ser el archivo de MyApp.exe.config. El archivo de configuración usa un elemento [bindingRedirect](/previous-versions/dotnet/netframework-1.1/eftw1fys(v=vs.71)) para forzar que todas las versiones anteriores se asignen a la versión más reciente, como se muestra en el ejemplo siguiente:

`<bindingRedirect oldVersion="0.0.0.0-1.7.2600.xxxx" newVersion="1.7.2600.xxxx" />`

Para obtener más información sobre los archivos de configuración, incluidos ejemplos de cómo construir el lenguaje de marcado extensible (XML) para el archivo de configuración, vea [bindingRedirect](/previous-versions/dotnet/netframework-1.1/eftw1fys(v=vs.71)) y [redirección de versiones de ensamblado](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconassemblyversionredirection.asp%3fframe%3dtrue).

Las aplicaciones creadas con el kit de desarrollo de Microsoft Windows XP Tablet PC Edition 1,7 y versiones posteriores se enlazan automáticamente a la nueva versión del ensamblado Microsoft. Ink. Para obtener más información sobre el enlace de ensamblados, vea [cómo el motor en tiempo de ejecución ubica ensamblados](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconHowRuntimeLocatesAssemblies.asp).

> [!Note]  
> El uso de la Directiva de aplicación para enlazar con el ensamblado actualizado no funciona para las aplicaciones que usan la clase [divisor](/previous-versions/ms583616(v=vs.100)) o la clase [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) . Las aplicaciones que usan cualquiera de esas clases deben seguir usando Microsoft.Ink.15.dll o volver a compilarse después de hacer referencia al ensamblado actualizado.

 

## <a name="working-with-events"></a>Trabajar con eventos

Si el código de un controlador de eventos para cualquiera de los objetos administrados produce una excepción, la excepción no se entrega al usuario. Para asegurarse de que se entreguen las excepciones, use bloques try-catch en los controladores de eventos para los eventos administrados.

## <a name="managing-forms"></a>Administrar formularios

La clase de [formulario](/dotnet/api/system.windows.forms.form?view=netcore-3.1) y sus clases base no definen un finalizador. Para limpiar los recursos en un formulario, escriba una subclase que proporcione un finalizador (por ejemplo, el destructor de C \# mediante el ~) que llama a [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1). Para realizar la limpieza, el finalizador invalida Dispose y llama a la clase base Dispose. No haga referencia a otros objetos que requieran el método [Finalize](/previous-versions/windows/) en el método Dispose cuando el parámetro booleano sea **false**, ya que es posible que esos objetos ya se hayan finalizado. Para obtener más información sobre la liberación de recursos [, vea métodos de finalización y destructores](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconfinalizemethodscdestructors.asp).

## <a name="forms-and-the-recognizercontext"></a>Formularios y RecognizerContext

Los eventos [RecognizerContext](/previous-versions/ms552546(v=vs.100)) se ejecutan en un subproceso diferente del subproceso en el que se encuentra el formulario. Los controles de Windows Forms se enlazan a un subproceso concreto y no son seguros para subprocesos. Por lo tanto, debe usar uno de los métodos de invocación del control para calcular las referencias de la llamada al subproceso adecuado. Cuatro métodos en un control son seguros para subprocesos: los métodos [Invoke](/dotnet/api/system.windows.forms.control.invoke?view=netcore-3.1), [BeginInvoke](/dotnet/api/system.windows.forms.control.begininvoke?view=netcore-3.1), [EndInvoke](/dotnet/api/system.windows.forms.control.endinvoke?view=netcore-3.1)y [CreateGraphics](/dotnet/api/system.windows.forms.control.creategraphics?view=netcore-3.1) . Para todas las demás llamadas a métodos, use uno de estos métodos de invocación cuando llame a desde un subproceso diferente. Para obtener más información sobre el uso de estos métodos, vea [manipular controles desde subprocesos](/previous-versions/757y83z4(v=vs.140)).

## <a name="waiting-for-events"></a>Esperando eventos

El entorno de Tablet PC es multiproceso. Utilice la función [**CoWaitForMultipleHandles**](/windows/win32/api/combaseapi/nf-combaseapi-cowaitformultiplehandles) en lugar de otros métodos wait para permitir que las llamadas del modelo de objetos componentes (com) reentrantes escriban el apartamento multiproceso (MTA) mientras la aplicación está esperando en un evento.

## <a name="using-ink-strokes-collections"></a>Usar colecciones de trazos de lápiz

Las instancias de las colecciones de [trazos](/previous-versions/ms552701(v=vs.100)) que se obtienen a partir de un objeto de [entrada manuscrita](/previous-versions/aa515768(v=msdn.10)) no se recolectan como elementos no utilizados. Para evitar una pérdida de memoria, siempre que trabaje con una de estas colecciones, use la instrucción "Using" tal y como se muestra a continuación.


```C++
using (Strokes strokes = myInk.Strokes)
{
    int i = strokes.Count;
}
```



## <a name="disposing-managed-objects-and-controls"></a>Desechar controles y objetos administrados

Para evitar una pérdida de memoria, debe llamar explícitamente al método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) en cualquier objeto o control de Tablet PC al que se haya adjuntado un controlador de eventos antes de que el objeto o el control salga del ámbito.

Para mejorar el rendimiento de la aplicación, elimine manualmente los siguientes objetos, controles y colecciones cuando ya no se necesiten.

-   [Divisor](/previous-versions/ms583616(v=vs.100))
-   [Entrada de lápiz](/previous-versions/aa515768(v=msdn.10))
-   [InkCollector](/previous-versions/ms583683(v=vs.100))
-   [InkEdit](/previous-versions/ms552265(v=vs.100))
-   [InkOverlay](/previous-versions/ms552322(v=vs.100))
-   [InkPicture](/previous-versions/aa514604(v=msdn.10))
-   [PenInputPanel](/previous-versions/aa514041(v=msdn.10))
-   [Estableció](/previous-versions/ms552546(v=vs.100))
-   [Trazos](/previous-versions/ms552701(v=vs.100))

En el siguiente \# ejemplo de C se muestran algunos escenarios en los que se usa el método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) .


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



 

 