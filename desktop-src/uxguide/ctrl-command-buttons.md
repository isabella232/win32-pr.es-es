---
title: Botones de comandos
description: Con un botón de comando, los usuarios inician una acción inmediata.
ms.assetid: 0e2ff31a-657b-4e4c-afee-2a6bd742f46c
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 32c8c16cef275e1fefe44e579105515d3e61c497
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "103820082"
---
# <a name="command-buttons"></a>Botones de comandos

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

Con un botón de comando, los usuarios inician una acción inmediata.

![captura de pantalla del botón de comando aceptar ](images/ctrl-command-buttons-image1.png)

Botón de comando típico.

El botón de comando predeterminado se invoca cuando los usuarios presionan la tecla entrar. Lo asigna el desarrollador, pero cualquier botón de comando se convierte en el valor predeterminado cuando los usuarios la pestaña.

> [!Note]  
> Las instrucciones relacionadas con el [diseño](vis-layout.md) se presentan en un artículo independiente.

 

## <a name="is-this-the-right-control"></a>¿Es este el control adecuado?

Para decidirte, intenta responder a estas preguntas:

-   **¿Se usa el botón de comando para iniciar una acción inmediata?** Si no es así, usa otro control.
-   **¿Sería un vínculo una opción mejor?** Use un vínculo si:
    -   La acción es desplazarse a otra página, ventana o tema de ayuda. **Excepción**: la navegación del asistente utiliza los botones de comando atrás y siguiente.
    -   El comando se incrusta en un cuerpo de texto.
    -   El comando es de naturaleza secundaria. Es decir, no se relaciona con el propósito principal de la ventana. En este caso, un botón o vínculo de comando ligero sería adecuado.
    -   El comando forma parte de un menú o grupo de vínculos relacionados.
    -   La etiqueta es larga y consta de cinco o más palabras, lo que permite que un botón de comando sea un aspecto extraño.
-   **¿Una combinación de botones de radio y botones de comando genéricos es una opción mejor?** A menudo, los botones de radio se usan junto con los botones de comando genéricos (aceptar, cancelar) en lugar de un conjunto de botones de comando específicos cuando se cumple cualquiera de las siguientes condiciones:
    -   Hay cinco o más acciones posibles.
    -   Los usuarios deben ver información adicional antes de tomar una decisión.
    -   Los usuarios deben interactuar con las opciones (quizás para ver información adicional) antes de tomar una decisión.
    -   Los usuarios ven las opciones como opciones en lugar de comandos diferentes.

        **Correcto:** ![ captura de pantalla del cuadro de diálogo, botones de radio y texto ](images/ctrl-command-buttons-image2.png)

        En este ejemplo, los botones de radio se combinan con los botones aceptar y Cancelar para proporcionar información adicional sobre las opciones.

        **Incorrecto:** ![ captura de pantalla del mensaje con botones de comando ](images/ctrl-command-buttons-image3.png)

        En este ejemplo, los botones de comando solo hacen que sea difícil para los usuarios tomar una decisión informada.

## <a name="design-concepts"></a>Conceptos de diseño

**Usar puntos suspensivos**

Aunque se usan botones de comando para acciones inmediatas, es posible que se necesite más información para realizar la acción. **Indicar un comando que necesita información adicional (incluida la confirmación) agregando un botón de puntos suspensivos al final de la etiqueta del botón**.

![captura de pantalla del botón de comando imprimir con puntos suspensivos ](images/ctrl-command-buttons-image4.png)

En este ejemplo, se imprime... comando muestra un cuadro de diálogo de impresión para recopilar más información.

![captura de pantalla del botón de comando imprimir, sin puntos suspensivos ](images/ctrl-command-buttons-image5.png)

Por el contrario, en este ejemplo, el comando Imprimir imprime una única copia de un documento en la impresora predeterminada sin ninguna interacción adicional del usuario.

**El uso correcto de las elipses es importante para indicar que los usuarios pueden tomar más opciones antes de realizar la acción, o incluso cancelar la acción por completo**. La indicación visual ofrecida por un botón de puntos suspensivos permite a los usuarios explorar el software sin miedo.

