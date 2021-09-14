---
title: Comparación de la aceleración de hardware de Direct2D y GDI
description: Direct2D y GDI son API de representación 2D en modo inmediato y ambas ofrecen cierto grado de aceleración de hardware.
ms.assetid: 0028a0c3-445d-46b7-b55b-46dff3bce9ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f05dce8719f4d07d3160c65b88570391c3eb736
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164190"
---
# <a name="comparing-direct2d-and-gdi-hardware-acceleration"></a>Comparación de la aceleración de hardware de Direct2D y GDI

[Direct2D](./direct2d-portal.md) y [GDI son](/windows/desktop/gdi/windows-gdi) API de representación 2D en modo inmediato y ambas ofrecen cierto grado de aceleración de hardware. En este tema se exploran las diferencias entre Direct2D y GDI, incluidas las diferencias pasadas y presentes en las características de aceleración de hardware de ambas API.

Este tema tiene las siguientes partes:

-   [Diferencias entre Direct2D y GDI](#differences-between-direct2d-and-gdi)
-   [Aceleración de hardware de GDI y Direct2D](#gdi-and-direct2d-hardware-acceleration)
    -   [Aumento de la complejidad y el tamaño de los controladores de pantalla](#increasing-complexity-and-size-of-display-drivers)
    -   [Dificultad para sincronizar la sesión y los espacios de direcciones globales del kernel](#difficulty-in-synchronizing-session-and-global-kernel-address-spaces)
    -   [Administración de ventanas compuestas](#composited-window-management)
-   [Representación de GDI en Windows 7](#gdi-rendering-in-windows-7)
-   [Contraste de la aceleración de Direct2D y GDI en Windows 7](#contrasting-direct2d-and-gdi-acceleration-in-windows-7)
    -   [Ubicación de los recursos](#location-of-resources)
    -   [Método de representación](#rendering-method)
    -   [Escalabilidad](#scalability)
    -   [Ubicación](#location-of-resources)
    -   [Disponibilidad de la aceleración de hardware](#availability-of-hardware-acceleration)
    -   [Modelo de presentación](#presentation-model)
-   [Conclusión](#conclusion)

## <a name="differences-between-direct2d-and-gdi"></a>Diferencias entre Direct2D y GDI

[GDI](/windows/desktop/gdi/windows-gdi) representa geometrías opacas con alias, como polígonos, elipses y líneas. Representa texto con alias y ClearType, y puede admitir la combinación de transparencia a través de alphablend API. Sin embargo, su control de transparencia es incoherente y la mayoría de las API de GDI simplemente omiten el canal alfa. Algunas API de GDI garantizan lo que contendrá el canal alfa después de una operación. Lo que es más importante, la representación de GDI no se asigna fácilmente a las operaciones 3D y una GPU moderna se representa de forma más eficaz en la parte 3D de su motor de representación. Por ejemplo, las líneas con alias de [Direct2D](./direct2d-portal.md)están diseñadas para implementarse simplemente como dos triángulos representados en la GPU, mientras que GDI usa el algoritmo de dibujo de línea de Bresenham.

[Direct2D](./direct2d-portal.md) representa primitivas opacas, transparentes, con alias y con suavizado de alias. A menudo, las URI modernas usan la transparencia y la animación. Direct2D facilita la creación de una interfaz de usuario moderna porque tiene garantías estrictas sobre cómo acepta y representa contenido transparente, y todas sus primitivas se representan mediante la aceleración de hardware. Direct2D no es un superconjunto puro de [GDI:](/windows/desktop/gdi/windows-gdi)los primitivos que habrían sido excesivamente lentos cuando se implementan en una GPU no están presentes en Direct2D. Como Direct2D se ha creado con este énfasis en la aceleración 3D, también es fácil de usar con Direct3D.

Desde Windows NT 4, [GDI](/windows/desktop/gdi/windows-gdi) se ha ejecutado en modo kernel. La aplicación llama a GDI, que luego llama a su homólogo en modo kernel, que pasa las primitivas a su propio modelo de controlador. A continuación, este controlador envía los resultados al controlador de visualización del modo kernel global.

A partir Windows 2000, [GDI](/windows/desktop/gdi/windows-gdi) y los controladores GDI se han ejecutado en un espacio independiente en el kernel denominado "espacio de sesión". Se crea un espacio de direcciones de sesión para cada sesión de inicio de sesión y cada instancia de GDI se ejecuta de forma independiente en este espacio de direcciones en modo kernel distinto. Sin embargo, Direct2D se ejecuta en modo de usuario y pasa comandos de dibujo a través del controlador Direct3D en modo de usuario al controlador en modo kernel.

![Figura 1: direct2d en comparación con gdi](images/direct2d-vs-gdi1.png)

## <a name="gdi-and-direct2d-hardware-acceleration"></a>Aceleración de hardware de GDI y Direct2D

La diferencia más importante entre la aceleración de hardware [de Direct2D](./direct2d-portal.md) y [GDI](/windows/desktop/gdi/windows-gdi) es la tecnología subyacente que las impulsa. Direct2D está en capas sobre Direct3D y GDI tiene su propio modelo de controlador, la interfaz de controlador de dispositivos GDI (DDI), que corresponde a las primitivas de GDI. El modelo de controlador direct3D corresponde a lo que representa el hardware de representación 3D en una GPU. Cuando se definió por primera vez el DDI de GDI, la mayoría del hardware de aceleración de pantalla tenía como destino las primitivas de GDI. Con el tiempo, cada vez se ha puesto más énfasis en la aceleración de juegos 3D y menos en la aceleración de aplicaciones. Como consecuencia, la API de BitBlt estaba acelerada por hardware y la mayoría de las demás operaciones GDI no lo estaban.

Esto establece la fase de una secuencia de cambios en la representación [de GDI](/windows/desktop/gdi/windows-gdi) en la pantalla. En la ilustración siguiente se muestra cómo ha cambiado la representación de pantalla de GDI Windows XP a Windows 7.

![figura 2: evolución de la representación de pantalla gdi](images/direct2d-vs-gdi2.png)

También hubo una serie de factores adicionales que provocaron cambios en el modelo de controlador [GDI,](/windows/desktop/gdi/windows-gdi) como se explica a continuación.

### <a name="increasing-complexity-and-size-of-display-drivers"></a>Aumento de la complejidad y el tamaño de los controladores de pantalla

Los controladores 3D se han vuelto más complejos con el tiempo. El código más complejo tiende a tener más defectos, lo que hace que sea beneficioso que el controlador exista en modo de usuario, donde un error del controlador no puede provocar un reinicio del sistema. Como se puede ver en la ilustración anterior, el controlador de pantalla se divide en un componente de modo de usuario complejo y un componente de modo kernel más sencillo.

### <a name="difficulty-in-synchronizing-session-and-global-kernel-address-spaces"></a>Dificultad para sincronizar la sesión y los espacios de direcciones globales del kernel

En Windows XP, existe un controlador de pantalla en dos espacios de direcciones diferentes: espacio de sesión y espacio de kernel. Las partes del controlador deben responder a eventos como los eventos de administración de energía. Esto debe sincronizarse con el estado del controlador en el espacio de direcciones de la sesión. Se trata de una tarea difícil y puede dar lugar a defectos cuando los controladores de pantalla intentan tratar con estos espacios de direcciones distintos.

### <a name="composited-window-management"></a>Administración de ventanas compuestas

El Administrador de ventanas de escritorio (DWM), el administrador de ventanas de composición introducido en Windows 7, representa todas las ventanas en superficies fuera de la pantalla y, a continuación, las compone para mostrarlas en pantalla. Esto requiere [que GDI](/windows/desktop/gdi/windows-gdi) pueda representarse en una superficie que, a continuación, direct3D representará para mostrarse. Esto planteaba un problema en el modelo de controlador XP, ya que GDI y Direct3D eran pilas de controladores paralelas.

Como resultado, en Windows Vista, el controlador de pantalla DDI de [GDI](/windows/desktop/gdi/windows-gdi) se implementó como el controlador de pantalla canónico (CDD) proporcionado por Microsoft que representó el contenido GDI en un mapa de bits de memoria del sistema que se componerá en la pantalla.

## <a name="gdi-rendering-in-windows-7"></a>Representación de GDI en Windows 7

El modelo de controlador usado en Windows Vista requiere que cada [ventana GDI](/windows/desktop/gdi/windows-gdi) tenga el respaldo de una superficie de memoria de vídeo y una superficie de memoria del sistema. Esto dio lugar a que se usara la memoria del sistema para cada ventana GDI.

Por esta razón, [GDI](/windows/desktop/gdi/windows-gdi) se cambió de nuevo en Windows 7. . En lugar de representarse en una superficie de memoria del sistema, GDI se modificó para representarse en un segmento de memoria de apertura. La memoria de apertura se puede actualizar desde la superficie de memoria de vídeo que contiene el contenido de la ventana. GDI puede volver a representarse en la memoria de apertura y el resultado se puede devolver a la superficie de la ventana. Dado que el segmento de memoria de apertura es direccionable por la GPU, la GPU puede acelerar estas actualizaciones en la superficie de memoria de vídeo. Por ejemplo, la representación de texto, BitBlts, AlphaBlend, TransparentBlt y StretchBlt se aceleran en estos casos.

## <a name="contrasting-direct2d-and-gdi-acceleration-in-windows-7"></a>Contraste de la aceleración de Direct2D y GDI en Windows 7

[Direct2D](./direct2d-portal.md) y [GDI](/windows/desktop/gdi/windows-gdi) son API de representación en modo inmediato 2D y aceleradas por hardware. Sin embargo, hay una serie de diferencias que permanecen en ambas API.

### <a name="location-of-resources"></a>Ubicación de los recursos

[GDI](/windows/desktop/gdi/windows-gdi) mantiene sus recursos, en particular mapas de bits, en la memoria del sistema de forma predeterminada. [Direct2D mantiene](./direct2d-portal.md) sus recursos en la memoria de vídeo en el adaptador de pantalla. Cuando GDI necesita actualizar la memoria de vídeo, debe hacerse a través del bus, a menos que el recurso ya esté en el segmento de memoria de apertura o si la operación se puede expresar directamente. Por el contrario, Direct2D puede traducir simplemente sus primitivas a primitivas de Direct3D porque los recursos ya están en memoria de vídeo.

### <a name="rendering-method"></a>Método de representación

Para mantener la compatibilidad, [GDI](/windows/desktop/gdi/windows-gdi) realiza una gran parte de su representación en la memoria de apertura mediante la CPU. Por el contrario, [Direct2D](./direct2d-portal.md) traduce sus llamadas API en primitivas de Direct3D y operaciones de dibujo. A continuación, el resultado se representa en la GPU. Parte de la representación de GDI se realiza en la GPU cuando la memoria de apertura se copia en la superficie de memoria de vídeo que representa la ventana GDI.

### <a name="scalability"></a>Escalabilidad

Las llamadas de representación de [Direct2D](./direct2d-portal.md)son secuencias de comandos independientes a la GPU. Cada factoría de Direct2D representa un dispositivo Direct3D diferente. [GDI](/windows/desktop/gdi/windows-gdi) usa un flujo de comandos para todas las aplicaciones del sistema. El método de GDI puede dar lugar a una acumulación de sobrecarga de contexto de representación de CPU y GPU.

### <a name="location"></a>Location

[Direct2D](./direct2d-portal.md) funciona completamente en modo de usuario, incluido el tiempo de ejecución de Direct3D y el controlador Direct3D en modo de usuario. Esto ayuda a evitar bloqueos del sistema causados por defectos de código en el kernel. [Sin embargo, GDI](/windows/desktop/gdi/windows-gdi)tiene la mayor parte de su funcionalidad en el espacio de sesión en modo kernel, con su superficie de API en modo de usuario.

### <a name="availability-of-hardware-acceleration"></a>Disponibilidad de la aceleración de hardware

[GDI](/windows/desktop/gdi/windows-gdi) se acelera por hardware en Windows XP y se acelera en Windows 7 cuando el Administrador de ventanas de escritorio se ejecuta y se usa un controlador WDDM 1.1. [Direct2D es](./direct2d-portal.md) un hardware acelerado en casi cualquier controlador WDDM y tanto si DWM está en uso como si no. En Vista, GDI siempre se representará en la CPU.

### <a name="presentation-model"></a>Modelo de presentación

Cuando Windows diseño, no había memoria suficiente para permitir que cada ventana se almacenara en su propio mapa de bits. Como resultado, [GDI](/windows/desktop/gdi/windows-gdi) siempre se representaba lógicamente directamente en la pantalla, con varias regiones de recorte aplicadas para garantizar que una aplicación no se representara fuera de su ventana. En el [modelo de Direct2D,](./direct2d-portal.md) una aplicación se representa en un búfer de reserva y el resultado se muestra cuando la aplicación ha terminado de dibujarse. Esto permite que Direct2D controle los escenarios de animación de forma mucho más fluida de lo que puede GDI.

## <a name="conclusion"></a>Conclusión

El [código GDI](/windows/desktop/gdi/windows-gdi) existente seguirá funcionando bien en Windows 7. Sin embargo, al escribir código de representación de gráficos nuevo, se debe tener en cuenta [Direct2D,](./direct2d-portal.md) ya que aprovecha mejor las GPU modernas.

 

 