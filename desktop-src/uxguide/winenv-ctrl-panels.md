---
title: Paneles de control
description: Use los elementos del panel de control para ayudar a los usuarios a configurar características de nivel de sistema y realizar tareas relacionadas. En su lugar, los programas que tienen una interfaz de usuario deben configurarse directamente desde su interfaz de usuario.
ms.assetid: 845325ef-9f1d-4aa7-a5b0-685fac74a9f8
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: dde41544f2bf8c920365f160f71dce7e88d89b81
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104003283"
---
# <a name="control-panels"></a>Paneles de control

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

Use los elementos del panel de control para ayudar a los usuarios a configurar características de nivel de sistema y realizar tareas relacionadas. En su lugar, los programas que tienen una interfaz de usuario deben configurarse directamente desde su interfaz de usuario.

Con el panel de control de Microsoft Windows, los usuarios pueden configurar características de nivel de sistema y realizar tareas relacionadas. Entre los ejemplos de configuración de características de nivel de sistema se incluyen instalación y configuración de hardware y software, seguridad, mantenimiento del sistema y administración de cuentas de usuario.

El término panel de control hace referencia a toda la característica del panel de control de Windows. Los paneles de control individuales se denominan elementos del panel de control. Un elemento del panel de control se considera de nivel superior cuando es accesible directamente desde la Página principal del panel de control o una página de categorías.

![captura de pantalla de la categoría de voz del panel de control ](images/winenv-ctrl-panels-image1.png)

Un elemento típico del panel de control.

La Página principal del panel de control es el punto de entrada principal para todos los elementos del panel de control. Enumera los elementos por su categoría, junto con las tareas más comunes. Se muestra cuando los usuarios hacen clic en panel de control en el menú Inicio.

Una página de categorías del panel de control enumera los elementos de una única categoría, junto con las tareas más comunes. Se muestra cuando los usuarios hacen clic en un nombre de categoría en la Página principal.

Los elementos del panel de control se implementan mediante [flujos de tareas](glossary.md) o hojas de propiedades. En Windows Vista y versiones posteriores, los flujos de tareas son la interfaz de usuario preferida (UI).

