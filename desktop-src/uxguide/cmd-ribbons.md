---
title: Barras de herramientas
description: Las cintas de opciones son la manera moderna de ayudar a los usuarios a encontrar, comprender y usar comandos de forma eficaz y directa \ 8212; con un número mínimo de clics, con menos necesidad de recurrir a la prueba y el error, y sin tener que consultar la ayuda.
ms.assetid: 8a4699da-9840-4622-9e94-d6d5c4e7708c
ms.custom: contperf-fy21q1
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 2327a633f02c9d56116367405803c4da56ad5b19
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104361804"
---
# <a name="ribbons"></a>Barras de herramientas

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

Las cintas de opciones son la manera moderna de ayudar a los usuarios a buscar, comprender y usar comandos de forma eficaz y directa con un número mínimo de clics, con menos necesidad de recurrir a la prueba y el error, y sin tener que hacer referencia a la ayuda.

Una cinta de opciones es una barra de comandos que organiza las características de un programa en una serie de pestañas en la parte superior de una ventana. El uso de una cinta aumenta la capacidad de detección de las características y las funciones, permite un aprendizaje más rápido del programa en su conjunto y hace que los usuarios sientan más el control de su experiencia con el programa. Una cinta de opciones puede reemplazar a la barra de menús y las barras de herramientas tradicionales.

![captura de pantalla de una cinta de opciones ](images/cmd-ribbons-image1.png)

Una cinta de opciones típica.

Las pestañas de la cinta de opciones se componen de grupos, que son un conjunto con etiqueta de comandos estrechamente relacionados. Además de las pestañas y los grupos, las cintas de opciones constan de:

- Un botón aplicación, que presenta un menú de comandos que implica realizar algo en o con un documento o área de trabajo, como comandos relacionados con archivos.
- Barra de herramientas de acceso rápido, que es una pequeña barra de herramientas personalizable que muestra los comandos usados con frecuencia.
- Las pestañas principales son las pestañas que se muestran siempre.
- Pestañas contextuales, que solo se muestran cuando se selecciona un tipo de objeto determinado. Las pestañas que se muestran siempre se denominan pestañas básicas.
- Un conjunto de pestañas es una colección de pestañas contextuales para un único tipo de objeto. Dado que los objetos pueden tener varios tipos (por ejemplo, un encabezado de una tabla que tiene una imagen es tres tipos), se pueden mostrar varios conjuntos de pestañas contextuales a la vez.
- Pestañas modales, que son pestañas principales que se muestran con un modo temporal determinado, como la vista previa de impresión.
- Galerías, que son listas de comandos u opciones que se presentan gráficamente. Una galería basada en resultados ilustra el efecto de los comandos u opciones en lugar de los propios comandos. En una cinta de opciones, se muestra una galería de la cinta de opciones, en lugar de una ventana emergente.
- Información sobre herramientas mejorada, que explican de manera concisa sus comandos asociados y proporcionan las teclas de método abreviado. También pueden incluir gráficos y referencias a la ayuda. La información sobre herramientas mejorada reduce la necesidad de ayuda relacionada con los comandos.
- Iniciadores de cuadros de diálogo, que son botones en la parte inferior de algunos grupos que abren cuadros de diálogo que contienen características relacionadas con el grupo.

Las cintas de opciones se introdujeron originalmente con Microsoft Office 2007. Para saber por qué Office necesita usar las cintas de opciones y los muchos problemas que se resuelven al usar una cinta de opciones, consulte [la historia de la cinta de](/archive/blogs/jensenh/the-story-of-the-ribbon)opciones.

> [!Note]  
> Las instrucciones relacionadas con los [menús](cmd-menus.md), las [barras de herramientas](cmd-toolbars.md), los [botones de comando](ctrl-command-buttons.md)y los [iconos](vis-icons.md) se presentan en artículos independientes.

## <a name="is-this-the-right-user-interface"></a>¿Es la interfaz de usuario correcta?

Para decidir usar una cinta de opciones, tenga en cuenta estas preguntas:

### <a name="program-type"></a>Tipo de programa

- **¿Qué tipo de programa está diseñando?** El tipo de programa es un buen indicador de la adecuada de una cinta de opciones. Las cintas de opciones funcionan bien para la creación y los programas de creación de documentos, así como para visores y exploradores de documentos. Las cintas de opciones pueden funcionar en otros tipos de programas, pero es posible que otras formas de presentación de comandos sean más adecuadas. Por lo general, los programas ligeros deben tener una presentación de comandos ligera.

### <a name="discoverability-and-learning-issues"></a>Problemas de detección y aprendizaje

- **¿Los usuarios tienen problemas para encontrar comandos? ¿Los usuarios solicitan características que ya están en el programa?** Si es así, el uso de una cinta de opciones facilitará la búsqueda de comandos mediante etiquetas autoexplicativas y agrupación de comandos relacionados. El uso de una cinta también se escala mejor que las barras de menús y las barras de herramientas para el crecimiento futuro.
- **¿Los usuarios tienen problemas para entender los comandos del programa? ¿Suelen recurrir a "prueba y error" para seleccionar el comando correcto o determinar cómo funcionan los comandos?** Si es así, el uso de una cinta con comandos orientados a resultados basados en galerías y vistas previas dinámicas facilita la comprensión de los comandos.

### <a name="command-characteristics"></a>Características del comando

- **¿Los comandos se muestran en varias ubicaciones? Si el programa ya existe, ¿los comandos se muestran en barras de menús, barras de herramientas, paneles de tareas y dentro del área de trabajo?** Si es así, el uso de una cinta de opciones unificará los comandos en una sola ubicación, lo que facilita su búsqueda.
- **¿Los comandos se aplican a toda la ventana o solo a paneles específicos?** Las cintas funcionan mejor en los comandos que se aplican a toda la ventana o a objetos específicos. Los comandos en contexto funcionan mejor para los paneles de ventana individuales.
- **¿Se puede presentar la mayoría de los comandos directamente? Es decir, ¿pueden los usuarios interactuar con ellos mediante un solo clic? Si se tiene acceso a los comandos usados con frecuencia desde los menús y los cuadros de diálogo, ¿se pueden refactorizar para ser directos?** Aunque algunos comandos se pueden presentar con menús y cuadros de diálogo, la mayoría de los comandos de esta manera desmine la eficacia de una cinta de opciones, lo que podría hacer que una barra de menús sea una opción mejor.

### <a name="command-scale"></a>Escala de comandos

- **¿Hay un pequeño número de comandos? ¿Se pueden presentar fácilmente los comandos usados con más frecuencia en una sola barra de herramientas sencilla?** El uso de una cinta de opciones merece la pena si la adición de pestañas básicas y contextuales da como resultado una pestaña principal simple que se puede usar solo para realizar las tareas más comunes. Si no es así, es posible que la ventaja de usar una cinta de opciones no justifique su peso adicional para un pequeño número de comandos.
- **¿Hay un gran número de comandos? Usar una cinta requiere más de siete pestañas principales? ¿Los usuarios tendrían que cambiar constantemente las pestañas para realizar tareas comunes?** Si es así, el uso de barras de herramientas (que no requieren pestañas de cambio) y [ventanas de paleta](cmd-toolbars.md) (que pueden requerir cambiar las pestañas, pero puede haber varias abiertas a la vez) puede ser una opción más eficaz.
- **¿Los usuarios tienden a usar un pequeño número de comandos la mayor parte del tiempo?** Si es así, puede usar una cinta de opciones de forma eficaz si coloca estos comandos en la pestaña Inicio. Las pestañas que cambian constantemente harán que una cinta de opciones sea demasiado ineficaz.
- **¿El programa se beneficia de hacer que el área de contenido del programa sea lo más grande posible?** Si es así, el uso de una barra de menús y una sola barra de herramientas es más eficaz que una cinta. Sin embargo, si el programa requiere tres o más filas de barras de herramientas o usa paneles de tareas, el uso de una cinta es más eficaz.
- **¿Los usuarios tienden a trabajar en un área específica dentro de una ventana grande del programa durante largos períodos de tiempo?** Si es así, se beneficiaría de la proximidad de las barras de herramientas, las ventanas de paleta y los comandos directos. Realizar el recorrido de ida y vuelta desde el área de trabajo hasta la cinta de opciones sería demasiado ineficaz.
- **Por motivos de eficacia y flexibilidad, ¿es necesario que los usuarios realicen cambios significativos en el contenido, la ubicación o el tamaño de la presentación del comando?** Si es así, las ventanas de paleta y las barras de herramientas personalizables y extensibles son una mejor opción. Tenga en cuenta que algunos tipos de barras de herramientas se pueden desacoplar para que se conviertan en ventanas de paleta y las ventanas de paleta se pueden cambiar, cambiar de tamaño y personalizar.

Por último, tenga en cuenta esta última pregunta: ¿ **la mejora en la detectabilidad, la facilidad de aprendizaje, la eficacia y la productividad merecen el costo del espacio adicional y la necesidad de pestañas para organizar los comandos?** Si es así, el uso de una cinta es una opción excelente. Si no está seguro, considere la posibilidad de usar un diseño basado en cinta y compararlo con la mejor alternativa.

Las cintas de opciones son una forma nueva y atractiva de presentación de comandos y una excelente manera de modernizar un programa. Pero tan atractivo como lo son, no son la opción adecuada para todos los programas.

**Incorrecto:**

![captura de pantalla de una cinta de opciones con una calculadora ](images/cmd-ribbons-image2.png)

No lo haga.

## <a name="seven-most-important-things"></a>Siete cosas más importantes

1. Elija una solución de comando que sea adecuada para el tipo de programa. El uso de una cinta de opciones debe hacer que un programa sea más sencillo, más eficaz y fácil de usar nunca lo contrario. Si el uso de una cinta no es adecuado, considere la posibilidad de usar comandos enriquecidos en su lugar.  
2. No subestimar el desafío de crear una cinta de opciones efectiva. No se espera que sea un puerto simple de las barras de menús y las barras de herramientas existentes. Y no se aplican los permisos concedidos por el uso de una cinta de opciones para mejorar el programa. Estar dispuesto a confirmar el tiempo y el esfuerzo necesarios para el rediseño de un comando es un factor importante a la hora de decidirse a usar una cinta de opciones.  
3. Haga que los comandos sean reconocibles. Elija un diseño de pestaña que tenga una asignación clara, obvia y exclusiva entre los comandos y las pestañas con etiqueta descriptiva en las que residen. Los usuarios deben poder determinar con rapidez y confianza qué pestaña tiene el comando que buscan y, en raras ocasiones, elegir la pestaña equivocada.  
4. Haga que los comandos sean autoexplicativos. Los usuarios deben entender el efecto de un comando con respecto a su etiqueta, icono, información sobre herramientas y vista previa. No deben tener que experimentar ni leer un tema de ayuda para ver cómo funciona un comando.  
5. Haga uso de los comandos eficientes:
    - Los usuarios deben gastar la mayor parte del tiempo en la pestaña Inicio.
    - En raras ocasiones, los usuarios deben cambiar las pestañas durante las tareas comunes.
    - Cuando la ventana está maximizada y los usuarios están en la pestaña correcto, los comandos que se usan con más frecuencia tienen el énfasis más visual y los usuarios pueden invocarlos con un solo clic. Los usuarios pueden realizar todos los demás comandos de la pestaña con al menos cuatro clics.
    - Los usuarios no deben tener que abrir cuadros de diálogo para proporcionar comandos y cambiar atributos en tareas comunes.
