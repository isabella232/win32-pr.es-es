---
title: Información sobre herramientas e información sobre herramientas
description: Una información sobre herramientas es una pequeña ventana emergente que etiqueta el control sin etiquetar al que se apunta, como los controles de barra de herramientas sin etiquetar o los botones de comando.
ms.assetid: 80979281-eefb-485a-b42f-7f9e05665357
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 8911c5a008d2de6cec2bd564fd786a23c670d633
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127267444"
---
# <a name="tooltips-and-infotips"></a>Información sobre herramientas e información sobre herramientas

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

Una información sobre herramientas es una pequeña ventana emergente que etiqueta el control sin etiquetar al que se apunta, como los controles de barra de herramientas sin etiquetar o los botones de comando.

![Captura de pantalla que muestra el botón de impresión con la información sobre herramientas "Imprimir (Ctrl+P)" mostrada.](images/ctrl-tooltips-and-infotips-image1.png)

Información sobre herramientas típica para un botón de la barra de herramientas.

Dado que la información sobre herramientas ha demostrado ser tan útil, existe un control relacionado denominado información sobre herramientas, que proporciona texto más descriptivo de lo que es posible con la información sobre herramientas.

Una información es una pequeña ventana emergente que describe concisamente el objeto al que se apunta, como descripciones de controles de barra de herramientas, iconos, gráficos, vínculos, objetos del Explorador de Windows, elementos menú Inicio y botones de la barra de tareas. La información sobre información es una forma de controles [de divulgación progresiva,](ctrl-progressive-disclosure-controls.md)lo que elimina la necesidad de tener siempre texto descriptivo en pantalla.

![captura de pantalla del botón Compartir con información ](images/ctrl-tooltips-and-infotips-image2.png)

Información típica.

Para los fines de este artículo, la información sobre herramientas y la información sobre herramientas se conocen colectivamente como sugerencias.

Sugerencias a los usuarios a comprender objetos desconocidos o desconocidos que no se describen directamente en la interfaz de usuario (UI). Se muestran automáticamente cuando los usuarios mantienen el puntero sobre un objeto y se quitan cuando los usuarios hacen clic en el control o mueven el mouse, o cuando se supera el tiempo de espera de la propina.

**Desarrolladores:** No hay ningún control de información sobre información; La información sobre herramientas se implementa con el control de información sobre herramientas. La distinción está en uso, no en implementación.

> [!Note]  
> Las directrices relacionadas [con los globos,](ctrl-balloons.md) [las barras](cmd-toolbars.md)de herramientas y [la Ayuda](winenv-help.md) se presentan en artículos independientes.

 

## <a name="is-this-the-right-control"></a>¿Es este el control adecuado?

Para decidirte, intenta responder a estas preguntas:

-   **¿La información que se muestra se basa en el puntero?** Si no es así, usa otro control. Mostrar sugerencias solo como resultado de la interacción del usuario nunca las muestra por su cuenta. Por el contrario, [los globos](ctrl-balloons.md) se pueden mostrar por sí mismos (como lo hacen con las notificaciones), por lo que tienen una cola que identifica su origen.
-   **¿Tiene el control una etiqueta de texto?** Si no es así, usa la información sobre herramientas para proporcionar la etiqueta que no tiene. Tenga en cuenta que la mayoría de los controles deben etiquetarse y, por tanto, no tener información sobre herramientas. Los controles de la barra de herramientas y los botones de comando con etiquetas gráficas deben tener información sobre herramientas.
-   **¿Un objeto se beneficia de una descripción complementaria o de información adicional?** Si es así, use una información detallada. Sin embargo, el texto debe ser complementario, es decir, no es esencial para las tareas principales. Si es un concepto esencial, deberías ponerlo directamente en la UI para que los usuarios no tengan que descubrirlo ni buscarlo.
-   **¿La información complementaria es un error, una advertencia o un estado?** Si es así, use otro elemento de la interfaz de usuario, como un globo, un [mensaje de error](mess-error.md)o una barra de [estado](ctrl-status-bars.md). La información sobre el icono del área de notificación es una excepción porque se pueden usar para mostrar información de estado.
-   **¿Es necesario que los usuarios interactúen con el texto de información?** Si es así, use otro control, como un globo. Los usuarios no pueden interactuar con el texto de información ya que en cuanto se mueve el mouse el texto desaparece.
-   **¿Los usuarios necesitan imprimir la información complementaria?** Si es así, use otro control, como un campo de comentario estático. Sin embargo, también puede usar información sobre información para proporcionar acceso más directo a esta información.

    ![captura de pantalla del globo de comentarios ](images/ctrl-tooltips-and-infotips-image3.png)

    En este ejemplo, un campo de comentario estático en Microsoft Word permite a los usuarios imprimir comentarios.

