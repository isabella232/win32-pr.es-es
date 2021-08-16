---
title: Paneles de control
description: Use elementos del panel de control para ayudar a los usuarios a configurar características de nivel de sistema y realizar tareas relacionadas. En su lugar, los programas que tienen una interfaz de usuario deben configurarse directamente desde su interfaz de usuario.
ms.assetid: 845325ef-9f1d-4aa7-a5b0-685fac74a9f8
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 86226e3643f741d277c0e2864870a7e81c25614a6dd5ba2e01a05c67729c26d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117853552"
---
# <a name="control-panels"></a>Paneles de control

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

Use elementos del panel de control para ayudar a los usuarios a configurar características de nivel de sistema y realizar tareas relacionadas. En su lugar, los programas que tienen una interfaz de usuario deben configurarse directamente desde su interfaz de usuario.

Con Panel de control en Microsoft Windows, los usuarios pueden configurar características de nivel de sistema y realizar tareas relacionadas. Entre los ejemplos de configuración de características de nivel de sistema se incluyen la configuración y configuración de hardware y software, la seguridad, el mantenimiento del sistema y la administración de cuentas de usuario.

El término Panel de control hace referencia a toda la Windows Panel de control característica. Los paneles de control individuales se conocen como elementos del panel de control. Un elemento del panel de control se considera de nivel superior cuando es accesible directamente desde la página principal del panel de control o desde una página de categoría.

![captura de pantalla de la categoría de voz del panel de control ](images/winenv-ctrl-panels-image1.png)

Elemento típico del panel de control.

La página principal del panel de control es el punto de entrada principal de todos los elementos del panel de control. Enumera los elementos por categoría, junto con las tareas más comunes. Se muestra cuando los usuarios hacen clic Panel de control en el menú Inicio.

Una página de categoría del panel de control enumera los elementos dentro de una sola categoría, junto con las tareas más comunes. Se muestra cuando los usuarios hacen clic en un nombre de categoría en la página principal.

Los elementos del panel de control se implementan mediante flujos [de tareas o](glossary.md) hojas de propiedades. Para Windows Vista y versiones posteriores, los flujos de tareas son la interfaz de usuario (UI) preferida.

