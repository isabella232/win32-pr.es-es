---
title: Superficie de composición
description: En este tema se describen los tipos de tipos de superficies que admite Microsoft DirectComposition.
ms.assetid: E19B4F0E-1CFA-4E93-BB6A-BFB701BC72CA
keywords:
- superficie de composición
- Superficie lógica de DirectComposition
- DirectComposition superficie virtual
- actualizar una superficie lógica
- superficie lógica, actualizar
- recorte de una superficie virtual
- superficie virtual, recorte
- cortar superficie virtual
- cambiar el tamaño de una superficie virtual
- Surace virtuales, cambio de tamaño
- cambiar el tamaño de la superficie virtual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f4bd30bfbd1de91444b7076184db597cd7a8c82
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077929"
---
# <a name="composition-surface"></a>Superficie de composición

> [!NOTE]
> En el caso de las aplicaciones de Windows 10, se recomienda usar las API de Windows. UI. Composition en lugar de DirectComposition. Para obtener más información, consulte [modernice su aplicación de escritorio con el nivel de objetos visuales](/windows/uwp/composition/visual-layer-in-desktop-apps).

En este tema se describen los tipos de tipos de superficies que admite Microsoft DirectComposition.

-   [Superficie lógica de DirectComposition](#directcomposition-logical-surface)
    -   [Actualizar una superficie lógica](#updating-a-logical-surface)
    -   [Suspender actualizaciones en una superficie lógica](#suspending-updates-to-a-logical-surface)
    -   [Reanudar actualizaciones en una superficie lógica](#resuming-updates-to-a-logical-surface)
    -   [Finalizar actualizaciones en una superficie lógica](#suspending-updates-to-a-logical-surface)
    -   [Ejemplo de uso de una superficie lógica](#example-of-using-a-logical-surface)
-   [DirectComposition superficie virtual](#directcomposition-virtual-surface)
    -   [Cambiar el tamaño de una superficie virtual](#resizing-a-virtual-surface)
    -   [Recorte de una superficie virtual](#trimming-a-virtual-surface)
-   [Temas relacionados](#related-topics)

## <a name="directcomposition-logical-surface"></a>Superficie lógica de DirectComposition

DirectComposition expone el objeto [**IDCompositionSurface**](/windows/win32/api/dcomp/nn-dcomp-idcompositionsurface) para representar una superficie lógica de composición. DirectComposition expone las API que puede usar para crear, actualizar y eliminar estas superficies lógicas. Cada superficie puede estar asociada a uno o varios objetos visuales. Una aplicación es responsable de administrar la duración de las superficies lógicas.

### <a name="updating-a-logical-surface"></a>Actualizar una superficie lógica

Una aplicación puede actualizar una superficie lógica llamando a [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) y especificando el tamaño y el desplazamiento del rectángulo en la superficie lógica que la aplicación quiere actualizar. DirectComposition asigna un rectángulo del tamaño especificado y, a continuación, devuelve la superficie y el desplazamiento correspondiente que la aplicación necesita para dibujar o actualizar. Los límites del rectángulo de actualización están enlazados por el tamaño de la superficie. Por ejemplo, el rectángulo de actualización de una superficie de píxel 40 por 100 puede ser de hasta (0,0, 40100). Además, la región actualizable se aplica mediante un rectángulo de protección. Dado que solo puede haber un rectángulo de protección a la vez, solo se puede actualizar una superficie lógica a la vez. **BeginDraw** devuelve un código de error si no se ha llamado a [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) o [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) después de una llamada anterior a **BeginDraw**. Una aplicación puede Agregar una llamada confirmada a **BeginDraw** a un lote, pero no surte efecto hasta que se llama a **EndDraw** y se confirma.

### <a name="suspending-updates-to-a-logical-surface"></a>Suspender actualizaciones en una superficie lógica

Una aplicación que necesita actualizar superficies diferentes puede llamar a [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) en la actualización actual y, después, llamar a [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) para iniciar una nueva actualización. Microsoft DirectComposition permite varias actualizaciones, pero solo una puede estar activa cada vez. Esto significa que debe llamar a **SuspendDraw** o [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) en una superficie antes de llamar a **BeginDraw** en el siguiente. A diferencia de **EndDraw**, un lote confirmado puede contener una superficie que está en un estado **SuspendDraw** , pero dichas actualizaciones no se mostrarán en la pantalla hasta que se llame a **EndDraw** .

### <a name="resuming-updates-to-a-logical-surface"></a>Reanudar actualizaciones en una superficie lógica

Una aplicación puede reanudar una actualización en una superficie que se encuentra en estado [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) llamando a [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw). Solo se puede llamar a este método en una superficie suspendida.

### <a name="ending-updates-to-a-logical-surface"></a>Finalizar actualizaciones en una superficie lógica

Llamar a [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) y [**commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) es la única manera de ver los cambios en la actualización de mapas de bits en la pantalla. Cada llamada a **EndDraw** debe tener una llamada correspondiente a [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) para quitar el rectángulo de protección. La superficie lógica conserva todas las actualizaciones hasta que se llama a **commit** . También puede llamar a **EndDraw** en una superficie que esté en el estado [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) porque **EndDraw** es un resume/end implícito. Después de llamar a **EndDraw**, el contenido actualizado se presenta en la pantalla y se descarta para que se pueda volver a usar la memoria de la actualización para una actualización posterior.

### <a name="example-of-using-a-logical-surface"></a>Ejemplo de uso de una superficie lógica

En el ejemplo siguiente se describen los pasos que realizará una aplicación si creó un árbol visual que consta de dos objetos visuales y, a continuación, necesitaba actualizar regiones específicas de las dos superficies lógicas asociadas a los objetos visuales:

1.  Cree un dispositivo DirectComposition.
2.  Cree el árbol visual que se compone de un nodo raíz y los objetos visuales 1 y 2.
3.  Cree las superficies lógicas 1 y 2.
4.  Llame a [**SetContent**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setcontent) para asociar una superficie lógica con los objetos visuales 1 y 2.
5.  Llame a [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) en un subrectángulo de la superficie lógica 1.
6.  Actualice la superficie en el desplazamiento devuelto por DirectComposition.
7.  Pasos opcionales:
    1.  Llame a [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) en la superficie lógica 1.
    2.  Llame a [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) en el subrectángulo de la superficie lógica 2.
    3.  Actualice la superficie en el desplazamiento devuelto por DirectComposition.
    4.  Llame a [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) en la superficie lógica 2.
    5.  Llame a [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) en la superficie lógica 1.
8.  Actualice la superficie en el desplazamiento devuelto por DirectComposition.
9.  Llame a [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) en la superficie lógica 1.
10. Llamar a [**commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit).

## <a name="directcomposition-virtual-surface"></a>DirectComposition superficie virtual

DirectComposition expone la interfaz [**IDCompositionVirtualSurface**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvirtualsurface) para representar una superficie virtual, que es una colección de superficies lógicas (mosaicos) organizadas en una cuadrícula fija con mosaicos de tamaño fijo. La aplicación especifica el tamaño de la textura virtual en el momento de la creación. El tamaño establece los límites para la superficie virtual. La superficie puede estar asociada a uno o varios objetos visuales.

Cuando se inicializa una superficie virtual, no está respaldada por asignaciones reales. En otras palabras, no contiene ningún bit. DirectComposition asigna mosaicos (es decir, objetos de superficie de composición) una vez que la aplicación empieza a actualizar la superficie. La aplicación actualiza la superficie virtual mediante una llamada a [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) y especifica la región de interés con respecto a las coordenadas de la superficie virtual. A continuación, DirectComposition asigna los mosaicos necesarios para almacenar la actualización y devuelve la superficie de composición y el desplazamiento que se van a actualizar.

Al igual que con las superficies lógicas, puede llamar a [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw), [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw), [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) y [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) en una superficie virtual. Además, DirectComposition expone métodos que se pueden usar para cambiar el tamaño y recortar una superficie virtual existente.

### <a name="resizing-a-virtual-surface"></a>Cambiar el tamaño de una superficie virtual

El método de cambio de [**tamaño**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvirtualsurface-resize) cambia los límites de la superficie virtual, lo que significa que las nuevas actualizaciones o asignaciones deben estar en los límites establecidos por el nuevo tamaño. Una aplicación utiliza el **ajuste de tamaño** para indicar a DirectComposition que una región determinada de la superficie virtual ya no es necesaria y se puede reclamar. Si el **ajuste de tamaño** reduce la superficie virtual, la aplicación ya no puede actualizar las regiones fuera de los límites nuevos.

En la ilustración siguiente se muestra una superficie virtual de 3 por 3 cuyo tamaño se ha cambiado a 2 por 2. La región roja representa los mosaicos que se descartan como parte de la operación de cambiar el tamaño y DirectComposition recupera la memoria. Después del cambio de tamaño, la aplicación no puede realizar actualizaciones en la región roja sin cambiar el tamaño de la superficie virtual de nuevo.

![cambiar el tamaño de una superficie virtual ](images/resize-virtual-surface.png)

La operación de cambiar el tamaño surte efecto inmediatamente. DirectComposition no espera a que la aplicación llame a [**commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) para realizar las actualizaciones de tamaño. Por ejemplo, supongamos que una aplicación realiza la siguiente secuencia de llamadas.


```
pVirtualSurface->Resize(0, 0);
pVirtualSurface->Resize(INT_MAX, INT_MAX);
pDevice->Commit();
```



En este ejemplo, la aplicación pierde todo el contenido en el primer ajuste de tamaño. El segundo cambio de tamaño no tiene ningún efecto a pesar de que se llamó antes de la [**confirmación**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit). En este caso, no se muestra nada en la pantalla.

### <a name="trimming-a-virtual-surface"></a>Recorte de una superficie virtual

El método [**Trim**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvirtualsurface-trim) identifica la región de la superficie virtual que necesita la aplicación. No cambia el tamaño de los límites de la superficie virtual, pero indica a DirectComposition qué superficies lógicas hay que asignar actualmente.

En la ilustración siguiente, el cuadrado verde es la ventanilla de la aplicación. La aplicación se representa inicialmente en los seis primeros mosaicos (azul) de la superficie virtual (gris claro) que se encuentran en la ventanilla. A medida que la página representada por la superficie virtual se desplaza, la aplicación debe representar los últimos seis mosaicos. La aplicación llama a [**Trim**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvirtualsurface-trim) para indicar que la región definida por los seis últimos iconos es donde el contenido es y el resto no es necesario en este momento. A continuación, DirectComposition puede optar por reciclar las superficies lógicas que originalmente representaban los seis primeros mosaicos (gris oscuro).

![recorte de una superficie virtual](images/trim-virtual-surface.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de DirectComposition](directcomposition-concepts.md)
</dt> </dl>

 

 