-   **¿El contexto es tal que a los usuarios les pueden parecer molestos o distraer las propinas?** Si es así, considere la posibilidad de usar otra solución, incluido no hacer nada. Si usa sugerencias en estos contextos, permita que los usuarios las desactiven.

Cuando se usan correctamente, las sugerencias mejoran la comunicación con el usuario. **No use nunca sugerencias como sustituto de un buen diseño.** Si un gráfico, un botón u otro objeto requieren que los usuarios sigan comprobando una sugerencia para entenderlo, el diseño es malo. En su lugar, corrija el diseño.

## <a name="design-concepts"></a>Conceptos de diseño

Sugerencias son una manera eficaz de simplificar una interfaz de usuario. Proporcionan información que los usuarios necesitan cuando la necesitan, con el mínimo esfuerzo por su parte. Sugerencias puede ayudarle a usar el espacio de pantalla de forma más eficaz y a reducir el desorden de la pantalla. Sin embargo, las sugerencias mal diseñadas pueden ser molestos, distraídas, poco útiles, abrumadoras o en el camino. Los siguientes conceptos de diseño están diseñados para mostrar la diferencia.

### <a name="discoverability"></a>Detectabilidad

Sugerencias se muestra automáticamente cuando los usuarios mantienen el puntero sobre un objeto durante un período de tiempo. Este mecanismo de retraso de tiempo hace que las sugerencias sea muy conveniente, pero también reduce su detectabilidad.

Con el tiempo, los usuarios aprenden que determinados objetos estándar, como los botones de la barra de herramientas, los botones gráficos, los elementos menú Inicio y los iconos del área de notificación, tienen sugerencias, por lo que puede dar por hecho su detectabilidad.

Los usuarios tardan más tiempo en detectar sugerencias en lugares no estándar. No hay ninguna pista visual, como una zona de acceso rápido o un cambio de puntero, que indique que un objeto tiene una propina. Peor aún, algunos usuarios mueven mucho el mouse, especialmente cuando están aprendiendo a navegar por la interfaz de usuario. Los usuarios deben saber que un objeto tiene una sugerencia, ya sea a través de la experiencia pasada o mediante experimentación.

Puede mejorar la detectabilidad mediante sugerencias de forma coherente, lo que a su vez fomenta la predictibilidad. Si proporciona sugerencias para algunos objetos, debe proporcionarlas para todos los objetos similares para los que es probable que los usuarios quieran obtener información complementaria. A veces, hacerlo puede ser complicado, ya que también debe asegurarse de que las sugerencias son útiles y no obvias.

Si proporcionar sugerencias reconocibles y útiles de forma coherente resulta ser un problema, considere la posibilidad de diseñar diseños alternativos, como etiquetas de control autoexplicativas o texto complementario en su lugar.

### <a name="appropriate-information"></a>Información adecuada

La información adecuada para las sugerencias tiene las siguientes características:

-   **Concisa.** Las ventanas emergentes que usan las sugerencias son perfectas para oraciones cortas y fragmentos de oraciones, así como texto con formato. Los bloques de texto grandes y sin formato son difíciles de leer y abrumadores.
-   **Útil.** El texto de la sugerencia debe ser informativo. No debería ser obvio o simplemente repetir lo que ya está en la pantalla.
-   **Suplemental.** Dado que el texto de sugerencia no siempre está visible, debe ser información complementaria que los usuarios no tengan que leer. La información importante se debe comunicar mediante etiquetas de control autoexplicativas o texto complementario en su lugar.
-   **Estática.** Los usuarios no esperan que las sugerencias cambien de una instancia a la siguiente, por lo que es poco probable que observen cambios en el contenido dinámico, como la información de estado. Las sugerencias de icono del área de notificación son una excepción importante: es más probable que los usuarios detecte cambios en la información de sugerencia porque estos iconos comunican principalmente el estado.

### <a name="appropriate-timeouts"></a>Tiempos de espera adecuados

