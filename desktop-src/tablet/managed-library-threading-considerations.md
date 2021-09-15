---
description: Las siguientes consideraciones de subprocesamiento de Tablet PC son específicas de la biblioteca administrada.
ms.assetid: bcc398d3-22ea-466c-9206-92b0ac208def
title: Consideraciones sobre subprocesos de biblioteca administrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b8677375b8bbdb5f171329927d01e6178b5cb83
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360250"
---
# <a name="managed-library-threading-considerations"></a>Consideraciones sobre subprocesos de biblioteca administrada

Las siguientes consideraciones de subprocesamiento de Tablet PC son específicas de la biblioteca administrada.

-   [Seguridad para subprocesos](#thread-safety)
-   [Aplicaciones STA y MTA](#sta-and-mta-applications)
-   [Windows Consideraciones sobre subprocesamiento de formularios](#windows-forms-threading-considerations)
-   [Consideraciones sobre el Portapapeles](#clipboard-considerations)
-   [Excepciones dentro de controladores de eventos](#exceptions-within-event-handlers)
-   [Eliminación de objetos y controles](#disposing-objects-and-controls)
-   [API stylusInput](#stylusinput-apis)

## <a name="thread-safety"></a>Thread-Safety

Las clases de biblioteca administrada de la plataforma de Tablet PC no suelen ser seguras para subprocesos. Las siguientes colecciones son seguras para subprocesos en el nivel de miembro; Sin embargo, estas colecciones no garantizan que un enumerador esté protegido si otro subproceso funciona en la colección simultáneamente:

-   [CursorButtons](/previous-versions/ms839506(v=msdn.10))
-   [Cursores](/previous-versions/ms839493(v=msdn.10))
-   [DivisionUnits](/previous-versions/ms837954(v=msdn.10))
-   [RecognitionAlternates](/previous-versions/ms830115(v=msdn.10))
-   [Reconocedores](/previous-versions/ms828520(v=msdn.10))
-   [Tabletas](/previous-versions/ms827599(v=msdn.10))

## <a name="sta-and-mta-applications"></a>Aplicaciones STA y MTA

Las aplicaciones administradas creadas mediante los asistentes incluidos en Microsoft Visual Studio .NET son de un solo subproceso (STA) de forma predeterminada. Puede cambiar el apartamento de la aplicación estableciendo el subproceso STA o el atributo de subproceso multiproceso (MTA) en el punto de entrada de la aplicación.

Si la aplicación se ejecuta en un MTA, debe escribir código seguro para subprocesos; sin embargo, al hacerlo, puede mejorar ciertos problemas de rendimiento de control de eventos.

Para obtener más información sobre los atributos de subproceso STA y de subproceso MTA, vea [STAThreadAttribute](/dotnet/api/system.stathreadattribute?view=netcore-3.1) (clase) y [MTAThreadAttribute (clase).](/dotnet/api/system.mtathreadattribute?view=netcore-3.1)

## <a name="windows-forms-threading-considerations"></a>Windows Consideraciones sobre subprocesamiento de formularios

Los [controles InkPicture](/previous-versions/aa514604(v=msdn.10)) y [InkEdit](/previous-versions/ms552265(v=vs.100)) amplían Windows Forms. Windows Los controles forms usan el modelo de apartamento de un solo subproceso (STA) porque los formularios Windows Forms se basan en ventanas nativas de Win32 que son inherentemente de un solo subproceso. En el código administrado, los controles de entrada de lápiz deben crearse en el mismo subproceso que el subproceso principal del formulario.

En una aplicación STA, ciertos eventos se suceden en un subproceso distinto del subproceso de interfaz de usuario (UI) de la aplicación. Al llamar a cualquier objeto o control de Windows Forms, incluidos los controles [InkPicture](/previous-versions/aa514604(v=msdn.10)) y [InkEdit,](/previous-versions/ms552265(v=vs.100)) desde un controlador de eventos de Tablet PC, use el método [Control.Invoke](/dotnet/api/system.windows.forms.control.invoke?view=netcore-3.1) heredado del objeto o control. La [propiedad InvokeRequired,](/dotnet/api/system.windows.forms.control.invokerequired?view=netcore-3.1) heredada de la clase Control, se puede usar para determinar si es necesario.

Por ejemplo, en el siguiente controlador de eventos para el evento [Recognition,](/previous-versions/ms829424(v=msdn.10)) se prueba la propiedad [InvokeRequired](/dotnet/api/system.windows.forms.control.invokerequired?view=netcore-3.1) y, si es **TRUE,** el controlador de eventos se vuelve a invocar desde el subproceso de la interfaz de usuario.


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



Si coloca un [control UserControl](/dotnet/api/system.web.ui.usercontrol?view=netframework-4.8) en una página web en un explorador (vea [Controles web](web-controls.md)), se ejecuta como una aplicación STA. Para las aplicaciones cliente inteligentes [(consulte No Touch Deployment),](no-touch-deployment.md)el desarrollador tiene control total sobre [ApartmentState.](/dotnet/api/system.threading.apartmentstate?view=netcore-3.1) (El valor predeterminado suele ser STA, pero puede ser MTA, dependiendo de la versión de CLR). Para problemas de subprocesos relacionados con [**RealTimeStylus,**](realtimestylus-class.md)vea Consideraciones de [subprocesos para las API StylusInput](threading-considerations-for-the-stylusinput-apis.md).

Para obtener más información sobre cómo llamar a Windows Forms desde una aplicación MTA, vea [Multithreaded Windows Forms Control Sample](/previous-versions/dotnet/netframework-1.1/3s8xdz5c(v=vs.71)).

## <a name="clipboard-considerations"></a>Consideraciones sobre el Portapapeles

El [objeto Clipboard](../dataxchg/clipboard.md) solo funciona desde un subproceso STA. Al intentar copiar o pegar desde el Portapapeles desde un subproceso que no es STA, obtiene una [excepción ThreadStateException](/previous-versions/windows/). Si la aplicación es MTA, cree un subproceso STA para controlar las llamadas al método del Portapapeles y algunos de los otros aspectos de la interfaz de usuario de la aplicación.

## <a name="exceptions-within-event-handlers"></a>Excepciones dentro de controladores de eventos

No se pueden realizar excepciones desde los controladores de eventos de Tablet PC. Por ejemplo, si un delegado de controlador de eventos para un objeto o colección de Tablet PC tiene tres controladores registrados y el primero produce una excepción, se produce la siguiente secuencia:

1.  Se cierra el primer controlador.
2.  Se pierde la excepción.
3.  No se invocan los controladores restantes.

## <a name="disposing-objects-and-controls"></a>Eliminación de objetos y controles

Para evitar una pérdida de memoria, debe llamar explícitamente al método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) en cualquier objeto o control de Tablet PC al que se haya asociado un controlador de eventos antes de que el objeto o control salga del ámbito.

Para mejorar el rendimiento de la aplicación, deseche manualmente cualquier objeto o control de Tablet PC que implemente el método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) cuando el objeto o control ya no sea necesario.

## <a name="stylusinput-apis"></a>API stylusInput

Para obtener información sobre las consideraciones de subprocesos para el objeto [**RealTimeStylus**](realtimestylus-class.md) y las interfaces de programación de aplicaciones (API) StylusInput, vea Consideraciones de subprocesamiento para las [API StylusInput](threading-considerations-for-the-stylusinput-apis.md).

 

 
