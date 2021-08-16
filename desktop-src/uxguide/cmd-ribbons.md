---
title: Barras de herramientas
description: Las cintas de opciones son la manera moderna de ayudar a los usuarios a encontrar, comprender y usar comandos de forma eficaz y directa \ 8212; con un número mínimo de clics, con menos necesidad de recurrir a la prueba y el error, y sin tener que hacer referencia a la Ayuda.
ms.assetid: 8a4699da-9840-4622-9e94-d6d5c4e7708c
ms.custom: contperf-fy21q1
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: db5a64d50bd225b714c2ff0578145c47c66bedb557dd067e0cdf89f369178b1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118042743"
---
# <a name="ribbons"></a>Barras de herramientas

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

Las cintas de opciones son la manera moderna de ayudar a los usuarios a encontrar, comprender y usar comandos de forma eficaz y directa con un número mínimo de clics, con menos necesidad de recurrir a pruebas y errores y sin tener que hacer referencia a la Ayuda.

Una cinta de opciones es una barra de comandos que organiza las características de un programa en una serie de pestañas en la parte superior de una ventana. El uso de una cinta de opciones aumenta la detectabilidad de características y funciones, permite un aprendizaje más rápido del programa en su conjunto y hace que los usuarios se sientan más controlados por su experiencia con el programa. Una cinta de opciones puede reemplazar la barra de menús tradicional y las barras de herramientas.

![captura de pantalla de una cinta de opciones ](images/cmd-ribbons-image1.png)

Una cinta de opciones típica.

Las pestañas de la cinta de opciones se componen de grupos, que son un conjunto etiquetado de comandos estrechamente relacionados. Además de las pestañas y los grupos, las cintas de opciones constan de:

- Un botón Aplicación, que presenta un menú de comandos que implican hacer algo con un documento o área de trabajo, como comandos relacionados con archivos.
- Una barra de herramientas de acceso rápido, que es una barra de herramientas pequeña y personalizable que muestra los comandos usados con frecuencia.
- Las pestañas principales son las pestañas que siempre se muestran.
- Pestañas contextuales, que solo se muestran cuando se selecciona un tipo de objeto determinado. Las pestañas que siempre se muestran se denominan pestañas principales.
- Un conjunto de pestañas es una colección de pestañas contextuales para un único tipo de objeto. Dado que los objetos pueden tener varios tipos (por ejemplo, un encabezado de una tabla que tiene una imagen es de tres tipos), puede haber varios conjuntos de pestañas contextuales mostrados a la vez.
- Pestañas modales, que son pestañas principales que se muestran con un modo temporal determinado, como la vista previa de impresión.
- Galerías, que son listas de comandos u opciones que se presentan gráficamente. Una galería basada en resultados muestra el efecto de los comandos u opciones en lugar de los propios comandos. Una galería en la cinta de opciones se muestra dentro de una cinta de opciones, en lugar de una ventana emergente.
- Información sobre herramientas mejorada, que explica de forma concisa sus comandos asociados y proporciona las teclas de método abreviado. También pueden incluir gráficos y referencias a la Ayuda. La información sobre herramientas mejorada reduce la necesidad de ayuda relacionada con comandos.
- Selectores de cuadros de diálogo, que son botones en la parte inferior de algunos grupos que abren cuadros de diálogo que contienen características relacionadas con el grupo.

Las cintas de opciones se introdujeron originalmente con Microsoft Office 2007. Para obtener información sobre Office necesita usar cintas de opciones y los muchos problemas que se resuelven al usar una cinta de opciones, consulte [La historia de la cinta de opciones](/archive/blogs/jensenh/the-story-of-the-ribbon).

> [!Note]  
> Las directrices relacionadas con [los menús,](cmd-menus.md)las [barras de herramientas,](cmd-toolbars.md)los [botones de](ctrl-command-buttons.md)comando y [los iconos](vis-icons.md) se presentan en artículos independientes.

## <a name="is-this-the-right-user-interface"></a>¿Es la interfaz de usuario adecuada?

Para decidir usar una cinta de opciones, tenga en cuenta estas preguntas:

### <a name="program-type"></a>Tipo de programa

- **¿Qué tipo de programa está diseñando?** El tipo de programa es un buen indicador de la utilidad de una cinta de opciones. Las cintas de opciones funcionan bien para los programas de creación y creación de documentos, así como para los visores de documentos y los exploradores. Las cintas de opciones pueden funcionar para otros tipos de programas, pero otras formas de presentación de comandos pueden ser más adecuadas. Por lo general, los programas ligeros deben tener una presentación de comandos ligera.

### <a name="discoverability-and-learning-issues"></a>Problemas de detectabilidad y aprendizaje

- **¿Los usuarios tienen problemas para encontrar comandos? ¿Los usuarios solicitan características que ya están en el programa?** Si es así, el uso de una cinta de opciones hará que los comandos sean más fáciles de encontrar al tener etiquetas autoexplicativas y la agrupación de comandos relacionados. El uso de una cinta de opciones también se escala mejor que las barras de menús y las barras de herramientas para el crecimiento futuro.
- **¿Los usuarios tienen problemas para comprender los comandos del programa? ¿Recurren a menudo a "prueba y error" para seleccionar el comando correcto o determinar cómo funcionan los comandos?** Si es así, el uso de una cinta de opciones con comandos orientados a resultados basados en galerías y vistas previas en vivo facilita la información de los comandos.

### <a name="command-characteristics"></a>Características del comando

- **¿Se presentan los comandos en varias ubicaciones? Si el programa ya existe, ¿se presentan los comandos en las barras de menús, las barras de herramientas, los paneles de tareas y dentro del propio área de trabajo?** Si es así, el uso de una cinta de opciones unificará los comandos en una sola ubicación, lo que facilita su búsqueda.
- **¿Los comandos se aplican a toda la ventana o solo a paneles específicos?** Las cintas de opciones funcionan mejor para los comandos que se aplican a toda la ventana o a objetos específicos. Los comandos locales funcionan mejor para paneles de ventana individuales.
- **¿Se pueden presentar directamente la mayoría de los comandos? Es decir, ¿los usuarios pueden interactuar con ellos con un solo clic? Si se accede a los comandos usados habitualmente desde menús y cuadros de diálogo, ¿se pueden refactorizar para que sean directos?** Aunque algunos comandos se pueden presentar mediante menús y cuadros de diálogo, presentar la mayoría de los comandos de esta manera desvirtúa la eficacia de una cinta de opciones, lo que posiblemente hace que una barra de menús sea una mejor opción.

### <a name="command-scale"></a>Escala de comandos

- **¿Hay un número reducido de comandos? ¿Se pueden presentar fácilmente los comandos usados con más frecuencia en una sola barra de herramientas sencilla?** El uso de una cinta de opciones merece la pena si la adición de pestañas principales y contextuales da como resultado una pestaña Inicio sencilla que se puede usar por sí sola para realizar las tareas más comunes. Si no es así, es posible que la ventaja de usar una cinta de opciones no justifique su peso adicional para un número reducido de comandos.
- **¿Hay un gran número de comandos? ¿El uso de una cinta de opciones requeriría más de siete pestañas principales? ¿Tendrían los usuarios que cambiar constantemente las pestañas para realizar tareas comunes?** Si es así, el uso de barras de herramientas (que no requieren cambiar las pestañas) y las ventanas de paleta [(que](cmd-toolbars.md) pueden requerir cambiar las pestañas, pero puede haber varias abiertas a la vez) podría ser una opción más eficaz.
- **¿Tienden los usuarios a usar un pequeño número de comandos la mayoría de las veces?** Si es así, pueden usar una cinta de opciones de forma eficaz colocando estos comandos en la pestaña Inicio. Cambiar constantemente las pestañas haría que una cinta de opciones sea demasiado ineficaz.
- **¿Se beneficia el programa de hacer que el área de contenido del programa sea lo más grande posible?** Si es así, el uso de una barra de menús y una sola barra de herramientas es más eficaz que una cinta de opciones. Sin embargo, si el programa requiere tres o más filas de barras de herramientas o usa paneles de tareas, el uso de una cinta de opciones es más eficaz.
- **¿Tienden los usuarios a trabajar en un área específica dentro de una ventana grande del programa durante largos períodos de tiempo?** Si es así, se beneficiarían de la proximidad de las mini barras de herramientas, las ventanas de paleta y los comandos directos. Realizar el recorrido de ida y vuelta desde el área de trabajo a la cinta de opciones sería demasiado ineficaz.
- **Para mayor eficacia y flexibilidad, ¿los usuarios necesitan realizar cambios significativos en el contenido, la ubicación o el tamaño de la presentación de comandos?** Si es así, las barras de herramientas personalizables y extensibles y las ventanas de paleta son una mejor opción. Tenga en cuenta que algunos tipos de barras de herramientas se pueden desacoplar para convertirse en ventanas de paleta, y las ventanas de paleta se pueden mover, cambiar de tamaño y personalizar.

Por último, considere esta pregunta final: ¿Merece la pena la mejora en la detectabilidad, la facilidad de aprendizaje, la eficacia y la productividad del costo del espacio adicional y la necesidad de pestañas para organizar **comandos?** Si es así, el uso de una cinta de opciones es una opción excelente. Si no está seguro, considere la posibilidad de probar la facilidad de uso de un diseño basado en cinta de opciones y compararlo con la mejor alternativa.

Las cintas de opciones son una forma nueva y atractiva de presentación de comandos y una excelente manera de modernizar un programa. Pero por atractivas que sean, no son la opción adecuada para cada programa.

**Incorrecto:**

![captura de pantalla de una cinta de opciones con una calculadora ](images/cmd-ribbons-image2.png)

No haga esto.

## <a name="seven-most-important-things"></a>Siete cosas más importantes

1. Elija una solución de comandos adecuada para el tipo de programa. El uso de una cinta de opciones debe hacer que un programa sea más sencillo, eficaz y fácil de usar nunca al contrario. Si no es adecuado usar una cinta de opciones, considere la posibilidad de usar comandos enriquecidos en su lugar.  
2. No subestime el desafío de crear una cinta de opciones eficaz. No espere que sea un puerto sencillo de las barras de menús y barras de herramientas existentes. Y no da por hecho que el uso de una cinta de opciones mejora automáticamente el programa. Estar dispuesto a confirmar el tiempo y el esfuerzo necesarios para un rediseño de comandos es un factor importante a la hora de decidir usar una cinta de opciones.  
3. Haga que los comandos se detecte. Elija un diseño de pestaña que tenga una asignación clara, obvia y única entre los comandos y las pestañas etiquetadas de forma descriptiva donde residen. Los usuarios deben poder determinar de forma rápida y segura qué pestaña tiene el comando que buscan y rara vez elegir la pestaña incorrecta.  
4. Haga que los comandos se explican por sí solos. Los usuarios deben comprender el efecto de un comando desde su etiqueta, icono, información sobre herramientas y vista previa. No deben tener que experimentar ni leer un tema de Ayuda para ver cómo funciona un comando.  
5. Haga que el uso de los comandos sea eficaz:
    - Los usuarios deben dedicar la mayor parte de su tiempo a la pestaña Inicio.
    - Los usuarios rara vez deben tener que cambiar las pestañas durante las tareas comunes.
    - Cuando la ventana está maximizada y los usuarios están en la pestaña correcta, los comandos usados con más frecuencia tienen el énfasis más visual y los usuarios pueden invocarlos con un solo clic. Los usuarios pueden realizar todos los demás comandos en la pestaña con un máximo de cuatro clics.
    - Los usuarios no deben tener que abrir cuadros de diálogo para proporcionar comandos y cambiar atributos en tareas comunes.