La presentación y eliminación automáticas adecuadas de sugerencias es fundamental para el objetivo de los usuarios de mantener el control de su entorno de interfaz de usuario. Sugerencias tres valores de tiempo de espera:

-   **Inicial.** Hora a la que el puntero debe permanecer estacionada para que aparezca la sugerencia. El tiempo predeterminado es 0,5 segundos.
-   **Volver a mostrar.** Hora en la que el puntero debe permanecer insostez a medida que el puntero se mueve de un destino a otro. El tiempo predeterminado es 0,1 segundos.
-   **Retiro.** Hora a la que se quita automáticamente la sugerencia. El tiempo predeterminado es 5 segundos.

Tener valores iniciales demasiado cortos y volver a mostrar los resultados da lugar a una experiencia de interrupción y desconcierto, ya que a menudo se muestran de forma involuntaria, mientras que los resultados demasiado largos hacen que las sugerencias no responsiven o no se detectan. El tiempo de eliminación predeterminado funciona bien para el texto de sugerencia corta, como se usa en la información sobre herramientas. Las información sobre información tienen texto más largo, por lo que necesitan tiempos de presentación más largos.

### <a name="appropriate-placement"></a>Ubicación adecuada

Sugerencias debe colocarse cerca del objeto que se mantiene el puntero, normalmente en la cola o la cabeza del puntero, si es posible. Sin embargo, nunca deben colocarse de forma que interfiera con lo que el usuario está haciendo ocultando el objeto de interés. Evitar este problema puede requerir que mueva la propina fuera del puntero, pero adyacente al objeto . Esto no es un problema siempre y cuando la relación entre el objeto y su propina esté clara. Asegúrese de que los usuarios no muevan el puntero solo para obtener las sugerencias del programa para desaparecer.

### <a name="accessibility"></a>Accesibilidad

Sugerencias tienen un efecto inusual en la accesibilidad. Aunque normalmente se desencadenan al mantener el puntero sobre un [](inter-accessibility.md) objeto, los lectores de pantalla controlan las sugerencias para los controles con acceso mediante teclado. Cuando se usa adecuadamente para obtener información concisa, útil, estática y complementaria, las sugerencias pueden mejorar la accesibilidad general. De hecho, el patrón de sugerencia de texto alternativo es la manera preferida de hacer que los gráficos se puedan acceder. Sin embargo, cuando se usan de forma inapropiada, dañan la accesibilidad al dificultar la obtención de información importante o dinámica.

Proporcione más de una manera de acceder a un control si ese control requiere una sugerencia que no tenga acceso al teclado.

![captura de pantalla del botón de impresión con información sobre herramientas ](images/ctrl-tooltips-and-infotips-image4.png)

En este ejemplo, los usuarios pueden imprimir mediante el botón de la barra de herramientas (que no es accesible con el teclado) o el método abreviado de teclado del comando Imprimir.

**Si solo hace una cosa...**

Diseñe sugerencias reconocibles que muestren información concisa, útil, estática y complementaria en el lugar adecuado en el momento adecuado.

## <a name="usage-patterns"></a>Patrones de uso

Sugerencias varios patrones de uso:



|    Uso                                                                                                                             |    Ejemplo                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Información sobre herramientas**<br/> muestra la etiqueta de un glifo o control sin etiquetar. <br/>                                         | Dado que estas sugerencias sirven como etiquetas, su texto sigue las directrices de etiqueta para el control subyacente. <br/> ![captura de pantalla del botón exportar lista con información sobre herramientas ](images/ctrl-tooltips-and-infotips-image5.png)<br/> En este ejemplo, la información sobre herramientas proporciona la etiqueta de comando.<br/> ![captura de pantalla del botón Cerrar con información sobre herramientas ](images/ctrl-tooltips-and-infotips-image6.png)![captura de pantalla del botón de reproducción con información sobre herramientas ](images/ctrl-tooltips-and-infotips-image7.png)<br/> en estos ejemplos, la información sobre herramientas etiqueta botones gráficos.<br/> ![captura de pantalla de mostrar glifo de menú con información sobre herramientas ](images/ctrl-tooltips-and-infotips-image8.png)<br/> En este ejemplo, la información sobre herramientas etiqueta un glifo.<br/> |
| **Información sobre información**<br/> proporcionar una descripción complementaria o una explicación de un objeto o control. <br/>                  | Use información sobre cómo describir o explicar [](cmd-toolbars.md) objetos y controles como controles de barra [](ctrl-progressive-disclosure-controls.md)de [herramientas,](vis-icons.md) iconos (incluidas superposiciones de [iconos),](ctrl-links.md)vínculos, [pestañas,](ctrl-tabs.md)controles de divulgación progresiva y controles personalizados. <br/> ![captura de pantalla del botón de correo electrónico con información ](images/ctrl-tooltips-and-infotips-image9.png)<br/> ![captura de pantalla del botón de grabación con información ](images/ctrl-tooltips-and-infotips-image10.png)<br/> En estos ejemplos, la información sobre información proporciona información complementaria sobre controles y objetos.<br/>                                                                                        |
| **Información sobre texto alternativo**<br/> describir un gráfico de accesibilidad. <br/>                                              | Este patrón es principalmente para los usuarios que tienen algún tipo de discapacidad visual y pueden usar un lector de pantalla. <br/> ![captura de pantalla del botón de inicio de Windows con información ](images/ctrl-tooltips-and-infotips-image11.png)<br/> En este ejemplo, la información describe el menú Inicio gráfico.<br/>                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Vistas en miniatura**<br/> mostrar una imagen pequeña de un elemento. <br/>                                                         | Las miniaturas dan una representación gráfica fácilmente reconocible de una ventana o documento. <br/> ![captura de pantalla de la miniatura de categorías del panel de control ](images/ctrl-tooltips-and-infotips-image12.png)<br/> En este ejemplo, la barra de tareas de Windows proporciona sugerencias en miniatura para sus elementos.<br/> ![captura de pantalla de la miniatura de la foto y sus datos ](images/ctrl-tooltips-and-infotips-image13.png)<br/> En este ejemplo, Windows Galería de fotos sugerencias en miniatura para sus elementos.<br/>                                                                                                                                                                                                                      |
| **Información detallada**<br/> mostrar información detallada sobre un objeto. <br/>                                        | La información sobre información es una manera eficaz de mostrar información detallada sobre un objeto o de proporcionar datos. <br/> ![captura de pantalla de información de la foto que muestra el tipo de archivo ](images/ctrl-tooltips-and-infotips-image14.png)![captura de pantalla del gráfico con valores detallados de información ](images/ctrl-tooltips-and-infotips-image15.png)<br/> En estos ejemplos, la información proporciona información detallada sobre un objeto o datos.<br/>                                                                                                                                                                                                                                                                                                      |
| **Información sobre el menú Inicio**<br/> describir un elemento en el menú Inicio. <br/>                                              | El menú inicio consta de nombres de programa y destinos de ventanas importantes, como documentos, imágenes y panel de control. Estas sugerencias describen los elementos del menú inicio, normalmente mediante una breve descripción del programa o destino, así como las tareas principales que los usuarios pueden realizar con él. Estas descripciones también se indexa mediante el cuadro de búsqueda del menú Inicio, lo que ayuda a los usuarios a encontrar los programas que necesitan. <br/> ![captura de pantalla de información del centro de bienvenida ](images/ctrl-tooltips-and-infotips-image16.png)<br/> En este ejemplo, la información describe lo que los usuarios pueden hacer con un programa en el menú Inicio.<br/>                                                                                    |
| **Panel de control información detallada**<br/> describir una categoría o tarea del panel de control. <br/>                                    | Estas sugerencias proporcionan información complementaria para ayudar a los usuarios a elegir la categoría y el elemento del panel de control adecuados. <br/> ![captura de pantalla de la categoría de cuentas de usuario con información ](images/ctrl-tooltips-and-infotips-image17.png)<br/> En este ejemplo, la información describe las cuentas de usuario Panel de control categoría.<br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| **Información sobre nombres completos**<br/> mostrar el nombre completo de un elemento cuando el nombre se trunca o no es totalmente visible. <br/> | Estas sugerencias le permiten mostrar elementos en un espacio más compacto, a la vez que reducen la necesidad de desplazamiento horizontal. esto es especialmente importante cuando se desconoce la longitud del contenido porque es dinámica. A diferencia de los demás patrones, cuando se usan en listas y árboles, estas sugerencias se muestran directamente sobre el objeto de origen. <br/> ![captura de pantalla de información de grupo de título de botón de radio ](images/ctrl-tooltips-and-infotips-image18.png)<br/> En este ejemplo, se usa una información sobre cómo mostrar el nombre completo del elemento al mantener el puntero.<br/>                                                                                                                                                                                     |
| **Información sobre el estado**<br/> mostrar información de estado de los iconos del área de notificación. <br/>                              | Normalmente, las sugerencias deben ser estáticas porque los usuarios no esperan que cambien de una instancia a la siguiente. **Los iconos del área de notificación son una excepción** porque estos iconos comunican el estado y no hay ningún otro espacio de pantalla disponible para el texto de estado. <br/> ![captura de pantalla de la información sobre "Messenger no ha iniciado sesión" ](images/ctrl-tooltips-and-infotips-image19.png)<br/> ![captura de pantalla de la información sobre "messenger signed in" ](images/ctrl-tooltips-and-infotips-image20.png)<br/> En estos ejemplos, la información sobre información proporciona información de estado para los iconos del área de notificación.<br/>                                                                                                                                  |



 

