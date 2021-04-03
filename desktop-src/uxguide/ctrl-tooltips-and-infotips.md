---
title: Información sobre herramientas y recuadros informativos
description: La información sobre herramientas es una pequeña ventana emergente que etiqueta el control sin etiqueta al que se apunta, como los controles de barra de herramientas o los botones de comando sin etiquetar.
ms.assetid: 80979281-eefb-485a-b42f-7f9e05665357
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: ddccf694b51bf8357dd779bd70146bebf4f14345
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "103913990"
---
# <a name="tooltips-and-infotips"></a>Información sobre herramientas y recuadros informativos

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

La información sobre herramientas es una pequeña ventana emergente que etiqueta el control sin etiqueta al que se apunta, como los controles de barra de herramientas o los botones de comando sin etiquetar.

![Captura de pantalla que muestra el botón imprimir con la información sobre herramientas "Imprimir (Ctrl + P)" mostrada.](images/ctrl-tooltips-and-infotips-image1.png)

Información sobre herramientas típica para un botón de la barra de herramientas.

Dado que la información sobre herramientas ha demostrado ser útil, existe un control relacionado denominado recuadros informativos, que proporciona un texto más descriptivo que el que es posible con la información sobre herramientas.

Un recuadro informativo es una pequeña ventana emergente que describe de manera concisa el objeto al que se apunta, como descripciones de controles de barra de herramientas, iconos, gráficos, vínculos, objetos del explorador de Windows, elementos del menú Inicio y botones de la barra de tareas. Recuadros informativos son una forma de [controles de divulgación progresiva](ctrl-progressive-disclosure-controls.md), lo que elimina la necesidad de tener siempre texto descriptivo en la pantalla.

![captura de pantalla del botón compartir con recuadro informativo ](images/ctrl-tooltips-and-infotips-image2.png)

Un recuadro informativo típico.

Para los fines de este artículo, la información sobre herramientas y recuadros informativos se conocen colectivamente como sugerencias.

Las sugerencias ayudan a los usuarios a comprender objetos desconocidos o desconocidos que no se describen directamente en la interfaz de usuario (UI). Se muestran automáticamente cuando los usuarios desplazan el puntero sobre un objeto y se quitan cuando los usuarios hacen clic en el control o mueven el mouse, o cuando se agota el tiempo de espera de la sugerencia.

**Desarrolladores:** No hay ningún control de recuadro informativo; recuadros informativos se implementan con el control ToolTip. La distinción está en uso, no en la implementación.

> [!Note]  
> Las instrucciones relacionadas con los [globos](ctrl-balloons.md), las [barras de herramientas](cmd-toolbars.md)y la [ayuda](winenv-help.md) se presentan en artículos independientes.

 

## <a name="is-this-the-right-control"></a>¿Es este el control adecuado?

Para decidirte, intenta responder a estas preguntas:

-   **¿La información se muestra en función del desplazamiento del puntero?** Si no es así, usa otro control. Mostrar sugerencias solo como resultado de la interacción del usuario nunca las muestra por sí mismas. Por el contrario, los [globos](ctrl-balloons.md) se pueden mostrar por su cuenta (como hacen con las notificaciones), por lo que tienen un final que identifica su origen.
-   **¿Tiene el control una etiqueta de texto?** Si no es así, usa la información sobre herramientas para proporcionar la etiqueta que no tiene. Tenga en cuenta que la mayoría de los controles deben etiquetarse y, por lo tanto, no tener información sobre herramientas. Los controles de barra de herramientas y los botones de comando con etiquetas gráficas deben tener información sobre herramientas.
-   **¿Se beneficia un objeto de una descripción complementaria o de información adicional?** Si es así, use un recuadro informativo. Sin embargo, el texto debe ser complementario, es decir, no es esencial para las tareas principales. Si es un concepto esencial, deberías ponerlo directamente en la UI para que los usuarios no tengan que descubrirlo ni buscarlo.
-   **¿La información complementaria es un error, una advertencia o un estado?** Si es así, use otro elemento de la interfaz de usuario, como un globo, un [mensaje de error](mess-error.md)o una [barra de estado](ctrl-status-bars.md). El icono del área de notificación recuadros informativos son una excepción porque se pueden usar para mostrar información de estado.
-   **¿Es necesario que los usuarios interactúen con el texto de información?** Si es así, use otro control, como un globo. Los usuarios no pueden interactuar con el texto de información ya que en cuanto se mueve el mouse el texto desaparece.
-   **¿Los usuarios deben imprimir la información complementaria?** Si es así, use otro control, como un campo de comentario estático. Sin embargo, también puede usar recuadros informativos para proporcionar un acceso más directo a esta información.

    ![captura de pantalla de globo de comentario ](images/ctrl-tooltips-and-infotips-image3.png)

    En este ejemplo, un campo de comentario estático en Microsoft Word permite a los usuarios imprimir comentarios.

