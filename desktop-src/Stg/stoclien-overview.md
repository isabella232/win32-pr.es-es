---
title: Información general de StoClien
description: En el ejemplo StoClien se muestra cómo el cliente usa el almacenamiento estructurado y cómo dirige un componente de servidor para que use este almacenamiento.
ms.assetid: 1f540e0f-2189-4f45-aad3-9b4b56732907
keywords:
- Información general de StoClien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee37f6f84cf981bda637abbd96ff8e8f0314d8ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665577"
---
# <a name="stoclien-overview"></a>Información general de StoClien

## <a name="purpose"></a>Propósito

El enfoque principal del ejemplo [StoClien](structured-storage-client-sample--stoclien-.md) es cómo el cliente usa el almacenamiento estructurado y cómo indica a un componente de servidor que use este almacenamiento. En el ejemplo StoClien se muestra un modelo de programación de servicios de almacenamiento estructurado.

## <a name="functionality"></a>Funcionalidad

La funcionalidad [StoClien](structured-storage-client-sample--stoclien-.md) es similar a los ejemplos de "Scribble" en algunas versiones de Microsoft Visual C++. La diferencia entre el ejemplo StoClien y el ejemplo [StoServe](structured-storage-server-sample--stoserve-.md) es una arquitectura interna basada en la tecnología com. Una distinción de arquitectura clara se mantiene entre el cliente COM y el servidor COM.

[StoClien](structured-storage-client-sample--stoclien-.md) carga y guarda sus dibujos en el almacenamiento estructurado de archivos compuestos com.

En el ejemplo [StoClien](structured-storage-client-sample--stoclien-.md) se crea y se usa el objeto com de copaper conectable que se proporciona como \_ componente DllPaper CLSID en el servidor [StoServe](structured-storage-server-sample--stoserve-.md) . El cliente StoClien crea un objeto de copaper y lo controla a través de la interfaz IPaper que expone el objeto. StoClien obtiene los datos de dibujo del usuario y los representa gráficamente en una ventana que administra. StoClien usa la interfaz IPaper de copaper para guardar los datos de dibujo en copapeles y dirigir las operaciones de almacenamiento de archivos en estos datos.

Un objeto COM de copapeles encapsula solo el almacenamiento basado en servidor de los datos del papel de dibujo: no se proporciona ningún comportamiento de la interfaz gráfica de usuario (GUI) en el lado del servidor. Todo el comportamiento de la interfaz gráfica de usuario está aislado en el cliente. Las características de almacenamiento y administración de datos de los objetos de copaper solo están disponibles a través de una interfaz personalizada COM, IPaper.

[StoClien](structured-storage-client-sample--stoclien-.md) coopera con el copapel para cargar y guardar los datos del dibujo de copapeles. StoClien obtiene una interfaz [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) para el objeto de almacenamiento en un archivo compuesto. En las operaciones de carga y guardado, StoClien pasa un puntero a la interfaz **IStorage** para copaper en el servidor. El copaper usa el **IStorage** proporcionado para crear secuencias en el almacenamiento. El copaper puede usar la interfaz [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) estándar para leer y escribir los datos de dibujo que administra.

El copapel solo administra los datos del dibujo; no realiza ninguna acción de la GUI. [StoClien](structured-storage-client-sample--stoclien-.md) proporciona la interfaz gráfica de usuario para la aplicación de dibujo. Lo encapsula en un objeto central de C++ CGuiPaper.

[StoClien](structured-storage-client-sample--stoclien-.md) también implementa la interfaz personalizada de IPaperSink en un objeto COPaperSink com y conecta esta interfaz con un punto de conexión adecuado en el objeto de copaper del servidor. El copaper usa la interfaz IPaperSink conectada para volver a enviar las notificaciones a StoClien. La repintado normal de la GUI de los datos del dibujo de copapeles se realiza en StoClien con la tecnología de objetos conectables de copapeles.

