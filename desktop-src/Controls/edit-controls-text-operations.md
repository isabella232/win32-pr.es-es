---
title: Editar operaciones de texto de control
description: El sistema procesa automáticamente todas las operaciones de texto iniciadas por el usuario y notifica a la aplicación cuando se completan las operaciones.
ms.assetid: 9af3a1bc-4c87-4cc9-966d-50742be7c811
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9640616cf70b9a2933ef9d4c3fdb2accbfdcabf0
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078431"
---
# <a name="edit-control-text-operations"></a>Editar operaciones de texto de control

El sistema procesa automáticamente todas las operaciones de texto iniciadas por el usuario y notifica a la aplicación cuando se completan las operaciones.

En los temas siguientes se describen las operaciones de texto iniciadas por el usuario y la respuesta de la aplicación:

-   [Seleccionar un control de edición](#selecting-an-edit-control)
-   [Establecer y recuperar texto](#setting-and-retrieving-text)
-   [Seleccionar texto](#selecting-text)
-   [Reemplazar texto](#replacing-text)
-   [Cambiar la fuente utilizada por un control de edición](#changing-the-font-used-by-an-edit-control)
-   [Cortar copiar operaciones de pegar y borrar](#cut-copy-paste-and-clear-operations)
-   [Modificar texto](#modifying-text)
-   [Limitar el texto escrito por el usuario](#limiting-user-entered-text)
-   [Operaciones de carácter y línea](#character-and-line-operations)
-   [Desplazamiento de texto en un control de edición](#scrolling-text-in-an-edit-control)
-   [Establecer los márgenes y las tabulaciones](#setting-tab-stops-and-margins)
-   [Ocultar la entrada del usuario](#concealing-user-input)
-   [Usar enteros](#using-integers)
-   [Deshacer operaciones de texto](#undoing-text-operations)
-   [Controlar los saltos de línea y WordWrap](#handling-wordwrap-and-line-breaks)
-   [Recuperar puntos y caracteres](#retrieving-points-and-characters)
-   [Autocompletar cadenas](#autocompletion-of-strings)
-   [Script complejo en controles de edición](#complex-script-in-edit-controls)

## <a name="selecting-an-edit-control"></a>Seleccionar un control de edición

El usuario puede seleccionar un control de edición haciendo clic en él con el mouse o presionando la tecla TAB para desplace hasta él. El método de tabulación forma parte de una interfaz de teclado predefinida que el sistema proporciona. Para obtener una descripción completa de esta interfaz, vea [cuadros de diálogo](/windows/desktop/dlgbox/dialog-boxes). Cuando el usuario selecciona un control de edición, el sistema proporciona al control el foco de teclado (vea "foco y activación del teclado" en acerca de la [entrada del teclado](/windows/desktop/inputdev/about-keyboard-input)) y resalta el texto mediante el vídeo inverso.

## <a name="setting-and-retrieving-text"></a>Establecer y recuperar texto

Una aplicación puede establecer el texto de un control de edición mediante la función [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta) , la función [**SetDlgItemText**](/windows/desktop/DevNotes/-setdlgitemtext) o mediante el envío de un mensaje de [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) .

Para recuperar todo el texto de un control de edición, utilice primero la función [**GetWindowTextLength**](/windows/desktop/api/winuser/nf-winuser-getwindowtextlengtha) o el mensaje de [**\_ GETTEXTLENGTH de WM**](/windows/desktop/winmsg/wm-gettextlength) para determinar el tamaño del búfer necesario para contener el texto. A continuación, recupere el texto con la función [**GetWindowText**](/windows/desktop/DevNotes/-getwindowtext) , la función [**GetDlgItemText**](/windows/desktop/api/winuser/nf-winuser-getdlgitemtexta) o el mensaje de [**\_ GETTEXT de WM**](/windows/desktop/winmsg/wm-gettext) .

## <a name="selecting-text"></a>Seleccionar texto

Después de seleccionar un control de edición, el usuario puede seleccionar texto en el control mediante el mouse o el teclado. Una aplicación puede recuperar las posiciones de caracteres inicial y final de la selección actual en un control de edición mediante el envío de un mensaje [**\_ GETSEL em**](em-getsel.md) . El valor devuelto para la posición final es uno mayor que el último carácter de la selección (es decir, la posición del primer carácter que sigue al último carácter seleccionado).

Una aplicación también puede seleccionar texto en un control de edición enviando el control un [**mensaje \_ SETSEL em**](em-setsel.md) con los índices de carácter inicial y final para la selección. Por ejemplo, la aplicación puede usar **em \_ SETSEL** con [**em \_ REPLACESEL**](em-replacesel.md) para eliminar texto de un control de edición.

Estos tres mensajes se aplican a los controles de edición de línea única y multilínea.

## <a name="replacing-text"></a>Reemplazar texto

Una aplicación puede reemplazar el texto seleccionado en un control de edición mediante el envío de un mensaje [**\_ REPLACESEL em**](em-replacesel.md) con un puntero al texto de reemplazo. Si no hay ninguna selección actual, **em \_ REPLACESEL** inserta el texto de reemplazo en el punto de inserción. La aplicación puede recibir un código de notificación [en \_ ERRSPACE](en-errspace.md) si el texto de reemplazo supera la memoria disponible. Este mensaje se aplica a los controles de edición de línea única y multilínea.

Una aplicación puede usar [**em \_ REPLACESEL**](em-replacesel.md) para reemplazar parte del texto de un control de edición o la función [**SetDlgItemText**](/windows/desktop/api/winuser/nf-winuser-setdlgitemtexta) para reemplazarlo todo.

## <a name="changing-the-font-used-by-an-edit-control"></a>Cambiar la fuente utilizada por un control de edición

Una aplicación puede cambiar la fuente que usa un control de edición mediante el envío del mensaje de [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont) . La mayoría de las aplicaciones lo hacen al procesar el mensaje de [**\_ INITDIALOG de WM**](/windows/desktop/dlgbox/wm-initdialog) . Al cambiar la fuente no se cambia el tamaño del control de edición. es posible que las aplicaciones que envían el mensaje de **WM de WM \_** tengan que recuperar las métricas de fuente del texto y volver a calcular el tamaño del control de edición. Para obtener más información sobre fuentes y métricas de fuentes, vea [fuentes y texto](/windows/desktop/gdi/fonts-and-text).

## <a name="cut-copy-paste-and-clear-operations"></a>Cortar copiar operaciones de pegar y borrar

Hay cuatro mensajes para mover texto entre un control de edición y el portapapeles. El mensaje de [**\_ copia de WM**](/windows/desktop/dataxchg/wm-copy) copia la selección actual (si existe) de un control de edición en el portapapeles sin eliminarla del control de edición. El mensaje de [**\_ corte de WM**](/windows/desktop/dataxchg/wm-cut) elimina la selección actual (si existe) en el control de edición y copia el texto eliminado en el portapapeles. El mensaje de [**\_ borrado de WM**](/windows/desktop/dataxchg/wm-clear) elimina la selección actual (si existe) de un control de edición, pero no lo copia en el portapapeles (a menos que el usuario presione la tecla Mayús). El mensaje de [**\_ pegado de WM**](/windows/desktop/dataxchg/wm-paste) copia texto del portapapeles en un control de edición en el punto de inserción. Estos cuatro mensajes se aplican a los controles de edición de línea única y multilínea.

Microsoft Windows NT 4,0 y versiones posteriores: un control de edición incluye un menú contextual integrado que facilita al usuario el movimiento de texto entre el control de edición y el portapapeles. El menú contextual aparece cuando el usuario hace clic con el botón secundario en el control. Los comandos del menú contextual incluyen **Deshacer**, **cortar**, **copiar**, **pegar**, **eliminar** y **seleccionar todo**.

## <a name="modifying-text"></a>Modificar texto

El usuario puede seleccionar, eliminar o desplace texto en un control de edición. El sistema mantiene una marca interna para cada control de edición que indica si se ha modificado el contenido del control. El sistema borra esta marca cuando crea el control y establece la marca cada vez que se modifica el texto del control. Una aplicación puede recuperar la marca de modificación mediante el envío de un mensaje [**\_ GETMODIFY em**](em-getmodify.md) . A continuación, la aplicación puede establecer o borrar la marca de modificación mediante el envío de un mensaje de [**\_ SETMODIFY em**](em-setmodify.md) . Estos mensajes se aplican a los controles de edición de línea única y multilínea.

## <a name="limiting-user-entered-text"></a>Limitar el texto escrito por el usuario

El límite predeterminado para la cantidad de texto que un usuario puede escribir en un control de edición es de 32 KB. Una aplicación puede cambiar el límite predeterminado mediante el envío de un [**mensaje \_ SETLIMITTEXT em**](em-setlimittext.md) . Este mensaje establece un límite máximo para el número de bytes que el usuario puede escribir en un control de edición, pero no afecta al texto que ya está en el control cuando el mensaje se envió o se copia texto en el control mediante la función [**SetDlgItemText**](/windows/desktop/api/winuser/nf-winuser-setdlgitemtexta) o el mensaje de [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) . Por ejemplo, supongamos que la aplicación utiliza la función **SetDlgItemText** para colocar 500 bytes en un control de edición y el usuario también introduce 500 bytes (1.000 bytes en total). Si la aplicación envía un mensaje **\_ SETLIMITTEXT em** que limita el texto especificado por el usuario a 300 bytes, los 1.000 bytes que ya están en el control de edición permanecen allí y el usuario no puede agregar más texto. Por otro lado, si la aplicación envía un mensaje **\_ SETLIMITTEXT em** que limita el texto especificado por el usuario a 1.300 bytes, se conservan los 1.000 bytes, pero el usuario puede Agregar 300 más bytes.

Cuando el usuario alcanza el límite de caracteres de un control de edición, el sistema envía a la aplicación un mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) que contiene un código de notificación [en \_ MAXTEXT](en-maxtext.md) . Este código de notificación no significa que se haya agotado la memoria, pero se ha alcanzado el límite para el texto escrito por el usuario; el usuario no puede escribir más texto. Para cambiar este límite, una aplicación debe enviar el control a un nuevo mensaje [**\_ SETLIMITTEXT em**](em-setlimittext.md) con un límite superior.

Como ejemplo del uso de [**em \_ SETLIMITTEXT**](em-setlimittext.md) y [en \_ MAXTEXT](en-maxtext.md), supongamos que la aplicación debe limitar el usuario a un máximo de cuatro caracteres en un control de edición. La aplicación usaría **em \_ SETLIMITTEXT** para especificar un límite de cuatro caracteres. Si el usuario ha intentado escribir un quinto carácter, el sistema enviará un \_ código de notificación en MAXTEXT a la aplicación.

## <a name="character-and-line-operations"></a>Operaciones de carácter y línea

Hay varios mensajes que devuelven información sobre los caracteres y las líneas de un control de edición. La mayoría de los mensajes devuelven un índice, normalmente un número basado en cero, para hacer referencia a un carácter o una línea. Por ejemplo, en un control de edición de una sola línea que contiene n caracteres, el índice de línea es cero y los caracteres se indizan de cero a n-1. En un control de edición multilínea que contiene las líneas m y n caracteres, las líneas se indizan de cero a m-1 y los caracteres se indizan de cero a n-1. Tenga en cuenta que la indización de caracteres omite los saltos de línea.

Una aplicación puede determinar el número de caracteres en un control de edición mediante el envío del mensaje de [**WM \_ GETTEXTLENGTH**](/windows/desktop/winmsg/wm-gettextlength) al control de edición. Este mensaje devuelve la longitud, en caracteres (sin incluir el carácter nulo de terminación), del texto de un control de edición de línea única o multilínea. El [**mensaje \_ LINELENGTH em**](em-linelength.md) devuelve la longitud, en caracteres, de una línea especificada por el índice de carácter de un carácter de la línea. La longitud devuelta no incluye ningún carácter seleccionado. Una aplicación puede utilizar estos mensajes en un control de edición de línea única o multilínea.

El [**mensaje \_ GETFIRSTVISIBLELINE em**](em-getfirstvisibleline.md) devuelve el índice de base cero de la línea visible superior en un control de edición multilínea, o el índice de base cero del primer carácter visible en un control de edición de una sola línea. Una aplicación puede copiar una línea de un control de edición en un búfer enviando el [**mensaje \_ GETLINE em**](em-getline.md) al control de edición. La línea se especifica mediante su índice de línea y la primera palabra del búfer de recepción contiene el número máximo de bytes que se van a copiar en el búfer. El valor devuelto es el número de bytes copiados. Este mensaje también puede usarse en un control de edición de una sola línea o multilínea.

Hay mensajes únicos disponibles para devolver la información sobre una línea en un control de edición multilínea. El [**mensaje \_ GETLINECOUNT em**](em-getlinecount.md) devuelve el número de líneas de un control de edición. El [**mensaje \_ LINEFROMCHAR em**](em-linefromchar.md) devuelve el índice de la línea que contiene un índice de carácter especificado. El [**mensaje \_ LINEINDEX em**](em-lineindex.md) devuelve el índice del primer carácter de una línea especificada.

## <a name="scrolling-text-in-an-edit-control"></a>Desplazamiento de texto en un control de edición

Para implementar el desplazamiento en un control de edición, puede usar los estilos de desplazamiento automático descritos en [Editar tipos y estilos de control](about-edit-controls.md), o puede Agregar explícitamente barras de desplazamiento al control de edición. Para agregar una barra de desplazamiento horizontal, use el estilo WS \_ HSCROLL; para agregar una barra de desplazamiento vertical, use el estilo [**WS \_ VSCROLL**](/windows/desktop/winmsg/window-styles). Un control de edición con barras de desplazamiento procesa sus propios mensajes de barra de desplazamiento. Para obtener información detallada sobre cómo agregar barras de desplazamiento a controles de edición, vea [barras de desplazamiento](scroll-bars.md).

El sistema proporciona tres mensajes que una aplicación puede enviar a un control de edición con barras de desplazamiento. El [**mensaje \_ LINESCROLL em**](em-linescroll.md) puede desplazar un control de edición multilínea tanto vertical como horizontalmente. El parámetro *lParam* especifica el número de líneas que se va a desplazar verticalmente a partir de la línea actual y el parámetro *wParam* especifica el número de caracteres que se va a desplazar horizontalmente, empezando por el carácter actual. El control de edición no confirma los mensajes de desplazamiento horizontal si tiene el estilo [**\_ derecho**](edit-control-styles.md) [**\_ Center**](edit-control-styles.md) o es. El **mensaje \_ LINESCROLL em** se aplica solo a los controles de edición multilínea.

El mensaje de [**\_ desplazamiento em**](em-scroll.md) desplaza verticalmente un control de edición de varias líneas. El parámetro *wParam* especifica la acción de desplazamiento. El mensaje de **\_ desplazamiento em** se aplica solo a los controles de edición multilínea. **Em \_ El desplazamiento** tiene el mismo efecto que el mensaje [**\_ VSCROLL de WM**](wm-vscroll.md) .

El [**mensaje \_ SCROLLCARET em**](em-scrollcaret.md) desplaza el símbolo de intercalación en la vista de un control de edición.

## <a name="setting-tab-stops-and-margins"></a>Establecer los márgenes y las tabulaciones

Una aplicación puede establecer paradas de tabulación en un control de edición multilínea mediante el mensaje [**\_ SETTABSTOPS em**](em-settabstops.md) . (El valor predeterminado para una detención de tabulación es de ocho caracteres). Cuando una aplicación agrega texto al control de edición, los caracteres de tabulación del texto generan automáticamente espacio hasta la siguiente posición de tabulación. El **mensaje \_ SETTABSTOPS em** no hace que el sistema vuelva a dibujar el texto automáticamente. Para ello, una aplicación puede llamar a la función [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) . El **mensaje \_ SETTABSTOPS em** se aplica solo a los controles de edición multilínea.

Una aplicación puede establecer el ancho de los márgenes izquierdo y derecho de un control de edición mediante el [**mensaje \_ SETMARGINS em**](em-setmargins.md) . Después de enviar este mensaje, el sistema vuelve a dibujar el control de edición para reflejar la nueva configuración de márgenes. Una aplicación puede recuperar el ancho del margen izquierdo o derecho mediante el envío del [**mensaje \_ GETMARGINS em**](em-getmargins.md) . De forma predeterminada, los márgenes del control de edición se establecen en el ancho suficiente para alojar el voladizo horizontal de mayor carácter (ancho ABC negativo) de la fuente actual que se usa en el control de edición.

## <a name="concealing-user-input"></a>Ocultar la entrada del usuario

Una aplicación puede usar un carácter de contraseña en un control de edición para ocultar los datos proporcionados por el usuario. Cuando se establece un carácter de contraseña, se muestra en lugar de cada carácter que el usuario escribe. Cuando se quita un carácter de contraseña, el control muestra los caracteres que el usuario escribe. Si la aplicación crea un control de edición de una sola línea con [**la \_ contraseña**](edit-control-styles.md)del estilo es, el carácter de contraseña predeterminado es un asterisco ( \* ). Una aplicación puede usar el mensaje [**em \_ SETPASSWORDCHAR**](em-setpasswordchar.md) para quitar o definir un carácter de contraseña diferente y el mensaje [**\_ GETPASSWORDCHAR em**](em-getpasswordchar.md) para recuperar el carácter de contraseña actual. Estos mensajes solo se aplican a los controles de edición de una sola línea.

## <a name="using-integers"></a>Usar enteros

Hay dos funciones de conversión de enteros para los controles de edición diseñados para contener solo números. La función [**SetDlgItemInt**](/windows/desktop/api/winuser/nf-winuser-setdlgitemint) crea la representación de cadena de un entero especificado (con o sin signo) y envía la cadena a un control de edición. **SetDlgItemInt** no devuelve ningún valor. La función [**GetDlgItemInt**](/windows/desktop/api/winuser/nf-winuser-getdlgitemint) crea un entero (con o sin signo) a partir de su representación de cadena en un control de edición. **GetDlgItemInt** devuelve el entero (o un valor de error).

## <a name="undoing-text-operations"></a>Deshacer operaciones de texto

Cada control de edición mantiene una marca de deshacer que indica si una aplicación puede revertir o deshacer la operación más reciente en el control de edición (deshacer una eliminación de texto, por ejemplo). El control de edición establece la marca de deshacer para indicar que la operación se puede deshacer y restablece para indicar que la operación no se puede deshacer. Una aplicación puede determinar el valor de la marca de deshacer mediante el envío de un mensaje de [**\_ CANUNDO de EM**](em-canundo.md) .

Una aplicación puede deshacer la operación más reciente mediante el envío de un mensaje de [**\_ Deshacer de EM**](em-undo.md) . Una operación se puede deshacer si no se produce ninguna otra operación de control de edición. Por ejemplo, el usuario puede eliminar texto, reemplazar el texto (deshacer la eliminación) y, a continuación, eliminar el texto de nuevo (deshacer el reemplazo). El mensaje de **\_ Deshacer em** se aplica a los controles de edición de línea única y multilínea y siempre funciona para los controles de edición de una sola línea.

Una aplicación puede restablecer el indicador de deshacer de un control de edición mediante el envío de un mensaje [**\_ EMPTYUNDOBUFFER em**](em-emptyundobuffer.md) . El sistema restablece automáticamente la marca de deshacer cada vez que un control de edición recibe un mensaje [**em \_ SETHANDLE**](em-sethandle.md) o [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) . La función [**SetDlgItemText**](/windows/desktop/api/winuser/nf-winuser-setdlgitemtexta) envía un mensaje de **WM \_ SETTEXT** .

## <a name="handling-wordwrap-and-line-breaks"></a>Controlar los saltos de línea y WordWrap

Una aplicación puede usar funciones de ajuste de línea con controles de edición multilínea para buscar la palabra o fragmento de Word que debe ajustarse a la línea siguiente. Con la función de ajuste de línea predeterminada proporcionada por el sistema, las líneas siempre terminan en los espacios entre las palabras. Una aplicación puede especificar su propia función WordWrap proporcionando una función WordWrap [*EditWordBreakProc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca) y enviando el control de edición de un mensaje [**\_ SETWORDBREAKPROC em**](em-setwordbreakproc.md) . Una aplicación puede recuperar la dirección de la función WordWrap actual mediante el envío de un [**mensaje \_ GETWORDBREAKPROC em**](em-getwordbreakproc.md) .

Una aplicación puede dirigir un control de edición multilínea para agregar o quitar un carácter de salto de línea flexible (dos retornos de carro y un avance de línea) automáticamente al final de las líneas de texto ajustado. Una aplicación puede activar o desactivar esta característica mediante el envío de un mensaje de [**\_ FMTLINES em**](em-fmtlines.md) a un control de edición. Este mensaje solo se aplica a los controles de edición de varias líneas y no afecta a una línea que termina con un salto de línea rígido (un retorno de carro y un avance de línea introducidos por el usuario). Además, en los controles de edición multilínea, una aplicación puede especificar el estilo [**es \_ WANTRETURN**](edit-control-styles.md) para solicitar que el sistema Inserte un retorno de carro cuando el usuario presione la tecla entrar en el control de edición.

## <a name="retrieving-points-and-characters"></a>Recuperar puntos y caracteres

Para determinar el carácter más cercano a un punto especificado en el área cliente de un control de edición, envíe el mensaje [**\_ CHARFROMPOS em**](em-charfrompos.md) al control. El mensaje devuelve el índice de carácter y el índice de línea del carácter más próximo al punto. Del mismo modo, puede recuperar las coordenadas del área de cliente de un carácter especificado enviando el mensaje [**\_ POSFROMCHAR em**](em-posfromchar.md) . El mensaje devuelve las coordenadas x e y de la esquina superior izquierda del carácter especificado.

## <a name="autocompletion-of-strings"></a>Autocompletar cadenas

La finalización automática expande las cadenas que se han especificado parcialmente en un control de edición en cadenas completas. Por ejemplo, cuando un usuario comienza a escribir una dirección URL en el control de edición de direcciones que está incrustado en la barra de herramientas de Windows Internet Explorer, la finalización automática expande la cadena en una o más direcciones URL completas que son coherentes con la cadena parcial existente. Una cadena de dirección URL parcial como "MIC" podría expandirse a " https://www.microsoft.com " o " https://www.microsoft.com/windows ". La finalización automática se usa normalmente con controles de edición o con controles que tienen un control de edición incrustado.

Para obtener más información, consulte la documentación de la interfaz de [**IAutoComplete**](/windows/desktop/api/shldisp/nn-shldisp-iautocomplete) y [**IAutoComplete2**](/windows/desktop/api/shldisp/nn-shldisp-iautocomplete2) .

## <a name="complex-script-in-edit-controls"></a>Script complejo en controles de edición

Un *script complejo* es un lenguaje cuyo formulario impreso no está diseñado de forma sencilla. Por ejemplo, un script complejo puede permitir la representación bidireccional, el modelado de glifos o la combinación de caracteres. Los controles de edición estándar se han ampliado para admitir texto multilingüe y scripts complejos. Esto incluye no solo la entrada y la presentación, sino también el movimiento del cursor en los clústeres de caracteres (en el script tailandés y Devanagari, por ejemplo).

Una aplicación bien escrita recibe esta compatibilidad automáticamente, sin modificaciones. De nuevo, considere la posibilidad de agregar compatibilidad con el orden de lectura de derecha a izquierda y la alineación a la derecha. En este caso, alterne las marcas de estilo extendido de la ventana Editar control para controlar estos atributos, tal y como se muestra en el ejemplo siguiente.


```
// ID_EDITCONTROL is the control ID in the resource file.
HANDLE hWndEdit = GetDlgItem(hDlg, ID_EDITCONTROL);
LONG lAlign = GetWindowLong(hWndEdit, GWL_EXSTYLE) ;

// To toggle alignment
lAlign ^= WS_EX_RIGHT ;

// To toggle reading order
lAlign ^= WS_EX_RTLREADING ;
```



Después de establecer el valor de **lAlign** , habilite la nueva presentación estableciendo el estilo extendido de la ventana de control de edición como se indica a continuación.


```
// This assumes your edit control is in a dialog box. If not, 
// get the edit control handle from another source.

SetWindowLong(hWndEdit, GWL_EXSTYLE, lAlign);
InvalidateRect(hWndEdit, NULL, FALSE);
```



Uniscribe es otro conjunto de funciones que proporcionan un control preciso para procesar scripts complejos. Para obtener más información, vea [Uniscribe](/windows/desktop/Intl/uniscribe).

 

 