**Esto no significa que deba usar puntos suspensivos cada vez que una acción muestre otra ventana** solo cuando se requiera información adicional para realizar la acción. Por lo tanto, **cualquier botón de comando cuyo verbo implícito sea "Mostrar otra ventana" no toma puntos suspensivos**, como con los comandos acerca de, Advanced, Help (o cualquier otro comando que vincule a un tema de ayuda), opciones, propiedades o configuraciones.

Por lo general, se usan puntos suspensivos en las interfaces de usuario para indicar incompletas. Los comandos que muestran otras ventanas no están incompletos, deben mostrar otra ventana y no se necesita información adicional para realizar su acción. Este enfoque elimina la confusión de la pantalla en situaciones en las que los puntos suspensivos tienen poco valor.

**Nota:** Al determinar si un botón de comando necesita puntos suspensivos, no use la necesidad de [elevar los privilegios](winenv-uac.md) como un factor. La elevación no es información necesaria para ejecutar un comando (en su lugar, tiene permiso) y la necesidad de elevar se indica con el escudo de seguridad.

**Si solo hace algo...** Use una etiqueta concisa, específica y autoexplicativa que describa claramente la acción que realiza el botón de comando y use puntos suspensivos cuando corresponda.

## <a name="usage-patterns"></a>Patrones de uso

Los botones de comando tienen varios patrones de uso:



|                                                                                                                                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Botones de comando estándar** Puede usar los botones de comando estándar para iniciar una acción inmediata.<br/>                                                           | ![captura de pantalla del botón de comando estándar (gris) ](images/ctrl-command-buttons-image6.png)<br/> Botón de comando estándar.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Botones de comando predeterminados** El botón de comando predeterminado de una ventana indica el botón de comando que se activará cuando los usuarios presionen la tecla entrar.<br/>       | ![captura de pantalla del botón de comando predeterminado (azul) ](images/ctrl-command-buttons-image7.png)<br/> Botón de comando predeterminado.<br/> Cualquier botón de comando se convierte en el valor predeterminado cuando el usuario le pestaña. Si el foco de entrada está en un control que no es un botón de comando, el botón de comando con el atributo de botón predeterminado se convierte en el valor predeterminado. Solo un botón de comando de una ventana puede ser el valor predeterminado.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Botones de comando ligeros** Un botón de comando ligero es similar a un botón de comando estándar, excepto que el marco de botón solo se muestra al mantener el mouse. <br/> | ![captura de pantalla de uno de los dos botones de impresión seleccionados ](images/ctrl-command-buttons-image8.png)<br/> En este ejemplo, el comando tiene una apariencia muy ligera (similar a un [vínculo](ctrl-links.md)) hasta que el usuario mantiene el mouse sobre el comando, momento en el que se dibuja con un marco de botón.<br/> Puede usar botones de comandos ligeros en situaciones en las que usaría un botón de comando estándar, pero desea evitar mostrar siempre el marco del botón. Los botones de comando ligero son ideales para los comandos que desea subrayar y usar un vínculo no sería adecuado.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **Botones de menú** Use un botón de menú cuando necesite un menú para un conjunto pequeño de comandos relacionados.<br/>                                                                 | ![captura de pantalla del botón de menú Formato y sus comandos ](images/ctrl-command-buttons-image9.png)<br/> Botón de menú con un pequeño conjunto de comandos relacionados.<br/> Use un botón de menú cuando no se desea una barra de menús, como en un cuadro de diálogo, barra de herramientas u otra ventana que no tenga una barra de menús. Un solo triángulo que apunta hacia abajo indica que al hacer clic en el botón se desplegará un menú.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **Botones de expansión** Use un botón de expansión para consolidar un conjunto de variaciones de un comando, especialmente cuando uno de los comandos se usa la mayor parte del tiempo.<br/>          | ![captura de pantalla del botón abrir división sin comandos ](images/ctrl-command-buttons-image10.png)<br/> botón de expansión contraído.<br/> al igual que un botón de menú, un solo triángulo que apunta hacia abajo indica que al hacer clic en la parte más a la derecha del botón se desplegará un menú.<br/> ![captura de pantalla del botón abrir División con comandos ](images/ctrl-command-buttons-image11.png)<br/> botón de expansión desplegable.<br/> en este ejemplo, se usa un botón de expansión para consolidar seis variaciones del comando Open. el comando Open normal se usa la mayoría de las veces, por lo que los usuarios normalmente no necesitan ver los demás comandos. el uso de un botón de expansión guarda una cantidad significativa de espacio de pantalla, a la vez que proporciona opciones eficaces.<br/> a diferencia de un botón de menú, al hacer clic en la parte izquierda del botón, la acción se realiza directamente en la etiqueta. los botones de expansión son eficaces en situaciones en las que es probable que la siguiente acción con una herramienta específica sea la misma que la última acción. en este caso, la etiqueta se cambia a la última acción, como sucede con un selector de colores:<br/> ![captura de pantalla del botón de expansión de relleno sin comandos ](images/ctrl-command-buttons-image12.png)<br/> En este ejemplo, la etiqueta se cambia a la última acción.<br/> |
| **Botones examinar** Use un botón Examinar para mostrar un cuadro de diálogo que ayude a los usuarios a seleccionar un valor válido.<br/>                                                           | los cuadros de diálogo que se inician mediante un botón examinar ayudan a los usuarios a seleccionar archivos, carpetas, equipos, usuarios, colores, etc. Normalmente, se combinan con un control sin restricciones, como un cuadro de texto. normalmente se etiquetan como examinar, otros, o más, y siempre tienen un botón de puntos suspensivos para indicar que se requiere más información. <br/> ![captura de pantalla de un cuadro de texto con el botón examinar ](images/ctrl-command-buttons-image13.png)<br/> un cuadro de texto con un botón examinar.<br/> en el caso de las ventanas que tienen muchos botones de exploración, puede usar una versión corta:<br/> ![captura de pantalla del botón de exploración breve con puntos suspensivos ](images/ctrl-command-buttons-image14.png)<br/> Botón examinar breve.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **Botones de divulgación progresiva** Use un botón de divulgación progresiva para mostrar u ocultar las opciones que se usan con poca frecuencia.<br/>                                            | la ocultación de las opciones que se usan con poca frecuencia hasta que sean necesarias se denomina divulgación progresiva. se usan comillas angulares dobles para indicar una divulgación progresiva y apuntan a la dirección en la que se realiza la revelación u ocultación: <br/> ![captura de pantalla del botón con las flechas ' más ' y derecha ](images/ctrl-command-buttons-image15.png)<br/> después de hacer clic en el botón, la etiqueta cambia para indicar que el siguiente clic tendrá el efecto opuesto:<br/> ![captura de pantalla del botón con las flechas ' menos ' y izquierda ](images/ctrl-command-buttons-image16.png)<br/> Para obtener más información y ejemplos, vea [controles de divulgación progresiva](ctrl-progressive-disclosure-controls.md). <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **Botones de dirección** Use un botón direccional para indicar la dirección en la que se llevará a cabo una acción.<br/>                                               | en este caso, se usa un corchete angular único en lugar de un cheurón doble: <br/> ![captura de pantalla de los botones de flecha derecha e izquierda ](images/ctrl-command-buttons-image17.png)<br/> Un botón direccional indica la dirección de la acción.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="guidelines"></a>Directrices

### <a name="general"></a>General