-   **¿Es el contexto de modo que los usuarios puedan encontrar las sugerencias molestas o distraerles?** Si es así, considere la posibilidad de usar otra solución, que incluye no hacer nada. Si usa sugerencias en estos contextos, permita que los usuarios los desactiven.

Cuando se usa de forma adecuada, las sugerencias mejoran la comunicación con el usuario. **No use nunca sugerencias como sustitutos de un buen diseño.** Si un gráfico, un botón u otro objeto requiere que los usuarios sigan comprobando una sugerencia para comprenderlo, el diseño es incorrecto. En su lugar, corrija el diseño.

## <a name="design-concepts"></a>Conceptos de diseño

Las sugerencias son una manera eficaz de simplificar una interfaz de usuario. Proporcionan información que los usuarios necesitan cuando lo necesitan, con el mínimo esfuerzo por su parte. Las sugerencias pueden ayudarle a usar el espacio de pantalla de forma más eficaz y a reducir el desorden de la pantalla. Sin embargo, las sugerencias mal diseñadas pueden resultar molestas, distraerles, no útiles, abrumantes o en el camino. Los siguientes conceptos de diseño están diseñados para mostrar la diferencia.

### <a name="discoverability"></a>Detectabilidad

Las sugerencias se muestran automáticamente cuando los usuarios desplazan el puntero sobre un objeto durante un período de tiempo. Este mecanismo de retraso de tiempo hace que las sugerencias sean muy convenientes, pero también reduce su capacidad de detección.

Con el tiempo, los usuarios aprenden que ciertos objetos estándar, como los botones de la barra de herramientas, los botones gráficos, los elementos del menú Inicio y los iconos del área de notificación, tienen sugerencias, por lo que puede aprovechar la capacidad de detección de concedidos.

Permite que los usuarios obtengan más sugerencias en lugares no estándar. No hay ninguna pista visual, como una zona activa o un cambio de puntero, que indica que un objeto tiene una sugerencia. Peor aún, algunos usuarios mueven el mouse sobre un gran número, especialmente cuando aprenden a navegar por la interfaz de usuario. Los usuarios deben saber que un objeto tiene una sugerencia, ya sea a través de la experiencia anterior o por experimentación.

Puede mejorar la capacidad de detección mediante el uso de sugerencias de forma coherente, lo que a su vez fomenta la previsibilidad. Si proporciona sugerencias para algunos objetos, debe proporcionarlos para todos los objetos similares para los que es probable que los usuarios deseen obtener información complementaria. En ocasiones, esto puede resultar complicado, porque también debe asegurarse de que las sugerencias son útiles y no obvias.

Si proporciona sugerencias que se pueden detectar de manera coherente y que resultan un problema, considere la posibilidad de diseñar diseños alternativos, como etiquetas de control autoexplicativas o texto complementario en contexto.

### <a name="appropriate-information"></a>Información adecuada

La información adecuada para las sugerencias tiene las siguientes características:

-   **Precisa.** Las ventanas emergentes que se usan en las sugerencias son perfectas para frases cortas y fragmentos de oraciones, así como texto con formato. Los bloques de texto grandes y sin formato son difíciles de leer y abrumar.
-   **Muy.** El texto de sugerencia debe ser informativo. No debe ser obvio o simplemente repetir lo que ya está en la pantalla.
-   **Complementario.** Dado que el texto de sugerencia no está siempre visible, debe ser información complementaria que los usuarios no tienen que leer. La información importante debe comunicarse con etiquetas de control autoexplicativas o texto complementario en contexto.
-   **Estático.** Los usuarios no esperan que las sugerencias cambien de una instancia a la siguiente, por lo que es probable que no perciban cambios en el contenido dinámico, como la información de estado. Los iconos del área de notificación son una excepción importante: los usuarios tienen más probabilidades de detectar los cambios en la información de sugerencia porque estos iconos comunican principalmente el estado.

### <a name="appropriate-timeouts"></a>Tiempos de espera adecuados

La presentación y desinstalación automáticas adecuadas es fundamental para el objetivo de los usuarios que mantienen el control de su entorno de interfaz de usuario. Las sugerencias tienen tres valores de tiempo de espera:

