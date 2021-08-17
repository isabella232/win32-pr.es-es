---
title: 'Herramientas de accesibilidad: AccScope'
description: La herramienta AccScope permite a los desarrolladores y evaluadores evaluar la accesibilidad de su aplicación durante el desarrollo y el diseño de la aplicación, en lugar de en las fases de pruebas tardías del ciclo de desarrollo de una aplicación.
ms.assetid: 7C4D78CD-CDDA-8369-B747-6224C152A997
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4e55aa40822b786ee69185abe753bb0bacd65345d042526a126b4c8343a2639
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118327731"
---
# <a name="accessibility-tools---accscope"></a>Herramientas de accesibilidad: AccScope

La **herramienta AccScope** permite a los desarrolladores y evaluadores evaluar la accesibilidad de su aplicación durante el desarrollo y el diseño de la aplicación, en lugar de en las fases de pruebas tardías del ciclo de desarrollo de una aplicación. Las pruebas pueden comenzar incluso en las frases prototipo tempranas. **AccScope** puede visualizar cómo un lector de pantalla expone la información de Automatización de la interfaz de usuario que proporciona una aplicación y puede mostrar áreas en las que es posible que quiera agregar información o soporte técnico a la aplicación para mejorar su accesibilidad.

> [!NOTE]
> **AccScope** es una herramienta heredada. En su [lugar,](https://accessibilityinsights.io/) se recomienda usar Ideas accesibilidad.

## <a name="about-accscope"></a>Acerca de AccScope

**AccScope** se instala con Windows Software Development Kit (SDK). Se encuentra en la carpeta AccScope de la plataforma bin version \\ \\ <  > \\ <  > \\ de la ruta de instalación del SDK. Ejecute el programa AccScope.exe.

**AccScope** es una aplicación de escritorio, no una Windows store. Puede usarlo para ver cualquier aplicación que aparezca como una ventana, incluida una aplicación de escritorio o una aplicación Windows Store.

Es posible que tenga que ejecutar **AccScope** como administrador la primera vez que lo use para habilitar el modo Narrador.

**AccScope** está disponible como parte de los archivos binarios de las herramientas de accesibilidad, en Windows SDK. No se distribuye como una descarga de exe independiente y no existe en los SDK anteriores.

## <a name="file-menu-options"></a>Opciones del menú Archivo

- Seleccione **Actualizar** para actualizar toda la información de **AccScope** para que coincida con el estado actual de la ventana de destino. Para una interfaz de usuario que contiene un gran número de elementos, esto puede tardar varios segundos en completarse.
- Active o desactive **Always on Top para** cambiar el comportamiento de ventana de la interfaz de usuario de **AccScope.** **Always on Top checked** es el valor predeterminado.
- Seleccione **Salir para** salir de **AccScope.**

## <a name="view-options"></a>Ver las opciones

- Seleccione **Pantalla completa** para ejecutar la herramienta **AccScope** en una vista de pantalla completa (a continuación, use la tabulación para ver la ventana de destino). Si **AccScope y** la aplicación de destino ejecutan pantalla completa, la ubicación, los rectángulos delimitadores y la visualización general de los elementos se corresponderán entre la aplicación y la **vista AccScope.**
    > [!Note]  
    > **AccScope** y su destino deben ejecutarse en la misma pantalla.

     

- Seleccione **Enfoque automático** para permitir que AccScope cambie la ventana de destino cada vez que un usuario mueva el foco a la ventana (mediante el mouse o el teclado).
- Seleccione **Actualización automática** para habilitar el modo **AccScope** que actualiza todos los datos de accesibilidad de la ventana de destino cada 5 segundos. Esto resulta útil si microsoft Automatización de la interfaz de usuario datos de la ventana de destino cambian constantemente.
- Seleccione **Regiones activas** para resaltar las regiones activas que emiten notificaciones en la ventana de destino. La activación de un evento de región en directo muestra un elemento emergente rojo con información sobre la región en directo, incluido su nombre y su valor "aria-live" (o el equivalente análogo de valor de ARIA para aplicaciones que no usan directamente HTML, sino que usan el concepto de regiones en directo en la compatibilidad con Automatización de la interfaz de usuario).

## <a name="element-mode"></a>Modo de elemento

Puede elegir ver una ventana de destino a través de uno de estos modos:

- **Control hoja:** muestra una Automatización de la interfaz de usuario de elementos **control** con relaciones de elementos primarios y secundarios, es decir, una vista de controles interactivos de "nivel hoja". Use esta opción para ver si todos los controles interactivos aparecen correctamente en el Automatización de la interfaz de usuario de una **vista de** control.
- **Patrón de texto:** muestra los intervalos de texto visibles de los contenedores **TextPattern** desde la ventana de destino. Use esta opción para representar visualmente los intervalos de texto visibles Automatización de la interfaz de usuario **elementos TextPattern.**
- **Narrador:** muestra los elementos Automatización de la interfaz de usuario que el Narrador puede identificar mediante la metáfora "navegación de elementos" del narrador.
- **Filtro personalizado:** muestra un árbol de control filtrado con una selección de subconjuntos de control: **Button**, **Checkbox**, **Combobox**, **Grid**, **Hyperlink**, **List**, **Menu** o **Table**.

Al cambiar **la configuración del modo** de elemento se desencadena una actualización de la visualización. Para una interfaz de usuario que contiene un gran número de elementos, esto puede tardar varios segundos en completarse.

## <a name="layout-options"></a>Opciones de diseño

Puede seleccionar Visual o **Lista como** **modo** de visualización para el **diseño accScope.** **El objeto** visual coloca los elementos en el espacio de coordenadas en la misma relación que la ventana de destino. **La** lista ordena los elementos de una lista descendente alineada a la izquierda en la ventana **AccScope** y el orden de la lista es equivalente al orden de tabulación o de lectura.

- Seleccione una  opción de Mostrar imágenes para controlar cuándo los rectángulos simples de los elementos de imagen se reemplazan por la imagen real (o una ventanilla pequeña de esa imagen, ya que a menudo los rectángulos son más pequeños que la imagen real). El valor predeterminado **es Al mantener el** puntero , que muestra la imagen cuando navega dentro de **AccScope** y mantiene el mouse sobre el rectángulo de un elemento de imagen. Las opciones alternativas **son Siempre** o **Nunca.**
- Seleccione **Mostrar información sobre** herramientas para mostrar información básica del elemento cada vez que mantenga el mouse sobre un elemento en la visualización **AccScope.** Si el **modo de elemento** es **Control** hoja o Patrón de **texto,** la información que se muestra en la información sobre herramientas es el nivel de elemento de prioridad Automatización de la interfaz de usuario propiedades. Si el **modo de elemento** es **Narrador,** la información incluye el texto que el Narrador leería para el elemento.
- Seleccione **Mostrar números para** mostrar los números de secuencia que indican el orden de representación del control en el diseño. El esquema de número se basa en la configuración **modo de** elemento:
    - **Control hoja:** los números indican el orden en que aparecen los controles hoja en el Automatización de la interfaz de usuario hoja.
    - **Patrón de** texto: los números indican el orden en que aparecen los intervalos de texto en un intervalo de documentos.
    - **Narrador:** el número indica el orden en el que se navegan los elementos en la navegación de elementos del narrador.

## <a name="choosing-a-window"></a>Elección de una ventana

En la ventana **de** etiqueta, encontrará una lista desplegable que muestra todas las ventanas HWND que están activas actualmente en el sistema. El texto de cada ventana que aparece en la lista desplegable es el título de la ventana y también un identificador hexadecimal de ventana entre corchetes. Elija una de estas opciones para cambiar la ventana de destino en la **que AccScope** está informando. Puede volver a elegir el mismo elemento para obtener el mismo comportamiento que una actualización **explícita.**

## <a name="using-the-accscope-visualization"></a>Uso de la visualización AccScope

La imagen siguiente es una captura de pantalla de la **visualización AccScope.** En esta captura de pantalla concreta se muestra la **herramienta AccScope** que ve la ventana de nivel superior para la salida de ejemplo de accesibilidad [xaml,](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/XAML%20accessibility%20sample) que se ejecuta como una aplicación en la misma máquina. En esta captura de pantalla se muestra el modo de elemento predeterminado **de Control hoja** y el valor **visual** de **Diseño**.

![Captura de pantalla de la visualización accScope](images/accscopescreenshot.png)

Observe cómo esta visualización representa los controles en el espacio de coordenadas aproximado que vería en la aplicación. Pero en lugar de mostrar los objetos visuales XAML o el texto completo de los controles de texto, muestra los valores de la propiedad **Name** que proceden de cada elemento de control, mediante Automatización de la interfaz de usuario.

Además de las opciones de menú descritas anteriormente, también puede usar estas técnicas:

- Haga clic en el rectángulo de cualquier elemento en **las visualizaciones Visual** o **List** para mostrar un elemento emergente Propiedades **de UIA.** Muestra una serie de las propiedades Automatización de la interfaz de usuario importantes para ese elemento, incluidas algunas de las propiedades estándar de [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) y otra información, como valores de ARIA y una descripción del **proveedor**.
- Haga clic con el botón derecho en el rectángulo de cualquier elemento de las visualizaciones **Visual** o **List** para mostrar un menú contextual para ejercer los patrones que admite el elemento. Por ejemplo, si un elemento admite [**InvokePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationinvokepattern), el menú contextual incluye un elemento para **Invoke**. Seleccione ese elemento y la API de patrón adecuada se ejercerá en la aplicación correspondiente. **AccScope** admite esta característica para los patrones siguientes: **Invoke**, **ExpandCollapse**, **Toggle**, **SelectionItem**, **ScrollItem**.
- Ajuste el **control deslizante Transparencia** para cambiar la opacidad o transparencia de la ventana **AccScope.** De forma predeterminada, se muestra como una opacidad del 100 %. Hacer que la ventana sea parcialmente transparente puede ser útil para ver las partes de la ventana de destino a través de la interfaz de usuario de **AccScope** mientras se usa **Always On modo** Superior.
- Si se muestran, use las barras de desplazamiento horizontal y vertical para cambiar el centro de la vista de la visualización. Esto resulta útil si usa  la opción Diseño  visual pero no usa la opción de vista De pantalla completa, a la vez que deja la ventana **AccScope** pequeña en comparación con la ventana de destino.

## <a name="testing-the-narrator-scenario"></a>Prueba del escenario del narrador

El escenario narrador es el aspecto más importante que se debe probar al usar **AccScope,** que está diseñado específicamente para visualizar cómo funciona la navegación básica del elemento Narrador cuando se aplica a la aplicación.

Para probar el escenario del Narrador, use estas **opciones de configuración de AccScope:**

- **Modo de elemento:** **Narrador**
- **Diseño:** **Objeto visual**
- **Opciones de** diseño: **Mostrar información sobre herramientas** y Mostrar **números** seleccionados

Estas son algunas áreas específicas de la aplicación para probar el escenario del Narrador:

- **Orden de los elementos:** Compruebe que el orden en el que Narrador lee los controles es preciso, según los números (círculos verdes) que se muestran en las visualizaciones. Si los elementos no están en el orden esperado para la lectura, modifique la estructura de la interfaz de usuario de la aplicación y el árbol Automatización de la interfaz de usuario resultante y vuelva a probar hasta que haya comprobado que los elementos están en el orden de lectura esperado.
- **Texto hablado:** Mueva el mouse dentro de la visualización y mantenga el puntero sobre cada uno de los rectángulos de elemento para mostrar las sugerencias de herramientas para cada elemento. En el modo Narrador, las sugerencias de herramientas muestran una entrada De texto **del narrador** que es literalmente el texto que lee el narrador. Por lo general, este texto se compone del **nombre y** del tipo **de control**. Compruebe que esta es la información adecuada para cada control de la interfaz de usuario. Si alguna información es incorrecta, modifique las propiedades Automatización de la interfaz de usuario mediante las técnicas habilitadas por su marco de interfaz de usuario determinado para hacerlo. (Si **el tipo de** control es inesperado, es posible que tenga que usar un control diferente, ya que a menudo se controla exclusivamente mediante implementaciones de controles de un marco de interfaz de usuario). A continuación, vuelva a probar y compruebe que **El texto del narrador** es correcto.
- **Diseño de elementos:** Compruebe cada uno de estos casos:
    - Compruebe que narrador no expone elementos redundantes. Un ejemplo de un elemento redundante es el control de clasificaciones de cada elemento Windows de icono store.
    - Compruebe que los elementos importantes (elementos que el usuario necesita para realizar tareas clave en la aplicación) aparecen en la navegación de elementos del Narrador.
    - Si usa el  diseño visual y falta un elemento porque los  controles se superponen entre sí, cambie a Diseño de lista para ver la secuencia que narrador notifica.
    - Compruebe que la estructura Automatización de la interfaz de usuario estructura general del árbol es precisa y esperada para la aplicación.

## <a name="related-topics"></a>Temas relacionados

- [Accessible Event Watcher](accessible-event-watcher.md)
- [Herramientas de prueba](testing-tools.md)
- [UI Accessibility Checker](ui-accessibility-checker.md)
- [UI Automation Verify](ui-automation-verify.md)
- [Accesibilidad de Microsoft](https://www.microsoft.com/accessibility/)