6. Ayude a los usuarios a elegir comandos y opciones con confianza y minimizar la necesidad de prueba y error. Use comandos orientados a resultados siempre que sea necesario, a menudo en forma de galerías y vistas previas dinámicas.  
7. Asegúrese de que la cinta de opciones se escala bien desde los tamaños de ventana más grandes hasta el más pequeño.  

## <a name="design-concepts"></a>Conceptos de diseño

### <a name="adapting-a-ribbon-in-an-existing-program"></a>Adaptar una cinta de opciones en un programa existente

Aunque podría simplemente refactorizar un diseño de barra de herramientas y una barra de herramientas tradicionales de un programa existente a un formato de cinta, al hacerlo se pierde la mayor parte del valor de usar una cinta de opciones. Las cintas de opciones tienen el máximo valor cuando se usan para presentar comandos inmediatos orientados a los resultados, a menudo en forma de galerías y vistas previas dinámicas. Los comandos orientados a resultados facilitan la comprensión de los comandos y los usuarios son mucho más eficientes y productivos. En lugar de refactorizar los comandos existentes, es mejor rediseñar completamente el modo en que se realizan los comandos en el programa.

No subestimar el desafío de crear una cinta de opciones efectiva. Y no se aplican los permisos concedidos por el uso de una cinta de opciones para mejorar el programa. La creación de una cinta de opciones eficaz requiere mucho tiempo y esfuerzo. Estar dispuesto a confirmar el tiempo y el esfuerzo necesarios para este rediseño de comando es un factor importante a la hora de decidir usar una cinta de opciones.

### <a name="the-nature-of-ribbons"></a>La naturaleza de las cintas de opciones

En comparación con las barras de menús y las barras de herramientas tradicionales, las cintas de opciones tienen las siguientes características:

- **Una sola interfaz de usuario (UI) para todos los comandos.** Las barras de menús son completas y fáciles de aprender, y las barras de herramientas son eficaces y directas, pero ¿por qué no usar un poco más de espacio de pantalla para crear una interfaz de usuario de comandos única que realice todas estas cosas? Con solo una interfaz de usuario, las cintas de opciones no requieren que los usuarios averigüen qué interfaz de usuario tiene el comando que están buscando.
- **Visible y autoexplicativo.** Los comandos de la barra de menús se explican por sí solos a través de sus etiquetas, pero se ocultan en la mayor parte del tiempo. Para ahorrar espacio en la pantalla, los botones de la barra de herramientas se representan principalmente mediante iconos en lugar de etiquetas (aunque algunos botones de la barra de herramientas usan ambos) y dependen de la información sobre herramientas cuando el icono no se explica por sí mismo. Sin embargo, los usuarios generalmente saben los iconos únicamente para los comandos que se usan con más frecuencia.
- Al presentar la mayoría de los comandos con iconos con etiqueta, los comandos de la cinta de opciones son visibles y autoexplicativos, y usan la información sobre herramientas únicamente para proporcionar información complementaria. Hay poca necesidad de ir a otra parte (como ayuda) para comprender un comando.
- **Agrupación de etiquetas.** Mientras que las categorías de menús tienen la etiqueta, los grupos dentro de un menú desplegable no se indican y solo se indican con un separador sin etiquetar. Los grupos dentro de las barras de herramientas también se indican con separadores sin etiquetar.
- Mediante la organización de comandos en grupos con etiqueta, las cintas de opciones facilitan la búsqueda de comandos y la determinación de su propósito.
- **Modal pero no jerárquico.** Las barras de menús se escalan creando una jerarquía de comandos. Los menús con muchos elementos pueden usar uno o varios niveles de submenús para proporcionar más comandos.
- Los comandos de la cinta requieren más espacio que los comandos de la barra de herramientas, por lo que usan pestañas para escalar. Este uso de las pestañas hace que las cintas de opciones sean modales y requieren que los usuarios cambien los modos ocasionalmente para buscar comandos. Sin embargo, dentro de una pestaña, la mayoría de los comandos son directos o usan un solo botón de expansión o botón de menú, no una jerarquía.
- **Directa e inmediata.** Un comando es directo si se invoca con un solo clic (es decir, sin navegar por los menús) y de inmediato si surte efecto inmediatamente (es decir, sin cuadros de diálogo para recopilar datos adicionales). Los comandos de la barra de menús siempre son indirectos y a menudo no son inmediatos. Al igual que las barras de herramientas, la mayoría de los comandos de la cinta están diseñados para ser directos e inmediatos, con los comandos que se usan con más frecuencia se invocan con un solo clic y sin necesidad de un cuadro de diálogo para recopilar datos adicionales.
- **"Espacioso".** Las barras de menús y las barras de herramientas están diseñadas principalmente para que el espacio sea eficiente. Para proporcionar sus ventajas, las cintas de opciones pueden consumir más espacio vertical, aproximadamente el equivalente de una barra de menús más tres filas de barras de herramientas. Cuando hay pocos programas que tienen tres o más filas de barras de herramientas, las cintas suelen consumir más espacio que las interfaces de IU tradicionales para los comandos.
- **Tiene un botón de aplicación y una barra de herramientas de acceso rápido.** Una cinta de opciones siempre se presenta con un botón de aplicación y una barra de herramientas de acceso rápido. Esto permite a los usuarios tener acceso a comandos relacionados con archivos y usados con frecuencia sin cambiar las pestañas y promueve la coherencia entre programas.
- **Personalización mínima.** Mientras que las barras de menús tienen una presentación fija, muchas barras de herramientas son bastante personalizables, lo que permite a los usuarios establecer ubicaciones, tamaños y contenido. No se puede personalizar una cinta de opciones, pero la barra de herramientas de acceso rápido proporciona una personalización limitada.
- **Accesibilidad mejorada del teclado.** Las barras de menús tienen una accesibilidad de teclado excelente, porque al presionar la tecla Alt directamente, se proporciona el foco de entrada de la barra de menús. Sin embargo, no hay ningún mecanismo de este tipo para las barras de herramientas porque comparten la navegación mediante el teclado con el contenido de la ventana. Por lo tanto, los usuarios deben ir a la barra de herramientas mediante la tecla TAB (que recibe la última tabulación) y, a continuación, navegar a un comando específico con las teclas de dirección.

Por el contrario, las cintas proporcionan una accesibilidad de teclado mejorada mediante [keytips](glossary.md), normalmente con un proceso de tres pasos:

- Presione Alt para entrar en el modo KeyTip.
- Presione un carácter para elegir una pestaña, el botón aplicación o un comando en la barra de herramientas de acceso rápido.
- En una pestaña, presione una o dos letras para elegir un comando.

    Este enfoque es muy visual. También es más flexible, lo que permite escalar mejor y tener más asignaciones de teclas de acceso de la tecla de acceso.

    No confunda las claves de acceso con teclas de método abreviado. Aunque tanto las teclas de acceso como las teclas de acceso directo proporcionan acceso de teclado a la interfaz de usuario, tienen distintos propósitos e instrucciones. Para obtener más información, consulte [teclado](inter-keyboard.md).

### <a name="the-nature-of-rich-commands"></a>La naturaleza de los comandos enriquecidos

Los comandos enriquecidos hacen referencia a la presentación y la interacción de los comandos usados por las cintas de opciones, sin necesidad de usar un contenedor de la cinta de opciones. Los comandos enriquecidos tienen estas características:

- **Etiquetado.** A todos los comandos se les proporcionan etiquetas autoexplicativas, con excepciones solo cuando los iconos son extremadamente conocidos y el espacio es Premium.

    **Correcto:**

    ![captura de pantalla de una cinta de opciones de formato de caracteres ](images/cmd-ribbons-image3.png)

    Estos comandos son muy conocidos, por lo que no necesitan etiquetas.

    **Incorrecto:**

    ![captura de pantalla de una cinta con iconos de uso poco frecuente ](images/cmd-ribbons-image4.png)

    Estos iconos ininteligibles requieren etiquetas para comandos enriquecidos.

