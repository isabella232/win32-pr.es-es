---
title: Información general de StoServe
description: En el ejemplo de código StoServe se muestra cómo usar los servicios de almacenamiento estructurado tal y como se proporciona en la implementación de archivos compuestos. Se describe el uso de las interfaces estándar IStorage y IStream.
ms.assetid: 41ccd333-15c8-46b2-91c6-3e1929f7198c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c0c8325fbc20d4917785d0b83ca70bffa996824
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359239"
---
# <a name="stoserve-overview"></a>Información general de StoServe

## <a name="purpose"></a>Propósito

El objetivo principal de este ejemplo de código es el uso de los servicios de almacenamiento estructurado tal y como se proporciona en la implementación de archivos compuestos. Se describe el uso de las interfaces estándar [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) y [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) . **StoServe** funciona con el ejemplo de código [StoClien](structured-storage-client-sample--stoclien-.md) para ilustrar el uso conjunto de almacenamiento de archivos compuesto por cliente y servidor.

## <a name="functionality"></a>Funcionalidad

En el ejemplo **StoServe** se presenta el objeto com de copaper, que prácticamente representa una hoja en blanco de un papel de dibujo.

Los objetos de copapeles exponen un conjunto de características para el dibujo de forma libre en la superficie del papel usando "tinta" del color y el ancho especificados. La funcionalidad es similar a la de los ejemplos del tutorial "Scribble" en muchas versiones de Microsoft Visual C++. La diferencia en los ejemplos de **StoServe** / **StoClien** es una arquitectura basada principalmente en la tecnología com. Las características de papel de dibujo electrónico de los objetos de copapers están disponibles para los clientes a través de una interfaz [**IPaper**](ipaper-methods.md) personalizada. El copaper implementa la interfaz **IPaper** . Se mantiene una distinción de arquitectura clara entre el cliente y el servidor. No se proporciona ninguna interfaz gráfica de usuario (GUI). El diseño del objeto de copaper se basa en el cliente para todo el comportamiento de la interfaz gráfica de usuario. El copapel encapsula solo la captura basada en servidor y el almacenamiento de los datos de la tinta dibujada.

Los datos de tinta que se dibujan en la superficie de copapeles se pueden almacenar y cargar desde archivos compuestos. Los métodos [**IPaper**](ipaper-methods.md), [**Save**](ipaper--save.md) y [**Load**](ipaper--load.md) aceptan un puntero de interfaz [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) . El copaper usa esta interfaz **IStorage** proporcionada por el cliente para almacenar los datos del dibujo.

El copaper se aloja en un servidor en proceso y se pone a disposición pública como un componente COM personalizado. De forma similar a otros servidores de esta serie de tutoriales, StoServe es un servidor COM de registro automático. Hace que el tipo de objeto de copaper esté disponible para los clientes como el componente DllPaper mediante un \_ registro CLSID DllPaper en el registro.

Como en el servidor de conservación anterior, las características de los objetos conectables se admiten en el copaper. La interfaz [**IConnectionPointContainer**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) se expone y se implementa un punto de conexión adecuado. En este contexto, se declara una interfaz IPaperSink personalizada saliente para su uso en el envío de notificaciones al cliente.

Las dos interfaces personalizadas [**IPaper**](ipaper-methods.md) y [**IPaperSink**](ipapersink-methods.md) se declaran en IPaper. H ubicado en el directorio común del mismo nivel \\ . Los GUID para las interfaces y los objetos se definen en PAPGUIDS. H ubicado en el mismo directorio de inclusión común.

La instalación de CThreaded en APPUTIL la usa **StoServe** para lograr la seguridad para subprocesos, tal y como se encontraba en el ejemplo FRESERVE. Los objetos de copapers se derivan de la clase CThreaded y heredan sus métodos OwnThis y UnOwnThis. Estos métodos permiten que solo un subproceso cada vez tenga acceso al servidor **StoServe** y a los objetos de copapeles administrados por el servidor.

## <a name="copaper-com-object"></a>Objeto COM de copaper

El objeto COM de copapel es el tipo de objeto único administrado por este servidor en proceso de **StoServe** . El copaper se construye como un objeto COM conectable con una implementación de la interfaz [**IConnectionPointContainer**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) estándar y una implementación de la interfaz [**IPaper**](ipaper-methods.md) personalizada. El copaper expone la interfaz **IPaper** para que los clientes puedan realizar un pequeño conjunto de operaciones electrónicas de papel en una instancia de copaper. Las operaciones esenciales están iniciando una secuencia de dibujo de tinta, dibujando los datos de tinta en la superficie del papel virtual de copapeles y finalizando la secuencia de dibujo de la tinta. En este esquema, se supone que el cliente es una aplicación GUI controlada por un mouse o un dispositivo de tableta. El cliente es responsable de traducir los movimientos del mouse en solicitudes de copaper, lo que guarda estas solicitudes como datos de entrada de lápiz.

