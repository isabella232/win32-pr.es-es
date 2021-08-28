---
title: Impresión (conceptos básicos de diseño)
description: La impresión es la experiencia del usuario en papel. Es fácil pasar por alto, pero es una parte importante de la experiencia general del usuario.
ms.assetid: 26f5a8dc-27b2-4c2d-a05a-f942784c3cf9
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 125c0eab965597c3e359f323f43b8881ff50b754
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482161"
---
# <a name="printing-design-basics"></a>Impresión (conceptos básicos de diseño)

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

La impresión es la experiencia del usuario en papel. Es fácil pasar por alto, pero es una parte importante de la experiencia general del usuario.

En este artículo, *la impresión hace* referencia a la experiencia del usuario en papel, donde la salida se dirige al papel en lugar de a la pantalla. *El formato descriptivo de la impresora* hace referencia a las modificaciones que el programa puede realizar en la salida de la pantalla que lo hace más adecuado para la salida del papel.

A pesar de la predicción de que la computación daría lugar a la "oficina sin papel", sorprendentemente ya se imprime tanto como nunca. Distribuimos copias en disco de las presentaciones de Microsoft PowerPoint, imprimemos artículos que detectamos en línea, pero queremos investigar más detenidamente más adelante, imprimemos correos electrónicos importantes o reanudaciones que hemos recibido en formato electrónico, etc. Aunque es fácil pasar por alto la impresión al diseñar una interfaz de usuario, recuerde que la impresión es una parte importante de la experiencia general del usuario.

**Nota:** Las instrucciones relacionadas [con los diálogos comunes](win-common-dlg.md) se presentan en un artículo independiente.

## <a name="is-this-the-right-user-interface"></a>¿Es la interfaz de usuario adecuada?

Para decidir si el programa necesita admitir la impresión, tenga en cuenta estas preguntas:

