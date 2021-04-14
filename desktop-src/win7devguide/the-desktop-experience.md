---
title: Experiencia de escritorio
description: El nuevo escritorio de Windows 7 pone en vida las aplicaciones.
ms.assetid: e706167a-435b-4c32-bb64-87113f368866
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3476f70c46aecceb365e17dba1803b876fd51e8d
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/06/2021
ms.locfileid: "104564993"
---
# <a name="the-desktop-experience"></a>Experiencia de escritorio

El nuevo escritorio de Windows 7 pone en vida las aplicaciones. Ahora, las aplicaciones son más reconocibles e interactivas. Las interfaces de usuario modernas e intuitivas son más fáciles de desarrollar con Windows 7. Las nuevas experiencias de escritorio y aplicación incluyen lo siguiente:

-   La barra de tareas mejorada incluye miniaturas interactivas y permite animar e interactuar con las aplicaciones minimizadas.
-   El concepto de destinos permite a los usuarios saltar con un solo clic a los archivos, ubicaciones o tareas que usan con mayor frecuencia.
-   Los nuevos controles y las API de la *cinta* de opciones, basados en la interfaz de usuario de Office Fluent, están disponibles para agregar fácilmente controles, menús y galerías de estilo de *la cinta* de opciones a las aplicaciones.
-   Un marco de animación le ayuda a mejorar las animaciones personalizadas.

Las mejoras en la plataforma de gadgets permiten a las aplicaciones instalar gadgets complementarios durante la instalación o la primera ejecución.

![Captura de pantalla que muestra el escritorio de Windows 7.](images/windows7-6.jpg)

El nuevo escritorio de Windows 7 pone las aplicaciones en vida

## <a name="jump-listsgetting-users-into-your-application-quickly"></a>Jump Lists: obtener rápidamente a los usuarios de la aplicación

Las listas de accesos directos ayudan a los usuarios a empezar a trabajar más rápido. Las listas de accesos directos son archivos, direcciones URL, tareas o elementos personalizados que se abren dentro de la aplicación. El nuevo menú Jump Lists del menú *Inicio* y la barra de tareas hacen que los destinos y las tareas clave comunes estén disponibles con un solo clic. El menú Jump Lists se rellena automáticamente en función de la frecuencia y el uso de los elementos recientes. Los desarrolladores pueden proporcionar listas de saltos personalizadas basadas en su propia semántica. Las aplicaciones también pueden definir *tareas* para que aparezcan en sus menús; estas son las acciones de la aplicación a las que los usuarios desean acceder directamente, como la creación de un correo electrónico. (Consulte [las extensiones](../shell/taskbar-extensions.md) de la barra de tareas y la [interfaz ICustomDestinationList](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist)).

![Jump Lists](images/windows7-7.jpg)

Las listas de accesos directos ayudan a los usuarios a empezar a trabajar más rápido

## <a name="enhanced-taskbar"></a>Barra de tareas mejorada

Con la nueva barra de tareas de Windows 7, las aplicaciones pueden proporcionar más información al usuario de maneras más intuitivas. Por ejemplo, las aplicaciones pueden mostrar barras de progreso en los botones de la barra de tareas para que los usuarios puedan seguir teniendo en cuenta el progreso sin tener que mantener la ventana visible. Esto resulta útil para realizar un seguimiento de las operaciones que consumen mucho tiempo, como la copia de archivos, las descargas, las instalaciones o la grabación multimedia. Las superposiciones de los iconos se pueden mostrar en el área inferior derecha del botón de la barra de tareas de la aplicación, y se usan para comunicar el estado o las notificaciones (por ejemplo, nuevo correo). Las nuevas API de miniaturas permiten a una aplicación definir ventanas secundarias e imágenes en miniatura correspondientes para esas ventanas. La barra de herramientas de miniaturas proporciona un lugar para controlar las acciones comunes sin necesidad de restaurar la ventana, como *reproducir/detener* para medios. (Consulte [extensiones](../shell/taskbar-extensions.md) de la barra de tareas y [Windows 7: recursos para desarrolladores](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples)).

## <a name="gadgets-platform"></a>Plataforma de gadgets

Los gadgets son una característica popular del escritorio de Windows Vista y, en Windows 7, es aún más fácil para las aplicaciones instalar gadgets. En Windows 7, una aplicación puede Agregar un gadget al escritorio de Windows mediante programación durante la instalación de la aplicación o la primera ejecución. Esto significa que la experiencia rápida de una aplicación puede incluir una casilla simple, por ejemplo, para instalar un gadget complementario que esté disponible en el escritorio en cuanto la aplicación esté lista para usarse. (Consulte [Introducción a la plataforma de gadgets](/previous-versions/windows/desktop/gadgetplatform/introduction-to-the-gadget-platform)).

![Gadgets de Windows](images/windows7-8.jpg)

En Windows 7, es aún más fácil para las aplicaciones instalar gadgets

## <a name="windows-ribbon"></a>Cinta de Windows



El control de la cinta de opciones de Windows ayuda a los desarrolladores a mejorar la facilidad de uso, ya que expone las características a las que se accede con más frecuencia directamente a los usuarios finales. La cinta de opciones facilita a los usuarios finales la búsqueda y el uso de características de aplicaciones, ya que se oculta menos funcionalidad, lo que aumenta la productividad. La cinta de opciones está diseñada como una alternativa basada en la intención del modelo de presentación de comandos de los menús, las barras de herramientas, los paneles de tareas y los cuadros de diálogo de las aplicaciones estándar basadas en Windows.

Los controles de la cinta de opciones constan de un conjunto de Win32APIs que invalidan la funcionalidad de la barra de menús de nivel superior y representan en su lugar una interfaz de usuario de comandos de estilo de cinta. Es similar en la funcionalidad y la apariencia de la *cinta* de opciones en el sistema 2007 de Office. La interfaz de usuario se compone de varios SubControles que incluyen lo siguiente:

-   Botón de aplicación (o perla)
-   Barra de herramientas de acceso rápido
-   Control de *la cinta* de opciones contextuales
-   Barras de herramientas
-   Galerías de estilos

Las plantillas y la creación de marcado están disponibles para que los desarrolladores puedan desarrollar e integrar rápidamente la funcionalidad de la cinta de opciones. (Consulte [marco de cinta de Windows](../windowsribbon/-uiplat-windowsribbon-entry.md) y [marco de cinta de Windows: recursos para desarrolladores](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsRibbon)).

![barra de herramientas de la cinta](images/windows7-9.jpg)

El control ribbon ayuda a los desarrolladores a mejorar la facilidad de uso mediante la exposición de las características a las que se accede con más frecuencia.

## <a name="animation"></a>Animación

Las animaciones suaves son fundamentales para muchas aplicaciones de interfaz de usuario gráficas y Windows 7 incluye un marco de animación nativo para administrar la programación y la ejecución de animaciones. El marco de trabajo de animación proporciona una biblioteca de funciones matemáticas útiles para especificar el comportamiento a lo largo del tiempo y también permite a los desarrolladores proporcionar sus propias funciones de comportamiento. El marco de trabajo admite la resolución sofisticada de conflictos cuando varias animaciones intentan manipular el mismo valor al mismo tiempo. Una aplicación puede especificar que una animación se debe completar antes de que se pueda iniciar otra y puede forzar la finalización dentro de un tiempo establecido. El nuevo marco también ayuda a animaciones a determinar las duraciones adecuadas. (Consulte [Administrador de animaciones de Windows](../uianimation/-main-portal.md)).

 

 