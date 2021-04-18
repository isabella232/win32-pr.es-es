---
description: Las siguientes consideraciones sobre el subproceso de Tablet PC son específicas de la biblioteca administrada.
ms.assetid: bcc398d3-22ea-466c-9206-92b0ac208def
title: Consideraciones sobre los subprocesos de biblioteca administrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b8677375b8bbdb5f171329927d01e6178b5cb83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706687"
---
# <a name="managed-library-threading-considerations"></a>Consideraciones sobre los subprocesos de biblioteca administrada

Las siguientes consideraciones sobre el subproceso de Tablet PC son específicas de la biblioteca administrada.

-   [Seguridad para subprocesos](#thread-safety)
-   [Aplicaciones STA y MTA](#sta-and-mta-applications)
-   [Consideraciones sobre el subprocesamiento de Windows Forms](#windows-forms-threading-considerations)
-   [Consideraciones sobre el portapapeles](#clipboard-considerations)
-   [Excepciones dentro de los controladores de eventos](#exceptions-within-event-handlers)
-   [Desechar objetos y controles](#disposing-objects-and-controls)
-   [API de StylusInput](#stylusinput-apis)

## <a name="thread-safety"></a>Thread-Safety

Las clases de biblioteca administrada de la plataforma de Tablet PC no suelen ser seguras para subprocesos. Las colecciones siguientes son seguras para subprocesos en el nivel de miembro; sin embargo, estas colecciones no garantizan que un enumerador esté protegido si otro subproceso funciona en la colección simultáneamente:

-   [CursorButtons](/previous-versions/ms839506(v=msdn.10))
-   [Cursores](/previous-versions/ms839493(v=msdn.10))
-   [DivisionUnits](/previous-versions/ms837954(v=msdn.10))
-   [RecognitionAlternates](/previous-versions/ms830115(v=msdn.10))
-   [Reconocedores](/previous-versions/ms828520(v=msdn.10))
-   [Digitaliza](/previous-versions/ms827599(v=msdn.10))

## <a name="sta-and-mta-applications"></a>Aplicaciones STA y MTA

De forma predeterminada, las aplicaciones administradas creadas con los asistentes contenidos en Microsoft Visual Studio .NET son un contenedor uniproceso (STA). Puede cambiar el apartamento de la aplicación estableciendo el subproceso STA o el atributo de subproceso de Apartamento multiproceso (MTA) en el punto de entrada de la aplicación.

Si la aplicación se ejecuta en un MTA, debe escribir código seguro para subprocesos; sin embargo, si lo hace, puede mejorar determinados problemas de rendimiento de control de eventos.

Para obtener más información sobre los atributos de subprocesos y subprocesos de MTA, consulte clase [STAThreadAttribute](/dotnet/api/system.stathreadattribute?view=netcore-3.1) y clase [MTAThreadAttribute](/dotnet/api/system.mtathreadattribute?view=netcore-3.1) .

## <a name="windows-forms-threading-considerations"></a>Consideraciones sobre el subprocesamiento de Windows Forms

Los controles [InkPicture](/previous-versions/aa514604(v=msdn.10)) y [InkEdit](/previous-versions/ms552265(v=vs.100)) extienden Windows Forms controles. Los controles de Windows Forms utilizan el modelo de contenedor uniproceso (STA) porque Windows Forms se basan en ventanas nativas de Win32 que son de un solo subproceso. En código administrado, los controles de entrada de lápiz deben crearse en el mismo subproceso que el subproceso principal del formulario.

En una aplicación STA, ciertos eventos se producen en un subproceso distinto del subproceso de la interfaz de usuario (IU) de la aplicación. Al llamar a cualquier Windows Forms objeto o control, incluidos los controles [InkPicture](/previous-versions/aa514604(v=msdn.10)) y [InkEdit](/previous-versions/ms552265(v=vs.100)) , desde dentro de un controlador de eventos de Tablet PC, use el método heredado [control. Invoke](/dotnet/api/system.windows.forms.control.invoke?view=netcore-3.1) del objeto o el control. La propiedad [InvokeRequired](/dotnet/api/system.windows.forms.control.invokerequired?view=netcore-3.1) , heredada de la clase control, se puede utilizar para determinar si es necesario.

Por ejemplo, en el siguiente controlador de eventos para el evento de [reconocimiento](/previous-versions/ms829424(v=msdn.10)) , se prueba la propiedad [InvokeRequired](/dotnet/api/system.windows.forms.control.invokerequired?view=netcore-3.1) y, si es **true**, el controlador de eventos se vuelve a invocar desde el subproceso de la interfaz de usuario.


```C++
void recoContext_Recognition(object sender, 
        RecognizerContextRecognitionEventArgs e)
{
    if (InvokeRequired)
    {
        Invoke( new RecognizerContextRecognitionEventHandler(  
                     recoContext_Recognition ),
                    new object[] { sender, e } );
        return;
    }
     // Use the recognition result here.
}
```



Si coloca [UserControl](/dotnet/api/system.web.ui.usercontrol?view=netframework-4.8) en awebpagein en un explorador (consulte [controles Web](web-controls.md)), se ejecuta como una aplicación Sta. En el caso de las aplicaciones Smart Client (no se ve [ninguna implementación táctil](no-touch-deployment.md)), el desarrollador tiene control total sobre el [ApartmentState](/dotnet/api/system.threading.apartmentstate?view=netcore-3.1). (El valor predeterminado es generalmente STA, pero puede ser MTA, dependiendo de la versión de CLR). En el caso de problemas de subprocesamiento que impliquen a [**RealTimeStylus**](realtimestylus-class.md), consulte [consideraciones sobre subprocesos para las API de StylusInput](threading-considerations-for-the-stylusinput-apis.md).

Para obtener más información sobre cómo llamar a Windows Forms desde una aplicación MTA, vea [ejemplo de control multiproceso Windows Forms](/previous-versions/dotnet/netframework-1.1/3s8xdz5c(v=vs.71)).

## <a name="clipboard-considerations"></a>Consideraciones sobre el portapapeles

El objeto [Clipboard](../dataxchg/clipboard.md) solo funciona desde un subproceso STA. Al intentar copiar o pegar desde el Portapapeles desde un subproceso que no es STA, obtiene un [ThreadStateException](/previous-versions/windows/). Si la aplicación es MTA, cree un subproceso STA para controlar las llamadas al método del portapapeles y algunos de los demás aspectos de la interfaz de usuario de la aplicación.

## <a name="exceptions-within-event-handlers"></a>Excepciones dentro de los controladores de eventos

No se pueden iniciar excepciones desde los controladores de eventos de Tablet PC. Por ejemplo, si un delegado de controlador de eventos para un objeto o colección de Tablet PC tiene tres controladores registrados y el primero de ellos inicia una excepción, se produce la siguiente secuencia:

1.  El primer controlador se cierra.
2.  La excepción se pierde.
3.  No se invocan los controladores restantes.

## <a name="disposing-objects-and-controls"></a>Desechar objetos y controles

Para evitar una pérdida de memoria, debe llamar explícitamente al método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) en cualquier objeto o control de Tablet PC al que se haya adjuntado un controlador de eventos antes de que el objeto o el control salga del ámbito.

Para mejorar el rendimiento de la aplicación, elimine manualmente cualquier objeto o control de Tablet PC que implemente el método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) cuando el objeto o el control ya no se necesiten.

## <a name="stylusinput-apis"></a>API de StylusInput

Para obtener información sobre las consideraciones de subprocesos para el objeto [**RealTimeStylus**](realtimestylus-class.md) y las interfaces de programación de aplicaciones (API) StylusInput, consulte [consideraciones sobre los subprocesos para las API de StylusInput](threading-considerations-for-the-stylusinput-apis.md).

 

 