## <a name="guidelines"></a>Directrices

### <a name="timeouts"></a>Tiempos de espera

-   **Use el valor predeterminado inicial y vuelva a mostrar los tiempos de espera. Excepción:**
    -   Las miniaturas que no son redundantes y que se muestran en el lado de su objeto asociado se pueden mostrar inmediatamente (sin ningún retraso). Sin embargo, use el tiempo de espera inicial predeterminado para miniaturas redundantes (como una sugerencia de miniatura grande para un objeto gráfico pequeño) o miniaturas que cubren su objeto asociado.
-   **Para información sobre herramientas, use el tiempo de espera predeterminado de eliminación de propinas de cinco segundos.**
-   **Para obtener información, desactive el tiempo de espera de eliminación de propinas. Desarrolladores:** puesto que técnicamente no se puede desactivar el tiempo de espera de eliminación, estamúzcalo en su valor más grande.
-   Para lograr accesibilidad, si necesita establecer los valores de tiempo de espera en un valor distinto del valor máximo, consúltelos múltiplos de los parámetros del sistema SPI \_ GETMOUSEHOVERTIME y SPI GETMESSAGEDURATION en lugar de usar horas \_ fijas. Al hacerlo, se ajustan los tiempos de espera a la velocidad del usuario.

### <a name="placement"></a>Selección de ubicación

-   **Evite cubrir el objeto con el que el usuario está a punto de ver o interactuar.** Coloque siempre la sugerencia en el lado del objeto, incluso si eso requiere separación entre el puntero y la sugerencia. Cierta separación no es un problema siempre y cuando la relación entre el objeto y su propina esté clara.

    -   **Excepción:** Información sobre herramientas de nombre completo que se usa en listas y árboles.

    **Incorrecto:**

    ![captura de pantalla del cuadro de búsqueda de ocultación de información ](images/ctrl-tooltips-and-infotips-image21.png)

    **Correcto:**

    ![captura de pantalla de información sobre información colocada debajo del cuadro de búsqueda ](images/ctrl-tooltips-and-infotips-image22.png)

    En el ejemplo correcto, la información sobre la información se coloca fuera del cuadro de búsqueda, aunque eso requiere espacio entre ella y el caret.

    **Incorrecto:**

    ![captura de pantalla de información sobre el texto revisado ](images/ctrl-tooltips-and-infotips-image23.png)

    **Correcto:**

    ![captura de pantalla de información sobre texto revisado ](images/ctrl-tooltips-and-infotips-image24.png)

    En el ejemplo correcto, el texto subyacente es mucho más útil que la sugerencia, por lo que la información se coloca fuera del camino.

-   **En el caso de las colecciones de elementos, evite cubrir el siguiente objeto con el que es probable que el usuario vea o interactúe.** Para los elementos organizados horizontalmente, evite colocar sugerencias a la derecha; para elementos organizados verticalmente, evite colocar sugerencias a continuación.

    **Incorrecto:**

    ![captura de pantalla de información sobre la lista de elementos recientes ](images/ctrl-tooltips-and-infotips-image25.png)

    **Correcto:**

    ![captura de pantalla de información junto a la lista de elementos recientes ](images/ctrl-tooltips-and-infotips-image26.png)

    En el ejemplo incorrecto, la sugerencia cubre el objeto con el que es más probable que el usuario interactúe a continuación.