-   **Inicial.** La hora a la que debe permanecer el puntero para que aparezca la sugerencia. El tiempo predeterminado es de 0,5 segundos.
-   **Mostrar.** La hora a la que el puntero debe permanecer estacionario cuando el puntero se mueve de un destino a otro. El tiempo predeterminado es de 0,1 segundos.
-   **Retirada.** Hora a partir de la cual se quita automáticamente la sugerencia. El tiempo predeterminado es de 5 segundos.

El hecho de tener valores iniciales y de volver a mostrar demasiado cortos da lugar a una experiencia molesta y molesta, ya que a menudo se mostraban involuntariamente, mientras que los resultados demasiado largos en las sugerencias no responden o no se detectan. El tiempo de eliminación predeterminado funciona bien para el texto de sugerencia corta, tal como se usa en la información sobre herramientas. Recuadros informativos tienen texto más largo, por lo que necesitan tiempos de visualización más largos.

### <a name="appropriate-placement"></a>Selección de ubicación adecuada

Las sugerencias deben colocarse cerca del objeto que se mantiene, normalmente en la cola del puntero o en el encabezado si es posible. Sin embargo, nunca deben colocarse de forma que interfieran con lo que está haciendo el usuario ocultando el objeto de interés. Para evitar este problema, es posible que le obligue a desplazar la sugerencia fuera del puntero pero junto al objeto. Esto no supone un problema, siempre que la relación entre el objeto y su sugerencia esté clara. Asegúrese de que los usuarios no mueven el puntero solo para que las sugerencias del programa se eliminen.

### <a name="accessibility"></a>Accesibilidad

Las sugerencias tienen un efecto inusual en la accesibilidad. Aunque normalmente se desencadenan al mantener el puntero sobre un objeto, los [lectores de pantalla](inter-accessibility.md) controlan las sugerencias para los controles con acceso mediante teclado. Cuando se usa de forma adecuada para obtener información complementaria, de utilidad y concisa, las sugerencias pueden mejorar la accesibilidad global. De hecho, el patrón de sugerencia de texto alternativo es la manera preferida de que los gráficos sean accesibles. Sin embargo, cuando se usa de forma inapropiada, perjudican la accesibilidad al hacer más difícil obtener información importante o dinámica.

Proporcionar más de una manera de tener acceso a un control si ese control requiere una sugerencia que no tenga acceso mediante teclado.

![captura de pantalla del botón imprimir con información sobre herramientas ](images/ctrl-tooltips-and-infotips-image4.png)

En este ejemplo, los usuarios pueden imprimir con el botón de barra de herramientas (que no es accesible desde el teclado) o con el método abreviado de teclado del comando imprimir.

**Si solo hace algo...**

Diseñar sugerencias reconocibles que muestren información complementaria, concisa y útil en el lugar adecuado en el momento adecuado.

## <a name="usage-patterns"></a>Patrones de uso

Las sugerencias tienen varios patrones de uso:



