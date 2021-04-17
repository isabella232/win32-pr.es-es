---
title: 'Herramientas de accesibilidad: AccScope'
description: La herramienta AccScope permite a los desarrolladores y evaluadores evaluar la accesibilidad de su aplicación durante el desarrollo y el diseño de la aplicación, en lugar de en las fases de prueba en tiempo de ejecución del ciclo de desarrollo de una aplicación.
ms.assetid: 7C4D78CD-CDDA-8369-B747-6224C152A997
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d057e818a0fe01ef6f219f1a03d82190d21ac14
ms.sourcegitcommit: 305298a7727a428310fa138b45a933bcd7ef2532
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/25/2020
ms.locfileid: "104567282"
---
# <a name="accessibility-tools---accscope"></a>Herramientas de accesibilidad: AccScope

La herramienta **AccScope** permite a los desarrolladores y evaluadores evaluar la accesibilidad de su aplicación durante el desarrollo y el diseño de la aplicación, en lugar de en las fases de prueba en tiempo de ejecución del ciclo de desarrollo de una aplicación. Las pruebas pueden comenzar incluso en las frases prototipo tempranas. **AccScope** puede visualizar cómo un lector de pantalla expone la información de automatización de la interfaz de usuario que proporciona una aplicación, y puede mostrar áreas en las que desee agregar información o soporte técnico a la aplicación para mejorar su accesibilidad.