-   **Para sugerencias potencialmente distraídas (a menudo grandes), asegúrese de que la información sea útil para la mayoría de los usuarios.** Si ese no es el caso, puede hacer que las sugerencias de distracción sea opcional o incluso eliminarlas. De lo contrario, la mayoría de los usuarios tendrán que mover el puntero fuera del objeto de destino para deshacerse de la propina.

### <a name="tooltips"></a>Información sobre herramientas

-   **Use información sobre herramientas para proporcionar etiquetas para controles sin etiquetar.** Los controles que normalmente tienen información sobre herramientas son botones de barra [de](cmd-toolbars.md)herramientas, botones gráficos y [controles de divulgación progresiva.](ctrl-progressive-disclosure-controls.md) Los controles con avisos se consideran etiquetados, como cuadros [de texto](ctrl-text-boxes.md) y [cuadros combinados.](/windows/desktop/uxguide/ctrl-drop) Todos los demás controles deben tener etiquetas explícitas.
-   Use fragmentos de oración sin finalizar los signos de puntuación.
-   Use mayúsculas de estilo de frase.
    -   **Excepción:** Esta guía es nueva para Windows Vista. En el caso de las aplicaciones heredadas, puede usar mayúsculas de estilo de título si es necesario para evitar mezclar estilos de mayúsculas.
-   Agregue puntos [suspensivos si](ctrl-command-buttons.md) la etiqueta es para un comando que necesita información adicional.
-   Al igual que con las etiquetas normales, mantenga la información sobre **herramientas breve,** normalmente cinco palabras o menos, pero prefiere etiquetas específicas en lugar de etiquetas imprecisas.

    **Aceptable:**

    ![captura de pantalla de la información sobre herramientas de impresión ](images/ctrl-tooltips-and-infotips-image27.png)

    **Mejor:**

    ![captura de pantalla de la información sobre herramientas "Imprimir en impresora predeterminada" ](images/ctrl-tooltips-and-infotips-image28.png)

    **Mejor:**

    ![captura de pantalla de la información sobre herramientas "imprimir (escritor de documentos)" ](images/ctrl-tooltips-and-infotips-image29.png)

    **Incorrecto:**

    ![captura de pantalla de información detallada ](images/ctrl-tooltips-and-infotips-image30.png)

    En estos ejemplos, el mejor ejemplo es conciso y específico, mientras que el ejemplo incorrecto es innecesariamente detallado.

-   **La información sobre herramientas también puede proporcionar más detalles para los botones de la barra de herramientas etiquetados si resulta útil.** No repita o dé una declaración de palabras de lo que ya está en la etiqueta.

    **Correcto:**

    ![captura de pantalla de la información sobre herramientas "Buscar en todas las perspectivas" ](images/ctrl-tooltips-and-infotips-image31.png)

    En este ejemplo, la información sobre herramientas explica lo que hace la búsqueda.

    **Incorrecto:**

    ![captura de pantalla de la etiqueta de botón de repetición de información sobre herramientas ](images/ctrl-tooltips-and-infotips-image32.png)

    En este ejemplo, la información sobre herramientas solo repite lo que ya está en la etiqueta.

-   **No tiene que proporcionar información sobre herramientas de controles etiquetados simplemente por coherencia.**

    ![captura de pantalla de botones etiquetados y sin etiquetar ](images/ctrl-tooltips-and-infotips-image33.png)

    En este ejemplo, los botones de la barra de herramientas sin etiquetar tienen información sobre herramientas, pero los etiquetados no.

-   Siempre que sea necesario, **haga que la información sobre herramientas sea más útil proporcionando métodos abreviados de teclado y valores predeterminados.** Coloque esta información adicional entre paréntesis. Si lo hace, la información sobre herramientas resulta útil para los controles etiquetados incluso cuando, de lo contrario, simplemente repiten la etiqueta. No tenga en cuenta este texto adicional al evaluar la conciso de una información sobre herramientas.

    ![captura de pantalla de la información sobre herramientas "imprimir (escritor de documentos)" ](images/ctrl-tooltips-and-infotips-image29.png)

    En este ejemplo, Word muestra los valores predeterminados y los métodos abreviados de teclado en la información sobre herramientas de la barra de herramientas.

### <a name="infotips"></a>Información sobre información