|                                                                                                                                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Información sobre herramientas**<br/> muestra la etiqueta de un control o glifo sin etiquetar. <br/>                                         | Dado que estas sugerencias sirven como etiquetas, el texto sigue las instrucciones de etiqueta del control subyacente. <br/> ![captura de pantalla del botón Exportar lista con información sobre herramientas ](images/ctrl-tooltips-and-infotips-image5.png)<br/> en este ejemplo, la información sobre herramientas proporciona la etiqueta del comando.<br/> ![captura de pantalla del botón cerrar con información sobre herramientas ](images/ctrl-tooltips-and-infotips-image6.png)![captura de pantalla del botón de reproducción con información sobre herramientas ](images/ctrl-tooltips-and-infotips-image7.png)<br/> en estos ejemplos, los botones gráficos de etiqueta de información sobre herramientas.<br/> ![captura de pantalla del glifo de menú Mostrar con información sobre herramientas ](images/ctrl-tooltips-and-infotips-image8.png)<br/> En este ejemplo, la información sobre herramientas etiqueta un glifo.<br/> |
| **Recuadros informativos**<br/> proporcione una descripción complementaria o una explicación de un objeto o control. <br/>                  | Use recuadros informativos para describir o explicar objetos y controles como, por ejemplo, controles de [barra de herramientas](cmd-toolbars.md) , [iconos](vis-icons.md) (incluidas las superposiciones de iconos), [vínculos](ctrl-links.md), [pestañas](ctrl-tabs.md), [controles de divulgación progresiva](ctrl-progressive-disclosure-controls.md)y controles personalizados. <br/> ![captura de pantalla del botón de correo electrónico con recuadro informativo ](images/ctrl-tooltips-and-infotips-image9.png)<br/> ![captura de pantalla del botón de grabación con recuadro informativo ](images/ctrl-tooltips-and-infotips-image10.png)<br/> En estos ejemplos, recuadros informativos proporciona información complementaria sobre los controles y los objetos.<br/>                                                                                        |
| **Recuadros informativos de texto alternativo**<br/> describir un gráfico para accesibilidad. <br/>                                              | Este patrón es principalmente para los usuarios que tienen alguna forma de discapacidad visual y pueden usar un lector de pantalla. <br/> ![captura de pantalla del botón Inicio de Windows con recuadro informativo ](images/ctrl-tooltips-and-infotips-image11.png)<br/> En este ejemplo, el recuadro informativo describe el gráfico del menú Inicio.<br/>                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Vistas en miniatura**<br/> muestra una imagen pequeña de un elemento. <br/>                                                         | Las miniaturas proporcionan una representación gráfica fácilmente reconocible de una ventana o un documento. <br/> ![captura de pantalla de la miniatura de las categorías del panel de control ](images/ctrl-tooltips-and-infotips-image12.png)<br/> en este ejemplo, la barra de tareas de Windows proporciona sugerencias de miniaturas para sus elementos.<br/> ![captura de pantalla de la miniatura de la fotografía y sus datos ](images/ctrl-tooltips-and-infotips-image13.png)<br/> En este ejemplo, la Galería fotográfica de Windows proporciona sugerencias de miniaturas para sus elementos.<br/>                                                                                                                                                                                                                      |
| **Detalle recuadros informativos**<br/> muestra información detallada acerca de un objeto. <br/>                                        | Recuadros informativos son una manera eficaz de Mostrar información detallada sobre un objeto o de proporcionar datos. <br/> ![captura de pantalla del recuadro informativo de la foto que muestra el tipo de archivo ](images/ctrl-tooltips-and-infotips-image14.png)![captura de pantalla de un gráfico con valores representativos detallados ](images/ctrl-tooltips-and-infotips-image15.png)<br/> En estos ejemplos, recuadros informativos proporciona información detallada sobre un objeto o datos.<br/>                                                                                                                                                                                                                                                                                                      |
| **Menú Inicio recuadros informativos**<br/> describir un elemento en el menú Inicio. <br/>                                              | El menú Inicio consta de nombres de programas y destinos importantes de Windows, como documentos, imágenes y el panel de control. estas sugerencias describen los elementos del menú Inicio, normalmente proporcionando una breve descripción del programa o el destino, así como las tareas principales que los usuarios pueden realizar con él. estas descripciones también se indexan mediante el cuadro de búsqueda del menú Inicio, lo que ayuda a los usuarios a encontrar los programas que necesitan. <br/> ![captura de pantalla de la sugerencia del centro de bienvenida ](images/ctrl-tooltips-and-infotips-image16.png)<br/> En este ejemplo, el recuadro informativo describe lo que los usuarios pueden hacer con un programa en el menú Inicio.<br/>                                                                                    |
| **Panel de control recuadros informativos**<br/> describir una categoría o tarea del panel de control. <br/>                                    | Estas sugerencias proporcionan información adicional para ayudar a los usuarios a elegir la categoría y el elemento del panel de control correctos. <br/> ![captura de pantalla de la categoría cuentas de usuario con el recuadro informativo ](images/ctrl-tooltips-and-infotips-image17.png)<br/> En este ejemplo, el recuadro informativo describe la categoría del panel de control cuentas de usuario.<br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| **Nombre completo recuadros informativos**<br/> muestra el nombre completo de un elemento cuando el nombre se trunca o no es totalmente visible. <br/> | Estas sugerencias permiten mostrar elementos en un espacio más compacto, a la vez que se reduce la necesidad de desplazamiento horizontal. Esto es especialmente importante cuando la longitud del contenido es desconocida porque es dinámica. a diferencia de otros patrones, cuando se usan en listas y árboles, estas sugerencias se muestran directamente sobre el objeto de origen. <br/> ![captura de pantalla del grupo de botones de radio: recuadro informativo ](images/ctrl-tooltips-and-infotips-image18.png)<br/> En este ejemplo, se usa un recuadro informativo para mostrar el nombre completo del elemento al mantener el mouse.<br/>                                                                                                                                                                                     |
| **Recuadros informativos de estado**<br/> muestra información de estado de los iconos del área de notificación. <br/>                              | Normalmente, las sugerencias deben ser estáticas porque los usuarios no esperan que cambien de una instancia a la siguiente. los **iconos del área de notificación son una excepción** porque estos iconos comunican el estado y no hay ningún otro espacio de pantalla disponible para el texto de estado. <br/> ![captura de pantalla de la sugerencia de ' Messenger sin iniciar sesión ' ](images/ctrl-tooltips-and-infotips-image19.png)<br/> ![captura de pantalla de la sugerencia de ' Messenger con sesión iniciada ' ](images/ctrl-tooltips-and-infotips-image20.png)<br/> En estos ejemplos, recuadros informativos proporciona información de estado para los iconos del área de notificación.<br/>                                                                                                                                  |



 

