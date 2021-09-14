---
title: Información general de StoServe
description: En el ejemplo de código de StoServe se muestra cómo usar servicios Storage estructurados tal como se proporciona en la implementación de archivos compuestos. Se describe el uso de las interfaces IStorage e IStream estándar.
ms.assetid: 41ccd333-15c8-46b2-91c6-3e1929f7198c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c0c8325fbc20d4917785d0b83ca70bffa996824
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160691"
---
# <a name="stoserve-overview"></a>Información general de StoServe

## <a name="purpose"></a>Propósito

El enfoque principal de este ejemplo de código es el uso de servicios Storage estructurados tal como se proporciona en la implementación de archivos compuestos. Se describe el uso de [**las interfaces IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) e [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) estándar. **StoServe funciona** con el ejemplo [de código de StoClien](structured-storage-client-sample--stoclien-.md) para ilustrar el uso conjunto de almacenamiento de archivos compuestos por cliente y servidor.

## <a name="functionality"></a>Funcionalidad

El **ejemplo StoServe** presenta el objeto COM COPaper, que representa virtualmente una hoja en blanco de papel de dibujo.

Los objetos COPaper exponen un conjunto de características para dibujar de forma libre en la superficie de papel mediante "ink" del color y ancho especificados. La funcionalidad es externamente similar a los ejemplos de tutoriales de "scribble" en muchas versiones de Microsoft Visual C++. La diferencia en los **ejemplos de StoServe** / **StoClien** es una arquitectura basada principalmente en la tecnología COM. Las características de papel de dibujo electrónico de objetos COPaper están disponibles para los clientes a través de una interfaz [**IPaper**](ipaper-methods.md) personalizada. COPaper implementa la **interfaz IPaper.** Se mantiene una distinción de arquitectura clara entre el cliente y el servidor. COPaper no proporciona ninguna interfaz gráfica de usuario (GUI). El diseño del objeto COPaper se basa en el cliente para todo el comportamiento de la GUI. COPaper encapsula solo la captura basada en servidor y el almacenamiento de los datos de entrada de lápiz dibujados.

Los datos de entrada de lápiz que se dibujan en la superficie copaper se pueden almacenar y cargar desde archivos compuestos. Los [**métodos IPaper**](ipaper-methods.md), [**Save**](ipaper--save.md) [**y Load**](ipaper--load.md) aceptan un puntero de interfaz [**IStorage.**](/windows/desktop/api/Objidl/nn-objidl-istorage) COPaper usa esta interfaz **IStorage** proporcionada por el cliente para almacenar los datos de dibujo.

COPaper se encuentra en un servidor en proceso y está disponible públicamente como un componente COM personalizado. Al igual que otros servidores de esta serie de tutoriales, StoServe es un servidor COM de registro propio. Hace que el tipo de objeto COPaper esté disponible para los clientes como el componente DllPaper mediante un registro DLLPaper de CLSID \_ en el Registro.

Al igual que en el servidor CONSERVE anterior, las características de objetos conectables se admiten en COPaper. Se expone la interfaz [**IConnectionPointContainer**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) y se implementa un punto de conexión adecuado. En este contexto, se declara una interfaz IPaperSink personalizada saliente para su uso en el envío de notificaciones al cliente.

Las dos [**interfaces personalizadas IPaper**](ipaper-methods.md) [**e IPaperSink**](ipapersink-methods.md) se declaran en IPAPER. H ubicado en el directorio común de \\ INC relacionado. Los GUID de las interfaces y objetos se definen en PAPGUIDS. H ubicado en ese mismo directorio de include común.

La instalación CThreaded de APPUTIL la usa **StoServe** para lograr la seguridad de subprocesos, como se encontraba en el ejemplo FRESERVE. Los objetos COPaper se derivan de la clase CThreaded y heredan sus métodos OwnThis y UnOwnThis. Estos métodos permiten que solo un subproceso a la vez tenga acceso al servidor **de StoServe** y a los objetos COPaper administrados por el servidor.

## <a name="copaper-com-object"></a>CoPaper (objeto COM)

El objeto COM COPaper es el tipo de objeto único administrado por este servidor en proceso **de StoServe.** COPaper se construye como un objeto COM conectable con una implementación de la interfaz [**IConnectionPointContainer**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) estándar y una implementación de la interfaz [**IPaper**](ipaper-methods.md) personalizada. COPaper expone la interfaz **IPaper** para que los clientes puedan realizar un pequeño conjunto de operaciones de papel electrónico en una instancia de COPaper. Las operaciones esenciales son iniciar una secuencia de dibujo de lápiz, dibujar los datos de entrada de lápiz en la superficie de papel virtual de COPaper y finalizar la secuencia de dibujo de lápiz. En este esquema, se supone que el cliente es una aplicación de guión gráfica de usuario controlada por un dispositivo de mouse o tableta. El cliente es responsable de traducir los movimientos del mouse en solicitudes a COPaper, que guarda estas solicitudes como datos de entrada manuscrita.

