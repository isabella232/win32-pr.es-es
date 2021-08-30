---
title: Acerca de los controles selectores de fecha y hora
description: Un control selector de fecha y hora (DTP) proporciona una interfaz sencilla e intuitiva a través de la cual intercambiar información de fecha y hora con un usuario.
ms.assetid: 6749c3ae-2c52-4183-ac4e-68ca7ebf1e13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f267d5cc5fdfe3000988ec7696442db736cc30d098b20d9514a098f6a26e42d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920504"
---
# <a name="about-date-and-time-picker-controls"></a>Acerca de los controles selectores de fecha y hora

Un control selector de fecha y hora *(DTP)* proporciona una interfaz sencilla e intuitiva a través de la cual intercambiar información de fecha y hora con un usuario. Por ejemplo, con un control DTP, puede pedir al usuario que escriba una fecha y, a continuación, recuperar fácilmente la selección.

Se tratan los temas siguientes:

-   [Selector de fecha y hora Interfaz de usuario](#date-and-time-picker-user-interface)
-   [Estilos y formatos de control del selector de fecha y hora](#date-and-time-picker-control-styles-and-formats)
    -   [Formatos preestablecidos](#preset-formats)
    -   [Formatos personalizados](#custom-formats)
    -   [Cadenas de formato](#format-strings)
    -   [Campos de devolución de llamada](#callback-fields)
-   [Mensajes de notificación de control de selector de fecha y hora](#date-and-time-picker-control-notification-messages)
-   [Temas relacionados](#related-topics)

> [!Note]
> Windows no admite fechas anteriores a la 1601. Consulte la [**estructura FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) para obtener más información.
>
> El control se basa en el calendario gregoriano, que se introdujo en 1753. No calculará las fechas coherentes con el calendario de Maya.

## <a name="date-and-time-picker-user-interface"></a>Selector de fecha y hora Interfaz de usuario

El área de cliente de un control selector de fecha y hora (DTP) muestra información de fecha y hora, o ambas, y actúa como la interfaz a través de la cual los usuarios modifican la información. La fecha se puede seleccionar desde un calendario o mediante un control de arriba a abajo; la hora se puede cambiar escribiendo en campos definidos por las [cadenas](#format-strings)de formato del control . Opcionalmente, el control muestra una casilla. Cuando se comprueba, se puede recuperar el valor del control ; De lo contrario, se considera que el control no está inicializado.

En la ilustración siguiente se muestra una ventana que contiene tres controles de selector de fecha. El primer control de selector de fecha se creó con el estilo [**DTS \_ SHOWNONE,**](date-and-time-picker-control-styles.md) el segundo con el estilo [**\_ UPDOWN**](date-and-time-picker-control-styles.md) de DTS y el tercero sin estilos especiales. En el tercer control, el usuario ha hecho clic en la flecha abajo para mostrar el calendario.

![captura de pantalla de una ventana que muestra tres estilos de controles de selector de fecha](images/dtpdatepick.png)

En la ilustración siguiente se muestra una ventana con tres controles que contienen la hora.

El primer control se ha creado con el estilo [**\_ TIMEFORMAT de DTS**](date-and-time-picker-control-styles.md) y muestra la hora en la hora predeterminada, que consta de cuatro campos. El usuario puede escribir un valor válido en cualquiera de estos campos o seleccionar el campo y cambiar el valor mediante el control o las teclas de flecha hacia abajo.

El segundo control muestra un conjunto de formato personalizado mediante [**DateTime \_ SetFormat**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setformat). Al igual que con el primer control, el usuario puede cambiar los campos de tiempo escribiendo o usando teclas de dirección. El día de la semana se puede cambiar seleccionando una fecha del calendario que se abre cuando el usuario hace clic en la flecha abajo.

El tercer control muestra cómo se puede agregar texto arbitrario al control . El usuario puede seleccionar una hora (de 1 a 24) escribiendo, usando las teclas de dirección o usando el control de arriba abajo.

![captura de pantalla de una ventana que muestra tres controles que contienen el tiempo](images/dtpdatetimepick.png)

El control DTP actualiza automáticamente la información interna en función de la entrada del usuario. El control reconoce lo siguiente como entrada válida.



| Categoría de entrada | Descripción                                                                                                                                                                                                                                                                                                                                                                  |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Teclas de dirección     | El control acepta teclas de dirección para navegar por los campos del control y cambiar los valores. El usuario puede presionar las teclas o para desplazarse por el control Si el usuario intenta pasar más allá del último campo en una dirección determinada, el foco del teclado "se ajusta" al campo en el lado opuesto del control. Las claves y cambian los valores del campo actual de forma incremental. |
| Fin y inicio   | El control acepta las claves virtuales VK END y VK HOME para cambiar el valor del campo actual a sus límites superior \_ \_ e inferior, respectivamente.                                                                                                                                                                                                                          |
| Claves de función  | La clave activa el modo de edición. La clave hace que el control muestre un control de calendario de mes desplegable (al presionar también hace esto).                                                                                                                                                                                                                                          |
| Números        | El control acepta entradas numéricas en segmentos de dos caracteres. Si el valor especificado por el usuario no es válido (como establecer el mes en 14), el control lo rechaza y restablece la presentación al valor anterior.                                                                                                                                                                |
| Más y menos | El control acepta las claves virtuales VK ADD y VK SUBTRACT del teclado numérico para incrementar y disminuir el valor \_ \_ en el campo actual.                                                                                                                                                                                                                             |



 

Los controles DTP que no usan el [**estilo \_ UPDOWN de DTS**](date-and-time-picker-control-styles.md) muestran un botón de flecha. Si el usuario hace clic en este botón, se reduce un control de calendario mensual. El usuario puede seleccionar una fecha específica haciendo clic en un área del calendario.

## <a name="date-and-time-picker-control-styles-and-formats"></a>Estilos y formatos de control del selector de fecha y hora

Los controles selector de fecha y hora (DTP) tienen varios estilos de [control](date-and-time-picker-control-styles.md) selector de fecha y hora que determinan la apariencia y el comportamiento de un control. Especifique el estilo al crear el control con el *parámetro dwStyle* [**de CreateWindowEx.**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) Para recuperar o cambiar el estilo de la ventana después de crear el control, use [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) y [**SetWindowLong.**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)

### <a name="preset-formats"></a>Formatos preestablecidos

Hay tres formatos preestablecidos disponibles para mostrar la fecha y otro para mostrar la hora. Para establecer estos formatos, elija uno de los siguientes estilos de ventana.



|   Formato                                                                                                    |   Descripción                                                         |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| [**DTS \_ LONGDATEFORMAT**](date-and-time-picker-control-styles.md)                 | La pantalla tendrá el siguiente aspecto: "Viernes, 19 de abril de 1996".      |
| [**DTS \_ SHORTDATEFORMAT**](date-and-time-picker-control-styles.md)               | La pantalla tendrá el siguiente aspecto: "19/4/96".                     |
| [**DTS \_ SHORTDATECENTURYFORMAT**](date-and-time-picker-control-styles.md) | **Versión 5.80.** La pantalla tendrá el siguiente aspecto: "19/4/1996". |
| [**DTS \_ TIMEFORMAT**](date-and-time-picker-control-styles.md)                         | La pantalla tendrá el siguiente aspecto: "5:31:42 p. m.".                  |



 

### <a name="custom-formats"></a>Formatos personalizados

Un control DTP se basa en una cadena de formato para determinar cómo mostrará campos de información. Si los formatos preestablecidos no son suficientes, puede crear un formato personalizado definiendo su propia cadena de formato. Los formatos personalizados proporcionan mayor flexibilidad para una aplicación. Permiten especificar el orden en el que el control mostrará campos de información. Puede incluir texto del cuerpo, así como campos de devolución de llamada para solicitar información al usuario. Una vez creada la cadena, se asigna al control DTP con un [**mensaje \_ SETFORMAT de DTM.**](dtm-setformat.md)

### <a name="format-strings"></a>Cadenas de formato

Una cadena de formato DTP consta de una serie de elementos que representan un fragmento de información determinado y definen su formato de presentación. Los elementos se mostrarán en el orden en que aparecen en la cadena de formato.

Los elementos de formato de fecha y hora se reemplazarán por la fecha y hora reales. Se definen mediante los siguientes grupos de caracteres.



| Elemento | Descripción                                                                       |
|---------|-----------------------------------------------------------------------------------|
| "d"     | El día de uno o dos dígitos.                                                        |
| "dd"    | Día de dos dígitos. Los valores de día de un solo dígito van precedidos de un cero.                |
| "ddd"   | Abreviatura del día de la semana de tres caracteres.                                         |
| "dddd"  | Nombre completo del día de la semana.                                                            |
| "h"     | Hora de uno o dos dígitos en formato de 12 horas.                                     |
| "hh"    | Hora de dos dígitos en formato de 12 horas. Los valores de un solo dígito van precedidos de un cero. |
| "H"     | Hora de uno o dos dígitos en formato de 24 horas.                                     |
| "HH"    | Hora de dos dígitos en formato de 24 horas. Los valores de un solo dígito van precedidos de un cero. |
| "m"     | Minuto de uno o dos dígitos.                                                     |
| "mm"    | Minuto de dos dígitos. Los valores de un solo dígito van precedidos de un cero.                 |
| "M"     | Número de mes de uno o dos dígitos.                                               |
| "MM"    | Número de mes de dos dígitos. Los valores de un solo dígito van precedidos de un cero.           |
| "MMM"   | Abreviatura del mes de tres caracteres.                                           |
| "MMMM"  | Nombre completo del mes.                                                              |
| "t"     | La abreviatura am/PM de una letra (es decir, AM se muestra como "A").              |
| "tt"    | La abreviatura de AM/PM de dos letras (es decir, AM se muestra como "AM").             |
| "yy"    | Los dos últimos dígitos del año (es decir, 1996 se mostrarían como "96").       |
| "yyyy"  | El año completo (es decir, 1996 se mostraría como "1996").                       |



 

Para que la información sea más legible, puede agregar texto del cuerpo a la cadena de formato si la incluye entre comillas simples. No es necesario entrecomillar espacios ni signos de puntuación.

> [!Note]  
> Los caracteres sin formato que no estén delimitados por comillas simples darán lugar a una presentación imprevisible por parte del control DTP.

Por ejemplo, para mostrar la fecha actual con el formato "'Today is: 04:22:31 Tuesday Mar 23, 1996", la cadena de formato es "'Today is: 'hh':'m':'s dddd MMM dd', 'yyyy". Para incluir una comilla simple en el texto del cuerpo, use dos comillas simples consecutivas. Por ejemplo, "'Don't forget' MMM dd',' yyyy" genera una salida similar a la siguiente: No olvide el 23 de marzo de 1996. No es necesario usar comillas con la coma, por lo que "'Don't forget' MMM dd, yyyy" también es válido y genera la misma salida.

### <a name="callback-fields"></a>Campos de devolución de llamada

Además de las [cadenas de formato](#format-strings) estándar y el texto del cuerpo, también puede definir ciertas partes de la presentación como campos de [devolución de llamada](#callback-fields). Estos campos se pueden usar para consultar al usuario para obtener información. Para declarar un campo de devolución de llamada, incluya uno o varios caracteres "X" (código ASCII 88) en cualquier lugar de la cadena de formato. Puede crear campos de devolución de llamada que tengan una identidad única repitiendo el carácter "X". Por lo tanto, la cadena de formato "XX dddd MMM dd", "yyy XXX" contiene dos campos de devolución de llamada únicos, "XX" y "XXX". Al igual que otros campos de control DTP, los campos de devolución de llamada se muestran en orden de izquierda a derecha en función de su ubicación en la cadena de formato.

Cuando el control DTP analiza la cadena de formato y encuentra un campo de devolución de llamada, envía los códigos de [notificación DTN \_ FORMAT](dtn-format.md) y [DTN \_ FORMATQUERY.](dtn-formatquery.md) El elemento de cadena de formato correspondiente al campo de devolución de llamada se incluye con las notificaciones para permitir que la aplicación receptora determine qué campo de devolución de llamada se está consultando. El propietario del control debe responder a estas notificaciones para asegurarse de que la información personalizada se muestra correctamente.

## <a name="date-and-time-picker-control-notification-messages"></a>Mensajes de notificación de control de selector de fecha y hora

Un control selector de fecha y hora (DTP) envía códigos de notificación cuando recibe entradas o procesos del usuario y reacciona a los campos de devolución de llamada. El elemento primario del control recibe estos códigos de notificación en forma de [**mensajes WM \_ NOTIFY.**](wm-notify.md)

Los siguientes códigos de notificación se usan con controles DTP.



| Código de notificación                             | Descripción                                                                                                                                                                                                       |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CIERRE DE \_ DTN](dtn-closeup.md)               | Indica que el calendario del mes desplegable está a punto de quitarse.                                                                                                                                               |
| [DTN \_ DATETIMECHANGE](dtn-datetimechange.md) | Señala un cambio dentro del control DTP.                                                                                                                                                                          |
| [LISTA DESPLEGABLE DE DTN \_](dtn-dropdown.md)             | Indica que el calendario del mes de lista desplegable está a punto de mostrarse.                                                                                                                                             |
| [FORMATO \_ DTN](dtn-format.md)                 | Solicita texto para mostrar en una parte de la cadena de formato descrita como un campo de devolución de llamada.                                                                                                                         |
| [DTN \_ FORMATQUERY](dtn-formatquery.md)       | Solicita información sobre el tamaño máximo permitido del texto que se va a mostrar en un campo de devolución de llamada.                                                                                                            |
| [DTN \_ USERSTRING](dtn-userstring.md)         | Señala el final de la operación de edición de un usuario dentro del control . Esta notificación solo la envían los controles DTP que usan el estilo [**\_ APPCANPARSE de DTS.**](date-and-time-picker-control-styles.md) |
| [DTN \_ WMKEYDOWN](dtn-wmkeydown.md)           | Indica que el usuario ha presionado una tecla en un campo de devolución de llamada del control DTP.                                                                                                                                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia del control Selector de fecha y hora](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 