-   **Para obtener información sobre información en lugares no estándar, favorezca la coherencia sobre la utilidad para mejorar la detectabilidad.** Proporcione sugerencias para todos los objetos para los que es probable que los usuarios quieran información complementaria, aunque algunas información puedan ser obvias. De este modo, se evita que los usuarios esperen una información que nunca llegará.
    -   **Excepción:** Si solo algunos objetos tienen información útil, no use ninguna información. En su lugar, use etiquetas de control autoexplicativas o texto complementario en su lugar.
-   Use oraciones completa con puntuación final.
    -   **Excepción:** La información sobre [el icono del](winenv-notification.md) área de notificación no usa la puntuación final.
-   Use mayúsculas de estilo de frase.
-   Use el tiempo presente, no el futuro.
-   Use construcciones gramaticales paralelas. El paralelismo requiere que las palabras y frases que tienen la misma función tengan la misma forma.
    -   **Excepción:** Para el patrón de información de nombre completo, el texto de información coincide exactamente con la expresión, la mayúscula y la puntuación del control subyacente.
-   **Evite información de gran tamaño.** La información de gran tamaño es difícil de leer y difícil de colocar sin interferir con el objeto subyacente.
-   **Dar formato a información para que su contenido sea más fácil de leer y examinar.** Los bloques grandes de texto sin formato pueden ser difíciles de leer.

    **Incorrecto:**

    ![captura de pantalla de información sobre herramientas larga, no estructurada y de ejecución ](images/ctrl-tooltips-and-infotips-image34.png)

    **Correcto:**

    ![captura de pantalla de la misma información sobre herramientas con una línea por elemento ](images/ctrl-tooltips-and-infotips-image35.png)

    En el ejemplo correcto, el texto con formato es mucho más fácil de leer y examinar.

-   En el primer uso dentro de una información, deletree los nombres de los acrónimos, seguidos del acrónimo entre paréntesis. Ejemplo: "Protocolo de configuración dinámica de host (DHCP)".

### <a name="start-menu-infotips"></a>Información sobre el menú Inicio

-   Use menú Inicio información para describir el elemento de forma concisa y enumerar las tareas principales que los usuarios **pueden realizar con el elemento.**
-   **Ser útil.** Céntrate en lo que pueden hacer los usuarios. No repita simplemente el nombre del elemento ni siquiera úselo en la descripción.
-   **Ser específico.** Evite verbos genéricos y frases como y otras tareas. Si la información es importante, enumédala específicamente; De lo contrario, suponga que los usuarios entienden que no todo aparece en la información.
-   **Sea conciso.** Use 25 palabras o menos. La información más larga desaconseja la lectura.
-   **Comience con un verbo imperativo presente-tenso,** como crear, editar, mostrar y enviar. Prefiere verbos específicos sobre verbos genéricos, como administrar y abrir, que realmente se aplican a la mayoría menú Inicio elementos. Ir directamente al punto.

    **Incorrecto:**

    ![captura de pantalla de información sobre herramientas: abre la carpeta music ](images/ctrl-tooltips-and-infotips-image36.png)

    **Mejor:**

    ![captura de pantalla de información sobre herramientas: almacenar y reproducir música ](images/ctrl-tooltips-and-infotips-image37.png)

    En el ejemplo incorrecto, la información comienza con un verbo genérico. El mejor ejemplo llega hasta el punto con verbos específicos, pero sigue utilizando las expresiones innecesarias "y otras" al final de la propina.

-   **No use lenguaje que suene a marketing.**

    **Incorrecto:**

    ![Captura de pantalla de la información de "punto de partida único" ](images/ctrl-tooltips-and-infotips-image38.png)

    En este ejemplo, la información sobre información parece marketing.

-   Dado que estas información se indexan para el cuadro de búsqueda menú Inicio, describa las tareas importantes del programa mediante términos para los que es más probable que los **usuarios busquen. Considere la posibilidad de usar palabras clave y sinónimos comunes.**

    **Incorrecto:**

    ![captura de pantalla de información sobre herramientas: creación de dvds ](images/ctrl-tooltips-and-infotips-image39.png)

    **Correcto:**

    ![captura de pantalla de información sobre herramientas: crear (grabar) cds, dvds ](images/ctrl-tooltips-and-infotips-image40.png)

    En el ejemplo correcto, la información sobre información tiene sinónimos comunes.

-   Use mayúsculas de estilo de frase.
-   **Desarrolladores:** El menú Inicio de información del elemento procede del campo Comentario del elemento.