## <a name="guidelines"></a>Directrices

### <a name="timeouts"></a>Tiempos de espera

-   **Use los tiempos de espera predeterminados iniciales y de visualización. Excepcional**
    -   Las miniaturas que no son redundantes y se muestran en el lado de su objeto asociado se pueden mostrar inmediatamente (sin ningún retraso). Sin embargo, use el tiempo de espera inicial predeterminado para las miniaturas redundantes (por ejemplo, una sugerencia de miniatura grande para un objeto gráfico pequeño) o las miniaturas que cubren su objeto asociado.
-   **Para información sobre herramientas, use el tiempo de espera predeterminado de la eliminación de la sugerencia de cinco segundos.**
-   **En el caso de recuadros informativos, desactive el tiempo de espera de eliminación de propinas. Desarrolladores:** dado que técnicamente no puede desactivar el tiempo de espera de eliminación, establézcalo en su valor mayor.
-   Para obtener accesibilidad, si tiene que establecer los valores de tiempo de espera en un valor distinto del valor máximo, haga que sean múltiplos de los \_ parámetros del sistema SPI GETMOUSEHOVERTIME y SPI \_ GETMESSAGEDURATION en lugar de usar tiempos fijos. Al hacerlo, se ajustan los tiempos de espera a la velocidad del usuario.

### <a name="placement"></a>Ubicación

-   **Evite abarcar el objeto con el que el usuario está a punto de ver o interactuar.** Coloque siempre la sugerencia en el lateral del objeto, incluso si esto requiere una separación entre el puntero y la punta. Cierta separación no supone un problema, siempre y cuando la relación entre el objeto y su sugerencia esté clara.

    -   **Excepción:** Información sobre herramientas de nombre completo utilizada en listas y árboles.

    **Incorrecto:**

    ![captura de pantalla del cuadro de búsqueda de ocultación informativa ](images/ctrl-tooltips-and-infotips-image21.png)

    **Correcto:**

    ![captura de pantalla de un cuadro informativo situado debajo del cuadro de búsqueda ](images/ctrl-tooltips-and-infotips-image22.png)

    En el ejemplo correcto, el recuadro informativo se coloca fuera del cuadro de búsqueda, aunque esto requiere espacio entre él y el símbolo de intercalación.

    **Incorrecto:**

    ![captura de pantalla de texto retocado oculto ](images/ctrl-tooltips-and-infotips-image23.png)

    **Correcto:**

    ![captura de pantalla de un recuadro informativo colocado sobre el texto revisado ](images/ctrl-tooltips-and-infotips-image24.png)

    En el ejemplo correcto, el texto subyacente es mucho más útil que la sugerencia, por lo que el recuadro informativo se coloca bien.

-   **En el caso de las colecciones de elementos, evite abarcar el siguiente objeto con el que es probable que el usuario vea o interactúe.** En el caso de los elementos dispuestos horizontalmente, evite colocar sugerencias a la derecha; para los elementos organizados verticalmente, evite colocar sugerencias a continuación.

    **Incorrecto:**

    ![captura de pantalla de la lista de elementos recientes de ocultación informativa ](images/ctrl-tooltips-and-infotips-image25.png)

    **Correcto:**

    ![captura de pantalla de la lista de recuadro informativo junto a elementos recientes ](images/ctrl-tooltips-and-infotips-image26.png)

    En el ejemplo incorrecto, la sugerencia cubre el objeto con el que es más probable que el usuario interactúe con el siguiente.

-   **En el caso de sugerencias (a menudo grandes), asegúrese de que la información es útil para la mayoría de los usuarios.** Si no es el caso, puede hacer que las sugerencias distraigan sean opcionales o incluso eliminarlas. De lo contrario, la mayoría de los usuarios tendrán que desplazar el puntero fuera del objeto de destino para deshacerse de la sugerencia.

