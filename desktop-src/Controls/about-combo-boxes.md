---
title: Acerca de los cuadros combinados
description: En esta sección se describen los diferentes tipos de cuadros combinados.
ms.assetid: 76410a87-aa0e-4da9-9e78-c80ac485e3cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 344596a3c0aa772568956344aaddcc053b534993
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104556195"
---
# <a name="about-combo-boxes"></a>Acerca de los cuadros combinados

Un cuadro combinado combina un cuadro de edición o texto estático y una lista.

En este tema se incluyen las siguientes secciones.

-   [Tipos y estilos de cuadro combinado](#combo-box-types-and-styles)
-   [Lista de cuadro combinado](#combo-box-list)
    -   [Selección actual](#current-selection)
    -   [Listas desplegables](#drop-down-lists)
    -   [Contenido de la lista](#list-contents)
-   [Editar campos de selección de controles](#edit-control-selection-fields)
-   [Cuadros combinados dibujados por el propietario](#owner-drawn-combo-boxes)
-   [Cuadros combinados de subclases](#subclassed-combo-boxes)

## <a name="combo-box-types-and-styles"></a>Tipos y estilos de cuadro combinado

Un cuadro combinado consta de una lista y un campo de selección. La lista presenta las opciones que un usuario puede seleccionar y el campo de selección muestra la selección actual. Si el campo de selección es un control de edición, el usuario puede escribir información que no esté disponible en la lista. de lo contrario, el usuario solo puede seleccionar los elementos de la lista.

La biblioteca de controles comunes incluye tres estilos principales de cuadro combinado, tal y como se muestra en la tabla siguiente.



| Tipo de cuadro combinado             | Constante de estilo                                                 | Descripción                                                                                  |
|----------------------------|----------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| Simple                     | [**CBS \_ simple**](combo-box-styles.md)             | Muestra la lista en todo momento y muestra el elemento seleccionado en un control de edición.              |
| Drop-down                  | [**\_lista desplegable de CBS**](combo-box-styles.md)         | Muestra la lista al hacer clic en el icono y muestra el elemento seleccionado en un control de edición.  |
| Lista desplegable (lista desplegable) | [**DROPDOWNLIST de CBS \_**](combo-box-styles.md) | Muestra la lista al hacer clic en el icono y muestra el elemento seleccionado en un control estático. |



 

Las capturas de pantalla siguientes muestran los tres tipos de cuadro combinado tal como pueden aparecer en Windows Vista. En la primera captura de pantalla, el usuario ha seleccionado un elemento en el cuadro combinado simple. El usuario también puede escribir un nuevo valor en el cuadro de edición de este control. La lista tiene el mismo tamaño en el editor de recursos de Microsoft Visual Studio y es lo suficientemente grande como para alojar dos elementos.

![captura de pantalla que muestra un elemento seleccionado en un cuadro combinado simple](images/simplecombo.png)

En la segunda captura de pantalla, el usuario ha escrito nuevo texto en el control de edición del cuadro combinado desplegable. El usuario también podría haber seleccionado un elemento existente. El cuadro de lista se expande para acomodar tantos elementos como sea posible.

![captura de pantalla que muestra el texto escrito en un cuadro combinado desplegable](images/dropdown.png)

En la tercera captura de pantalla, el usuario ha abierto el cuadro combinado de la lista desplegable. El cuadro de lista se expande para acomodar tantos elementos como sea posible. El usuario no puede escribir texto nuevo.

![captura de pantalla que muestra un elemento seleccionado en un cuadro combinado de lista desplegable](images/droplist.png)

También hay varios estilos de cuadro combinado que definen propiedades específicas. Los estilos de cuadro combinado definen propiedades específicas de un cuadro combinado. Puede combinar estilos; sin embargo, algunos estilos solo se aplican a determinados tipos de cuadro combinado. Para obtener una tabla de estilos de cuadro combinado, vea [estilos de cuadro combinado](combo-box-styles.md).

> [!Note]  
> Para usar estilos visuales con cuadros combinados, una aplicación debe incluir un manifiesto y debe llamar a [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) al principio del programa. Para obtener información sobre los estilos visuales, vea [estilos visuales](themes-overview.md). Para obtener información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).

 

## <a name="combo-box-list"></a>Lista de cuadro combinado

La lista es la parte de un cuadro combinado que muestra los elementos que un usuario puede seleccionar. Normalmente, una aplicación inicializa el contenido de la lista cuando crea un cuadro combinado. Cualquier elemento de lista seleccionado por el usuario es la *selección actual*. No se pueden seleccionar varios elementos. En los cuadros combinados simple y desplegable, el usuario puede escribir en el campo de selección en lugar de seleccionar un elemento de lista. En estos casos, no hay ninguna selección actual y es responsabilidad de la aplicación agregar el elemento a la lista y convertirlo en la selección actual, si es adecuado hacerlo.

En esta sección se tratan los temas siguientes:

-   [Selección actual](#current-selection)
-   [Listas desplegables](#drop-down-lists)
-   [Contenido de la lista](#list-contents)

### <a name="current-selection"></a>Selección actual

La selección actual es un elemento de lista que el usuario ha seleccionado; el texto seleccionado aparece en el campo de selección del cuadro combinado. Sin embargo, en el caso de un cuadro combinado simple o un cuadro combinado desplegable, la selección actual solo es una forma de posible entrada del usuario en un cuadro combinado. El usuario también puede escribir texto en el campo de selección.

La selección actual está identificada por el índice de base cero del elemento de lista seleccionado. Una aplicación puede establecerla y recuperarla en cualquier momento. La ventana primaria o el procedimiento de cuadro de diálogo recibe una notificación cuando el usuario cambia la selección actual de un cuadro combinado. La ventana o el cuadro de diálogo primario no se notifican cuando la aplicación cambia la selección.

Cuando se crea un cuadro combinado, no hay ninguna selección actual. Esto también se aplica a un cuadro combinado simple o desplegable, si el usuario ha editado el contenido del campo de selección. Para establecer la selección actual, una aplicación envía el mensaje [**CB \_ SETCURSEL**](cb-setcursel.md) al cuadro combinado. Una aplicación también puede usar el mensaje [**CB \_ SELECTSTRING**](cb-selectstring.md) para establecer la selección actual en un elemento de lista cuya cadena comienza con una cadena especificada. Para determinar la selección actual, una aplicación envía el mensaje [**CB \_ GETCURSEL**](cb-getcursel.md) al cuadro combinado. Si no hay ninguna selección actual, este mensaje devuelve el \_ error CB.

Cuando el usuario cambia la selección actual en un cuadro combinado, el procedimiento de cuadro de diálogo o la ventana primaria recibe un mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) con el código de notificación [ \_ SELCHANGE de CBN](cbn-selchange.md) en la palabra de orden superior del parámetro *wParam* . Este código de notificación no se envía cuando la selección actual se establece mediante el mensaje [**CB \_ SETCURSEL**](cb-setcursel.md) .

Un cuadro combinado desplegable o un cuadro de lista desplegable envía el código de notificación [CBN \_ primer plano](cbn-closeup.md) al procedimiento primario de la ventana o cuadro de diálogo cuando se cierra la lista desplegable. Si el usuario ha cambiado la selección actual, el cuadro combinado también enviará el código de notificación [CBN \_ SELCHANGE](cbn-selchange.md) cuando se cierre la lista desplegable. Para ejecutar un proceso específico cada vez que el usuario selecciona un elemento de lista, puede controlar el \_ código de notificación CBN SELCHANGE o CBN \_ primer plano. Normalmente, se espera el \_ código de notificación primer plano de CBN antes de procesar un cambio en la selección actual. Esto puede ser especialmente importante si se requiere una cantidad significativa de procesamiento.

Una aplicación también podría procesar los códigos de notificación [CBN \_ SELENDOK](cbn-selendok.md) y [CBN \_ SELENDCANCEL](cbn-selendcancel.md) . El sistema envía CBN \_ SELENDOK cuando el usuario selecciona un elemento de lista, o selecciona un elemento y, a continuación, cierra la lista. Esto indica que el usuario ha finalizado y que se debe procesar la selección. CBN \_ SELENDCANCEL se envía cuando el usuario selecciona un elemento, pero selecciona otro control, presiona ESC mientras la lista desplegable está abierta o cierra el cuadro de diálogo. Esto indica que la selección del usuario se debe omitir. CBN \_ SELENDOK se envía antes de cada mensaje de [CBN \_ SELCHANGE](cbn-selchange.md) .

En un cuadro combinado simple, el sistema envía el código de notificación [CBN \_ DBLCLK](cbn-dblclk.md) cuando el usuario hace doble clic en un elemento de lista. En un cuadro combinado desplegable o una lista desplegable, un solo clic oculta la lista, por lo que no es posible hacer doble clic en un elemento.

### <a name="drop-down-lists"></a>Listas desplegables

Ciertas notificaciones y mensajes solo se aplican a los cuadros combinados que contienen listas desplegables. Cuando una lista desplegable está abierta o cerrada, la ventana primaria de un cuadro combinado recibe una notificación en forma de mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) . Si se abre la lista, la palabra de orden superior de *wParam* es [CBN \_ DROPDOWN](cbn-dropdown.md). Si se cierra la lista, es [CBN \_ primer plano](cbn-closeup.md).

Una aplicación puede abrir la lista de un cuadro combinado desplegable o un cuadro de lista desplegable mediante el mensaje [**CB \_ SHOWDROPDOWN**](cb-showdropdown.md) . Puede determinar si la lista está abierta mediante el mensaje [**CB \_ GETDROPPEDSTATE**](cb-getdroppedstate.md) y puede determinar las coordenadas de una lista desplegable mediante el mensaje [**CB \_ GETDROPPEDCONTROLRECT**](cb-getdroppedcontrolrect.md) . Una aplicación también puede aumentar el ancho de una lista desplegable mediante el mensaje [**CB \_ SETDROPPEDWIDTH**](cb-setdroppedwidth.md) .

### <a name="list-contents"></a>Contenido de la lista

Cuando una aplicación crea un cuadro combinado, normalmente inicializa el cuadro combinado agregando uno o más elementos a la lista. Más adelante, una aplicación puede Agregar o eliminar elementos de lista, reinicializar la lista o recuperar información de los elementos de ella.

Una aplicación agrega elementos de lista a un cuadro combinado mediante el envío del mensaje [**CB \_ ADDSTRING**](cb-addstring.md) a él. El elemento especificado se agrega al final de la lista o, en un cuadro combinado ordenado, en su posición ordenada correcta en función de la cadena del elemento. En un cuadro combinado sin ordenar, una aplicación puede utilizar el mensaje [**CB \_ INSERTSTRING**](cb-insertstring.md) para insertar un elemento en una posición específica. Una vez agregado, un elemento de lista se identifica por su posición.

Mediante el mensaje [**CB \_ FINDSTRING**](cb-findstring.md) o [**CB \_ FindExactString con**](cb-findstringexact.md) , una aplicación puede determinar la posición de un elemento de lista. **CB \_ FINDSTRING** busca un elemento cuya cadena comienza con la cadena especificada. **CB \_ FINDEXACTSTRING con** busca un elemento cuya cadena coincide exactamente con la cadena. Ninguno de los mensajes distingue mayúsculas de minúsculas.

Una aplicación puede quitar un elemento de lista mediante el mensaje [**CB \_ DELETESTRING**](cb-deletestring.md) . Si una aplicación necesita reinicializar la lista de cuadro combinado, primero puede borrar todo su contenido mediante el mensaje [**CB \_ RESETCONTENT**](cb-resetcontent.md) . Cuando se agregan varios elementos a la lista después de que ya se haya mostrado un cuadro combinado, una aplicación puede desactivar la marca volver a dibujar para evitar que el cuadro combinado se vuelva a dibujar después de agregar cada elemento. Para obtener más información sobre cómo volver a dibujar, vea la descripción del mensaje de [**\_ SETREDRAW de WM**](/windows/desktop/gdi/wm-setredraw) .

Para recuperar la cadena asociada con un elemento de lista, una aplicación puede usar el mensaje [**CB \_ GETLBTEXT**](cb-getlbtext.md) . La cadena del elemento se copia en el búfer especificado por la aplicación. Para asegurarse de que el búfer es lo suficientemente grande como para recibir la cadena, la aplicación puede utilizar primero el mensaje [**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md) para determinar la longitud de la cadena. Para obtener el número de elementos de lista en un cuadro combinado, una aplicación puede usar el mensaje [**\_ GETCOUNT GETCOUNT**](cb-getcount.md) .

## <a name="edit-control-selection-fields"></a>Editar campos de selección de controles

Una aplicación puede recuperar o establecer el contenido del campo de selección y puede determinar o establecer la selección de edición. La aplicación también puede limitar la cantidad de texto que un usuario puede escribir en el campo de selección. Cuando cambia el contenido del campo de selección, el sistema envía mensajes de notificación a la ventana primaria o al procedimiento de cuadro de diálogo.

Para recuperar el contenido del campo de selección, una aplicación puede enviar el mensaje de [**\_ GETTEXT de WM**](/windows/desktop/winmsg/wm-gettext) al cuadro combinado. Para establecer el contenido del campo de selección de un cuadro combinado simple o desplegable, una aplicación puede enviar el mensaje de [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) al cuadro combinado.

La selección de edición es el intervalo de texto seleccionado, si existe, en el campo de selección de un cuadro combinado simple o desplegable. Una aplicación puede determinar las posiciones de caracteres inicial y final de la selección actual mediante el mensaje [**CB \_ GETEDITSEL**](cb-geteditsel.md) . También puede seleccionar caracteres en la selección de edición mediante el mensaje [**CB \_ SETEDITSEL**](cb-seteditsel.md) .

Inicialmente, la cantidad de texto que el usuario puede escribir en el campo de selección está limitada por el tamaño del campo de selección. Sin embargo, si el cuadro combinado tiene el estilo [**CBS \_ AUTOHSCROLL**](combo-box-styles.md) , el texto puede continuar más allá del tamaño del campo de selección. Una aplicación puede usar el mensaje [**CB \_ LIMITTEXT**](cb-limittext.md) para limitar la cantidad de texto que un usuario puede escribir en el campo de selección, independientemente de si el control tiene el estilo **CBS \_ AUTOHSCROLL** .

Cuando el usuario edita el contenido del campo de selección, la ventana primaria o el procedimiento de cuadro de diálogo recibe mensajes de notificación. El código de notificación [ \_ EDITUPDATE de CBN](cbn-editupdate.md) se envía en primer lugar, lo que indica que se ha editado el texto en el campo de selección. Una vez mostrado el texto modificado, el sistema envía [CBN \_ EDITCHANGE](cbn-editchange.md). Cuando el contenido del campo de selección cambia a medida que el resultado de un elemento de lista se selecciona, estos mensajes no se envían.

## <a name="owner-drawn-combo-boxes"></a>Owner-Drawn cuadros combinados

Una aplicación puede crear un cuadro combinado dibujado por el propietario para asumir la responsabilidad de dibujar los elementos de la lista. La ventana primaria de un cuadro combinado dibujado por el propietario (su propietario) recibe mensajes de [**WM \_ DRAWITEM**](wm-drawitem.md) cuando es necesario pintar una parte del cuadro combinado. Un cuadro combinado dibujado por el propietario puede mostrar información distinta de las cadenas de texto, o además de ellas. Los cuadros combinados dibujados por el propietario pueden ser de cualquier tipo. Sin embargo, el control de edición de un cuadro combinado simple o desplegable solo puede mostrar texto, mientras que el propietario pinta el campo de selección en un cuadro de lista desplegable.

El propietario de un cuadro combinado dibujado por el propietario debe procesar el mensaje de la [**\_ DRAWITEM de WM**](wm-drawitem.md) . Este mensaje se envía siempre que se debe volver a dibujar una parte del cuadro combinado. Es posible que el propietario tenga que procesar otros mensajes, en función de los estilos especificados para el cuadro combinado.

Una aplicación puede crear un cuadro combinado dibujado por el propietario especificando el estilo [**CBS \_ OWNERDRAWFIXED**](combo-box-styles.md) o [**CBS \_ OWNERDRAWVARIABLE**](combo-box-styles.md) . Si todos los elementos de la lista del cuadro combinado tienen el mismo alto, como cadenas o iconos, una aplicación puede usar el estilo de **CBS \_ OWNERDRAWFIXED** . Si los elementos de lista son de alto variable, como mapas de bits de tamaño diferente, una aplicación puede usar el estilo **CBS \_ OWNERDRAWVARIABLE** .

El propietario de un cuadro combinado dibujado por el propietario puede procesar un mensaje de [**\_ MEASUREITEM de WM**](wm-measureitem.md) para especificar las dimensiones de los elementos de la lista en el cuadro combinado. Si la aplicación crea el cuadro combinado mediante el estilo de [**CBS \_ OWNERDRAWFIXED**](combo-box-styles.md) , el sistema envía el mensaje de **WM \_ MEASUREITEM** una sola vez. Las dimensiones especificadas por el propietario se usan para todos los elementos de lista. Si se usa el estilo [**CBS \_ OWNERDRAWVARIABLE**](combo-box-styles.md) , el sistema envía un mensaje de **WM \_ MEASUREITEM** para cada elemento de lista que se agrega al cuadro combinado. El propietario puede determinar o establecer el alto de un elemento de lista en cualquier momento mediante los mensajes [**CB \_ GETITEMHEIGHT**](cb-getitemheight.md) y [**CB \_ SETITEMHEIGHT**](cb-setitemheight.md) , respectivamente.

Si la información que se muestra en un cuadro combinado dibujado por el propietario incluye texto, una aplicación puede realizar un seguimiento del texto de cada elemento de la lista especificando el estilo de [**CBS \_ HASSTRINGS**](combo-box-styles.md) . Los cuadros combinados con el estilo de [**\_ ordenación CBS**](combo-box-styles.md) se ordenan en función de este texto. Si un cuadro combinado está ordenado y no es el estilo **\_ HASSTRINGS de CBS** , el propietario debe procesar el mensaje de [**\_ COMPAREITEM de WM**](wm-compareitem.md) .

En un cuadro combinado dibujado por el propietario, el propietario debe realizar un seguimiento de los elementos de la lista que contienen información que no es o además del texto. Una manera cómoda de hacerlo es guardar el identificador de la información como datos de elemento. Para liberar los objetos de datos asociados a los elementos de un cuadro combinado, el propietario puede procesar el mensaje de [**WM \_ DELETEITEM**](wm-deleteitem.md) .

## <a name="subclassed-combo-boxes"></a>Cuadros combinados de subclases

La subclase es un procedimiento que permite que una aplicación intercepte y procese mensajes enviados o publicados en una ventana. Mediante el uso de subclases, una aplicación puede sustituir su propio procesamiento para ciertos mensajes, a la vez que se mantiene la mayor parte del procesamiento de mensajes en el procedimiento de ventana definido por la clase.

Cuando el sistema operativo crea una ventana, guarda información sobre ella en una estructura de datos interna que incluye un puntero al procedimiento de ventana. Para subclases de una ventana, una aplicación llama a la función [**SetClassLong**](/windows/desktop/api/winuser/nf-winuser-setclasslonga) para reemplazar el puntero a ese procedimiento con un puntero a un procedimiento de subclase definido por la aplicación. A partir de ese momento, todos los mensajes a la ventana se envían al procedimiento de subclase. Este procedimiento utiliza la función [**CallWindowProc**](/windows/desktop/api/winuser/nf-winuser-callwindowproca) para pasar los mensajes no procesados al procedimiento de ventana original. Para obtener una descripción del procesamiento de mensajes realizado por el procedimiento de ventana de clase COMBOBOX, vea [comportamiento del cuadro combinado predeterminado](combo-box-features.md).

Cuando el cuadro combinado está fuera de un cuadro de diálogo, una aplicación no puede procesar las teclas TAB, entrar y ESC a menos que use un procedimiento de subclase. Cuando un cuadro combinado simple o desplegable recibe el foco de entrada, establece inmediatamente el foco en su control de edición secundario. Por lo tanto, una aplicación debe subclase del control de edición para interceptar la entrada del teclado para un cuadro combinado simple o desplegable. Para obtener un ejemplo de esto, vea [subclase de un cuadro combinado](using-combo-boxes.md).

Si un procedimiento de subclase procesa el mensaje de [**\_ dibujo de WM**](/windows/desktop/gdi/wm-paint) , debe utilizar la función [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) para preparar el dibujo. Antes de llamar a la función [**EndPaint**](/windows/desktop/api/winuser/nf-winuser-endpaint) , pasa el identificador de contexto de dispositivo (DC) como parámetro *wParam* para el procedimiento de ventana. Si se llama primero a **EndPaint** , el procedimiento de ventana de clase no realiza ningún dibujo porque **EndPaint** valida toda la ventana.

Una técnica relacionada con la subclase es la superclase. Una superclase es similar a cualquier otra clase, salvo que su procedimiento de ventana no llama a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para controlar los mensajes no procesados. En su lugar, pasa los mensajes no procesados al procedimiento de ventana para la clase de ventana primaria. Siga las instrucciones de [procedimientos de ventana](/windows/desktop/winmsg/window-procedures) para evitar problemas que pueden producirse con subclases y superclases.

 

 