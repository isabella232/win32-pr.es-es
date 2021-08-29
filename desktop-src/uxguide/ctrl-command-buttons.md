---
title: Botones de comandos
description: Con un botón de comando, los usuarios inician una acción inmediata.
ms.assetid: 0e2ff31a-657b-4e4c-afee-2a6bd742f46c
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: d73e9104edb9e02746660e9e2052e756c5ad7be382e3504ac1f101e7c712a7b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091894"
---
# <a name="command-buttons"></a>Botones de comandos

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

Con un botón de comando, los usuarios inician una acción inmediata.

![captura de pantalla del botón de comando Aceptar ](images/ctrl-command-buttons-image1.png)

Botón de comando típico.

El botón de comando predeterminado se invoca cuando los usuarios presionan la tecla Entrar. Lo asigna el desarrollador, pero cualquier botón de comando se convierte en el valor predeterminado cuando los usuarios le tabulan.

> [!Note]  
> Las directrices relacionadas [con el](vis-layout.md) diseño se presentan en un artículo independiente.

 

## <a name="is-this-the-right-control"></a>¿Es este el control adecuado?

Para decidirte, intenta responder a estas preguntas:

-   **¿Se usa el botón de comando para iniciar una acción inmediata?** Si no es así, usa otro control.
-   **¿Sería mejor un vínculo?** Use un vínculo si:
    -   La acción es navegar a otra página, ventana o tema de Ayuda. **Excepción:** la navegación del asistente usa los botones de comando Atrás y Siguiente.
    -   El comando se incrusta en un cuerpo de texto.
    -   El comando es secundario por naturaleza. Es decir, no se relaciona con el propósito principal de la ventana. En este caso, un botón de comando ligero o un vínculo sería adecuado.
    -   El comando forma parte de un menú o grupo de vínculos relacionados.
    -   La etiqueta es larga, consta de cinco o más palabras, lo que da a un botón de comando un aspecto extraño.
-   **¿Sería mejor una combinación de botones de radio y botones de comandos genéricos?** A menudo, los botones de radio se usan junto con los botones de comando genéricos (Aceptar, Cancelar) en lugar de un conjunto de botones de comando específicos cuando se cumple cualquiera de los siguientes requisitos:
    -   Hay cinco o más acciones posibles.
    -   Los usuarios deben ver información adicional antes de tomar una decisión.
    -   Los usuarios deben interactuar con las opciones (quizás para ver información adicional) antes de tomar una decisión.
    -   Los usuarios ven las opciones como opciones en lugar de comandos diferentes.

        **Correcto:** ![ captura de pantalla del cuadro de diálogo, botones de radio y texto ](images/ctrl-command-buttons-image2.png)

        En este ejemplo, los botones de radio se combinan con los botones Aceptar y Cancelar para proporcionar información adicional sobre las opciones.

        **Incorrecto:** ![ captura de pantalla del mensaje con botones de comando ](images/ctrl-command-buttons-image3.png)

        En este ejemplo, los botones de comando por sí solos dificultan a los usuarios tomar una decisión informada.

## <a name="design-concepts"></a>Conceptos de diseño

**Uso de puntos suspensivos**

Aunque los botones de comando se usan para acciones inmediatas, es posible que se necesite más información para realizar la acción. **Indique un comando que necesita información adicional (incluida la confirmación) agregando** puntos suspensivos al final de la etiqueta del botón .

![captura de pantalla del botón de comando de impresión con puntos suspensivos ](images/ctrl-command-buttons-image4.png)

En este ejemplo, imprimir... El comando muestra un cuadro de diálogo Imprimir para recopilar más información.

![captura de pantalla del botón de comando de impresión, sin puntos suspensivos ](images/ctrl-command-buttons-image5.png)

Por el contrario, en este ejemplo, el comando Imprimir imprime una sola copia de un documento en la impresora predeterminada sin ninguna interacción adicional del usuario.

**El uso adecuado de puntos suspensivos** es importante para indicar que los usuarios pueden tomar más decisiones antes de realizar la acción, o incluso cancelar la acción por completo. La indicación visual que ofrece un botón de puntos suspensivos permite a los usuarios explorar el software sin miedo.