6. Ayude a los usuarios a elegir comandos y opciones con confianza y minimice la necesidad de prueba y error. Use comandos orientados a resultados siempre que sea necesario, a menudo en forma de galerías y vistas previas en directo.  
7. Asegúrese de que la cinta de opciones se escala bien desde los tamaños de ventana más grandes hasta los más pequeños.  

## <a name="design-concepts"></a>Conceptos de diseño

### <a name="adapting-a-ribbon-in-an-existing-program"></a>Adaptación de una cinta de opciones en un programa existente

Aunque es posible que simplemente refactorice un diseño tradicional de barra de menús y barra de herramientas de un programa existente a un formato de cinta de opciones, al hacerlo se pierde la mayor parte del valor de usar una cinta de opciones. Las cintas de opciones tienen el máximo valor cuando se usan para presentar comandos inmediatos orientados a resultados, a menudo en forma de galerías y vistas previas en vivo. Los comandos orientados a resultados hacen que los comandos sean más fáciles de entender y los usuarios sean mucho más eficaces y productivos. En lugar de refactorizar los comandos existentes, es mejor rediseñar completamente cómo se realizan los comandos en el programa.

No subestime el desafío de crear una cinta de opciones eficaz. Y no des por supuesto que el uso de una cinta de opciones mejora automáticamente el programa. La creación de una cinta de opciones eficaz requiere mucho tiempo y esfuerzo. Estar dispuesto a confirmar el tiempo y el esfuerzo necesarios para este rediseño de comandos es un factor importante a la hora de decidir usar una cinta de opciones.

### <a name="the-nature-of-ribbons"></a>La naturaleza de las cintas de opciones

En comparación con las barras de menús y las barras de herramientas tradicionales, las cintas de opciones tienen las siguientes características:

- **Una única interfaz de usuario (UI) para todos los comandos.** Las barras de menús son completas y fáciles de aprender, y las barras de herramientas son eficaces y directas, pero ¿por qué no usar un poco más de espacio de pantalla para crear una interfaz de usuario de comandos única que lo consigue todo? Con una sola interfaz de usuario, las cintas de opciones no requieren que los usuarios averiguar qué interfaz de usuario tiene el comando que buscan.
- **Visible y autoexplicativo.** Los comandos de la barra de menús se explican por sí solos a través de sus etiquetas, pero se ocultan a la vista la mayoría de las veces. Para ahorrar espacio en la pantalla, los botones de la barra de herramientas se representan principalmente mediante iconos en lugar de etiquetas (aunque algunos botones de la barra de herramientas usan ambos) y dependen de la información sobre herramientas cuando el icono no se explica por sí mismo. Sin embargo, los usuarios suelen conocer los iconos solo para los comandos que se usan con más frecuencia.
- Al presentar la mayoría de los comandos con iconos etiquetados, los comandos de la cinta de opciones son visibles y autoexplicativos, y usan información sobre herramientas solo para proporcionar información complementaria. No es necesario ir a otro lugar (como ayuda) para comprender un comando.
- **Agrupación etiquetada.** Aunque las categorías de menú están etiquetadas, los grupos de un menú desplegable no son y solo se indican con un separador sin etiquetar. Los grupos de las barras de herramientas también se indican con separadores sin etiquetar.
- Al organizar comandos en grupos etiquetados, las cintas de opciones facilitan la búsqueda de comandos y la determinación de su propósito.
- **Modal, pero no jerárquico.** Las barras de menús se escalan mediante la creación de una jerarquía de comandos. Los menús con muchos elementos pueden usar uno o varios niveles de submenús para proporcionar más comandos.
- Los comandos de la cinta de opciones requieren más espacio que los comandos de la barra de herramientas, por lo que usan pestañas para escalar. Este uso de pestañas hace que las cintas de opciones sea modal, lo que requiere que los usuarios cambien de modo ocasionalmente para buscar comandos. Sin embargo, dentro de una pestaña, la mayoría de los comandos son directos o usan un solo botón de división o botón de menú, no una jerarquía.
- **Directa e inmediata.** Un comando es directo si se invoca con un solo clic (es decir, sin navegar por los menús) e inmediato si tiene efecto inmediato (es decir, sin cuadros de diálogo para recopilar entradas adicionales). Los comandos de la barra de menús siempre son indirectos y, a menudo, no son inmediatos. Al igual que las barras de herramientas, la mayoría de los comandos de la cinta de opciones están diseñados para ser directos e inmediatos, con los comandos usados con más frecuencia invocados con un solo clic y sin necesidad de un cuadro de diálogo para recopilar entradas adicionales.
- **Amplias.** Las barras de menús y las barras de herramientas están diseñadas principalmente para que sean eficientes en el espacio. Para proporcionar sus ventajas, las cintas de opciones pueden consumir más espacio vertical, siendo aproximadamente el equivalente de una barra de menús más tres filas de barras de herramientas. Al ser que algunos programas tienen tres o más filas de barras de herramientas, las cintas de opciones suelen consumir más espacio que las interfaces de usuario tradicionales para los comandos.
- **Tiene un botón Aplicación y una barra de herramientas de acceso rápido.** Una cinta de opciones siempre se presenta con un botón Aplicación y una barra de herramientas de acceso rápido. Esto permite a los usuarios acceder a comandos relacionados con archivos y usados con frecuencia sin cambiar las pestañas, y promueve la coherencia entre programas.
- **Personalización mínima.** Aunque las barras de menús tienen una presentación fija, muchas barras de herramientas son bastante personalizables, lo que permite a los usuarios establecer ubicaciones, tamaños y contenido. Una cinta de opciones en sí no es personalizable, pero la barra de herramientas de acceso rápido proporciona una personalización limitada.
- **Se ha mejorado la accesibilidad del teclado.** Las barras de menús tienen una excelente accesibilidad con el teclado porque al presionar la tecla Alt directamente se proporciona el foco de entrada de la barra de menús. Sin embargo, no hay ningún mecanismo de este tipo para las barras de herramientas porque comparten la navegación con el teclado con el contenido de la ventana. Por lo tanto, los usuarios deben navegar a la barra de herramientas mediante la tecla Tab (a la que se le da la última tabulación) y, a continuación, navegar a un comando específico mediante las teclas de dirección.

Por el contrario, las cintas de opciones proporcionan una accesibilidad mejorada del teclado a través de la información sobre teclas [,](glossary.md)normalmente con un proceso de tres pasos:

- Presione Alt para entrar en el modo de información sobre teclas.
- Presione un carácter para elegir una pestaña, el botón Aplicación o un comando en la barra de herramientas de acceso rápido.
- Dentro de una pestaña, presione una o dos letras para elegir un comando.

    Este enfoque es muy visual. También es más flexible, lo que le permite escalar mejor y tener más asignaciones de claves de acceso mnemotécnicas.

    No confunda las teclas de acceso con teclas de método abreviado. Aunque tanto las teclas de acceso como las teclas de método abreviado proporcionan acceso mediante teclado a la interfaz de usuario, tienen diferentes propósitos e instrucciones. Para obtener más información, vea [Teclado](inter-keyboard.md).

### <a name="the-nature-of-rich-commands"></a>La naturaleza de los comandos enriquecidos

Los comandos enriquecidos hacen referencia a la presentación y la interacción de los comandos que usan las cintas de opciones, sin necesidad de usar un contenedor de cinta de opciones. Los comandos enriquecidos tienen estas características:

- **Etiquetado.** A todos los comandos se les dan etiquetas autoexplicativas, con excepciones solo cuando los iconos son muy conocidos y el espacio es premium.

    **Correcto:**

    ![captura de pantalla de una cinta de opciones de formato de caracteres ](images/cmd-ribbons-image3.png)

    Estos comandos son muy conocidos, por lo que no necesitan etiquetas.

    **Incorrecto:**

    ![captura de pantalla de una cinta de opciones con iconos que rara vez se usan ](images/cmd-ribbons-image4.png)

    Estos iconos no inteligentes requieren etiquetas para comandos enriquecidos.

