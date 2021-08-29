---
title: Superficie de composición
description: En este tema se describen los tipos de superficies que admite Microsoft DirectComposition.
ms.assetid: E19B4F0E-1CFA-4E93-BB6A-BFB701BC72CA
keywords:
- superficie de composición
- Superficie lógica de DirectComposition
- Superficie virtual de DirectComposition
- actualizar una superficie lógica
- superficie lógica, actualización
- recortar una superficie virtual
- superficie virtual, recorte
- recortar superficie virtual
- redimensionar una superficie virtual
- surace virtual, redimensionamiento
- cambiar el tamaño de la superficie virtual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc7fd2ac653fe46ea4530a39e5dad364e312845b6950a2051b39896f7fbb1e61
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787955"
---
# <a name="composition-surface"></a>Superficie de composición

> [!NOTE]
> Para las aplicaciones de Windows 10, se recomienda usar Windows.UI.Composition API en lugar de DirectComposition. Para obtener más información, [consulte Modernización de la aplicación de escritorio mediante la capa visual](/windows/uwp/composition/visual-layer-in-desktop-apps).

En este tema se describen los tipos de superficies que admite Microsoft DirectComposition.

-   [Superficie lógica de DirectComposition](#directcomposition-logical-surface)
    -   [Actualización de una superficie lógica](#updating-a-logical-surface)
    -   [Suspender actualizaciones en una superficie lógica](#suspending-updates-to-a-logical-surface)
    -   [Reanudación de actualizaciones en una superficie lógica](#resuming-updates-to-a-logical-surface)
    -   [Finalización de actualizaciones en una superficie lógica](#suspending-updates-to-a-logical-surface)
    -   [Ejemplo de uso de una superficie lógica](#example-of-using-a-logical-surface)
-   [Superficie virtual de DirectComposition](#directcomposition-virtual-surface)
    -   [Redimensionamiento de una superficie virtual](#resizing-a-virtual-surface)
    -   [Recorte de una superficie virtual](#trimming-a-virtual-surface)
-   [Temas relacionados](#related-topics)

## <a name="directcomposition-logical-surface"></a>Superficie lógica de DirectComposition

DirectComposition expone el objeto [**IDCompositionSurface**](/windows/win32/api/dcomp/nn-dcomp-idcompositionsurface) para representar una superficie de composición lógica. DirectComposition expone las API que puede usar para crear, actualizar y eliminar estas superficies lógicas. Cada superficie se puede asociar a uno o varios objetos visuales. Una aplicación es responsable de administrar la duración de las superficies lógicas.

### <a name="updating-a-logical-surface"></a>Actualización de una superficie lógica

Una aplicación puede actualizar una superficie lógica llamando a [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) y especificando el tamaño y el desplazamiento del rectángulo en la superficie lógica que la aplicación quiere actualizar. DirectComposition asigna un rectángulo del tamaño especificado y, a continuación, devuelve la superficie y el desplazamiento correspondiente que la aplicación necesita dibujar o actualizar. Los límites del rectángulo de actualización están enlazados por el tamaño de la superficie. Por ejemplo, el rectángulo de actualización de una superficie de 40 por 100 píxeles puede ser hasta (0,0,40,100). Además, la región actualizable se aplica mediante un rectángulo de protección. Dado que solo puede haber un rectángulo de protección a la vez, solo se puede actualizar una superficie lógica a la vez. **BeginDraw** devuelve un código de error si no se ha llamado a [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) o [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) después de una llamada anterior a **BeginDraw.** Una aplicación puede agregar una llamada confirmada a **BeginDraw** a un lote, pero no se aplica hasta que se llama a **EndDraw** y se confirma.

### <a name="suspending-updates-to-a-logical-surface"></a>Suspender actualizaciones en una superficie lógica

Una aplicación que necesita actualizar diferentes superficies puede llamar a [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) en la actualización actual y, a continuación, llamar a [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) para comenzar una nueva actualización. Microsoft DirectComposition permite varias actualizaciones, pero solo una puede estar activa a la vez. Esto significa que debe llamar a **SuspendDraw** o [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) en una superficie antes de llamar a **BeginDraw** en la siguiente. A **diferencia de EndDraw,** un lote confirmado puede contener una superficie que está en estado **SuspendDraw,** pero estas actualizaciones no se mostrarán en la pantalla hasta que se llame a **EndDraw.**

### <a name="resuming-updates-to-a-logical-surface"></a>Reanudación de actualizaciones en una superficie lógica

Una aplicación puede reanudar una actualización de una superficie que se encuentra en un estado [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) llamando a [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw). Solo se puede llamar a este método en una superficie suspendida.

### <a name="ending-updates-to-a-logical-surface"></a>Finalización de actualizaciones en una superficie lógica

Llamar [**a EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) y [**Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) es la única manera de ver los cambios de actualización de mapa de bits en la pantalla. Cada llamada a **EndDraw** debe tener una llamada correspondiente a [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) para quitar el rectángulo de protección. La superficie lógica conserva todas las actualizaciones hasta que se **llama** a Commit. También puede llamar a **EndDraw en una** superficie que esté en estado [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) porque **EndDraw** es un resume/end implícito. Después de llamar a **EndDraw**, el contenido actualizado se presenta en la pantalla y se descarta para que la memoria de la actualización se pueda reutilizar para una actualización posterior.

### <a name="example-of-using-a-logical-surface"></a>Ejemplo de uso de una superficie lógica

En el ejemplo siguiente se describen los pasos que una aplicación realizaría si creara un árbol visual que constase de dos objetos visuales y, a continuación, necesita actualizar regiones específicas de las dos superficies lógicas asociadas a los objetos visuales:

1.  Cree un dispositivo DirectComposition.
2.  Cree el árbol visual que consta de un nodo raíz y los objetos visuales 1 y 2.
3.  Cree superficies lógicas 1 y 2.
4.  Llame [**a SetContent**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setcontent) para asociar una superficie lógica a los objetos visuales 1 y 2.
5.  Llame [**a BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) en un sub rectángulo de la superficie lógica 1.
6.  Actualice la superficie en el desplazamiento devuelto por DirectComposition.
7.  Pasos opcionales:
    1.  Llame [**a SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) en la superficie lógica 1.
    2.  Llame [**a BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) en la subcodificación de la superficie lógica 2.
    3.  Actualice la superficie en el desplazamiento devuelto por DirectComposition.
    4.  Llame [**a EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) en la superficie lógica 2.
    5.  Llame [**a ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) en la superficie lógica 1.
8.  Actualice la superficie en el desplazamiento devuelto por DirectComposition.
9.  Llame [**a EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) en la superficie lógica 1.
10. Llame a [**Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit).

## <a name="directcomposition-virtual-surface"></a>Superficie virtual de DirectComposition

DirectComposition expone la interfaz [**IDCompositionVirtualSurface**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvirtualsurface) para representar una superficie virtual, que es una colección de superficies lógicas (mosaicos) organizadas en una cuadrícula fija con mosaicos de un tamaño fijo. La aplicación especifica el tamaño de la textura virtual en el momento de la creación. El tamaño establece los límites de la superficie virtual. La superficie se puede asociar a uno o varios objetos visuales.

Cuando se inicializa una superficie virtual, no cuenta con el respaldo de asignaciones reales. En otras palabras, no contiene ningún bit. DirectComposition asigna iconos (es decir, objetos de superficie de composición) después de que la aplicación empiece a actualizar la superficie. La aplicación actualiza la superficie virtual llamando a [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) y especificando la región de interés con respecto a las coordenadas de la superficie virtual. A continuación, DirectComposition asigna los iconos necesarios para contener la actualización y devuelve la superficie de composición y el desplazamiento que se actualizarán.

Al igual que con las superficies lógicas, puede llamar a [**BeginDraw,**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) [**SuspendDraw,**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) y [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) en una superficie virtual. Además, DirectComposition expone métodos que puede usar para cambiar el tamaño y recortar una superficie virtual existente.

### <a name="resizing-a-virtual-surface"></a>Redimensionamiento de una superficie virtual

El [**método Resize**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvirtualsurface-resize) cambia los límites de la superficie virtual, lo que significa que las nuevas actualizaciones o asignaciones deben estar dentro de los límites establecidos por el nuevo tamaño. Una aplicación usa **Resize** para decir a DirectComposition que una región determinada de la superficie virtual ya no es necesaria y se puede reclamar. Si **resize** reduce la superficie virtual, la aplicación ya no podrá actualizar las regiones fuera de los nuevos límites.

En la ilustración siguiente se muestra una superficie virtual de 3 por 3 que se ha cambiado de tamaño a 2 por 2. La región roja representa los iconos que se descartan como parte de la operación de cambio de tamaño y DirectComposition reclama la memoria. Después del cambio de tamaño, la aplicación no puede realizar actualizaciones en la región roja sin cambiar el tamaño de la superficie virtual de nuevo.

![redimensionar una superficie virtual ](images/resize-virtual-surface.png)

La operación de cambio de tamaño entra en vigor inmediatamente. DirectComposition no espera a que la aplicación llame a [**Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) para realizar las actualizaciones de cambio de tamaño. Por ejemplo, suponga que una aplicación realiza la siguiente secuencia de llamadas.


```
pVirtualSurface->Resize(0, 0);
pVirtualSurface->Resize(INT_MAX, INT_MAX);
pDevice->Commit();
```



En este ejemplo, la aplicación pierde todo el contenido en el primer cambio de tamaño. El segundo cambio de tamaño no tiene ningún efecto aunque se llamó antes de [**Confirmar**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit). En este caso, no se muestra nada en la pantalla.

### <a name="trimming-a-virtual-surface"></a>Recorte de una superficie virtual

El [**método Trim**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvirtualsurface-trim) identifica la región de la superficie virtual que necesita la aplicación. No cambia el tamaño de los límites de la superficie virtual, pero sí le dice a DirectComposition qué superficies lógicas deben asignarse actualmente.

En la siguiente ilustración, el cuadrado verde es la ventanilla de la aplicación. Inicialmente, la aplicación se representa en los seis primeros iconos (azul) de la superficie virtual (gris claro) que se encuentran en la ventanilla. A medida que se desplaza la página representada por la superficie virtual, la aplicación debe representar los últimos seis iconos. La aplicación llama [**a Trim**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvirtualsurface-trim) para indicar que la región definida por los últimos seis iconos es donde está el contenido y el resto no es necesario en este momento. Después, DirectComposition puede optar por reciclar las superficies lógicas que representaron originalmente los seis primeros iconos (gris oscuro).

![recortar una superficie virtual](images/trim-virtual-surface.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de DirectComposition](directcomposition-concepts.md)
</dt> </dl>

 

 