**Esto no significa que deba usar** puntos suspensivos cada vez que una acción muestre otra ventana solo cuando se requiera información adicional para realizar la acción. Por lo tanto, cualquier botón de comando cuyo verbo implícito es "mostrar otra **ventana"** no toma puntos suspensivos, como con los comandos About, Advanced, Help (o cualquier otro comando que se vincule a un tema de Ayuda), Options, Properties o Configuración.

Por lo general, los puntos suspensivos se usan en las interfaces de usuario para indicar que están incompletos. Los comandos que muestran que otras ventanas no están incompletas deben mostrar otra ventana y no se necesita información adicional para realizar su acción. Este enfoque elimina el desorden de pantalla en situaciones en las que los puntos suspensivos tienen poco valor.

**Nota:** Al determinar si un botón de comando necesita puntos suspensivos, no use la necesidad de elevar los [privilegios](winenv-uac.md) como un factor. La elevación no es información necesaria para realizar un comando (en su lugar, es para el permiso) y la necesidad de elevarse se indica con el escudo de seguridad.

**Si solo hace una cosa...** Use una etiqueta concisa, específica y autoexplicativa que describa claramente la acción que realiza el botón de comando y use puntos suspensivos cuando corresponda.

## <a name="usage-patterns"></a>Patrones de uso

Los botones de comando tienen varios patrones de uso:



|     Uso                                                                                                                                                                    |    Ejemplo                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Botones de comando estándar** Puede usar botones de comando estándar para iniciar una acción inmediata.<br/>                                                           | ![captura de pantalla del botón de comando estándar (gris) ](images/ctrl-command-buttons-image6.png)<br/> Botón de comando estándar.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Botones de comando predeterminados** El botón de comando predeterminado de una ventana indica el botón de comando que se activará cuando los usuarios presionen la tecla Entrar.<br/>       | ![captura de pantalla del botón de comando predeterminado (azul) ](images/ctrl-command-buttons-image7.png)<br/> Botón de comando predeterminado.<br/> Cualquier botón de comando se convierte en el valor predeterminado cuando los usuarios le fichan. Si el foco de entrada está en un control que no es un botón de comando, el botón de comando con el atributo de botón predeterminado se convierte en el valor predeterminado. Solo un botón de comando de una ventana puede ser el valor predeterminado.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Botones de comandos ligeros** Un botón de comando ligero es similar a un botón de comando estándar, salvo que su marco de botón solo se muestra al mantener el puntero del mouse. <br/> | ![captura de pantalla de uno de los dos botones de impresión seleccionados ](images/ctrl-command-buttons-image8.png)<br/> En este ejemplo, el comando tiene una apariencia muy ligera (similar [a](ctrl-links.md)un vínculo ) hasta que el usuario mantiene el puntero sobre el comando, momento en el que se dibuja con un marco de botón.<br/> Puede usar botones de comandos ligeros en situaciones en las que usaría un botón de comando estándar, pero quiere evitar mostrar siempre el marco del botón. Los botones de comandos ligeros son ideales para los comandos que desea reducir el tamaño y usar un vínculo no sería adecuado.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **Botones de menú** Use un botón de menú cuando necesite un menú para un pequeño conjunto de comandos relacionados.<br/>                                                                 | ![captura de pantalla del botón de menú formato y sus comandos ](images/ctrl-command-buttons-image9.png)<br/> Botón de menú con un pequeño conjunto de comandos relacionados.<br/> Use un botón de menú cuando no se desea una barra de menús, como en un cuadro de diálogo, una barra de herramientas u otra ventana que no tenga una barra de menús. Un único triángulo que apunta hacia abajo indica que al hacer clic en el botón se mostrará un menú.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **Botones de división** Use un botón de división para consolidar un conjunto de variaciones de un comando, especialmente cuando se usa uno de los comandos la mayoría de las veces.<br/>          | ![captura de pantalla del botón de división abierta sin comandos ](images/ctrl-command-buttons-image10.png)<br/> un botón de división contraído.<br/> Al igual que un botón de menú, un único triángulo que apunta hacia abajo indica que al hacer clic en la parte más derecha del botón, se mostrará un menú.<br/> ![captura de pantalla del botón de división abierto con comandos ](images/ctrl-command-buttons-image11.png)<br/> un botón de división desplegable.<br/> En este ejemplo, se usa un botón de división para consolidar seis variaciones del comando open. El comando abierto normal se usa la mayoría de las veces, por lo que los usuarios normalmente no necesitan ver los demás comandos. el uso de un botón de división ahorra una cantidad significativa de espacio en la pantalla, al tiempo que proporciona opciones eficaces.<br/> A diferencia de un botón de menú, al hacer clic en la parte izquierda del botón se realiza la acción directamente en la etiqueta. Los botones de división son efectivos en situaciones en las que es probable que la siguiente acción con una herramienta específica sea la misma que la última acción. En este caso, la etiqueta se cambia a la última acción, como con un selector de colores:<br/> ![captura de pantalla del botón de división de relleno sin comandos ](images/ctrl-command-buttons-image12.png)<br/> En este ejemplo, la etiqueta cambia a la última acción.<br/> |
| **Botones examinar** Use un botón Examinar para mostrar un cuadro de diálogo para ayudar a los usuarios a seleccionar un valor válido.<br/>                                                           | Los cuadros de diálogo iniciados por un botón Examinar ayudan a los usuarios a seleccionar archivos, carpetas, equipos, usuarios, colores, entre otros. normalmente se combinan con un control sin restricciones, como un cuadro de texto. normalmente se etiquetan como examinar, otros o más, y siempre tienen puntos suspensivos para indicar que se requiere más información. <br/> ![captura de pantalla del cuadro de texto con el botón Examinar ](images/ctrl-command-buttons-image13.png)<br/> un cuadro de texto con un botón Examinar.<br/> Para las ventanas que tienen muchos botones de exploración, puede usar una versión corta:<br/> ![captura de pantalla del botón de exploración corta con puntos suspensivos ](images/ctrl-command-buttons-image14.png)<br/> Un botón examinar corto.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **Botones de divulgación progresiva** Use un botón de divulgación progresiva para mostrar u ocultar las opciones usadas con poca frecuencia.<br/>                                            | Ocultar las opciones usadas con poca frecuencia hasta que se necesiten se denomina divulgación progresiva. Los contenidos de contenido adicional dobles se usan para indicar la divulgación progresiva y apuntan en la dirección en la que se llevará a cabo la revelación u ocultación: <br/> ![captura de pantalla del botón con "más" y flechas derechas ](images/ctrl-command-buttons-image15.png)<br/> Después de hacer clic en el botón, su etiqueta cambia para indicar que el siguiente clic tendrá el efecto contrario:<br/> ![captura de pantalla del botón con "less" y flechas izquierdas ](images/ctrl-command-buttons-image16.png)<br/> Para obtener más información y ejemplos, vea [Controles de divulgación progresiva](ctrl-progressive-disclosure-controls.md). <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **Botones direccionales** Use un botón direccional para indicar la dirección en la que se llevará a cabo una acción.<br/>                                               | En este caso, se usa un corchete angular único en lugar de un botón de contenido adicional doble: <br/> ![captura de pantalla de los botones de flecha derecha e izquierda ](images/ctrl-command-buttons-image17.png)<br/> Un botón direccional indica la dirección de la acción.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="guidelines"></a>Directrices

### <a name="general"></a>General