[StoClien](structured-storage-client-sample--stoclien-.md) es una aplicación que puede ejecutar directamente de forma normal o desde la ventana del símbolo del sistema. StoClien acepta un parámetro de nombre de archivo opcional en la línea de comandos.

En el ejemplo siguiente, Drawing. PAP es un archivo compuesto que contiene almacenamiento estructurado compatible con DllPaper de datos de dibujo. Si no se especifica ningún parámetro de nombre de archivo de línea de comandos, [StoClien](structured-storage-client-sample--stoclien-.md) usa el nombre de archivo predeterminado StoClien. PAP e intenta abrirlo en el mismo directorio que el Stoclien.exe en ejecución.

**StoClien c: \\ dibujos \\ Drawing. PAP**

## <a name="support-information"></a>Información complementaria

Para obtener más información, descripciones funcionales y un tutorial de código para [StoClien](structured-storage-client-sample--stoclien-.md), consulte la sección sobre el paseo por el código de Stoclien.htm. Para obtener más información acerca de la operación de usuario externo de StoClien, consulte las secciones uso y operación de Stoclien.htm. Para leer Stoclient.htm, ejecute Tutorial.exe en el directorio principal del tutorial y haga clic en la lección StoClien en la tabla de lecciones. O bien, haga clic en Stoclien.htm después de buscar el directorio principal del tutorial en el explorador de Windows. Para obtener más información sobre cómo funciona [**StoServe**](structured-storage-server-sample--stoserve-.md) y expone sus servicios a StoClien, consulte Stoserve.htm en el directorio principal del tutorial. Tenga en cuenta que debe compilar el Stoserve.dll antes de generar StoClien. El archivo make de [**StoServe**](structured-storage-server-sample--stoserve-.md) registra ese servidor en el registro del sistema, por lo que debe compilar [**StoServe**](structured-storage-server-sample--stoserve-.md) antes de intentar ejecutar StoClien.

Para obtener más información sobre cómo configurar un sistema para compilar y probar los ejemplos de código de esta serie de tutoriales de COM, vea [Cómo crear ejemplos](how-to-build-samples.md). El archivo make proporcionado (make) es compatible con Microsoft NMAKE. Para crear una compilación de depuración, emita el comando NMAKE en la ventana del símbolo del sistema.

Para mayor comodidad, se proporciona un archivo de proyecto para cada ejemplo que se usa en Microsoft Visual Studio. Para cargar el proyecto para el ejemplo [StoClien](structured-storage-client-sample--stoclien-.md) , ejecute Visual Studio en el símbolo del sistema en el directorio de ejemplo de la siguiente manera:

MSDEV STOCLIEN. DSP

También puede hacer doble clic en el archivo Stoclient. DSP en el explorador de Windows para cargar un proyecto de ejemplo en Visual Studio. En Visual Studio, puede examinar las clases de C++ del origen de ejemplo y, por lo general, realizar las demás operaciones de edición-compilación-depuración. Tenga en cuenta que, como parte del SDK del servidor, la compilación de estos ejemplos desde dentro de Visual Studio requiere la configuración adecuada de las rutas de acceso de directorio en Visual Studio. Para obtener más información, vea [Cómo crear ejemplos](how-to-build-samples.md).

## <a name="remarks"></a>Observaciones

El ejemplo de cliente y otros ejemplos relacionados deben compilarse antes de poder ejecutar el cliente. Para obtener más información sobre la creación de los ejemplos, vea [Cómo crear ejemplos](how-to-build-samples.md). Si ha creado los ejemplos adecuados, Stoclien.exe es el ejecutable de cliente que se ejecutará para este ejemplo.

La aplicación Stoclien.exe proporciona la interfaz de usuario para este tutorial. Ejercita los Stoserve.dll asociados, pero independientes, para demostrar el uso de cliente y servidor del almacenamiento estructurado COM en archivos compuestos.

 

 