### <a name="tooltips"></a>Información sobre herramientas

-   **Use la información sobre herramientas para proporcionar etiquetas para controles sin etiquetar.** Los controles que suelen tener información sobre herramientas son botones de la [barra de herramientas](cmd-toolbars.md), botones gráficos y [controles de divulgación progresiva](ctrl-progressive-disclosure-controls.md). Los controles con mensajes se consideran etiquetados, como [cuadros de texto](ctrl-text-boxes.md) y [cuadros combinados](/windows/desktop/uxguide/ctrl-drop). Todos los demás controles deben tener etiquetas explícitas.
-   Use fragmentos de oraciones sin puntuación final.
-   Use mayúsculas de estilo de frase.
    -   **Excepción:** Esta directriz es nueva para Windows Vista. En el caso de las aplicaciones heredadas, puede utilizar el uso de mayúsculas de estilo de título si es necesario para evitar la combinación de estilos de capitalización.
-   Agregue un [botón de puntos suspensivos](ctrl-command-buttons.md) si la etiqueta es para un comando que necesita información adicional.
-   Al igual que con las etiquetas normales, **mantener la información sobre herramientas** suele ser de cinco palabras o menos, pero prefiere etiquetas específicas sobre las imprecisas.

    **Aceptable:**

    ![captura de pantalla de la información sobre herramientas de impresión ](images/ctrl-tooltips-and-infotips-image27.png)

    **Manera**

    ![captura de pantalla de la información sobre herramientas "imprimir en impresora predeterminada" ](images/ctrl-tooltips-and-infotips-image28.png)

    **Rendimiento**

    ![captura de pantalla de la información sobre herramientas ' imprimir (escritor de documentos) ' ](images/ctrl-tooltips-and-infotips-image29.png)

    **Incorrecto:**

    ![captura de pantalla de la información sobre herramientas detallada ](images/ctrl-tooltips-and-infotips-image30.png)

    En estos ejemplos, el mejor ejemplo es conciso y específico, mientras que el ejemplo incorrecto es innecesariamente detallado.

-   **La información sobre herramientas también puede proporcionar más información sobre los botones de la barra de herramientas con etiqueta si es útil hacerlo.** No basta con repetir o dar una redefinición de la palabra de lo que ya está en la etiqueta.

    **Correcto:**

    ![captura de pantalla de la información sobre herramientas "buscar todo Outlook" ](images/ctrl-tooltips-and-infotips-image31.png)

    En este ejemplo, la información sobre herramientas explica qué hace la búsqueda.

    **Incorrecto:**

    ![captura de pantalla de la etiqueta del botón repetitivo de la información sobre herramientas ](images/ctrl-tooltips-and-infotips-image32.png)

    En este ejemplo, la información sobre herramientas simplemente repite lo que ya está en la etiqueta.

-   **No tiene que proporcionar información sobre herramientas de controles etiquetados simplemente para garantizar la coherencia.**

    ![captura de pantalla de los botones con etiqueta y sin etiquetar ](images/ctrl-tooltips-and-infotips-image33.png)

    En este ejemplo, los botones de la barra de herramientas sin etiqueta tienen información sobre herramientas, pero las etiquetas no lo tienen.

-   Siempre que sea necesario, haga que la **información sobre herramientas sea más útil proporcionando métodos abreviados de teclado y valores predeterminados.** Coloque esta información adicional entre paréntesis. Esto hace que la información sobre herramientas resulte útil para los controles etiquetados, incluso si, de lo contrario, solo se repite la etiqueta. No tenga en cuenta este texto adicional al evaluar la conciso de una información sobre herramientas.

    ![captura de pantalla de la información sobre herramientas ' imprimir (escritor de documentos) ' ](images/ctrl-tooltips-and-infotips-image29.png)

    En este ejemplo, Word muestra los valores predeterminados y los métodos abreviados de teclado en la información sobre herramientas de la barra de herramientas.

### <a name="infotips"></a>Recuadros informativos

-   **En el caso de recuadros informativos en lugares no estándar, favorece la coherencia con respecto a la utilidad para mejorar la detectabilidad.** Proporcione sugerencias para todos los objetos en los que es probable que los usuarios deseen obtener información complementaria, aunque algunos recuadros informativos sean obvios. De este modo, se evita que los usuarios esperen a que un recuadro informativo no vaya nunca.
    -   **Excepción:** Si solo unos pocos objetos tienen recuadros informativos útiles, no use recuadros informativos en absoluto. En su lugar, use etiquetas de control autoexplicativas o texto complementario en contexto.