-   **¿Qué tipo de programa está diseñando?** El tipo de programa es un buen indicador del nivel adecuado de compatibilidad con la impresión. Los programas de creación, visualización y exploración de documentos e imágenes necesitan una excelente compatibilidad con la impresión, mientras que otros tipos de programas solo pueden necesitar compatibilidad con la impresión en menor medida. (Para obtener una lista de tipos de programa, consulte la [sección Patrones de](#printing-patterns) impresión de este artículo).
-   **¿Se usa el programa en escenarios que se benefician de la salida directa del papel?** Si es así, es más conveniente agregar compatibilidad con la impresión al programa que exigir a los usuarios que copien los datos en otro programa para imprimirlos.

## <a name="design-concepts"></a>Conceptos de diseño

### <a name="design-your-program-to-eliminate-unnecessary-printing"></a>Diseño del programa para eliminar la impresión innecesaria

Hay muchas razones por las que los usuarios necesitan imprimir algunas que son buenas, otras menos. Los usuarios deben imprimir porque quieran, no porque deba hacerlo. Requerir que los usuarios impriman puede ser un signo de que faltan características. Por ejemplo, en el pasado, los usuarios tenían que imprimir documentos para realizar comentarios y sugerir revisiones, pero ahora los usuarios pueden realizar estas tareas directamente dentro de Microsoft Word documentos. **Revise los escenarios del programa que implican la impresión y, en la mejor medida de lo posible, asegúrese de que la necesidad de imprimir es opcional y no el resultado de las características que faltan.**

También merece la pena recordar que conservar recursos como papel y lápiz es útil desde el entorno y ahorra dinero a las organizaciones a largo plazo.

### <a name="understand-the-differences-between-screen-display-and-print"></a>Comprender las diferencias entre la pantalla y la impresión

Aunque hay muchas similitudes entre la salida de pantalla y la impresión, también hay muchas diferencias. Salida de impresión:

-   **Tiene un valor de ppp alto.** La salida de la pantalla suele estar en 96 o 120 puntos por pulgada (ppp), mientras que la salida de la impresora suele ser de 600 ppp o superior.
-   **Tiene diferentes fuentes óptimas.** Aunque las fuentes bien diseñadas funcionan bien para mostrar e imprimir, las fuentes serif son más legibles a alta resolución para grandes cantidades de texto que las fuentes sans serif. Por lo tanto, grandes cantidades de texto destinadas principalmente a la impresión deben usar una fuente serif, mientras que el texto destinado principalmente a la presentación debe usar una fuente sans serif. Para obtener más información, vea [Fuentes](vis-fonts.md) (Segoe UI).
-   **Tiene relación de aspecto.** La pantalla suele [](glossary.md) tener una relación de aspecto baja (4:3 o 5:4), mientras que la impresión usa una relación de aspecto alta (8.5:11 o 1:1.4142 según los tamaños de página estándar). Esto se debe a [que la impresión en modo](glossary.md) vertical es más común que el modo [horizontal.](glossary.md)
-   **Tiene páginas.** Por lo tanto, imprima la salida:
    -   Tiene tamaños de página estándar. El estándar del Estados Unidos y Canadá es de 8,5 "x11"; el estándar en todas las demás partes es el documento A4.
    -   Tiene saltos de página.
    -   Tiene márgenes de página.
    -   Tiene encabezados y pies de página.
    -   Tiene una salida de una o dos lados.
    -   Puede tener varias copias.
    -   Se puede imprimir de forma no manual o selectiva.
-   **Tiene muchas opciones.** Es posible que los usuarios quieran elegir un tamaño de impresora y papel, opciones de impresora (como calidad de impresión, impresión de doble cara y estapling), número de copias, intervalos de página, intercalación y formato de impresión.
-   **Lleva tiempo y dinero.** Puede tardar mucho tiempo en imprimir un documento grande o una foto de alta calidad, y el costo del papel y la entrada de lápiz aumenta con el tiempo. Por el contrario, la salida de la presentación es instantánea y esencialmente libre.
-   **Puede ser blanco y negro.** En la actualidad, muchas impresoras son en blanco y negro, mientras que pocas pantallas son monocromáticas.
-   **No es interactivo.** Los usuarios no pueden desplazarse por páginas ni controles para ver más contenido. No pueden hacer clic en vínculos ni botones, ni mantener el puntero sobre los controles. El contenido interactivo no tiene ningún valor cuando se imprime.
-   **Puede que se le queme el papel, la entrada de lápiz o elner, o estar sin conexión.** Por lo tanto, la salida del papel necesita más control de errores y solución de problemas.

Estas diferencias pueden afectar al diseño de impresión. La creación de una buena experiencia de impresión requiere algo más que dirigir la salida del programa a la impresora.

### <a name="wysiwyg-and-the-evolving-requirements-of-screen-display"></a>WYSIWYG y los requisitos en constante evolución de la pantalla

Históricamente, el principio más fundamental para la experiencia del usuario de impresión se conoce como WYSIWYG ("lo que se ve es lo que se obtiene"). Este principio sugiere que debe haber una relación fuerte entre lo que se ve en la pantalla y lo que se imprime. Antes de que WYSIWYG se convirtiese en una práctica estándar, a menudo no había ninguna relación entre las versiones de presentación e impresión de un documento. Los usuarios tenían que imprimir para ver el aspecto del documento en papel. El uso de WYSIWYG fue una gran mejora en la productividad porque la mayoría de los programas en ese momento se diseñaron principalmente para la creación e impresión de documentos.

En la actualidad, es habitual que los sitios web se optimicen para la presentación, y su formato descriptivo para impresoras puede parecer muy diferente. Además, tenemos diversos dispositivos informáticos (por ejemplo, teléfonos inteligentes y asistentes digitales personales) que a menudo necesitan una salida optimizada para pantallas pequeñas. Aunque WYSIWYG sigue siendo el mejor enfoque para los programas de creación de documentos, para otros programas a menudo tiene más sentido optimizar para una variedad de dispositivos de destino. Para estos programas, lo que se ve en una pantalla de pc puede ser diferente de lo que se ve en otras pantallas de dispositivo, que pueden ser diferentes de lo que se obtiene en la página impresa.

### <a name="optimize-for-printing"></a>Optimización para la impresión

Los programas que no emplean una experiencia de impresión WYSIWYG estricta pueden seguir optimizando la impresión de las maneras siguientes:

-   Vuelva a formatear el diseño para el tamaño de página de destino.
-   Proporcione la vista previa de impresión, preferiblemente con opciones de personalización sencillas que permiten a los usuarios experimentar directamente en el cuadro de diálogo de impresión (por ejemplo, arrastrar márgenes).
-   Si es necesario, proporcione una opción de formato compatible con la impresora.
    -   Consolide documentos parciales independientes en un único documento.
    -   Quite los fondos y otros elementos de diseño, como los anuncios, especialmente si no son adecuados para una impresora en blanco y negro.
    -   Quite los elementos interactivos, como los controles de navegación y los botones de comando.
    -   Asegúrese de que todos los datos están visibles sin barras de desplazamiento ni mantener el puntero sobre él.

        **Versión para mostrar:**

        ![captura de pantalla del informe optimizado para pantalla ](images/exper-printing-image1.png)

        **Versión compatible con impresoras:**

        ![captura de pantalla del mismo informe optimizado para impresión ](images/exper-printing-image2.png)

        En la versión compatible con la impresora, todos los datos están visibles en la página impresa y se quitan los elementos interactivos.

    -   Reemplace los vínculos por su equivalente de texto.

        **Aceptable:**

        Para obtener más información, vea Guía de UX.

        **Optimizado para impresión:**

        Para obtener más información, vea Guía de UX ( https://msdn.microsoft.com/windowsvista/uxguide) .

-   Convertir texto claro en un fondo oscuro en texto oscuro en un fondo blanco.

### <a name="include-the-right-print-options"></a>Incluir las opciones de impresión correctas

El cuadro de diálogo Opciones de impresión común proporciona opciones para:

-   Seleccione el tamaño de impresora y papel.
-   Establezca las propiedades de la impresora.
-   Seleccione el intervalo de páginas, el número de copias y la intercalación.
-   Use ambos lados del papel.

El programa puede requerir opciones adicionales, como opciones de contenido del documento (qué contenido se va a imprimir), opciones de formato (cómo imprimir, incluida la calidad de impresión, tamaños de imagen, ajuste al marco) y opciones de color. Si necesita proporcionar opciones adicionales, para ello, extienda el cuadro de diálogo común Opciones de impresión. No cree un cuadro de diálogo Imprimir personalizado.

Al diseñar las opciones de impresión, tenga en cuenta la experiencia al imprimir varios documentos. Lo más probable es que el siguiente trabajo de impresión sea muy similar al último trabajo de impresión. La optimización de la configuración predeterminada para las huellas digitales y trabajos de impresión similares no hace que los usuarios se inicien por completo cada vez.

### <a name="design-print-preview-for-performance-and-usability"></a>Diseño de la vista previa de impresión para mejorar el rendimiento y la facilidad de uso

**Un trabajo de impresión incorrecto pierde tiempo y dinero. En el caso de los programas de creación de documentos, los usuarios deben poder evaluar los resultados antes de realizar la impresión real.** Una vista previa de impresión debe permitir a los usuarios:

-   Evaluar márgenes, saltos de página, orientación de página, encabezados y pies de página.
-   Examine todas las páginas.
-   Imprimir directamente desde la vista previa de impresión.

Algunos documentos complejos (como dibujos CAD de diseño asistidos por pc) pueden \[ tardar mucho tiempo en \] representarse. El rendimiento de la versión preliminar es importante que una vista previa de impresión pueda ser bastante tediosa si tarda un tiempo en representar cada página. **Por lo tanto, es mejor tener una vista previa de impresión que se represente rápidamente y sea lo suficientemente precisa como para permitir a los usuarios evaluar los resultados de impresión que tener una vista previa completamente precisa que se represente lentamente.**

Al diseñar la vista previa de impresión, tenga en cuenta toda la tarea de preparación para imprimir. ¿Qué van a buscar los usuarios? ¿Qué van a cambiar? Los programas de creación de documentos deben proporcionar una vista previa de impresión interactiva para que los usuarios puedan ajustar la configuración cambiada con frecuencia, como los márgenes y los saltos de línea dentro de la versión preliminar.

Sin embargo, en la medida de lo posible, el programa debe hacer lo correcto de forma predeterminada. Cuando sea necesario, advertir sobre situaciones de impresión que no es probable que sean lo que el usuario ha previsto. No confíe en que los usuarios encuentran problemas con la versión preliminar de impresión. Por ejemplo, suponga que una hoja de cálculo tiene demasiadas columnas para imprimir en una sola página en modo vertical. Aunque el programa podría presentar un cuadro de diálogo de confirmación, una mejor solución es imprimir automáticamente en modo horizontal.

**Si solo hace cinco cosas...**

1.  Diseñe una experiencia de impresión adecuada para el tipo de programa.
2.  Revise los escenarios del programa que implican la impresión y, en la medida de lo posible, haga que la necesidad de imprimir sea opcional.
3.  Proporcione extensiones de impresión útiles personalizando el cuadro de diálogo Imprimir común. No cree un cuadro de diálogo Imprimir personalizado para este propósito.
4.  Optimice las opciones de impresión para las huellas digitales y trabajos de impresión similares.
5.  Proporcione una característica en versión preliminar siempre que corresponda.

## <a name="printing-patterns"></a>Patrones de impresión

El tipo de programa es el indicador principal de la experiencia de impresión adecuada:




| | | <strong>Creación avanzada de documentos</strong><br /> Se usa para crear, ver e imprimir documentos de gama alta. La capacidad de crear copias impresas de alta calidad es una de las razones principales por las que existe el programa. Dirigido a usuarios expertos. <br /> | <strong>Objetivos del usuario:</strong> Control detallado de los resultados perfectos sobre la salida de impresión.<br /><strong>Ejemplo:</strong> Microsoft Word<br /><strong>Experiencia de impresión recomendada:</strong><br /><ul><li>Salida optimizada para impresión (WYSIWYG).</li><li>Características avanzadas de formato de documentos, con opciones para imprimir objetos grandes.</li><li>Opciones avanzadas de impresión, incluidos encabezados y pies de página. Las opciones de impresión relacionadas con el documento se guardan en el propio documento.</li><li>Vistas previas de impresión rápidas, precisas y eficaces.</li></ul> | | <strong>Creación de documentos intermedios</strong><br /> Se usa para crear y ver documentos más complejos. La capacidad de crear copias impresas de buena calidad es importante, pero no necesariamente una de las razones principales por las que existe el programa. Dirigido a usuarios intermedios. <br /> | <strong>Objetivos de usuario:</strong> Buenos resultados con un esfuerzo mínimo. Control sobre la salida de impresión.<br /><strong>Ejemplos:</strong> La mayoría Microsoft Office programas, como Outlook y Excel.<br /><strong>Experiencia de impresión recomendada:</strong><br /><ul><li>Salida optimizada para impresión (WYSIWYG).</li><li>Algunas características de formato de documento, con la capacidad de imprimir objetos grandes sin truncamiento.</li><li>Algunas opciones de impresión personalizadas, incluidos encabezados y pies de página.</li><li>Vistas previas de impresión precisas y fáciles de usar.</li></ul> | | <strong>Creación de documentos sencilla</strong><br /> Se usa para crear y ver documentos simples. Dirigido a todos los usuarios. <br /> | <strong>Objetivos de usuario:</strong> Compatibilidad de impresión básica con opciones de impresión estándar. Los usuarios esperan buenos resultados sin ningún ajuste.<br /><strong>Ejemplos:</strong> WordPad, Paint.<br /><strong>Experiencia de impresión recomendada:</strong><br /><ul><li>La salida se puede optimizar para impresión (WYSIWYG), pero esto no es necesario.</li><li>Algunas características de formato de documento, con la capacidad de imprimir objetos grandes sin truncamiento.</li><li>Opciones de impresión estándar; las opciones de impresión personalizadas son opcionales.</li><li>Vistas previas de impresión simples o sin formato.</li></ul> | | <strong>Visores de documentos</strong><br /> Se usa para ver documentos. Los usuarios no pueden cambiar el contenido ni el formato del documento. <br /> | <strong>Objetivos de usuario:</strong> Compatibilidad de impresión básica con opciones de impresión estándar. Los usuarios esperan buenos resultados sin ningún ajuste. Los problemas de impresión se controlan automáticamente porque los usuarios no pueden modificar el documento.<br /><strong>Ejemplo:</strong> Windows Internet Explorer<br /><strong>Experiencia de impresión recomendada:</strong><br /><ul><li>La salida se puede optimizar para impresión (WYSIWYG), pero esto no es necesario.</li><li>El programa controla automáticamente los saltos de página, elimina las páginas en blanco, controla objetos grandes y quita fondos y otros elementos de diseño.</li><li>Opciones de impresión estándar; las opciones de impresión personalizadas son opcionales.</li><li>Vistas previas de impresión simples o sin formato.</li></ul> | | <strong>Utilidades o aplicaciones de línea de negocio</strong><br /> Se usa para realizar tareas sencillas y específicas. Dirigido a todos los usuarios. <br /> | <strong>Objetivos de usuario:</strong> Capacidad de exportar los datos seleccionados de forma eficaz. Los usuarios esperan buenos resultados sin ningún ajuste. A menudo, para estos programas, los usuarios se sorprendan de manera cómoda al encontrar compatibilidad con la impresión.<br /><strong>Experiencia de impresión recomendada:</strong><br /><ul><li>La compatibilidad con la impresión es opcional en función de los escenarios admitidos.</li><li>La salida se puede optimizar para impresión (WYSIWYG), pero esto no es necesario.</li><li>Algunas características de formato de documento. Podría ser aceptable si se truncan objetos grandes.</li><li>Opciones de impresión estándar.</li><li>Las vistas previas de impresión son opcionales.</li></ul> | 




 

## <a name="guidelines"></a>Directrices

### <a name="general"></a>General

-   **No imprima páginas en blanco ni páginas solo con encabezados y pies de página.** Sin embargo, imprima páginas en blanco si los encabezados o pies de página contienen números de página y es posible que se haga referencia a esos números de página en otro lugar.
-   **Resalte por completo los trabajos de impresión pendientes antes de apagar un programa.**

### <a name="formatting-pages"></a>Aplicación de formato a páginas

-   **Vuelva a formatear el diseño de texto para que se ajuste al tamaño de página de destino.** Nunca truncar texto.
-   Si los usuarios no controlan el formato del documento:
    -   **Controle automáticamente objetos grandes mediante el escalado, la rotación o la división entre páginas.** Para obtener más instrucciones sobre la impresión de objetos grandes, vea [Objetos sobredimensionados.](#oversized-objects)
    -   **Optimice los saltos de página para eliminar las páginas en blanco y casi en blanco.**
    -   **Convertir texto claro de un fondo oscuro en texto oscuro en un fondo blanco.**
    -   **Quite los fondos y otros elementos de diseño,** especialmente si no son adecuados para una impresora en blanco y negro.
-   **Si el programa presenta documentos parciales independientes, proporcione una opción de formato descriptivo para la impresora para consolidarlos en un único documento para imprimir.**
-   **Quitar elementos interactivos:**
    -   Quite los controles de navegación y los botones de comando.
    -   Asegúrese de que todos los datos están visibles sin barras de desplazamiento.
    -   Reemplace los vínculos por su equivalente de texto.

        **Aceptable:**

        Para obtener más información, consulte la Guía de experiencia de usuario.

        **Optimizado para impresión:**

        Para obtener más información, vea Guía de experiencia de usuario ( https://msdn.microsoft.com/windowsvista/uxguide) .

        En este ejemplo, el vínculo se reemplaza por su texto equivalente entre paréntesis.

    -   Mueva la información útil que se muestra al mantener el puntero a insertada.

### <a name="oversized-objects"></a>Objetos sobredimensionados

El control de objetos grandes, como hojas de cálculo, gráficos y fotos, es un problema único de impresión. Elija uno de los enfoques siguientes:

-   **Escale el objeto para que quepa en la página.** Este enfoque funciona bien si el objeto solo es ligeramente demasiado grande para imprimir, mantener el objeto en una sola página es importante y el objeto sigue siendo legible cuando se escala verticalmente.

    ![captura de pantalla de la foto escalada a la mitad de una página ](images/exper-printing-image3.png)

    En este ejemplo, la imagen grande se escala para ajustarse a la página.

-   **Girar la página.** Este enfoque funciona bien cuando algunas páginas se imprimen mejor en modo horizontal cuando están en modo vertical (y viceversa).

    ![captura de pantalla de la foto horizontal girada a vertical ](images/exper-printing-image4.png)

    En este ejemplo, la imagen grande se gira para ajustarse mejor a la página.

-   **Imprima el objeto en varias páginas.** El enfoque funciona bien cuando el objeto no se puede escalar o no se debe escalar, y la rotación de la página no ayuda o no se quiere. Si el objeto tiene límites internos (como los divisores de columna y fila de una hoja de cálculo), divida las páginas de estos límites en lugar de dentro del contenido. Además, repita los elementos necesarios para comprender la página, como leyendas o encabezados de columna. Al dividir un objeto en varias páginas, asigne los números de página en orden de lectura (de izquierda a derecha, de arriba a abajo).

    ![captura de pantalla de los encabezados de columna repetidos en la página siguiente ](images/exper-printing-image5.png)

    En este ejemplo, la tabla grande se imprime en dos páginas. Los encabezados de columna se conservan de una página a otra para facilitar la comprensión rápida.

-   **Truncar el objeto** (imprimir solo la parte del objeto todavía visible después del truncamiento). Este enfoque es la solución más sencilla de implementar, pero es probable que sea la menos aceptable. Tenga en cuenta también que el truncamiento nunca es aceptable para el texto.

    ![captura de pantalla de la mitad de la foto ancha en la página vertical ](images/exper-printing-image6.png)

    En este ejemplo, se trunca la imagen grande.

### <a name="headers-and-footers"></a>Encabezados y pies de página

-   **Proporcione encabezados y pies de página para los programas de creación de documentos avanzados e intermedios.** Considere la posibilidad de proporcionar encabezados y pies de página para otros tipos de programas si se usan para documentos de varias páginas.
-   **Haga que los encabezados y pies de página se personalización.** Permitir a los usuarios definir las partes izquierda, central y derecha.
    -   Para los encabezados, coloque el nombre del documento en el lado izquierdo de forma predeterminada.
    -   En el caso de los pies de página, coloque el copyright o el origen del documento en el lado izquierdo y el número de página en el lado derecho, de forma predeterminada.
-   **Use direcciones URL y ruta de acceso de archivo descriptivos.** Mostrar espacios como espacios, no "%20".

### <a name="print-commands"></a>Comandos de impresión

-   **Para las barras de menús y los menús contextuales, use el comando Imprimir que muestra el cuadro de diálogo común Opciones de impresión.** Use puntos suspensivos para indicar que se requiere información adicional.

    ![captura de pantalla del menú de archivo, comando de impresión seleccionado ](images/exper-printing-image7.png)

    En este ejemplo, el comando Imprimir tiene puntos suspensivos para indicar que mostrará el cuadro de diálogo Común Opciones de impresión para obtener más información.

-   **Para las barras de herramientas usadas con una barra de menús, use un comando Imprimir inmediato.** Al hacer clic en el botón se imprime una sola copia del documento en la impresora predeterminada. Estos comandos de la barra de herramientas deben ser inmediatos. Para indicar que el comando es inmediato, coloque la impresora predeterminada en la información sobre herramientas. Los usuarios pueden acceder al comando Imprimir completo desde la barra de menús.

    ![captura de pantalla del icono de impresora y su información sobre herramientas ](images/exper-printing-image8.png)

    En este ejemplo, el comando Imprimir de una barra de herramientas se imprime inmediatamente en lugar de mostrar el cuadro de diálogo común Opciones de impresión. Colocar la impresora predeterminada en la información sobre herramientas proporciona un refuerzo textual de que el usuario omite el cuadro de diálogo.

-   **Para las barras de herramientas que se usan sin una barra de menús, use un botón Imprimir división.** Al hacer clic en el botón se imprime una sola copia del documento en la impresora predeterminada. Al hacer clic en la parte de flecha del botón, se coloca un menú con los comandos completos Imprimir, Vista previa de impresión y Configuración de página.

    ![captura de pantalla del icono de impresora en el botón de división ](images/exper-printing-image9.png)

    En este ejemplo, la barra Windows Internet Explorer de herramientas usa un control de botón de división para proporcionar todos los comandos de impresión.

-   **Para la interfaz de usuario del comando de la cinta de opciones, coloque el comando Imprimir en el menú de la aplicación.**

    ![captura de pantalla de comandos colocados verticalmente a la izquierda ](images/exper-printing-image10.png)

    Para las cintas de opciones, se accede al comando Imprimir mediante el menú de la aplicación.

### <a name="print-options"></a>Opciones de impresión

-   **No cree un cuadro de diálogo opciones de impresión personalizadas.** Si debe proporcionar opciones adicionales, extienda el cuadro de diálogo Opciones de impresión comunes. No use un cuadro de diálogo independiente para opciones de impresión adicionales.

**Incorrecto:**

![captura de pantalla del cuadro de diálogo opciones de impresión personalizadas ](images/exper-printing-image11.png)

En este ejemplo, Fabrikam usa incorrectamente un cuadro de diálogo independiente para opciones de impresión adicionales.

**Desarrolladores:** Para obtener información sobre cómo extender el cuadro de diálogo Imprimir común, vea [PRINTDLGEX (Estructura).](/windows/win32/api/commdlg/ns-commdlg-printdlgexa)

-   **Al extender el cuadro de diálogo común Opciones de impresión, no duplique ninguna de las características ya proporcionadas.**
-   **Si es probable que los usuarios mantengan la configuración de un trabajo de impresión al siguiente, haga que esa configuración sea la predeterminada.** Para el primer trabajo de impresión después del inicio del programa, use los valores predeterminados estándar, incluida la impresora predeterminada. Para los trabajos de impresión posteriores en la instancia [del programa](glossary.md), conserve la última impresora y el tamaño de papel seleccionados. No conserve el número de copias o intervalos de páginas, ya que es mucho menos probable que se vuelvan a elegir más adelante.
-   **Optimice la configuración quitando las opciones que actualmente no se aplican.** Quite las opciones que son incoherentes con las funciones de la impresora seleccionada o las características del documento actual. Por ejemplo, una aplicación de impresión con fotos podría limitar las combinaciones de tamaño de papel, tipo de papel y calidad de impresión que dan los mejores resultados, por lo que elegir una opción de papel con un aspecto glosario podría quitar sobres de los formatos de papel. Si por cualquier motivo los usuarios quieren ver todas las opciones, puede proporcionar esta capacidad a través de un control como una casilla.

**Desarrolladores:** Para obtener información sobre cómo determinar las funciones de la impresora seleccionada, vea [Esquema de impresión](../printdocs/print-schema.md).

-   **Para los programas avanzados de creación de documentos, guarde las opciones de impresión relacionadas con el documento en el propio documento.** Para estos programas, las opciones de impresión son una parte integral del documento.
-   **Para otros tipos de programas, guarde la configuración por usuario.**
-   **Considere la posibilidad de seleccionar una impresora no predeterminada para impresión especializada.** Por ejemplo, una aplicación de impresión de fotos siempre podría seleccionar la impresora usada por última vez por el programa, independientemente de la impresora predeterminada del sistema. Al hacerlo, se supone que la impresora predeterminada del sistema no es probable que sea una impresora de fotos. Estos programas deben guardar la configuración de la última impresora seleccionada.
-   **No bloquee el programa al detectar las funcionalidades de la impresora.** Al hacerlo, se presenta una experiencia de usuario deficiente. En su lugar, puede:
    -   Realice la detección de la funcionalidad de la impresora en un subproceso independiente.
    -   Tiempo de espera transcurridos 10 segundos.
    -   Proporcione un cuadro de diálogo para permitir a los usuarios cancelar.

![captura de pantalla del cuadro de diálogo "conectarse a" ](images/exper-printing-image12.png)

En este ejemplo, el cuadro de diálogo facilita la cancelación de la detección de la funcionalidad de impresora si el usuario decide que la tarea tarda demasiado.

### <a name="print-previews"></a>Vistas previas de impresión

-   **Proporcione una característica de vista previa de impresión siempre que sea necesario.** Todos los programas de creación de documentos se benefician de las vistas previas de impresión, pero los usuarios no los esperan en programas sencillos de creación de documentos. Para los programas avanzados de creación de documentos, considere la posibilidad de tener compatibilidad con la vista previa de impresión directamente en la ventana principal del programa.

![captura de pantalla de la página que se muestra en la vista previa de impresión ](images/exper-printing-image13.png)

En este ejemplo, Word tiene compatibilidad con la vista previa de impresión dentro de la ventana principal del programa.

-   Proporcione características de vista previa de impresión que permiten a los usuarios:
    -   Evalúe los márgenes, los saltos de página, la orientación de la página, los encabezados y los pies de página.
    -   Examine todas las páginas.
    -   Imprimir directamente desde la vista previa de impresión.

Considere la posibilidad de proporcionar una vista previa de impresión interactiva para que los usuarios puedan ajustar la configuración cambiada con frecuencia, como los márgenes y los saltos de línea directamente dentro de la versión preliminar.

-   **Hacer que las páginas de vista previa de impresión se represente en un segundo.** Es mejor tener una vista previa de impresión que se represente rápidamente y sea lo suficientemente precisa como para permitir a los usuarios evaluar los resultados de impresión que tener una vista previa completamente precisa que se represente lentamente.
-   **Para los programas de creación de** documentos avanzados, considere la posibilidad de ampliar el cuadro de diálogo Imprimir estándar incorporando la funcionalidad de vista previa directamente dentro de él, en lugar de crear un diálogo independiente para él.
-   **Proporcione un botón obvio para cerrar el modo de vista previa.**

![captura de pantalla del icono y la etiqueta de cierre de la vista previa de impresión ](images/exper-printing-image14.png)

El modo vista previa de impresión en Word tiene un comando de vista previa de cierre obvio.

### <a name="printing-errors"></a>Errores de impresión

**Nota:** Una vez que el trabajo de impresión se ha puesto en cola en la impresora, Windows responsable de los errores posteriores. El programa solo tiene que controlar los errores que se producen antes de que el trabajo de impresión se en cola.

-   **Antes de colar un trabajo de impresión, compruebe si hay posibles problemas de impresión que el usuario pueda corregir.** Presente una confirmación clara y concisa antes de continuar con la impresión. Siempre que sea posible, ofrezca para corregir el problema automáticamente. Si lo hace, puede evitar una pérdida de tiempo y dinero.

## <a name="text"></a>Texto

-   Para la opción de imprimir en ambos lados del papel, etiquete la opción Imprimir de dos caras. No use la frase Dúplex manual.

## <a name="documentation"></a>Documentación

-   Use print, no print out, como verbo.
-   Es aceptable usar printout para hacer referencia al resultado de un trabajo de impresión.
-   Use la cola de impresión, no la cola de impresoras.