**Desarrolladores:** Para obtener información sobre cómo crear elementos del panel de control, consulte [elementos del panel de control](/previous-versions//bb776838(v=vs.85)).

**Nota:** Las instrucciones relacionadas con las [hojas de propiedades](win-property-win.md) se presentan en un artículo independiente.

## <a name="is-this-the-right-user-interface"></a>¿Es la interfaz de usuario correcta?

Para decidirte, intenta responder a estas preguntas:

-   **¿Es el propósito de configurar características de nivel de sistema?** Si no es así, use otro punto de integración. Haga que las características de la aplicación se puedan configurar directamente desde la interfaz de usuario mediante los cuadros de diálogo Opciones, en lugar de usar el panel de control. En el caso de las utilidades que no se usan para la instalación, la configuración o las tareas relacionadas (como la solución de problemas), use el menú Inicio como punto de integración.
-   **¿La característica de nivel de sistema tiene su propia interfaz de usuario?** Si es así, esa interfaz de usuario es donde los usuarios deben ir para realizar los cambios. Por ejemplo, una utilidad de copia de seguridad del sistema debe configurarse desde las opciones del programa en lugar de desde el panel de control.
-   **¿Los usuarios tendrán que cambiar la configuración a menudo?** Si es así (por ejemplo, varias veces a la semana), considere soluciones alternativas, quizás además de usar el panel de control. Por ejemplo, la configuración del volumen maestro de Windows puede configurarse directamente desde su icono en el área de notificación. Algunos valores de configuración se pueden configurar automáticamente. En el explorador de Windows, por ejemplo, la pestaña Compatibilidad de las propiedades de la aplicación permite que una aplicación se ejecute en modo de color 256 en lugar de requerir que los usuarios cambien el modo de vídeo manualmente.
-   **¿Los profesionales de TI de los usuarios de destino?** Si es así, use un complemento de [Microsoft Management Console (MMC)](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) en su lugar, que está diseñado específicamente para tareas de administración del sistema. En algunos casos, la mejor solución es tener un elemento del panel de control para los usuarios generales y un complemento MMC para los profesionales de ti.

    ![captura de pantalla de la ventana Administración de equipos ](images/winenv-ctrl-panels-image2.png)

    En este ejemplo, el complemento MMC usuarios y grupos locales proporciona administración de usuarios dirigida a los profesionales de ti. Es más probable que otros usuarios utilicen el elemento cuentas de usuario del panel de control.

-   **¿La característica es una característica de OEM que solo se usa durante la configuración inicial del sistema?** Si es así, use el centro de bienvenida de Windows como punto de integración.

Los elementos del panel de control son necesarios porque muchas características de nivel de sistema no tienen un punto de integración más obvio o directo. Además, el panel de control no se debe ver como "una ubicación" para todas las opciones de configuración. **Los programas que tienen una interfaz de usuario deben configurarse directamente desde su interfaz de usuario en lugar de usar elementos del panel de control.**

**Incorrecto:**

![captura de pantalla del elemento opciones de Internet del panel de control ](images/winenv-ctrl-panels-image3.png)

En este ejemplo, Windows Internet Explorer no debe representarse en el panel de control, porque su propia interfaz de usuario es un punto de integración mejor.

### <a name="create-a-new-control-panel-item-or-extend-an-existing-one"></a>¿Crear un nuevo elemento del panel de control o extender uno existente?

Para decidirte, intenta responder a estas preguntas:

-   **¿Se puede expresar la funcionalidad como tareas que se pueden conectar a un elemento del panel de control extensible existente?** Los siguientes elementos del panel de control son extensibles: dispositivos Bluetooth, pantalla, Internet, teclado, Mouse, red, alimentación, sistema, inalámbrico (infrarrojos).
-   **¿Las propiedades y las tareas reemplazan las características del elemento del panel de control extensible existente?** Si es así, debe extender el elemento existente del panel de control, ya que resulta en una experiencia de usuario más sencilla. Si no es así, cree un nuevo elemento del panel de control.

## <a name="design-concepts"></a>Conceptos de diseño

**El concepto del panel de control se basa en una metáfora del mundo real.** Un panel de control del mundo real es una colección de controles (botones, conmutadores, medidores y pantallas) que se usa para supervisar y controlar un dispositivo. Los usuarios de estos paneles de control suelen necesitar aprendizaje para comprender cómo usarlos.

A diferencia de sus homólogos del mundo real, **los diseños del panel de control de Windows están optimizados para los usuarios de primera vez.** Los usuarios no realizan la mayoría de las tareas del panel de control con mucha frecuencia, por lo que normalmente no recuerdan cómo realizarlas y, de hecho, tienen que volver a aprenderlas cada vez.

Para diseñar un elemento del panel de control que sea útil y fácil de usar:

-   Asegúrese de que las propiedades son necesarias.
-   Presente propiedades en términos de objetivos de usuario en lugar de tecnología.
-   Presentar propiedades en el nivel de la derecha.
-   Diseñe páginas para tareas específicas.
-   Diseñe páginas para usuarios estándar y administradores protegidos.

Al diseñar y evaluar los elementos que se van a incluir en el panel de control, determine las tareas comunes que realizan los usuarios y asegúrese de que hay una ruta de acceso clara para realizar dichas tareas. Normalmente, los usuarios realizan los siguientes tipos de tareas con los elementos del panel de control:

-   Configuración inicial
-   Cambios poco frecuentes (para la mayoría de los valores)
-   Cambios frecuentes (para algunos valores de configuración importantes)
-   Revertir la configuración a un estado inicial o anterior
-   Solución de problemas

**Si solo hace algo...**

Diseñe páginas del panel de control para tareas específicas y preséntelas en términos de objetivos del usuario en lugar de tecnología.

## <a name="usage-patterns"></a>Patrones de uso

En el caso de los elementos del panel de control, puede usar un flujo de tareas o una hoja de propiedades. Estos son sus patrones de uso:

### <a name="task-flow-patterns"></a>Patrones de flujo de tareas

Los elementos de flujo de tareas usan una página de concentrador para presentar las opciones de alto nivel y las páginas radiales para realizar la configuración real.

**Páginas del concentrador**

-   Páginas de concentrador basadas en tareas. Estas páginas del concentrador presentan las tareas que se usan con más frecuencia. Se usan mejor para algunas tareas importantes o de uso frecuente en las que los usuarios necesitan más instrucciones y explicación. Las páginas del concentrador no tienen botones de confirmación. Las páginas de concentrador basadas en tareas híbridas también tienen algunas propiedades o comandos directamente en ellas. Se recomienda encarecidamente usar páginas centrales híbridas cuando es más probable que los usuarios usen el panel de control para tener acceso a esas propiedades y comandos.
-   Páginas de concentrador basadas en objetos. Estas páginas del concentrador presentan los objetos disponibles mediante un control de vista de lista. Se usan mejor cuando podría haber varios objetos. Las páginas del concentrador no tienen botones de confirmación.

**Páginas de radios**

-   Páginas de tareas. Estas páginas de radios presentan una tarea o un paso en una tarea con una instrucción principal específica basada en tareas. Se usan mejor para las tareas que se benefician de instrucciones y explicaciones adicionales.
-   Páginas de formulario. Estas páginas de radios presentan una colección de propiedades y tareas relacionadas basadas en una instrucción principal general. Se usan mejor para las características que tienen muchas propiedades y se benefician de una presentación directa de una sola página, como las propiedades avanzadas.

### <a name="property-sheet-patterns"></a>Patrones de la hoja de propiedades

-   Las hojas de propiedades se usan mejor en elementos heredados con muchas configuraciones destinadas a usuarios avanzados. Los elementos nuevos pueden lograr el mismo efecto con un flujo de tareas mediante el patrón de página de formulario.

## <a name="guidelines"></a>Directrices

### <a name="property-sheet-control-panel-items"></a>Elementos del panel de control de la hoja de propiedades

-   **No use hojas de propiedades para los nuevos elementos del panel de control.** En su lugar, use flujos de tareas para crear una experiencia sin problemas y hacer uso completo de la funcionalidad de categorización y búsqueda de la Página principal del panel de control.

### <a name="task-flow-control-panel-items"></a>Elementos del panel de control del flujo de tareas

**General**

-   **Mantenga visible el contenido y los controles más importantes sin desplazarse.** Los usuarios no se desplazarán para ver el contenido de la página a menos que tengan un motivo. Puede hacer que los botones de confirmación siempre estén visibles si los coloca en un [área de comandos](glossary.md) en lugar de en el área de contenido. No divida las páginas solo para evitar el desplazamiento.
    -   **Puede desplazar verticalmente las páginas largas,** siempre que los controles más importantes estén visibles sin desplazarse.
    -   **No utilice el desplazamiento horizontal.** En su lugar, rediseñe el contenido de la página y utilice el desplazamiento vertical. Las páginas pueden tener barras de desplazamiento horizontales solo cuando se hacen muy estrechas.
-   **Para navegar entre las páginas:**
    -   Use los [vínculos de tarea](glossary.md) para iniciar una tarea.
    -   Use los vínculos de tarea o el botón siguiente para navegar a la página siguiente en una tarea de varios pasos.
    -   Use los botones de confirmación para completar una tarea.
    -   Use el botón atrás de la barra de menús para volver a las páginas vistas anteriormente. No agregue un botón atrás al área de comandos.
    -   Use la barra de direcciones para volver directamente a la Página principal del panel de control.
    -   Use vea también vínculos en el panel de tareas para ir a las páginas de otros elementos del panel de control. De lo contrario, la navegación debe permanecer dentro de un único elemento del panel de control.
-   **Coloque solo la Página principal del panel de control en la barra de direcciones.** Al hacer clic en ese vínculo, se vuelve a la Página principal del panel de control y se abandona todo el trabajo en curso sin [confirmación](https://msdn.microsoft.com/library/windows/desktop/aa511273.aspx).
-   **No coloque un botón de comando cerrar en las páginas del panel de control.** Los usuarios pueden cerrar una ventana del panel de control con el botón cerrar de la barra de título.

**Vínculos y botones de tareas**

-   **Cuando una página tiene un pequeño conjunto de opciones fijas, use los vínculos de tarea en lugar de una combinación de botones de radio y un botón siguiente.** Esto permite a los usuarios seleccionar una respuesta con un solo clic.
-   Puede colocar vínculos de tarea y botones en los lugares siguientes (en orden de detectabilidad):
    -   [Área de comandos](glossary.md) (solo para botones de comando en páginas de radios).
    -   El [área de contenido](glossary.md):
        -   Botones de comando
        -   Vínculos de tarea
        -   Otros vínculos
    -   Vínculos en el [Panel de tareas](glossary.md) (solo páginas del concentrador).
-   **Base la ubicación de los vínculos de tarea y los botones de importancia y necesidad de detectarlos.**
    -   **Coloque solo los botones de confirmación en el área de comandos.**
    -   **Coloque tareas esenciales en el área de contenido.** Los botones de comando tienden a atraer la atención, de modo que se reservan para los comandos que los usuarios deben ver. Los vínculos de tarea también dibujan la atención, pero menos que los botones de comando.
    -   **Reserve el panel de tareas y los vínculos sin formato para las tareas secundarias (menos importantes).** El panel de tareas es el área menos reconocible de una página de tareas y los vínculos sin formato no son tan visibles como botones de comando y vínculos de tarea.
-   Para los vínculos de tareas presentados en el área de contenido:
    -   **Si hay más de siete vínculos, agrupe los vínculos en categorías.** Proporcione encabezados para cada uno de los grupos.
    -   **Para menos de siete vínculos, presente los vínculos en un solo grupo sin encabezado.**
-   **Presente los vínculos de tarea y los botones en un orden lógico.** Enumerar vínculos de tarea verticalmente, botones de comando horizontalmente.
-   Dentro de las categorías, **Divida los comandos en grupos relacionados.** Coloque los grupos de tareas colocando el más usado primero y, dentro de cada grupo, coloque primero las tareas que se usan con más frecuencia. **El orden resultante debe seguir aproximadamente la probabilidad de uso, pero también tiene un flujo lógico.**
    -   **Excepción:** Los vínculos de tareas que dan lugar a hacer todo deben colocarse en primer lugar.
-   **Si hay muchos vínculos de tareas, asigne a las tareas más importantes una apariencia más prominenta** mediante el uso de un icono de 24x24 píxeles y dos líneas de texto. En el caso de tareas menos importantes, use un icono de 16x16 píxeles o ningún icono, y una sola línea de texto de vínculo.

    ![captura de pantalla de elementos con iconos grandes y pequeños ](images/winenv-ctrl-panels-image4.png)

    En este ejemplo, los comandos importantes reciben una apariencia más prominente.

-   **Tener una separación física clara entre los comandos usados con frecuencia y los comandos destructivos.** De lo contrario, los usuarios podrían hacer clic en comandos destructivos accidentalmente. Es posible que tenga que volver a ordenar los comandos para colocar comandos destructivos juntos.
-   **Proporcione el mecanismo para deshacer los comandos directamente en la página.** Los usuarios no deben tener que navegar en otro lugar para deshacer un error.
-   **Para los vínculos de tarea, use todos los iconos de vínculo de tarea predeterminados o todos los iconos personalizados.** No las mezcle. Considere la posibilidad de usar iconos personalizados solo si:
    -   Ayudan a los usuarios a comprender las tareas.
    -   Cumplen con los [estándares de iconos de Aero](vis-icons.md).
    -   Tienen una apariencia discreta.

**Cuadros de diálogo**

Cuando se usan flujos de tareas, normalmente se desea que una tarea fluya de una página a una en una sola ventana, pero las siguientes circunstancias son excepciones. Utilice los cuadros de diálogo en las siguientes circunstancias:

-   Para solicitar a los usuarios un nombre de usuario y una contraseña de administrador. Use siempre el cuadro de diálogo Administrador de credenciales para este fin. (Debe ser [modal](glossary.md)).
-   Para confirmar un comando en contexto mediante un cuadro de diálogo de tarea o un cuadro de mensaje. (Debe ser modal).
-   Para obtener la entrada para comandos en contexto, como para los comandos nuevo, agregar, guardar como, cambiar nombre e imprimir.

    ![captura de pantalla del cuadro de diálogo eliminar ubicaciones de red ](images/winenv-ctrl-panels-image5.png)

    En este ejemplo, el comando eliminar se realiza en un cuadro de diálogo en lugar de en una página independiente.

-   Para realizar tareas secundarias independientes. El uso de una ventana secundaria no [modal](glossary.md)permite realizar estas tareas de forma independiente y fuera del flujo de tareas principal.

### <a name="hub-pages"></a>Páginas del concentrador

**General**

-   Usar páginas de concentrador basadas en tareas cuando:
    -   **Hay un pequeño número de tareas muy utilizadas o importantes.**
    -   **La configuración implica uno o dos objetos** (ejemplos: monitores, teclado, Mouse, controladores de juegos).
    -   **La configuración se aplica a todo el sistema** (ejemplos: fecha y hora, seguridad, opciones de energía).
-   Usar páginas de concentrador basadas en objetos cuando:
    -   **La configuración puede implicar varios objetos** (ejemplos: cuentas de usuario, conexiones de red, impresoras).
    -   **La configuración solo se aplica al objeto seleccionado**.
-   **No use una página de concentrador si el elemento del panel de control tiene una sola página** que contiene todas las tareas y propiedades implicadas.

**Listas de objetos**

-   **Enumerar los elementos en un orden lógico.** Ordene los objetos con nombre en orden alfabético, números en orden numérico y fechas en orden cronológico.
-   En el caso de los concentradores basados en objetos, **proporcione comandos de la vista de objetos en el panel de tareas si la capacidad de cambiar la vista es importante para las tareas**. La capacidad de cambiar las vistas es importante si hay muchos objetos y la presentación predeterminada no funciona bien en todos los escenarios. Los usuarios pueden cambiar la vista de lista incluso si no hay comandos explícitos a través del menú contextual de la vista de lista, pero es menos reconocible.

Para obtener más instrucciones sobre cómo presentar listas de objetos, vea [vistas de lista](ctrl-list-views.md).

**Interacción**

-   **No coloque botones de confirmación en páginas del concentrador.** Las páginas del concentrador son puntos de inicio fundamentalmente. Los usuarios nunca "confirman" páginas del concentrador que nunca se llevan a cabo con ellas. Y los botones de confirmación en las páginas del concentrador hacen que las tareas iniciadas desde un centro resulten confusas (los usuarios se preguntarán si es necesario confirmar esas tareas).
    -   **Excepción:** Si el cambio de una configuración requiere [elevación](glossary.md), proporcione un botón aplicar con un [icono de escudo de seguridad](winenv-uac.md). Deshabilite el botón de confirmación una vez que se hayan aplicado los cambios.
-   **Considere la posibilidad de colocar las propiedades más útiles directamente en las páginas del concentrador.** Se recomienda encarecidamente usar estas páginas de concentrador híbrido cuando es más probable que los usuarios usen el panel de control para tener acceso a esas propiedades.

    ![captura de pantalla de la página del concentrador de opciones de energía ](images/winenv-ctrl-panels-image6.png)

    En este ejemplo, el elemento opciones de energía del panel de control tiene la configuración más útil directamente en la página del concentrador.

-   **Use un modelo de confirmación inmediato para cualquier configuración en las páginas del concentrador híbrido para que los cambios se realicen inmediatamente.** De nuevo, los usuarios nunca confirman una página de concentrador. Si un valor de configuración requiere un botón confirmar, no lo coloque en una página del concentrador.
-   **Considere la posibilidad de colocar comandos sencillos "de un paso" directamente en páginas del concentrador en lugar de usar vínculos de navegación.**
-   **Confirme los comandos en contexto cuyos efectos no se puedan deshacer fácilmente.** Use un cuadro de [diálogo de tarea](win-dialog-box.md) o de [mensaje](glossary.md).

    ![captura de pantalla del cuadro de diálogo confirmar eliminación ](images/winenv-ctrl-panels-image7.png)

    En este ejemplo, el comando DELETE se confirma con un cuadro de diálogo.

-   **En el caso de las páginas del concentrador basado en tareas, identifique cada tarea con un vínculo de tarea y un icono.** También puede proporcionar una descripción opcional para cada vínculo. Sin embargo, intente hacer que los vínculos de tarea sean autodescriptivos y proporcione descripciones opcionales solo a los vínculos que realmente los necesiten.

    ![captura de pantalla de la página del concentrador de rendimiento del equipo ](images/winenv-ctrl-panels-image8.png)

    En este ejemplo, cada tarea tiene un vínculo de tarea y un icono.

-   **En el caso de las páginas de concentrador basadas en objetos, al hacer clic con un solo clic se seleccionan objetos y, al hacer doble clic en, se selecciona un objeto y se navega a su página predeterminada.** La página predeterminada suele ser una página de propiedades o una página de concentrador basada en tareas.
-   **Una página de concentrador basada en objetos puede desplazarse a un concentrador basado en tareas para los objetos seleccionados.** Sin embargo, estos centros secundarios deben evitarse porque hacen que un elemento del panel de control se sienta demasiado indirecto.

**Paneles de tareas**

Use los paneles de tareas para presentar vínculos a comandos, vistas y elementos del panel de control relacionados.

-   En el caso de los paneles de tareas de los concentradores basados en tareas, presente los vínculos en el orden siguiente:
    -   **Comandos secundarios**. Presente solo las tareas principales en el área de contenido. Use el panel de tareas para las tareas secundarias y opcionales. Considere la posibilidad de una tarea principal si los usuarios deben detectarla en escenarios importantes; secundario si es aceptable que los usuarios no lo detecten.
    -   **Vea también**. Los vínculos opcionales que se desplazan a los elementos relacionados del panel de control.
-   En el caso de los paneles de tareas de los concentradores basados en objetos, presente los vínculos en el orden siguiente:
    -   **Vistas de objeto**. Vínculos opcionales que se usan para controlar la presentación de los objetos.
    -   **Comandos fijos**. Comandos que son independientes de los objetos seleccionados actualmente.
    -   **Comandos contextuales**. Los comandos que dependen de los objetos seleccionados actualmente y, por tanto, no se muestran siempre.
    -   **Vea también**. Los vínculos opcionales que se desplazan a los elementos relacionados del panel de control.
-   **No use paneles de tareas en las páginas de radios.** A diferencia de las páginas del concentrador, las páginas radiales deben centrarse en completar la tarea. No quiere animar a los usuarios a salir antes de la finalización.

**Vea también vínculos**

-   **Proporcione también vínculos en el panel de tareas para ayudar a los usuarios a buscar elementos relacionados del panel de control o el elemento derecho del panel de control si tienen uno incorrecto.** Vínculo a elementos es probable que los usuarios asocien con el elemento del panel de control.

    ![captura de pantalla del centro de actividades "vea también" vínculos ](images/winenv-ctrl-panels-image9.png)

    En este ejemplo, el elemento del panel de control del centro de actividades se vincula a los elementos relacionados del panel de control.

-   **Vincular a una página de tarea específica si es lo que es más probable que reconozcan los usuarios.** De lo contrario, vincule a todo el elemento del panel de control. Use el nombre del panel de control sin agregar la frase, panel de control.

### <a name="spoke-pages"></a>Páginas de radios

**General**

-   **Use las páginas de tareas para tareas importantes o de uso frecuente en las que los usuarios necesitan más instrucciones y explicación.**
-   **Usar páginas de formulario para características que tienen muchos valores y se benefician de una presentación directa de una sola página.** Las tareas ideales para estas páginas normalmente implican cambios obvios en algunas propiedades simples.
-   **No use paneles de tareas en las páginas de radios.**

**Interacción**

-   **Intente limitar las tareas principales a una sola página.** Si se necesita más de una página, puede:
    -   **Use páginas radiales intermedias para pasos adicionales u opcionales.** La página de radios final confirma las páginas de radios intermedias.
    -   **Use ventanas independientes para tareas auxiliares independientes.** Las ventanas independientes se confirman por sí mismas y de forma independiente de la tarea principal.

Al hacerlo, se mantiene el significado de los botones de confirmación de la tarea principal sin ambigüedades. Los usuarios siempre deben estar seguros de saber en qué se están confirmando.

-   **No usar vea también vínculos dentro de un flujo de tareas.** Estos vínculos a elementos de panel de control relacionados, pero diferentes. Aunque la navegación a un elemento diferente es aceptable en las páginas del concentrador, no se encuentra en páginas radiales, porque esto interrumpe la tarea.
-   **No utilice páginas de radios para entradas o confirmaciones simples.** En su lugar, use cuadros de diálogo modales.

**Interacción (páginas radiales intermedias)**

-   **Use los vínculos de tarea o el botón siguiente para navegar a la página siguiente.** La manera de continuar con el paso siguiente siempre debe ser obvia.
-   **Puede tener vínculos de navegación a pasos de tareas opcionales.** Para evitar confusiones cuando los usuarios se confirman en la tarea, esas páginas adicionales deben ser páginas intermedias dentro del mismo elemento del panel de control. No deben tener botones de confirmación, pero se deben confirmar cuando se confirma la tarea principal.

**Interacción (páginas radios finales)**

-   **Use los botones de confirmación para completar una tarea.** Use un [modelo de confirmación diferida](glossary.md) para las páginas radiales, de modo que los cambios no se realicen hasta que se confirmen explícitamente (si los usuarios se desplazan con atrás, cerrar o la barra de direcciones, se abandonan los cambios). Los botones de confirmación son una pista visual de que el usuario está a punto de completar una tarea. No use vínculos para este fin.
-   **No confirme los botones de confirmación (incluida la cancelación).** Esto puede resultar molesto. Excepciones:
    -   La acción tiene consecuencias importantes y, si es incorrecta, no se fixable fácilmente.
    -   La acción puede provocar una pérdida significativa del tiempo o del trabajo del usuario.
    -   La acción es claramente incoherente con otras acciones.
-   **No confirme si los usuarios abandonan los cambios** desplazándose hacia afuera, cerca o desde la barra de direcciones. Sin embargo, puede confirmar si una navegación potencialmente no intencionada puede provocar una pérdida significativa del tiempo o del trabajo del usuario.
-   **No use vínculos de comandos o de navegación** (incluidos los vínculos). En las páginas de radios finales, los usuarios deben completar o cancelar explícitamente la tarea. No se debe animar a los usuarios a navegar en otra parte, ya que si lo hace, es probable que cancele la tarea implícitamente.
-   **Cuando los usuarios completan o cancelan una tarea, deben enviarse de vuelta a la página del concentrador desde la que se inició la tarea.** Si no existe esa página, cierre la ventana del panel de control en su lugar. No suponga que las páginas de radio siempre se inician desde otra página.
-   **Quite las páginas "confirmadas" obsoletas de la pila de retroceso del explorador de Windows** cuando devuelva los usuarios a la página desde la que se inició la tarea. Los usuarios nunca deben ver las páginas en las que ya se han confirmado al hacer clic en el botón atrás. Los usuarios siempre deben realizar cambios adicionales rehaciendo completamente la tarea en lugar de hacer clic en atrás para modificar páginas obsoletas.
    -   **Desarrolladores:** Puede quitar estas páginas obsoletas mediante las API ITravelLog:: FindTravelEntry () y ITravelLogEx::D eleteEntry ().

**Botones de confirmación**

**Nota:** Los botones cancelar se consideran botones de confirmación.

-   **Confirmar tareas mediante botones de confirmación que son respuestas específicas a la instrucción principal, en lugar de etiquetas genéricas, como aceptar.** Las etiquetas de los botones de confirmación deben tener sentido por sí mismas. Evite usar OK porque no es una respuesta específica a la instrucción principal y, por lo tanto, es más fácil misunderstand. Además, aceptar se usa normalmente con los cuadros de diálogo modales e implica cerrar incorrectamente la ventana de elemento del panel de control.
    -   **Excepciones:**
        -   Utilice aceptar para las páginas que no tienen configuración.
        -   Use aceptar cuando la respuesta específica siga siendo genérica, como guardar, seleccionar o elegir, como cuando se cambia una configuración concreta o una colección de valores de configuración.
        -   Use aceptar si la página tiene botones de radio que son respuestas a la instrucción principal. Para mantener el modelo de confirmación diferida, no puede usar vínculos de tarea en una página de radio final.

            ![captura de pantalla de restricciones web con el botón Aceptar ](images/winenv-ctrl-panels-image10.png)

            En este ejemplo, los botones de radio, no los botones de confirmación, son respuestas a la instrucción principal.
-   **Proporcione un botón Cancelar para permitir que los usuarios abandonen los cambios explícitamente.** Aunque los usuarios pueden abandonar implícitamente una tarea si no confirman sus cambios, proporcionar un botón Cancelar les permite hacerlo con mayor confianza.
    -   **Excepción:** No proporcione un botón Cancelar para las tareas en las que los usuarios no pueden realizar cambios. El botón Aceptar tiene el mismo efecto que cancelar en este caso.
-   **No use los botones de confirmación cerrar, listo o finalizar.** Estos botones suelen usarse con cuadros de diálogo modales y, de forma incorrecta, cerrar la ventana de elemento del panel de control. Los usuarios pueden cerrar la ventana con el botón cerrar de la barra de título. Además, listo y finalizar son engañosos, ya que los usuarios se devuelven a la página en la que se inició la tarea, por lo que no se han hecho realmente.
-   **No deshabilite los botones de confirmación.** De lo contrario, los usuarios deben deducir por qué están deshabilitados los botones de confirmación. Es mejor dejar habilitados los botones de confirmación y proporcionar un mensaje de error útil siempre que haya un problema.
-   **Asegúrese de que los botones de confirmación aparecen en la página sin desplazarse.** Si la página es larga, puede hacer que los botones de confirmación siempre estén visibles si los coloca en un [área de comandos](glossary.md), en lugar de en el área de contenido.

    ![captura de pantalla del cuadro de diálogo reproducción automática ](images/winenv-ctrl-panels-image11.png)

    En este ejemplo, el tamaño del área de contenido es ilimitado, por lo que los botones de confirmación se colocan en el área de comandos.

-   Alinee a la derecha los botones de confirmación y use este orden (de izquierda a derecha): botones de confirmación positivos, cancelar y aplicar.

**Botones de vista previa**

-   Asegúrese de que **el botón vista previa significa aplicar los cambios pendientes ahora pero restaure la configuración actual si los usuarios navegan fuera de la página sin confirmar los cambios.**
-   **Puede usar los botones de vista previa en cualquier página de radio.** Las páginas del concentrador no necesitan botones de vista previa porque usan un [modelo de confirmación inmediata](glossary.md).
-   **Considere la posibilidad de usar un botón de vista previa en lugar de un botón aplicar en las páginas del panel de control.** Los botones de vista previa son más fáciles de entender para los usuarios y se pueden usar en cualquier página de radio.
-   **Proporcione un botón de vista previa solo si la página tiene valores de configuración (al menos uno) con efectos que los usuarios pueden ver.** Los usuarios deben poder obtener una vista previa de un cambio, evaluar el cambio y realizar cambios adicionales en función de esa evaluación.
-   **Habilite siempre el botón vista previa.**

**Vistas previas en vivo**

Un elemento del panel de control tiene una vista previa dinámica cuando el efecto de los cambios en una página radial se puede ver de inmediato.

-   **Considere la posibilidad de usar la vista previa dinámica para la configuración de pantalla cuando:**
    -   El efecto es obvio, normalmente porque se aplica a todo el monitor.
    -   El efecto se puede aplicar sin un retraso significativo.
    -   El efecto es seguro y se puede deshacer fácilmente.

        ![captura de pantalla del cuadro de diálogo Cambiar configuración de color ](images/winenv-ctrl-panels-image12.png)

        En este ejemplo, el efecto de la configuración de color y apariencia de Windows se ve inmediatamente. Esto permite a los usuarios realizar cambios con un esfuerzo mínimo.

-   **Use guardar cambios y Cancelar para los botones de confirmación.** "Guardar cambios" mantiene la configuración actual, mientras que cancelar vuelve a la configuración original. "Guardar cambios" se usa en lugar de aceptar para aclarar que todavía no se han aplicado los cambios de vista previa.
-   **No proporcione un botón aplicar.** La vista previa dinámica hace que la aplicación sea innecesaria.
-   **Restaure los cambios si los usuarios se desplazan** con atrás, cerrar o la barra de direcciones. Para conservar los cambios, los usuarios deben confirmarlos explícitamente.

**Aplicar botones**

-   Asegúrese **de que el botón aplicar significa que se aplican los cambios pendientes (realizados desde que se inició la tarea o se aplicó la última), pero permanecen en la página actual.** Esto permite a los usuarios evaluar los cambios antes de pasar a otras tareas.
-   **Use los botones aplicar solo en las páginas de radios finales.** Los botones aplicar no se deben usar en páginas de radios intermedias para mantener un modelo de confirmación inmediato.
    -   **Excepción:** Puede usar los botones aplicar en una página central híbrida si el cambio de una configuración requiere [elevación](glossary.md). Para obtener más información, consulte interacción de la [página del concentrador](#hub-pages).
-   **Proporcione un botón Aplicar solo si la página tiene valores de configuración (al menos uno) con efectos que los usuarios pueden evaluar de forma significativa.** Normalmente, se usan botones aplicar cuando la configuración realiza cambios visibles. Los usuarios deben poder aplicar un cambio, evaluar el cambio y realizar cambios adicionales en función de esa evaluación.
-   **Habilite el botón Aplicar solo cuando haya cambios pendientes;** de lo contrario, deshabilítelo.
-   **Asigne "A" como tecla de acceso.**

### <a name="control-panel-integration"></a>Integración del panel de control

Para integrar el elemento del panel de control con Windows, puede:

-   **Registre el elemento del panel de control (incluido el nombre, la descripción y el icono)** para que Windows sea consciente de ello.
-   Si el elemento del panel de control es de nivel superior (consulte a continuación):
    -   Asócielo a la página de **categorías** adecuada.
    -   **Proporcione vínculos de tareas (incluido el nombre, la descripción, las palabras clave y la línea de comandos)** para indicar las tareas principales y permitir que los usuarios naveguen directamente a las tareas.
-   **Proporcione términos de búsqueda** para ayudar a los usuarios a encontrar los vínculos de tareas mediante la característica de búsqueda del panel de control.

    Tenga en cuenta que solo puede proporcionar esta información para los elementos individuales del panel de control. no puede Agregar o cambiar esta información para los elementos del panel de control existentes que extiende.

**Páginas de categorías**

-   **Agregue el elemento del panel de control a una página de categoría solo si:**

    -   La mayoría de los usuarios la necesitan. Ejemplo: Centro de redes y recursos compartidos
    -   Se usa muchas veces. Ejemplo: System
    -   Proporciona una funcionalidad importante que no se expone en ningún otro lugar. Ejemplo: impresoras

    Los elementos del panel de control que cumplen estos criterios se conocen como nivel superior.

-   **No agregue el elemento del panel de control a una página de categorías si:**

    -   Rara vez se usa o se usa para la configuración única. Ejemplo: Centro de bienvenida
    -   Está destinado a usuarios avanzados o profesionales de ti. Ejemplo: administración del color
    -   No se aplica a la configuración de hardware o software actual. Ejemplo: Windows SideShow (si no se admite en el hardware actual).

    Quitar estos elementos del panel de control de las páginas de categorías facilita la búsqueda de los elementos de nivel superior. Dado su uso, estos elementos del panel de control son suficientemente detectables a través de puntos de entrada contextuales o de búsqueda.

-   **Asocie el elemento de nivel superior del panel de control a la categoría en la que los usuarios tienen más probabilidades de buscarlo.** Esta decisión debe basarse en las pruebas de usuario.
-   **Considere la posibilidad de asociar el elemento de nivel superior del panel de control con la segunda categoría más probable.** Debe asociar un elemento del panel de control con dos categorías si es probable que los usuarios busquen sus tareas principales en más de un lugar.
-   **No asocie el elemento del panel de control con más de dos categorías.** El valor de la categorización está desordenado si los elementos del panel de control aparecen en varias categorías.

**Vínculos de tarea**

-   **Asocie el elemento del panel de control con sus tareas principales.** Puede mostrar hasta cinco tareas en una página de categoría, pero las tareas adicionales se usan para la búsqueda en el panel de control. Use la misma frase que para los vínculos de tareas, posiblemente quitando algunas palabras para que los vínculos de tarea sean más concisos.
-   **Prefiere que los vínculos de tarea conducen a lugares diferentes en el elemento del panel de control.** Tener varios vínculos al mismo lugar puede ser confuso.

**Términos de búsqueda**

-   **Registre los términos de búsqueda del elemento del panel de control que los usuarios tienen más probabilidades de usar para describirlos.** Estos términos de búsqueda deben incluir:

    -   Las características o los objetos configurados.
    -   Tareas principales.

    Estos términos de búsqueda deben basarse en las pruebas de usuario.

-   **Incluya también sinónimos comunes para estos términos de búsqueda.** Por ejemplo, supervisar y mostrar son sinónimos, por lo que se deben incluir ambas palabras.
-   **Incluir palabras alternativas o saltos de palabra.** Por ejemplo, los usuarios pueden buscar sitio web y sitio Web. Considere la posibilidad de escribir también errores comunes.
-   **Considere los formatos singular y plural.** La característica de búsqueda del panel de control no busca automáticamente ambos formularios; proporcione los formularios para los que es probable que los usuarios busquen.
-   **Usar verbos de presentación en el pasado sencillo.** Si registra Connect como término de búsqueda, la característica de búsqueda no buscará automáticamente las conexiones, la conexión y la conexión.
-   **No se preocupe por las mayúsculas y minúsculas.** La característica de búsqueda no distingue entre mayúsculas y minúsculas.

### <a name="standard-users-and-protected-administrators"></a>Usuarios estándar y administradores protegidos

**Muchas opciones requieren privilegios de administrador para cambiar.** Si un proceso requiere privilegios de administrador, Windows Vista y versiones posteriores requieren que [los usuarios estándar](glossary.md) y [los administradores protegidos](glossary.md) eleven sus privilegios explícitamente. Esto ayuda a evitar que se ejecute código malintencionado con privilegios de administrador.

Para obtener más información y ejemplos, vea [control de cuentas de usuario](winenv-uac.md).

### <a name="schemes-and-themes"></a>Esquemas y temas

Un esquema es una colección con nombre de la configuración visual. Un tema es una colección con nombre de valores de configuración en todo el sistema. Entre los ejemplos de esquemas y temas se incluyen las opciones pantalla, Mouse, teléfono y módem, opciones de energía y sonido y audio.

-   **Permitir a los usuarios crear esquemas cuando:**

    -   **Es probable que los usuarios cambien la configuración.**
    -   **Lo más probable es que los usuarios cambien la configuración como una colección.**

    Los esquemas son útiles cuando los usuarios se encuentran en un entorno diferente, como una ubicación física diferente (país o región, zona horaria). usar su equipo en una situación diferente (con baterías, acopladas o desacopladas); o usar su equipo para una función diferente (presentaciones, reproducción de vídeo).

-   **Proporcione al menos un esquema predeterminado.** El esquema predeterminado debe ser bien denominado y aplicarse a la mayoría de los usuarios en la mayoría de los casos. Los usuarios no deben tener que crear un esquema propio.
-   **Proporcione una vista previa** u otro mecanismo para que los usuarios puedan ver los valores dentro del esquema.

    ![captura de pantalla del cuadro de diálogo de personalización ](images/winenv-ctrl-panels-image13.png)

    En este ejemplo, el elemento del panel de control personalización muestra una vista previa de la configuración de escritorio y apariencia.

-   **Proporcione los comandos Guardar como y eliminar.** Un comando rename no es necesario los usuarios pueden cambiar el nombre de los esquemas guardando en el nombre deseado y eliminando el esquema original.
-   Si no se puede aplicar la configuración sin un esquema, **no permita que los usuarios eliminen todos los esquemas.** Los usuarios no deben tener que crear un esquema propio.
-   Si los esquemas no son completamente independientes (por ejemplo, los esquemas de energía dependen del modo de funcionamiento del portátil actual), asegúrese de que **hay una forma sencilla de cambiar la configuración que se aplica a todos los esquemas.** Por ejemplo, con los esquemas de energía, asegúrese de que los usuarios pueden establecer lo que ocurre cuando se cierra la tapa de un equipo portátil en una sola ubicación.

### <a name="miscellaneous"></a>Varios

-   **Use las extensiones del panel de control para las características que reemplazan o extienden la funcionalidad existente de Windows.** Los siguientes elementos del panel de control son extensibles: dispositivos Bluetooth, pantalla, Internet, teclado, Mouse, red, alimentación, sistema, inalámbrico (infrarrojos).

### <a name="default-values"></a>Valores predeterminados

-   **La configuración de un elemento del panel de control debe reflejar el estado actual de la característica.** De lo contrario, podría ser engañoso y, posiblemente, provocar resultados no deseados. Por ejemplo, si la configuración refleja las recomendaciones pero no el estado actual, los usuarios pueden hacer clic en Cancelar en lugar de realizar cambios, pensando que no se necesita ningún cambio.
-   **Elija el más seguro (para evitar la pérdida de datos o el acceso al sistema) y el estado inicial más seguro.** Supongamos que la mayoría de los usuarios no cambiarán la configuración.
-   **Si la seguridad y la seguridad no son factores, elija el estado inicial que sea más probable o práctico.**

## <a name="text"></a>Texto

### <a name="item-names"></a>Nombres de elementos

-   **Elija un nombre descriptivo que se comunique claramente y describa lo que hace el elemento del panel de control.** La mayoría de los nombres describen la característica o el objeto de Windows que se está configurando y se muestran en la vista clásica de la Página principal del panel de control.
-   **No incluya las palabras "configuración", "opciones", "propiedades" o "configuración" en el nombre.** Esto es implícito y, si se deja desactivado, facilita la exploración de los usuarios.

    **Incorrecto:**

    Opciones de accesibilidad

    Configuración del módem

    Opciones de energía

    Configuración regional y de idioma

    **Correcto:**

    Accesibilidad

    Módem

    Power

    Idiomas y formatos regionales

    En los ejemplos correctos, se quitan las palabras innecesarias.

-   **Si el elemento del panel de control configura características relacionadas, enumera solo las características necesarias para identificar el elemento y enumera las características que es más probable que se reconozcan o se usen primero.**

    **Incorrecto:**

    Opciones de carpeta

    Opciones de teléfono y módem

    **Correcto:**

    Archivos y carpetas

    Módem

    En los ejemplos correctos, se da énfasis a las características principales del elemento del panel de control.

-   Usar [mayúsculas y minúsculas de estilo de título](glossary.md).

### <a name="page-titles"></a>Títulos de página

**Nota:** Al igual que con todas las ventanas del explorador, los títulos de página del panel de control se muestran en la [barra de direcciones](glossary.md), pero no en la barra de título.

-   **En el caso de las páginas del concentrador, use el nombre del elemento del panel de control.**
-   **En el caso de las páginas radiales, use un resumen conciso del propósito de la página.** Use la instrucción principal de la página si es concisa; de lo contrario, use una resituación concisa de la instrucción principal.

    ![captura de pantalla del cuadro de diálogo Opciones de energía ](images/winenv-ctrl-panels-image6.png)

    En este ejemplo, se usan las opciones de energía para el título de la página en lugar de la instrucción principal.

-   Usar mayúsculas y minúsculas de estilo de título.

### <a name="task-link-text"></a>Texto de vínculo de tarea

Las siguientes directrices se aplican a los vínculos a las páginas de tareas, como los vínculos de tarea de la página de categorías y los vínculos.

-   **Elija nombres de tarea concisos que se comunican claramente y diferencian la tarea.** Los usuarios no deben tener que averiguar qué significa realmente la tarea o cómo se diferencia de otras tareas.

    **Incorrecto:**

    Ajustar la configuración de pantalla

    **Correcto:**

    Resolución de pantalla

    En el ejemplo correcto, el texto transmite más precisión.

-   **Conserve el idioma similar entre los vínculos de tareas y las páginas a las que apuntan.** Los usuarios no deben sorprender por la página que se muestra en un vínculo.
-   **En el caso de las páginas de tareas, diseñe la instrucción principal, los botones de confirmación y los vínculos de tareas como un conjunto de texto relacionado.**

    **Ejemplos:**

    

    |                              |                                                       |
    |------------------------------|-------------------------------------------------------|
    | Vínculo de tarea:<br/>        | Conexión a una red inalámbrica<br/>              |
    | Instrucción principal:<br/> | Elegir una red a la que conectarse<br/>             |
    | Botón confirmar:<br/>    | Conectar<br/>                                    |
    | Vínculo de tarea:<br/>        | Configurar controles parentales<br/>                   |
    | Instrucción principal:<br/> | Elegir un usuario y configurar el control parental<br/> |
    | Botón confirmar:<br/>    | Aplicar control parental<br/>                     |
    | Vínculo de tarea:<br/>        | Resolver los conflictos de sincronización<br/>                |
    | Instrucción principal:<br/> | ¿Cómo desea resolver este conflicto?<br/>  |
    | Botón confirmar:<br/>    | Resolver<br/>                                    |

    

     

    En estos ejemplos se muestra la relación entre el texto del vínculo de la tarea, la instrucción principal y el texto del botón confirmar.

-   Aunque las tareas suelen empezar con verbos, **considere la posibilidad de omitir el verbo en las páginas de categorías si es un verbo genérico relacionado con la configuración que no ayuda a comunicar la tarea.**

    **Verbos específicos y útiles:**

    Sumar

    de Azure Functions

    Conectar

    Copiar

    Crear

    Eliminar

    Desconectar

    Instalar

    Remove

    Configurar

    Start

    Stop

    Solución de problemas

    **Verbos genéricos no Ayudales:**

    Ajustar

    Cambio

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

-   **Si la tarea configura varias características relacionadas, enumere solo las características representativas del conjunto.** Omitir los detalles que se pueden deducir fácilmente.

    **Incorrecto:**

    Icono de volumen, silenciar, volumen de altavoz

    Altavoces, micrófonos, MIDI y esquemas de sonido

    **Correcto:**

    Volumen de altavoz

    Altavoces y micrófonos

    En los ejemplos correctos, solo se proporcionan las características representativas en el vínculo de tarea.

-   **Solo se deben formular las tareas en términos de tecnología si los usuarios de destino lo harían también.**

    **Incorrecto:**

    Connectoids

    Profundidad de píxeles

    ppp

    **Correcto:**

    Impresoras

    Escáneres

    Mouse

    Los ejemplos correctos son términos basados en tecnología que es probable que utilicen los usuarios, mientras que los ejemplos incorrectos no lo son.

-   Use sustantivos plural solo si el sistema puede admitir más de uno.
-   Usar [mayúsculas y minúsculas en el estilo de oraciones](glossary.md).
-   No uses puntuación final.

### <a name="main-instructions"></a>Instrucciones principales

-   **En la página del concentrador, use la instrucción principal para explicar el objetivo del usuario con el elemento del panel de control.** La instrucción principal debe ayudar a los usuarios a determinar si han seleccionado el elemento derecho del panel de control. Tenga en cuenta que es posible que los usuarios hayan seleccionado el elemento del panel de control por error y que busquen valores que formen parte de otro elemento del panel de control.

    **Ejemplos:**

    Mantenga su equipo seguro y actualizado

    Optimizar el equipo para que sea más fácil de ver, oír y controlar

-   **En el caso de las páginas radiales, use la instrucción principal para explicar qué hacer en la página.** La instrucción debe ser una instrucción específica, una dirección imperativa o una pregunta. Las buenas instrucciones comunican el objetivo del usuario con la página en lugar de centrarse exclusivamente en la mecánica de la manipulación.

    **Incorrecto:**

    Seleccionar una tarea de notificación

    **Correcto:**

    Indicar cómo controlar la información entrante

    La versión correcta comunica mejor el objetivo logrado por la página.

-   **Use verbos específicos siempre que sea posible.** Los verbos específicos son más significativos para los usuarios que los genéricos.
-   Usar [mayúsculas y minúsculas en el estilo de oraciones](glossary.md).
-   **No incluya los períodos finales si la instrucción es una instrucción.** Si la instrucción es una pregunta, incluya un signo de interrogación final.

### <a name="supplemental-instructions"></a>Instrucciones complementarias

-   **En la página del concentrador, use la instrucción complementaria opcional para explicar mejor el propósito del elemento del panel de control.**
-   **En el caso de las páginas radiales, use la instrucción complementaria opcional para presentar información adicional útil para entender o usar la página.** Puede proporcionar información más detallada y definir la terminología.
-   Use frases completas y uso [de mayúsculas del estilo de oraciones](glossary.md).

### <a name="page-text"></a>Texto de la página

-   **No represente la instrucción principal en el área de contenido.**
-   **Use la palabra "página" para hacer referencia a la propia página.**
-   **Use la segunda persona (usted, su) para indicar a los usuarios qué hacer** en la instrucción principal y en el área de contenido. A menudo, la segunda persona está implícita.

    **Ejemplo**:

    Elija las imágenes que desea imprimir.

-   **Use la primera persona (I, me, My) para permitir que los usuarios indiquen al elemento del panel de control qué hacer** en el área de contenido que responda a la instrucción principal.

    **Ejemplo**:

    Imprimir las fotos en la cámara.

### <a name="task-links"></a>Vínculos de tarea

-   **Elija texto de vínculo conciso que se comunique claramente y diferencie lo que hace el vínculo de tarea.** Debe ser autoexplicativo y corresponder a la instrucción principal. Los usuarios no deben tener que averiguar qué significa realmente el vínculo o cómo se diferencia de otros vínculos.
-   **Inicie siempre los vínculos de tarea con un verbo.**
-   Usar [mayúsculas y minúsculas en el estilo de oraciones](glossary.md).
-   No uses puntuación final.
-   **Si el vínculo de tarea requiere una explicación más detallada, proporcione la explicación en un control de texto independiente** mediante frases completas y puntuación final. Sin embargo, agregue estas explicaciones solo cuando sea necesario no agregue explicaciones a todos los vínculos de tarea porque otro vínculo de tarea necesita uno.

Para obtener más información y ejemplos, vea [vínculos](ctrl-command-links.md).

### <a name="commit-buttons"></a>Botones de confirmación

-   **Use etiquetas de botón de confirmación específicas que tengan sentido por sí mismas y que coincidan con la instrucción principal.** Lo ideal es que los usuarios no tengan que leer nada más para entender la etiqueta. Es mucho más probable que los usuarios lean etiquetas de botón de comando que el texto estático.
-   **Iniciar siempre etiquetas de botón de confirmación con un verbo.**
-   **No utilice Close, Done o Finish.** Estas etiquetas de botón son más adecuadas para otros tipos de ventanas.
-   Usar [mayúsculas y minúsculas en el estilo de oraciones](glossary.md).
-   No uses puntuación final.
-   Asigne una [clave de acceso](glossary.md)única.
    -   **Excepción:** No asigne teclas de acceso para cancelar botones, porque ESC es su clave de acceso. Esto hace que las demás claves de acceso sean más fáciles de asignar.

## <a name="documentation"></a>Documentación

Al hacer referencia a la Página principal del panel de control o a las páginas de categorías:

-   En la documentación del usuario, consulte panel de control, uso de mayúsculas y minúsculas del estilo de título y omisión de un artículo definitivo anterior.

    **Ejemplo**:

    En el panel de control, Abra **Security Center**.

-   En programación y otra documentación técnica, consulte la Página principal del panel de control y la página de categorías del panel de control sin mayúsculas en ninguna de las palabras. Un artículo definitivo anterior es opcional.

Para los elementos del panel de control:

-   Al hacer referencia a un elemento individual del panel de control, use " \[ nombre \] del elemento del panel de control en el panel de control" o, por lo general, "elemento del panel de control" en la documentación del usuario. No use el applet, el programa o el panel de control para hacer referencia a elementos individuales del panel de control.
-   Al hacer referencia a la página del concentrador de un elemento del panel de control, use la \[ Página de nombre de elemento del panel de control principal \] .
-   Siempre que sea posible, formatee el nombre del panel de control usando texto en negrita. De lo contrario, ponga el nombre entre comillas solo si es necesario para evitar confusiones.

Ejemplos:

-   En el panel de control, Abra **controles parentales**.
-   Vuelva a la Página principal de **controles parentales** .

