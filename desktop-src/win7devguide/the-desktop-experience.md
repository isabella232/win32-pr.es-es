---
title: La experiencia de escritorio
description: La nueva Windows escritorio 7 da vida a las aplicaciones.
ms.assetid: e706167a-435b-4c32-bb64-87113f368866
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a8d62c94cfaae137a921979e514c9500376be4abf858da5b64eee5ac3c8ec6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811421"
---
# <a name="the-desktop-experience"></a>La experiencia de escritorio

La nueva Windows escritorio 7 da vida a las aplicaciones. Las aplicaciones ahora son más reconocibles, informativas e interactivas. Las interfaces de usuario modernas e intuitivas son más fáciles de desarrollar con Windows 7. Entre las nuevas experiencias de escritorio y aplicación se incluyen las siguientes:

-   La barra de tareas mejorada presenta miniaturas interactivas y permite la animación y la interacción para aplicaciones minimizadas.
-   El concepto Destinos permite a los usuarios saltar con un solo clic a los archivos, ubicaciones o tareas que usan con más frecuencia.
-   Los nuevos controles y API de la cinta de *opciones,* basados en la interfaz de usuario de Office Fluent, están disponibles para agregar fácilmente controles, menús y galerías de estilo ribbon a las aplicaciones.
-   Un marco de animación ayuda a mejorar las animaciones personalizadas.

Las mejoras en la plataforma de los dispositivos permiten a las aplicaciones instalar dispositivos complementarios durante la instalación o la experiencia de primera ejecución.

![Captura de pantalla que muestra Windows escritorio 7.](images/windows7-6.jpg)

La nueva Windows escritorio 7 da vida a las aplicaciones

## <a name="jump-listsgetting-users-into-your-application-quickly"></a>Listas de accesos rápidos: introducción rápida de usuarios a la aplicación

Las listas de accesos rápidos ayudan a los usuarios a llegar a donde quieren ir más rápido. Jump Lists son archivos, direcciones URL, tareas o elementos personalizados que se abren dentro de la aplicación. El nuevo menú Listas de accesos rápidos del *menú* Inicio y la barra de tareas hace que los destinos comunes y las tareas clave estén disponibles con un solo clic. El menú Listas de saltos se rellena automáticamente en función de la frecuencia y la frecuencia con que se han usado los elementos recientemente. Los desarrolladores pueden proporcionar listas de salto personalizadas basadas en su propia semántica. Las aplicaciones también pueden definir *tareas* para que aparezcan en sus menús: son acciones de la aplicación a las que los usuarios quieren acceder directamente, como crear un correo electrónico. (Vea [Extensiones de la barra de tareas](../shell/taskbar-extensions.md) e Interfaz [ICustomDestinationList).](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist)

![listas de saltos](images/windows7-7.jpg)

Las listas de accesos rápidos ayudan a los usuarios a llegar a donde quieren ir más rápido.

## <a name="enhanced-taskbar"></a>Barra de tareas mejorada

Con la nueva barra de tareas Windows 7, las aplicaciones pueden proporcionar más información al usuario de maneras más intuitivas. Por ejemplo, las aplicaciones pueden mostrar barras de progreso en los botones de la barra de tareas para que los usuarios puedan mantenerse al tanto del progreso sin tener que mantener la ventana visible. Esto es útil para realizar un seguimiento de las operaciones que requieren mucho tiempo, como la copia de archivos, las descargas, las instalaciones o la grabación de medios. Las superposiciones de iconos se pueden mostrar en el área inferior derecha del botón de la barra de tareas de la aplicación y se usan para comunicar el estado o las notificaciones (por ejemplo, correo nuevo). Las nuevas API de miniaturas permiten a una aplicación definir ventanas secundarias y las imágenes en miniatura correspondientes para esas ventanas. La barra de herramientas de miniaturas proporciona un lugar para controlar acciones comunes sin necesidad de restauración de ventanas, como *Reproducir/Detener* para medios. (Vea [Extensiones de la barra de](../shell/taskbar-extensions.md) tareas y Windows [7: Recursos para desarrolladores).](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples)

## <a name="gadgets-platform"></a>Plataforma Descándalo

Los artefactos son una característica popular del escritorio Windows Vista y, en Windows 7, es incluso más fácil para las aplicaciones instalar los dispositivos. En Windows 7, una aplicación puede agregar mediante programación un dispositivo al escritorio Windows durante la instalación de la aplicación o la primera ejecución. Esto significa que la experiencia lista para usar de una aplicación puede incluir una casilla simple, por ejemplo, para instalar un complemento que esté disponible en el escritorio en cuanto la aplicación esté lista para usarse. (Consulte [Introducción a la plataforma de Plataforma Dei).](/previous-versions/windows/desktop/gadgetplatform/introduction-to-the-gadget-platform)

![ventanas de windows](images/windows7-8.jpg)

En Windows 7, es incluso más fácil para las aplicaciones instalar los dispositivos.

## <a name="windows-ribbon"></a>Windows Cinta



El Windows cinta de opciones ayuda a los desarrolladores a mejorar la facilidad de uso al exponer las características a las que se accede con más frecuencia de la aplicación directamente a los usuarios finales. La cinta de opciones facilita a los usuarios finales la búsqueda y el uso de características de la aplicación, ya que hay menos funcionalidad oculta, lo que aumenta la productividad. La cinta de opciones está diseñada como una alternativa basada en intenciones al modelo de presentación de comandos de menús, barras de herramientas, paneles de tareas y cuadros de diálogo en aplicaciones basadas Windows estándar.

Los controles de la cinta de opciones constan de un conjunto de Win32APIs que invalidan la funcionalidad de la barra de menús de nivel superior y representan en su lugar una interfaz de usuario de comandos de estilo cinta de opciones. Es similar en funcionalidad y apariencia a la cinta *de* opciones del sistema de Office 2007. La interfaz de usuario se compone de varios controles secundarios que incluyen lo siguiente:

-   Botón de aplicación (o botón de la aplicación)
-   Barra de herramientas de acceso rápido
-   *Control de* cinta de opciones de pestañas contextuales
-   Mini-barras de herramientas
-   Galerías de estilo

Las plantillas y la creación de marcado están disponibles para los desarrolladores para el desarrollo rápido y la integración de la funcionalidad ribbon. (Vea [Windows Ribbon Framework](../windowsribbon/-uiplat-windowsribbon-entry.md) y Windows Ribbon [Framework: Recursos para desarrolladores).](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsRibbon)

![barra de herramientas de la cinta de opciones](images/windows7-9.jpg)

El control Ribbon ayuda a los desarrolladores a mejorar la facilidad de uso mediante la exposición de las características a las que se accede con más frecuencia.

## <a name="animation"></a>Animación

Las animaciones smooth son fundamentales para muchas aplicaciones gráficas de interfaz de usuario y Windows 7 presenta un marco de animación nativo para administrar la programación y ejecución de animaciones. El marco de animación proporciona una biblioteca de funciones matemáticas útiles para especificar el comportamiento a lo largo del tiempo y también permite a los desarrolladores proporcionar sus propias funciones de comportamiento. El marco admite una resolución sofisticada de conflictos cuando varias animaciones intentan manipular el mismo valor al mismo tiempo. Una aplicación puede especificar que una animación se debe completar antes de que otra pueda iniciarse y puede forzar la finalización en un tiempo establecido. El nuevo marco también ayuda a las animaciones a determinar las duraciones adecuadas. (Vea [Windows Animation Manager).](../uianimation/-main-portal.md)

 

 