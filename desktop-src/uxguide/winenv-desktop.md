---
title: Escritorio
description: El escritorio es el área de trabajo del usuario para sus programas. No es una forma de promover el reconocimiento de su programa o su marca. No lo Abuse.
ms.assetid: 99cb218d-9b1f-4e43-94d2-4ea74b0e10d3
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 159be01b1058eac99c30b83534b7a9eafd9c4eb4
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104083531"
---
# <a name="desktop"></a>Escritorio

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

El escritorio es el área de trabajo del usuario para sus programas. No es una forma de promover el reconocimiento de su programa o su marca. ¡ No abuse!

El escritorio es el área de trabajo en pantalla que proporciona Microsoft Windows, de forma análoga a un escritorio físico. Consta de un [área de trabajo](glossary.md) y una [barra de tareas](winenv-taskbar.md). El área de trabajo puede abarcar varios monitores.

![captura de pantalla de un escritorio de Windows típico ](images/winenv-desktop-image1.png)

Un escritorio de Windows típico.

El monitor activo es el monitor en el que se ejecuta el programa activo. El monitor predeterminado es el que tiene el menú Inicio, la barra de tareas y el área de notificación.

## <a name="design-concepts"></a>Conceptos de diseño

El escritorio de Windows tiene los siguientes puntos de acceso de programa:

-   **Área de trabajo.** Área en pantalla en la que los usuarios pueden realizar su trabajo, así como almacenar programas, documentos y sus métodos abreviados. Aunque técnicamente el escritorio incluye la barra de tareas, en la mayoría de los contextos, hace referencia solo al área de trabajo.
-   **Botón iniciar.** El punto de acceso para todos los programas y lugares especiales de Windows (documentos, imágenes, música, juegos, equipo, panel de control), con las listas de "usados más recientemente" para obtener acceso rápidamente a los programas y documentos usados recientemente.
-   **Inicio rápido. Se ha quitado de Windows 7.** Punto de acceso directo para los programas seleccionados por el usuario.
-   **Situada.** Punto de acceso para ejecutar programas que tienen presencia de escritorio. Aunque técnicamente la barra de tareas abarca toda la barra desde el botón Inicio hasta el área de notificación, en la mayoría de los contextos barra de tareas hace referencia al área de entre, que contiene los botones de la barra de tareas. A veces, esta área se denomina taskband.
-   **Deskbands. No se recomienda.** Programas funcionales y de larga ejecución minimizados, como la barra de idioma. Los programas que se minimizan a deskbands no muestran los botones de la barra de tareas cuando se minimizan.
-   **Área de notificación.** Un origen a corto plazo para las notificaciones y el estado, así como un punto de acceso para las características relacionadas con el sistema y los programas que no tienen presencia en el escritorio.

![captura de pantalla del botón Inicio, barra de tareas, miniatura ](images/winenv-desktop-image2.png)

Los puntos de acceso del escritorio de Windows incluyen el botón Inicio, la barra de tareas y el área de notificación. Observe la característica de miniaturas del botón de la barra de tareas.

**El escritorio de Windows es un recurso compartido limitado que es el punto de entrada del usuario a Windows. Dejar a los usuarios en el control.** Debe usar sus áreas según lo previsto; cualquier otro uso se debe considerar un abuso. No los vea nunca como formas de promover el reconocimiento de su programa o su [marca](exper-branding.md).

En Windows 7, los fabricantes de equipos originales (OEM) y los proveedores de hardware independientes (IHV) pueden usar Device Stage para diseñar una interfaz de usuario personalizada de la marca para el equipo y los dispositivos, sin saturar los escritorios de los usuarios. En particular, los OEM pueden usar Device Stage PC para incluir programas, ofertas de servicio y soporte técnico personalizados. Para obtener más información, vea el kit de desarrollo de la [experiencia del dispositivo de Microsoft](https://www.microsoft.com/whdc/device/DeviceExperience/Dev-Kit.mspx).

**Si solo hace algo...**

-   No abuse del escritorio: Mantenga a los usuarios en el control. Si es probable que los usuarios de destino usen el programa con frecuencia, proporcione una opción durante la instalación para colocar un acceso directo en el escritorio, no seleccionada de forma predeterminada.

## <a name="guidelines"></a>Directrices

-   **Si es muy probable que los usuarios usen el programa con frecuencia, proporcione una opción durante la instalación para colocar un acceso directo al programa en el escritorio.** La mayoría de los programas no se usarán con la frecuencia suficiente para garantizar que ofrece esta opción.
-   **Presente la opción no seleccionada de forma predeterminada.** Requerir a los usuarios que seleccionen la opción es importante porque, una vez que los iconos no deseados se encuentran en el escritorio, muchos usuarios se ven previstos para quitarlos. Esto puede dar lugar a un desorden innecesario del escritorio.
-   **Si los usuarios seleccionan la opción, solo tiene que proporcionar un acceso directo a un programa.** Si el producto consta de varios programas, proporcione un acceso directo solo al programa principal.
-   **Coloque solo los accesos directos a programas en el escritorio.** No coloque el programa real ni otros tipos de archivos.

    **Correcto:**

    ![captura de pantalla del icono de acceso directo con la superposición de flecha ](images/winenv-desktop-image3.png)

    **Incorrecto:**

    ![captura de pantalla del icono del programa ](images/winenv-desktop-image4.png)

    En el ejemplo incorrecto, el programa, no un acceso directo, se copia en el escritorio.

-   **Elija una etiqueta que se puede mostrar sin truncamiento.** Los usuarios no deben ver puntos suspensivos.

    **Correcto:**

    ![captura de pantalla del icono de acceso directo con el nombre completo ](images/winenv-desktop-image3.png)

    **Incorrecto:**

    ![captura de pantalla del icono de acceso directo con el nombre truncado ](images/winenv-desktop-image5.png)

    En el ejemplo incorrecto, la etiqueta de acceso directo del programa es tan larga que se trunca.

## <a name="documentation"></a>Documentación

-   Al hacer referencia al escritorio, use escritorio, en mayúsculas.
-   Al hacer referencia a los métodos abreviados de escritorio, use el método abreviado, en mayúsculas.

 

 