**Desarrolladores:** Para obtener información sobre cómo crear elementos del panel de control, [vea Panel de control Items](/previous-versions//bb776838(v=vs.85)).

**Nota:** Las directrices relacionadas [con las hojas de](win-property-win.md) propiedades se presentan en un artículo independiente.

## <a name="is-this-the-right-user-interface"></a>¿Es la interfaz de usuario adecuada?

Para decidirte, intenta responder a estas preguntas:

-   **¿El propósito es configurar características de nivel de sistema?** Si no es así, use otro punto de integración. Haga que las características de la aplicación se configurablen directamente desde la interfaz de usuario mediante cuadros de diálogo de opciones, en lugar de usar Panel de control. En el caso de las utilidades que no se usan para la instalación, la configuración o las tareas relacionadas (como la solución de problemas), use el menú Inicio como punto de integración.
-   **¿La característica de nivel de sistema tiene su propia interfaz de usuario?** Si es así, esa interfaz de usuario es donde los usuarios deben ir para realizar cambios. Por ejemplo, una utilidad de copia de seguridad del sistema debe configurarse a partir de sus opciones de programa en lugar de Panel de control.
-   **¿Necesitarán los usuarios cambiar la configuración con frecuencia?** Si es así (por ejemplo, varias veces a la semana), considere soluciones alternativas, quizás además de usar Panel de control. Por ejemplo, la Windows de volumen maestro se puede configurar directamente desde su icono en el área de notificación. Algunas opciones se pueden configurar automáticamente. En Windows Explorer, por ejemplo, la pestaña Compatibilidad para las propiedades de la aplicación permite que una aplicación se ejecute en modo de color 256 en lugar de requerir a los usuarios que cambien el modo de vídeo manualmente.
-   **¿Son los usuarios de destino profesionales de IT?** Si es así, use un [complemento Microsoft Management Console (MMC)](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) en su lugar, que está diseñado específicamente para las tareas de administración del sistema. En algunos casos, la mejor solución es tener un elemento de panel de control para usuarios generales y un complemento MMC para profesionales de TI.

    ![captura de pantalla de la ventana de administración de equipos ](images/winenv-ctrl-panels-image2.png)

    En este ejemplo, el complemento MMC Usuarios y grupos locales proporciona administración de usuarios dirigida a profesionales de IT. Es más probable que otros usuarios usen el elemento Cuentas de usuario en Panel de control.

-   **¿La característica es una característica de OEM que solo se usa durante la configuración inicial del sistema?** Si es así, use el Windows Centro de bienvenida como punto de integración.

Los elementos del panel de control son necesarios porque muchas características de nivel de sistema no tienen un punto de integración más obvio o directo. Sin Panel de control no se debería ver como el "único lugar" para todas las opciones de configuración. **Los programas que tienen una interfaz de usuario deben configurarse directamente desde su interfaz de usuario en lugar de usar elementos del panel de control.**

**Incorrecto:**

![captura de pantalla del elemento de opciones de Internet del panel de control ](images/winenv-ctrl-panels-image3.png)

En este ejemplo, Windows Internet Explorer debe representarse en Panel de control, porque su propia interfaz de usuario es un mejor punto de integración.

### <a name="create-a-new-control-panel-item-or-extend-an-existing-one"></a>¿Cree un nuevo elemento del panel de control o extienda uno existente?

Para decidirte, intenta responder a estas preguntas:

-   **¿Se puede expresar la funcionalidad como tareas que se pueden conectar a un elemento del panel de control extensible existente?** Los siguientes elementos del panel de control son extensibles: Bluetooth Dispositivos, Pantalla, Internet, Teclado, Mouse, Red, Energía, Sistema, Inalámbrico (infiel).
-   **¿Las propiedades y las tareas reemplazan las características del elemento del panel de control extensible existente?** Si es así, debe extender el elemento del panel de control existente, ya que esto da como resultado una experiencia de usuario más sencilla. Si no es así, cree un nuevo elemento del panel de control.

## <a name="design-concepts"></a>Conceptos de diseño

**El Panel de control se basa en una metáfora del mundo real.** Un panel de control real es una colección de controles (botones, conmutadores, medidores y pantallas) que se usan para supervisar y controlar un dispositivo. Los usuarios de estos paneles de control a menudo necesitan entrenamiento para entender cómo usarlos.

A diferencia de sus homólogos del mundo real, **Windows diseños del panel de control están optimizados para los usuarios por primera vez.** Los usuarios no realizan la mayoría de las tareas del panel de control con mucha frecuencia, por lo que normalmente no recuerda cómo hacerlos y, de hecho, tienen que volver a aprenderlas cada vez.

Para diseñar un elemento del panel de control que sea útil y fácil de usar:

-   Asegúrese de que las propiedades son necesarias.
-   Presentar propiedades en términos de objetivos de usuario en lugar de tecnología.
-   Presentar propiedades en el nivel correcto.
-   Páginas de diseño para tareas específicas.
-   Páginas de diseño para usuarios estándar y administradores protegidos.

Al diseñar y evaluar elementos que se incluirán en Panel de control, determine las tareas comunes que realizan los usuarios y asegúrese de que hay una ruta de acceso clara para realizar esas tareas. Normalmente, los usuarios realizan los siguientes tipos de tareas con elementos del panel de control:

-   Configuración inicial
-   Cambios poco frecuentes (para la mayoría de la configuración)
-   Cambios frecuentes (para algunas configuraciones importantes)
-   Revertir la configuración a un estado inicial o anterior
-   Solución de problemas

**Si solo hace una cosa...**

Diseñar páginas del panel de control para tareas específicas y presentarlas en términos de objetivos de usuario en lugar de tecnología.

## <a name="usage-patterns"></a>Patrones de uso

Para los elementos del panel de control, puede usar un flujo de tareas o una hoja de propiedades. Estos son sus patrones de uso:

### <a name="task-flow-patterns"></a>Patrones de flujo de tareas

Los elementos de flujo de tareas usan una página central para presentar las opciones de alto nivel y las páginas de radio para realizar la configuración real.

**Páginas centrales**

-   Páginas centrales basadas en tareas. Estas páginas centrales presentan las tareas más usadas. Se usan mejor para algunas tareas de uso frecuente o importantes en las que los usuarios necesitan más instrucciones y explicaciones. Las páginas centrales no tienen botones de confirmación. Las páginas centrales basadas en tareas híbridas también tienen algunas propiedades o comandos directamente en ellas. Las páginas del centro híbrido se recomiendan encarecidamente cuando es más probable que los usuarios usen Panel de control acceso a esas propiedades y comandos.
-   Páginas centrales basadas en objetos. Estas páginas centrales presentan los objetos disponibles mediante un control de vista de lista. Se usan mejor cuando podría haber varios objetos. Las páginas centrales no tienen botones de confirmación.

**Páginas de radio**

-   Páginas de tareas. Estas páginas de radio presentan una tarea o un paso en una tarea con una instrucción principal específica basada en tareas. Se usan mejor para tareas que se benefician de instrucciones y explicaciones adicionales.
-   Páginas de formulario. Estas páginas de radio presentan una colección de propiedades y tareas relacionadas basadas en una instrucción principal general. Se usan mejor para las características que tienen muchas propiedades y se benefician de una presentación directa de una sola página, como las propiedades avanzadas.

### <a name="property-sheet-patterns"></a>Patrones de hoja de propiedades

-   Las hojas de propiedades se usan mejor en elementos heredados con muchas configuraciones dirigidas a usuarios avanzados. Los nuevos elementos pueden lograr el mismo efecto con un flujo de tareas mediante el patrón de página del formulario.

## <a name="guidelines"></a>Directrices

### <a name="property-sheet-control-panel-items"></a>Elementos del panel de control de hoja de propiedades

-   **No use hojas de propiedades para los nuevos elementos del panel de control.** En su lugar, use flujos de tareas para crear una experiencia sin problemas y hacer un uso completo de la funcionalidad de categorización y búsqueda de la página principal del panel de control.

### <a name="task-flow-control-panel-items"></a>Elementos del panel de control de flujo de tareas

**General**

-   **Mantenga visible el contenido y los controles más importantes sin desplazarse.** Los usuarios no se desplazarán para ver el contenido de la página a menos que tengan una razón para hacerlo. Puede hacer que los botones de confirmación siempre sean visibles si los coloca en un [área de comandos](glossary.md) en lugar del área de contenido. No rompa las páginas solo para evitar el desplazamiento.
    -   **Puede desplazarse verticalmente por páginas largas,** siempre y cuando los controles más importantes estén visibles sin desplazarse.
    -   **No use el desplazamiento horizontal.** En su lugar, rediseñar el contenido de la página y usar el desplazamiento vertical. Las páginas pueden tener barras de desplazamiento horizontales solo cuando se hacen muy estrechas.
-   **Para navegar entre páginas:**
    -   Use [vínculos de tarea](glossary.md) para iniciar una tarea.
    -   Use vínculos de tarea o un botón Siguiente para ir a la página siguiente de una tarea de varios pasos.
    -   Use botones de confirmación para completar una tarea.
    -   Use el botón Atrás en la barra de menús para volver a las páginas vistas previamente. No agregue una botón Atrás al área de comandos.
    -   Use la barra de direcciones para volver directamente a la página principal del panel de control.
    -   Use Ver también vínculos en el panel de tareas para navegar a las páginas de otros elementos del panel de control. De lo contrario, la navegación debe permanecer dentro de un único elemento del panel de control.
-   **Coloque solo la página principal del panel de control en la barra de direcciones.** Al hacer clic en ese vínculo, vuelve a la página principal del panel de control, abandonando cualquier trabajo en curso sin una [confirmación](https://msdn.microsoft.com/library/windows/desktop/aa511273.aspx).
-   **No coloque un botón de comando Cerrar en las páginas del panel de control.** Los usuarios pueden cerrar una ventana del panel de control mediante el botón Cerrar de la barra de título.

**Botones y vínculos de tareas**

-   **Cuando una página tiene un pequeño conjunto de opciones fijas, use vínculos de tarea en lugar de una combinación de botones de radio y un botón Siguiente.** Esto permite a los usuarios seleccionar una respuesta con un solo clic.
-   Puede colocar botones y vínculos de tareas en los siguientes lugares (en orden de detectabilidad):
    -   El [área de comandos](glossary.md) (solo para botones de comando en páginas de radio).
    -   El [área de contenido](glossary.md):
        -   Botones de comando
        -   Vínculos de tareas
        -   Otros vínculos
    -   Vínculos en el [panel de tareas](glossary.md) (solo páginas centrales).
-   **Base la ubicación de los vínculos y botones de tareas en función de la importancia y la necesidad de detectabilidad.**
    -   **Coloque solo los botones de confirmación en el área de comandos.**
    -   **Coloque tareas esenciales en el área de contenido.** Los botones de comando tienden a llamar más la atención, por lo que se reservan para los comandos que los usuarios deben ver. Los vínculos de tareas también llama la atención, pero menos que los botones de comando.
    -   **Reserve el panel de tareas y los vínculos sin formato para las tareas secundarias (menos importantes).** El panel de tareas es el área menos reconocible de una página de tareas y los vínculos sin formato no son tan visibles como los botones de comando y los vínculos de tareas.
-   Para los vínculos de tareas que se presentan en el área de contenido:
    -   **Si hay más de siete vínculos, a agrupar los vínculos en categorías.** Proporcione encabezados para cada uno de los grupos.
    -   **Para menos de siete vínculos, presente los vínculos en un único grupo sin un encabezado.**
-   **Presentar vínculos y botones de tareas en un orden lógico.** Mostrar vínculos de tareas verticalmente, botones de comando horizontalmente.
-   Dentro de las **categorías, divida los comandos en grupos relacionados.** Presente los grupos de tareas colocando primero el más usado y, dentro de cada grupo, coloque primero las tareas más usadas. **El orden resultante debe seguir aproximadamente la probabilidad de uso, pero también tener un flujo lógico.**
    -   **Excepción:** Los vínculos de tareas que hacen que todo se haga primero deben colocarse en primer lugar.
-   **Si hay muchos vínculos** de tareas, dé a las tareas más importantes una apariencia más destacada mediante un icono de 24 x 24 píxeles y dos líneas de texto. Para las tareas menos importantes, use un icono de 16 x 16 píxeles, o ningún icono, y una sola línea de texto de vínculo.

    ![captura de pantalla de elementos con iconos grandes y pequeños ](images/winenv-ctrl-panels-image4.png)

    En este ejemplo, los comandos importantes tienen una apariencia más destacada.

-   **Tener una separación física clara entre los comandos usados con frecuencia y los comandos destructivos.** De lo contrario, los usuarios podrían hacer clic en comandos destructivos accidentalmente. Es posible que tenga que reordenar los comandos un poco para colocar comandos destructivos juntos.
-   **Proporcione el mecanismo para deshacer comandos directamente en la página.** Los usuarios no deben tener que navegar a otro lugar para deshacer un error.
-   **Para los vínculos de tareas, use todos los iconos de vínculo de tareas predeterminados o todos los iconos personalizados.** No los mezcle. Considere la posibilidad de usar iconos personalizados solo si:
    -   Ayudan a los usuarios a comprender las tareas.
    -   Cumplen con los estándares [de icono de Avión.](vis-icons.md)
    -   Tienen una apariencia discreta.

**Cuadros de diálogo**

Cuando se usan flujos de tareas, normalmente se quiere que una tarea fluya de página a página dentro de una sola ventana, pero las siguientes circunstancias son excepciones. Use cuadros de diálogo en las siguientes circunstancias:

-   Para solicitar a los usuarios un nombre de usuario y una contraseña de administrador. Use siempre el cuadro de diálogo Administrador de credenciales para este propósito. (Debe ser [modal).](glossary.md)
-   Para confirmar un comando local mediante un cuadro de diálogo de tarea o un cuadro de mensaje. (Debe ser modal).
-   Para obtener la entrada de los comandos locales, como para los comandos Nuevo, Agregar, Guardar como, Cambiar nombre e Imprimir.

    ![captura de pantalla del cuadro de diálogo Eliminar ubicaciones de red ](images/winenv-ctrl-panels-image5.png)

    En este ejemplo, el comando Eliminar se realiza en un cuadro de diálogo en lugar de en una página independiente.

-   Para realizar tareas secundarias independientes. Con una [ventana modeless](glossary.md), la ventana secundaria permite que estas tareas se realicen de forma independiente y fuera del flujo de tareas principal.

### <a name="hub-pages"></a>Páginas centrales

**General**

-   Use páginas centrales basadas en tareas cuando:
    -   **Hay un pequeño número de tareas de uso frecuente o importantes.**
    -   **La configuración implica uno o dos objetos** (ejemplos: monitores, teclado, mouse y controladores de juegos).
    -   **La configuración se aplica a todo el sistema** (ejemplos: fecha y hora, seguridad, opciones de energía).
-   Use páginas centrales basadas en objetos cuando:
    -   **La configuración podría implicar varios objetos** (ejemplos: cuentas de usuario, conexiones de red, impresoras).
    -   **La configuración solo se aplica al objeto seleccionado.**
-   **No use una página central si el** elemento del panel de control tiene una sola página que contiene todas las tareas y propiedades implicadas.

**Listas de objetos**

-   **Enumera los elementos en un orden lógico.** Ordene los objetos con nombre en orden alfabético, números en orden numérico y fechas en orden cronológico.
-   En el caso de los concentradores basados en objetos, proporcione comandos de vista de objetos en el panel de tareas si la capacidad de cambiar la vista es **importante para las tareas**. La capacidad de cambiar las vistas es importante si hay muchos objetos y la presentación predeterminada no funciona bien en todos los escenarios. Los usuarios pueden cambiar la vista de lista incluso si no hay comandos explícitos a través del menú contextual de la vista de lista, pero es menos reconocible.

Para obtener más instrucciones sobre cómo presentar listas de objetos, vea [List Views](ctrl-list-views.md).

**Interacción**

-   **No coloque botones de confirmación en las páginas centrales.** Las páginas centrales son fundamentalmente puntos de inicio. Los usuarios nunca "confirman" las páginas del centro que nunca han terminado con ellas. Y los botones de confirmación de las páginas del centro hacen que las tareas iniciadas desde un centro sean confusas (los usuarios se preguntarán si es necesario confirmar esas tareas).
    -   **Excepción:** Si cambiar una configuración requiere [elevación,](glossary.md)proporcione un botón Aplicar con un icono [de escudo de seguridad](winenv-uac.md). Deshabilite el botón de confirmación una vez aplicados los cambios.
-   **Considere la posibilidad de colocar las propiedades más útiles directamente en las páginas centrales.** Estas páginas del centro híbrido se recomiendan encarecidamente cuando es más probable que los usuarios usen Panel de control para acceder a esas propiedades.

    ![captura de pantalla de la página del centro de opciones de energía ](images/winenv-ctrl-panels-image6.png)

    En este ejemplo, el Opciones de energía panel de control tiene la configuración más útil directamente en la página central.

-   **Use un modelo de confirmación inmediata para cualquier configuración en las páginas del centro híbrido para que los cambios se realicen inmediatamente.** De nuevo, los usuarios nunca confirman una página del centro. Si una configuración requiere un botón de confirmación, no lo coloque en una página central.
-   **Considere la posibilidad de colocar comandos sencillos de "un paso" directamente en las páginas centrales en lugar de usar vínculos de navegación.**
-   **Confirme los comandos locales cuyos efectos no se pueden deshacer fácilmente.** Use un cuadro [de diálogo de tarea](win-dialog-box.md) o un cuadro de [mensaje](glossary.md).

    ![captura de pantalla del cuadro de diálogo Confirmar eliminación ](images/winenv-ctrl-panels-image7.png)

    En este ejemplo, el comando Eliminar se confirma con un cuadro de diálogo.

-   **En el caso de las páginas centrales basadas en tareas, identifique cada tarea con un vínculo de tarea y un icono.** También puede proporcionar una descripción opcional para cada vínculo. Sin embargo, intente que los vínculos de tarea se explican por sí mismos y proporcione descripciones opcionales solo a los vínculos que realmente los necesiten.

    ![captura de pantalla de la página del centro de rendimiento del equipo ](images/winenv-ctrl-panels-image8.png)

    En este ejemplo, cada tarea tiene un vínculo de tarea y un icono.

-   **En el caso de las páginas centrales basadas en objetos, al hacer clic único se seleccionan objetos y, al hacer doble clic, se selecciona un objeto y se navega a su página predeterminada.** La página predeterminada suele ser una página de propiedades o una página central basada en tareas.
-   **Una página central basada en objetos puede navegar a un centro basado en tareas para los objetos seleccionados.** Sin embargo, estos concentradores secundarios deben evitarse porque hacen que un elemento del panel de control se sienta demasiado indirecto.

**Paneles de tareas**

Use paneles de tareas para presentar vínculos a comandos, vistas y elementos relacionados del panel de control.

-   En el caso de los paneles de tareas en centros basados en tareas, presente vínculos en el orden siguiente:
    -   **Comandos secundarios**. Presente las tareas principales solo en el área de contenido. Use el panel de tareas para tareas secundarias opcionales. Considere una tarea principal si los usuarios deben detectarla en escenarios importantes. secundaria si es aceptable que los usuarios no lo detecte.
    -   **Vea también**. Vínculos opcionales que navegan a los elementos relacionados del panel de control.
-   En el caso de los paneles de tareas en centros basados en objetos, presente vínculos en el orden siguiente:
    -   **Vistas de objeto**. Vínculos opcionales que se usan para controlar la presentación de los objetos.
    -   **Se han corregido los comandos**. Comandos que son independientes de los objetos seleccionados actualmente.
    -   **Comandos contextuales**. Los comandos que dependen de los objetos seleccionados actualmente y, por tanto, no siempre se muestran.
    -   **Vea también**. Vínculos opcionales que navegan a los elementos relacionados del panel de control.
-   **No use paneles de tareas en páginas de radio.** A diferencia de las páginas de concentrador, las páginas de radio deben centrarse en completar la tarea. No quiere animar a los usuarios a salir antes de finalizar.

**Consulte también vínculos**

-   **Proporcionar Vea también vínculos en el panel de tareas para ayudar a los usuarios a encontrar elementos relacionados del panel de control o el elemento del panel de control correcto si tienen uno incorrecto.** Es probable que los usuarios asocie un vínculo a elementos con el elemento del panel de control.

    ![captura de pantalla de centro de actividades vínculos "ver también" ](images/winenv-ctrl-panels-image9.png)

    En este ejemplo, el elemento del panel de control del Centro de acciones se vincula a los elementos relacionados del panel de control.

-   **Vincule a una página de tareas específica si es lo que es más probable que reconozcan los usuarios.** De lo contrario, vincule a todo el elemento del panel de control. Use el nombre del panel de control sin agregar la frase, panel de control.

### <a name="spoke-pages"></a>Páginas de radio

**General**

-   **Use páginas de tareas para tareas de uso frecuente o importantes en las que los usuarios necesiten más instrucciones y explicaciones.**
-   **Use páginas de formulario para las características que tienen muchas configuraciones y se benefician de una presentación directa de una sola página.** Las tareas ideales para estas páginas suelen implicar cambios obvios en algunas propiedades simples.
-   **No use paneles de tareas en páginas de radio.**

**Interacción**

-   **Intente limitar las tareas principales a una sola página.** Si se requiere más de una página, puede:
    -   **Use páginas de radio intermedias para pasos adicionales u opcionales.** Las páginas de radio intermedias se confirman en la página de radio final.
    -   **Use ventanas independientes para tareas auxiliares independientes.** Las ventanas independientes se confirman por sí solas e independientemente de la tarea principal.

Si lo hace, el significado de los botones de confirmación de la tarea principal es claro e inequívovo. Los usuarios siempre deben estar seguros de comprender a qué se comprometen.

-   **No use Consulte también vínculos dentro de un flujo de tareas.** Estos vínculos a elementos relacionados, pero diferentes, del panel de control. Aunque la navegación a un elemento diferente es aceptable en las páginas centrales, no se encuentra en páginas de radio, ya que al hacerlo se interrumpe la tarea.
-   **No use páginas de radio para entradas o confirmaciones simples.** Use cuadros de diálogo modales en su lugar.

**Interacción (páginas de radio intermedias)**

-   **Use vínculos de tarea o un botón Siguiente para ir a la página siguiente.** La manera de continuar con el paso siguiente siempre debe ser obvia.
-   **Puede tener vínculos de navegación a pasos de tareas opcionales.** Para evitar confusiones cuando los usuarios se confirman en la tarea, esas páginas adicionales deben ser páginas intermedias dentro del mismo elemento del panel de control. No deben tener botones de confirmación, pero deben confirmarse cuando se confirma la tarea principal.

**Interacción (páginas de radio final)**

-   **Use botones de confirmación para completar una tarea.** Use un modelo [de](glossary.md) confirmación retrasada para las páginas de radio, de modo que los cambios no se realicen hasta que se confirmen explícitamente (si los usuarios se desplazan fuera mediante Atrás, Cerrar o la barra de direcciones, los cambios se abandonan). Los botones de confirmación son una pista visual de que el usuario está a punto de completar una tarea. No use vínculos para este propósito.
-   **No confirme los botones de confirmación (incluido Cancelar).** Si lo hace, puede ser molesto. Excepciones:
    -   La acción tiene consecuencias significativas y, si es incorrecta, no se puede corregir fácilmente.
    -   La acción puede provocar una pérdida significativa del tiempo o el esfuerzo del usuario.
    -   La acción es claramente incoherente con otras acciones.
-   **No confirme si los usuarios abandonan los cambios;** para ello, vaya hacia atrás, cierre o la barra de direcciones. Sin embargo, puede confirmar si una navegación potencialmente no deseada puede dar lugar a una pérdida significativa del tiempo o el esfuerzo del usuario.
-   **No use vínculos de navegación o comandos** (incluidos los vínculos ver también). En las páginas de radio finales, los usuarios deben completar o cancelar explícitamente la tarea. No se debe animar a los usuarios a navegar por otro lugar, ya que es probable que al hacerlo se cancele la tarea implícitamente.
-   **Cuando los usuarios completen o cancelen una tarea, deben devolverse a la página del centro desde la que se inició la tarea.** Si no hay ninguna página de este tipo, cierre la ventana del panel de control en su lugar. No suponga que las páginas de radio siempre se inician desde otra página.
-   **Quite las páginas obsoletas "confirmados"** de la pila back-stack de Windows Explorer cuando devuelva a los usuarios a la página desde la que se inició la tarea. Los usuarios nunca deben ver las páginas en las que ya se han confirmado al hacer clic en botón Atrás. Los usuarios siempre deben realizar cambios adicionales rehaciendo completamente la tarea en lugar de hacer clic en Atrás para modificar páginas obsoletas.
    -   **Desarrolladores:** Puede quitar estas páginas obsoletas mediante las API ITravelLog::FindTravelEntry() e ITravelLogEx::D eleteEntry().

**Botones de confirmación**

**Nota:** Los botones de cancelación se consideran botones de confirmación.

-   **Confirme las tareas mediante botones de confirmación que son respuestas específicas a la instrucción principal, en lugar de etiquetas genéricas como Aceptar.** Las etiquetas de los botones de confirmación deben tener sentido por sí solas. Evite usar Aceptar porque no es una respuesta específica a la instrucción principal y, por tanto, es más fácil de entender. Además, Ok se usa normalmente con cuadros de diálogo modales e implica cerrar incorrectamente la ventana de elementos del panel de control.
    -   **Excepciones:**
        -   Use Aceptar para las páginas que no tienen configuración.
        -   Use Aceptar cuando la respuesta específica todavía sea genérica, como Guardar, Seleccionar o Elegir, como al cambiar una configuración específica o una colección de valores.
        -   Use Aceptar si la página tiene botones de radio que son respuestas a la instrucción principal. Para mantener el modelo de confirmación retrasada, no puede usar vínculos de tareas en una página de radio final.

            ![captura de pantalla de restricciones web con el botón Aceptar ](images/winenv-ctrl-panels-image10.png)

            En este ejemplo, los botones de radio, no los botones de confirmación, son respuestas a la instrucción principal.
-   **Proporcione un botón Cancelar para permitir que los usuarios abandonen explícitamente los cambios.** Aunque los usuarios pueden abandonar implícitamente una tarea al no confirmar sus cambios, proporcionar un botón Cancelar les permite hacerlo con mayor confianza.
    -   **Excepción:** No proporcione un botón Cancelar para las tareas en las que los usuarios no puedan realizar cambios. En este caso, el botón Aceptar tiene el mismo efecto que Cancelar.
-   **No use los botones de confirmación Cerrar, Listo o Finalizar.** Estos botones se usan normalmente con cuadros de diálogo modales e implican incorrectamente el cierre de la ventana de elementos del panel de control. Los usuarios pueden cerrar la ventana mediante el botón Cerrar de la barra de título. Además, Done y Finish son confusos porque los usuarios se devuelven a la página desde la que se inició la tarea, por lo que no se realizan realmente.
-   **No deshabilite los botones de confirmación.** De lo contrario, los usuarios tienen que deducir por qué los botones de confirmación están deshabilitados. Es mejor dejar habilitados los botones de confirmación y proporcionar un mensaje de error útil siempre que haya un problema.
-   **Asegúrese de que los botones de confirmación aparecen en la página sin desplazarse.** Si la página es larga, puede hacer que los botones de confirmación siempre sean visibles colocándolos en un área de [comandos,](glossary.md)en lugar de en el área de contenido.

    ![captura de pantalla del cuadro de diálogo Reproducción automática ](images/winenv-ctrl-panels-image11.png)

    En este ejemplo, el tamaño del área de contenido está sin enlazar, por lo que los botones de confirmación se colocan en el área de comandos.

-   Alinee a la derecha los botones de confirmación y use este orden (de izquierda a derecha): botones de confirmación positivos, Cancelar y Aplicar.

**Botones de vista previa**

-   Asegúrese de que el botón Vista previa significa aplicar los cambios pendientes ahora, pero restaure la configuración actual si los usuarios se alejan de la página sin confirmar **los cambios.**
-   **Puede usar botones de vista previa en cualquier página de radio.** Las páginas centrales no necesitan botones de vista previa porque usan un [modelo de confirmación inmediata.](glossary.md)
-   **Considere la posibilidad de usar un botón Vista previa en lugar de un botón Aplicar para las páginas del panel de control.** Los botones de vista previa son más fáciles de entender para los usuarios y se pueden usar en cualquier página de radio.
-   **Proporcione un botón Vista previa solo si la página tiene una configuración (al menos una) con efectos que los usuarios pueden ver.** Los usuarios deben poder obtener una vista previa de un cambio, evaluarlo y realizar más cambios en función de esa evaluación.
-   **Habilite siempre el botón Vista previa.**

**Vistas previas en directo**

Un elemento del panel de control tiene una vista previa dinámica cuando el efecto de los cambios en una página de radio se puede ver inmediatamente.

-   **Considere la posibilidad de usar la versión preliminar en vivo para la configuración de pantalla cuando:**
    -   El efecto es obvio, normalmente porque se aplica a todo el monitor.
    -   El efecto se puede aplicar sin retrasos significativos.
    -   El efecto es seguro y se puede deshacer fácilmente.

        ![captura de pantalla del cuadro de diálogo Cambiar configuración de color ](images/winenv-ctrl-panels-image12.png)

        En este ejemplo, el efecto de la configuración Windows color y apariencia se ve inmediatamente. Esto permite a los usuarios realizar cambios con el mínimo esfuerzo.

-   **Use Guardar cambios y Cancelar para los botones de confirmación.** "Guardar cambios" mantiene la configuración actual, mientras que Cancelar vuelve a la configuración original. "Guardar cambios" se usa en lugar de Aceptar para dejar claro que aún no se han aplicado los cambios en vista previa.
-   **No proporcione un botón Aplicar.** La versión preliminar en directo hace que Aplicar sea innecesario.
-   **Restaure los cambios si los usuarios se desplazan** fuera mediante Atrás, Cerrar o la barra de direcciones. Para conservar los cambios, los usuarios deben confirmarlos explícitamente.

**Aplicar botones**

-   Asegúrese de que el botón Aplicar significa aplicar los cambios pendientes (realizados desde que se inició la tarea o la última aplicación), pero **permanezca en la página actual.** Esto permite a los usuarios evaluar los cambios antes de pasar a otras tareas.
-   **Use los botones Aplicar solo en las páginas de radio finales.** Los botones Aplicar no deben usarse en páginas de radio intermedias para mantener un modelo de confirmación inmediata.
    -   **Excepción:** Puede usar Aplicar botones en una página de centro híbrido si cambiar una configuración requiere [elevación](glossary.md). Para más información, consulte Interacción [de la página central.](#hub-pages)
-   **Proporcione un botón Aplicar solo si la página tiene una configuración (al menos una) con efectos que los usuarios pueden evaluar de forma significativa.** Normalmente, los botones Aplicar se usan cuando la configuración realiza cambios visibles. Los usuarios deben poder aplicar un cambio, evaluarlo y realizar más cambios en función de esa evaluación.
-   **Habilite el botón Aplicar solo cuando haya cambios pendientes.** De lo contrario, deshabilite .
-   **Asigne "A" como clave de acceso.**

### <a name="control-panel-integration"></a>Integración del panel de control

Para integrar el elemento del panel de control Windows, puede hacer lo siguiente:

-   **Registre el elemento del panel de control (incluido** su nombre, descripción e icono) para que Windows sea consciente de ello.
-   Si el elemento del panel de control es de nivel superior (consulte a continuación):
    -   Asócialo a la página **de categoría adecuada.**
    -   Proporcione vínculos a tareas (incluido su **nombre, descripción, palabras** clave y línea de comandos) para indicar las tareas principales y permitir que los usuarios naveguen directamente a las tareas.
-   **Proporcione términos de búsqueda** para ayudar a los usuarios a encontrar vínculos de tareas mediante la característica Panel de control búsqueda.

    Tenga en cuenta que solo puede proporcionar esta información para los elementos individuales del panel de control que no puede agregar ni cambiar esta información para los elementos del panel de control existentes que extiende.

**Páginas de categoría**

-   **Agregue el elemento del panel de control a una página de categoría solo si:**

    -   La mayoría de los usuarios lo necesitan. Ejemplo: Centro de redes y recursos compartidos
    -   Se usa muchas veces. Ejemplo: Sistema
    -   Proporciona una funcionalidad importante que no se expone en ningún otro lugar. Ejemplo: impresoras

    Los elementos del panel de control que cumplen estos criterios se conocen como de nivel superior.

-   **No agregue el elemento del panel de control a una página de categoría si:**

    -   Rara vez se usa o se usa para la configuración de un solo uso. Ejemplo: Centro de bienvenida
    -   Está dirigido a usuarios avanzados o profesionales de IT. Ejemplo: Administración de colores
    -   No se aplica a la configuración actual de hardware o software. Ejemplo: Windows SideShow (si no es compatible con el hardware actual).

    Quitar estos elementos del panel de control de las páginas de categorías facilita la búsqueda de los elementos de nivel superior. Dado su uso, estos elementos del panel de control son lo suficientemente reconocibles a través de puntos de entrada contextuales o de búsqueda.

-   **Asocie el elemento del panel de control de nivel superior a la categoría en la que es más probable que los usuarios lo busquen.** Esta decisión debe basarse en las pruebas de usuario.
-   **Considere la posibilidad de asociar también el elemento del panel de control de nivel superior a la segunda categoría más probable.** Debe asociar un elemento del panel de control a dos categorías si es probable que los usuarios busquen sus tareas principales en más de un lugar.
-   **No asocie el elemento del panel de control a más de dos categorías.** El valor de la categorización se contrae si los elementos del panel de control aparecen en varias categorías.

**Vínculos de tareas**

-   **Asocie el elemento del panel de control a sus tareas principales.** Puede mostrar hasta cinco tareas en una página Categoría, pero se usan tareas adicionales para la búsqueda en el panel de control. Use la misma expresión que para los vínculos de tarea, posiblemente quitando algunas palabras para que los vínculos de tarea sea más concisa.
-   **Prefiere que los vínculos de tareas lleve a distintos lugares del elemento del panel de control.** Tener varios vínculos al mismo lugar puede resultar confuso.

**Términos de búsqueda**

-   **Registre los términos de búsqueda del elemento del panel de control que es más probable que los usuarios usen para describirlo.** Estos términos de búsqueda deben incluir:

    -   Características u objetos configurados.
    -   Tareas principales.

    Estos términos de búsqueda deben basarse en pruebas de usuario.

-   **Incluya también sinónimos comunes para estos términos de búsqueda.** Por ejemplo, supervisar y mostrar son sinónimos, por lo que se deben incluir ambas palabras.
-   **Incluya ortografías alternativas o saltos de palabras.** Por ejemplo, los usuarios pueden buscar sitios web y sitios web. Considere también la posibilidad de proporcionar errores ortográficos comunes.
-   **Considere las formas singulares frente a los nombres plurales.** La característica de búsqueda del panel de control no busca automáticamente ambos formularios; proporcione los formularios para los que es probable que los usuarios busquen.
-   **Use verbos de tiempo presentes simples.** Si registra la conexión como término de búsqueda, la característica de búsqueda no buscará automáticamente las conexiones, la conexión ni la conexión.
-   **No se preocupe por las mayúsculas y minúsculas.** La característica de búsqueda no distingue mayúsculas de minúsculas.

### <a name="standard-users-and-protected-administrators"></a>Usuarios estándar y administradores protegidos

**Muchas configuraciones requieren privilegios de administrador para cambiar.** Si un proceso requiere privilegios de administrador, [](glossary.md) Windows [](glossary.md) Vista y versiones posteriores requiere que los usuarios estándar y los administradores protegidos eleve sus privilegios explícitamente. Esto ayuda a evitar que el código malintencionado se ejecute con privilegios de administrador.

Para obtener más información y ejemplos, vea [Control de cuentas de usuario](winenv-uac.md).

### <a name="schemes-and-themes"></a>Esquemas y temas

Un esquema es una colección con nombre de configuración visual. Un tema es una colección con nombre de configuración en todo el sistema. Entre los ejemplos de esquemas y temas se incluyen Display, Mouse, Teléfono and Modem, Opciones de energía y Opciones de sonido y audio.

-   **Permitir a los usuarios crear esquemas cuando:**

    -   **Es probable que los usuarios cambien la configuración.**
    -   **Es más probable que los usuarios cambien la configuración como una colección.**

    Los esquemas son útiles cuando los usuarios están en un entorno diferente, como una ubicación física diferente (país o región, zona horaria); usar su equipo en una situación diferente (en baterías, acopladas o desacopladas); o usar su equipo para una función diferente (presentaciones, reproducción de vídeo).

-   **Proporcione al menos un esquema predeterminado.** El esquema predeterminado debe tener el nombre y aplicarse a la mayoría de los usuarios en la mayoría de las circunstancias. Los usuarios no deben tener que crear un esquema propio.
-   **Proporcione una vista previa** u otro mecanismo para que los usuarios puedan ver la configuración dentro del esquema.

    ![captura de pantalla del cuadro de diálogo personalización ](images/winenv-ctrl-panels-image13.png)

    En este ejemplo, el elemento del panel de control Personalization muestra una vista previa de la configuración de escritorio y apariencia.

-   **Proporcione los comandos Guardar como y Eliminar.** Un comando rename no es necesario para que los usuarios puedan cambiar el nombre de los esquemas guardando en el nombre deseado y eliminando el esquema original.
-   Si la configuración no se puede aplicar sin un esquema, no permita que los usuarios **eliminen todos los esquemas.** Los usuarios no deben tener que crear un esquema propio.
-   Si los esquemas no son completamente independientes (por ejemplo, los esquemas de energía dependen del modo de funcionamiento actual del equipo portátil), asegúrese de que hay una manera sencilla de cambiar la configuración que se aplica en todos los **esquemas.** Por ejemplo, con esquemas de energía, asegúrese de que los usuarios puedan establecer lo que sucede cuando la tapa de un equipo portátil se cierra en una sola ubicación.

### <a name="miscellaneous"></a>Varios

-   **Use Panel de control para las características que reemplazan o extienden la funcionalidad de Windows existente.** Los siguientes elementos del panel de control son extensibles: Bluetooth Dispositivos, Pantalla, Internet, Teclado, Mouse, Red, Energía, Sistema, Inalámbrico (infiel).

### <a name="default-values"></a>Valores predeterminados

-   **La configuración dentro de un elemento del panel de control debe reflejar el estado actual de la característica.** De lo contrario, sería engañoso y posiblemente provocaría resultados no deseados. Por ejemplo, si la configuración refleja las recomendaciones, pero no el estado actual, los usuarios pueden hacer clic en Cancelar en lugar de realizar cambios, pensando que no se necesitan cambios.
-   **Elija el estado inicial más seguro (para evitar la pérdida de datos o el acceso al sistema) y el estado inicial más seguro.** Suponga que la mayoría de los usuarios no cambiarán la configuración.
-   **Si la seguridad y la seguridad no son factores, elija el estado inicial más probable o conveniente.**

## <a name="text"></a>Texto

### <a name="item-names"></a>Nombres de elemento

-   **Elija un nombre descriptivo que comunique claramente y diferencie lo que hace el elemento del panel de control.** La mayoría de los nombres describen Windows o el objeto que se está configurando y se muestran en la vista clásica de la página principal del panel de control.
-   **No incluya las palabras "Configuración", "Options", "Properties" o "Configuration" en el nombre.** Esto está implícito y dejarla desactivada facilita el examen de los usuarios.

    **Incorrecto:**

    Opciones de accesibilidad

    Módem Configuración

    Opciones de energía

    Configuración regional y de idioma

    **Correcto:**

    Accesibilidad

    Módem

    Potencia

    Formatos e idiomas regionales

    En los ejemplos correctos, se quitan palabras innecesarias.

-   **Si el elemento del panel de control configura características relacionadas, enumére solo las características necesarias para identificar el elemento y enumére las características que más probabilidades de que se reconozcan o se utilicen primero.**

    **Incorrecto:**

    Opciones de carpeta

    Teléfono y opciones de módem

    **Correcto:**

    Archivos y carpetas

    Módem

    En los ejemplos correctos, se da énfasis a las características del elemento del panel de control principal.

-   Use [el uso de mayúsculas de estilo de título.](glossary.md)

### <a name="page-titles"></a>Títulos de página

**Nota:** Al igual que con todas las ventanas del Explorador, los títulos de las páginas del panel de control se muestran en la [barra](glossary.md)de direcciones, pero no en la barra de título.

-   **Para las páginas centrales, use el nombre del elemento del panel de control.**
-   **Para las páginas de radio, use un resumen conciso del propósito de la página.** Use la instrucción principal de la página si es concisa; de lo contrario, use una nueva declaración concisa de la instrucción principal.

    ![captura de pantalla del cuadro de diálogo opciones de energía ](images/winenv-ctrl-panels-image6.png)

    En este ejemplo, Opciones de energía se usa para el título de página en lugar de la instrucción principal.

-   Use mayúsculas de estilo de título.

### <a name="task-link-text"></a>Texto del vínculo de tarea

Las siguientes directrices se aplican a los vínculos a páginas de tareas, como vínculos a tareas de página Categoría y Ver también vínculos.

-   **Elija nombres de tareas concisos que comuniquen y diferencien claramente la tarea.** Los usuarios no deben tener que averiguar qué significa realmente la tarea ni cómo difiere de otras tareas.

    **Incorrecto:**

    Ajuste de la configuración de pantalla

    **Correcto:**

    Resolución de pantalla

    En el ejemplo correcto, la redacción transmite más precisión.

-   **Conserve un lenguaje similar entre los vínculos de tarea y las páginas a las que apuntan.** Los usuarios no deben desapreorse de la página que se muestra mediante un vínculo.
-   **Para las páginas de tareas, diseñe la instrucción principal, los botones de confirmación y los vínculos de tarea como un conjunto de texto relacionado.**
    

    | Ejemplo                             |    Instrucción                                                   |
    |------------------------------|-------------------------------------------------------|
    | Vínculo de tarea:<br/>        | Conexión a una red inalámbrica<br/>              |
    | Instrucción principal:<br/> | Elección de una red a la que conectarse<br/>             |
    | Botón Confirmar:<br/>    | Conectar<br/>                                    |
    | Vínculo de tarea:<br/>        | Configuración de controles parentales<br/>                   |
    | Instrucción principal:<br/> | Elección de un usuario y configuración de controles parentales<br/> |
    | Botón Confirmar:<br/>    | Aplicación del control parental<br/>                     |
    | Vínculo de tarea:<br/>        | Resolución de conflictos de sincronización<br/>                |
    | Instrucción principal:<br/> | ¿Cómo desea resolver este conflicto?<br/>  |
    | Botón Confirmar:<br/>    | Resolver<br/>                                    |

    

     

    En estos ejemplos se muestra la relación del texto del vínculo de tarea, la instrucción principal y el texto del botón de confirmación.

-   Aunque las tareas suelen comenzar con verbos, considere la posibilidad de omitir el verbo en las páginas categoría si es un verbo genérico relacionado con la configuración que no ayuda **a comunicar la tarea.**

    **Verbos específicos y útiles:**

    Agregar

    de Azure Functions

    Conectar

    Copiar

    Crear

    Eliminar

    Desconectar

    Instalar

    Quitar

    Configurar

    Inicio

    Stop

    Solución de problemas

    **Verbos genéricos y poco útiles:**

    Ajustar

    Change

    Elegir

    Configuración

    Editar

    Administrar

    Abrir

    Seleccionar

    Set

    Seleccionar

    Mostrar

    Ver

-   **Si la tarea configura varias características relacionadas, enumre solo las características que son representativas del conjunto.** Omita los detalles que se pueden inferir fácilmente.

    **Incorrecto:**

    Volumen del altavoz, exclusión mutua, icono de volumen

    Altavoces, micrófonos, MIDI y esquemas de sonido

    **Correcto:**

    Volumen del altavoz

    Altavoces y micrófonos

    En los ejemplos correctos, solo se proporcionan las características representativas en el vínculo de tarea.

-   **Debe incluir tareas en términos de tecnología solo si los usuarios de destino también lo harían.**

    **Incorrecto:**

    Connectoids

    Profundidad de píxeles

    ppp

    **Correcto:**

    Impresoras

    Escáneres

    Mouse

    Los ejemplos correctos son términos basados en tecnología que es probable que usen los usuarios de destino, mientras que los ejemplos incorrectos no lo son.

-   Use nombres plurales solo si el sistema puede admitir más de uno.
-   Use [mayúsculas de estilo oración.](glossary.md)
-   No uses puntuación final.

### <a name="main-instructions"></a>Instrucciones principales

-   **Para la página central, use la instrucción principal para explicar el objetivo del usuario con el elemento del panel de control.** La instrucción principal debe ayudar a los usuarios a determinar si han seleccionado el elemento del panel de control correcto. Tenga en cuenta que los usuarios podrían haber seleccionado el elemento del panel de control en error y realmente buscan la configuración que forma parte de otro elemento del panel de control.

    **Ejemplos:**

    Mantener el equipo seguro y actualizado

    Optimice el equipo para que sea más fácil de ver, escuchar y controlar.

-   **En el caso de las páginas de radio, use la instrucción principal para explicar qué hacer en la página.** La instrucción debe ser una instrucción específica, una dirección imperativa o una pregunta. Las instrucciones correctas comunican el objetivo del usuario con la página en lugar de centrarse exclusivamente en la mecánica de su manipulación.

    **Incorrecto:**

    Selección de una tarea de notificación

    **Correcto:**

    Indicar cómo controlar la información entrante

    La versión correcta comunica mejor el objetivo logrado por la página.

-   **Use verbos específicos siempre que sea posible.** Los verbos específicos son más significativos para los usuarios que los genéricos.
-   Use [mayúsculas de estilo oración.](glossary.md)
-   **No incluya períodos finales si la instrucción es una instrucción .** Si la instrucción es una pregunta, incluya un signo de interrogación final.

### <a name="supplemental-instructions"></a>Instrucciones complementarias

-   **Para la página central, use la instrucción complementaria opcional para explicar aún más el propósito del elemento del panel de control.**
-   **Para las páginas de radio, use la instrucción complementaria opcional para presentar información adicional útil para comprender o usar la página.** Puede proporcionar información más detallada y definir terminología.
-   Use oraciones completas y mayúsculas [de estilo oración.](glossary.md)

### <a name="page-text"></a>Texto de página

-   **No vuelva a establecer la instrucción principal en el área de contenido.**
-   **Use la palabra "page" para hacer referencia a la propia página.**
-   **Use la segunda persona (usted, su) para decir** a los usuarios qué hacer en el área principal de instrucción y contenido. A menudo, la segunda persona está implícita.

    **Ejemplo**:

    Elija las imágenes que desea imprimir.

-   **Use la primera persona (I, me, my)** para permitir que los usuarios digan al elemento del panel de control qué hacer en el área de contenido que responde a la instrucción principal.

    **Ejemplo**:

    Imprima las fotos en mi cámara.

### <a name="task-links"></a>Vínculos de tareas

-   **Elija texto de vínculo conciso que comunique y diferencie claramente lo que hace el vínculo de tarea.** Debe ser autoexplicativo y corresponder a la instrucción principal. Los usuarios no deben tener que averiguar qué significa realmente el vínculo ni cómo difiere de otros vínculos.
-   **Inicie siempre los vínculos de tarea con un verbo.**
-   Use [mayúsculas de estilo oración.](glossary.md)
-   No uses puntuación final.
-   **Si el vínculo de tarea requiere una explicación adicional, proporcione** la explicación en un control de texto independiente mediante oraciones completas y signos de puntuación finales. Sin embargo, agregue estas explicaciones solo cuando sea necesario, no agregue explicaciones a todos los vínculos de tarea porque otro vínculo de tarea necesita uno.

Para obtener más información y ejemplos, vea [Vínculos](ctrl-command-links.md).

### <a name="commit-buttons"></a>Botones de confirmación

-   **Use etiquetas de botón de confirmación específicas que tienen sentido por sí solas y que coincidan con la instrucción principal.** Lo ideal es que los usuarios no tengan que leer nada más para comprender la etiqueta. Es mucho más probable que los usuarios lean las etiquetas del botón de comando que el texto estático.
-   **Inicie siempre las etiquetas de botón de confirmación con un verbo.**
-   **No use Cerrar, Listo o Finalizar.** Estas etiquetas de botón son más adecuadas para otros tipos de ventanas.
-   Use [mayúsculas de estilo oración.](glossary.md)
-   No uses puntuación final.
-   Asigne una clave [de acceso única.](glossary.md)
    -   **Excepción:** No asigne claves de acceso a los botones Cancelar, ya que Esc es su clave de acceso. Esto facilita la asignación de las otras claves de acceso.

## <a name="documentation"></a>Documentación

Al hacer referencia a la página principal del panel de control o a las páginas de categorías:

-   En la documentación del usuario, consulte Panel de control, usando mayúsculas de estilo de título y omitiendo un artículo definido anterior.

    **Ejemplo**:

    En Panel de control, abra **Security Center**.

-   En la programación y otra documentación técnica, consulte la página principal del panel de control y la página de categorías del panel de control, sin usar ninguna palabra en mayúsculas. Un artículo definido anterior es opcional.

Para los elementos del panel de control:

-   Al hacer referencia a un elemento de panel de control individual, use "nombre de elemento del panel de control en Panel de control" o, por \[ lo general, "Panel de control elemento" en la documentación \] del usuario. No use applet, programa ni panel de control para hacer referencia a elementos individuales del panel de control.
-   Al hacer referencia a la página central de un elemento del panel de control, use "página de nombre de elemento \[ del panel de control \] principal".
-   Cuando sea posible, formatee el nombre del panel de control con texto en negrita. De lo contrario, coloque el nombre entre comillas solo si es necesario para evitar confusiones.

Ejemplos:

-   En Panel de control, abra **Controles parentales**.
-   Vuelva a la página **principal controles parentales.**