Hay dos niveles de almacenamiento de datos de entrada manuscrita en COPaper. COPaper guarda los datos de entrada de lápiz en una matriz basada en RAM que representa el dibujo actual y COPaper guarda de forma persistente un dibujo completo en un archivo compuesto. Los métodos de [**la interfaz IPaper**](ipaper-methods.md) realizan ambos.

Dado que el cliente no administra los datos de papel dibujado, pero es responsable de representarlos como una imagen en la pantalla, la implementación de [**IPaper**](ipaper-methods.md) en COPaper debe exponer un método que permita al cliente obtener los datos de dibujo. La tecnología de objetos conectables de COPaper se usa para este propósito. COPaper implementa un punto de conexión CONNPOINT PAPERSINK para que un cliente pueda conectarse a COPaper para recibir los datos de entrada de lápiz \_ para dibujar. El cliente llama primero [al método IPaper::Redraw](ipaper--redraw.md) en el objeto COPaper para solicitar todos los datos de entrada de lápiz del dibujo actual. A continuación, la implementación de COPaper de Redraw usa la implementación de cliente de [**IPaperSink**](ipapersink-methods.md) para pasar los datos al cliente.

A medida que el usuario dibuja interactivamente en el cliente, pinta los datos inmediatamente en la pantalla y los envía también a COPaper para guardarlos. Cuando el cliente requiere que se vuelva a dibujar la pantalla, llama al método COPaper [Redraw.](ipaper--redraw.md) Este tipo de repintado es común en las aplicaciones. Por ejemplo, el repintado se produce cuando otra ventana de aplicación sobrelada la ventana de cliente. El cliente tiene una representación de mapa de bits de la imagen dibujada, pero el mapa de bits se pierde fácilmente y a menudo se debe volver a dibujar. El cliente se basa en COPaper en el servidor para los datos de entrada de lápiz necesarios para volver a dibujar.

Se trata de una división común de cliente/servidor de mano de obra. Es especialmente adecuado cuando hay un requisito para que varios clientes compartan los datos. COPaper está codificado para habilitarlo. Usa la instalación APPUTIL CThreaded para lograr la seguridad de subprocesos. Una aplicación que podría aprovechar este diseño es una aplicación de pizarra compartida, donde varios clientes pueden contribuir a un dibujo que se ve normalmente. La compatibilidad con COM para COM distribuido (DCOM) admite este tipo de uso de aplicaciones de grupo de trabajo a través de la red. Para obtener más información, vea el ejemplo remclien anterior.

Un uso más moderado del esquema de cliente/servidor de COPaper es integrar el comportamiento de los objetos implementados en distintas aplicaciones en el mismo equipo. En este caso, los clientes pueden ser un contenedor ActiveX en aplicaciones independientes que comparten datos administrados por el mismo objeto. Es posible que estos datos no sean los datos de dibujo de lápiz que admite el componente DllPaper. **StoServe se** puede usar como marco de inicio para programar componentes que administran otros tipos de datos compartidos.

## <a name="support-information"></a>Información complementaria

El **archivo make de StoServe** registra el componente COM **StoServe** DllPaper en el registro. Este componente debe registrarse antes de **que StoServe** esté disponible para clientes COM externos como servidor para ese componente. Este registro se realiza mediante la utilidad Register.exe integrada en el ejemplo REGISTER. Para compilar o ejecutar **StoServe,** primero compile el ejemplo de código REGISTER.

Para obtener más información sobre cómo configurar el sistema para compilar y probar los ejemplos de código de esta serie de tutoriales COM, vea [How to Build Samples](how-to-build-samples.md). El archivo make proporcionado (MAKEFILE) es compatible con Microsoft NMAKE. Para crear una compilación de depuración, emita el comando NMAKE en la ventana del símbolo del sistema.

Para un uso cómodo en Microsoft Visual Studio, se proporciona un archivo de proyecto para cada ejemplo. Para cargar el proyecto para el **ejemplo de StoServe,** puede ejecutar Visual Studio en el símbolo del sistema en el directorio samples como se indica a continuación:

MSDEV STOSERVE. DSP

También puede hacer doble clic en el archivo Stoserve.dsp en Windows Explorer para cargar un proyecto de ejemplo en Visual Studio. En Visual Studio puede examinar las clases de C++ del origen de ejemplo y, por lo general, realizar las demás operaciones de edición,compilación y depuración.

> [!Note]  
> Como parte del Kit de desarrollo de software de plataforma (SDK), la compilación de estos ejemplos desde dentro de Visual Studio requiere la configuración adecuada de las rutas de acceso de directorio en Visual Studio. Para obtener más información, [vea How to Build Samples](how-to-build-samples.md).

 

 

 