-   **Muestra un puntero ocupado si el resultado de hacer clic en un botón de comando no es instantáneo.** Sin comentarios, los usuarios pueden suponer que el clic no se ha producido y hacer clic de nuevo.
-   Si el mismo botón de comando aparece en más de una ventana, **intente usar el mismo texto de etiqueta y la misma clave de acceso, y búsquela aproximadamente en el mismo lugar de cada ventana cuando sea práctico.**
-   **En el caso de los botones de comando con etiquetas de texto, use un ancho de botón mínimo y el alto del botón de comando estándar.** Para obtener más información, vea [ajuste de tamaño y espaciado recomendados](#recommended-sizing-and-spacing).
-   En cada ventana, **los botones de comando se convierten en el mismo ancho**. Si eso no es práctico, limite el número de anchos distintos para los botones de comando con etiquetas de texto a dos.
-   Cuando otro control interopera con un botón de comando, como un cuadro de texto con un botón examinar, **denote la relación colocando el botón de comando en uno de los tres lugares:**
    -   A la derecha de y alineado en la parte superior con el otro control.
    -   Debajo y alineado a la izquierda con el otro control.
    -   Centrado verticalmente entre los controles que interoperan (por ejemplo, los botones agregar y quitar entre dos cuadros de lista interoperativos).
-   Si varios botones de comando interoperan con el mismo control, **apilarlos verticalmente a la derecha y alineados en la parte superior con el otro control, o colocarlos horizontalmente alineados a la izquierda bajo el control.**
-   Cuando los botones de comando están subordinados a otros controles, **use la selección de ubicación anterior y deshabilite el botón de comando subordinado hasta que se seleccione el control superior.**
-   **No use botones de comando estrechos, cortos o altos con etiquetas de texto** porque tienden a ser no profesionales. Intente trabajar con el ancho y el alto predeterminados.

**Correcto:** ![ captura de pantalla del botón aceptar de tamaño predeterminado ](images/ctrl-command-buttons-image18.png)

En este ejemplo, el tamaño del botón es estándar y tiene el aspecto profesional.

**Incorrecto:** ![ captura de pantalla del botón de aceptar corto ](images/ctrl-command-buttons-image19.png)

En este ejemplo, el botón es demasiado pequeño.

**Incorrecto:** ![ captura de pantalla de botón aceptar de tamaño grande y cuadrado ](images/ctrl-command-buttons-image20.png)

En este ejemplo, el botón tiene demasiado espacio alrededor de la etiqueta.

-   **Evite combinar etiquetas de texto y gráficos en botones de comando.** La combinación de texto y gráficos suele agregar un desorden visual innecesario y no mejora la comprensión del usuario. Considere la posibilidad de combinar texto y gráficos solo cuando el gráfico ayude en la comprensión, como cuando es un símbolo estándar para el comando o ayuda a los usuarios a visualizar los resultados del comando. En caso contrario, se prefiere el texto, pero se usa texto o gráficos.

**Correcto:** ![ captura de pantalla del comando rotar con flecha curvada ](images/ctrl-command-buttons-image21.png)

En este ejemplo, el gráfico de flecha ayuda a los usuarios a visualizar los resultados del comando.

**Correcto:** ![ captura de pantalla de la barra de direcciones con iconos y texto ](images/ctrl-command-buttons-image22.png)

En este ejemplo, los símbolos estándar se combinan con el texto para facilitar la comprensión.

**Incorrecto:** ![ captura de pantalla del botón con el icono x y cancelar ](images/ctrl-command-buttons-image23.png)

En este ejemplo, el gráfico cancelar no agrega nada al texto.

-   **No use botones de comando para establecer el estado**. En su lugar, use los botones o las casillas de radio. Los botones de comando son solo para iniciar acciones.

### <a name="split-buttons"></a>Botones de expansión

-   **Haga que el comando más probable sea el comportamiento predeterminado**. Si hay más de un comando probable, elija uno que no requiera información adicional.
-   **Si el comando más probable es la última selección de usuario, cambie la etiqueta del botón a la última selección.**
-   **Mostrar el comando predeterminado usando texto en negrita en el menú**. Esto facilita a los usuarios la búsqueda del comando predeterminado, especialmente cuando el comando predeterminado es dinámico o el botón de expansión usa un gráfico en lugar de una etiqueta de texto.

### <a name="default-values"></a>Valores predeterminados

-   Incluya un botón de comando predeterminado en cada cuadro de diálogo. **Seleccione la opción más segura (para evitar la pérdida de datos o el acceso al sistema) y el comando más seguro es el predeterminado**. Si seguridad y seguridad no son factores, seleccione el comando más probable o práctico.
-   **No realice una acción destructiva el botón de comando predeterminado** , a menos que haya una manera fácil de deshacer el comando.

## <a name="recommended-sizing-and-spacing"></a>Ajuste de tamaño y espaciado recomendados

![diagrama de dimensiones de botón en píxeles y DLU ](images/ctrl-command-buttons-image24.png)

Ajuste de tamaño y espaciado recomendados para los botones de comando.

## <a name="labels"></a>Etiquetas

-   Etiquetar cada botón de comando.
-   Si el botón solo tiene una etiqueta gráfica, asigne su propiedad nombre a una etiqueta de texto adecuada. Esto permite a los productos de tecnología de asistencia, como lectores de pantalla, proporcionar a los usuarios información alternativa sobre el gráfico.

    ![captura de pantalla de los botones subir, bajar y copiar ](images/ctrl-command-buttons-image25.png)

    En este ejemplo se muestran los botones gráficos; internamente, estos botones se etiquetan como anterior, siguiente y copiar.

-   En el caso de los botones de exploración breves (con la etiqueta "..."), la etiqueta interna debe examinarse.
-   Asigne una [clave de acceso](glossary.md)única. Para obtener instrucciones, consulte [teclado](inter-keyboard.md).

    **Excepciones:**

    -   No asigne claves de acceso a los botones aceptar y cancelar, ya que entrar es la tecla de acceso del botón predeterminado (que suele ser el botón Aceptar) y ESC es la tecla de acceso para cancelar. Esto hace que las demás claves de acceso sean más fáciles de asignar.
    -   No asigne las claves de acceso a los botones de exploración cortos (etiquetados como "..."), ya que no se pueden asignar de forma única.

-   Prefiere etiquetas específicas sobre las genéricas. Lo ideal es que los usuarios no tengan que leer nada más para entender la etiqueta. Es mucho más probable que los usuarios lean etiquetas de botón de comando que el texto estático.

    -   **Excepción:** No cambie el nombre del botón Cancelar si el significado de la cancelación no es ambiguo. Los usuarios no deben tener que leer todos los botones para determinar qué botón cancela una acción. Sin embargo, cambie el nombre de cancelar si no está claro qué acción se está cancelando, por ejemplo, cuando hay varias acciones pendientes.

    **Aceptable:**

    ![Captura de pantalla que muestra los botones "Aceptar" y "Cancelar".](images/ctrl-command-buttons-image26.png)

    En este ejemplo, aceptar y cancelar son etiquetas aceptables pero no específicas.

    **Manera**

    ![captura de pantalla de los botones grabar CD y cancelar ](images/ctrl-command-buttons-image27.png)

    En este ejemplo, grabar CD es más específico que el correcto.

    **Incorrecto:**

    ![captura de pantalla de los botones grabar CD y no grabar CD ](images/ctrl-command-buttons-image28.png)

    En este ejemplo, se debe usar cancelar en lugar de no grabar CD.

-   Inicie las etiquetas con un verbo imperativo y describa claramente la acción que realiza el botón. No uses puntuación final.
    -   **Excepción:** Las siguientes etiquetas estándar son aceptables sin verbos: avanzado, atrás, detalles, reenviar, menos, más, nuevo, siguiente, no, aceptar, opciones, anterior, propiedades, configuración y sí.
-   Aunque se prefieren etiquetas cortas, use el texto suficiente para explicar el comando lo suficiente. Use un objeto directo (un sustantivo después del verbo) cuando el objeto no sea aparente del contexto. Lo ideal es que los usuarios no tengan que leer nada más para entender la etiqueta.

    **Aceptable:**

    ![captura de pantalla del botón con agregar etiqueta ](images/ctrl-command-buttons-image29.png)

    En este ejemplo, una etiqueta corta es aceptable si su significado en contexto es evidente fácilmente.

    **Mejor:** (si Add no está claro)

    ![captura de pantalla de un botón con la etiqueta agregar elementos ](images/ctrl-command-buttons-image30.png)

    En este ejemplo, agregar un sustantivo al verbo ayuda a la comprensión de los usuarios.

    **Mejor:** (si agregar o agregar elementos no están claros)

    ![captura de pantalla del botón con agregar elementos seleccionados ](images/ctrl-command-buttons-image31.png)

    En este ejemplo, la etiqueta se explica por sí misma.

-   Usar [mayúsculas y minúsculas en el estilo de oraciones](glossary.md). Hacerlo es más adecuado para el [](text-style-tone.md)[tono](https://msdn.microsoft.com/library/windows/desktop/aa974175.aspx) de Windows de tono de Windows y el uso de frases cortas para los botones de comando.
    -   **Excepción:** En el caso de las aplicaciones heredadas, puede utilizar [el uso de mayúsculas de estilo de título](glossary.md) si es necesario para evitar la combinación de estilos de capitalización.
-   No use ahora las etiquetas del botón de comando porque se puede realizar la inmediatez del comando para concedido.

    -   **Excepción:** Cuando sea necesario, use ahora para diferenciar los comandos que inician una tarea de comandos que realizan una tarea inmediatamente.

    ![captura de pantalla del botón con etiqueta de descarga ](images/ctrl-command-buttons-image32.png)

    En este ejemplo, al hacer clic en el botón de comando se dirige a una ventana o página que permite a los usuarios descargar.

    ![captura de pantalla del botón con la etiqueta Descargar ahora ](images/ctrl-command-buttons-image33.png)

    En este ejemplo, al hacer clic en el botón de comando se realiza la descarga.

    Solo un comando de un flujo de tareas debe etiquetarse con Now. Por lo tanto, por ejemplo, un comando **Descargar ahora** nunca debe ir seguido de otro comando **Descargar ahora** .

-   No use más adelante en etiquetas de botón de comando si implica una acción que no se producirá. Por ejemplo, no use instalar más tarde (a diferencia de instalar ahora) a menos que ese comando se instale en otro momento. En su lugar, use no instalar ni cancelar.

    **Incorrecto:**

    ![captura de pantalla del reinicio ahora y reinicie más tarde ](images/ctrl-command-buttons-image34.png)

    En este ejemplo, el reinicio más adelante implica incorrectamente que el comando se reinicie automáticamente en otro momento.

-   Use un botón Avanzado solo para las opciones que sean relevantes para los usuarios avanzados o para que requieran conocimientos de usuario avanzados. No use un botón avanzado para las características que se consideran tecnológicamente avanzadas. Por ejemplo, la característica de grapado de una impresora no es una opción avanzada, pero su sistema de administración del color es.

    **Incorrecto:** (si las opciones no son realmente avanzadas)

    ![captura de pantalla del botón con etiqueta avanzada ](images/ctrl-command-buttons-image35.png)

    En este ejemplo, la configuración avanzada es engañosa.

    **Correcto:**

    ![captura de pantalla del botón con más etiquetas de opciones ](images/ctrl-command-buttons-image36.png)

    En este ejemplo, la etiqueta es más específica y precisa.

-   En el caso de los botones de comando que abren otras ventanas, elija una etiqueta que use parte o todo el texto de la barra de título de la ventana secundaria. Por ejemplo, un botón de comando con la etiqueta examinar puede abrir un cuadro de diálogo titulado Buscar carpeta. Usar la misma terminología a lo largo de la tarea ayuda a mantener orientado a los usuarios.
-   Al formular una pregunta, use etiquetas que coincidan con la pregunta. No use Aceptar/Cancelar para responder a preguntas de sí/no.

    **Correcto:**

    ![captura de pantalla de los botones sí y no ](images/ctrl-command-buttons-image37.png)

    En este ejemplo, los botones responden a la pregunta.

    **Incorrecto:**

    ![captura de pantalla de los botones aceptar y cancelar ](images/ctrl-command-buttons-image38.png)

    En este ejemplo, los botones no responden a la pregunta.

-   Finalice la etiqueta con un botón de puntos suspensivos si el comando requiere información adicional para ejecutarse.

    -   **Excepción:** Las etiquetas gráficas no tienen puntos suspensivos.

    **Correcto:** (si se muestra un cuadro de diálogo de opciones de impresión)

    ![captura de pantalla del botón imprimir con puntos suspensivos ](images/ctrl-command-buttons-image39.png)

    En este ejemplo, después de hacer clic en el botón, se muestra el cuadro de diálogo Opciones de impresión y requiere más información del usuario.

-   No use puntos suspensivos cuando la finalización correcta de la acción sea simplemente Mostrar otra ventana. Los siguientes comandos nunca toman puntos suspensivos: about, Advanced, Options, Properties, Help.

    **Incorrecto:**

    ![captura de pantalla del botón opciones con puntos suspensivos ](images/ctrl-command-buttons-image40.png)

    En este ejemplo, después de hacer clic en el botón, se muestra el cuadro de diálogo Opciones, pero no se requiere más información del usuario.

-   En caso de ambigüedad (por ejemplo, la etiqueta de comando carece de un verbo), decida en función de la acción más probable del usuario. Si simplemente la ventana es una acción común, no use puntos suspensivos.

    **Correcto:**

    Más colores...

    Información de la versión

    En el primer ejemplo, lo más probable es que los usuarios elijan un color, por lo que el uso de puntos suspensivos es correcto. En el segundo ejemplo, lo más probable es que los usuarios vayan a ver la información de la versión, lo que hará que las elipses sean innecesarias.

-   En el caso de los botones de exploración, use botones de exploración cortos (etiquetados como "...") cuando haya más de dos botones examinar en una ventana. Use siempre la versión abreviada cuando quiera mostrar un botón examinar en una cuadrícula.
-   En el caso de los botones de dirección, use un solo corchete angular y haga que apunte en la dirección en la que se produce la acción.

En la tabla siguiente se muestran algunas etiquetas de botón de comando comunes y su uso.



|                             |                                                                                                              |                             |
|-----------------------------|--------------------------------------------------------------------------------------------------------------|-----------------------------|
| **Etiqueta del botón**<br/> | **Significado**<br/>                                                                                       | **Clave de acceso**<br/>   |
| **Atrás**<br/>         | En asistentes y flujos de tareas, vaya a la página anterior.<br/>                                               | 'B'<br/>              |
| **Examinar...**<br/>    | Muestra un cuadro de diálogo para buscar un archivo o un objeto.<br/>                                                | ' B ' o ' r '<br/>       |
| **Opciones**<br/>      | Muestra las opciones disponibles para los usuarios para personalizar un programa.<br/>                                 | 'O'<br/>              |
| **Pausar**<br/>        | En los cuadros de diálogo en curso, suspenda la tarea.<br/>                                                       | M<br/>              |
| **Personalizar**<br/>  | Personalice una experiencia principal que sea fundamental para la identificación personal del usuario con un programa.<br/> | M<br/>              |
| **Preferencias**<br/>  | No use. En su lugar, use las opciones.<br/>                                                                   | No es aplicable.<br/>  |
| **Propiedades**<br/>   | Mostrar los atributos y la configuración de un objeto.<br/>                                                | ' P ' o primera ' r '<br/> |
| **Guardar**<br/>         | Guarde un grupo de opciones de configuración o guarde un archivo o un objeto con su nombre actual.<br/>                        | Seg<br/>              |
| **Guardar como...**<br/>   | Guardar un archivo o un objeto con un nombre especificado.<br/>                                                     | Segunda ' a '<br/>       |
| **Configuración**<br/>     | No use. En su lugar, use las opciones.<br/>                                                                   | No es aplicable.<br/>  |
| **Solución de problemas**<br/> | No use. En su lugar, use un vínculo de ayuda específico.<br/>                                                      | No es aplicable.<br/>  |



 

Para obtener instrucciones acerca de las etiquetas de los botones de confirmación (aceptar, cancelar, sí/no, cerrar, detener, aplicar, siguiente, finalizar, listo), vea texto de la [interfaz de usuario](text-ui.md).

## <a name="documentation"></a>Documentación

Al hacer referencia a los botones de comando:

-   Use el texto de etiqueta exacto, incluido el uso de mayúsculas, pero no incluya el carácter de subrayado o los puntos suspensivos de la tecla de acceso. No incluya el botón palabra.
-   Para describir la interacción del usuario, use haga clic en.
-   Siempre que sea posible, dé formato a la etiqueta usando texto en negrita. De lo contrario, coloque la etiqueta entre comillas solo si es necesario para evitar confusiones.

Ejemplo: haga clic en **Imprimir** para imprimir el documento.

 