> [!NOTE]
> **AccScope** es una herramienta heredada. En su lugar, se recomienda usar [información de accesibilidad](https://accessibilityinsights.io/) .

## <a name="about-accscope"></a>Acerca de AccScope

**AccScope** se instala con el kit de desarrollo de software (SDK) de Windows. Se encuentra en la \\ carpeta bin \\ < *version* > \\ < *Platform* > \\ AccScope de la ruta de instalación del SDK. Ejecute el programa AccScope.exe.

**AccScope** es una aplicación de escritorio, no una aplicación de la tienda Windows. Puede usarlo para examinar cualquier aplicación que aparezca como una ventana, incluida una aplicación de escritorio o una aplicación de la tienda Windows.

Es posible que tenga que ejecutar **AccScope** como administrador la primera vez que lo use para habilitar el modo de narrador.

**AccScope** está disponible como parte de los binarios de herramientas de accesibilidad en el Windows SDK. No se distribuye como una descarga independiente de exe y no existe en los SDK anteriores.

## <a name="file-menu-options"></a>Opciones del menú Archivo

- Seleccione **Actualizar** para actualizar toda la información en **AccScope** para que coincida con el estado actual de la ventana de destino. Para una interfaz de usuario que contiene un gran número de elementos, esto puede tardar varios segundos en completarse.
- Active o desactive **siempre visible** para cambiar el comportamiento de la ventana de la interfaz de usuario de **AccScope** . El valor predeterminado es **siempre visible** .
- Seleccione **salir** para salir de **AccScope**.

## <a name="view-options"></a>Ver las opciones

- Seleccione **pantalla completa** para ejecutar la herramienta **AccScope** en una vista de pantalla completa (a continuación, use el tabulador para ver la ventana de destino). Si tanto **AccScope** como la aplicación de destino se ejecutan en pantalla completa, la selección de ubicación, los rectángulos delimitadores y la visualización general de los elementos se corresponden entre la aplicación y la vista **AccScope** .
    > [!Note]  
    > **AccScope** y su destino deben ejecutarse en la misma pantalla.

     

- Seleccione **enfoque automático** para permitir que AccScope cambie la ventana de destino cada vez que un usuario mueva el foco a la ventana (mediante el mouse o el teclado).
- Seleccione **actualización automática** para habilitar el modo **AccScope** que actualiza todos los datos de accesibilidad de la ventana de destino cada 5 segundos. Esto resulta útil si los datos de la ventana de destino de Microsoft UI Automation cambian constantemente.
- Seleccione **regiones en directo** para resaltar las regiones activas que emiten notificaciones en la ventana de destino. Una activación de eventos de región activa muestra un elemento emergente rojo con información sobre la región activa, incluido su nombre y su valor "Aria-activo" (o el valor de ARIA equivalente análogo para aplicaciones que no usan HTML directamente, sino que usan el concepto de regiones activas en la compatibilidad de UI Automation).

## <a name="element-mode"></a>Modo de elemento

Puede optar por ver una ventana de destino a través de uno de estos modos:

- **Control hoja**: muestra una vista de automatización de la interfaz de usuario de los elementos de **control** con relaciones de elementos primarios y secundarios, es decir, una vista de los controles interactivos de nivel hoja. Use esta opción para ver si todos los controles interactivos aparecen correctamente en el árbol de automatización de la interfaz de usuario para una vista de **control** .
- **Patrón de texto**: muestra los intervalos de texto visibles de los contenedores **Textpattern** desde la ventana de destino. Use esta opción para representar visualmente los intervalos de texto visibles de los elementos **Textpattern** de UI Automation.
- **Narrador**: muestra los elementos de automatización de la interfaz de usuario que narrador puede identificar mediante la metáfora ' navegación de elementos ' del narrador.
- **Filtro personalizado**: muestra un árbol de controles filtrados con una selección de subconjuntos de controles: **botón**, **casilla**, **cuadro combinado**, **cuadrícula**, **hipervínculo**, **lista**, **menú** o **tabla**.

Al cambiar la configuración de **modo de elemento** , se desencadena una actualización de la visualización. Para una interfaz de usuario que contiene un gran número de elementos, esto puede tardar varios segundos en completarse.

## <a name="layout-options"></a>Opciones de diseño

Puede seleccionar **Visual** o **List** como modo de visualización para el diseño **AccScope** . **Visual** coloca los elementos en el espacio de coordenadas en la misma relación que la ventana de destino. **List** ordena los elementos de una lista descendente que se alinea a la izquierda en la ventana de **AccScope** y el orden de la lista es equivalente al orden de tabulación o de lectura.

- Seleccione una opción de **Mostrar imágenes** para controlar cuándo se reemplazan los rectángulos simples para los elementos de imagen por la imagen real (o una pequeña ventanilla de la imagen, ya que a menudo los rectángulos son más pequeños que la imagen real). El valor predeterminado es al **mantener** el mouse, que muestra la imagen al navegar dentro de **AccScope** y mantener el mouse sobre el rectángulo para un elemento de imagen. Las opciones alternativas son **siempre** o **nunca**.
- Seleccione **Mostrar información sobre herramientas** para mostrar información básica del elemento siempre que mantenga el mouse sobre un elemento en la visualización **AccScope** . Si el **modo del elemento** es un **control hoja** o un **patrón de texto** , la información que se muestra en la información sobre herramientas es la propiedad de automatización de la interfaz de usuario de nivel de elemento de prioridad máxima. Si el **modo del elemento** es **narrador** , la información incluye el texto que el narrador leerá para el elemento.
- Seleccione **Mostrar números** para mostrar los números de secuencia que indican el orden de representación del control en el diseño. El esquema de números se basa en la configuración del **modo de elemento** :
    - **Control hoja**: los números indican el orden en que los controles hoja aparecen en el árbol de automatización de la interfaz de usuario.
    - **Patrón de texto**: los números indican el orden en el que aparecen los intervalos de texto en un intervalo de documento.
    - **Narrador**: el número indica el orden en el que se navegan los elementos en la navegación de elementos del narrador.

## <a name="choosing-a-window"></a>Elección de una ventana

En la **ventana** etiqueta encontrará una lista desplegable que muestra todas las ventanas de HWND que están activas actualmente en el sistema. El texto de cada ventana que aparece en la lista desplegable es el título de la ventana y también un identificador de ventana hexadecimal entre corchetes. Elija una de ellas para cambiar la ventana de destino en la que se notifica **AccScope** . Puede volver a elegir el mismo elemento para obtener el mismo comportamiento que una **actualización** explícita.

## <a name="using-the-accscope-visualization"></a>Uso de la visualización AccScope

La imagen siguiente es una captura de pantalla de la visualización de **AccScope** . En esta captura de pantalla se muestra la herramienta **AccScope** que ve la ventana de nivel superior de la salida de [ejemplo de accesibilidad XAML](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/XAML%20accessibility%20sample) , que se ejecuta como una aplicación en el mismo equipo. Esta captura de pantalla muestra el modo de elemento predeterminado de **control de hoja** y el valor **Visual** para el **diseño**.

![Captura de pantalla de la visualización de AccScope](images/accscopescreenshot.png)

Observe cómo esta visualización representa los controles en el espacio de coordenadas aproximado que vería en la aplicación. Pero en lugar de mostrarle los objetos visuales XAML, o el texto completo de los controles de texto, muestra los valores de propiedad de **nombre** que proceden de todos los elementos de control, mediante la automatización de la interfaz de usuario.

Además de las opciones de menú descritas anteriormente, también puede usar estas técnicas:

- Haga clic en el rectángulo de cualquier elemento en visualizaciones **visuales** o de **lista** para mostrar un menú emergente de **propiedades de UIA** . Esto muestra una serie de las propiedades importantes de automatización de la interfaz de usuario para ese elemento, incluidas algunas de las propiedades estándar de [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) y otra información, como los valores de Aria y una **Descripción del proveedor**.
- Haga clic con el botón derecho en el rectángulo de cualquier elemento en visualizaciones **visuales** o de **lista** para mostrar un menú contextual para ejercitar los patrones admitidos por el elemento. Por ejemplo, si un elemento admite [**InvokePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationinvokepattern), el menú contextual incluye un elemento para la **invocación**. Seleccione el elemento y se ejercita la API de patrón adecuada en la aplicación correspondiente. **AccScope** admite esta característica para los siguientes patrones: **Invoke**, **ExpandCollapse**, **Toggle**, **SelectionItem**, **ScrollItem**.
- Ajuste el control deslizante **transparencia** para cambiar la opacidad y transparencia de la ventana **AccScope** . De forma predeterminada, se muestra como una opacidad del 100%. Hacer que la ventana sea totalmente transparente puede ser útil para ver las partes de la ventana de destino a través de la interfaz de usuario de **AccScope** mientras usa el modo **superior Always on** .
- Si se muestran, use las barras de desplazamiento horizontal y vertical para cambiar el centro de la vista de la visualización. Esto resulta útil si se usa la opción de diseño **Visual** pero no se usa la opción de vista de **pantalla completa** , mientras que la ventana de **AccScope** se mantiene reducida en comparación con la ventana de destino.

## <a name="testing-the-narrator-scenario"></a>Probar el escenario de narrador

El escenario de narrador es el aspecto más importante que se debe probar al usar **AccScope**, que está diseñado específicamente para visualizar cómo funciona la navegación de elementos de narrador básica cuando se aplica a la aplicación.

Para probar el escenario de narrador, use estas opciones de configuración de **AccScope** :

- **Modo de elemento**: **narrador**
- **Diseño**: **Visual**
- Opciones de **diseño** : **Mostrar información sobre herramientas** y **Mostrar números** seleccionados

Estas son algunas áreas específicas de la aplicación para probar el escenario de narrador:

- **Orden de los elementos:** Compruebe que el orden en el que narrador Lee los controles es preciso, de acuerdo con los números (círculos verdes) mostrados en las visualizaciones. Si los elementos no están en el orden previsto para la lectura, modifique la estructura de la interfaz de usuario de la aplicación y el árbol de automatización de la interfaz de usuario resultante y vuelva a probarlo hasta que haya comprobado que los elementos están en el orden de lectura esperado.
- **Texto hablado:** Mueva el mouse dentro de la visualización y mantenga el puntero sobre cada uno de los rectángulos de elementos para mostrar la información sobre herramientas para cada elemento. En el modo de narrador, la información sobre herramientas muestra una entrada de **texto de narrador** que es literalmente el texto que lee el narrador. Por lo general, este texto se compone del **nombre** y del **tipo de control**. Compruebe que esta es la información adecuada para cada control de la interfaz de usuario. Si alguna información es incorrecta, modifique las propiedades de automatización de la interfaz de usuario a través de las técnicas habilitadas por el marco de interfaz de usuario concreto para hacerlo. (Si el **tipo de control** es inesperado, puede que tenga que usar un control diferente, porque a menudo se controla mediante las implementaciones de control de un marco de interfaz de usuario). Después, vuelva a probar y compruebe que el **texto del narrador** es correcto.
- **Diseño de elementos:** Compruebe cada uno de estos casos:
    - Compruebe que el narrador no expone los elementos redundantes. Un ejemplo de un elemento redundante es el control de clasificación de cada elemento de mosaico de la tienda Windows.
    - Compruebe que los elementos importantes (elementos que el usuario necesita para realizar las tareas clave en la aplicación) aparecen cada uno en la navegación de elementos de narrador.
    - Si está utilizando el diseño **Visual** y falta un elemento porque los controles se superponen entre sí, cambie al diseño de la **lista** para ver la secuencia que notifica el narrador.
    - Compruebe que la estructura de árbol de automatización de la interfaz de usuario global es exacta y esperada para la aplicación.

## <a name="related-topics"></a>Temas relacionados

- [Accessible Event Watcher](accessible-event-watcher.md)
- [Herramientas de pruebas](testing-tools.md)
- [UI Accessibility Checker](ui-accessibility-checker.md)
- [UI Automation Verify](ui-automation-verify.md)
- [Accesibilidad de Microsoft](https://www.microsoft.com/accessibility/)
