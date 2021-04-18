---
title: Impresión (conceptos básicos del diseño)
description: La impresión es la experiencia del usuario en papel. Es fácil de pasar por alto, pero es una parte importante de la experiencia global del usuario.
ms.assetid: 26f5a8dc-27b2-4c2d-a05a-f942784c3cf9
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: a98bf29da1169ad43a3b1d16ab52298d62612037
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104555707"
---
# <a name="printing-design-basics"></a>Impresión (conceptos básicos del diseño)

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

La impresión es la experiencia del usuario en papel. Es fácil de pasar por alto, pero es una parte importante de la experiencia global del usuario.

En este artículo, la *impresión* hace referencia a la experiencia del usuario en papel, donde la salida se dirige al papel en lugar de a la pantalla. El *formato compatible con impresoras* hace referencia a las modificaciones que el programa puede realizar en la salida de la pantalla de presentación para que sea más adecuada para la salida de papel.

A pesar de la predicción, la informática daría lugar a la "oficina sin papel", sorprendentemente lo bastante posible. Se distribuyen copias impresas de presentaciones de Microsoft PowerPoint, se imprimen los artículos que se detectan en línea, pero se quiere investigar más detenidamente más adelante, se imprimen mensajes de correo electrónico o currículos importantes que se han recibido en formato electrónico, etc. Aunque es fácil pasar por alto la impresión al diseñar una interfaz de usuario, recuerde que la impresión es una parte importante de la experiencia de usuario global.

**Nota:** Las instrucciones relacionadas con los [cuadros de diálogo comunes](win-common-dlg.md) se presentan en un artículo independiente.

## <a name="is-this-the-right-user-interface"></a>¿Es la interfaz de usuario correcta?

Para decidir si el programa debe admitir la impresión, tenga en cuenta estas preguntas:

