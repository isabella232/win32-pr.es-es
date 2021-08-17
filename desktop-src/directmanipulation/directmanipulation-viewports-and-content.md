---
description: La manipulación directa usa ventanillas, contenido y contactos para describir los elementos interactivos de la interfaz de usuario.
ms.assetid: 1564F6F2-844F-4392-9EB5-AA46059D514C
title: Ventanillas y contenido
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: a103df916e5880380064250d05806169ff4187e6a8be0b22d2dd72d92343f38f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118787122"
---
# <a name="viewports-and-content"></a>Ventanillas y contenido

[La manipulación directa](direct-manipulation-portal.md) *usa ventanillas,* *contenido* y *contactos* para describir los elementos interactivos de la interfaz de usuario.

- [Configuración de una ventanilla](#configuring-a-viewport)
- [Puntos de ajuste y límites](#snap-points-and-boundaries)
- [Escenarios de desplazamiento de punto de ajuste y RTL](#snap-point-offset-and-rtl-scenarios)
- [Comportamientos](#behaviors)
- [Sistema de coordenadas](#coordinate-system)
- [Transformaciones](#transforms)
- [Estado de la ventanilla](#viewport-state)
- [Temas relacionados](#related-topics)

Una *ventanilla* es una región dentro de una ventana que puede recibir y procesar la entrada de las interacciones del usuario. La ventanilla representa la región del contenido que puede ver el usuario final en un momento dado (también denominado clip de contenido). La ventanilla tiene varias funciones:

- Administra el estado de interacción (por ejemplo, cuando el contenido está listo para manipularse, cuando el contenido está en proceso de manipulación, cuando el contenido está en animación de inercia) y asigna la entrada a las transformaciones de salida.
- Contiene contenido que se mueve en respuesta a la interacción del usuario. Podría ser un elemento div HTML (desplazamiento), una lista con capacidad de desplazamiento (el Windows 8 pantalla Inicio) o el menú emergente de un control select.

Se crea una ventanilla mediante una llamada [**a CreateViewport**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-createviewport). Se pueden crear varias ventanillas en una sola ventana para generar una experiencia de interfaz de usuario completa.

*El* contenido representa el elemento que se transforma en respuesta a una interacción. En otras palabras, el contenido es lo que se mueve o escala a medida que el usuario se desplaza o se acerca. Hay dos tipos de contenido:

- *El contenido principal* es el único elemento intrínseco dentro de una ventanilla que responde a manipulaciones de entrada e inercia. El contenido principal se crea al mismo tiempo que la ventanilla y no se puede agregar ni quitar de una ventanilla. Puede personalizar el comportamiento del contenido principal mediante puntos de instantánea (que se analizarán más adelante).
- *El contenido secundario* se mueve en relación con el movimiento del contenido principal. El contenido secundario se crea por separado desde la ventanilla y se puede agregar o quitar de una ventanilla. Todas las transformaciones de contenido secundarias se calculan en función de la transformación del contenido principal. Se pueden aplicar reglas específicas para cambiar cómo se calcula la transformación en función del propósito previsto del elemento, identificado por su CLSID durante la creación.

En este diagrama que muestra antes y después de una panorámica, se ha usado un único contacto para desplazarse por el contenido principal. Aunque el usuario no interactúa directamente con el indicador de movimiento panorámico (contenido secundario), el contenido secundario se mueve a medida que se desplaza el contenido principal. Esto proporciona indicaciones visuales sobre hasta qué punto el usuario ha pasado desatendido.

![diagrama que muestra antes y después de un panorámica](images/dm-art-2.png)

## <a name="configuring-a-viewport"></a>Configuración de una ventanilla

Después de crear la ventanilla. configure su comportamiento mediante una configuración *de interacción*. La configuración de interacción especifica qué manipulaciones, como el movimiento panorámico, se admiten.

*El movimiento panorámico* cambia la posición del contenido a lo largo del eje horizontal o vertical, o ambos, a medida que el usuario se desplazará. Al configurar la traducción en ambos ejes, el contenido se mueve libremente en cualquier dirección.

Para restringir el movimiento del contenido, configure *los raíles*, normalmente en el eje horizontal y vertical. Si la interacción de un usuario se encuentra principalmente a lo largo de un  único eje (representado por las regiones azules en el diagrama siguiente), el panorámica se vuelve en raíl y el contenido solo se mueve a lo largo del eje de raíl. Si el usuario se ha panorámicado y está actualmente en el raíl y realiza una segunda panorámica mientras el contenido está en inercia, la nueva panorámica sigue siendo de raíl.

![diagrama que muestra el contenido dentro de una ventanilla en un panorámica con raíl](images/dm-art-3.png)

Ejemplo: se configura una ventanilla para el movimiento panorámico horizontal y vertical. En el primer fotograma, el contacto aparece. En el segundo, se inicia una panorámica vertical y el contacto está bloqueado en el raíl vertical. Por último, una vez que el panorámica está en el raíl, solo se usa el componente vertical de una panorámica diagonal para mover el contenido.

Si el usuario se desplaza diagonalmente de forma que no se encuentra en las regiones de detección de raíles (las regiones blancas), la panorámica se descarrila y el contenido se moverá libremente en ambos ejes. 

![diagrama que muestra el contenido que se mueve en una panorámica sin barreras](images/dm-art-4.png)

*El zoom* cambia el factor de escala del contenido a medida que un usuario se reduce o se ajusta. El punto alrededor del cual se escala el contenido (denominado centro de zoom) está en el centro de los contactos. Si ha establecido la alineación horizontal o vertical, el centro de zoom cambia para conservar la alineación.

![diagrama que muestra el zoom del contenido con una alineación especificada](images/dm-art-5.png)

Puede invalidar este comportamiento especificando el centro de desbloqueo, que establece el centro de zoom en el centro de los contactos.

![diagrama que muestra el zoom del contenido con el centro de zoom desbloqueado](images/dm-art-6.png)

 La inercia es la disminución gradual de una manipulación, tanto de movimiento panorámico como de zoom, después de que se hayan elevado todos los contactos (en el caso de la entrada táctil) o después de la entrada del teclado o del mouse (como hacer clic en una barra de desplazamiento o presionar las teclas de dirección). Cuando un usuario manipula el contenido, la manipulación no se detiene inmediatamente después de que se eleva el contacto. En su lugar, el contenido continúa en la dirección y la velocidad actuales, con lo que se ralentiza gradualmente hasta que se detiene.

## <a name="snap-points-and-boundaries"></a>Puntos de ajuste y límites

Una animación de inercia tiene lugar después de que finaliza la manipulación como resultado de que se quita un dedo de la pantalla (en el caso de la entrada táctil) o como resultado de una acción de teclado o mouse (como teclas de dirección, subir y bajar, desplazarse por la rueda del mouse, etc.).

Hay dos fragmentos de información que definen la animación de inercia:

- El punto de resto de la animación: la posición final final del componente de transformación determinado.
- Duración de la animación, curva y velocidad: se determinan por el tipo del punto de resto.

La animación de inercia se ve afectada por los puntos de ajuste y los límites. Los límites especifican los puntos de reposo máximo y mínimo para el contenido. Si el contenido alcanza un límite durante la inercia, se aplicará una animación de límites. Los puntos de ajuste se definen en el contenido principal para modificar el punto de resto y modificar la propia curva de animación de inercia.

Los puntos de ajuste se definen [**con SetSnapInterval**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapinterval) cuando el contenido se espaciado periódicamente o [**con SetSnapPoints**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnappoints) cuando el contenido está espaciado de forma desigual. Este es un ejemplo de puntos de instantánea:

![diagrama que muestra cómo afectan los puntos de ajuste establecidos en el contenido al movimiento panorámico](images/dm-snappoint-states-3.png)

En el diagrama, hay un fragmento de contenido con una serie de bloques de subconsono: elementos de noticias en una aplicación de tipo lector de noticias o elementos en una vista de cuadrícula. La intención es ajustar el borde izquierdo de un elemento en el borde izquierdo de la ventanilla una vez finalizada la inercia.

Hay dos grupos de tipos de punto de instantánea:

- *Opcional frente a Obligatorio:* un punto de instantánea opcional ajusta la animación de inercia solo si el punto de reposo de inercia está cerca del punto de instantánea. Un punto de instantánea obligatorio siempre ajusta la animación de inercia a un punto de instantánea especificado.
- Uno frente a *varios:* un tipo de punto de instantánea múltiple permite que el contenido pase de varios puntos de instantánea antes de llegar a un punto de instantánea cercano a su punto de reposo natural. Un único tipo de punto de instantánea elige el siguiente punto de instantánea más cercano como punto de reposo para la animación de inercia.

En el diagrama siguiente se muestra cómo los tipos de punto de ajuste modifican la posición restante de la animación de inercia.

![diagrama que muestra cómo interactúan los puntos de inercia y de ajuste](images/dm-snappoint-states-1.png)

En este diagrama, el punto de inicio de inercia se etiqueta como "Inicio" y la posición final de inercia natural en ausencia de puntos de ajuste como "Final". Las líneas verticales marcan los distintos puntos de ajuste. En esta tabla se describe cómo cada tipo de punto de instantánea afectará a la posición final de la animación.

| Tipo de punto         | Descripción                                                                                |
|--------------------|--------------------------------------------------------------------------------------------|
| Single obligatorio   | Se elige el punto de ajuste P1 porque es el primer punto de ajuste en la dirección de la inercia     |
| Varios obligatorios | Se elige el punto de ajuste P2 porque está más cerca del punto final en la dirección de la inercia |
| Opcional único    | Se elige el punto de ajuste P1 porque es el primer punto de instantánea encontrado durante la inercia.      |
| Múltiplo opcional  | Se elige el punto de ajuste P2 porque está cerca del punto final natural.                           |

## <a name="snap-point-offset-and-rtl-scenarios"></a>Escenarios de desplazamiento de punto de ajuste y RTL

![diagrama que muestra el uso del punto de instantánea rtl](images/dm-snappoint-states-2.png)

El desplazamiento del punto de instantánea y el sistema de coordenadas se aplican mediante la API [**SetSnapCoordinate,**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate) que desplaza todos los puntos de ajuste o intervalos de ajuste mediante el sistema de desplazamiento y coordenadas especificado.

El sistema de coordenadas es muy útil en escenarios rtl, donde se quieren describir los puntos de ajuste del borde izquierdo del contenido en la dirección inversa. En el diagrama anterior, [**SetSnapCoordinate**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate) se usa con la marca **DIRECTMANIPULATION \_ MOTION \_ TRANSLATEX** y **DIRECTMANIPULATION \_ COORDINATE \_ MIRRORED,** que desplaza automáticamente los puntos de ajuste desde el borde izquierdo del contenido y los proporciona en orden de derecha a izquierda: S1 está en 0px, S2 en 50 px (y así sucesivamente). Cualquier conjunto de desplazamiento que use **SetSnapCoordinate** desplazará aún más desde este borde izquierdo del contenido automáticamente, incluido el factor de escala correcto.

Casi siempre usará [**SetSnapCoordinate**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate) con el parámetro *de* origen establecido para evitar establecer puntos de ajuste fuera del área de contenido.

Por ejemplo, si la ventanilla es 200 x 200 y el contenido es 1000 x 200 y la interfaz es RTL, la ventanilla tendrá su borde izquierdo en x=800 cuando se presente por primera vez la ventanilla. Llame [**a SetSnapCoordinate**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate) con para especificar que los puntos de ajuste se deben calcular de derecha a izquierda a partir del borde `SetSnapCoordinate(DIRECTMANIPULATION_MOTION_TRANSLATEX, DIRECTMANIPULATION_COORDINATE_MIRRORED, 1000.0)` DERECHO del contenido.

## <a name="behaviors"></a>Comportamientos

Un *comportamiento* es un objeto que se puede adjuntar [](direct-manipulation-portal.md) a una ventanilla para modificar cómo la manipulación directa controla la transformación de salida del contenido principal o secundario de una ventanilla. Un objeto de comportamiento puede afectar a uno o varios aspectos de una manipulación, como cómo se procesa la entrada o cómo se aplica la animación de inercia. Por ejemplo, un comportamiento de desplazamiento automático afecta a la animación de inercia realizando una animación de desplazamiento hacia un extremo del contenido principal. Un comportamiento de configuración de diapositivas cruzadas afecta al procesamiento de entrada de manipulación directa, que detecta cuándo se realiza una acción de deslizamiento cruzado.

Un objeto de comportamiento se crea mediante una llamada a [**CreateBehavior**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager2-createbehavior), que se agrega a una ventanilla y, a continuación, su comportamiento se configura de forma asincrónica. Al quitar el comportamiento de la ventanilla, se quitan sus efectos.

## <a name="coordinate-system"></a>Sistema de coordenadas

Hay tres sistemas de coordenadas principales empleados por [la manipulación directa:](direct-manipulation-portal.md)

- Sistema de coordenadas de cliente: describe el rectángulo de la ventana de cliente. Las unidades están en píxeles.
- Sistema de coordenadas de ventanilla: describe el rectángulo de una región dentro del cliente que puede procesar la entrada. Las unidades están definidas por la aplicación (mediante [**SetViewportRect**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setviewportrect)).
- Sistema de coordenadas de contenido: describe el rectángulo o el tamaño del contenido principal. Las unidades están definidas por la aplicación (mediante [**SetContentRect**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-setcontentrect)).

Para los tres sistemas, las coordenadas se definen en relación con su origen superior izquierdo respectivo y son positivas a la derecha y hacia abajo. Estos sistemas de coordenadas se ilustran en el diagrama siguiente. El usuario final solo puede ver o manipular la sección del contenido dentro del rectángulo de la ventanilla.

![diagrama que muestra cómo interactúan las coordenadas de contenido, cliente y ventanilla](images/dm-art-7.png)

## <a name="transforms"></a>Transformaciones

[La manipulación](direct-manipulation-portal.md) directa mantiene varias transformaciones diferentes que contribuyen a la salida global mostrada.

- *Transformación de contenido:* la transformación inicial calculada por [manipulación directa](direct-manipulation-portal.md) basada en una manipulación o inercia. Captura los efectos de los puntos de ajuste, la barandilla, el sobrepantalla predeterminado (manipulación), la sobrecuencia predeterminada (inercia) y las animaciones ZoomToRect.
- *Transformación de salida:* el objeto visual final o la transformación de salida. Es la combinación del contenido, así como de las transformaciones de sincronización.
- *Transformación de sincronización:* se calcula cuando se llama [**a SyncContentTransform.**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-synccontenttransform) Ayuda a [la manipulación directa](direct-manipulation-portal.md) a aplicar una nueva transformación de contenido proporcionada por la aplicación mientras se mantiene también la transformación de salida existente.
- *Mostrar transformación:* aplicada por la aplicación como parte del procesamiento posterior. Consulte [**SyncDisplayTransform para**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-syncdisplaytransform) obtener más detalles.

Dado que la transformación de salida está diseñada para desplazar una superficie visualmente en la [pantalla,](direct-manipulation-portal.md) la manipulación directa realiza el redondeo necesario en los componentes de transformación de salida para que el texto y otro contenido siempre se representen o se componen en un límite de píxeles entero. El mecanismo de redondeo depende de varios factores, incluida la velocidad del movimiento y la presencia de Escritorio remoto. El mecanismo de redondeo del contenido secundario coincide con el del contenido principal, teniendo en cuenta la diferencia en el movimiento entre los dos. Los clientes [**de GetOutputTransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-getoutputtransform) no deben depender del mecanismo de redondeo exacto de la transformación de salida, ya que varios factores la afectan.

> [!Note]
>
> Esto significa que los componentes de una transformación de contenido pueden no ser enteros y pueden contener desplazamientos de subpíxeles. Se recomienda [a los](direct-manipulation-portal.md) clientes que usan manipulación directa usar [**GetOutputTransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-getoutputtransform) para calcular la transformación visual correcta que se aplicará en el contenido al usar el modo de actualización manual. Cuando se usa el modo de actualización automática mediante el compositor integrado, la manipulación directa aplica automáticamente esta transformación en nombre del cliente. Esta transformación se genera mediante la manipulación directa para garantizar resultados visualmente satisfactorios al crear la salida visual.

## <a name="viewport-state"></a>Estado de la ventanilla

A medida que se procesa la entrada, la ventanilla administra el estado de interacción y la asignación de la entrada a las transformaciones de salida. Compruebe el estado de interacción de la ventanilla mediante una [**llamada a GetStatus**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-getstatus).

![diagrama que muestra los estados de interacción de directmanipulation](images/dm-states-diagram.png)

- Building: la ventanilla se está creando y aún no puede procesar la entrada. Para procesar la entrada, llame a [**IDirectManipulationViewport::Enable**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-enable). Si **no** se llama a Habilitar, la ventanilla pasa al estado Deshabilitado.

    > [!Note]  
    > Este es el estado inicial de la interacción.

- Habilitado: la ventanilla está lista para procesar la entrada. Cuando un contacto baja (se llama a [**SetContact)**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) y se detecta una manipulación, la ventanilla pasa a En ejecución.

- En ejecución: la ventanilla está procesando actualmente la entrada y actualizando el contenido. Cuando se eleva el contacto, la ventanilla pasa a Inercia, si está configurada.

- Inercia: el contenido se mueve en una animación de inercia. Una vez completada la inercia, la ventanilla pasará a Listo. Si se ha establecido la deshabilitación automática en la ventanilla, pasará de Inercia a Listo y, a continuación, a Deshabilitado.

- Listo: la ventanilla está lista para procesar la entrada. Cuando un contacto baja (se llama a [**SetContact)**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) y se detecta una manipulación, la ventanilla pasa a En ejecución.

- Suspendido: la ventanilla puede convertirse en Suspendida cuando su entrada se ha promocionado a un elemento primario en la [**cadena SetContact.**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) Esto se describe con más detalle en Varias [ventanillas: pruebas de acceso y jerarquía de ventanillas.](directmanipulation-multiple-vieports.md)

- Deshabilitado: la ventanilla no procesará la entrada ni realizará devoluciones de llamada. Una ventanilla se puede deshabilitar desde varios estados mediante una llamada a [**IDirectManipulationViewport::D isable**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-disable). Si se ha establecido la deshabilitación automática en la ventanilla, pasará automáticamente a Deshabilitado después de procesar una manipulación. Para volver a habilitar una ventanilla deshabilitada, llame a [**IDirectManipulationViewport::Enable**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-enable).

## <a name="related-topics"></a>Temas relacionados

[Varias ventanillas: pruebas de impacto y jerarquía de](directmanipulation-multiple-vieports.md)ventanilla, [**ActivateConfiguration,**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-activateconfiguration) [**GetOutputTransform,**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-getoutputtransform) [**SyncDisplayTransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-syncdisplaytransform)