-   **Muestra un puntero ocupado si el resultado de hacer clic en un botón de comando no es instantáneo.** Sin comentarios, los usuarios podrían suponer que el clic no se ha hecho y hacer clic de nuevo.
-   Si aparece el mismo botón de comando en más de una ventana, intente usar el mismo texto de etiqueta y la misma clave de acceso y localícelo aproximadamente en el mismo lugar de cada ventana cuando **sea práctico.**
-   **Para los botones de comando con etiquetas de texto, use un ancho de botón mínimo y el alto del botón de comando estándar.** Para obtener más información, vea [Tamaño y espaciado recomendados.](#recommended-sizing-and-spacing)
-   Para cada **ventana, los botones de comando tienen el mismo ancho.** Si no es práctico, limite el número de anchos diferentes para los botones de comando con etiquetas de texto a dos.
-   Cuando otro control interopera con un botón de comando, como un cuadro de texto con un botón Examinar, denota la relación colocando el botón de comando en uno de **estos tres lugares:**
    -   A la derecha de y alineado en la parte superior con el otro control.
    -   Debajo y alineado a la izquierda con el otro control.
    -   Centrado verticalmente entre los controles que interoperan (como los botones Agregar y Quitar entre dos cuadros de lista de interoperabilidad).
-   Si varios botones de comando interoperan con el mismo control, apilándolos verticalmente a la derecha de y alineados en la parte superior con el otro control, u colópelos horizontalmente alineados a la izquierda bajo el **control.**
-   Cuando los botones de comando estén subordinados a otros controles, use la selección de ubicación anterior y deshabilite el botón de comando subordinado hasta que se seleccione **el control superior.**
-   **No use botones de comando estrechos,** cortos o altos con etiquetas de texto porque tienden a parecer poco profesionales. Intente trabajar con los anchos y alturas predeterminados.

**Correcto:** ![ captura de pantalla del botón aceptar de tamaño predeterminado ](images/ctrl-command-buttons-image18.png)

En este ejemplo, el tamaño del botón es estándar y tiene un aspecto profesional.

**Incorrecto:** ![ captura de pantalla del botón aceptar corto ](images/ctrl-command-buttons-image19.png)

En este ejemplo, el botón es demasiado pequeño.

**Incorrecto:** ![ captura de pantalla del botón grande aceptar cuadrado ](images/ctrl-command-buttons-image20.png)

En este ejemplo, el botón tiene demasiado espacio alrededor de la etiqueta.

-   **Evite combinar etiquetas de texto y gráficos en los botones de comando.** La combinación de texto y gráficos suele agregar desorden visual innecesario y no mejora la comprensión del usuario. Considere la posibilidad de combinar texto y gráficos solo cuando el gráfico contribuye a la comprensión, como cuando es un símbolo estándar para el comando o ayuda a los usuarios a visualizar los resultados del comando. De lo contrario, prefiere texto, pero use texto o gráficos.

**Correcto:** ![ captura de pantalla del comando de rotación con flecha curva ](images/ctrl-command-buttons-image21.png)

En este ejemplo, el gráfico de flecha ayuda a los usuarios a visualizar los resultados del comando.

**Correcto:** ![ captura de pantalla de la barra de direcciones con iconos y texto ](images/ctrl-command-buttons-image22.png)

En este ejemplo, los símbolos estándar se combinan con texto para facilitar la comprensión

**Incorrecto:** ![ captura de pantalla del botón con el icono x y cancelar ](images/ctrl-command-buttons-image23.png)

En este ejemplo, el gráfico de cancelación no agrega nada al texto.

-   **No use botones de comando para establecer el estado**. En su lugar, use botones de radio o casillas. Los botones de comando solo son para iniciar acciones.

### <a name="split-buttons"></a>Botones de división

-   **Haga que el comando más probable sea el comportamiento predeterminado.** Si hay más de un comando probable, elija uno que no requiera información adicional.
-   **Si el comando más probable es la última selección de usuario, cambie la etiqueta del botón a la última selección.**
-   **Muestre el comando predeterminado mediante texto en negrita en el menú**. Esto facilita a los usuarios la búsqueda del comando predeterminado, especialmente cuando el comando predeterminado es dinámico o el botón de división usa un gráfico en lugar de una etiqueta de texto.

### <a name="default-values"></a>Valores predeterminados

-   Incluya un botón de comando predeterminado en cada cuadro de diálogo. **Seleccione el comando más seguro (para evitar la pérdida** de datos o del sistema) y el comando más seguro para que sea el predeterminado. Si la seguridad y la seguridad no son factores, seleccione el comando más probable o conveniente.
-   **No realice una acción destructiva con el botón de comando predeterminado** a menos que haya una manera fácil de deshacer el comando.

## <a name="recommended-sizing-and-spacing"></a>Tamaño y espaciado recomendados

![diagrama de dimensiones de botón en píxeles y dlus ](images/ctrl-command-buttons-image24.png)

Tamaño y espaciado recomendados para los botones de comando.

## <a name="labels"></a>Etiquetas

-   Etiquete cada botón de comando.
-   Si el botón solo tiene una etiqueta gráfica, asigne su propiedad Name a una etiqueta de texto adecuada. Esto permite que los productos de tecnología de asistencia, como los lectores de pantalla, proporcionen a los usuarios información alternativa sobre el gráfico.

    ![captura de pantalla de los botones de arriba, abajo y copia ](images/ctrl-command-buttons-image25.png)

    En este ejemplo se muestran botones gráficos; internamente, estos botones se etiquetan como Anterior, Siguiente y Copiar.

-   Para los botones de exploración breve (con la etiqueta "..."), la etiqueta interna debe ser Examinar.
-   Asigne una clave [de acceso única.](glossary.md) Para obtener instrucciones, vea [Teclado.](inter-keyboard.md)

    **Excepciones:**

    -   No asigne claves de acceso a los botones Aceptar y Cancelar, ya que Entrar es la clave de acceso del botón predeterminado (que suele ser el botón Aceptar) y Esc es la clave de acceso para Cancelar. Esto facilita la asignación de las demás claves de acceso.
    -   No asigne claves de acceso a los botones de exploración breve (etiquetados como "..."), ya que no se pueden asignar de forma única.

-   Prefiere etiquetas específicas en lugar de genéricas. Lo ideal es que los usuarios no tengan que leer nada más para comprender la etiqueta. Es mucho más probable que los usuarios lean las etiquetas de los botones de comando que el texto estático.

    -   **Excepción:** No cambie el nombre del botón Cancelar si el significado de cancelar no es ambiguo. Los usuarios no deben tener que leer todos los botones para determinar qué botón cancela una acción. Sin embargo, cambie el nombre de Cancelar si no está claro qué acción se está cancelando, por ejemplo, cuando hay varias acciones pendientes.

    **Aceptable:**

    ![Captura de pantalla que muestra los botones "Aceptar" y "Cancelar".](images/ctrl-command-buttons-image26.png)

    En este ejemplo, OK y Cancel son etiquetas aceptables pero no específicas.

    **Mejor:**

    ![captura de pantalla de los botones grabar cd y cancelar ](images/ctrl-command-buttons-image27.png)

    En este ejemplo, Grabar CD es más específico que Aceptar.

    **Incorrecto:**

    ![captura de pantalla de los botones grabar cd y no grabar cd ](images/ctrl-command-buttons-image28.png)

    En este ejemplo, se debe usar Cancelar en lugar de No grabar CD.

-   Inicie las etiquetas con un verbo imperativo y describa claramente la acción que realiza el botón. No uses puntuación final.
    -   **Excepción:** Las siguientes etiquetas estándar son aceptables sin verbos: Advanced, Back, Details, Forward, Less, More, New, Next, No, OK, Options, Previous, Properties, Configuración y Yes.
-   Aunque se prefieren etiquetas cortas, use suficiente texto para explicar el comando lo suficiente. Use un objeto directo (un sustantivo después del verbo) cuando el objeto no sea evidente desde el contexto. Lo ideal es que los usuarios no tengan que leer nada más para comprender la etiqueta.

    **Aceptable:**

    ![captura de pantalla del botón con agregar etiqueta ](images/ctrl-command-buttons-image29.png)

    En este ejemplo, una etiqueta corta es aceptable si su significado en el contexto es evidente.

    **Mejor:** (si Agregar no está claro)

    ![captura de pantalla del botón con la etiqueta Agregar elementos ](images/ctrl-command-buttons-image30.png)

    En este ejemplo, agregar un sustantivo al verbo ayuda a la comprensión de los usuarios.

    **Mejor:** (si agregar o agregar elementos no están claros)

    ![captura de pantalla del botón con agregar elementos seleccionados ](images/ctrl-command-buttons-image31.png)

    En este ejemplo, la etiqueta se explica por sí sola.

-   Use [mayúsculas de estilo oración.](glossary.md) Esto es más adecuado para Windows [tono Windows](text-style-tone.md)[y](https://msdn.microsoft.com/library/windows/desktop/aa974175.aspx) el uso de frases cortas para los botones de comando.
    -   **Excepción:** En el caso de las aplicaciones heredadas, puede usar mayúsculas de estilo de [título](glossary.md) si es necesario para evitar mezclar estilos de mayúsculas.
-   No use ahora en etiquetas de botón de comando porque se puede conceder lamediacia del comando.

    -   **Excepción:** Cuando sea necesario, use ahora para diferenciar los comandos que inician una tarea de los comandos que realizan una tarea inmediatamente.

    ![captura de pantalla del botón con la etiqueta de descarga ](images/ctrl-command-buttons-image32.png)

    En este ejemplo, al hacer clic en el botón de comando se va a una ventana o página que permite a los usuarios descargar.

    ![captura de pantalla del botón con la etiqueta Descargar ahora ](images/ctrl-command-buttons-image33.png)

    En este ejemplo, al hacer clic en el botón de comando se realiza la descarga.

    Solo un comando de un flujo de tareas debe etiquetarse con ahora. Por ejemplo, un comando **Descargar ahora** nunca debe ir seguido de otro **comando Descargar** ahora.

-   No use más adelante en las etiquetas de botón de comando si implica una acción que no se va a producir. Por ejemplo, no use Instalar más adelante (a diferencia de Instalar ahora) a menos que ese comando se instale más adelante. En su lugar, use No instalar o Cancelar.

    **Incorrecto:**

    ![captura de pantalla de reiniciar ahora y reiniciar más adelante ](images/ctrl-command-buttons-image34.png)

    En este ejemplo, Reiniciar posteriormente implica incorrectamente que el comando se reinicia automáticamente más adelante.

-   Use un botón Avanzado solo para las opciones que son relevantes para los usuarios avanzados o requieren conocimientos avanzados del usuario. No use un botón Avanzado para las características que se consideran tecnológicamente avanzadas. Por ejemplo, la característica de estapling de una impresora no es una opción avanzada, pero su sistema de administración de colores es .

    **Incorrecto:** (si las opciones realmente no están avanzadas)

    ![captura de pantalla del botón con etiqueta avanzada ](images/ctrl-command-buttons-image35.png)

    En este ejemplo, Advanced es engañoso.

    **Correcto:**

    ![captura de pantalla del botón con más etiquetas de opciones ](images/ctrl-command-buttons-image36.png)

    En este ejemplo, la etiqueta es más específica y precisa.

-   Para los botones de comando que abren otras ventanas, elija una etiqueta que use parte o todo el texto de la barra de título de la ventana secundaria. Por ejemplo, un botón de comando con la etiqueta Examinar podría abrir un cuadro de diálogo denominado Buscar carpeta. El uso de la misma terminología a lo largo de la tarea ayuda a mantener orientados a los usuarios.
-   Al hacer una pregunta, use etiquetas que coincidan con la pregunta. No use Aceptar/Cancelar para responder preguntas sí/no.

    **Correcto:**

    ![captura de pantalla de botones sí y no ](images/ctrl-command-buttons-image37.png)

    En este ejemplo, los botones responden a la pregunta.

    **Incorrecto:**

    ![captura de pantalla de los botones Aceptar y Cancelar ](images/ctrl-command-buttons-image38.png)

    En este ejemplo, los botones no responden a la pregunta.

-   Finalice la etiqueta con puntos suspensivos si el comando requiere información adicional para ejecutarse.

    -   **Excepción:** Las etiquetas gráficas no toman puntos suspensivos.

    **Correcto:** (si se muestra un cuadro de diálogo Opciones de impresión)

    ![captura de pantalla del botón de impresión con puntos suspensivos ](images/ctrl-command-buttons-image39.png)

    En este ejemplo, después de hacer clic en el botón, se muestra el cuadro de diálogo Opciones de impresión y se requiere más información del usuario.

-   No use puntos suspensivos cuando la finalización correcta de la acción sea simplemente mostrar otra ventana. Los siguientes comandos nunca toman puntos suspensivos: Acerca de, Opciones, Opciones, Propiedades, Ayuda.

    **Incorrecto:**

    ![captura de pantalla del botón de opciones con puntos suspensivos ](images/ctrl-command-buttons-image40.png)

    En este ejemplo, después de hacer clic en el botón, se muestra el cuadro de diálogo Opciones, pero no se requiere más información del usuario.

-   En caso de ambigüedad (por ejemplo, la etiqueta de comando no tiene un verbo), decida en función de la acción del usuario más probable. Si simplemente ver la ventana es una acción común, no use puntos suspensivos.

    **Correcto:**

    Más colores...

    Información de la versión

    En el primer ejemplo, lo más probable es que los usuarios elijan un color, por lo que el uso de puntos suspensivos es correcto. En el segundo ejemplo, lo más probable es que los usuarios van a ver la información de la versión, lo que hace que los puntos suspensivos sean innecesarios.

-   En el caso de los botones de exploración, use botones de exploración breve (etiquetados como "...") cuando haya más de dos botones de exploración en una ventana. Use siempre la versión corta cuando desee mostrar un botón Examinar en una cuadrícula.
-   Para los botones direccionales, use un corchete angular único y haga que apunte en la dirección en la que tiene lugar la acción.

En la tabla siguiente se muestran algunas etiquetas de botón de comando comunes y su uso.



| Etiqueta de botón | Significado              | Clave de acceso   |
|-----------------------------|--------------------------------------------------------------------------------------------------------------|-----------------------------|
| **Atrás**<br/>         | En los asistentes y flujos de tareas, vaya a la página anterior.<br/>                                               | 'B'<br/>              |
| **Examinar...**<br/>    | Mostrar un cuadro de diálogo para buscar un archivo u objeto.<br/>                                                | 'B' o 'r'<br/>       |
| **Opciones**<br/>      | Mostrar las opciones disponibles para los usuarios para personalizar un programa.<br/>                                 | 'O'<br/>              |
| **Pausar**<br/>        | En los cuadros de diálogo en curso, suspenda la tarea.<br/>                                                       | 'P'<br/>              |
| **Personalizar**<br/>  | Personalice una experiencia básica que sea fundamental para la identificación personal del usuario con un programa.<br/> | 'P'<br/>              |
| **Preferencias**<br/>  | No lo use. En su lugar, use Opciones.<br/>                                                                   | No es aplicable.<br/>  |
| **Propiedades**<br/>   | Muestra los atributos y la configuración de un objeto .<br/>                                                | 'P' o primer 'r'<br/> |
| **Guardar**<br/>         | Guarde un grupo de valores o guarde un archivo u objeto con su nombre actual.<br/>                        | 'S'<br/>              |
| **Guardar como...**<br/>   | Guarde un archivo u objeto con un nombre especificado.<br/>                                                     | Segundo "a"<br/>       |
| **Configuración**<br/>     | No lo use. En su lugar, use Opciones.<br/>                                                                   | No es aplicable.<br/>  |
| **Solución de problemas**<br/> | No lo use. En su lugar, use un vínculo de Ayuda específico.<br/>                                                      | No es aplicable.<br/>  |



 

Para obtener instrucciones sobre las etiquetas de botón de confirmación (Ok, Cancel, Yes/No, Close, Stop, Apply, Next, Finish, Done), [vea Interfaz de usuario Text](text-ui.md).

## <a name="documentation"></a>Documentación

Al hacer referencia a los botones de comando:

-   Use el texto exacto de la etiqueta, incluida su inclusión en mayúsculas, pero no incluya el carácter de subrayado ni los puntos suspensivos de la clave de acceso. No incluya el botón de palabra.
-   Para describir la interacción del usuario, use click.
-   Cuando sea posible, formatee la etiqueta con texto en negrita. De lo contrario, coloque la etiqueta entre comillas solo si es necesario para evitar confusiones.

Ejemplo: haga clic **en Imprimir** para imprimir el documento.

 