-   **¿Qué tipo de programa está diseñando?** El tipo de programa es un buen indicador del nivel de compatibilidad de impresión adecuado. La creación de documentos e imágenes, la visualización y la exploración de programas necesitan un soporte de impresión excelente, mientras que otros tipos de programas solo pueden necesitar una compatibilidad de impresión a un menor grado. (Para obtener una lista de tipos de programa, consulte la sección [patrones de impresión](#printing-patterns) de este artículo).
-   **¿El programa se usa en escenarios que se benefician de la salida de papel directo?** Si es así, es más conveniente agregar soporte de impresión al programa que para requerir a los usuarios que copien los datos en otro programa para imprimirlos.

## <a name="design-concepts"></a>Conceptos de diseño

### <a name="design-your-program-to-eliminate-unnecessary-printing"></a>Diseñar el programa para eliminar la impresión innecesaria

Hay muchas razones por las que los usuarios necesitan imprimir algunas que son buenas, algunas de las cuales son menos. Los usuarios deben imprimir porque quieren, no porque deben hacerlo. Requerir que los usuarios impriman puede ser un signo de las características que faltan. Por ejemplo, en los usuarios anteriores tenía que imprimir documentos para realizar comentarios y sugerir revisiones, pero ahora los usuarios pueden realizar estas tareas directamente en los documentos de Microsoft Word. **Revise los escenarios del programa que impliquen la impresión y, en el mejor de los casos, asegúrese de que la necesidad de imprimir es opcional y no el resultado de las características que faltan.**

También merece la pena recordar que el ahorro de recursos, como el papel y la tinta, es útil de forma práctica y ahorra dinero a las organizaciones a largo plazo.

### <a name="understand-the-differences-between-screen-display-and-print"></a>Descripción de las diferencias entre la presentación de pantalla y la impresión

Aunque hay muchas similitudes entre la presentación de la salida y la impresión, también hay muchas diferencias. Imprimir salida:

-   **Tiene un alto ppp.** La salida de la presentación suele estar en 96 o 120 puntos por pulgada (PPP), mientras que la salida de la impresora suele tener una velocidad de 600 ppp o superior.
-   **Tiene fuentes óptimas diferentes.** Aunque las fuentes bien diseñadas funcionan bien para mostrar e imprimir, las fuentes serif son más legibles en resoluciones altas de grandes cantidades de texto que las fuentes Sans Serif. Por lo tanto, las grandes cantidades de texto que se destinan principalmente a imprimir deben usar una fuente serif, mientras que el texto destinado principalmente a mostrarse debe usar una fuente sans serif. Para obtener más información, vea [fuentes](vis-fonts.md) (Segoe UI).
-   **Tiene relación de aspecto.** La presentación normalmente tiene una [relación de aspecto](glossary.md) baja (4:3 o 5:4), mientras que la impresión usa una relación de aspecto alta (8.5:11 ó 1:1.4142 según los tamaños de página estándar). Esto se debe a que la impresión en [modo vertical](glossary.md) es más común que el [modo horizontal](glossary.md).
-   **Tiene páginas.** Por lo tanto, la salida imprime:
    -   Tiene tamaños de página estándar. El estándar en el Estados Unidos y Canadá es 8,5 "X11". la norma en todo el mundo es el papel A4.
    -   Tiene saltos de página.
    -   Tiene márgenes de página.
    -   Tiene encabezados y pies de página.
    -   Tiene una salida de una o dos caras.
    -   Puede tener varias copias.
    -   Puede imprimirse sin orden o de manera selectiva.
-   **Tiene muchas opciones.** Es posible que los usuarios deseen elegir una impresora y un tamaño de papel, opciones de impresora (como la calidad de impresión, impresión a doble cara y grapado), el número de copias, los intervalos de páginas, la intercalación y el formato de impresión.
-   **Lleva tiempo y dinero.** Puede tardar una cantidad considerable de tiempo en imprimir un documento grande o una foto de alta calidad, y el costo del papel y la tinta se agregan con el tiempo. Por el contrario, la salida de pantalla es instantánea y esencialmente gratuita.
-   **Puede ser blanco y negro.** Muchas impresoras hoy en día son negras y blancas, mientras que algunas pantallas son monocromáticas.
-   **No es interactivo.** Los usuarios no pueden desplazarse por las páginas o los controles para ver más contenido. No pueden hacer clic en los vínculos o botones, ni mantener el mouse sobre los controles. El contenido interactivo no tiene ningún valor cuando se imprime.
-   **Se puede quedarse sin papel, tinta o tóner, o estar sin conexión.** Por lo tanto, la salida de papel necesita más control de errores y solución de problemas.

Estas diferencias pueden afectar al diseño de impresión. La creación de una buena experiencia de impresión requiere algo más que simplemente dirigir la salida del programa a la impresora.

### <a name="wysiwyg-and-the-evolving-requirements-of-screen-display"></a>WYSIWYG y los requisitos en constante evolución de la pantalla

Históricamente, el principio más fundamental para la experiencia del usuario de impresión se conoce como WYSIWYG ("lo que se ve es lo que se obtiene"). Este principio sugiere que debe haber una relación sólida entre lo que se muestra en la pantalla y lo que se imprime. Antes de que el WYSIWYG se convirtiera en una práctica estándar, a menudo no había ninguna relación entre las versiones de presentación e impresión de un documento. Los usuarios tenían que imprimir para ver el aspecto real del documento. El uso de WYSIWYG supuso una gran mejora en la productividad, ya que la mayoría de los programas en el momento estaban diseñados principalmente para la creación e impresión de documentos.

Hoy en día, es habitual que los sitios web optimicen la presentación y que el formato de impresión sea muy diferente. Además, tenemos diversos dispositivos informáticos (por ejemplo, teléfonos inteligentes y asistentes digitales personales) que a menudo necesitan una salida optimizada para pantallas pequeñas. Aunque WYSIWYG sigue siendo el mejor enfoque para los programas de creación de documentos, para otros programas suele tener más sentido optimizar para una variedad de dispositivos de destino. En el caso de estos programas, lo que se ve en la pantalla de un PC puede ser diferente de lo que se ve en otras pantallas de dispositivo, que puede ser diferente de lo que se obtiene en la página impresa.

### <a name="optimize-for-printing"></a>Optimizar para impresión

Los programas que no emplean una experiencia de impresión WYSIWYG estricta pueden seguir optimizando para la impresión de las siguientes maneras:

-   Cambiar el formato del diseño para el tamaño de la página de destino.
-   Proporcione la vista previa de impresión, preferiblemente con opciones de personalización sencillas que permitan a los usuarios experimentar directamente en el cuadro de diálogo de impresión (por ejemplo, arrastrando los márgenes).
-   Si es necesario, proporcione una opción de formato fácil de imprimir.
    -   Consolide documentos parciales independientes en un único documento.
    -   Quitar el fondo y otros elementos de diseño como los anuncios, especialmente si no son adecuados para una impresora en blanco y negro.
    -   Quitar elementos interactivos, como controles de navegación y botones de comando.
    -   Asegúrese de que todos los datos están visibles sin barras de desplazamiento ni se mantiene el mouse.

        **Versión de presentación:**

        ![captura de pantalla del informe optimizado para la pantalla ](images/exper-printing-image1.png)

        **Versión con impresora:**

        ![captura de pantalla del mismo informe optimizado para impresión ](images/exper-printing-image2.png)

        En la versión con impresora, todos los datos están visibles en la página impresa y se quitan los elementos interactivos.

    -   Reemplace los vínculos por su equivalente de texto.

        **Aceptable:**

        Para obtener más información, consulte la guía de la experiencia del usuario.

        **Optimizado para impresión:**

        Para obtener más información, consulte la guía de la experiencia del usuario ( https://msdn.microsoft.com/windowsvista/uxguide) .

-   Convierte el texto claro de un fondo oscuro en texto oscuro sobre un fondo blanco.

### <a name="include-the-right-print-options"></a>Incluir las opciones de impresión correctas

El cuadro de diálogo Opciones comunes de impresión proporciona opciones para:

-   Seleccione la impresora y el tamaño del papel.
-   Establecer las propiedades de la impresora.
-   Seleccione el intervalo de páginas, el número de copias y la intercalación.
-   Use ambos lados del papel.

El programa puede requerir opciones adicionales, como las opciones de contenido del documento (el contenido que se va a imprimir), las opciones de formato (cómo imprimir, como la calidad de impresión, los tamaños de las imágenes, la conexión a un marco) y las opciones de color. Si necesita proporcionar opciones adicionales, extienda el cuadro de diálogo común opciones de impresión. No cree un cuadro de diálogo de impresión personalizado.

Al diseñar las opciones de impresión, tenga en cuenta la experiencia al imprimir varios documentos. Lo más probable es que el siguiente trabajo de impresión sea muy similar al último trabajo de impresión. Optimizar la configuración predeterminada para las reimpresiones y los trabajos de impresión similares no hacen que los usuarios se inicien por completo cada vez.

### <a name="design-print-preview-for-performance-and-usability"></a>Diseño de vista previa de impresión para rendimiento y facilidad de uso

**Un trabajo de impresión incorrecto desperdicia tiempo y dinero. En el caso de los programas de creación de documentos, los usuarios deben poder evaluar los resultados antes de realizar la impresión real.** Una vista previa de impresión debe permitir a los usuarios:

-   Evalúe los márgenes, los saltos de página, la orientación de la página, los encabezados y los pies de página.
-   Desplazarse por todas las páginas.
-   Imprimir directamente desde la vista previa de impresión.

Algunos documentos complejos (como los dibujos CAD de diseño asistidos por PC \[ \] ) pueden tardar mucho tiempo en representarse. El rendimiento de la vista previa es importante, ya que la vista previa de impresión puede resultar bastante tediosa si se tarda algún tiempo en representar cada página. **Por lo tanto, es mejor tener una vista previa de impresión que se represente rápidamente y sea lo suficientemente precisa como para permitir que los usuarios evalúen los resultados de impresión que tener una vista previa completamente precisa que se represente lentamente.**

Al diseñar la vista previa de impresión, tenga en cuenta la tarea completa de preparar la impresión. ¿Qué van a buscar los usuarios? ¿Qué van a cambiar? Los programas de creación de documentos deben proporcionar una vista previa de impresión interactiva para que los usuarios puedan ajustar la configuración con frecuencia modificada, como los márgenes y los saltos de línea en la vista previa.

Sin embargo, en el mejor de los posible, el programa debería hacer lo correcto de forma predeterminada. Cuando sea necesario, advierta sobre las situaciones de impresión que es improbable que sean las prepensadas por el usuario. No confíe en que los usuarios encuentren problemas con la vista previa de impresión. Por ejemplo, supongamos que una hoja de cálculo tiene demasiadas columnas para imprimir en una sola página en modo vertical. Aunque el programa podría presentar un cuadro de diálogo de confirmación, una solución mejor es imprimir en modo horizontal automáticamente.

**Si solo hace cinco cosas...**

1.  Diseñar una experiencia de impresión adecuada para el tipo de programa.
2.  Revise los escenarios del programa que impliquen la impresión y, en la medida de lo posible, haga que sea necesario imprimir opcionalmente.
3.  Proporcione extensiones de impresión útiles personalizando el cuadro de diálogo Imprimir común. No cree un cuadro de diálogo de impresión personalizado para este fin.
4.  Optimice las opciones de impresión para reimpresiones y trabajos de impresión similares.
5.  Proporcione una característica de vista previa siempre que sea necesario.

## <a name="printing-patterns"></a>Patrones de impresión

El tipo de programa es el indicador principal de la experiencia de impresión adecuada:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Creación avanzada de documentos</strong><br/> Se usa para crear, ver e imprimir documentos de gama alta. La capacidad de crear copias impresas de alta calidad es una de las principales razones por las que existe el programa. Dirigido a usuarios expertos. <br/></td>
<td><strong>Objetivos del usuario:</strong> Resultados perfectos controlan el resultado de la impresión.<br/> <strong>Ejemplo:</strong> Microsoft Word<br/> <strong>Experiencia de impresión recomendada:</strong><br/>
<ul>
<li>Salida optimizada para impresión (WYSIWYG).</li>
<li>Características avanzadas de formato de documentos, con opciones para imprimir objetos grandes.</li>
<li>Opciones de impresión avanzadas, incluidos encabezados y pies de página. Las opciones de impresión relacionadas con documentos se guardan en el documento.</li>
<li>Vistas previas de impresión rápidas, precisas y eficaces.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Creación intermedia de documentos</strong><br/> Se utiliza para crear y ver documentos más complejos. La capacidad de crear copias impresas de buena calidad es importante, pero no necesariamente una de las razones principales por las que existe el programa. Dirigido a usuarios intermedios. <br/></td>
<td><strong>Objetivos del usuario:</strong> Buenos resultados con un esfuerzo mínimo. Cierto control sobre la salida de impresión.<br/> <strong>Ejemplos:</strong> La mayoría de los programas Microsoft Office, como Outlook y Excel.<br/> <strong>Experiencia de impresión recomendada:</strong><br/>
<ul>
<li>Salida optimizada para impresión (WYSIWYG).</li>
<li>Algunas características de formato de documento, con capacidad para imprimir objetos grandes sin truncamiento.</li>
<li>Algunas opciones de impresión personalizadas, incluidos los encabezados y pies de página.</li>
<li>Las vistas previas de impresión precisas y fáciles de usar.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Creación de documentos simples</strong><br/> Se utiliza para crear y ver documentos simples. Dirigido a todos los usuarios. <br/></td>
<td><strong>Objetivos del usuario:</strong> Compatibilidad con impresión básica con las opciones de impresión estándar. Los usuarios esperan buenos resultados sin ningún ajuste.<br/> <strong>Ejemplos:</strong> WordPad, Paint.<br/> <strong>Experiencia de impresión recomendada:</strong><br/>
<ul>
<li>La salida puede estar optimizada para la impresión (WYSIWYG), pero esto no es necesario.</li>
<li>Algunas características de formato de documento, con capacidad para imprimir objetos grandes sin truncamiento.</li>
<li>Opciones de impresión estándar; las opciones de impresión personalizadas son opcionales.</li>
<li>Vista previa de impresión simple o no.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Visores de documentos</strong><br/> Se usa para ver documentos. Los usuarios no pueden cambiar el formato o el contenido del documento. <br/></td>
<td><strong>Objetivos del usuario:</strong> Compatibilidad con impresión básica con las opciones de impresión estándar. Los usuarios esperan buenos resultados sin ningún ajuste. Los problemas de impresión se controlan automáticamente porque los usuarios no pueden modificar el documento.<br/> <strong>Ejemplo:</strong> Windows Internet Explorer<br/> <strong>Experiencia de impresión recomendada:</strong><br/>
<ul>
<li>La salida puede estar optimizada para la impresión (WYSIWYG), pero esto no es necesario.</li>
<li>El programa controla automáticamente los saltos de página, elimina páginas en blanco, trata objetos grandes y quita los elementos de fondo y otros elementos de diseño.</li>
<li>Opciones de impresión estándar; las opciones de impresión personalizadas son opcionales.</li>
<li>Vista previa de impresión simple o no.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Utilidades o aplicaciones de línea de negocio</strong><br/> Se utiliza para realizar tareas sencillas y específicas. Dirigido a todos los usuarios. <br/></td>
<td><strong>Objetivos del usuario:</strong> Capacidad de exportar los datos seleccionados de forma eficaz. Los usuarios esperan buenos resultados sin ningún ajuste. A menudo, para estos programas, los usuarios se sorprenden de una manera agradable de encontrar compatibilidad con la impresión.<br/> <strong>Experiencia de impresión recomendada:</strong><br/>
<ul>
<li>La compatibilidad con la impresión es opcional en función de los escenarios admitidos.</li>
<li>La salida puede estar optimizada para la impresión (WYSIWYG), pero esto no es necesario.</li>
<li>Algunas características de formato del documento. Puede ser aceptable si se truncan objetos grandes.</li>
<li>Opciones de impresión estándar.</li>
<li>Las vistas previas de impresión son opcionales.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a>Directrices

### <a name="general"></a>General

-   **No imprima páginas o páginas en blanco con solo encabezados y pies de página.** Sin embargo, imprima páginas en blanco si los encabezados o pies de página contienen números de página y se puede hacer referencia a ellos en otra parte.
-   **Poner en cola completamente todos los trabajos de impresión pendientes antes de cerrar un programa.**

### <a name="formatting-pages"></a>Aplicar formato a páginas

-   **Cambiar el formato del diseño del texto para que quepa en el tamaño de la página de destino.** No trunque nunca el texto.
-   Si los usuarios no controlan el formato del documento:
    -   **Controle automáticamente objetos grandes mediante el escalado, la rotación o la división entre páginas.** Para obtener más instrucciones sobre cómo imprimir objetos grandes, vea objetos de gran [tamaño](#oversized-objects).
    -   **Optimice los saltos de página para eliminar páginas en blanco y casi en blanco.**
    -   **Convierte el texto claro de un fondo oscuro en texto oscuro sobre un fondo blanco.**
    -   **Quitar el fondo y otros elementos de diseño,** especialmente si no son adecuados para una impresora en blanco y negro.
-   **Si el programa presenta documentos parciales independientes, proporcione una opción de formato compatible con la impresora para consolidarlos en un único documento para imprimirlos.**
-   **Quitar elementos interactivos:**
    -   Quitar controles de navegación y botones de comando.
    -   Asegúrese de que todos los datos están visibles sin barras de desplazamiento.
    -   Reemplace los vínculos por su equivalente de texto.

        **Aceptable:**

        Para obtener más información, consulte la guía de la experiencia del usuario.

        **Optimizado para impresión:**

        Para obtener más información, consulte la guía de la experiencia del usuario ( https://msdn.microsoft.com/windowsvista/uxguide) .

        En este ejemplo, el vínculo se reemplaza por su equivalente de texto entre paréntesis.

    -   Mover información útil que se muestra al mantener el mouse en línea.

### <a name="oversized-objects"></a>Objetos sobredimensionados

El control de objetos grandes, como hojas de cálculo, gráficos y fotos, es un problema exclusivo de la impresión. Elija uno de los enfoques siguientes:

-   **Escale el objeto para que quepa en la página.** Este enfoque funciona bien si el objeto solo es ligeramente demasiado grande para imprimirlo, mantener el objeto en una sola página es importante y el objeto sigue siendo legible cuando se reduce verticalmente.

    ![captura de pantalla de la foto escalada a la mitad de una página ](images/exper-printing-image3.png)

    En este ejemplo, la imagen grande se escala para ajustarse a la página.

-   **Gire la página.** Este enfoque funciona bien cuando algunas páginas se imprimen mejor en modo horizontal en modo vertical (y viceversa).

    ![captura de pantalla de la fotografía horizontal girada a vertical ](images/exper-printing-image4.png)

    En este ejemplo, la imagen grande se gira para ajustarse mejor a la página.

-   **Imprime el objeto en varias páginas.** El enfoque funciona bien cuando el objeto no se puede escalar o no se debe escalar, y el giro de la página no es de ayuda o no se desea. Si el objeto tiene límites internos (como los divisores de columna y fila de una hoja de cálculo), divida las páginas en estos límites en lugar de en el contenido. Además, repita los elementos necesarios para comprender la página, como leyendas o encabezados de columna. Al dividir un objeto en varias páginas, asigne los números de página en orden de lectura (de izquierda a derecha, de arriba abajo).

    ![captura de pantalla de los encabezados de columna repetidos en la siguiente página ](images/exper-printing-image5.png)

    En este ejemplo, la tabla grande se imprime en dos páginas. Los encabezados de columna se conservan de la página a la página para facilitar la comprensión rápida.

-   **Trunque el objeto** (imprimir solo la parte del objeto todavía visible después del truncamiento). Este enfoque es la solución más sencilla de implementar, pero probablemente sea lo menos aceptable. Tenga en cuenta también que el truncamiento nunca es aceptable para el texto.

    ![captura de pantalla de la mitad de la fotografía ancha en la página vertical ](images/exper-printing-image6.png)

    En este ejemplo, se trunca la imagen grande.

### <a name="headers-and-footers"></a>Encabezados y pies de página

-   **Proporcione encabezados y pies de página para programas de creación de documentos intermedios y avanzados.** Considere la posibilidad de proporcionar encabezados y pies de página para otros tipos de programas si se usan para documentos de páginas diferentes.
-   **Crear encabezados y pies de página personalizables.** Permite a los usuarios definir las partes izquierda, central y derecha.
    -   En el caso de los encabezados, coloque el nombre del documento en el lado izquierdo de forma predeterminada.
    -   En el caso de los pies de página, coloque los derechos de autor o de fuente del documento en el lado izquierdo y el número de página del lado derecho de forma predeterminada.
-   **Use la ruta de acceso y las direcciones URL de archivo descriptivos.** Mostrar espacios como espacios, no en "%20".

### <a name="print-commands"></a>Comandos de impresión

-   **En el caso de las barras de menús y los menús contextuales, use el comando imprimir que muestra el cuadro de diálogo común opciones de impresión.** Use un botón de puntos suspensivos para indicar que se requiere información adicional.

    ![captura de pantalla del menú Archivo, comando Imprimir seleccionado ](images/exper-printing-image7.png)

    En este ejemplo, el comando Print tiene puntos suspensivos para indicar que mostrará el cuadro de diálogo común opciones de impresión para obtener más información.

-   **En el caso de las barras de herramientas utilizadas con una barra de menús, use un comando de impresión inmediato.** Al hacer clic en el botón, se imprime una sola copia del documento en la impresora predeterminada. Estos comandos de la barra de herramientas deberían ser inmediatos. Para indicar que el comando es inmediato, coloque la impresora predeterminada en la información sobre herramientas. Los usuarios pueden tener acceso al comando Imprimir completo desde la barra de menús.

    ![captura de pantalla del icono de la impresora y su información sobre herramientas ](images/exper-printing-image8.png)

    En este ejemplo, el comando imprimir de una barra de herramientas se imprime inmediatamente en lugar de mostrar el cuadro de diálogo común opciones de impresión. La colocación de la impresora predeterminada en la información sobre herramientas proporciona un refuerzo de texto que el usuario omite en el cuadro de diálogo.

-   **En el caso de las barras de herramientas utilizadas sin una barra de menús, use un botón de expansión de impresión.** Al hacer clic en el botón, se imprime una sola copia del documento en la impresora predeterminada. Al hacer clic en la parte de la flecha del botón, se muestra un menú con los comandos impresión completa, vista previa de impresión y configurar página.

    ![captura de pantalla del icono de la impresora en el botón de expansión ](images/exper-printing-image9.png)

    En este ejemplo, la barra de herramientas de Windows Internet Explorer usa un control de botón de expansión para proporcionar todos los comandos de impresión.

-   **En la interfaz de usuario de comandos de la cinta de opciones, coloque el comando imprimir en el menú aplicación.**

    ![captura de pantalla de los comandos situados verticalmente a la izquierda ](images/exper-printing-image10.png)

    En las cintas de opciones, se tiene acceso al comando Print mediante el menú de la aplicación.

### <a name="print-options"></a>Opciones de impresión

-   **No cree un cuadro de diálogo Opciones de impresión personalizadas.** Si debe proporcionar opciones adicionales, extienda el cuadro de diálogo común opciones de impresión. No use un cuadro de diálogo independiente para otras opciones de impresión.

**Incorrecto:**

![captura de pantalla del cuadro de diálogo Opciones de impresión personalizadas ](images/exper-printing-image11.png)

En este ejemplo, Fabrikam usa incorrectamente un cuadro de diálogo independiente para otras opciones de impresión.

**Desarrolladores:** Para obtener información sobre cómo extender el cuadro de diálogo de impresión común, vea [estructura de PRINTDLGEX](/windows/win32/api/commdlg/ns-commdlg-printdlgexa).

-   **Al extender el cuadro de diálogo común de opciones de impresión, no duplique las características que ya se hayan proporcionado.**
-   **Si es probable que los usuarios mantengan la configuración de un trabajo de impresión al siguiente, haga que dichos valores sean los predeterminados.** Para el primer trabajo de impresión después del inicio del programa, use los valores predeterminados estándar, incluida la impresora predeterminada. Para los trabajos de impresión posteriores en la [instancia](glossary.md)del programa, conserve la última impresora y el tamaño de papel seleccionados. No conserve el número de copias o intervalos de páginas, ya que es mucho menos probable que se vuelvan a seleccionar más adelante.
-   **Optimice la configuración quitando las opciones que actualmente no se aplican.** Quitar las opciones incoherentes con las capacidades de la impresora o características seleccionadas del documento actual. Por ejemplo, una aplicación de impresión fotográfica podría limitar las combinaciones de tamaño de papel, tipo de papel y calidad de impresión que ofrecen los mejores resultados, por lo que elegir una opción de papel brillante podría quitar los sobres de los formatos de papel. Si, por alguna razón, los usuarios desean ver todas las opciones, puede proporcionar esta capacidad a través de un control, como una casilla.

**Desarrolladores:** Para obtener información sobre cómo determinar las capacidades de la impresora seleccionada, vea [Print Schema](../printdocs/print-schema.md).

-   **Para programas de creación de documentos avanzados, guarde las opciones de impresión relacionadas con documentos en el documento.** Para estos programas, las opciones de impresión son una parte integral del documento.
-   **Para otros tipos de programas, guarde la configuración por usuario.**
-   **Considere la posibilidad de seleccionar una impresora no predeterminada para la impresión especializada.** Por ejemplo, una aplicación de impresión fotográfica siempre podría seleccionar la última impresora usada por el programa, independientemente de la impresora predeterminada del sistema. Al hacerlo, se supone que la impresora predeterminada del sistema no es probable que sea una impresora fotográfica. Estos programas deben guardar la configuración de la última impresora seleccionada.
-   **No bloquee el programa al detectar las capacidades de la impresora.** Al hacerlo, se presenta una experiencia de usuario deficiente. En su lugar, puede:
    -   Realice la detección de la capacidad de la impresora en un subproceso independiente.
    -   Tiempo de espera transcurridos 10 segundos.
    -   Proporcione un cuadro de diálogo para permitir que los usuarios puedan cancelar.

![captura de pantalla del cuadro de diálogo "conectando a" ](images/exper-printing-image12.png)

En este ejemplo, el cuadro de diálogo facilita la cancelación de la detección de la capacidad de la impresora si el usuario decide que la tarea está tardando demasiado.

### <a name="print-previews"></a>Vistas previas de impresión

-   **Proporcione una característica de vista previa de impresión siempre que sea necesario.** Todos los programas de creación de documentos se benefician de las vistas previas de impresión, pero los usuarios no los esperan en programas de creación de documentos simples. Para programas de creación de documentos avanzados, considere la posibilidad de tener compatibilidad con la vista previa de impresión directamente en la ventana principal del programa.

![captura de pantalla de la página que se muestra en la vista previa de impresión ](images/exper-printing-image13.png)

En este ejemplo, Word tiene compatibilidad con la vista previa de impresión en la ventana principal del programa.

-   Proporcionar características de vista previa de impresión que permitan a los usuarios:
    -   Evalúe los márgenes, los saltos de página, la orientación de la página, los encabezados y los pies de página.
    -   Desplazarse por todas las páginas.
    -   Imprimir directamente desde la vista previa de impresión.

Considere la posibilidad de proporcionar una vista previa de impresión interactiva para que los usuarios puedan ajustar la configuración modificada con frecuencia, como los márgenes y saltos de línea, directamente en la vista previa.

-   **Las páginas de vista previa de impresión se representan en un segundo.** Es mejor tener una vista previa de impresión que se represente rápidamente y sea lo suficientemente precisa como para permitir que los usuarios evalúen los resultados de impresión que tener una vista previa completamente precisa que se represente lentamente.
-   En **el caso de los programas de creación de documentos avanzados, considere la posibilidad de extender el cuadro de diálogo Imprimir estándar mediante la incorporación de la funcionalidad de vista previa directamente en él,** en lugar de crear un cuadro de diálogo independiente para él.
-   **Proporcione un botón obvio para cerrar el modo de vista previa.**

![captura de pantalla del icono cerrar vista previa de impresión y etiqueta ](images/exper-printing-image14.png)

El modo de vista previa de impresión de Word tiene un comando de cierre de vista previa obvio.

### <a name="printing-errors"></a>Errores de impresión

**Nota:** Una vez que el trabajo de impresión se ha puesto en cola en la impresora, Windows es responsable de los errores posteriores. El programa solo tiene que controlar los errores que se producen antes de que el trabajo de impresión se ponga en cola.

-   **Antes de poner en cola un trabajo de impresión, busque posibles problemas de impresión que el usuario pueda corregir.** Presente una confirmación clara y concisa antes de continuar con la impresión. Siempre que sea posible, ofrezca la posibilidad de corregir el problema automáticamente. Si lo hace, puede evitar una pérdida de tiempo y dinero.

## <a name="text"></a>Texto

-   Para la opción de imprimir en ambas caras del papel, etiquete la opción Imprimir de doble cara. No use la frase dúplex manual.

## <a name="documentation"></a>Documentación

-   Use imprimir, no imprimir, como un verbo.
-   Es aceptable usar PrintOut para hacer referencia al resultado de un trabajo de impresión.
-   Usar cola de impresión, no cola de impresora.

