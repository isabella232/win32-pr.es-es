---
title: Escritorio
description: El escritorio es el área de trabajo del usuario para sus programas. No es una manera de promover el conocimiento de su programa o su marca. No lo maltrate.
ms.assetid: 99cb218d-9b1f-4e43-94d2-4ea74b0e10d3
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: f72230d5177ed9f0714282a8eec7168994ba9bdfd60cdeff0b0409d714d216f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119594055"
---
# <a name="desktop"></a>Escritorio

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

El escritorio es el área de trabajo del usuario para sus programas. No es una manera de promover el conocimiento de su programa o su marca. No lo maltrate.

El escritorio es el área de trabajo en pantalla proporcionada por Microsoft Windows, análoga a un escritorio físico. Consta de un área [de trabajo y una](glossary.md) barra de [tareas](winenv-taskbar.md). El área de trabajo puede abarcar varios monitores.

![captura de pantalla de un escritorio típico de Windows ](images/winenv-desktop-image1.png)

Un escritorio Windows típico.

El monitor activo es el monitor donde se ejecuta el programa activo. El monitor predeterminado es el que tiene el menú Inicio, la barra de tareas y el área de notificación.

## <a name="design-concepts"></a>Conceptos de diseño

El Windows escritorio tiene los siguientes puntos de acceso del programa:

-   **Área de trabajo.** Área en pantalla donde los usuarios pueden realizar su trabajo, así como almacenar programas, documentos y sus accesos directos. Aunque técnicamente el escritorio incluye la barra de tareas, en la mayoría de los contextos hace referencia solo al área de trabajo.
-   **botón Inicio.** Punto de acceso para todos los programas y lugares Windows especiales (Documentos, Imágenes, Música, Juegos, Equipo, Panel de control), con listas "usadas más recientemente" para acceder rápidamente a los documentos y programas usados recientemente.
-   **inicio rápido. Se ha quitado Windows 7.** Un punto de acceso directo para los programas seleccionados por el usuario.
-   **Barra.** Punto de acceso para ejecutar programas que tienen presencia en el escritorio. Aunque técnicamente la barra de tareas abarca toda la barra desde el botón Inicio hasta el área de notificación, en la mayoría de los contextos, la barra de tareas hace referencia al área entre, que contiene los botones de la barra de tareas. Esta área se conoce a veces como la banda de tareas.
-   **Deskbands. No se recomienda.** Programas funcionales y de ejecución larga minimizados, como la barra de idioma. Los programas que minimizan a deskbands no muestran botones de la barra de tareas cuando se minimizan.
-   **Área de notificación.** Un origen a corto plazo para las notificaciones y el estado, así como un punto de acceso para las características relacionadas con el sistema y el programa que no tienen presencia en el escritorio.

![captura de pantalla del botón de inicio, la barra de tareas, la miniatura ](images/winenv-desktop-image2.png)

Los Windows de acceso de escritorio incluyen el botón Inicio, la barra de tareas y el área de notificación. Observe la característica de miniatura del botón de la barra de tareas.

**El Windows es un recurso compartido limitado que es el punto de entrada del usuario para Windows. Deje a los usuarios bajo control.** Debe usar sus áreas según lo previsto: cualquier otro uso debe considerarse un abuso. No los vea nunca como maneras de promover el reconocimiento del programa o de su [marca.](exper-branding.md)

Para Windows 7, los fabricantes de equipos originales (OEM) y los fabricantes de hardware independientes (IHV) pueden usar la fase del dispositivo para diseñar una interfaz de usuario personalizada y de marca para el equipo y los dispositivos, sin desordenar los escritorios de los usuarios. En concreto, los OEM pueden usar device stage PC para ofrecer programas personalizados, ofertas de servicio y soporte técnico. Para obtener más información, vea [Microsoft Device Experience Development Kit](https://www.microsoft.com/whdc/device/DeviceExperience/Dev-Kit.mspx).

**Si solo hace una cosa...**

-   No maltrate el escritorio: mantenga a los usuarios bajo control. Si es probable que los usuarios de destino usen el programa con frecuencia, proporcione una opción durante la instalación para colocar un acceso directo en el escritorio, no seleccionado de forma predeterminada.

## <a name="guidelines"></a>Directrices

-   **Si es muy probable que los usuarios usen el programa con frecuencia, proporcione una opción durante la instalación para colocar un acceso directo de programa en el escritorio.** La mayoría de los programas no se usarán con la frecuencia suficiente para garantizar la oferta de esta opción.
-   **Presente la opción no seleccionada de forma predeterminada.** Exigir a los usuarios que seleccionen la opción es importante porque, una vez que los iconos no deseados están en el escritorio, muchos usuarios son reacios a quitarlos. Esto puede provocar un desorden innecesario en el escritorio.
-   **Si los usuarios seleccionan la opción, proporcione solo un acceso directo de programa.** Si el producto consta de varios programas, proporcione un acceso directo solo al programa principal.
-   **Coloque solo los métodos abreviados de programa en el escritorio.** No coloque el programa real ni otros tipos de archivos.

    **Correcto:**

    ![captura de pantalla del icono de acceso directo con superposición de flecha ](images/winenv-desktop-image3.png)

    **Incorrecto:**

    ![captura de pantalla del icono del programa ](images/winenv-desktop-image4.png)

    En el ejemplo incorrecto, el programa, no un acceso directo, se copia en el escritorio.

-   **Elija una etiqueta que se pueda mostrar sin truncamiento.** Los usuarios no deben ver puntos suspensivos.

    **Correcto:**

    ![captura de pantalla del icono de acceso directo con el nombre completo ](images/winenv-desktop-image3.png)

    **Incorrecto:**

    ![captura de pantalla del icono de acceso directo con nombre truncado ](images/winenv-desktop-image5.png)

    En el ejemplo incorrecto, la etiqueta de acceso directo del programa es tan larga que se trunca.

## <a name="documentation"></a>Documentación

-   Al hacer referencia al escritorio, use escritorio, sin mayúsculas.
-   Al hacer referencia a los accesos directos de escritorio, use acceso directo, sin mayúsculas.

 

 