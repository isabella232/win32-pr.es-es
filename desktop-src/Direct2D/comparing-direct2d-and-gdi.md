---
title: Comparar la aceleración de hardware de Direct2D y GDI
description: Direct2D y GDI son API de representación 2D en modo inmediato y ambos ofrecen cierto grado de aceleración de hardware.
ms.assetid: 0028a0c3-445d-46b7-b55b-46dff3bce9ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f05dce8719f4d07d3160c65b88570391c3eb736
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359015"
---
# <a name="comparing-direct2d-and-gdi-hardware-acceleration"></a>Comparar la aceleración de hardware de Direct2D y GDI

[Direct2D](./direct2d-portal.md) y [GDI](/windows/desktop/gdi/windows-gdi) son API de representación 2D en modo inmediato y ambos ofrecen cierto grado de aceleración de hardware. En este tema se analizan las diferencias entre Direct2D y GDI, incluidas las diferencias anteriores y las presentes en las características de aceleración de hardware de ambas API.

Este tema consta de las siguientes partes:

-   [Diferencias entre Direct2D y GDI](#differences-between-direct2d-and-gdi)
-   [Aceleración de hardware de GDI y Direct2D](#gdi-and-direct2d-hardware-acceleration)
    -   [Aumento de la complejidad y el tamaño de los controladores de pantalla](#increasing-complexity-and-size-of-display-drivers)
    -   [Dificultad en la sincronización de espacios de direcciones de kernel globales y de sesión](#difficulty-in-synchronizing-session-and-global-kernel-address-spaces)
    -   [Administración de ventanas compuestas](#composited-window-management)
-   [Representación de GDI en Windows 7](#gdi-rendering-in-windows-7)
-   [Comparación de la aceleración de Direct2D y GDI en Windows 7](#contrasting-direct2d-and-gdi-acceleration-in-windows-7)
    -   [Ubicación de los recursos](#location-of-resources)
    -   [Método de representación](#rendering-method)
    -   [Escalabilidad](#scalability)
    -   [Ubicación](#location-of-resources)
    -   [Disponibilidad de aceleración de hardware](#availability-of-hardware-acceleration)
    -   [Modelo de presentación](#presentation-model)
-   [Conclusión](#conclusion)

## <a name="differences-between-direct2d-and-gdi"></a>Diferencias entre Direct2D y GDI

[GDI](/windows/desktop/gdi/windows-gdi) representa geometrías opacas y con alias, como polígonos, elipses y líneas. Representa el texto con alias y ClearType, y puede admitir la combinación de transparencia a través de la API de AlphaBlend. Sin embargo, su control de transparencia es incoherente y la mayoría de las API de GDI simplemente omiten el canal alfa. Algunas API de GDI garantizan lo que contendrá el canal alfa después de una operación. Lo que es más importante, la representación de GDI no se asigna fácilmente a las operaciones 3D y una GPU moderna se representa de forma más eficaz en la parte 3D de su motor de representación. Por ejemplo, las líneas con alias de [Direct2D](./direct2d-portal.md)están diseñadas para implementarse simplemente como dos triángulos representados en la GPU, mientras que GDI usa el algoritmo de dibujo de líneas de Bresenham.

[Direct2D](./direct2d-portal.md) representa primitivos opacos, transparentes, con alias y suavizado de contorno. Las ius modernas suelen usar la transparencia y la animación. Direct2D facilita la creación de una interfaz de usuario moderna porque tiene garantías estrictas sobre cómo acepta y representa el contenido transparente, y todas sus primitivas se representan mediante la aceleración de hardware. Direct2D no es un supraconjunto puro de [GDI](/windows/desktop/gdi/windows-gdi): los primitivos que se habrían ralentizado excesivamente cuando se implementó en una GPU no están presentes en Direct2D. Dado que Direct2D se crea con este énfasis en la aceleración 3D, también es fácil de usar con Direct3D.

Desde Windows NT 4, [GDI](/windows/desktop/gdi/windows-gdi) se ha ejecutado en modo kernel. La aplicación llama a GDI que, a continuación, llama a su homólogo en modo kernel, que pasa los primitivos a su propio modelo de controlador. A continuación, este controlador envía los resultados al controlador de pantalla del modo kernel global.

A partir de Windows 2000, [GDI](/windows/desktop/gdi/windows-gdi) y los controladores GDI se han ejecutado en un espacio independiente en el kernel denominado "espacio de sesión". Se crea un espacio de direcciones de sesión para cada sesión de inicio de sesión y cada instancia de GDI se ejecuta de forma independiente en este espacio de direcciones de modo kernel distinto. Sin embargo, Direct2D se ejecuta en modo usuario y pasa los comandos de dibujo a través del controlador de Direct3D modo usuario al controlador de modo kernel.

![Figura 1: direct2d comparado con GDI](images/direct2d-vs-gdi1.png)

## <a name="gdi-and-direct2d-hardware-acceleration"></a>Aceleración de hardware de GDI y Direct2D

La diferencia más importante entre [Direct2D](./direct2d-portal.md) y la aceleración de hardware de [GDI](/windows/desktop/gdi/windows-gdi) es la tecnología subyacente que las controla. Direct2D está superpuesto en Direct3D y GDI tiene su propio modelo de controlador, la interfaz del controlador de dispositivo GDI (DDI), que corresponde a las primitivas de GDI. El modelo de controlador de Direct3D corresponde a lo que representa el hardware de representación 3D en una GPU. Cuando se definió el DDI de GDI por primera vez, la mayoría del hardware de aceleración de pantalla destinaba a los primitivos de GDI. Con el tiempo, se ha hecho más hincapié en la aceleración de juegos 3D y menos en la aceleración de la aplicación. Como consecuencia, la API de BitBlt se aceleró en hardware y la mayoría de las demás operaciones de GDI no.

Esto establece la fase para una secuencia de cambios en la forma en que se representa [GDI](/windows/desktop/gdi/windows-gdi) en la pantalla. En la siguiente ilustración se muestra cómo la representación de pantalla de GDI ha cambiado de Windows XP a Windows 7.

![Figura 2: evolución de la representación de la visualización de GDI](images/direct2d-vs-gdi2.png)

También había varios factores adicionales que causaron cambios en el modelo de controlador de [GDI](/windows/desktop/gdi/windows-gdi) , como se explica a continuación.

### <a name="increasing-complexity-and-size-of-display-drivers"></a>Aumento de la complejidad y el tamaño de los controladores de pantalla

los controladores 3D se han vuelto más complejos con el tiempo. Un código más complejo tiende a tener más defectos, lo que hace que sea beneficioso que el controlador exista en modo de usuario, en el que un error de controlador no puede hacer que se reinicie el sistema. Como se puede ver en la figura anterior, el controlador de pantalla se divide en un componente de modo de usuario complejo y un componente de modo kernel más sencillo.

### <a name="difficulty-in-synchronizing-session-and-global-kernel-address-spaces"></a>Dificultad en la sincronización de espacios de direcciones de kernel globales y de sesión

En Windows XP, existe un controlador de pantalla en dos espacios de direcciones diferentes: espacio de sesión y espacio del kernel. Las partes del controlador deben responder a eventos como eventos de administración de energía. Esto se debe sincronizar con el estado del controlador en el espacio de direcciones de la sesión. Esta es una tarea difícil y puede dar lugar a defectos cuando los controladores de pantalla intentan tratar con estos espacios de direcciones distintos.

### <a name="composited-window-management"></a>Administración de ventanas compuestas

El Administrador de ventanas de escritorio (DWM), el administrador de ventanas de composición introducido en Windows 7, representa todas las ventanas en superficies fuera de la pantalla y, a continuación, las compone para que se muestren en la pantalla. Esto requiere que [GDI](/windows/desktop/gdi/windows-gdi) sea capaz de representarse en una superficie que Direct3D representará a continuación para que se muestre. Esto suponía un problema en el modelo de controladores de XP, ya que GDI y Direct3D eran pilas de controladores paralelas.

Como resultado, en Windows Vista, el controlador de visualización DDI de [GDI](/windows/desktop/gdi/windows-gdi) se implementó como el controlador de pantalla canónica (CDC) proporcionado por Microsoft, que representó el contenido GDI en un mapa de bits de memoria del sistema para que se componga en la pantalla.

## <a name="gdi-rendering-in-windows-7"></a>Representación de GDI en Windows 7

El modelo de controladores usado en Windows Vista requiere que cada ventana de [GDI](/windows/desktop/gdi/windows-gdi) esté respaldada por una superficie de memoria de vídeo y una superficie de memoria del sistema. Esto dio lugar a que se usara la memoria del sistema para cada ventana de GDI.

Por esta razón, se cambió de nuevo [GDI](/windows/desktop/gdi/windows-gdi) en Windows 7. . En lugar de representar en una superficie de memoria del sistema, GDI se modificó para representarse en un segmento de memoria de abertura. La memoria de abertura puede actualizarse desde la superficie de memoria de vídeo que contiene el contenido de la ventana. GDI puede volver a representarse en la memoria de abertura y el resultado se puede devolver a la superficie de la ventana. Dado que el segmento de memoria de abertura es direccionable por la GPU, la GPU puede acelerar estas actualizaciones en la superficie de memoria de vídeo. Por ejemplo, la representación de texto, BitBlts, AlphaBlend, TransparentBlt y StretchBlt se aceleran en estos casos.

## <a name="contrasting-direct2d-and-gdi-acceleration-in-windows-7"></a>Comparación de la aceleración de Direct2D y GDI en Windows 7

[Direct2D](./direct2d-portal.md) y [GDI](/windows/desktop/gdi/windows-gdi) son dos API de representación en modo inmediato y tienen aceleración de hardware. Sin embargo, hay una serie de diferencias que permanecen en ambas API.

### <a name="location-of-resources"></a>Ubicación de los recursos

[GDI](/windows/desktop/gdi/windows-gdi) mantiene sus recursos, en determinados mapas de bits, en la memoria del sistema de forma predeterminada. [Direct2D](./direct2d-portal.md) mantiene sus recursos en la memoria de vídeo en el adaptador de pantalla. Cuando GDI necesita actualizar la memoria de vídeo, debe realizarse a través del bus, a menos que el recurso ya esté en el segmento de memoria de la abertura o si la operación se puede expresar directamente. En cambio, Direct2D puede traducir simplemente sus primitivas a primitivos de Direct3D porque los recursos ya están en la memoria de vídeo.

### <a name="rendering-method"></a>Método de representación

Con el fin de mantener la compatibilidad, [GDI](/windows/desktop/gdi/windows-gdi) realiza una gran parte de su representación para la abertura de memoria mediante la CPU. En cambio, [Direct2D](./direct2d-portal.md) traduce sus llamadas de API en primitivas de Direct3D y operaciones de dibujo. A continuación, el resultado se representa en la GPU. Parte de la representación de GDI? s se realiza en la GPU cuando la memoria de la abertura se copia en la superficie de memoria de vídeo que representa la ventana de GDI.

### <a name="scalability"></a>Escalabilidad

Las llamadas de representación de [Direct2D](./direct2d-portal.md)son secuencias de comandos independientes a la GPU. Cada fábrica de Direct2D representa un dispositivo Direct3D diferente. [GDI](/windows/desktop/gdi/windows-gdi) utiliza una secuencia de comandos para todas las aplicaciones del sistema. El método de GDI puede producir una acumulación de la sobrecarga de contexto de representación de CPU y GPU.

### <a name="location"></a>Location

[Direct2D](./direct2d-portal.md) funciona completamente en modo de usuario, incluido el controlador Direct3D en modo usuario y el tiempo de ejecución de Direct3D. Esto ayuda a evitar los bloqueos del sistema causados por defectos de código en el kernel. Sin embargo, [GDI](/windows/desktop/gdi/windows-gdi)tiene la mayor parte de su funcionalidad en el espacio de sesión en modo kernel, con su superficie de API en modo de usuario.

### <a name="availability-of-hardware-acceleration"></a>Disponibilidad de aceleración de hardware

[GDI](/windows/desktop/gdi/windows-gdi) es un hardware acelerado en Windows XP y acelerado en Windows 7 cuando se está ejecutando el administrador de ventanas de escritorio y se está usando un controlador WDDM 1,1. [Direct2D](./direct2d-portal.md) es el hardware acelerado en casi cualquier controlador WDDM y si DWM está en uso o no. En vista, GDI siempre se representará en la CPU.

### <a name="presentation-model"></a>Modelo de presentación

Cuando Windows se diseñó por primera vez, no había memoria suficiente para permitir que cada ventana se almacenara en su propio mapa de bits. Como resultado, [GDI](/windows/desktop/gdi/windows-gdi) siempre se representa lógicamente directamente en la pantalla, con varias regiones de recorte aplicadas para asegurarse de que una aplicación no se representó fuera de su ventana. En el modelo de [Direct2D](./direct2d-portal.md) , una aplicación se representa en un búfer de reserva y el resultado se muestra cuando la aplicación finaliza el dibujo. Esto permite a Direct2D administrar escenarios de animación de forma mucho más fluida que GDI.

## <a name="conclusion"></a>Conclusión

El código [GDI](/windows/desktop/gdi/windows-gdi) existente seguirá funcionando bien en Windows 7. Sin embargo, al escribir un nuevo código de representación de gráficos, se debe tener en cuenta [Direct2D](./direct2d-portal.md) , ya que aprovecha las GPU modernas.

 

 