- **Tamaño.** En lugar de un tamaño uniforme, los comandos tienen un tamaño relativo a su frecuencia de uso e importancia. Además de facilitar la búsqueda y el clic de los comandos usados con más frecuencia, también hace que sean [más táctiles.](https://msdn.microsoft.com/library/windows/desktop/cc872774.aspx)

    ![captura de pantalla de un botón grande y tres botones pequeños ](images/cmd-ribbons-image5.png)

    En este ejemplo, el botón usado con más frecuencia es mayor que el resto.

- **Tamaño dinámico.** Los controles de comandos enriquecidos cambian de tamaño para aprovechar al máximo el espacio disponible, en lugar de usar un tamaño fijo y truncar o usar desbordamiento cuando el tamaño es demasiado pequeño.

    ![captura de pantalla de cinta ancha con botones de igual tamaño ](images/cmd-ribbons-image6.png)![captura de pantalla de cinta pequeña con botones mixtos ](images/cmd-ribbons-image7.png)

    En este ejemplo, los botones de comando cambian de tamaño para funcionar bien en el espacio disponible.

- **Botones de división.** Los botones de división son una buena manera de consolidar un conjunto de variaciones de un comando cuando es necesario, al tiempo que se mantiene la directez para el comando que se usa con más frecuencia.

    ![captura de pantalla de guardar como comando y sus opciones ](images/cmd-ribbons-image8.png)

    En este ejemplo, el comando Guardar como usa un botón de división, donde el botón principal realiza la variación más común y la parte del menú muestra un menú con variaciones del comando.

- **Menús desplegables y galerías enriquecidos.** Los menús desplegables, las listas desplegables y las galerías toman el espacio que necesitan para comunicar y diferenciar el efecto de las opciones, a menudo mediante descripciones de gráficos y texto. Las categorías se usan para organizar grandes conjuntos de opciones.

    ![captura de pantalla de las opciones del menú desplegable con iconos ](images/cmd-ribbons-image9.png)

    En estos ejemplos, al hacer clic en un botón de menú se muestra una lista de opciones que muestran su efecto.

- **Vistas previas dinámicas.** Cada vez que el usuario mantiene el puntero sobre una opción de formato, el programa muestra el aspecto que tendrían los resultados con ese formato mediante el contenido real.

    ![captura de pantalla de los resultados de las opciones de formato ](images/cmd-ribbons-image10.png)

    Las vistas previas en directo muestran los resultados de aplicar una opción de formato al mantener el puntero.

- **Información sobre herramientas mejorada.** Estos explican de forma concisa sus comandos asociados y dan las teclas de método abreviado. También pueden incluir gráficos y referencias a la Ayuda (aunque eliminan en gran medida la necesidad de ayuda relacionada con comandos).

    ![captura de pantalla de información sobre herramientas grande con texto y gráfico ](images/cmd-ribbons-image11.png)

    La información sobre herramientas mejorada explica de forma concisa sus comandos asociados.

Aunque es posible que las cintas de opciones no sean adecuadas para todos los programas, todos los programas pueden beneficiarse de comandos enriquecidos.

### <a name="ribbons-always-have-an-application-button-and-quick-access-toolbar"></a>Las cintas de opciones siempre tienen un botón Aplicación y una barra de herramientas de acceso rápido

El botón Aplicación y la barra de herramientas de acceso rápido proporcionan comandos que son útiles en cualquier contexto, lo que reduce la necesidad de cambiar las pestañas. Aunque estos tres componentes son lógicamente independientes, una cinta siempre debe tener un botón Aplicación y una barra de herramientas de acceso rápido. Dado que los comandos pueden ir en la cinta de opciones o en el botón Aplicación, es posible que se pregunte dónde colocar los comandos. La elección no es arbitraria.

El botón Aplicación se usa para presentar un menú de comandos que implican hacer algo en o con un archivo, como comandos que tradicionalmente van en el menú Archivo para crear, abrir y guardar archivos, imprimir y enviar y publicar documentos.

Por el contrario, la propia cinta de opciones es para los comandos que afectan al contenido de la ventana. Algunos ejemplos son los comandos que se usan para leer, modificar o usar el contenido, o para cambiar la vista.

Si usa una cinta de opciones, también debe usar un botón Aplicación incluso si el programa no implica documentos o archivos. En tales casos, use el menú Aplicación para presentar comandos para imprimir, opciones de programa y salir del programa. Aunque podría decirse que el botón Aplicación no es necesario para estos programas, su uso proporciona coherencia entre programas. Los usuarios no tienen que buscar comandos de guardado y deshacer ni opciones de programa porque siempre están en el mismo lugar.

La barra de herramientas de acceso rápido es necesaria incluso si la cinta de opciones solo usa una pestaña. Una vez más, aunque es posible que estos programas no necesiten una barra de herramientas de acceso rápido (porque todos los comandos ya están presentes en la pestaña única), tener una barra de herramientas de acceso rápido personalizable proporciona coherencia entre programas. Por ejemplo, si los usuarios tienen el hábito de hacer clic en el comando Imprimir, deberían poder hacerlo en cualquier programa que use una cinta de opciones.

### <a name="organization-and-discoverability"></a>Organización y detectabilidad

Al proporcionar pestañas y grupos, las cintas de opciones permiten organizar los comandos para ayudar a la detectabilidad. El desafío es que si la organización se realiza mal, puede dañar enormemente la detectabilidad en su lugar. Debe haber una asignación clara, obvia y única entre los comandos y las pestañas y grupos etiquetados de forma descriptiva donde residen.

Los usuarios formarán un modelo mental de la cinta de opciones después de usarlo durante un tiempo. Si ese modelo mental no tiene sentido para los usuarios, es ineficaz o es incorrecto, provocará confusión y frustración. **El objetivo más importante al diseñar una cinta de opciones es facilitar la búsqueda rápida y segura de comandos. Si no lo consigue, se producirá un error en el diseño de la cinta de opciones.** Lograr este objetivo requiere un diseño, pruebas de usuario e iteración cuidadosas. No suponga que será fácil.

Estos son algunos problemas comunes que se deben evitar:

- **Evite los nombres de pestañas y grupos genéricos.** Un buen nombre de pestaña o grupo debe describir con precisión su contenido específico, preferiblemente mediante el lenguaje basado en tareas y objetivos. Evite nombres genéricos de pestañas y grupos, así como nombres basados en tecnología. Por ejemplo, casi cualquier comando de un documento que cree y cree un programa podría pertenecer a pestañas etiquetadas como Editar, Formato, Herramientas, Opciones, Avanzadas y Mucho más. Confíe en etiquetas específicas y descriptivas, no en la memorización.
- **Evite nombres de grupos y pestañas muy específicos.** Aunque queremos que los nombres de pestañas y grupos sean específicos, no deben ser tan específicos que los usuarios se sorprendan por su contenido. A menudo, los usuarios buscan cosas mediante el proceso de eliminación, por lo que evitan que se desenlazen las pestañas o los grupos porque el nombre es engañoso.
- **Evite varias rutas de acceso al mismo comando, especialmente si la ruta de acceso es inesperada o el comando requiere muchos clics para invocar.** Puede parecer una comodidad encontrar un comando a través de varias rutas de acceso. Pero tenga en cuenta que cuando los usuarios encuentran lo que buscan, dejan de buscar. Es demasiado fácil para los usuarios suponer que la primera ruta de acceso que encuentran es la única ruta de acceso que es un problema grave si esa ruta es ineficaz o inesperada. Además, tener comandos duplicados dificulta que los usuarios encuentren otros comandos que están buscando.

![captura de pantalla del comando ruta de acceso indirecta a los bordes ](images/cmd-ribbons-image12.png)

En este ejemplo, puede cambiar los bordes de párrafo mediante el comando Bordes de página, aunque haya una ruta de acceso más directa en la pestaña Inicio. Si los usuarios que buscan bordes de párrafo se desenredaban en esta ruta de acceso inesperada, es posible que supongan fácilmente que es la única ruta de acceso.

- **Evite la colocación arbitraria de comandos.** Supongamos que cree que tiene una buena pestaña y un diseño de grupo, pero descubra que no caben varios comandos. Lo más probable es que el diseño de pestañas y grupos no sea tan bueno como cree que es y debe seguir refinandolo. No solucione este problema colocando esos comandos a los que no pertenecen. Si lo hace, es probable que los usuarios tengan que inspeccionar todas las pestañas para encontrarlos y, a continuación, olviden rápidamente dónde están.
- **Evite la selección de ubicación basada en marketing.** Supongamos que tiene una nueva versión del programa y que el equipo de marketing realmente quiere promocionar sus nuevas características. Puede ser tentador colocarlos en la pestaña Inicio, pero hacerlo es un error costoso si daña la detectabilidad general. Tenga en cuenta las versiones futuras del producto y la frustración que provocará una organización que cambia constantemente.

### <a name="tabs"></a>Pestañas

El mejor primer paso es revisar las [pestañas estándar de la cinta de opciones](#standard-ribbon-tabs). Si los comandos del programa se asignan de forma natural a las pestañas estándar, base la organización de pestañas en estos estándares. Por otro lado, si los comandos del programa no se asignan de forma natural, no intente forzarlo. Determine una estructura más natural y asegúrese de realizar muchas pruebas de usuario para asegurarse de que lo ha hecho bien.

En el caso de las pestañas no estándar, tenga en cuenta estos problemas:

- **Cada nombre de pestaña debe describir su contenido.** Elija nombres significativos que sean específicos, pero no demasiado específicos. Los usuarios nunca deben despreorse por su contenido.
- **Cada nombre de pestaña debe reflejar su propósito.** Tenga en cuenta el objetivo o la tarea asociados a los comandos.
- **Cada nombre de pestaña debe ser claramente distinto de todos los demás nombres de pestaña.**

La pestaña Inicio es una excepción a estas consideraciones. Aunque no tiene que tener una pestaña Inicio, la mayoría de los programas deben hacerlo. La pestaña Inicio es la primera pestaña y contiene los comandos que se usan con más frecuencia. Si ha usado con frecuencia comandos que no caben en las otras pestañas, la pestaña Inicio es el lugar adecuado para ellos.

Si no puede determinar un nombre de pestaña descriptivo y descriptivo, es probable que se deba a que la pestaña no está bien diseñada. Si la organización de la cinta de opciones no funciona, replantee el diseño de pestañas.

### <a name="groups"></a>Grupos

La división de comandos en grupos estructura los comandos en conjuntos relacionados. La etiqueta de grupo explica el propósito común de sus comandos.

Hay una variedad de factores que se deben tener en cuenta al determinar los grupos y su presentación:

- **Agrupación estándar.** Aunque hay diferencias significativas en los comandos entre programas, hay [grupos](#standard-ribbon-groups) estándar que son comunes en muchos programas. Hacer que estos comandos aparezcan con los mismos nombres y ubicaciones similares mejora considerablemente la detectabilidad.

| Correcto                                                                                      | Incorrecto                                                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| ![captura de pantalla de zoom separada del grupo de edición ](images/cmd-ribbons-image13.png)<br/>El grupo de comandos de edición incluye todos los comandos de edición, pero no incluye el comando Zoom.         | ![captura de pantalla del zoom incluido en el grupo de edición ](images/cmd-ribbons-image14.png)<br/>El comando Zoom no es un comando de edición, pero está en el grupo de edición. |

- **Granularidad.** Alguna estructura es buena, pero demasiada estructura hace que los comandos sea más difíciles de encontrar. Si los nombres de grupo son genéricos, es posible que no tenga suficiente granularidad. Si hay grupos con solo uno o dos comandos cada uno, es probable que tenga demasiado (aunque es aceptable tener una galería en la cinta de opciones sin ningún otro comando dentro de un grupo).

| Correcto                                                                                                 | Incorrecto                                                                                                  |
|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| ![captura de pantalla de zoom separada del grupo de edición ](images/cmd-ribbons-image13.png)<br/> El grupo de comandos de edición incluye todos los comandos de edición.| ![captura de pantalla del grupo de edición dividido en dos grupos ](images/cmd-ribbons-image15.png)<br/>El grupo de comandos de edición se ha dividido en secciones demasiado granulares. Evite grupos con solo uno o dos comandos.|

- **Nombres.** Los nombres de grupo buenos explican el propósito de sus comandos. Si los nombres de grupo no lo tienen, replantee el nombre o la agrupación. Si no puede determinar un nombre descriptivo descriptivo, probablemente se deba a que el grupo no está bien diseñado.

| Correcto                                                                                                 | Incorrecto                                                                                                  |
|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| ![captura de pantalla de comandos divididos en cuatro grupos ](images/cmd-ribbons-image17.png) <br/> Use nombres de grupo que sean lo suficientemente específicos como para describir los comandos contenidos en el grupo. | ![captura de pantalla del grupo de formato con varios comandos ](images/cmd-ribbons-image16.png) <br/> Este nombre de grupo es demasiado impreciso para ser útil. Un enfoque mejor sería reorganizar estos comandos en grupos más específicos. |

- **Orden.** Las personas leen en un orden de izquierda a derecha (en las culturas occidental), por lo que podría pensar que los grupos del extremo izquierdo son los más perceptibles. Sin embargo, el nombre de la pestaña resaltada y el contenido de la ventana tienden a actuar como puntos [focales,](vis-layout.md)por lo que los grupos del centro de la pestaña suelen recibir más atención que el grupo más a la izquierda. Coloque los grupos más usados en las ubicaciones más destacadas y asegúrese de que haya un flujo lógico para los grupos en la pestaña.

![captura de pantalla del grupo del Portapapeles en el extremo izquierdo ](images/cmd-ribbons-image18.png)

En este ejemplo, los grupos Fuente y Párrafo son más perceptibles que el grupo Portapapeles, ya que son lo que el ojo ve primero al subir del documento.

![captura de pantalla del grupo de seguimiento en la pestaña de revisión ](images/cmd-ribbons-image19.png)

En este ejemplo, el grupo Seguimiento recibe la mayor atención, en parte porque la pestaña Revisar resaltada actúa como punto focal.

- **Uniformidad.** Puede ser difícil reconocer comandos cuando la presentación de comandos tiene el mismo aspecto. El uso de iconos con diferentes formas y colores, grupos con distintos formatos y comandos con distintos tamaños facilita a los usuarios el reconocimiento de grupos de comandos. Los comandos solo deben tener un tamaño uniforme cuando la cinta de opciones se escala verticalmente a sus tamaños más pequeños.

| Correcto | Incorrecto |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| ![captura de pantalla del grupo con iconos de diferentes tamaños ](images/cmd-ribbons-image20.png)<br/>Uso de una variedad de tamaños de icono para mejorar la reconocimiento| ![captura de pantalla del grupo con iconos del mismo tamaño ](images/cmd-ribbons-image21.png)<br/>Estos comandos son demasiado similares entre sí porque todos tienen el mismo tamaño. |

### <a name="previews"></a>Vistas previas

Puede usar varios tipos de vistas previas para mostrar el resultado de un comando. Mediante el uso de vistas previas útiles, puede mejorar la eficacia del programa y reducir la necesidad del enfoque de aprendizaje de prueba y error. Las versiones preliminares en directo también invitan a la experimentación y fomentan la creatividad.

Estos son algunos de los distintos tipos de versiones preliminares que puede usar:

- **Gráficos y iconos estáticos realistas.** Imágenes estáticas que dan una indicación realista del efecto de un comando. Se pueden usar en galerías, menús desplegables e información sobre herramientas mejorada.

![captura de pantalla de la lista desplegable de fuentes ](images/cmd-ribbons-image22.png)

En este ejemplo, la lista desplegable Fuente muestra cada nombre de fuente mediante la propia fuente.

![captura de pantalla de la galería de miniaturas de marca de agua ](images/cmd-ribbons-image23.png)

En este ejemplo, se usan miniaturas realistas para mostrar las diferentes marcas de agua.

- **Iconos dinámicos y gráficos.** Iconos y gráficos que se modifican para reflejar el estado actual. Estos iconos son especialmente útiles para las galerías, así como para los botones de división que cambian su efecto predeterminado para que sea el mismo que el de la última acción.

![captura de pantalla de la galería de estilos de párrafo ](images/cmd-ribbons-image24.png)

En este ejemplo, Microsoft Word la galería estilos para reflejar los estilos actuales.

![captura de pantalla de los botones de comandos de formato de texto ](images/cmd-ribbons-image25.png)

En este ejemplo, Word cambia los comandos Color de resaltado de texto y Color de fuente para indicar su efecto actual.

- **Vistas previas dinámicas.** Cuando los usuarios mantienen el puntero sobre una opción de formato, la vista previa activa muestra el aspecto de los resultados con ese formato. Las versiones preliminares dinámicas ayudan a los usuarios a realizar selecciones de forma más eficaz y segura en función del contexto real del usuario.

![captura de pantalla del selector de color de comando de color de página ](images/cmd-ribbons-image26.png)

En este ejemplo, el comando Color de página realiza una vista previa activa mostrando el efecto de las opciones de color al mantener el puntero.

Las versiones preliminares dinámicas son una característica eficaz que puede mejorar realmente la productividad de los usuarios, pero incluso las vistas previas estáticas simples pueden ser una gran ayuda.

### <a name="scaling-the-ribbon"></a>Escalado de la cinta de opciones

El escalado de una barra de herramientas es sencillo: si una ventana es demasiado estrecha para mostrar una barra de herramientas, la barra de herramientas muestra lo que se ajusta y hace que todo lo demás sea accesible a través de un botón de desbordamiento. Un objetivo de los comandos enriquecidos es aprovechar al máximo el espacio disponible, por lo que el escalado de una cinta de opciones requiere más trabajo de diseño. No hay ningún tamaño de cinta predeterminado, por lo que no debe diseñar una cinta de opciones con un ancho determinado en mente. Tiene que diseñar diseños con una amplia gama de anchos y tener en cuenta que cualquiera de ellos podría ser el que verán la mayoría de los usuarios. El escalado es una parte fundamental del diseño de la cinta de opciones, no el último paso. Al diseñar una pestaña, especifique los distintos diseños para cada grupo (hasta tres), así como las combinaciones que se pueden usar juntas. La cinta de opciones mostrará la combinación válida más grande que se ajuste al tamaño actual de la ventana.

![Captura de pantalla de comandos de formato en el menú de desbordamiento Escala de barras de ](images/cmd-ribbons-image27.png) herramientas mediante un botón de desbordamiento.

![captura de pantalla de cintas con varios anchos ](images/cmd-ribbons-image28.png) No hay ningún tamaño de cinta predeterminado. El tamaño más pequeño es un solo icono de grupo emergente.

## <a name="guidelines"></a>Directrices

### <a name="general"></a>General

- **No combine cintas de opciones con barras de menús y barras de herramientas dentro de una ventana.** Las cintas de opciones deben usarse en lugar de barras de menús y barras de herramientas. Sin embargo, una cinta de opciones se puede combinar con ventanas de paleta y elementos de navegación, como los botones Atrás y Adelante y una barra de direcciones.
- **Combine siempre una cinta de opciones con un botón Aplicación y la barra de herramientas de acceso rápido.**
- **Seleccione la pestaña más a la izquierda (normalmente Inicio) cuando se inicia un programa.** No haga que la última pestaña seleccionada se conserve entre las instancias del programa.
- **Muestre la cinta de opciones en su estado normal (no minimizado) cuando se inicia un programa por primera vez.** A menudo, los usuarios dejan sin modificar la configuración predeterminada, por lo que minimizar la cinta de opciones al inicio del programa probablemente hará que todos los comandos sean menos eficaces. Además, mostrar la cinta de opciones minimizada inicialmente puede ser desorientada.
- **Haga que el estado de la cinta de opciones se conserve entre las instancias del programa.** Por ejemplo, si un usuario minimiza la cinta de opciones, debe mostrarse minimizada la próxima vez que se ejecute el programa. Pero de nuevo, no haga que la última pestaña seleccionada se conserve de esta manera.

### <a name="using-tabs"></a>Uso de las fichas

Por lo general, tener menos pestañas es mejor, así que quite las pestañas que no ayudan a lograr estos objetivos.

- **Siempre que sea práctico, use pestañas estándar.** El uso de pestañas estándar mejora considerablemente la detectabilidad, especialmente en todos los programas. Consulte las [pestañas estándar de la cinta de opciones](#standard-ribbon-tabs) más adelante en este artículo.
- **Etiquete la primera pestaña Inicio, si procede.** La pestaña Inicio debe contener los comandos usados con más frecuencia. Si ha usado con frecuencia comandos que no caben en las otras pestañas, la pestaña Inicio es el lugar adecuado para ellos.
- Agregue una nueva pestaña si:
  - **Sus comandos están fuertemente relacionados con tareas específicas y se pueden describir con precisión mediante la etiqueta de tabulación.** Agregar la pestaña debería ayudar a que sus comandos se encuentren fácilmente, no más difíciles.
  - **Sus comandos no están relacionados principalmente con las tareas de otras pestañas.** La adición de la pestaña no debe requerir más cambio de pestaña durante las tareas que se realizan habitualmente.
  - **La pestaña tiene suficientes comandos para justificar que hay un lugar adicional para buscar.** No tenga pestañas con solo unos pocos comandos. **Excepción:** Considere la posibilidad de agregar una pestaña con algunos comandos si están fuertemente relacionados con una tarea específica y agregar la pestaña simplifica en gran medida una pestaña Inicio demasiado compleja.
- **En el caso de las pestañas restantes, coloque primero las pestañas que se usan con más frecuencia, al tiempo que mantiene un orden lógico entre las pestañas.**
- **Optimice el diseño de pestañas para que los usuarios encuentren comandos de forma rápida y segura.** Todas las demás consideraciones son secundarias.
- **No proporcione una pestaña Ayuda.** En su lugar, proporcione ayuda con ayuda para todo el programa e información sobre herramientas mejorada.
- **Use un máximo de siete pestañas principales.** Si hay más de siete, resulta difícil determinar qué pestaña tiene un comando. Aunque siete pestañas principales son aceptables para las aplicaciones con muchos comandos, la mayoría de los programas deben tener como objetivo cuatro o menos pestañas.

### <a name="contextual-tabs"></a>Pestañas contextuales

- **Use una pestaña contextual para mostrar una colección de comandos que solo son pertinentes cuando los usuarios seleccionan un tipo de objeto determinado.** Si solo hay algunos comandos que se usan con frecuencia, puede ser más cómodo y estable usar una pestaña normal y simplemente deshabilitar los comandos cuando no se aplican.
- ![captura de pantalla de los comandos cortar y copiar atenuados ](images/cmd-ribbons-image29.png)<br>Es mejor deshabilitar comandos comunes como Cortar y Copiar que usar una pestaña contextual.
- **Incluya solo los comandos específicos de un tipo de objeto determinado.** No coloque comandos solo en una pestaña contextual si es posible que los usuarios los necesiten sin seleccionar primero un objeto.
- **Incluya los comandos que se usan con frecuencia al trabajar con un tipo de objeto determinado.** Coloque comandos contextuales generales usados con frecuencia en menús contextuales y minicobús para evitar el cambio de tabulación durante las tareas que se realizan normalmente. Como alternativa, considere la posibilidad de colocar comandos generales de forma redundante en una pestaña contextual si esto evita el cambio frecuente de tabulación. Pero no lo haga en exceso: no intente incluir todos los comandos que un usuario pueda necesitar mientras trabaja con el objeto .
- ![captura de pantalla del comando bordes en la pestaña diseño ](images/cmd-ribbons-image30.png)<br/>En este ejemplo, el comando Bordes se incluye en la pestaña Diseño para evitar el cambio de pestaña frecuente durante las tareas que se realizan habitualmente.\
- **Elija un color de pestaña contextual que sea diferente de las pestañas contextuales que se muestran actualmente.** El mismo conjunto de pestañas puede aparecer más adelante con un color diferente para lograrlo, pero intente usar asignaciones de colores coherentes en las invocaciones siempre que sea posible.
- **La selección de una pestaña contextual ayuda** automáticamente a la detectabilidad, mejora la percepción de estabilidad y reduce la necesidad de cambiar de pestaña. Seleccione automáticamente una pestaña contextual cuando:
  - **El usuario inserta un objeto .** En este caso, seleccione la primera pestaña contextual del conjunto.
  - **El usuario hace doble clic en un objeto.** En este caso, seleccione la primera pestaña contextual del conjunto.
  - **El usuario seleccionó una pestaña contextual, hizo clic en el objeto y, a continuación, hizo clic inmediatamente en un objeto del mismo tipo.** En este caso, vuelva a la pestaña contextual seleccionada anteriormente.
- **Al quitar una pestaña contextual que sea la pestaña activa, haga que** la pestaña Inicio o la primera pestaña sea la pestaña activa. Al hacerlo, aparece el más estable.

### <a name="modal-tabs"></a>Pestañas modales

- **Use una pestaña modal para mostrar una colección de comandos que se aplican con un modo temporal determinado y no se aplica ninguna de las pestañas principales.** Si se aplican algunas de las pestañas principales, use una pestaña contextual en su lugar y deshabilite los comandos que no se aplican. Dado que las pestañas modales son muy limitantes, solo se deben usar cuando no hay una alternativa mejor.
- ![captura de pantalla de la pestaña vista previa de impresión ](images/cmd-ribbons-image31.png)<br/>Vista previa de impresión es una pestaña modal de uso frecuente.
- **Para cerrar una pestaña modal, coloque el comando <mode> Cerrar como último comando de la pestaña.** Use el icono Cerrar para facilitar la búsqueda del comando. Dé el modo en el comando para evitar confusiones sobre lo que se está cierrando.
- ![captura de pantalla del botón cerrar vista previa de impresión ](images/cmd-ribbons-image32.png)<br/>En este ejemplo, al etiquetar explícitamente el comando Cerrar con el modo se quita cualquier duda sobre lo que se está cierrando.
- **Para cerrar una pestaña modal, vuelva a definir también el botón Cerrar de la barra de título de la ventana para cerrar el modo en lugar del programa.** Las pruebas de usuario han demostrado que muchos usuarios esperan este comportamiento.

### <a name="standard-ribbon-tabs"></a>Pestañas estándar de la cinta de opciones

Siempre que sea práctico, asigne los comandos del programa a estas pestañas estándar, dadas en su orden de apariencia estándar.

#### <a name="regular-tabs"></a>Pestañas normales

- **Casa.** Contiene los comandos usados con más frecuencia. Si se usa, siempre es la primera pestaña.
- **insertar.** Contiene comandos para insertar contenido y objetos en un documento. Si se usa, siempre es la segunda pestaña.
- **Diseño de página.** Contiene comandos que afectan al diseño de la página, incluidos temas, configuración de página, fondos de página, sangría, espaciado y posicionamiento. (Tenga en cuenta que los grupos de sangría y espaciado pueden estar en su lugar en la pestaña Inicio, si hay suficiente espacio). Si se usa, siempre es la tercera pestaña.
- **Revisión.** Contiene comandos para agregar comentarios, realizar un seguimiento de los cambios y comparar versiones.
- **Vista.** Contiene comandos que afectan a la vista de documento, incluidos el modo de vista, las opciones mostrar u ocultar, el zoom, la administración de ventanas y las macros que tradicionalmente se encuentran en la Windows de menú. Si se usa, es la última pestaña normal a menos que se muestre la pestaña Desarrollador.
- **Desarrollador.** Contiene comandos que solo usan los desarrolladores. Si se usa, se oculta de forma predeterminada y la última pestaña normal cuando se muestra.

La mayoría de los programas no necesitan las pestañas Revisar y Desarrollador.

#### <a name="standard-contextual-tabs"></a>Pestañas contextuales estándar

- **Formato.** Contiene comandos relacionados con el cambio del formato del tipo de objeto seleccionado. Normalmente se aplica a parte de un objeto .
- **Diseño.** Contiene comandos, a menudo en galerías, para aplicar estilos al tipo de objeto seleccionado. Normalmente se aplica a todo el objeto .
- **Diseño.** Contiene comandos para cambiar la estructura de un objeto complicado, como una tabla o un gráfico.

Si tiene comandos contextuales relacionados con el formato, el diseño y el diseño, pero no lo suficiente para varias pestañas, solo tiene que proporcionar una pestaña Formato.

### <a name="standard-groups"></a>Grupos estándar

- **Siempre que sea práctico, use grupos estándar.** El hecho de que aparezcan comandos comunes con los mismos nombres y ubicaciones similares mejora considerablemente la detectabilidad. Consulte los [grupos estándar de la cinta de opciones](#standard-ribbon-groups) más adelante en este artículo.
- **Agregue un nuevo grupo si:**
  - **Sus comandos están fuertemente relacionados y se pueden describir con precisión mediante la etiqueta de grupo.** Agregar el grupo debe ayudar a que sus comandos se encuentren fácilmente, no más difíciles.
  - **Sus comandos tienen una relación más débil con los comandos de otros grupos.** Aunque todos los comandos de una pestaña deben estar estrechamente relacionados, algunas relaciones de comandos son más seguras que otras.
  - **El grupo tiene suficientes comandos para justificar tener un lugar adicional para buscar.** Apunte a entre 3 y 5 comandos para la mayoría de los grupos. Evite tener grupos con solo 1-2 comandos, aunque es aceptable tener una galería en la cinta de opciones sin ningún otro comando dentro de un grupo. Tener muchos grupos con un solo comando sugiere demasiada estructura o falta de coherencia de comandos.
- **No organice en exceso** agregando grupos donde no sean necesarios.
- **Considere la posibilidad de dividir un grupo** si:
  - ![captura de pantalla del grupo de comandos desorganizados ](images/cmd-ribbons-image35.png)<br/>El grupo tiene muchos comandos de diferentes tamaños y necesita organización.
  - ![captura de pantalla de dos nombres de grupo de párrafos largos ](images/cmd-ribbons-image33.png)<br>El grupo tiene comandos que se benefician enormemente de tener etiquetas adicionales.
- **Coloque los grupos más usados en las ubicaciones más destacadas y asegúrese de que hay un orden lógico para los grupos en la pestaña.**
- **Optimice el diseño del grupo para que los usuarios encuentren comandos de forma rápida y segura.** Todas las demás consideraciones son secundarias.
- **No escale grupos que contengan un solo botón a un icono de grupo emergente.** Al reducir verticalmente, déjelos como un solo botón.
- **Use un máximo de siete grupos.** Si hay más de siete grupos, resulta más difícil determinar qué grupo tiene un comando.

### <a name="standard-ribbon-groups"></a>Grupos de cinta de opciones estándar

Siempre que sea práctico, asigne los comandos del programa a estos grupos estándar, que se asignan dentro de sus pestañas asociadas en su orden de apariencia estándar.

#### <a name="main-tab"></a>Pestaña Principal

- Portapapeles
- Fuente
- Paragraph
- Edición

#### <a name="insert-tab"></a>Pestaña Insertar

- Tablas
- Ilustraciones

#### <a name="page-layout-tab"></a>Pestaña Diseño de página

- Temas
- Configurar página
- Organizar

#### <a name="review-tab"></a>Pestaña Revisar

- Revisión
- Comentarios

#### <a name="view-tab"></a>Pestaña Vista

- Vistas de documento
- Mostrar u ocultar
- Zoom
- Periodo

### <a name="commands"></a>Comandos

- ![Captura de pantalla del comando de números de línea en la cinta de opciones ](images/cmd-ribbons-image36.png)<br/>**Aproveche las ventajas de la detectabilidad y escalabilidad de las cintas de opciones mediante la exposición de todos los comandos usados habitualmente.** Cuando corresponda, mueva los comandos usados con frecuencia de los cuadros de diálogo a la cinta de opciones, especialmente los que se sabe que son difíciles de encontrar. Lo ideal es que los usuarios puedan realizar tareas comunes sin usar ningún cuadro de diálogo.

- **No use la escalabilidad de las cintas de opciones para justificar la adición de complejidad innecesaria.** Continúe con el ejercicio de moderación, no agregue comandos a una cinta de opciones solo porque puede hacerlo. Mantenga la experiencia general de comandos sencilla. Las siguientes son formas de simplificar la presentación:
  - ![captura de pantalla de la mini barra de herramientas y el menú contextual ](images/cmd-ribbons-image37.png)</br>**Use menús contextuales y mini barras de herramientas para comandos contextuales en contexto.**
  - **Mover (o mantener) comandos usados con rara frecuencia en los cuadros de diálogo.** Use los selectores de cuadro de diálogo para acceder a estos comandos. Todavía puede usar cuadros de diálogo con cintas de opciones. Simplemente intente reducir la necesidad de usarlos durante las tareas comunes.
  - **Elimine las características redundantes que rara vez se usan.**

#### <a name="presentation"></a>Presentación

- **Presente cada comando en una sola pestaña. Evite varias rutas de acceso al mismo comando, especialmente si el comando requiere muchos clics para invocar.** Puede parecer una comodidad encontrar un comando a través de varias rutas de acceso. Pero tenga en cuenta que cuando los usuarios encuentran lo que buscan, dejan de buscar. Es demasiado fácil para los usuarios suponer que la primera ruta de acceso que encuentran es la única ruta de acceso que es un problema grave si esa ruta de acceso es ineficaz. **Excepción:** Las pestañas contextuales pueden duplicar algunos comandos de las pestañas Inicio e Insertar si esto impide cambiar las pestañas para tareas contextuales comunes.
- **Dentro de un grupo, coloque los comandos en su orden lógico, al tiempo que da preferencia a los comandos usados con más frecuencia.** En general, los comandos deben tener un flujo lógico para que sea fácil de encontrar, a la vez que los comandos usados con más frecuencia aparecen primero. Por lo general, los comandos con iconos de 32 x 32 píxeles aparecen antes que los comandos con iconos de 16 x 16 píxeles para facilitar el análisis entre grupos.
- **Evite colocar comandos destructivos junto a los comandos usados con frecuencia.** Un comando se considera destructivo si su efecto está generalizado y no se puede deshacer fácilmente o el efecto no se nota inmediatamente.
- **Use separadores para indicar comandos fuertemente relacionados, como un conjunto de opciones mutuamente excluyentes.**
- ![captura de pantalla de grupos de fuentes y párrafos ](images/cmd-ribbons-image3.png)<br/> **Considere la posibilidad de usar grupos de estilo de barra de herramientas para conjuntos de comandos conocidos y fuertemente relacionados que no necesitan etiquetas.** Esto le permite presentar muchos comandos en un espacio compacto sin que ello afecte a la detectabilidad y a la facilidad de aprendizaje. Para ser tan conocidos, estos comandos se usan con frecuencia, se reconocen al instante y, por tanto, tienden a estar en la pestaña Inicio.

- **Use iconos de 32 x 32 píxeles para los comandos etiquetados más usados e importantes.** Al reducir verticalmente un grupo, haga que estos comandos se conviertan en iconos de 16 x 16 píxeles.
- **Evite la colocación arbitraria de comandos.** Piense detenidamente en el diseño de pestañas y grupos para asegurarse de que los usuarios no maltenten el tiempo inspeccionando cada pestaña para encontrar el comando que desean.
- **Evite la selección de ubicación basada en marketing.** Los objetivos de marketing en torno a la promoción de nuevas características tienden a cambiar con el tiempo. Tenga en cuenta las versiones futuras del producto y la frustración que provocará una organización que cambia constantemente.

#### <a name="interaction"></a>Interacción

- **Deshabilite los comandos que no se aplican al contexto actual o que generarían directamente un error.** Si es útil, use la [información sobre herramientas mejorada](glossary.md) para explicar por qué el comando está deshabilitado. No oculte estos comandos porque esto puede hacer que el diseño de la cinta cambie, lo que hace que la presentación de la cinta sea inestable.
- **No actualice las etiquetas de comando dinámicamente.** De nuevo, esto podría hacer que el diseño de la pestaña cambie, lo que da lugar a una apariencia inestable. En su lugar, diseñe comandos para que funcionen con etiquetas constantes.

    | Correcto                                                                                       | Incorrecto                                                                 |
    |-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
    | ![captura de pantalla de insertar nota y eliminar nota ](images/cmd-ribbons-image38.png)<br/> Deshabilitar comandos cuando no están disponibles | ![captura de pantalla de la nota de inserción, ninguna nota de eliminación ](images/cmd-ribbons-image39.png)<br/>No ocultar comandos, incluso cuando no estén disponibles |

- **Prefiere controles directos.** Un comando es directo si se invoca con un solo clic (es decir, sin navegar por los menús). Sin embargo, a excepción de las galerías en la cinta de opciones, los controles directos no admiten live preview, por lo que la necesidad de la versión preliminar en directo también es un factor.
- **Use la versión** preliminar en vivo para indicar el efecto de las opciones cuando un comando se encuentra entre un conjunto relacionado de opciones de formato y live preview es importante y práctico, especialmente si es probable que los usuarios elijan la opción incorrecta de lo contrario.
  - Si el comando se usa con frecuencia, use una galería en la cinta de opciones para la directness.
  - Si el comando se usa con poca frecuencia, use una galería desplegable.
- **Exponer comandos directos** mediante los siguientes controles en el orden de preferencia siguiente
  - **Botones de comando, casillas, botones de radio y galerías locales.** Siempre son directas.
  - **Botones de división.** Directo para el comando más común, pero indirecto para las variaciones de comandos.
  - **Botones de menú.** Son indirectos, pero presentan muchos comandos que son fáciles de encontrar.
  - **Cuadros de texto (con controles de giro).** Por lo general, la entrada de texto requiere más esfuerzo que los demás tipos de control.
- ![captura de pantalla de la cinta de opciones solo con botones de menú ](images/cmd-ribbons-image42.png)</br>Si la cinta de opciones consta principalmente de botones de menú cuando se muestra a tamaño completo, también puede usar una barra de menús.
- **Prefiere comandos inmediatos.** ![captura de pantalla del botón de impresión dividida y su submenú ](images/cmd-ribbons-image43.png)<br/>Un comando es inmediato si tiene efecto inmediato (es decir, sin cuadros de diálogo para recopilar entradas adicionales). Si un comando puede requerir entrada, considere la posibilidad de usar un botón de división, con el comando inmediato en la parte del botón y los comandos que requieren entrada en el submenú.

### <a name="galleries"></a>Galerías

**Use una [galería si:](glossary.md)**

- **Hay un conjunto de opciones bien definido y relacionado entre las que los usuarios suelen elegir.** Puede haber un número ilimitado de variaciones, pero las selecciones probables deben estar bien contenidas. Si las opciones no están fuertemente relacionadas, considere la posibilidad de usar galerías independientes.
- **Las opciones se expresan mejor visualmente, como las características de formato.** El uso de miniaturas facilita la exploración, la información y la toma de decisiones. Aunque las opciones se pueden etiquetar, la selección se realiza visualmente y no es necesario que las etiquetas de texto comprendan las opciones.
- **Las opciones muestran el resultado que se logra inmediatamente con un solo clic.** No debe haber ningún cuadro de diálogo de seguimiento para aclarar aún más la intención del usuario ni un conjunto de pasos para lograr el resultado indicado. Si es posible que los usuarios quieran ajustar la opción, deje que lo hagan después.

**Use una galería en la cinta de opciones** si:

- **Las opciones se usan con frecuencia.** Las opciones necesitan el espacio y merecen la pena el espacio que potencialmente se toma de otros comandos.
- **Para un uso típico, no es necesario agrupar ni filtrar las opciones presentadas.**
- **Las opciones se pueden mostrar de forma eficaz dentro del alto de una cinta de opciones (que es de 48 píxeles).**

#### <a name="thumbnails-in-galleries"></a>Miniaturas en galerías

**Elija el tamaño de miniatura estándar más pequeño de la galería** que realiza bien el trabajo.

- En el caso de las galerías en cinta, use miniaturas de 16 x 16, 48 x 48 o 64 x 48 píxeles.
- Para las galerías desplegables, use miniaturas de 16x16, 32x32, 48x48, 64x48, 72x96, 96x72, 96x96 o 128x128 píxeles.
- Todos los elementos de la galería deben tener el mismo tamaño de miniatura.

Para galerías en la cinta de opciones:

- **Mostrar un mínimo de tres opciones; más si hay espacio.** Si no hay espacio suficiente para mostrar al menos tres opciones en el tamaño típico de la ventana, use una galería desplegable en su lugar.
- **Expanda las galerías de la cinta de opciones para aprovechar el espacio disponible.** Use el espacio adicional para mostrar más elementos y facilitar su elección con un solo clic.

Para galerías desplegables:

- **Muestre la galería desde un cuadro combinado, una lista desplegable, un botón de división o un botón de menú.**
- **Si el usuario hace clic en la ventana principal para descartar la galería desplegable, simplemente descarte la galería sin seleccionar o modificar el contenido de la ventana principal.**
- **Si una galería tiene muchas opciones y algunas opciones rara vez se usan, simplifique la galería predeterminada al centrarse en las opciones más usadas.** Para los comandos restantes, proporcione un comando adecuado en la parte inferior de la lista desplegable de la galería.
  - Si el comando muestra una lista de más variaciones, así mismo den el nombre "Más `singular feature name` opciones...".
  - Si el comando presenta un cuadro de diálogo que permite a los usuarios crear sus propias opciones personalizadas, den el nombre `feature name` "Personalizado...".
- **Organice las opciones en grupos, si lo hace, hace que la exploración sea más eficaz.**
- ![captura de pantalla de la galería de símbolos y filtros ](images/cmd-ribbons-image44.png)<br/>**Si una galería tiene muchos elementos, considere la posibilidad de agregar un filtro para ayudar a los usuarios a encontrar opciones de forma más eficaz.** Para evitar confusiones, muestre inicialmente la galería sin filtrar. Sin embargo, la mayoría de las galerías no deben requerir un filtro porque no deben tener tantas opciones y el uso de grupos debería ser suficiente.

### <a name="command-previews"></a>Vistas previas de comandos

- **Use vistas previas para mostrar el efecto de un comando sin que los usuarios tengan que realizarlo primero.** Mediante el uso de vistas previas útiles, puede mejorar la eficacia y la facilidad de aprendizaje del programa y reducir la necesidad de prueba y error. Para ver los distintos tipos de versiones preliminares de comandos, consulte [Versiones preliminares](#previews) en la sección Conceptos de diseño de este artículo.
- **En el caso de las versiones preliminares dinámicas, asegúrese de que se pueda aplicar la versión preliminar y de que se restaure el estado actual en un plazo de 500 milisegundos.** Para ello, es necesario poder aplicar los cambios de formato rápidamente y de forma que sea interrumpible. Los usuarios deben poder evaluar rápidamente distintas opciones para que las versiones preliminares en directo tengan todas sus ventajas.
- **Evite el uso de texto en las versiones preliminares.** De lo contrario, las imágenes de vista previa tendrán que localizarse.

### <a name="icons"></a>Iconos

- ![captura de pantalla de la lista desplegable y las casillas ](images/cmd-ribbons-image45.png)<br/>**Proporcione iconos para todos los controles de la cinta, excepto las listas desplegables, las casillas y los botones de radio.** La mayoría de los comandos requerirán iconos de 32 x 32 y 16 x 16 píxeles (solo la barra de herramientas de acceso rápido usa iconos de 16 x 16 píxeles). Las galerías suelen usar iconos de 16 x 16, 48 x 48 o 64 x 48 píxeles.
- **Proporcione iconos únicos.** No use el mismo icono para distintos comandos.
- **Asegúrese de que los iconos de la cinta de opciones estén claramente visibles en el color de fondo de la cinta.** Evalúe siempre los iconos de la cinta de opciones en contexto y en modo de contraste alto.
- **Elija diseños de icono que comuniquen claramente su efecto,** especialmente para los comandos usados con más frecuencia. Las cintas de opciones bien diseñadas tienen iconos autoexplicativos para ayudar a los usuarios a encontrar y comprender los comandos de forma eficaz.
- **Elija iconos que sean reconocibles y distintivos,** especialmente para los comandos usados con más frecuencia. Asegúrese de que los iconos tienen formas y colores distintivos. Esto ayuda a los usuarios a encontrar los comandos rápidamente, aunque no recuerden el símbolo de icono.

    | Correcto                                                                                                 | Incorrecto                                                                               |
    |--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
    | ![captura de pantalla del cuentagotas azul y el lápiz amarillo ](images/cmd-ribbons-image46.png)<br/>Use la forma y el color para crear iconos que sean fáciles de distinguir. | ![captura de pantalla del dropper de ojos azul y el lápiz azul ](images/cmd-ribbons-image47.png)<br/> Los iconos que tienen el mismo color son difíciles de distinguir|

- ![captura de pantalla del comando comments en el contenedor emergente ](images/cmd-ribbons-image48.png)<br/>**Considere la posibilidad de crear iconos de grupo emergentes colocando el icono de 16 x 16 píxeles del comando más destacado del grupo dentro de un contenedor visual de 32 x 32 píxeles.** No tiene que crear iconos diferentes para los grupos emergentes.
- ![captura de pantalla de los botones de comandos de formato de texto ](images/cmd-ribbons-image25.png)<br/>**Si es útil, cambie el icono para reflejar el estado actual.** Esto es especialmente útil para los botones de división cuyo efecto predeterminado puede cambiar.
- **Asegúrese de que los iconos de la cinta de opciones se ajustan a las directrices de los iconos de estilo aerórmico.** Sin embargo, los iconos de la cinta de opciones se muestran directamente en lugar de mostrarse en perspectiva.

| Correcto                                                                                                 | Incorrecto                                                                               |
    |--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
    | ![captura de pantalla de iconos de comandos bidimensionales ](images/cmd-ribbons-image49.png)<br/> Use iconos bidimensionales.|![captura de pantalla de iconos de comandos tridimensionales ](images/cmd-ribbons-image50.png)<br/> No use iconos tridimensionales. |
 
### <a name="enhanced-tooltips"></a>Información sobre herramientas mejorada

- **Todos los comandos de la cinta de opciones deben tener información** sobre herramientas mejorada para proporcionar el nombre del comando, la tecla de método abreviado, la descripción y la información complementaria opcional. Evite la información sobre herramientas que simplemente restatique la etiqueta.

    **Incorrecto:**

    ![captura de pantalla de información sobre herramientas que repite el nombre del comando ](images/cmd-ribbons-image51.png)

    En este ejemplo, la información sobre herramientas simplemente restablece la etiqueta del comando.

- **Cuando sea práctico, describa completamente el comando mediante una descripción concisa.** Vincular a la Ayuda solo si realmente es necesaria una explicación adicional.

    **Incorrecto:**

    ![captura de pantalla de información sobre herramientas para el comando tachado ](images/cmd-ribbons-image52.png)

    En este ejemplo, el comando no necesita Ayuda.

- **Cuando sea útil, ilustra el efecto del comando mediante una vista previa.**

    ![captura de pantalla de información sobre herramientas y gráfico para insertar gráfico ](images/cmd-ribbons-image53.png)

    En este ejemplo, la imagen de información sobre herramientas muestra el efecto del comando.

Para obtener instrucciones de etiquetado, consulte [Etiquetas de información sobre herramientas mejoradas.](#enhanced-tooltips)

### <a name="access-keys-and-keytips"></a>Claves de acceso e información sobre claves

La información sobre claves es el mecanismo que se usa para mostrar las claves de acceso para los comandos que se muestran directamente en una cinta de opciones.

Las teclas de acceso para los comandos de menú desplegable se indican con un carácter subrayado. Difieren de las teclas de acceso del menú de las maneras siguientes:

- Se pueden usar dos claves de acceso de caracteres. Por ejemplo, FP se puede usar para tener acceso al comando Formatear símbolo del sistema.
- Las asignaciones de clave de acceso se muestran mediante sugerencias en lugar de subrayados, por lo que el ancho de caracteres y los descendientes no son un factor para realizar asignaciones.

- **Asigne claves de acceso a todas las pestañas y comandos de la cinta de opciones.** La única excepción posible es para los comandos procedentes de complementos heredados.
- **Para el botón Aplicación y la barra de herramientas de acceso rápido:**
  - Asigne F al botón Aplicación. Esta asignación se usa debido a la similitud del botón Aplicación con el menú Archivo tradicional.
  - ![captura de pantalla de la información sobre teclas de comando en una cinta de opciones ](images/cmd-ribbons-image54.png)<br/>Para la barra de herramientas de acceso rápido y las listas de archivos usadas recientemente, asigne claves de acceso numéricamente.
- ![captura de pantalla que muestra la información sobre teclas para las pestañas ](images/cmd-ribbons-image55.png)<br/>**Para pestañas:**
  - Asigne H a Inicio.
  - A partir de las pestañas que se usan con más frecuencia, asigne la primera letra de la etiqueta.
  - Para las pestañas que no se pueden asignar a la primera letra, elija una consonante distintiva o una voz en la etiqueta.
  - En el caso de los programas que solían admitir barras de menús, esfuérctese por mantener la compatibilidad de las claves de acceso en la mejor medida de lo posible. Evite asignar significados diferentes a las claves de acceso desde categorías de menú heredadas. Por ejemplo, si la versión heredada de la barra de menús de un programa tenía un menú Editar, esfuérctese por usar una clave de acceso E en la pestaña equivalente. Si no hay ninguna pestaña equivalente, no asigne una clave de acceso E a ninguna pestaña para evitar confusiones.
- ![captura de pantalla que muestra la información sobre claves de una cinta de opciones ](images/cmd-ribbons-image56.png)<br/>**Para comandos, menús y submenús de la cinta de opciones:**
  - Asigne combinaciones de teclas de acceso únicas dentro de una pestaña. Puede reutilizar las combinaciones de teclas de acceso en diferentes pestañas.
  - Siempre que sea posible, asigne las claves de acceso estándar para los comandos usados habitualmente. Consulte la [tabla de claves de acceso estándar](inter-keyboard.md).
  - Para otros comandos:
    - Para los comandos usados con más frecuencia, elija letras al principio de la primera o segunda palabra de la etiqueta, preferiblemente la primera letra.
    - En el caso de los comandos usados con menos frecuencia, elija letras que sean una consonante distintiva o una voz en la etiqueta, como "x" en "Salir".
    - Para los comandos usados con menos frecuencia y los selectores de cuadros de diálogo, use dos letras según sea necesario.
    - En el caso de los menús y submenús, use una sola letra para reducir el número de pulsaciones de teclas necesarias para el comando completo.
    - No use claves de acceso a partir de J, Y o Z porque se usan para pestañas contextuales, información sobre claves sin signo y grupos emergentes.
- ![captura de pantalla de información sobre claves para grupos emergentes ](images/cmd-ribbons-image58.png)<br/>**Para grupos emergentes:**
  - Use una clave de acceso de dos letras que comience por Z.
  - A partir de los grupos usados con más frecuencia, asigne la segunda letra de clave de acceso a la primera letra de la etiqueta.
  - Para los grupos restantes, elija una consonante distintiva o una voto en la etiqueta.

Para obtener instrucciones de teclas de método abreviado, vea [Teclado.](inter-keyboard.md)

### <a name="application-buttons"></a>Botones de aplicación

- **Use un botón Aplicación para presentar un menú de comandos que implican hacer algo con un archivo o con él.** Algunos ejemplos son los comandos que tradicionalmente van en el menú Archivo para crear, abrir y guardar archivos, imprimir y enviar y publicar documentos.
- **Proporcione siempre un botón Aplicación al usar una cinta de opciones.** Si el programa no usa archivos, use el botón Aplicación para acceder a las opciones del programa y al comando Salir. Los botones de aplicación siempre muestran un menú de comandos que nunca son simplemente decorados.
- **Use los siguientes comandos estándar del menú Aplicación cuando corresponda:**
  - Nuevo  
  - Abrir  
  - Guardar  
  - Guardar como...
  - Imprimir...
  - Impresión rápida  
  - Vista previa de impresión  
  - Cerrar  
  - Opciones  
  - Salir  
  
- **Reserve los comandos que pertenecen al menú Aplicación solo para ese menú.** No los coloque de forma redundante en ninguna de las pestañas.
- Para cada elemento de menú, proporcione:
  - **Etiqueta con el nombre del comando.**
  - **Icono de 32 x 32 píxeles.**
  - **Breve descripción.** Asegúrese de que la descripción se puede mostrar con como máximo dos líneas de texto.
- ![captura de pantalla de la tecla de método abreviado de documentación de información sobre herramientas ](images/cmd-ribbons-image59.png)<br/>**Use información sobre herramientas para documentar las teclas de método abreviado.** A diferencia de los menús normales, los menús de aplicación no documentan las teclas de método abreviado mediante etiquetas.

### <a name="quick-access-toolbars"></a>Barras de herramientas de acceso rápido

- **Use la barra de herramientas de acceso rápido para proporcionar acceso a los comandos usados con frecuencia.** Los comandos pueden ser desde el botón Aplicación o la cinta de opciones.
- **Proporcione siempre una barra de herramientas de acceso rápido cuando use una cinta de opciones.** Haga esto incluso si la cinta de opciones tiene una sola pestaña; esto proporciona coherencia entre programas.
- **Rellenar previamente la barra de herramientas de acceso rápido con los comandos usados con frecuencia en el menú Aplicación.** Proporcione Guardar y deshacer si el programa los admite, y Abrir e imprimir si se admite y se usa con frecuencia.
- **En el menú Personalizar barra de herramientas de acceso rápido, proporcione hasta 12 de los comandos inmediatos usados con más frecuencia.** Los comandos inmediatos no requieren entrada adicional antes de que su efecto y, por tanto, son adecuados para la barra de herramientas de acceso rápido. Aunque pueden ser comandos inmediatos, se prefieren los comandos que no están en la pestaña Inicio, ya que es más probable que los usuarios los elijan.
- **En el menú Personalizar barra de herramientas de acceso rápido, si hay un par de comandos relacionados, proporcione ambos, independientemente de la frecuencia.** Los pares comunes son Open/Close, Back/Forward y Undo/Redo.
- **En el cuadro de diálogo Personalizar barra de herramientas de acceso rápido, proporcione una manera de agregar cualquier comando.** Proporcione un filtro Comandos populares que muestre los comandos usados con más frecuencia y seleccione este filtro de forma predeterminada.

### <a name="dialog-box-launchers"></a>Selectores de cuadros de diálogo

- ![captura de pantalla del cuadro de diálogo de fuente y el grupo de fuentes ](images/cmd-ribbons-image60.png)<br/>**Proporcione un grupo con un iniciador de cuadro de diálogo si hay un cuadro de diálogo relacionado con comandos y configuraciones usados con poca frecuencia.** El cuadro de diálogo debe contener todos los comandos del grupo, además de otros que no son un conjunto de comandos completamente diferente o los mismos comandos que el grupo.
- **No use un iniciador de cuadro de diálogo para realizar comandos directamente.** Un iniciador de cuadro de diálogo debe mostrar un cuadro de diálogo.
- **No use un iniciador de cuadro de diálogo para acceder a los comandos y la configuración usados con frecuencia.** En comparación con los comandos directamente en la cinta de opciones, los comandos y la configuración del cuadro de diálogo son relativamente inexploables.
- **Haga coincidir el nombre del cuadro de diálogo con el nombre del grupo.** No tiene que ser una coincidencia exacta, pero los nombres deben ser lo suficientemente similares para que los resultados no sorprendan a los usuarios.

    **Incorrecto:**

    ![captura de pantalla del cuadro de diálogo de sonido del recordatorio ](images/cmd-ribbons-image61.png)

    Aunque un sonido de recordatorio es una opción de recordatorio, el uso del iniciador del cuadro de diálogo para establecer el sonido del recordatorio es inesperado.

- **Muestra solo los comandos y la configuración relacionados con el grupo.** Si el cuadro de diálogo muestra otras cosas, los usuarios pueden concluir que esta ruta de acceso a estos otros comandos y configuraciones es la única ruta de acceso.

    **Incorrecto:**

    ![captura de pantalla del cuadro de diálogo de fuente ](images/cmd-ribbons-image62.png)

    En este ejemplo, el cuadro de diálogo Fuente muestra la configuración espaciador de caracteres, que no está relacionada con la pestaña asociada.

## <a name="labels&quot;></a>Etiquetas

### <a name=&quot;tab-labels&quot;></a>Etiquetas de tabulación

- **Etiquete todas las pestañas.**
- Siempre que sea práctico, **use las pestañas estándar de la cinta de opciones**.
- **Prefiere etiquetas concisas y de una sola palabra.** Aunque las etiquetas de varias palabras son aceptables, necesitan más espacio y son más difíciles de localizar.
- **Elija nombres de pestaña significativos que describan clara y precisamente su contenido.** Los nombres deben ser específicos, pero no muy específicos. Los nombres de tabulación deben ser lo suficientemente predecibles para que los usuarios no se sorprendan por su contenido. Tenga en cuenta que la pestaña Inicio se denomina genéricamente porque se usa para los comandos usados con más frecuencia.
- **No use** nombres de grupo como &quot;Básico&quot; y &quot;Avanzado&quot;. Requieren que los usuarios determinen si el comando que buscan es básico o avanzado.
- **Elija nombres de pestaña que reflejen su propósito.** Tenga en cuenta los objetivos o tareas asociados a la pestaña.
- **Elija nombres de pestaña claramente distintos de los demás nombres de pestaña.**
- **Use nombres o verbos para las pestañas.** Los nombres de tabulación no requieren expresiones paralelas, así que elija la mejor etiqueta independientemente de si es un sustantivo o verbo.
- **No use los términos** (nombres que terminan en &quot;-ing"). En su lugar, use el verbo del que se deriva el archivo . (por ejemplo, use "Draw" en lugar de "Drawing").
- **Evite los nombres de tabulación con las mismas letras iniciales, especialmente las pestañas adyacentes.** Cuando se escala verticalmente la cinta de opciones, estos nombres de pestaña tendrán el mismo texto truncado.
- **Prefiere nombres singulares.** Sin embargo, puede usar un nombre pural si el nombre singular es difícil.
- **Use mayúsculas de estilo de título.**
- **No uses puntuación final.**

### <a name="contextual-tab-and-tab-set-labels"></a>Etiquetas contextuales de tabulación y conjunto de pestañas

- **Finalice las etiquetas del conjunto de pestañas contextuales con "Herramientas".** Esto ayuda a identificar el propósito de las pestañas contextuales.
- Use mayúsculas de estilo de título.
- No uses puntuación final.

### <a name="group-labels"></a>Etiquetas de grupo

- **Etiquete todos** los grupos a menos que el grupo tenga un único comando y las etiquetas de grupo y comando sean las mismas.

- **Use los grupos de la cinta de opciones estándarCuando sea práctico.**
- **Prefiere etiquetas concisas y de una sola palabra.** Aunque las etiquetas de varias palabras son aceptables, necesitan más espacio y son más difíciles de localizar.
- **Elija nombres de grupo significativos que describan clara y precisamente su contenido.** Los nombres deben ser específicos, no genéricos.
- **Elija nombres de grupo que reflejen su propósito.** Tenga en cuenta los objetivos o tareas asociados a los comandos del grupo.
- **Evite el uso de "-ing"** (nombres que terminan en "-ing"). Sin embargo, puede usar los términos si el uso del verbo del que se deriva el eund sería confuso. Por ejemplo, use "Edición" y "Prueba" en lugar de "Editar" y "Prueba".
- **No use nombres de grupo que sean iguales que los nombres de tabulación.** El uso del nombre de la pestaña en el que se encuentra el grupo no proporciona información y el uso del nombre de otra pestaña resulta confuso.
- **Prefiere nombres singulares.** Sin embargo, puede usar un nombre pural si el nombre singular es difícil. 
- **Use mayúsculas de estilo de frase.**
- **No uses puntuación final.**

### <a name="command-labels"></a>Etiquetas de comandos

- **Etiquete todos los comandos.** Tener etiquetas de texto explícitas ayuda a los usuarios a encontrar y comprender los comandos. **Excepción:** Un comando se puede desmarcar si su icono es muy conocido y el espacio es premium. Lo más probable es que los comandos sin etiquetar se encontrarán en la pestaña Inicio. En este caso, asigne su propiedad Name a una etiqueta de texto adecuada. Esto permite que los productos de tecnología de asistencia, como los lectores de pantalla, proporcionen a los usuarios información alternativa sobre el gráfico.
- **Para los botones de comando, use una etiqueta concisa y autoexplicativa.** Use una sola palabra si es posible; cuatro palabras como máximo.
- **En el caso de las listas desplegables, si la lista siempre tiene un valor, use el valor actual como etiqueta.**
- ![captura de pantalla del símbolo del sistema de la libreta de direcciones de búsqueda ](images/cmd-ribbons-image67.png)<br/>Si una [lista desplegable editable](/windows/desktop/uxguide/ctrl-drop) no tiene un valor, use un símbolo del [sistema](glossary.md).
- **Las listas desplegables que no se explican por sí solas o que se usan con poca frecuencia necesitan una etiqueta explícita.** Coloque dos puntos al final de la etiqueta.
- ![captura de pantalla de automáticamente después de: segundos<br.>Para los cuadros de \[ \] ](images/cmd-ribbons-image69.png) **texto, use una etiqueta explícita.** Coloque dos puntos al final de la etiqueta.
- **Use mayúsculas de estilo de frase.** Esto es más adecuado para el tono Windows [.](text-style-tone.md)
- **Inicie la etiqueta con un verbo imperativo.** a menos que sea igual que el nombre de la pestaña o grupo o un verbo común como Mostrar, Crear, Insertar o Formato.
- **No uses puntuación final.**
- **Para ahorrar espacio, no coloque puntos suspensivos en las etiquetas de comandos de la cinta.** Sin embargo, los comandos usan puntos suspensivos en el botón Aplicación y en los menús desplegables.

### <a name="enhanced-tooltip-labels"></a>Etiquetas de información sobre herramientas mejoradas

- **Use el título para dar el nombre del comando y su tecla de método abreviado, si procede.**
- **Para el título, no use la puntuación final.**
- **Inicie la descripción con un verbo.** Use la descripción para ayudar a los usuarios a determinar si una característica específica es la que buscan. La descripción debe estar frases para completar la frase "Esta es la característica adecuada para usar si lo desea...".
- **Mantenga la descripción corta.** Ir directamente al punto. El texto largo desaconseja la lectura.
-   ![captura de pantalla del botón de división de pegar y dos información sobre herramientas ](images/cmd-ribbons-image70.png)<br/>**Para los botones de división, use otra información sobre herramientas para explicar el menú del botón de división.**
- **Use una descripción complementaria opcional para explicar cómo usar el control .** Este texto puede incluir información sobre el estado del control (incluido por qué está deshabilitado) si el propio control no indica el estado. Mantenga este texto corto y use un tema de Ayuda para obtener explicaciones más detalladas.
- ![captura de pantalla de información sobre herramientas con gráfico y texto Para la descripción y la descripción complementaria, use oraciones ](images/cmd-ribbons-image71.png)**completas con signos de puntuación finales.**
- Use mayúsculas de estilo de frase.

### <a name="application-button-labels"></a>Etiquetas de botón de aplicación

- [captura de pantalla de la opción de impresión rápida seleccionada ](images/cmd-ribbons-image72.png)<br/>**Use "Rápido" para indicar una versión inmediata de un comando.**

- **Use puntos suspensivos para indicar que un comando requiere más información.**
- **Use mayúsculas de estilo de frase.**

## <a name="documentation"></a>Documentación

Al hacer referencia a las cintas de opciones:

- Consulte la cinta de opciones y sus componentes como cinta de opciones, pestañas, grupos y controles. Estos términos no están en mayúsculas.
- Consulte el botón de redondeo como el botón Aplicación y el menú que contiene como menú Aplicación.
- Consulte la barra de herramientas como barra de herramientas de acceso rápido.
- Consulte las pestañas por sus etiquetas y la pestaña de palabras. Use el texto exacto de la etiqueta, incluida su mayúscula.
- Consulte los comandos por sus etiquetas. Consulte los comandos sin etiquetar por sus nombres de información sobre herramientas. Use el texto exacto de la etiqueta, incluida su mayúscula, pero no incluya los puntos suspensivos. No incluya el botón de palabra ni el comando.
- Para describir la interacción del usuario, use clic para pestañas y controles. Use Entrar para listas desplegables editables. No use choose, select ni pick.
- Consulte elementos no disponibles como no disponibles, no como atenuados, deshabilitados o atenuados. En la documentación de programación, use deshabilitado.
- Cuando sea posible, formatee las etiquetas con texto en negrita. De lo contrario, coloque las etiquetas entre comillas solo si es necesario para evitar confusiones.

Ejemplos:

- En la **pestaña Inicio** , haga clic en **Pegar especial.**
- En la **pestaña Inicio** , en el **cuadro Fuente** , escriba "Segoe UI".
- En la **pestaña Revisar,** haga clic **en Mostrar marcado** y, a continuación, en **Revisores.**
- En la **pestaña Formato,** en **Herramientas de imagen**, haga clic en Comprimir **imágenes.**