Hay dos niveles de datos de tinta que se guardan en el copaper. El copapel guarda los datos de tinta en una matriz basada en RAM que representa el dibujo actual y el copapel guarda de forma persistente un dibujo completo en un archivo compuesto. Los métodos de la interfaz [**IPaper**](ipaper-methods.md) realizan ambos.

Dado que el cliente no administra los datos de papel trazados, pero es responsable de presentarlos como una imagen en la pantalla, la implementación de [**IPaper**](ipaper-methods.md) en el copaper debe exponer un método que permita al cliente obtener los datos de dibujo. La tecnología de objetos conectables en copaper se usa para este fin. Un punto de conexión de CONNPOINT \_ PAPERSINK se implementa mediante el copaper, por lo que un cliente puede conectarse al copaper para recibir los datos de tinta para el dibujo. El cliente llama primero al método [IPaper:: redraw](ipaper--redraw.md) en el objeto de copaper para solicitar todos los datos de tinta del dibujo actual. La implementación de copapers de redraw usa la implementación de cliente de [**IPaperSink**](ipapersink-methods.md) para pasar los datos al cliente.

A medida que el usuario dibuja interactivamente en el cliente, pinta los datos inmediatamente en la pantalla y, al mismo tiempo, lo envía al papel para guardarlos. Cuando el cliente requiere que se vuelva a dibujar la pantalla, llama al método de [redibujo](ipaper--redraw.md) de copapeles. Este repintado es habitual en las aplicaciones. Por ejemplo, la repintado se produce cuando la ventana de cliente está superpuesta por otra ventana de la aplicación. El cliente tiene una representación de mapa de bits de la imagen dibujada, pero el mapa de bits se pierde fácilmente y se debe volver a dibujar. El cliente se basa en el copapel del servidor para los datos de tinta necesarios para volver a pintar.

Se trata de una división de trabajo de cliente/servidor común. Es especialmente adecuado cuando hay un requisito para que varios clientes compartan los datos. El código de copapeles se codifica para habilitarlo. Usa la utilidad APPUTIL CThreaded para lograr la seguridad para subprocesos. Una aplicación que puede aprovechar este diseño es una aplicación de pizarra compartida, donde varios clientes pueden contribuir a un dibujo de uso común. La compatibilidad con COM para COM distribuido (DCOM) es compatible con este tipo de uso de aplicaciones de grupo de trabajo a través de la red. Para obtener más información, consulte el ejemplo de REMCLIEN anterior.

Un uso más modesto del esquema de cliente/servidor de copaper consiste en integrar el comportamiento de los objetos implementados en diferentes aplicaciones en el mismo equipo. En este caso, los clientes podrían ser un contenedor ActiveX en aplicaciones independientes que comparten datos administrados por el mismo objeto. Es posible que estos datos no sean los datos de dibujo de tinta que admite el componente DllPaper. **StoServe** se puede usar como un marco de inicio para programar componentes que administran otros tipos de datos compartidos.

## <a name="support-information"></a>Información complementaria

El archivo make de **StoServe** registra el componente com de **StoServe** DllPaper en el registro. Este componente se debe registrar antes de que **StoServe** esté disponible para los clientes com externos como servidor para ese componente. Este registro automático se realiza mediante la utilidad de Register.exe integrada en el ejemplo de registro. Para compilar o ejecutar **StoServe**, cree primero el ejemplo de código de registro.

Para obtener más información acerca de cómo configurar el sistema para compilar y probar los ejemplos de código de esta serie de tutoriales de COM, vea [Cómo crear ejemplos](how-to-build-samples.md). El archivo make proporcionado (make) es compatible con Microsoft NMAKE. Para crear una compilación de depuración, emita el comando NMAKE en la ventana del símbolo del sistema.

Para un uso práctico en Microsoft Visual Studio, se proporciona un archivo de proyecto para cada ejemplo. Para cargar el proyecto para el ejemplo de **StoServe** , puede ejecutar Visual Studio en el símbolo del sistema en el directorio Samples como se indica a continuación:

MSDEV STOSERVE. DSP

También puede hacer doble clic en el archivo Stoserve. DSP en el explorador de Windows para cargar un proyecto de ejemplo en Visual Studio. En Visual Studio puede examinar las clases de C++ del origen de ejemplo y, por lo general, realizar las demás operaciones de edición-compilación-depuración.

> [!Note]  
> Como parte del kit de desarrollo de software (SDK) de la plataforma, la compilación de estos ejemplos desde dentro de Visual Studio requiere la configuración adecuada de las rutas de acceso de directorio en Visual Studio. Para obtener más información, vea [Cómo crear ejemplos](how-to-build-samples.md).

 

 

 