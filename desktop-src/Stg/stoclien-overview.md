---
title: Información general de StoClien
description: En el ejemplo de StoClien se muestra cómo el cliente usa el almacenamiento estructurado y cómo dirige a un componente de servidor para que use este almacenamiento.
ms.assetid: 1f540e0f-2189-4f45-aad3-9b4b56732907
keywords:
- Información general de StoClien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a28c8d0f4740b5a1d5f93934fb055d16e2ed9d843bcb11b210e6cde9589d53b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661855"
---
# <a name="stoclien-overview"></a>Información general de StoClien

## <a name="purpose"></a>Propósito

El enfoque principal del [ejemplo de StoClien](structured-storage-client-sample--stoclien-.md) es cómo el cliente usa el almacenamiento estructurado y cómo indica a un componente de servidor que use este almacenamiento. El ejemplo StoClien muestra un modelo de programación de servicios de almacenamiento estructurado.

## <a name="functionality"></a>Funcionalidad

La [funcionalidad de StoClien](structured-storage-client-sample--stoclien-.md) es similar a los ejemplos de "scribble" en algunas versiones de Microsoft Visual C++. La diferencia entre el ejemplo de StoClien y [el ejemplo de StoServe](structured-storage-server-sample--stoserve-.md) es una arquitectura interna basada en la tecnología COM. Se mantiene una distinción de arquitectura clara entre el cliente COM y el servidor COM.

[StoClien carga](structured-storage-client-sample--stoclien-.md) y guarda sus dibujos en el almacenamiento estructurado de archivos compuestos COM.

El [ejemplo De StoClien](structured-storage-client-sample--stoclien-.md) crea y usa el objeto COM de COPaper conectable que se proporciona como el componente \_ ClSID DllPaper en el servidor de [StoServe.](structured-storage-server-sample--stoserve-.md) El cliente de StoClien crea un objeto COPaper y lo controla a través de la interfaz IPaper que expone el objeto. StoClien obtiene datos de dibujo del usuario y los representa gráficamente en una ventana que administra. StoClien usa la interfaz COPaper IPaper para guardar los datos de dibujo en COPaper y para dirigir las operaciones de almacenamiento de archivos en estos datos.

Un objeto COM COPaper encapsula solo el almacenamiento basado en servidor de los datos de papel de dibujo: no se proporciona ningún comportamiento de interfaz gráfica de usuario (GUI) en el lado servidor. Todo el comportamiento de la GUI está aislado en el cliente. Las características de administración de datos y almacenamiento de objetos COPaper solo están disponibles a través de una interfaz personalizada COM, IPaper.

[StoClien colabora](structured-storage-client-sample--stoclien-.md) con el COPaper para cargar y guardar los datos de dibujo del COPaper. StoClien obtiene una interfaz [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) para el objeto de almacenamiento en un archivo compuesto. En sus operaciones de carga y guardado, StoClien pasa un puntero a la interfaz **IStorage** a COPaper en el servidor. COPaper usa el **IStorage proporcionado** para crear secuencias en el almacenamiento. A continuación, COPaper puede usar la interfaz [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) estándar para leer y escribir los datos de dibujo que administra.

COPaper solo administra los datos de dibujo; no realiza ninguna acción de GUI. [StoClien proporciona](structured-storage-client-sample--stoclien-.md) la GUI para la aplicación de dibujo. Encapsula esto en un objeto CGuiPaper central de C++.

[StoClien también](structured-storage-client-sample--stoclien-.md) implementa la interfaz IPaperSink personalizada en un objeto COM COPaperSink y conecta esta interfaz a un punto de conexión adecuado en el objeto COPaper del servidor. COPaper usa la interfaz IPaperSink conectada para enviar notificaciones de vuelta a StoClien. El repintado normal de la GUI de los datos de dibujo de COPaper se realiza en StoClien mediante la tecnología de objetos conectables COPaper.

