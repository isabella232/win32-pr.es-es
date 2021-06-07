---
title: Interacción
description: La interacción es la variedad de formas en que los usuarios interactúan con la aplicación, como la función táctil, el teclado, el mouse, entre otras. Use estas directrices para crear experiencias intuitivas y distintivas optimizadas para la función táctil, pero que funcionen de forma coherente en todos los dispositivos de entrada.
ms.assetid: 1509c885-f4dc-4cf9-86a3-cc6754d3b4a0
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 869034e8d7cc8b9d7023e1511482dae203c14b49
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524179"
---
# <a name="interaction"></a>Interacción

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

La interacción es la variedad de formas en que los usuarios interactúan con la aplicación, como la función táctil, el teclado, el mouse, entre otras. Use estas directrices para crear experiencias intuitivas y distintivas optimizadas para la función táctil, pero que funcionen de forma coherente en todos los dispositivos de entrada.

## <a name="design-for-a-touch-first-experience"></a>Diseño para una experiencia táctil

Ante todo, diseña tu aplicación teniendo en mente que el principal método de entrada de los usuarios será táctil. Si usa los controles de plataforma, la compatibilidad con touchpad, mouse y pen/stylus no requiere programación adicional, ya que Windows proporciona esto de forma gratuita.

Pero ten presente que una interfaz de usuario optimizada para entrada táctil no es siempre mejor que una interfaz de usuario tradicional. Ambos proporcionan ventajas y desventajas exclusivas de la tecnología y la aplicación. En el paso a una interfaz de usuario táctil, es importante comprender las diferencias principales entre la entrada táctil (incluido el touchpad), el lápiz/lápiz, el mouse y la entrada de teclado. No tome propiedades y comportamientos conocidos del dispositivo de entrada por concedidos, ya que la función táctil en Windows 8 hace más que simplemente emular esa funcionalidad.

Como pronto descubrirá, la entrada táctil requiere un enfoque diferente para el diseño de la interfaz de usuario.

**Compara los requisitos de la interacción táctil**

En esta tabla se muestran algunas de las diferencias entre los dispositivos de entrada que debe tener en cuenta al diseñar aplicaciones de la Tienda Windows optimizadas para toques.



| Factor          | Interacciones táctiles   | Interacciones con mouse, teclado, pluma/lápiz | Panel táctil  |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| **Precisión**<br/>        | El área de contacto de la punta de un dedo es mayor que la de una sola coordenada x-y, lo que aumenta las probabilidades de activación no intencional de comandos.<br/>                                                               | El mouse y la pluma/lápiz suministran una coordenada x-y precisa.<br/>                                                                                                                                                                                                                                            | Es igual al mouse.<br/>                           |
|                                 | La forma del área de contacto cambia durante el movimiento. <br/>                                                                                                                                       | Los movimientos de mouse y los trazos de la pluma/lápiz suministran coordenadas x-y precisas. El foco del teclado es explícito.<br/>                                                                                                                                                                                                   | Es igual al mouse.<br/>                           |
|                                 | No hay cursor de mouse para ayudar con la selección del destino.<br/>                                                                                                                                                    | El cursor del mouse, el cursor de la pluma/lápiz y el foco del teclado ayudan a seleccionar el destino.<br/>                                                                                                                                                                                                                   | Es igual al mouse.<br/>                           |
| **Anatomía humana**<br/>    | Los movimientos de los dedos no son precisos, ya que es difícil realizar un movimiento en línea recta con uno o más dedos. Esto se debe a la curvatura de las articulaciones de la mano y a la cantidad de articulaciones involucradas en el movimiento.<br/> | Es más fácil ejecutar un movimiento en línea recta con mouse o pluma/lápiz porque la mano que los controla recorre una distancia física menor que el cursor en la pantalla.<br/>                                                                                                                    | Es igual al mouse.<br/>                           |
|                                 | Puede ser difícil llegar a algunas áreas de la superficie táctil de un dispositivo de pantalla debido a la posición de los dedos y la sujeción del dispositivo por parte del usuario.<br/>                                                                | El mouse y la pluma o el lápiz pueden llegar a cualquier parte de la pantalla. El teclado permite acceder a cualquier control con el orden de tabulación. <br/>                                                                                                                                                                 | La posición de los dedos y la empuñadura pueden ser un problema.<br/> |
|                                 | Puede ocurrir que los objetos queden ocultos por la punta de uno o más dedos o la mano del usuario. Esto se conoce como oclusión.<br/>                                                                                                   | Los dispositivos de entrada indirecta no provocan oclusión.<br/>                                                                                                                                                                                                                                                       | Es igual al mouse.<br/>                           |
| **Estado de objeto**<br/>     | La interacción táctil emplea un modelo de dos estados: la superficie táctil de un dispositivo de pantalla se toca (activado) o no se toca (desactivado). No existe un estado de movimiento que pueda desencadenar una respuesta visual adicional.<br/>                         | El mouse, la pluma/lápiz y el teclado exponen un modelo de tres estados: arriba (desactivado), abajo (activado) y movimiento (foco).<br/> Al mantener el puntero sobre un elemento, permite que el usuario explore y aprenda mediante informaciones sobre herramientas asociadas con elementos de la interfaz de usuario. Los efectos de foco y mantener el puntero pueden transmitir qué objetos son interactivos y también ayudar a seleccionar el destino. <br/> | Es igual al mouse.<br/>                           |
| **Interacción enriquecida**<br/> | Admite multitoque: múltiples puntos de entrada (puntas de los dedos) en una superficie táctil.<br/>                                                                                                                          | Admite un punto único de entrada.<br/>                                                                                                                                                                                                                                                                       | Es igual a la entrada táctil.<br/>                           |
|                                 | Admite manipulación directa de objetos por medio de gestos como pulsar, arrastrar, deslizar, reducir y girar.<br/>                                                                                  | No admite manipulación directa porque el mouse, la pluma o el lápiz y el teclado son dispositivos de entrada indirecta.<br/>                                                                                                                                                                                                    | Es igual al mouse.<br/>                           |



 

