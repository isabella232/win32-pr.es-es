---
title: Editar operaciones de texto de control
description: El sistema procesa automáticamente todas las operaciones de texto iniciadas por el usuario y notifica a la aplicación cuando se completan las operaciones.
ms.assetid: 9af3a1bc-4c87-4cc9-966d-50742be7c811
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8698fbd38241a0e5c3f40e69f7ab401fc22e3982e2bc70001733bc71daf49689
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826375"
---
# <a name="edit-control-text-operations"></a>Editar operaciones de texto de control

El sistema procesa automáticamente todas las operaciones de texto iniciadas por el usuario y notifica a la aplicación cuando se completan las operaciones.

En los temas siguientes se tratan las operaciones de texto iniciadas por el usuario y la respuesta de la aplicación:

-   [Selección de un control De edición](#selecting-an-edit-control)
-   [Configuración y recuperación de texto](#setting-and-retrieving-text)
-   [Selección de texto](#selecting-text)
-   [Reemplazar texto](#replacing-text)
-   [Cambiar la fuente utilizada por un control Edit](#changing-the-font-used-by-an-edit-control)
-   [Cortar operaciones de copiar pegar y borrar](#cut-copy-paste-and-clear-operations)
-   [Modificar texto](#modifying-text)
-   [Limitar el texto escrito por el usuario](#limiting-user-entered-text)
-   [Operaciones de caracteres y líneas](#character-and-line-operations)
-   [Desplazar texto en un control Edit](#scrolling-text-in-an-edit-control)
-   [Establecer tabulaciones y márgenes](#setting-tab-stops-and-margins)
-   [Ocultación de la entrada del usuario](#concealing-user-input)
-   [Usar enteros](#using-integers)
-   [Deshacer operaciones de texto](#undoing-text-operations)
-   [Control de wordwrap y saltos de línea](#handling-wordwrap-and-line-breaks)
-   [Recuperar puntos y caracteres](#retrieving-points-and-characters)
-   [Autocompletar de cadenas](#autocompletion-of-strings)
-   [Script complejo en controles de edición](#complex-script-in-edit-controls)

## <a name="selecting-an-edit-control"></a>Selección de un control De edición

El usuario puede seleccionar un control de edición haciendo clic en él con el mouse o presionando la tecla TAB para desplazarse a él. El método de tabulación forma parte de una interfaz de teclado predefinida que proporciona el sistema. Para obtener una descripción completa de esta interfaz, vea [Cuadros de diálogo](/windows/desktop/dlgbox/dialog-boxes). Cuando el usuario selecciona un control de edición, el sistema proporciona al control el foco del teclado (vea "Foco y activación del teclado" en Acerca de la entrada de [teclado)](/windows/desktop/inputdev/about-keyboard-input)y resalta su texto mediante el vídeo inverso.

## <a name="setting-and-retrieving-text"></a>Configuración y recuperación de texto

Una aplicación puede establecer el texto de un control de edición mediante la función [**SetWindowText,**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta) la función [**SetDlgItemText**](/windows/desktop/DevNotes/-setdlgitemtext) o enviando al control un mensaje [**WM \_ SETTEXT.**](/windows/desktop/winmsg/wm-settext)

Para recuperar todo el texto de un control de edición, use primero la función [**GetWindowTextLength**](/windows/desktop/api/winuser/nf-winuser-getwindowtextlengtha) o el mensaje [**\_ WM GETTEXTLENGTH**](/windows/desktop/winmsg/wm-gettextlength) para determinar el tamaño de búfer necesario para contener el texto. A continuación, recupere el texto mediante la [**función GetWindowText,**](/windows/desktop/DevNotes/-getwindowtext) la [**función GetDlgItemText**](/windows/desktop/api/winuser/nf-winuser-getdlgitemtexta) o el [**mensaje WM \_ GETTEXT.**](/windows/desktop/winmsg/wm-gettext)

## <a name="selecting-text"></a>Selección de texto

Después de seleccionar un control de edición, el usuario puede seleccionar texto en el control mediante el mouse o el teclado. Una aplicación puede recuperar las posiciones de caracteres inicial y final de la selección actual en un control de edición enviando al control un [**mensaje EM \_ GETSEL.**](em-getsel.md) El valor devuelto para la posición final es uno mayor que el último carácter de la selección (es decir, la posición del primer carácter después del último carácter seleccionado).

Una aplicación también puede seleccionar texto en un control de edición enviando al control un mensaje [**EM \_ SETSEL**](em-setsel.md) con los índices de caracteres inicial y final de la selección. Por ejemplo, la aplicación puede usar **EM \_ SETSEL** con [**EM \_ REPLACESEL**](em-replacesel.md) para eliminar texto de un control de edición.

Estos tres mensajes se aplican a los controles de edición de una sola línea y de varias líneas.

## <a name="replacing-text"></a>Reemplazar texto

Una aplicación puede reemplazar el texto seleccionado en un control de edición enviando al control un mensaje [**EM \_ REPLACESEL**](em-replacesel.md) con un puntero al texto de reemplazo. Si no hay ninguna selección actual, **EM \_ REPLACESEL** inserta el texto de reemplazo en el punto de inserción. La aplicación puede recibir un código [de notificación EN \_ ERRSPACE](en-errspace.md) si el texto de reemplazo supera la memoria disponible. Este mensaje se aplica a los controles de edición de línea única y multilínea.

Una aplicación puede usar [**EM \_ REPLACESEL**](em-replacesel.md) para reemplazar parte del texto de un control de edición o la función [**SetDlgItemText**](/windows/desktop/api/winuser/nf-winuser-setdlgitemtexta) para reemplazarlo todo.

## <a name="changing-the-font-used-by-an-edit-control"></a>Cambiar la fuente utilizada por un control Edit

Una aplicación puede cambiar la fuente que usa un control de edición mediante el envío del [**mensaje \_ WM SETFONT.**](/windows/desktop/winmsg/wm-setfont) La mayoría de las aplicaciones lo hacen al procesar [**el mensaje WM \_ INITDIALOG.**](/windows/desktop/dlgbox/wm-initdialog) Cambiar la fuente no cambia el tamaño del control de edición; Es posible que las aplicaciones que envían el mensaje **\_ SETFONT** de WM tengan que recuperar las métricas de fuente del texto y volver a calcular el tamaño del control de edición. Para obtener más información sobre las fuentes y las métricas de fuente, vea [Fuentes y texto.](/windows/desktop/gdi/fonts-and-text)

## <a name="cut-copy-paste-and-clear-operations"></a>Cortar operaciones de copiar pegar y borrar

Hay cuatro mensajes para mover texto entre un control de edición y el Portapapeles. El [**mensaje \_ WM COPY**](/windows/desktop/dataxchg/wm-copy) copia la selección actual (si la hay) de un control de edición en el Portapapeles sin eliminarlo del control de edición. El [**mensaje \_ WM CUT**](/windows/desktop/dataxchg/wm-cut) elimina la selección actual (si la hay) en el control de edición y copia el texto eliminado en el Portapapeles. El [**mensaje \_ WM CLEAR**](/windows/desktop/dataxchg/wm-clear) elimina la selección actual (si existe) de un control de edición, pero no lo copia en el Portapapeles (a menos que el usuario presione la tecla MAYÚS). El [**mensaje \_ WM PASTE**](/windows/desktop/dataxchg/wm-paste) copia texto del Portapapeles en un control de edición en el punto de inserción. Estos cuatro mensajes se aplican a los controles de edición de una sola línea y de varias líneas.

Microsoft Windows NT 4.0 y versiones posteriores: un control de edición incluye un menú contextual integrado que facilita al usuario mover texto entre el control de edición y el Portapapeles. El menú contextual aparece cuando el usuario hace clic con el botón derecho en el control. Los comandos del menú contextual incluyen **Deshacer,** **Cortar,** **Copiar,** **Pegar,** **Eliminar** y **Seleccionar todo.**

## <a name="modifying-text"></a>Modificar texto

El usuario puede seleccionar, eliminar o mover texto en un control de edición. El sistema mantiene una marca interna para cada control de edición que indica si se ha modificado el contenido del control. El sistema borra esta marca cuando crea el control y establece la marca cada vez que se modifica el texto del control. Una aplicación puede recuperar la marca de modificación enviando al control [**un mensaje \_ EM GETMODIFY.**](em-getmodify.md) A continuación, la aplicación puede establecer o borrar la marca de modificación enviando al control un mensaje [**\_ EM SETMODIFY.**](em-setmodify.md) Estos mensajes se aplican a los controles de edición de una sola línea y de varias líneas.

## <a name="limiting-user-entered-text"></a>Limitar el texto escrito por el usuario

El límite predeterminado para la cantidad de texto que un usuario puede escribir en un control de edición es de 32 KB. Una aplicación puede cambiar el límite predeterminado enviando al control [**un mensaje EM \_ SETLIMITTEXT.**](em-setlimittext.md) Este mensaje establece un límite máximo en el número de bytes que el usuario puede escribir en un control de edición, pero no afecta al texto que ya está en el control cuando el mensaje se envió ni al texto copiado al control por la función [**SetDlgItemText**](/windows/desktop/api/winuser/nf-winuser-setdlgitemtexta) o el mensaje [**\_ SETTEXT de WM.**](/windows/desktop/winmsg/wm-settext) Por ejemplo, suponga que la aplicación usa la función **SetDlgItemText** para colocar 500 bytes en un control de edición y el usuario también escribe 500 bytes (1000 bytes en total). Si la aplicación envía un mensaje **\_ EM SETLIMITTEXT** que limita el texto escrito por el usuario a 300 bytes, los 1000 bytes que ya están en el control de edición permanecen allí y el usuario no puede agregar más texto. Por otro lado, si la aplicación envía un mensaje **\_ EM SETLIMITTEXT** que limita el texto escrito por el usuario a 1300 bytes, los 1000 bytes permanecen, pero el usuario puede agregar 300 bytes más.

Cuando el usuario alcanza el límite de caracteres de un control de edición, el sistema envía a la aplicación un mensaje [**WM \_ COMMAND**](/windows/desktop/menurc/wm-command) que contiene un código de notificación [EN \_ MAXTEXT.](en-maxtext.md) Este código de notificación no significa que se haya agotado la memoria, sino que se ha alcanzado el límite de texto especificado por el usuario. El usuario no puede escribir más texto. Para cambiar este límite, una aplicación debe enviar al control un nuevo mensaje [**EM \_ SETLIMITTEXT**](em-setlimittext.md) con un límite mayor.

Como ejemplo del uso de [**EM \_ SETLIMITTEXT**](em-setlimittext.md) y [EN \_ MAXTEXT,](en-maxtext.md)suponga que la aplicación debe limitar al usuario a no más de cuatro caracteres en un control de edición. La aplicación usaría **EM \_ SETLIMITTEXT para** especificar un límite de cuatro caracteres. Si el usuario intentara escribir un quinto carácter, el sistema enviaría un código de notificación EN MAXTEXT a \_ la aplicación.

## <a name="character-and-line-operations"></a>Operaciones de caracteres y líneas

Hay varios mensajes que devuelven información sobre los caracteres y las líneas de un control de edición. La mayoría de los mensajes devuelven un índice, normalmente un número de base cero, para hacer referencia a un carácter o una línea. Por ejemplo, en un control de edición de una sola línea que contiene n caracteres, el índice de línea es cero y los caracteres se indexan de cero a n-1. En un control de edición multilínea que contiene m líneas y n caracteres, las líneas se indexan de cero a m-1 y los caracteres se indexan de cero a n-1. Tenga en cuenta que la indexación de caracteres omite los saltos de línea.

Una aplicación puede determinar el número de caracteres de un control de edición enviando el mensaje [**\_ WM GETTEXTLENGTH**](/windows/desktop/winmsg/wm-gettextlength) al control de edición. Este mensaje devuelve la longitud, en caracteres (sin incluir el carácter nulo de terminación), del texto en un control de edición de una sola línea o de varias líneas. El [**mensaje EM \_ LINELENGTH**](em-linelength.md) devuelve la longitud, en caracteres, de una línea especificada por el índice de caracteres de un carácter de la línea. La longitud devuelta no incluye ningún carácter seleccionado. Una aplicación puede usar estos mensajes en un control de edición de una o varias líneas.

El [**mensaje EM \_ GETFIRSTVISIBLELINE**](em-getfirstvisibleline.md) devuelve el índice de base cero de la línea visible superior en un control de edición multilínea o el índice de base cero del primer carácter visible en un control de edición de una sola línea. Una aplicación puede copiar una línea de un control de edición a un búfer mediante el envío del [**mensaje EM \_ GETLINE**](em-getline.md) al control de edición. La línea se especifica mediante su índice de línea y la primera palabra del búfer receptor contiene el número máximo de bytes que se van a copiar en el búfer. El valor devuelto es el número de bytes copiados. Este mensaje también se puede usar en un control de edición de una o varias líneas.

Hay mensajes únicos disponibles para devolver la información sobre una línea en un control de edición multilínea. El [**mensaje EM \_ GETLINECOUNT**](em-getlinecount.md) devuelve el número de líneas de un control de edición. El [**mensaje EM \_ LINEFROMCHAR**](em-linefromchar.md) devuelve el índice de la línea que contiene un índice de caracteres especificado. El [**mensaje EM \_ LINEINDEX**](em-lineindex.md) devuelve el índice del primer carácter de una línea especificada.

## <a name="scrolling-text-in-an-edit-control"></a>Desplazamiento de texto en un control Edit

Para implementar el desplazamiento en un control de edición, puede usar los estilos de desplazamiento automático analizados en Editar tipos y estilos de control [,](about-edit-controls.md)o puede agregar explícitamente barras de desplazamiento al control de edición. Para agregar una barra de desplazamiento horizontal, use el estilo WS HSCROLL; para agregar una barra de desplazamiento vertical, use el estilo \_ [**WS \_ VSCROLL**](/windows/desktop/winmsg/window-styles). Un control de edición con barras de desplazamiento procesa sus propios mensajes de barra de desplazamiento. Para obtener información detallada sobre cómo agregar barras de desplazamiento para editar controles, vea [Barras de desplazamiento](scroll-bars.md).

El sistema proporciona tres mensajes que una aplicación puede enviar a un control de edición con barras de desplazamiento. El [**mensaje EM \_ LINESCROLL**](em-linescroll.md) puede desplazarse por un control de edición de varias líneas vertical y horizontalmente. El *parámetro lParam* especifica el número de líneas que se desplazarán verticalmente a partir de la línea actual y el parámetro *wParam* especifica el número de caracteres que se desplazarán horizontalmente, empezando por el carácter actual. El control de edición no confirma los mensajes de desplazamiento horizontal si tiene el estilo [**ES \_ CENTER**](edit-control-styles.md) o [**ES \_ RIGHT.**](edit-control-styles.md) El **mensaje EM \_ LINESCROLL** solo se aplica a los controles de edición multilínea.

El [**mensaje EM \_ SCROLL**](em-scroll.md) desplaza verticalmente un control de edición de varias líneas. El *parámetro wParam* especifica la acción de desplazamiento. El **mensaje EM \_ SCROLL** solo se aplica a los controles de edición multilínea. **EM \_ SCROLL** tiene el mismo efecto que el [**mensaje \_ VSCROLL de WM.**](wm-vscroll.md)

El [**mensaje EM \_ SCROLLCARET**](em-scrollcaret.md) desplaza el aviso a la vista en un control de edición.

## <a name="setting-tab-stops-and-margins"></a>Establecer tabulaciones y márgenes

Una aplicación puede establecer tabulaciones en un control de edición multilínea mediante el mensaje [**EM \_ SETTABSTOPS.**](em-settabstops.md) (El valor predeterminado para un tabulador es de ocho caracteres). Cuando una aplicación agrega texto al control de edición, los caracteres de tabulación del texto generan automáticamente espacio hasta la siguiente detenerse. El **mensaje \_ EM SETTABSTOPS** no hace que el sistema vuelva a dibujar el texto automáticamente. Para ello, una aplicación puede llamar a [**la función InvalidateRect.**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) El **mensaje EM \_ SETTABSTOPS** solo se aplica a los controles de edición multilínea.

Una aplicación puede establecer el ancho de los márgenes izquierdo y derecho de un control de edición mediante el mensaje [**\_ EM SETMARGINS.**](em-setmargins.md) Después de enviar este mensaje, el sistema vuelve a dibujar el control de edición para reflejar la nueva configuración de margen. Una aplicación puede recuperar el ancho del margen izquierdo o derecho mediante el envío del [**mensaje EM \_ GETMARGINS.**](em-getmargins.md) De forma predeterminada, los márgenes de control de edición se establecen lo suficientemente anchos como para dar cabida al mayor sobresalgo horizontal de caracteres (anchos abc negativos) para la fuente actual que se usa en el control de edición.

## <a name="concealing-user-input"></a>Ocultación de la entrada del usuario

Una aplicación puede usar un carácter de contraseña en un control de edición para ocultar la entrada del usuario. Cuando se establece un carácter de contraseña, se muestra en lugar de cada carácter que el usuario tipos. Cuando se quita un carácter de contraseña, el control muestra los caracteres que el usuario tipos. Si la aplicación crea un control de edición de una sola línea con el estilo [**ES \_ PASSWORD**](edit-control-styles.md), el carácter de contraseña predeterminado es un asterisco ( \* ). Una aplicación puede usar el mensaje [**EM \_ SETPASSWORDCHAR**](em-setpasswordchar.md) para quitar o definir un carácter de contraseña diferente y el mensaje [**EM \_ GETPASSWORDCHAR**](em-getpasswordchar.md) para recuperar el carácter de contraseña actual. Estos mensajes solo se aplican a controles de edición de una sola línea.

## <a name="using-integers"></a>Usar enteros

Hay dos funciones de conversión de enteros para controles de edición diseñados para contener solo números. La [**función SetDlgItemInt**](/windows/desktop/api/winuser/nf-winuser-setdlgitemint) crea la representación de cadena de un entero especificado (con o sin signo) y envía la cadena a un control de edición. **SetDlgItemInt** no devuelve ningún valor. La [**función GetDlgItemInt**](/windows/desktop/api/winuser/nf-winuser-getdlgitemint) crea un entero (con o sin signo) a partir de su representación de cadena en un control de edición. **GetDlgItemInt devuelve** el entero (o un valor de error).

## <a name="undoing-text-operations"></a>Operaciones de deshacer texto

Cada control de edición mantiene una marca de deshacer que indica si una aplicación puede invertir o deshacer la operación más reciente en el control de edición (por ejemplo, deshacer una eliminación de texto). El control de edición establece la marca de deshacer para indicar que la operación se puede deshacer y la restablece para indicar que la operación no se puede deshacer. Una aplicación puede determinar la configuración de la marca de deshacer enviando al control un [**mensaje EM \_ CANUNDO.**](em-canundo.md)

Una aplicación puede deshacer la operación más reciente enviando al control un [**mensaje EM \_ UNDO.**](em-undo.md) Una operación se puede deshacer siempre que no se produzca antes ninguna otra operación de control de edición. Por ejemplo, el usuario puede eliminar texto, reemplazar el texto (deshacer la eliminación) y, a continuación, eliminar el texto de nuevo (deshacer el reemplazo). El **mensaje EM \_ UNDO** se aplica a los controles de edición de línea única y multilínea y siempre funciona para los controles de edición de una sola línea.

Una aplicación puede restablecer la marca de deshacer de un control de edición enviando al control [**un mensaje EM \_ EMPTYUNDOBUFFER.**](em-emptyundobuffer.md) El sistema restablece automáticamente la marca de deshacer cada vez que un control de edición recibe un mensaje [**EM \_ SETHANDLE**](em-sethandle.md) [**o WM \_ SETTEXT.**](/windows/desktop/winmsg/wm-settext) La [**función SetDlgItemText**](/windows/desktop/api/winuser/nf-winuser-setdlgitemtexta) envía un **mensaje \_ SETTEXT de WM.**

## <a name="handling-wordwrap-and-line-breaks"></a>Controlar el ajuste de línea y los saltos de línea

Una aplicación puede usar funciones de wordwrap con controles de edición multilínea para buscar la palabra o fragmento de palabras que se debe ajustar a la línea siguiente. Con la función wordwrap predeterminada proporcionada por el sistema, las líneas siempre terminan en los espacios entre palabras. Una aplicación puede especificar su propia función de wordwrap si proporciona una función [*EditWordBreakProc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca) Wordwrap y envía al control de edición un [**mensaje EM \_ SETWORDBREAKPROC.**](em-setwordbreakproc.md) Una aplicación puede recuperar la dirección de la función Wordwrap actual enviando al control [**un mensaje EM \_ GETWORDBREAKPROC.**](em-getwordbreakproc.md)

Una aplicación puede dirigir un control de edición multilínea para agregar o quitar un carácter de salto de línea flexible (dos retornos de carro y un avance de línea) automáticamente al final de las líneas de texto encapsulado. Una aplicación puede activar o desactivar esta característica enviando al control de edición un [**mensaje EM \_ FMTLINES.**](em-fmtlines.md) Este mensaje solo se aplica a los controles de edición multilínea y no afecta a una línea que termina con un salto de línea duro (un retorno de carro y un avance de línea especificado por el usuario). También en los controles de edición multilínea, una aplicación puede especificar el estilo [**ES \_ WANTRETURN**](edit-control-styles.md) para solicitar que el sistema inserte un retorno de carro cuando el usuario presione la tecla ENTRAR en el control de edición.

## <a name="retrieving-points-and-characters"></a>Recuperar puntos y caracteres

Para determinar el carácter más cercano a un punto especificado en el área de cliente de un control de edición, envíe el mensaje [**\_ CHARFROMPOS**](em-charfrompos.md) EM al control. El mensaje devuelve el índice de caracteres y el índice de línea del carácter más cercano al punto. De forma similar, puede recuperar las coordenadas de área de cliente de un carácter especificado mediante el envío del [**\_ mensaje EM POSFROMCHAR.**](em-posfromchar.md) El mensaje devuelve las coordenadas x e y de la esquina superior izquierda del carácter especificado.

## <a name="autocompletion-of-strings"></a>Autocompletar de cadenas

Autocompletar expande las cadenas que se han especificado parcialmente en un control de edición en cadenas completas. Por ejemplo, cuando un usuario comienza a escribir una dirección URL en el control Edición de direcciones que se inserta en la barra de herramientas de Windows Internet Explorer, la función de autocompletar expande la cadena en una o varias direcciones URL completas que son coherentes con la cadena parcial existente. Una cadena de dirección URL parcial, como "mic", podría expandirse a https://www.microsoft.com "" o https://www.microsoft.com/windows "". La autocompletar se usa normalmente con controles de edición o con controles que tienen un control de edición incrustado.

Para obtener más información, consulte la documentación de la interfaz [**IAutoComplete**](/windows/desktop/api/shldisp/nn-shldisp-iautocomplete) [**e IAutoComplete2.**](/windows/desktop/api/shldisp/nn-shldisp-iautocomplete2)

## <a name="complex-script-in-edit-controls"></a>Script complejo en controles de edición

Un *script complejo* es un lenguaje cuyo formato impreso no se ha diseñado de una manera sencilla. Por ejemplo, un script complejo puede permitir la representación bidireccional, la forma contextual de glifos o la combinación de caracteres. Los controles de edición estándar se han ampliado para admitir texto multilingüe y scripts complejos. Esto incluye no solo la entrada y la presentación, sino también el movimiento correcto del cursor sobre los clústeres de caracteres (por ejemplo, en el script tailandés y devaplacei).

Una aplicación bien escrita recibe esta compatibilidad automáticamente, sin modificaciones. De nuevo, debe considerar la posibilidad de agregar compatibilidad con el orden de lectura de derecha a izquierda y la alineación derecha. En este caso, alterne las marcas de estilo extendido de la ventana de control de edición para controlar estos atributos, como se muestra en el ejemplo siguiente.


```
// ID_EDITCONTROL is the control ID in the resource file.
HANDLE hWndEdit = GetDlgItem(hDlg, ID_EDITCONTROL);
LONG lAlign = GetWindowLong(hWndEdit, GWL_EXSTYLE) ;

// To toggle alignment
lAlign ^= WS_EX_RIGHT ;

// To toggle reading order
lAlign ^= WS_EX_RTLREADING ;
```



Después de establecer **el valor lAlign,** habilite la nueva pantalla estableciendo el estilo extendido de la ventana de control de edición como se muestra a continuación.


```
// This assumes your edit control is in a dialog box. If not, 
// get the edit control handle from another source.

SetWindowLong(hWndEdit, GWL_EXSTYLE, lAlign);
InvalidateRect(hWndEdit, NULL, FALSE);
```



Uniscribe es otro conjunto de funciones que proporcionan un control preciso para procesar scripts complejos. Para obtener más información, vea [Uniscribe](/windows/desktop/Intl/uniscribe).

 

 