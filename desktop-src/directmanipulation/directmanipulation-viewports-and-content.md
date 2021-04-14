---
description: La manipulación directa usa las ventanillas, el contenido y los contactos para describir los elementos interactivos de la interfaz de usuario.
ms.assetid: 1564F6F2-844F-4392-9EB5-AA46059D514C
title: Ventanillas y contenido
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 9cda367067ea860ce6a42a16e81d38393937276a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104565382"
---
# <a name="viewports-and-content"></a>Ventanillas y contenido

La [manipulación directa](direct-manipulation-portal.md) usa las *ventanillas*, el *contenido* y los *contactos* para describir los elementos interactivos de la interfaz de usuario.

- [Configurar una ventanilla](#configuring-a-viewport)
- [Puntos de acoplamiento y límites](#snap-points-and-boundaries)
- [Desplazamiento de punto de acoplamiento y escenarios RTL](#snap-point-offset-and-rtl-scenarios)
- [Comportamientos](#behaviors)
- [Sistema de coordenadas](#coordinate-system)
- [Transformaciones](#transforms)
- [Estado de la ventanilla](#viewport-state)
- [Temas relacionados](#related-topics)

Una *ventanilla* es una región de una ventana que puede recibir y procesar la entrada de interacciones del usuario. La ventanilla representa la región del contenido que el usuario final puede visualizar en un momento dado (también denominado clip de contenido). La ventanilla tiene varias funciones:

- Administra el estado de interacción (por ejemplo, cuando el contenido está listo para ser manipulado, cuando el contenido se está manipulando, cuando el contenido está en la animación de inercia) y asigna la entrada a las transformaciones de salida.
- Incluye contenido que se mueve en respuesta a la interacción del usuario. Puede tratarse de un elemento HTML div (Scrolling), una lista de selección panorámica (la pantalla Inicio de Windows 8) o el menú emergente de un control Select.

Una ventanilla se crea llamando a [**CreateViewport**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-createviewport). Se pueden crear varias ventanillas en una sola ventana para generar una experiencia de interfaz de usuario enriquecida.

El *contenido* representa el elemento que se transforma en respuesta a una interacción. En otras palabras, el contenido es lo que mueve o escala a medida que el usuario gira o se reduce. Hay dos tipos de contenido:

- El *contenido principal* es el único elemento intrínseco dentro de una ventanilla que responde a las manipulaciones de entrada y a la inercia. El contenido principal se crea al mismo tiempo que la ventanilla y no se puede agregar ni quitar de una ventanilla. Puede personalizar el comportamiento del contenido principal mediante puntos de acoplamiento (se describe más adelante).
- El *contenido secundario* se mueve en relación con el movimiento del contenido principal. El contenido secundario se crea por separado de la ventanilla y se puede Agregar o quitar de una ventanilla. Todas las transformaciones de contenido secundario se calculan en función de la transformación del contenido principal. Se pueden aplicar reglas específicas para cambiar el modo en que se calcula la transformación en función del propósito previsto del elemento, identificado por su CLSID durante la creación.

En este diagrama que muestra antes y después de una pan, se ha usado un solo contacto para desplazar el contenido principal. Aunque el usuario no interactúa directamente con el indicador de movimiento panorámico (contenido secundario), el contenido secundario se mueve a medida que se desplaza el contenido principal. Esto proporciona indicaciones visuales sobre hasta qué punto se ha desplazado el usuario.

![diagrama que muestra antes o después de una panorámica](images/dm-art-2.png)

## <a name="configuring-a-viewport"></a>Configurar una ventanilla

Después de crear la ventanilla. Configure su comportamiento mediante una *configuración de interacción*. La configuración de interacción especifica qué manipulaciones, como la panorámica, se admiten.

La *panorámica* cambia la posición del contenido a lo largo del eje horizontal o vertical, o bien de forma panorámica del usuario. Al configurar la traducción en ambos ejes, el contenido se mueve libremente en cualquier dirección.

Para restringir el movimiento de contenido, configure *raíles*, normalmente en el eje horizontal y vertical. Si la interacción de un usuario se encuentra principalmente en un solo eje (representado por las regiones azules en el diagrama siguiente), la panorámica se convierte en *raíla* y el contenido solo se mueve a lo largo del eje de raíles. Si el usuario se ha desplazado y actualmente está entrenando y realiza una segunda panorámica mientras el contenido está en la inercia, el nuevo pan seguirá siendo entreno.

![diagrama que muestra el contenido dentro de una ventanilla en una pan con raíles](images/dm-art-3.png)

Ejemplo: una ventanilla está configurada para el movimiento panorámico horizontal y vertical. En el primer fotograma, el contacto se vuelve inactivo. En el segundo, se inicia una panorámica vertical y el contacto está bloqueado en el raíl vertical. Por último, una vez que la panorámica está entrenándose, solo se usa el componente vertical de una pan diagonal para mover el contenido.

Si el usuario se desplaza diagonalmente de forma que no se encuentran en las regiones de detección de raíles (las regiones blancas), la panorámica no se *Guía* y el contenido se mueve libremente en ambos ejes.

![diagrama que muestra el movimiento de contenido en una pan no entrened](images/dm-art-4.png)

El zoom cambia el factor de escala del contenido a medida que un usuario se *reduce* o se expande. El punto en el que se escala el contenido (denominado Centro de zoom) es el centro de los contactos. Si ha establecido la alineación horizontal o vertical, el centro de zoom cambia a conservar alineación.

![diagrama que muestra el zoom del contenido con una alineación especificada](images/dm-art-5.png)

Puede invalidar este comportamiento mediante la especificación del centro de desbloqueo, que establece el centro de zoom en el centro de los contactos.

![diagrama que muestra el zoom del contenido con el centro de zoom desbloqueado](images/dm-art-6.png)

La *inercia* es la desaceleración gradual de una manipulación, tanto el movimiento panorámico como el zoom, después de que todos los contactos se hayan levantado (en el caso de la función táctil) o después de la entrada del teclado o del mouse (por ejemplo, al hacer clic en una barra de desplazamiento o al presionar las teclas de dirección). Cuando un usuario manipula el contenido, la manipulación no se detiene inmediatamente después de que se levante el contacto. En su lugar, el contenido continúa en la dirección y la velocidad actuales, lo que ralentiza gradualmente a una parada.

## <a name="snap-points-and-boundaries"></a>Puntos de acoplamiento y límites

Una animación de inercia tiene lugar una vez finalizada la manipulación como resultado de que un dedo se levante de la pantalla (en el caso de Touch) o como resultado de una acción del teclado o del mouse (como teclas de dirección, página arriba/abajo, desplazamiento de la rueda del mouse, etc.).

Hay dos fragmentos de información que definen la animación de inercia:

- El punto de REST de la animación: la posición final final del componente de transformación concreto.
- Duración de la animación, curva, velocidad: se determinan por el tipo del punto de descanso.

La animación de inercia se ve afectada por los puntos de acoplamiento y los límites. Los límites especifican los puntos de descanso máximo y mínimo para el contenido. Si el contenido alcanza un límite durante la inercia, se aplicará una animación de límite. Los puntos de acoplamiento se definen en el contenido principal para modificar el punto de REST y modificar la curva de animación de inercia en sí.

Los puntos de acoplamiento se definen con [**SetSnapInterval**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapinterval) cuando el contenido se espacia regularmente o con [**SetSnapPoints**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnappoints) cuando el contenido se espacia de forma desigual. A continuación se muestra un ejemplo de puntos de acoplamiento:

![diagrama que muestra cómo los puntos de acoplamiento establecidos en el contenido afectan al movimiento panorámico](images/dm-snappoint-states-3.png)

En el diagrama, hay un fragmento de contenido con una serie de bloques de subcontenido: elementos de noticias en una aplicación de tipo lector de noticias o elementos en una vista de cuadrícula. La intención es ajustar el borde izquierdo de un elemento en el borde izquierdo de la ventanilla una vez finalizada la inercia.

Hay dos grupos de tipos de punto de acoplamiento:

- *Opcional frente a obligatorio*: un punto de acoplamiento opcional solo ajusta la animación de inercia si el punto de REST de inercia está cerca del punto de acoplamiento. Un punto de ajuste obligatorio siempre ajusta la animación de inercia a un punto de acoplamiento especificado.
- *Único frente A varios*: un tipo de punto de ajuste múltiple permite que el contenido se mueva más allá de los puntos de ajuste antes de llegar a un resto en un punto de acoplamiento cerca de su punto de descanso natural. Un tipo de punto de ajuste único elige el punto de acoplamiento siguiente como punto de descanso para la animación de inercia.

En el diagrama siguiente se muestra cómo los tipos de punto de acoplamiento modifican la posición de REST de la animación de inercia.

![diagrama que muestra cómo interactúan la inercia y los puntos de acoplamiento](images/dm-snappoint-states-1.png)

En este diagrama, el punto de inicio de la inercia se etiqueta como "Inicio" y la posición final de la inercia natural en la ausencia de puntos de ajuste como "fin". Las líneas verticales marcan los distintos puntos de acoplamiento. En esta tabla se describe cómo afectará cada tipo de punto de ajuste a la posición final de la animación.

| Tipo de punto         | Descripción                                                                                |
|--------------------|--------------------------------------------------------------------------------------------|
| Único obligatorio   | Se elige el punto de acoplamiento P1 porque es el primer punto de ajuste en la dirección de la inercia     |
| Múltiplo obligatorio | Se elige el punto de ajuste P2 porque es más cercano al punto final en la dirección de la inercia. |
| Opcional Single    | Se elige el punto de acoplamiento P1 porque es el primer punto de ajuste encontrado durante la inercia      |
| Múltiplos opcionales  | Se elige el punto de acoplamiento P2 porque está cerca del punto final natural                           |

## <a name="snap-point-offset-and-rtl-scenarios"></a>Desplazamiento de punto de acoplamiento y escenarios RTL

![diagrama que muestra el uso de punto de acoplamiento RTL](images/dm-snappoint-states-2.png)

Puede aplicar el desplazamiento de punto de acoplamiento y el sistema de coordenadas mediante la API de [**SetSnapCoordinate**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate) , que desplaza todos los puntos de acoplamiento o los intervalos de ajuste mediante el sistema de coordenadas/coordenadas especificado.

El sistema de coordenadas es muy útil en escenarios de RTL, donde desea describir los puntos de acoplamiento del borde izquierdo del contenido en dirección inversa. En el diagrama anterior, [**SetSnapCoordinate**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate) se usa con la marca **\_ \_ reflejada** **DIRECTMANIPULATION \_ Motion \_ TRANSLATEX** y DIRECTMANIPULATION, que desplaza automáticamente los puntos de acoplamiento del borde izquierdo del contenido y los proporciona en orden de derecha a izquierda: S1 está en 0px, S2 está en 50px (y así sucesivamente). Cualquier desplazamiento establecido mediante **SetSnapCoordinate** se desplazará más allá de este borde izquierdo del contenido automáticamente, incluido el factor de escala correcto.

Casi siempre usará [**SetSnapCoordinate**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate) con el parámetro *Origin* establecido para evitar la configuración de puntos de acoplamiento fuera del área de contenido.

Por ejemplo, si la ventanilla es 200 x 200 y el contenido es 1000x200, y la interfaz es RTL, la ventanilla tendrá el borde izquierdo en x = 800 cuando la ventanilla se presente por primera vez. Llame a [**SetSnapCoordinate**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate) con `SetSnapCoordinate(DIRECTMANIPULATION_MOTION_TRANSLATEX, DIRECTMANIPULATION_COORDINATE_MIRRORED, 1000.0)` para especificar que los puntos de ajuste deben calcularse de derecha a izquierda orden a partir del borde derecho del contenido.

## <a name="behaviors"></a>Comportamientos

Un *comportamiento* es un objeto que se puede adjuntar a una ventanilla para modificar el modo en que la [manipulación directa](direct-manipulation-portal.md) controla la transformación de salida del contenido principal o secundario de una ventanilla. Un objeto de comportamiento puede afectar a uno o varios aspectos de una manipulación, como la forma en que se procesa la entrada o el modo en que se aplica la animación de inercia. Por ejemplo, un comportamiento de desplazamiento automático afecta a la animación de inercia mediante la realización de una animación de desplazamiento hacia un extremo del contenido principal. Un comportamiento de configuración entre diapositivas afecta al procesamiento de entradas de manipulación directa que detecta cuándo se realiza una acción de deslizamiento transversal.

Un objeto de comportamiento se crea llamando a [**CreateBehavior**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager2-createbehavior), se agrega a una ventanilla y, a continuación, su comportamiento se configura de forma asincrónica. Al quitar el comportamiento de la ventanilla, se quitan sus efectos.

## <a name="coordinate-system"></a>Sistema de coordenadas

Hay tres sistemas de coordenadas principales empleados por la [manipulación directa](direct-manipulation-portal.md):

- Sistema de coordenadas de cliente: describe el rectángulo de la ventana de cliente. Las unidades están en píxeles.
- Sistema de coordenadas de la ventanilla: describe el rectángulo de una región en el cliente que puede procesar la entrada. Las unidades están definidas por la aplicación (mediante [**SetViewportRect**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setviewportrect)).
- Sistema de coordenadas de contenido: describe el rectángulo o el tamaño del contenido principal. Las unidades están definidas por la aplicación (mediante [**SetContentRect**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-setcontentrect)).

En el caso de los tres sistemas, las coordenadas se definen en relación con su origen superior izquierdo y se incrementan positivamente hacia la derecha y hacia abajo. Estos sistemas de coordenadas se ilustran en el diagrama siguiente. El usuario final solo puede visualizar o manipular la sección del contenido dentro del rectángulo de la ventanilla.

![diagrama que muestra cómo interactúan las coordenadas de contenido, cliente y ventanilla](images/dm-art-7.png)

## <a name="transforms"></a>Transformaciones

La [manipulación directa](direct-manipulation-portal.md) mantiene varias transformaciones diferentes que contribuyen al resultado general mostrado.

- *Transformación de contenido* : transformación inicial calculada mediante la [manipulación directa](direct-manipulation-portal.md) basada en una manipulación o una inercia. Captura los efectos de los puntos de acoplamiento, los raíles, los overpan predeterminados (manipulación), las animaciones de sobrebote predeterminadas (inercia) y ZoomToRect.
- *Transformación de salida* : la transformación final de visual o de salida. Es la combinación del contenido y las transformaciones de sincronización.
- *Sync Transform* : se calcula cuando se llama a [**SyncContentTransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-synccontenttransform). Ayuda a la [manipulación directa](direct-manipulation-portal.md) a aplicar una nueva transformación de contenido proporcionada por la aplicación a la vez que se mantiene la transformación de salida existente.
- *Display Transform* : aplicado por la aplicación como parte del procesamiento posterior. Consulte [**SyncDisplayTransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-syncdisplaytransform) para obtener más información.

Dado que la transformación de salida está pensada para desplazar una superficie visualmente en la pantalla, la [manipulación directa](direct-manipulation-portal.md) realiza el redondeo necesario en los componentes de transformación de salida, de modo que el texto y otro contenido siempre se representan o se componen en un límite de píxeles entero. El mecanismo de redondeo depende de varios factores, incluida la velocidad del movimiento y la presencia de Escritorio remoto. El mecanismo de redondeo para el contenido secundario coincide con el del contenido principal, teniendo en cuenta la diferencia en el movimiento entre ambos. Los clientes de [**GetOutputTransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-getoutputtransform) no deben depender del mecanismo de redondeo exacto de la transformación de salida, a medida que se aplican varios factores.

> [!Note]
>
> Esto significa que los componentes de una transformación de contenido pueden no ser integrales y pueden contener desplazamientos de subpíxeles. Se recomienda a los clientes que usen la [manipulación directa](direct-manipulation-portal.md) usar el [**GetOutputTransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-getoutputtransform) para calcular la transformación visual correcta que se aplicará al contenido al usar el modo de actualización manual. Al usar el modo de actualización automática con el compositor integrado, la manipulación directa aplica automáticamente esta transformación en nombre del cliente. Esta transformación se genera mediante la manipulación directa para garantizar resultados visualmente agradables al crear la salida visual.

## <a name="viewport-state"></a>Estado de la ventanilla

A medida que se procesa la entrada, la ventanilla administra el estado de interacción y la asignación de entrada a las transformaciones de salida. Compruebe el estado de interacción de la ventanilla llamando a [**getStatus**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-getstatus).

![diagrama que muestra los Estados de interacción de directmanipulation](images/dm-states-diagram.png)

- Compilando: la ventanilla se está creando y aún no puede procesar la entrada. Para procesar la entrada, llame a [**IDirectManipulationViewport:: enable**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-enable). Si no se llama a **enable** , la ventanilla pasa al Estado deshabilitado.

    > [!Note]  
    > Este es el estado inicial de la interacción.

- Habilitado: la ventanilla está lista para procesar la entrada. Cuando se produce un contacto (se llama a [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) ) y se detecta una manipulación, la ventanilla cambia a Running (en ejecución).

- En ejecución: la ventanilla está procesando actualmente la entrada y la actualización de contenido. Cuando se eleva el contacto, la ventanilla realiza la transición a la inercia, si está configurado.

- Inercia: el contenido se mueve en una animación de inercia. Una vez completada la inercia, la ventanilla pasará a estar lista. Si se ha establecido la deshabilitación automática en la ventanilla, pasará de la inercia a lista y, a continuación, a deshabilitada.

- Listo: la ventanilla está lista para procesar la entrada. Cuando se produce un contacto (se llama a [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) ) y se detecta una manipulación, la ventanilla cambia a Running (en ejecución).

- Suspended: la ventanilla se puede suspender cuando su entrada se ha promocionado a un elemento primario en la cadena de [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) . Esto se describe con más detalle en [varias ventanillas: pruebas de posicionamiento y jerarquía de ventanilla](directmanipulation-multiple-vieports.md).

- Deshabilitado: la ventanilla no procesará la entrada ni realizará devoluciones de llamada. Una ventanilla se puede deshabilitar de varios Estados llamando a [**IDirectManipulationViewport::D**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-disable)deshabilitar. Si se ha establecido deshabilitar automáticamente en la ventanilla, se realizará la transición automáticamente a deshabilitado después de que se procese una manipulación. Para volver a habilitar una ventanilla deshabilitada, llame a [**IDirectManipulationViewport:: enable**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-enable).

## <a name="related-topics"></a>Temas relacionados

[Varias ventanillas: prueba de posicionamiento y jerarquía de ventanilla](directmanipulation-multiple-vieports.md), [**ActivateConfiguration**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-activateconfiguration), [**GetOutputTransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-getoutputtransform), [**SyncDisplayTransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-syncdisplaytransform)