-   Use oraciones completas con puntuación final.
    -   **Excepción:** El icono del área de notificación [recuadros informativos](winenv-notification.md) no usa la puntuación final.
-   Use mayúsculas de estilo de frase.
-   Usar el plazo presente, no el futuro.
-   Usar construcciones gramaticales en paralelo. El paralelismo requiere que las palabras y frases que tienen la misma función tengan el mismo formato.
    -   **Excepción:** En el caso del patrón de recuadro informativo de nombre completo, el texto del recuadro informativo coincide exactamente con las frases, las mayúsculas y los signos de puntuación del control subyacente.
-   **Evite recuadros informativos grandes.** Los recuadros informativos grandes son difíciles de leer y difíciles de colocar sin interferir con el objeto subyacente.
-   **Dé formato a recuadros informativos para facilitar la lectura y el análisis de su contenido.** Los bloques grandes de texto sin formato pueden ser difíciles de leer.

    **Incorrecto:**

    ![captura de pantalla de la información sobre herramientas larga, no estructurada y en ejecución ](images/ctrl-tooltips-and-infotips-image34.png)

    **Correcto:**

    ![captura de pantalla de la misma información sobre herramientas con una línea por elemento ](images/ctrl-tooltips-and-infotips-image35.png)

    En el ejemplo correcto, el texto con formato es mucho más fácil de leer y examinar.

-   Al usarse por primera vez dentro de un recuadro informativo, escriba los nombres de los acrónimos seguidos del acrónimo entre paréntesis. Ejemplo: "Protocolo de configuración dinámica de host (DHCP)".

### <a name="start-menu-infotips"></a>Menú Inicio recuadros informativos

-   Use el menú Inicio recuadros informativos para **describir el elemento de manera concisa y mostrar las tareas principales que los usuarios pueden realizar con el elemento.**
-   **Ser útil.** Céntrese en lo que los usuarios pueden hacer. No basta con repetir el nombre del elemento o incluso usarlo en la descripción.
-   **Ser específico.** Evite verbos genéricos y expresiones catch-all como y otras tareas. Si la información es importante, lista concretamente; en caso contrario, supongamos que los usuarios saben que no todo se muestra en el recuadros informativos.
-   **Sea conciso.** Use 25 palabras o menos. Recuadros informativos de lectura más larga.
-   **Comience con un verbo imperativo presente,** como crear, editar, mostrar y enviar. Prefiere verbos específicos sobre verbos genéricos, como administrar y abrir, que realmente se aplican a la mayoría de los elementos del menú Inicio. Ir directamente al punto.

    **Incorrecto:**

    ![captura de pantalla de la información sobre herramientas: abre la carpeta música ](images/ctrl-tooltips-and-infotips-image36.png)

    **Manera**

    ![captura de pantalla de la información sobre herramientas: almacenar y reproducir música ](images/ctrl-tooltips-and-infotips-image37.png)

    En el ejemplo incorrecto, el recuadro informativo comienza con un verbo genérico. El mejor ejemplo se obtiene directamente al punto con verbos específicos, pero continúa usando la frase innecesaria "y otra" al final de la sugerencia.

-   **No use el lenguaje que suene como marketing.**

    **Incorrecto:**

    ![captura de pantalla del recuadro informativo "un punto de inicio único" ](images/ctrl-tooltips-and-infotips-image38.png)

    En este ejemplo, el recuadro informativo suena como marketing.

-   Dado que estos recuadros informativos se indizan para el cuadro de búsqueda del menú Inicio, **describa las tareas importantes del programa con los términos para los que los usuarios tienen más probabilidades de buscar. Considere la posibilidad de usar palabras clave y sinónimos comunes.**

    **Incorrecto:**

    ![captura de pantalla de la información sobre herramientas: creación de DVDs ](images/ctrl-tooltips-and-infotips-image39.png)

    **Correcto:**

    ![captura de pantalla de la información sobre herramientas: creación (grabación) de CDs, DVDs ](images/ctrl-tooltips-and-infotips-image40.png)

    En el ejemplo correcto, el recuadro informativo tiene sinónimos comunes.

-   Use mayúsculas de estilo de frase.
-   **Desarrolladores:** El texto del recuadro informativo del menú Inicio proviene del campo Comentario del elemento.

### <a name="quick-launch-tooltips"></a>Información sobre herramientas de inicio rápido