**Note**

La entrada indirecta tiene la ventaja de más de 25 años de perfeccionamiento. Algunas funciones, como la información sobre herramientas desencadenada al mantener el mouse sobre un elemento, se diseñaron para explorar la interfaz de usuario específicamente con entrada de panel táctil, mouse, pluma o lápiz y teclado. Funciones de UI como esta se han rediseñado para lograr la experiencia completa que reporta la entrada táctil, sin poner en riesgo la experiencia de usuario de estos otros dispositivos.

Aquí se proporcionan algunas directrices generales de interacción del usuario y se tratan las directrices específicas del dispositivo en estos temas.

-   [Tocar](/windows/desktop/uxguide/inter-touch)
-   [Mouse](/windows/desktop/uxguide/inter-mouse)
-   [Lápiz](/windows/desktop/uxguide/inter-pen)
-   [Teclado](/windows/desktop/uxguide/inter-keyboard)
-   [Accesibilidad](/windows/desktop/uxguide/inter-accessibility)

## <a name="visuals-for-feedback"></a>Objetos visuales para comentarios

Los comentarios visuales adecuados durante las interacciones con la aplicación ayudan a los usuarios a reconocer, aprender y adaptarse a cómo la aplicación interpreta sus interacciones y los comentarios de Windows Visual pueden indicar interacciones correctas, retransmitir el estado del sistema, mejorar la sensación de control, reducir errores, ayudar a los usuarios a comprender el sistema y el dispositivo de entrada y fomentar la interacción.

La información visual es esencial cuando el usuario usa la entrada táctil para llevar a cabo actividades que requieren exactitud y precisión en lo que respecta a ubicación. Muestra información siempre que se detecte entrada táctil para ayudar al usuario a entender cualquier regla personalizada de selección de destinos que defina la aplicación y los controles correspondientes.

## <a name="optimize-for-accuracy"></a>Optimización para la precisión

La entrada táctil implica todo el área de contacto del dedo. Esta geometría de contacto se usa para determinar el objeto de destino más probable. Ajuste el tamaño de los controles para garantizar una interfaz de usuario cómoda con objetos y controles de destino fáciles y seguros.

Tamaño, espacio y posición de los controles para ayudar a eliminar la oclusión de los dedos y las manos, donde la interacción del usuario en sí oculta la interfaz de usuario.

Coloque los menús, los elementos emergentes y la información sobre herramientas sobre el área de contacto siempre que sea posible.

## <a name="constrain-for-confidence"></a>Restricción para la confianza

Evite o minimice las interacciones desordenada mediante restricciones de interfaz de usuario.

-   Los puntos de ajuste pueden facilitar la detenerse en las ubicaciones deseadas. Los puntos de acoplamiento especifican paradas lógicas en el contenido de tu aplicación. Desde el punto de vista cognitivo, los puntos de ajuste actúan como mecanismo de paginación para el usuario y minimizan la molestia de un deslizamiento excesivo, un deslizamiento o una rotación. Con ellos, puede controlar la entrada de usuario imprecisa y asegurarse de que se muestra un subconjunto específico de contenido o información clave.
-   "raíles" direccionales que resaltan el eje de movimiento (vertical u horizontal).

## <a name="avoid-timed-interactions"></a>Evitar interacciones con tiempo

Las interacciones no deben distinguirse temporalmente. La misma interacción debe tener el mismo resultado, independientemente del tiempo que se haya tardado en realizarla. Las activaciones temporales introducen retrasos obligatorios para los usuarios y reducen la naturaleza envolvente de la manipulación directa, así como la percepción de la respuesta del sistema.

Para determinar qué comando se ejecutará, las interacciones temporales suelen depender de umbrales invisibles, como el tiempo, la distancia o la velocidad. Las interacciones con tiempo no tienen comentarios visuales hasta que el sistema realiza la acción y los usuarios deben alcanzar umbrales arbitrarios e invisibles para lograr un resultado. La información visual instantánea durante las interacciones hace que los usuarios se sientan más comprometidos, seguros de si mismos y con el control.

Las interacciones que afectan directamente a los objetos y mimetizan las interacciones de la vida real son más intuitivas y fáciles de detectar y recordar. No dependen de interacciones oscuras o abstractas.

**Nota:** Una excepción a esto es que se usan interacciones con tiempo específicas para ayudar en el aprendizaje y la exploración (por ejemplo, mantener presionado). El uso de descripciones adecuadas e indicaciones visuales tiene un gran efecto en el uso de interacciones avanzadas.