### <a name="quick-launch-tooltips"></a>inicio rápido información sobre herramientas

-   **Use una información sobre herramientas con el formato :** Launch (nombre completo del programa)
-   No uses puntuación final.
-   No use texto adicional para describir el programa ni lo que hace. Dado que los usuarios eligen los programas que se muestran en la inicio rápido, ya conocen su propósito.

### <a name="control-panel-infotips"></a>Panel de control información general

-   Use Panel de control información para describir de forma concisa las **tareas Panel de control y el hardware y el software configurados.**
-   **Panel de control nombres e iconos deben tener información detallada.** Las tareas individuales no tienen información sobre herramientas.
-   **Ser útil.** Céntrate en lo que pueden hacer los usuarios. No repita simplemente el nombre Panel de control elemento o úselo en la descripción.
-   **Ser específico.** Evite verbos genéricos y frases como y otro hardware. Si la información es importante, enumédala específicamente; De lo contrario, suponga que los usuarios entienden que no todo aparece en la información.

    **Incorrecto:**

    ![captura de pantalla de información sobre herramientas: configura el mouse ](images/ctrl-tooltips-and-infotips-image41.png)

    **Correcto:**

    ![captura de pantalla de información sobre herramientas detallada para la configuración del mouse ](images/ctrl-tooltips-and-infotips-image42.png)

    En el ejemplo correcto, se enumeran específicamente los tipos de hardware configurados.

-   **Sea conciso.** Use 25 palabras o menos. La información más larga desaconseja la lectura.
-   **Comience con un verbo imperativo presente-tenso.**

    **Correcto:**

    Configure las opciones de conexión y presentación de Internet.

    Ajuste la configuración de la visión, la escucha y la movilidad.

-   **Ir directamente al punto.** No use lenguaje que se aplique a Panel de control, como "Use to view and configure settings for the appearance and functionality of your..." o "Proporciona opciones para que..."
-   No use lenguaje que suene a marketing.

    **Incorrecto:**

    Punto de partida único para todas las necesidades de configuración del disco.

-   Dado que estas información se indexan para el cuadro de Panel de control búsqueda, describa los elementos mediante términos para los que es más probable que **los usuarios busquen.** Considere la posibilidad de usar sinónimos comunes para tareas y objetos populares.

    ![captura de pantalla de información sobre herramientas con tareas de controlador de juegos ](images/ctrl-tooltips-and-infotips-image43.png)

    En este ejemplo, el elemento se describe mediante términos para los que es más probable que los usuarios busquen.

-   Si es probable que Panel de control elemento se confunda con otros, explique cómo es diferente en la información.

    **Incorrecto:**

    ![captura de pantalla de información que carece de detalles específicos ](images/ctrl-tooltips-and-infotips-image44.png)

    En este ejemplo, ambos Panel de control configuran el sonido, pero la información no aclara la diferencia.

    **Correcto:**

    ![captura de pantalla de información con detalles específicos ](images/ctrl-tooltips-and-infotips-image45.png)

    En este ejemplo, la diferencia entre los dos elementos es más evidente debido a la propina.

### <a name="icons"></a>Iconos

A diferencia de las versiones anteriores Windows, Windows Vista permite que las sugerencias tengan iconos.

-   En el caso de la información sobre herramientas, no use iconos.
-   Para obtener información, use iconos solo si ayudan en el reconocimiento o la comprensión, o proporcionan contexto. La mayoría de las sugerencias de información no deben tener iconos.

    ![captura de pantalla de información de volumen con icono de casco ](images/ctrl-tooltips-and-infotips-image46.png)

    En este ejemplo, la información sobre información tiene un icono para ayudar a asociar el icono a su significado.

-   El icono debe usar el [estilo Deer](vis-icons.md) y tener una apariencia discreta.

Para obtener instrucciones y ejemplos de iconos generales, vea [Iconos](vis-icons.md).

## <a name="documentation"></a>Documentación

Al hacer referencia a las sugerencias:

-   En programación y otra documentación técnica, consulte el tipo de sugerencia (información sobre herramientas o información). En cualquier otro lugar, simplemente llámelo propina.
-   Las siguientes variaciones son incorrectas: información sobre herramientas, información sobre herramientas e información sobre herramientas.
-   Para describir la interacción del usuario, use el mouse.