-   **Use una información sobre herramientas con el formato:** Iniciar (nombre completo del programa)
-   No uses puntuación final.
-   No use texto adicional para describir el programa o lo que hace. Dado que los usuarios eligen los programas mostrados en la barra de inicio rápido, ya saben su propósito.

### <a name="control-panel-infotips"></a>Panel de control recuadros informativos

-   Use el panel de control recuadros informativos para **describir de manera concisa las tareas del panel de control y el hardware y software configurados.**
-   **Los iconos y los nombres del panel de control deben tener recuadros informativos.** Las tareas individuales no tienen información sobre herramientas.
-   **Ser útil.** Céntrese en lo que los usuarios pueden hacer. No basta con repetir el nombre del elemento del panel de control o incluso usarlo en la descripción.
-   **Ser específico.** Evite verbos genéricos y expresiones catch-all como y otro hardware. Si la información es importante, lista concretamente; en caso contrario, supongamos que los usuarios saben que no todo se muestra en el recuadros informativos.

    **Incorrecto:**

    ![captura de pantalla de la información sobre herramientas: configura el mouse ](images/ctrl-tooltips-and-infotips-image41.png)

    **Correcto:**

    ![captura de pantalla de la información sobre herramientas detallada para la configuración del mouse ](images/ctrl-tooltips-and-infotips-image42.png)

    En el ejemplo correcto, se enumeran los tipos de hardware configurados de forma específica.

-   **Sea conciso.** Use 25 palabras o menos. Recuadros informativos de lectura más larga.
-   **Comience con un verbo imperativo presente.**

    **Correcto:**

    Configurar opciones de conexión y visualización de Internet.

    Ajuste la configuración de visión, audición y movilidad.

-   **Ir directamente al punto.** No use el lenguaje que se aplica a ningún panel de control, como "usar para ver y configurar las opciones de la apariencia y la funcionalidad de su..." o "proporciona opciones para..."
-   No use el lenguaje que suene como marketing.

    **Incorrecto:**

    El punto de inicio único para todas las necesidades de configuración de disco.

-   Dado que estos recuadros informativos se indizan para el cuadro de búsqueda del panel de control, **describa los elementos mediante términos para los que los usuarios tienen más probabilidades de buscar.** Considere la posibilidad de usar sinónimos comunes para tareas y objetos populares.

    ![captura de pantalla de la información sobre herramientas con tareas de controlador de juego ](images/ctrl-tooltips-and-infotips-image43.png)

    En este ejemplo, el elemento se describe mediante los términos para los que los usuarios tienen más probabilidades de buscar.

-   Si es probable que un elemento del panel de control se confunda con otros, explique cómo es diferente en el recuadro informativo.

    **Incorrecto:**

    ![captura de pantalla de recuadro informativo que carece de detalles específicos ](images/ctrl-tooltips-and-infotips-image44.png)

    En este ejemplo, los dos elementos del panel de control configuran el sonido, pero el recuadro informativo no clarifica la diferencia.

    **Correcto:**

    ![captura de pantalla de recuadro informativo con detalles específicos ](images/ctrl-tooltips-and-infotips-image45.png)

    En este ejemplo, la diferencia entre los dos elementos es más evidente debido a la sugerencia.

### <a name="icons"></a>Iconos

A diferencia de las versiones anteriores de Windows, Windows Vista permite sugerencias para tener iconos.

-   Para información sobre herramientas, no use iconos.
-   En el caso de recuadros informativos, use iconos solo si ayudan en el reconocimiento o la comprensión, o si proporcionan contexto. La mayoría de los recuadros informativos no deben tener iconos.

    ![captura de pantalla del icono de recuadro informativo de volumen con auriculares ](images/ctrl-tooltips-and-infotips-image46.png)

    En este ejemplo, el recuadro informativo tiene un icono para ayudar a asociar el icono a su significado.

-   El icono debe usar el [estilo Aero](vis-icons.md) y tener una apariencia discreta.

Para obtener instrucciones y ejemplos de iconos generales, vea [iconos](vis-icons.md).

## <a name="documentation"></a>Documentación

Al hacer referencia a las sugerencias:

-   En programación y otra documentación técnica, consulte el tipo de sugerencia (información sobre herramientas o recuadro informativo). En cualquier otro lugar, simplemente llámelo como una sugerencia.
-   Las siguientes variaciones son incorrectas: información sobre herramientas, información sobre herramientas e información sobre herramientas.
-   Para describir la interacción del usuario, use el puntero del mouse.