[StoClien es](structured-storage-client-sample--stoclien-.md) una aplicación que se puede ejecutar directamente de la manera normal o desde la ventana del símbolo del sistema. StoClien acepta un parámetro de nombre de archivo opcional en la línea de comandos.

En el ejemplo siguiente, Drawing.pap es un archivo compuesto que contiene almacenamiento estructurado compatible con DllPaper de datos de dibujo. Si no se especifica ningún parámetro de nombre de archivo de línea de comandos, [StoClien](structured-storage-client-sample--stoclien-.md) usa el nombre de archivo predeterminado Stoclien.pap e intenta abrirlo en el mismo directorio que el Stoclien.exe.

**StoClien c: \\ drawings \\ drawing.pap**

## <a name="support-information"></a>Información complementaria

Para obtener más información, descripciones funcionales y un tutorial de código [para StoClien,](structured-storage-client-sample--stoclien-.md)consulte la sección Paseo por el código en Stoclien.htm. Para obtener más información sobre la operación de usuario externo de StoClien, vea las secciones Uso y Operación en Stoclien.htm. Para leer Stoclient.htm, ejecute Tutorial.exe en el directorio principal del tutorial y haga clic en la lección StoClien de la tabla de lecciones. Como alternativa, haga clic Stoclien.htm después de buscar el directorio principal del tutorial en Windows Explorer. Para obtener más información sobre cómo [**funciona StoServe**](structured-storage-server-sample--stoserve-.md) y expone sus servicios a StoClien, consulte Stoserve.htm en el directorio principal del tutorial. Tenga en cuenta que debe compilar el Stoserve.dll antes de compilar StoClien. El archivo Make para [**StoServe**](structured-storage-server-sample--stoserve-.md) registra ese servidor en el registro del sistema, por lo que debe compilar [**StoServe**](structured-storage-server-sample--stoserve-.md) antes de intentar ejecutar StoClien.

Para obtener más información sobre cómo configurar un sistema para compilar y probar los ejemplos de código de esta serie de tutoriales COM, vea [How to Build Samples](how-to-build-samples.md). El archivo make proporcionado (MAKEFILE) es compatible con Microsoft NMAKE. Para crear una compilación de depuración, emita el comando NMAKE en la ventana del símbolo del sistema.

Para mayor comodidad, se proporciona un archivo de proyecto para cada ejemplo para su uso en Microsoft Visual Studio. Para cargar el proyecto para el [ejemplo de StoClien,](structured-storage-client-sample--stoclien-.md) ejecute Visual Studio en el símbolo del sistema en el directorio de ejemplo como se indica a continuación:

MSDEV STOCLIEN. Dsp

También puede hacer doble clic en el archivo Stoclient.dsp en Windows Explorer para cargar un proyecto de ejemplo en Visual Studio. En Visual Studio, puede examinar las clases de C++ del origen de ejemplo y, por lo general, realizar las demás operaciones de edición,compilación y depuración. Tenga en cuenta que, como parte del SDK de servidor, la compilación de estos ejemplos desde dentro de Visual Studio requiere la configuración adecuada de las rutas de acceso de directorio en Visual Studio. Para obtener más información, [vea How to Build Samples](how-to-build-samples.md).

## <a name="remarks"></a>Comentarios

El ejemplo de cliente y otros ejemplos relacionados deben compilarse para poder ejecutar el cliente. Para obtener más información sobre cómo compilar los ejemplos, [vea How to Build Samples](how-to-build-samples.md). Si ha creado los ejemplos adecuados, Stoclien.exe es el ejecutable del cliente que se va a ejecutar para este ejemplo.

La Stoclien.exe proporciona la interfaz de usuario para este tutorial. Se usa el almacenamiento estructurado COM asociado, pero independiente, Stoserve.dll para demostrar el uso de cliente y servidor del almacenamiento estructurado COM en archivos compuestos.

 

 