- **Server.** En lugar de ajustar el tamaño uniforme, los comandos tienen un tamaño relativo a su frecuencia de uso y importancia. Además de facilitar la búsqueda y el clic en los comandos usados con mayor frecuencia, también hace que sean más fáciles de [encontrar.](https://msdn.microsoft.com/library/windows/desktop/cc872774.aspx)

    ![captura de pantalla de un botón grande y tres botones pequeños ](images/cmd-ribbons-image5.png)

    En este ejemplo, el botón que se usa con más frecuencia es mayor que los demás.

- **Cambio de tamaño dinámico.** Controles de comandos enriquecidos se cambian de tamaño para sacar el máximo partido del espacio disponible, en lugar de usar un tamaño fijo y truncar o usar el desbordamiento cuando el tamaño es demasiado pequeño.

    ![captura de pantalla de la cinta ancha con botones de igual tamaño ](images/cmd-ribbons-image6.png)![captura de pantalla de una cinta pequeña con botones combinados ](images/cmd-ribbons-image7.png)

    En este ejemplo, se cambia el tamaño de los botones de comando para que funcionen bien en el espacio disponible.

- **Botones de expansión.** Los botones de expansión son una buena manera de consolidar un conjunto de variaciones de un comando cuando sea necesario, al tiempo que se mantiene la dirección del comando que se usa con más frecuencia.

    ![captura de pantalla del comando Guardar como y sus opciones ](images/cmd-ribbons-image8.png)

    En este ejemplo, el comando Guardar como usa un botón de expansión, donde el botón principal realiza la variación más común y la parte de menú revela un menú con variaciones del comando.

- **Menús desplegables y galerías enriquecidos.** Los menús desplegables, las listas desplegables y las galerías ocupan el espacio necesario para comunicarse y diferenciar el efecto de las opciones, a menudo mediante gráficos y descripciones de texto. Las categorías se utilizan para organizar grandes conjuntos de opciones.

    ![captura de pantalla de opciones de menú desplegable con iconos ](images/cmd-ribbons-image9.png)

    En estos ejemplos, al hacer clic en un botón de menú, se muestra una lista de opciones que muestran su efecto.

- **Vistas previas en vivo.** Siempre que el usuario mantiene el puntero sobre una opción de formato, el programa muestra el aspecto que tendrían los resultados con ese formato usando el contenido real.

    ![captura de pantalla de los resultados de las opciones de formato ](images/cmd-ribbons-image10.png)

    Las vistas previas activas muestran los resultados de aplicar una opción de formato al mantener el mouse.

- **Información sobre herramientas mejorada.** Explican de manera concisa sus comandos asociados y proporcionan las teclas de método abreviado. También pueden incluir gráficos y referencias a la ayuda (aunque eliminan en gran medida la necesidad de ayuda relacionada con comandos).

    ![captura de pantalla de información sobre herramientas grande con texto y gráfico ](images/cmd-ribbons-image11.png)

    La información sobre herramientas mejorada explica de manera concisa sus comandos asociados.

Aunque es posible que las cintas de opciones no sean adecuadas para todos los programas, todos los programas podrían beneficiarse de comandos enriquecidos.

### <a name="ribbons-always-have-an-application-button-and-quick-access-toolbar"></a>Las cintas de opciones siempre tienen un botón de aplicación y una barra de herramientas de acceso rápido

El botón aplicación y la barra de herramientas de acceso rápido proporcionan comandos útiles en cualquier contexto, lo que reduce la necesidad de cambiar las pestañas. Aunque estos tres componentes son lógicamente independientes, una cinta de opciones siempre debe tener un botón de aplicación y una barra de herramientas de acceso rápido. Dado que los comandos pueden ir en la cinta de opciones o en el botón aplicación, es posible que se pregunte dónde colocar los comandos. La elección no es arbitraria.

El botón aplicación se usa para presentar un menú de comandos que implican realizar algo en o con un archivo, como los comandos que tradicionalmente se encuentran en el menú Archivo para crear, abrir y guardar archivos, imprimir y enviar y publicar documentos.

Por el contrario, la cinta de opciones es para los comandos que afectan al contenido de la ventana. Algunos ejemplos son los comandos que se usan para leer, modificar o usar el contenido, o cambiar la vista.

Si usa una cinta de opciones, también debe usar un botón de aplicación incluso si el programa no implica documentos ni archivos. En tales casos, use el menú aplicación para presentar comandos para imprimir, opciones de programa y salir del programa. Aunque es posible que el botón aplicación no sea necesario para estos programas, el uso proporciona coherencia entre programas. Los usuarios no tienen que buscar los comandos para guardar y deshacer o las opciones del programa porque siempre están en el mismo lugar.

La barra de herramientas de acceso rápido es necesaria incluso si la cinta de opciones solo utiliza una pestaña. Una vez más, si bien estos programas no necesitan una barra de herramientas de acceso rápido (porque todos los comandos ya están presentes en la única pestaña), tener una barra de herramientas de acceso rápido personalizable proporciona coherencia entre los programas. Por ejemplo, si los usuarios se acostumbran a hacer clic en el comando imprimir, deberían poder hacerlo en cualquier programa que use una cinta de opciones.

### <a name="organization-and-discoverability"></a>Organización y detectabilidad

Al proporcionar pestañas y grupos, las cintas de opciones permiten organizar los comandos para facilitar la detección. El reto es que si la organización se hace mal, puede perjudicar en gran medida la capacidad de detección. Debe haber una asignación clara, obvia y única entre los comandos y las pestañas y los grupos con etiquetas descriptivas donde residen.

Los usuarios formarán un modelo mental de la cinta de opciones después de usarlo durante un tiempo. Si ese modelo mental no tiene sentido para los usuarios, es ineficaz o es incorrecto, dará lugar a confusión y frustración. **El objetivo más importante para diseñar una cinta es facilitar la búsqueda de comandos de forma rápida y segura. Si no lo hace, se producirá un error en el diseño de la cinta.** Lograr este objetivo requiere un cuidadoso diseño, pruebas de usuario e iteración. No asuma que será fácil.

Estos son algunos problemas comunes que se pueden evitar:

- **Evite los nombres de pestañas y grupos genéricos.** Un buen nombre de ficha o grupo debe describir con precisión su contenido específico, preferiblemente mediante el lenguaje basado en tareas y objetivos. Evite los nombres de pestañas y grupos genéricos, así como los nombres basados en tecnología. Por ejemplo, prácticamente cualquier comando de un documento crear y crear programa podría pertenecer a pestañas de edición, formato, herramientas, opciones, avanzadas y mucho más. Confíe en etiquetas descriptivas específicas, no en memorización.
- **Evite los nombres de pestaña y grupo demasiado específicos.** Aunque queremos que los nombres de las pestañas y los grupos sean específicos, no deben ser tan específicos que los usuarios se sorprendan por su contenido. A menudo, los usuarios buscan cosas con el proceso de eliminación, por lo que no pueden ver las pestañas o los grupos porque el nombre es engañoso.
- **Evite varias rutas de acceso al mismo comando, especialmente si la ruta de acceso es inesperada o si el comando requiere muchos clics para invocar.** Puede parecer una comodidad para encontrar un comando a través de varias rutas de acceso. Pero tenga en cuenta que cuando los usuarios encuentran lo que están buscando, dejan de buscar. A los usuarios les resulta demasiado fácil asumir que la primera ruta de acceso que encuentran es la única ruta de acceso que es un problema grave si esa ruta de acceso es ineficaz o inesperada. Además, tener comandos duplicados dificulta a los usuarios la búsqueda de otros comandos que están buscando.

![captura de pantalla de la ruta de acceso indirecta al comando de bordes ](images/cmd-ribbons-image12.png)

En este ejemplo, puede cambiar los bordes de párrafo a través del comando bordes de página, aunque haya una ruta de acceso más directa en la pestaña Inicio. Si los usuarios que buscan bordes de párrafo fueran caso en esta ruta de acceso inesperada, pueden suponer fácilmente que es la única ruta de acceso.

- **Evite la colocación de comandos arbitraria.** Supongamos que tiene un buen diseño de pestañas y grupos, pero descubre que no caben varios comandos. Lo más probable es que el diseño de la pestaña y el grupo no sea tan bueno como cree que es y que tenga que seguir refinando. No solucione este problema colocando los comandos a los que no pertenecen. Si lo hace, es probable que los usuarios tengan que inspeccionar todas las pestañas para encontrarlas y, después, olvidar dónde se encuentran.
- **Evite la colocación basada en marketing.** Supongamos que tiene una nueva versión del programa y que el equipo de marketing realmente desea promocionar sus nuevas características. Podría ser tentador colocarlas en la pestaña Inicio, pero hacerlo es un error costoso si se daña la detectabilidad global. Tenga en cuenta las versiones futuras del producto y la cantidad de frustración que producirá una organización que cambia constantemente.

### <a name="tabs"></a>Tabulaciones

El mejor primer paso es revisar las [pestañas estándar](#standard-ribbon-tabs)de la cinta de opciones. Si los comandos del programa se asignan de forma natural a las pestañas estándar, base la organización de pestañas en estos estándares. Por otro lado, si los comandos del programa no se asignan de forma natural, no intente forzarlos. Determine una estructura más natural y asegúrese de realizar una serie de pruebas de usuario para asegurarse de que la tiene correcta.

En el caso de pestañas no estándar, tenga en cuenta estos problemas:

- **Cada nombre de pestaña debe describir su contenido.** Elija nombres descriptivos que sean específicos, pero no demasiado específicos. Los usuarios nunca deben sorprender por su contenido.
- **Cada nombre de pestaña debe reflejar su propósito.** Tenga en cuenta el objetivo o la tarea asociada a los comandos.
- **Cada nombre de pestaña debe ser claramente distinto de los demás nombres de pestaña.**

La pestaña Inicio es una excepción a estas consideraciones. Aunque no es necesario tener una pestaña Inicio, la mayoría de los programas deberían. La pestaña Inicio es la primera pestaña y contiene los comandos que se usan con más frecuencia. Si los comandos usados con frecuencia no caben en las otras pestañas, la pestaña Inicio es el lugar adecuado para ellos.

Si no puede determinar un nombre de pestaña descriptivo significativo, es probable que la pestaña no esté bien diseñada. Si la organización de la cinta no funciona, reconsidere el diseño de las pestañas.

### <a name="groups"></a>Grupos

La división de comandos en grupos estructura los comandos en conjuntos relacionados. La etiqueta de grupo explica el propósito habitual de sus comandos.

Hay varios factores que se deben tener en cuenta a la hora de determinar los grupos y su presentación:

- **Agrupación estándar.** Aunque hay diferencias importantes en los comandos de todos los programas, hay [grupos estándar](#standard-ribbon-groups) que son comunes a muchos programas. Si estos comandos aparecen con los mismos nombres y ubicaciones similares, se mejora considerablemente la detectabilidad.

| Correcto                                                                                      | Incorrecto                                                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| ![captura de pantalla de zoom separado del grupo de edición ](images/cmd-ribbons-image13.png)<br/>El grupo comandos de edición incluye todos los comandos de edición, pero no incluye el comando zoom.         | ![captura de pantalla del zoom incluido en el grupo de edición ](images/cmd-ribbons-image14.png)<br/>El comando zoom no es un comando de edición, pero está en el grupo de edición. |

- **Granularidad.** Una estructura es buena, pero demasiada estructura hace que los comandos sean más difíciles de encontrar. Si los nombres de grupo son genéricos, es posible que no tenga una granularidad suficiente. Si hay grupos con solo uno o dos comandos, es probable que tenga demasiados (aunque es aceptable tener una galería en cinta sin ningún otro comando dentro de un grupo).

| Correcto                                                                                                 | Incorrecto                                                                                                  |
|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| ![captura de pantalla de zoom separado del grupo de edición ](images/cmd-ribbons-image13.png)<br/> El grupo comandos de edición incluye todos los comandos de edición| ![captura de pantalla del grupo de edición división en dos grupos ](images/cmd-ribbons-image15.png)<br/>El grupo comandos de edición se ha dividido en secciones que son demasiado granulares. Evite grupos con solo uno o dos comandos.|

- **Nombres.** Los nombres de grupo correctos explican el propósito de sus comandos. Si los nombres de grupo no son, reconsidere el nombre o la agrupación. Si no puede determinar un nombre descriptivo significativo, es probable que el grupo no esté bien diseñado.

| Correcto                                                                                                 | Incorrecto                                                                                                  |
|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| ![captura de pantalla de comandos divididos en cuatro grupos ](images/cmd-ribbons-image17.png) <br/> Use nombres de grupo que sean lo suficientemente específicos como para describir los comandos contenidos en el grupo. | ![captura de pantalla del grupo de formato con varios comandos ](images/cmd-ribbons-image16.png) <br/> Este nombre de grupo es demasiado impreciso para ser útil. Un mejor enfoque sería reorganizar estos comandos en grupos más específicos. |

- **Orden.** Las personas leen en orden de izquierda a derecha (en el caso de las culturas occidentales), por lo que puede pensar que los grupos de la izquierda son los más evidentes. Sin embargo, el nombre de la pestaña resaltada y el contenido de la ventana tienden a actuar como [puntos focales](vis-layout.md), por lo que los grupos en el centro de la pestaña suelen recibir más atención que el grupo situado más a la izquierda. Coloque los grupos que se usan con más frecuencia en las ubicaciones más destacadas y asegúrese de que hay un flujo lógico para los grupos en la pestaña.

![captura de pantalla del grupo del portapapeles en el extremo izquierdo ](images/cmd-ribbons-image18.png)

En este ejemplo, los grupos de fuentes y de párrafos son más perceptibles que el grupo del portapapeles, porque son lo que ve primero el ojo al desplazarse hacia arriba desde el documento.

![captura de pantalla del grupo de seguimiento en la pestaña revisar ](images/cmd-ribbons-image19.png)

En este ejemplo, el grupo de seguimiento recibe la mayor atención, en parte porque la pestaña revisión resaltada actúa como punto focal.

- **Uniformidad.** Puede ser difícil reconocer comandos cuando la presentación del comando tiene el mismo aspecto. El uso de iconos con diferentes formas y colores, grupos con formatos diferentes y comandos con distintos tamaños facilita a los usuarios el reconocimiento de grupos de comandos. Los comandos deben tener un tamaño uniforme solo cuando la cinta se reduce verticalmente a sus tamaños más pequeños.

| Correcto | Incorrecto |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| ![captura de pantalla del grupo con iconos de tamaño diferente ](images/cmd-ribbons-image20.png)<br/>Usar diversos tamaños de iconos para mejorar la reconocibilidad| ![captura de pantalla del grupo con iconos del mismo tamaño ](images/cmd-ribbons-image21.png)<br/>Estos comandos parecen ser demasiado similares, ya que tienen el mismo tamaño. |

### <a name="previews"></a>Vistas previas

Puede usar varios tipos de vistas previas para mostrar lo que resultará de un comando. Mediante el uso de vistas previas útiles, puede mejorar la eficacia del programa y reducir la necesidad de un enfoque de aprendizaje de prueba y error. Las vistas previas en vivo también invitan a experimentar y fomentan la creatividad.

Estos son algunos de los distintos tipos de vistas previas que puede usar:

- **Gráficos y iconos estáticos realistas.** Imágenes estáticas que proporcionan una indicación realista del efecto de un comando. Se pueden usar en galerías, menús desplegables y mejoras en la información sobre herramientas.

![captura de pantalla de la lista desplegable fuente ](images/cmd-ribbons-image22.png)

En este ejemplo, la lista desplegable fuente muestra cada nombre de fuente utilizando la propia fuente.

![captura de pantalla de la galería de miniaturas de marcas de agua ](images/cmd-ribbons-image23.png)

En este ejemplo, se usan miniaturas realistas para mostrar las diferentes marcas de agua.

- **Iconos y gráficos dinámicos.** Iconos y gráficos que se modifican para reflejar el estado actual. Estos iconos son especialmente útiles para las galerías, así como los botones de expansión que cambian su efecto predeterminado para que sean los mismos que la última acción.

![captura de pantalla de la galería de estilos de párrafo ](images/cmd-ribbons-image24.png)

En este ejemplo, Microsoft Word cambia la galería de estilos para reflejar los estilos actuales.

![captura de pantalla de los botones de comando de formato de texto ](images/cmd-ribbons-image25.png)

En este ejemplo, Word cambia los comandos color de resaltado de texto y color de fuente para indicar su efecto actual.

- **Vistas previas en vivo.** Cuando los usuarios mantienen el mouse sobre una opción de formato, la vista previa dinámica muestra el aspecto que tendrían los resultados con ese formato. Las vistas previas dinámicas ayudan a los usuarios a hacer selecciones de forma más eficaz y segura en función del contexto real del usuario.

![captura de pantalla del selector de color de comando de color de página ](images/cmd-ribbons-image26.png)

En este ejemplo, el comando color de página realiza una vista previa dinámica mostrando el efecto de las opciones de color al mantener el mouse.

Las vistas previas en vivo son una característica eficaz que puede mejorar realmente la productividad de los usuarios, pero incluso las vistas previas estáticas simples pueden ser una gran ayuda.

### <a name="scaling-the-ribbon"></a>Escalado de la cinta de opciones

El escalado de una barra de herramientas es sencillo: Si una ventana es demasiado estrecha para mostrar una barra de herramientas, la barra de herramientas muestra lo que cabe y hace que todo lo demás sea accesible a través de un botón de desbordamiento. Un objetivo de comandos enriquecidos es sacar el máximo partido del espacio disponible, por lo que el escalado de una cinta requiere más trabajo de diseño. No hay ningún tamaño de cinta predeterminado, por lo que no debe diseñar una cinta con un ancho determinado en mente. Tiene que diseñar diseños con una amplia gama de anchos y tener en cuenta que cualquiera de ellos podría ser el que la mayoría de los usuarios verán. El escalado es una parte fundamental del diseño de la cinta, no del último paso. Al diseñar una pestaña, especifique los distintos diseños para cada grupo (hasta tres), así como las combinaciones que se pueden usar conjuntamente. La cinta de opciones mostrará la combinación válida más grande que se ajusta al tamaño de la ventana actual.

![captura de pantalla de comandos de formato en la barra de herramientas del menú de desbordamiento ](images/cmd-ribbons-image27.png) escale mediante un botón de desbordamiento.

![captura de pantalla de las cintas de opciones con varios anchos ](images/cmd-ribbons-image28.png) no hay ningún tamaño de cinta predeterminado. El tamaño mínimo es un único icono de grupo emergente.

## <a name="guidelines"></a>Directrices

### <a name="general"></a>General

- **No combine las cintas de opciones con barras de menús y barras de herramientas en una ventana.** Las cintas de opciones deben usarse en lugar de las barras de menús y las barras de herramientas. Sin embargo, una cinta de opciones puede combinarse con ventanas de paleta y elementos de navegación, como botones atrás y adelante y una barra de direcciones.
- **Combine siempre una cinta con un botón de aplicación y una barra de herramientas de acceso rápido.**
- **Seleccione la pestaña situada más a la izquierda (normalmente Inicio) cuando se inicia un programa.** No haga que la última pestaña seleccionada se conserve entre instancias de programa.
- **Mostrar la cinta de opciones en su estado normal (no minimizado) cuando se inicia un programa por primera vez.** A menudo, los usuarios no modifican la configuración predeterminada, por lo que minimizar la cinta al inicio del programa probablemente hará que todos los comandos sean menos eficientes. Además, Mostrar la cinta de opciones minimizada inicialmente puede ser desorientada.
- **Hacer que el estado de la cinta persista entre instancias de programa.** Por ejemplo, si un usuario minimiza la cinta de opciones, se debería mostrar minimizada la próxima vez que se ejecute el programa. Pero de nuevo, no haga que la última pestaña seleccionada se conserve de esta manera.

### <a name="using-tabs"></a>Uso de las fichas

Por lo general, es mejor tener menos pestañas, por lo que debe quitar las pestañas que no ayuden a alcanzar estos objetivos.

- **Siempre que sea práctico, use fichas estándar.** El uso de pestañas estándar mejora en gran medida la capacidad de detección, especialmente en los programas. Vea las [pestañas estándar](#standard-ribbon-tabs) de la cinta de opciones más adelante en este artículo.
- **Etiquete la primera pestaña de la Página principal, si procede.** La pestaña Inicio debe contener los comandos que se usan con más frecuencia. Si los comandos usados con frecuencia no caben en las otras pestañas, la pestaña Inicio es el lugar adecuado para ellos.
- Agregue una nueva pestaña si:
  - **Sus comandos están estrechamente relacionados con tareas específicas y se pueden describir con precisión en la etiqueta de la pestaña.** La adición de la pestaña facilita la búsqueda de sus comandos, no es más difícil.
  - **Sus comandos no están relacionados principalmente con tareas de otras pestañas.** La adición de la pestaña no debe requerir más cambios de tabulación durante las tareas que se realizan habitualmente.
  - **La pestaña tiene suficientes comandos para justificar la presencia de un lugar adicional.** No tener pestañas con solo algunos comandos. **Excepción:** Considere la posibilidad de agregar una pestaña con algunos comandos si están estrechamente relacionados con una tarea específica y la adición de la pestaña simplifica considerablemente una pestaña principal demasiado compleja.
- **En el resto de las pestañas, coloque primero las pestañas usadas con mayor frecuencia, manteniendo un orden lógico en todas las pestañas.**
- **Optimice el diseño de las pestañas para que los usuarios busquen comandos con rapidez y confianza.** Todas las demás consideraciones son secundarias.
- **No proporcione una pestaña de ayuda.** En su lugar, proporcione asistencia mediante la ayuda de todo el programa y la información sobre herramientas mejorada.
- **Use un máximo de siete pestañas principales.** Si hay más de siete, resulta difícil determinar qué pestaña tiene un comando. Aunque siete pestañas principales son aceptables para aplicaciones con muchos comandos, la mayoría de los programas deben tener cuatro o menos pestañas.

### <a name="contextual-tabs"></a>Pestañas contextuales

- **Use una pestaña contextual para mostrar una colección de comandos que solo son relevantes cuando los usuarios seleccionan un tipo de objeto determinado.** Si solo hay algunos comandos usados con frecuencia, puede ser más cómodo y estable usar una pestaña normal y simplemente deshabilitar los comandos cuando no se aplican.
- ![captura de pantalla de comandos cortar y copiar atenuada ](images/cmd-ribbons-image29.png)<br>Es mejor deshabilitar comandos comunes, como cortar y copiar, que usar una pestaña contextual.
- **Incluye solo los comandos que son específicos de un tipo de objeto determinado.** No coloque comandos solo en una pestaña contextual si los usuarios pueden necesitarlos sin seleccionar primero un objeto.
- **Incluya los comandos que se usan con frecuencia cuando se trabaja con un tipo de objeto determinado.** Coloque los comandos contextuales generales que se usan con frecuencia en menús contextuales y Minibarras de herramientas para evitar el cambio de tabulación durante las tareas que se realizan habitualmente. Como alternativa, considere la posibilidad de colocar los comandos generales de forma redundante en una pestaña contextual si, al hacerlo, se evita el cambio frecuente de tabulación. Pero no lo abusar: no intente incluir todos los comandos que un usuario podría necesitar mientras trabajaba con el objeto.
- ![captura de pantalla del comando bordes en la pestaña diseño ](images/cmd-ribbons-image30.png)<br/>En este ejemplo, el comando bordes se incluye en la pestaña diseño para evitar el cambio frecuente de pestañas durante las tareas que se realizan habitualmente.
- **Elija un color de tabulación contextual que sea diferente de las pestañas contextuales mostradas actualmente.** El mismo conjunto de pestañas puede aparecer en un momento posterior con un color diferente para lograrlo, pero se intenta utilizar las asignaciones de color coherentes entre las invocaciones siempre que sea posible.
- **Al seleccionar una pestaña contextual** se contribuye automáticamente a la detectabilidad, se mejora la percepción de estabilidad y se reduce la necesidad de cambiar de pestaña. Seleccione una pestaña contextual automáticamente cuando:
  - **El usuario inserta un objeto.** En este caso, seleccione la primera pestaña contextual del conjunto.
  - **El usuario hace doble clic en un objeto.** En este caso, seleccione la primera pestaña contextual del conjunto.
  - **El usuario seleccionó una pestaña contextual, hizo clic en el objeto y, a continuación, hizo clic inmediatamente en un objeto del mismo tipo.** En este caso, vuelva a la pestaña contextual seleccionada anteriormente.
- **Al quitar una pestaña contextual que sea la pestaña activa, haga la pestaña Inicio o la pestaña activa.** Al hacerlo, aparece la más estable.

### <a name="modal-tabs"></a>Pestañas modales

- **Use una pestaña modal para mostrar una colección de comandos que se aplican con un modo temporal determinado y no se aplica ninguna de las fichas principales.** Si se aplican algunas de las pestañas principales, utilice en su lugar una pestaña contextual y deshabilite los comandos que no se aplican. Dado que las pestañas modales están muy restringidas, solo deben usarse cuando no hay una alternativa mejor.
- ![captura de pantalla de la pestaña de vista previa de impresión ](images/cmd-ribbons-image31.png)<br/>La vista previa de impresión es una pestaña modal utilizada comúnmente.
- **Para cerrar una pestaña modal, coloque el <mode> comando cerrar como último comando en la pestaña.** Use el icono cerrar para que el comando sea fácil de encontrar. Proporcione el modo en el comando para evitar confusiones sobre lo que se está cerrando.
- ![captura de pantalla del botón Cerrar vista previa de impresión ](images/cmd-ribbons-image32.png)<br/>En este ejemplo, si se etiqueta explícitamente el comando cerrar con el modo, se quita cualquier duda sobre lo que se está cerrando.
- **Para cerrar una pestaña modal, también debe volver a definir el botón cerrar en la barra de título de la ventana para cerrar el modo en lugar del programa.** La prueba de usuario ha demostrado que muchos usuarios esperan este comportamiento.

### <a name="standard-ribbon-tabs"></a>Pestañas estándar de la cinta

Siempre que sea práctico, asigne los comandos del programa a estas pestañas estándar, según su orden estándar de apariencia.

#### <a name="regular-tabs"></a>Pestañas normales

- **Inicio.** Contiene los comandos que se usan con más frecuencia. Si se usa, siempre es la primera pestaña.
- **Introducir.** Contiene comandos para insertar contenido y objetos en un documento. Si se usa, siempre es la segunda pestaña.
- **Diseño de página.** Contiene comandos que afectan al diseño de página, incluidos los temas, la configuración de página, el fondo de página, la sangría, el espaciado y la posición. (Tenga en cuenta que los grupos de sangría y espaciado pueden estar en la pestaña Inicio, si hay suficiente espacio allí). Si se usa, siempre es la tercera pestaña.
- **Revise.** Contiene comandos para agregar comentarios, realizar un seguimiento de los cambios y comparar versiones.
- **Visores.** Contiene comandos que afectan a la vista de documento, incluidos el modo de vista, opciones de mostrar u ocultar, zoom, administración de ventanas y macros que los comandos tradicionalmente encontraban en la categoría de menú de Windows. Si se usa, es la última ficha normal, a menos que se muestre la pestaña desarrollador.
- **Desarrollador.** Contiene comandos utilizados solo por los desarrolladores. Si se usa, se oculta de forma predeterminada y la última pestaña normal cuando se muestra.

La mayoría de los programas no necesitan las pestañas revisar y desarrollador.

#### <a name="standard-contextual-tabs"></a>Pestañas contextuales estándar

- **Aplique.** Contiene comandos relacionados con el cambio del formato del tipo de objeto seleccionado. Normalmente se aplica a parte de un objeto.
- **Concepción.** Contiene comandos, a menudo en galerías, para aplicar estilos al tipo de objeto seleccionado. Normalmente se aplica a todo el objeto.
- **Diseño.** Contiene comandos para cambiar la estructura de un objeto complicado, como una tabla o un gráfico.

Si tiene comandos contextuales relacionados con el formato, el diseño y el diseño, pero no suficientes para varias pestañas, solo tiene que proporcionar una pestaña formato.

### <a name="standard-groups"></a>Grupos estándar

- **Siempre que sea práctico, use grupos estándar.** El hecho de que aparezcan comandos comunes con los mismos nombres y ubicaciones similares mejora en gran medida la capacidad de detección. Vea los [grupos](#standard-ribbon-groups) de la cinta de opciones estándar más adelante en este artículo.
- **Agregue un nuevo grupo** si:
  - **Sus comandos están estrechamente relacionados y se pueden describir con precisión mediante la etiqueta de grupo.** Agregar el grupo debe ayudar a que sus comandos resulten fáciles de encontrar, no más difíciles.
  - **Sus comandos tienen una relación más débil con los comandos de otros grupos.** Aunque todos los comandos de una pestaña deben estar estrechamente relacionados, algunas relaciones de comandos son más seguras que otras.
  - **El grupo tiene suficientes comandos para justificar la presencia de un lugar adicional.** Objetivo de los comandos 3-5 para la mayoría de los grupos. Evite tener grupos con solo los comandos 1-2, aunque es aceptable tener una galería en cinta sin ningún otro comando dentro de un grupo. Tener muchos grupos con un solo comando sugiere demasiada estructura o falta de cohesión de comandos.
- **No organice la reorganización** agregando grupos en los que no sean necesarios.
- **Considere la posibilidad de dividir un grupo** si:
  - ![captura de pantalla del grupo de comandos desorganizados ](images/cmd-ribbons-image35.png)<br/>El grupo tiene muchos comandos de diferentes tamaños y necesidades de organización.
  - ![captura de pantalla de dos nombres de grupos de párrafos largos ](images/cmd-ribbons-image33.png)<br>El grupo tiene comandos que se benefician enormemente de tener etiquetas adicionales.
- **Coloque los grupos que se usan con más frecuencia en las ubicaciones más destacadas y asegúrese de que hay un orden lógico para los grupos en la pestaña.**
- **Optimice el diseño del grupo para que los usuarios busquen comandos de forma rápida y segura.** Todas las demás consideraciones son secundarias.
- **No escale los grupos que contengan un solo botón a un icono de grupo emergente.** Al reducir verticalmente, déjelas como un solo botón.
- **Use un máximo de siete grupos.** Si hay más de siete grupos, resulta más difícil determinar qué grupo tiene un comando.

### <a name="standard-ribbon-groups"></a>Grupos de la cinta de opciones estándar

Siempre que sea práctico, asigne los comandos del programa a estos grupos estándar, que se proporcionan en sus pestañas asociadas en su orden de aparición estándar.

#### <a name="main-tab"></a>Pestaña principal

- Portapapeles
- Fuente
- Paragraph
- Edición

#### <a name="insert-tab"></a>Pestaña Insertar

- Tablas
- Ilustraciones

#### <a name="page-layout-tab"></a>Pestaña diseño de página

- Temas
- Configurar página
- Organizar

#### <a name="review-tab"></a>Ficha revisar

- Revisión
- Comentarios

#### <a name="view-tab"></a>Pestaña Vista

- Vistas de documentos
- Mostrar u ocultar
- Zoom
- Periodo

### <a name="commands"></a>Comandos

- ![captura de pantalla del comando números de línea en la cinta de opciones ](images/cmd-ribbons-image36.png)<br/>**Aproveche las ventajas de la capacidad de detección y la escalabilidad de las cintas de opciones mediante la exposición de todos los comandos de uso frecuente.** Cuando sea necesario, mueva los comandos usados con frecuencia de los cuadros de diálogo a la cinta de opciones, especialmente aquellos que se sabe que son difíciles de encontrar. Idealmente, los usuarios deberían poder realizar tareas comunes sin usar ningún cuadro de diálogo.

- **No use la escalabilidad de las cintas de opciones para justificar la adición de complejidad innecesaria.** Continúe con la no agregar comandos a una cinta de opciones solo porque puede. Mantenga la experiencia de comando global sencilla. Las siguientes son formas de simplificar la presentación:
  - ![captura de pantalla de la minibarra de herramientas y el menú contextual ](images/cmd-ribbons-image37.png)</br>**Use los menús contextuales y las Minibarras de herramientas para los comandos contextuales en contexto.**
  - **Mueva (o mantenga) comandos usados con poca frecuencia en los cuadros de diálogo.** Use los iniciadores de cuadros de diálogo para tener acceso a estos comandos. Todavía puede usar cuadros de diálogo con las cintas de opciones. Simplemente intente reducir la necesidad de usarlos durante las tareas comunes.
  - **Elimine las características redundantes y poco utilizadas.**

#### <a name="presentation"></a>Presentación

- **Presente cada comando en una sola pestaña. Evite varias rutas de acceso al mismo comando, especialmente si el comando requiere muchos clics para invocar.** Puede parecer una comodidad para encontrar un comando a través de varias rutas de acceso. Pero tenga en cuenta que cuando los usuarios encuentran lo que están buscando, dejan de buscar. A los usuarios les resulta demasiado fácil asumir que la primera ruta de acceso que encuentran es la única ruta de acceso que es un problema grave si esa ruta de acceso es ineficaz. **Excepción:** Las pestañas contextuales pueden duplicar algunos comandos desde las pestañas Inicio e insertar si, al hacerlo, se impide el cambio de pestañas para tareas contextuales comunes.
- **Dentro de un grupo, coloque los comandos en su orden lógico y, al mismo tiempo, dé preferencia a los comandos usados con más frecuencia.** En general, los comandos deben tener un flujo lógico para que sean fáciles de encontrar y, al mismo tiempo, los comandos que se usan con más frecuencia aparecen en primer lugar. Por lo general, los comandos con iconos de 32x32 píxeles aparecen antes que los comandos con iconos de 16x16 píxeles para ayudar a explorar entre grupos.
- **Evite colocar comandos destructivos junto a los comandos usados con frecuencia.** Un comando se considera destructivo si su efecto está generalizado y no se puede deshacer fácilmente, o el efecto no se percibe de inmediato.
- **Utilice separadores para indicar comandos estrechamente relacionados, como un conjunto de opciones mutuamente excluyentes.**
- ![captura de pantalla de grupos de fuentes y párrafos ](images/cmd-ribbons-image3.png)<br/> **Considere la posibilidad de usar grupos de estilo de barra de herramientas para conjuntos de comandos conocidos muy relacionados que no necesitan etiquetas.** Esto le permite presentar muchos comandos en un espacio compacto sin que ello afecte a la capacidad de detección y la facilidad de aprendizaje. Para ser tan bien conocido, estos comandos se usan con frecuencia, se reconocen al instante y, por tanto, tienden a estar en la pestaña Inicio.

- **Use los iconos de 32x32 píxeles para los comandos más usados y con la etiqueta importante.** Al escalar un grupo hacia abajo, haga que estos comandos sean los últimos para convertirlos en iconos de 16x16 píxeles.
- **Evite la colocación de comandos arbitraria.** Piense detenidamente en el diseño de la pestaña y el grupo para asegurarse de que los usuarios no pierdan tiempo inspeccionando cada pestaña para encontrar el comando que desean.
- **Evite la colocación basada en marketing.** Los objetivos de marketing en torno a la promoción de nuevas características tienden a cambiar con el tiempo. Tenga en cuenta las versiones futuras del producto y la cantidad de frustración que producirá una organización que cambia constantemente.

#### <a name="interaction"></a>Interacción

- **Deshabilitar los comandos que no se aplican al contexto actual o que producirían un error directamente.** Si es útil, use la [información sobre herramientas mejorada](glossary.md) para explicar por qué el comando está deshabilitado. No oculte estos comandos porque esto puede hacer que el diseño de la cinta de opciones cambie, lo que hace que la cinta se muestre inestable.
- **No actualice las etiquetas de comando dinámicamente.** De nuevo, esto podría hacer que el diseño de pestañas cambiara, lo que provocaría una apariencia inestable. En su lugar, diseñe comandos para que funcionen con etiquetas constantes.

    | Correcto                                                                                       | Incorrecto                                                                 |
    |-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
    | ![captura de pantalla de la nota de inserción y la nota de eliminación ](images/cmd-ribbons-image38.png)<br/> Deshabilitar comandos cuando no están disponibles | ![captura de pantalla de la nota de inserción, no eliminar Nota ](images/cmd-ribbons-image39.png)<br/>No oculte comandos, incluso cuando no estén disponibles |

- **Prefiere controles directos.** Un comando es directo si se invoca con un solo clic (es decir, sin navegar por los menús). Sin embargo, con la excepción de las galerías de la cinta de opciones, los controles directos no admiten la vista previa dinámica, por lo que la necesidad de la vista previa dinámica también es un factor.
- **Use la vista previa dinámica** para indicar el efecto de las opciones cuando un comando está entre un conjunto relacionado de opciones de formato y la vista previa dinámica es importante y práctico, especialmente si es probable que los usuarios elijan la opción incorrecta en caso contrario.
  - Si el comando se usa con frecuencia, use una galería de la cinta de opciones para la dirección.
  - Si el comando se usa con poca frecuencia, use una galería desplegable.
- **Exponga comandos directos** mediante los siguientes controles en el orden de preferencia siguiente
  - **Botones de comando, casillas, botones de radio y galerías en contexto.** Siempre son directos.
  - **Botones de expansión.** Directo para el comando más común, pero indirecto para las variaciones de comando.
  - **Botones de menú.** Estos son indirectos, pero presentan muchos comandos que son fáciles de encontrar.
  - **Cuadros de texto (con controles de número).** La entrada de texto generalmente requiere más esfuerzo que los otros tipos de control.
- ![captura de pantalla de la cinta de opciones con solo botones de menú ](images/cmd-ribbons-image42.png)</br>Si la cinta de opciones se compone principalmente de botones de menú cuando se muestra en tamaño completo, también puede usar una barra de menús.
- **Prefiere comandos inmediatos.** ![captura de pantalla del botón de impresión dividida y su submenú ](images/cmd-ribbons-image43.png)<br/>Un comando es inmediato si surte efecto inmediatamente (es decir, sin cuadros de diálogo para recopilar datos adicionales). Si un comando puede requerir una entrada, considere la posibilidad de usar un botón de expansión, con el comando inmediato en la parte del botón, y los comandos que requieren la entrada en el submenú.

### <a name="galleries"></a>Galerías

**Use una [Galería](glossary.md)** si:

- **Hay un conjunto de opciones bien definido y relacionado entre las que suelen elegir los usuarios.** Puede haber un número ilimitado de variaciones, pero las selecciones probables deberían estar contenidas correctamente. Si las opciones no están estrechamente relacionadas, considere la posibilidad de usar galerías independientes.
- **Las opciones se expresan mejor visualmente, como las características de formato.** El uso de miniaturas facilita la exploración, la comprensión y la elección de las opciones. Aunque se pueden etiquetar las opciones, la selección se hace visualmente y las etiquetas de texto no deben ser necesarias para comprender las opciones.
- **Las opciones muestran el resultado que se consigue de inmediato con un solo clic.** No debe haber ningún cuadro de diálogo de seguimiento para aclarar mejor la intención del usuario o un conjunto de pasos para lograr el resultado indicado. Si es posible que los usuarios deseen ajustar la opción, hágalo después.

**Use una galería de la cinta de** opciones si:

- **Las opciones se usan con frecuencia.** Las opciones necesitan el espacio y vale la pena tomar el espacio de otros comandos.
- **Para un uso típico, no es necesario agrupar ni filtrar las opciones presentadas.**
- **Las opciones se pueden mostrar eficazmente dentro del alto de una cinta (que es de 48 píxeles).**

#### <a name="thumbnails-in-galleries"></a>Miniaturas en galerías

**Elija el tamaño de miniatura de la Galería estándar más pequeño** que realiza el trabajo.

- En el caso de las galerías en cinta, use miniaturas de 16x16, 48x48 o 64x48 píxeles.
- En el caso de las galerías desplegables, utilice miniaturas de 16x16, 32x32, 48x48, 64x48, 72x96, 96x72, 96x96 o 128x128 píxeles.
- Todos los elementos de la Galería deben tener el mismo tamaño de miniatura.

Para las galerías de la cinta de opciones:

- **Muestra un mínimo de tres opciones; más si hay espacio.** Si no hay suficiente espacio para mostrar al menos tres opciones en el tamaño de ventana típico, use una galería desplegable en su lugar.
- **Expanda galerías de la cinta de opciones para aprovechar el espacio disponible.** Use el espacio adicional para mostrar más elementos y facilitar su elección con un solo clic.

En el caso de las galerías desplegables:

- **Muestre la galería de un cuadro combinado, una lista desplegable, un botón de expansión o un botón de menú.**
- **Si el usuario hace clic en la ventana principal para descartar la Galería desplegable, solo tiene que descartar la Galería sin seleccionar ni modificar el contenido de la ventana principal.**
- **Si una galería tiene muchas opciones y algunas opciones se usan con poca frecuencia, simplifique la Galería predeterminada centrándose en las opciones de uso más frecuente.** En el caso de los comandos restantes, proporcione un comando adecuado en la parte inferior de la lista desplegable de la galería.
  - Si el comando muestra una lista de más variaciones, asígnele el nombre "más `singular feature name` Opciones..."
  - Si el comando muestra un cuadro de diálogo que permite a los usuarios crear sus propias opciones personalizadas, asígnele el nombre "Custom `feature name` ..."
- **Organice las opciones en grupos, si esto hace que la exploración sea más eficaz.**
- ![captura de pantalla de la galería de símbolos y los filtros ](images/cmd-ribbons-image44.png)<br/>**Si una galería tiene muchos elementos, considere la posibilidad de agregar un filtro para ayudar a los usuarios a buscar opciones de forma más eficaz.** Para evitar confusiones, muestre inicialmente la Galería sin filtrar. Sin embargo, la mayoría de las galerías no deben requerir un filtro porque no deberían tener tantas opciones y el uso de grupos debe ser suficiente.

### <a name="command-previews"></a>Vistas previas de comandos

- **Use las vistas previas para mostrar el efecto de un comando sin que los usuarios tengan que realizarlo primero.** Mediante el uso de vistas previas útiles, puede mejorar la eficacia y la facilidad de aprendizaje de su programa, y reducir la necesidad de pruebas y errores. Para los diferentes tipos de vistas previas de comandos, consulte [vistas previas](#previews) en la sección conceptos de diseño de este artículo.
- **En el caso de las vistas previas en vivo, asegúrese de que se puede aplicar la vista previa y de que el estado actual se restaure en 500 milisegundos.** Esto requiere la capacidad de aplicar los cambios de formato rápidamente y de una manera que sea interrumpible. Los usuarios deben ser capaces de evaluar diferentes opciones con rapidez para que las vistas previas en vivo tengan todas las ventajas.
- **Evite el uso de texto en las vistas previas.** De lo contrario, las imágenes de vista previa deberán estar localizadas.

### <a name="icons"></a>Iconos

- ![captura de pantalla de la lista desplegable y casillas ](images/cmd-ribbons-image45.png)<br/>**Proporcionar iconos para todos los controles de la cinta de opciones excepto las listas desplegables, las casillas y los botones de radio.** La mayoría de los comandos requerirán iconos de píxel de 32x32 y 16x16 (la barra de herramientas de acceso rápido usa solo los iconos de 16x16 píxeles). Las galerías suelen usar iconos de píxel 16x16, 48x48 o 64x48.
- **Proporcione iconos únicos.** No use el mismo icono para los distintos comandos.
- **Asegúrese de que los iconos de la cinta de opciones estén claramente visibles en el color de fondo de la cinta.** Evalúe siempre los iconos de la cinta de opciones en contexto y en modo de alto contraste.
- **Elija diseños de icono que comuniquen claramente su efecto,** especialmente para los comandos que se usan con más frecuencia. Las cintas de opciones bien diseñadas tienen iconos autoexplicativos para ayudar a los usuarios a encontrar y comprender los comandos de forma eficaz.
- **Elija los iconos que sean reconocibles y distinguibles,** especialmente para los comandos que se usan con más frecuencia. Asegúrese de que los iconos tienen formas y colores distintivos. Esto ayuda a los usuarios a encontrar los comandos rápidamente, incluso si no recuerdan el símbolo del icono.

    | Correcto                                                                                                 | Incorrecto                                                                               |
    |--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
    | ![captura de pantalla de un cuentagotas azul y un lápiz amarillo ](images/cmd-ribbons-image46.png)<br/>Use la forma y el color para crear iconos que resulten fáciles de distinguir. | ![captura de pantalla de un cuentagotas azul y un lápiz azul ](images/cmd-ribbons-image47.png)<br/> Los iconos que tienen el mismo color son difíciles de distinguir|

- ![captura de pantalla de un comando de comentarios en el contenedor emergente ](images/cmd-ribbons-image48.png)<br/>**Considere la posibilidad de crear iconos de grupo emergente colocando el icono de 16x16 píxeles del comando más destacado en el grupo dentro de un contenedor visual de 32x32 píxeles.** No tiene que crear iconos diferentes para los grupos emergentes.
- ![captura de pantalla de los botones de comando de formato de texto ](images/cmd-ribbons-image25.png)<br/>**Si es útil, cambie el icono para que refleje el estado actual.** Hacerlo es especialmente útil para los botones de expansión cuyo efecto predeterminado puede cambiar.
- **Asegúrese de que los iconos de la cinta de opciones cumplen las directrices del icono de estilo Aero.** Sin embargo, los iconos de la cinta de opciones se muestran directamente en lugar de mostrarse en perspectiva.

| Correcto                                                                                                 | Incorrecto                                                                               |
    |--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
    | ![captura de pantalla de iconos de comandos bidimensionales ](images/cmd-ribbons-image49.png)<br/> Usar iconos bidimensionales.|![captura de pantalla de iconos de comandos tridimensionales ](images/cmd-ribbons-image50.png)<br/> No utilice iconos tridimensionales. |
 
### <a name="enhanced-tooltips"></a>Información sobre herramientas mejorada

- **Todos los comandos de la cinta deben tener información sobre herramientas mejorada** para proporcionar el nombre del comando, la tecla de método abreviado, la descripción y la información complementaria opcional. Evite la información sobre herramientas que simplemente represente la etiqueta.

    **Incorrecto:**

    ![captura de pantalla de la información sobre herramientas que repite el nombre de comando ](images/cmd-ribbons-image51.png)

    En este ejemplo, la información sobre herramientas simplemente retiene el estado de la etiqueta del comando.

- **Cuando sea práctico, describa por completo el comando mediante una descripción concisa.** Vínculo a la ayuda solo si es realmente necesario una explicación adicional.

    **Incorrecto:**

    ![captura de pantalla de la información sobre herramientas para el comando StrikeThrough ](images/cmd-ribbons-image52.png)

    En este ejemplo, el comando no necesita ayuda.

- **Cuando sea útil, ilustre el efecto del comando mediante una vista previa.**

    ![captura de pantalla de la información sobre herramientas y el gráfico para insertar gráfico ](images/cmd-ribbons-image53.png)

    En este ejemplo, la imagen de información sobre herramientas muestra el efecto del comando.

Para instrucciones de etiquetado, consulte [etiquetas de información sobre herramientas mejoradas](#enhanced-tooltips).

### <a name="access-keys-and-keytips"></a>Teclas de acceso y keytips

Las Keytips son el mecanismo que se usa para mostrar las teclas de acceso de los comandos mostrados directamente en una cinta de opciones.

Las teclas de acceso de los comandos de menú desplegable se indican con un carácter subrayado. Se diferencian de las claves de acceso de menú de las siguientes maneras:

- Se pueden usar dos claves de acceso a caracteres. Por ejemplo, se puede usar FP para tener acceso al comando format pintor.
- Las asignaciones de teclas de acceso se muestran con sugerencias en lugar de subrayados, por lo que el ancho de caracteres y los descendentes no son un factor para la creación de asignaciones.

- **Asignar teclas de acceso a todas las pestañas y comandos de la cinta de opciones.** La única excepción posible es para los comandos que proceden de complementos heredados.
- **Para el botón de aplicación y la barra de herramientas de acceso rápido:**
  - Asigne F al botón aplicación. Esta asignación se utiliza debido a la similitud del botón de la aplicación con el menú Archivo tradicional.
  - ![captura de pantalla del comando keytips en una cinta de opciones ](images/cmd-ribbons-image54.png)<br/>Para la barra de herramientas de acceso rápido y las listas de archivos usados recientemente, asigne claves de acceso numéricamente.
- ![captura de pantalla que muestra keytips para pestañas ](images/cmd-ribbons-image55.png)<br/>**Para las pestañas:**
  - Asigne H a Inicio.
  - A partir de las pestañas usadas con más frecuencia, asigne la primera letra de la etiqueta.
  - En el caso de las pestañas que no se puedan asignar a la primera letra, elija una consonante distintiva o una vocal en la etiqueta.
  - En el caso de los programas que se usan para admitir barras de menús, se esfuerza por mantener la compatibilidad con las claves de acceso en el mejor grado práctico. Evite asignar distintos significados a las claves de acceso de las categorías de menú heredadas. Por ejemplo, si la versión heredada de la barra de menús de un programa tenía un menú Edición, procure usar una tecla de acceso E a la pestaña equivalente. Si no hay ninguna pestaña equivalente, no asigne una tecla de acceso E a ninguna pestaña para evitar confusiones.
- ![captura de pantalla que muestra keytips para una cinta de opciones ](images/cmd-ribbons-image56.png)<br/>**Para comandos de la cinta de opciones, menús y submenús:**
  - Asignar combinaciones de teclas de acceso únicas en una pestaña. Puede volver a usar las combinaciones de teclas de acceso en diferentes pestañas.
  - Siempre que sea posible, asigne las teclas de acceso estándar para los comandos de uso frecuente. Vea la [tabla de claves de acceso estándar](inter-keyboard.md).
  - Para otros comandos:
    - En el caso de los comandos usados con más frecuencia, elija letras al principio de la primera o la segunda palabra de la etiqueta, preferiblemente la primera letra.
    - En el caso de los comandos usados con menos frecuencia, elija las letras que son una consonante distintiva o una vocal en la etiqueta, como "x" en "salir".
    - En el caso de los comandos y los iniciadores de cuadros de diálogo usados con menos frecuencia, use dos letras según sea necesario.
    - En el caso de los menús y los submenús, utilice una sola letra para reducir el número de pulsaciones de teclas necesarias para el comando completo.
    - No use claves de acceso a partir de J, Y o Z porque se utilizan para pestañas contextuales, keytips sin asignar y grupos emergentes.
- ![captura de pantalla de keytips para grupos emergentes ](images/cmd-ribbons-image58.png)<br/>**Para los grupos emergentes:**
  - Use una clave de acceso de dos letras que empiece por Z.
  - A partir de los grupos usados con mayor frecuencia, asigne la segunda letra clave de acceso a la primera letra de la etiqueta.
  - En el caso de los grupos restantes, elija una consonante distintiva o una vocal en la etiqueta.

Para obtener instrucciones sobre las teclas de método abreviado, consulte [teclado](inter-keyboard.md).

### <a name="application-buttons"></a>Botones de la aplicación

- **Use un botón aplicación para mostrar un menú de comandos que impliquen realizar algo en o con un archivo.** Entre los ejemplos se incluyen comandos que tradicionalmente se encuentran en el menú Archivo para crear, abrir y guardar archivos, imprimir y enviar y publicar documentos.
- **Proporcione siempre un botón de aplicación al usar una cinta de opciones.** Si el programa no utiliza archivos, use el botón aplicación para tener acceso a las opciones del programa y al comando salir. Los botones de la aplicación siempre muestran un menú de comandos; nunca son simplemente decorativos.
- **Use los siguientes comandos de menú estándar de la aplicación cuando corresponda:**
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
  
- **Reserve comandos que pertenezcan solo al menú aplicación para ese menú.** No los Coloque de forma redundante en ninguna de las pestañas.
- Para cada elemento de menú, proporcione:
  - **Una etiqueta con el nombre de comando.**
  - **Icono de 32x32 píxeles.**
  - **Breve descripción.** Asegúrese de que la descripción se puede mostrar usando como máximo dos líneas de texto.
- ![captura de pantalla de la tecla de método abreviado de documentación de ToolTip ](images/cmd-ribbons-image59.png)<br/>**Use la información sobre herramientas para documentar las teclas de método abreviado.** A diferencia de los menús normales, los menús de la aplicación no documentan las teclas de método abreviado mediante etiquetas.

### <a name="quick-access-toolbars"></a>Barras de herramientas de acceso rápido

- **Use la barra de herramientas de acceso rápido para proporcionar acceso a los comandos usados con frecuencia.** Los comandos pueden estar en el botón aplicación o en la cinta de opciones.
- **Proporcione siempre una barra de herramientas de acceso rápido al usar una cinta de opciones.** Hágalo incluso si la cinta de opciones tiene una sola pestaña; Esto proporciona coherencia entre programas.
- **Rellene previamente la barra de herramientas de acceso rápido con los comandos usados con frecuencia en el menú de la aplicación.** Proporcione guardar y deshacer si el programa los admite y abra e imprima si es compatible y se usa con frecuencia.
- **En el menú personalizar barra de herramientas de acceso rápido, proporcione hasta 12 de los comandos inmediatos que se usan con más frecuencia.** Los comandos inmediatos no requieren ninguna entrada adicional para que surtan efecto y, por tanto, son adecuados para la barra de herramientas de acceso rápido. Aunque pueden ser comandos inmediatos, prefieren los comandos que no están en la pestaña Inicio, ya que es más probable que los usuarios los elijan.
- **En el menú personalizar barra de herramientas de acceso rápido, si hay un par de comandos relacionados, proporcione ambos, independientemente de la frecuencia.** Los pares comunes son abrir/cerrar, atrás/adelante y deshacer/rehacer.
- **En el cuadro de diálogo Personalizar barra de herramientas de acceso rápido, proporcione una manera de agregar cualquier comando.** Proporcione un filtro de comandos conocido que muestre los comandos usados con más frecuencia y seleccione este filtro de forma predeterminada.

### <a name="dialog-box-launchers"></a>Iniciadores de cuadros de diálogo

- ![captura de pantalla del cuadro de diálogo fuente y el grupo de fuentes ](images/cmd-ribbons-image60.png)<br/>**Proporcione un grupo con un selector de cuadro de diálogo si hay un cuadro de diálogo relacionado con comandos y valores de uso poco frecuente.** El cuadro de diálogo debe contener todos los comandos del grupo, además de otros no un conjunto de comandos completamente diferente o los mismos comandos que el grupo.
- **No use un selector de cuadro de diálogo para realizar comandos directamente.** Un selector de cuadro de diálogo debe mostrar un cuadro de diálogo.
- **No use un selector de cuadro de diálogo para tener acceso a los comandos y valores de configuración usados con frecuencia.** En comparación con los comandos directamente en la cinta de opciones, la configuración y los comandos del cuadro de diálogo son relativamente indetectables.
- **Haga coincidir el nombre del cuadro de diálogo con el nombre del grupo.** No tiene que ser una coincidencia exacta, pero los nombres deben ser lo suficientemente similares como para que los usuarios no sorprendan los resultados.

    **Incorrecto:**

    ![captura de pantalla del cuadro de diálogo sonido de aviso ](images/cmd-ribbons-image61.png)

    Aunque un sonido de recordatorio es una opción de recordatorio, no se espera usar el selector de cuadro de diálogo para establecer el sonido del aviso.

- **Mostrar solo los comandos y la configuración que se relacionan con el grupo.** Si el cuadro de diálogo muestra otras cosas, los usuarios pueden concluir que esta ruta de acceso a estos otros comandos y configuraciones es la única ruta de acceso.

    **Incorrecto:**

    ![captura de pantalla del cuadro de diálogo fuente ](images/cmd-ribbons-image62.png)

    En este ejemplo, el cuadro de diálogo fuente muestra la configuración de espaciado de caracteres, que no está relacionada con la ficha asociada.

## <a name="labels&quot;></a>Etiquetas

### <a name=&quot;tab-labels&quot;></a>Etiquetas de pestaña

- **Etiquete todas las pestañas.**
- Siempre que sea práctico, **use las pestañas estándar de la cinta de** opciones.
- **Prefiere etiquetas de palabra sencillas y concisas.** Aunque las etiquetas de varias palabras son aceptables, ocupan más espacio y son más difíciles de localizar.
- **Elija nombres de pestaña significativos que describan claramente y con precisión su contenido.** Los nombres deben ser específicos, pero no demasiado específicos. Los nombres de las pestañas deben ser suficientemente predecibles para que los usuarios no sorprendan por su contenido. Tenga en cuenta que la pestaña Inicio se denomina genéricamente porque se usa para los comandos que se usan con más frecuencia.
- **No** utilice nombres de grupo como &quot;Basic&quot; y &quot;Advanced&quot;. Requieren que los usuarios determinen si el comando que buscan es básico o avanzado.
- **Elija nombres de pestaña que reflejen su propósito.** Tenga en cuenta los objetivos o las tareas asociadas a la pestaña.
- **Elija nombres de pestaña que sean claramente distintos de los demás nombres de pestaña.**
- **Use sustantivos o verbos para las pestañas.** Los nombres de las pestañas no requieren frases paralelas, por lo que debe elegir la mejor etiqueta independientemente de si se trata de un nombre o un verbo.
- **No use los gerundios** (nombres que terminan en &quot;-Ing"). Use el verbo del que se deriva gerundio en su lugar. (por ejemplo, use "Draw" en lugar de "Drawing").
- **Evite los nombres de pestaña con las mismas letras iniciales, especialmente las pestañas adyacentes.** Cuando la cinta se reduce verticalmente, estos nombres de pestaña tendrán el mismo texto truncado.
- **Prefiere nombres singulares.** Sin embargo, puede usar un nombre Pural si el nombre singular es extraño.
- **Usar mayúsculas y minúsculas de estilo de título.**
- **No uses puntuación final.**

### <a name="contextual-tab-and-tab-set-labels"></a>Etiquetas de pestaña contextual y conjunto de pestañas

- **Finalizar las etiquetas del conjunto de pestañas contextuales con "herramientas".** Esto ayuda a identificar el propósito de las pestañas contextuales.
- Usar mayúsculas y minúsculas de estilo de título.
- No uses puntuación final.

### <a name="group-labels"></a>Etiquetas de grupo

- **Etiquete todos los grupos** a menos que el grupo tenga un solo comando y las etiquetas de grupo y de comando sean las mismas.

- **Usar la cinta de opciones estándar groupsWhenever práctico.**
- **Prefiere etiquetas de palabra sencillas y concisas.** Aunque las etiquetas de varias palabras son aceptables, ocupan más espacio y son más difíciles de localizar.
- **Elija nombres de grupo significativos que describan claramente y con precisión su contenido.** Los nombres deben ser específicos, no genéricos.
- **Elija los nombres de grupo que reflejen su propósito.** Tenga en cuenta los objetivos o las tareas asociados a los comandos del grupo.
- **Evite el uso de los gerundios** (nombres que terminan en "-Ing"). Puede usar los gerundios, sin embargo, si el uso del verbo desde el que se deriva gerundio es confuso. Por ejemplo, use "edición" y "prueba" en lugar de "Editar" y "prueba".
- **No utilice nombres de grupo que coincidan con los nombres de las pestañas.** El uso del nombre de la pestaña en la que está el grupo no proporciona información y el uso del nombre de una pestaña diferente es confuso.
- **Prefiere nombres singulares.** Sin embargo, puede usar un nombre Pural si el nombre singular es extraño. 
- **Use mayúsculas de estilo de frase.**
- **No uses puntuación final.**

### <a name="command-labels"></a>Etiquetas de comando

- **Etiquete todos los comandos.** Tener etiquetas de texto explícitas ayuda a los usuarios a encontrar y entender los comandos. **Excepción:** Se puede quitar la etiqueta de un comando si su icono es extremadamente conocido y el espacio es Premium. Lo más probable es que los comandos sin etiqueta estén en la pestaña Inicio. En este caso, asigne su propiedad Name a una etiqueta de texto adecuada. Esto permite a los productos de tecnología de asistencia, como lectores de pantalla, proporcionar a los usuarios información alternativa sobre el gráfico.
- **En el caso de los botones de comando, utilice una etiqueta concisa y autoexplicativa.** Use una sola palabra si es posible; cuatro palabras como máximo.
- **En el caso de las listas desplegables, si la lista siempre tiene un valor, use el valor actual como etiqueta.**
- ![captura de pantalla de la solicitud de búsqueda de libretas de direcciones ](images/cmd-ribbons-image67.png)<br/>Si una [lista desplegable editable](/windows/desktop/uxguide/ctrl-drop) no tiene un valor, use un [símbolo del sistema](glossary.md).
- **Las listas desplegables que no se explican por sí solas o que se usan con poca frecuencia necesitan una etiqueta explícita.** Coloque un signo de dos puntos al final de la etiqueta.
- ![captura de pantalla de de forma automática después de: \[ segundos \] ](images/cmd-ribbons-image69.png)<br. >**para cuadros de texto, use una etiqueta explícita.** Coloque un signo de dos puntos al final de la etiqueta.
- **Use mayúsculas de estilo de frase.** Hacerlo es más adecuado para el [tono](text-style-tone.md)de Windows.
- **Inicie la etiqueta con un verbo imperativo.** a menos que sea el mismo que el nombre de la pestaña o del grupo o un verbo común como mostrar, crear, insertar o dar formato.
- **No uses puntuación final.**
- **Para ahorrar espacio, no coloque puntos suspensivos en las etiquetas de comandos de la cinta de opciones.** Sin embargo, los comandos del botón de aplicación y los menús desplegables usan los puntos suspensivos.

### <a name="enhanced-tooltip-labels"></a>Etiquetas de información sobre herramientas mejorada

- **Use el título para asignar el nombre de comando y su tecla de método abreviado, si procede.**
- **Para el título, no use la puntuación final.**
- **Inicie la descripción con un verbo.** Use la descripción para ayudar a los usuarios a determinar si una característica específica es la que está buscando. La descripción debe escribirse como frase para completar la frase "esta es la característica correcta que se usará si se desea...".
- **Mantenga la descripción en breve.** Ir directamente al punto. El texto largo desaconseja la lectura.
-   ![captura de pantalla del botón pegar división y dos informaciones sobre herramientas ](images/cmd-ribbons-image70.png)<br/>**En el caso de los botones de expansión, use una información sobre herramientas diferente para explicar el menú del botón de expansión.**
- **Use una descripción complementaria opcional para explicar cómo usar el control.** Este texto puede incluir información sobre el estado del control (incluido por qué está deshabilitado) si el propio control no indica el estado. Mantenga este texto corto y use un tema de ayuda para obtener explicaciones más detalladas.
- ![captura de pantalla de la información sobre herramientas con gráficos y texto ](images/cmd-ribbons-image71.png)**para la descripción y la descripción complementaria, use oraciones completas con una puntuación final.**
- Use mayúsculas de estilo de frase.

### <a name="application-button-labels"></a>Etiquetas de botón de aplicación

- [captura de pantalla de la opción de impresión rápida seleccionada ](images/cmd-ribbons-image72.png)<br/>**Use "rápida" para indicar una versión inmediata de un comando.**

- **Use un botón de puntos suspensivos para indicar que un comando requiere más información.**
- **Use mayúsculas de estilo de frase.**

## <a name="documentation"></a>Documentación

Al hacer referencia a las cintas:

- Consulte la cinta de opciones y sus componentes como cinta, pestañas, grupos y controles. Estos términos no se escriben en mayúsculas.
- Haga referencia al botón de redondeo como el botón aplicación y el menú que contiene como menú de la aplicación.
- Haga referencia a la barra de herramientas como la barra de herramientas de acceso rápido.
- Haga referencia a las pestañas por sus etiquetas y la pestaña palabra. Use el texto de etiqueta exacto, incluido el uso de mayúsculas.
- Haga referencia a los comandos por sus etiquetas. Consulte los nombres de la información sobre herramientas para los comandos sin etiqueta. Use el texto de etiqueta exacto, incluido el uso de mayúsculas, pero no incluya los puntos suspensivos. No incluya el botón o el comando de palabra.
- Para describir la interacción del usuario, use haga clic en para las pestañas y los controles. Use entrar para listas desplegables editables. No use elegir, seleccionar o seleccionar.
- Haga referencia a los elementos no disponibles como no disponible, no como atenuado, deshabilitado o atenuado. En la documentación de programación, use Disabled.
- Siempre que sea posible, dé formato a las etiquetas usando texto en negrita. De lo contrario, coloque las etiquetas entre comillas solo si es necesario para evitar confusiones.

Ejemplos:

- En la pestaña **Inicio** , haga clic en **Pegar especial**.
- En la pestaña **Inicio** , en el cuadro **fuente** , escriba "Segoe UI".
- En la pestaña **revisar** , haga clic en **Mostrar marcado** y, a continuación, haga clic en **revisores**.
- En la pestaña **formato** , en **herramientas de imagen**, haga clic en **comprimir imágenes**.