---
title: Acerca de los controles de selector de fecha y hora
description: Un control selector de fecha y hora (DTP) proporciona una interfaz sencilla e intuitiva a través de la cual se va a intercambiar información de fecha y hora con un usuario.
ms.assetid: 6749c3ae-2c52-4183-ac4e-68ca7ebf1e13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04604c01a73aa8f2ebb8542061412372faee5282
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078486"
---
# <a name="about-date-and-time-picker-controls"></a>Acerca de los controles de selector de fecha y hora

Un *control selector de fecha y hora (DTP)* proporciona una interfaz sencilla e intuitiva a través de la cual se va a intercambiar información de fecha y hora con un usuario. Por ejemplo, con un control de DTP puede pedir al usuario que escriba una fecha y, a continuación, recupere fácilmente la selección.

Se tratan los temas siguientes:

-   [Interfaz de usuario del selector de fecha y hora](#date-and-time-picker-user-interface)
-   [Estilos y formatos del control selector de fecha y hora](#date-and-time-picker-control-styles-and-formats)
    -   [Formatos preestablecidos](#preset-formats)
    -   [Formatos personalizados](#custom-formats)
    -   [Cadenas de formato](#format-strings)
    -   [Campos de devolución de llamada](#callback-fields)
-   [Mensajes de notificación del control de selector de fecha y hora](#date-and-time-picker-control-notification-messages)
-   [Temas relacionados](#related-topics)

> [!Note]
> Windows no admite fechas anteriores a 1601. Consulte la estructura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) para obtener más información.
>
> El control se basa en el calendario gregoriano, que se presentó en 1753. No calculará fechas coherentes con el calendario juliano.

## <a name="date-and-time-picker-user-interface"></a>Interfaz de usuario del selector de fecha y hora

El área cliente de un control selector de fecha y hora (DTP) muestra información de fecha u hora, o ambas, y actúa como la interfaz a través de la cual los usuarios modifican la información. La fecha se puede seleccionar desde un calendario o mediante un control de flechas. el tiempo se puede cambiar escribiendo en los campos definidos por las [cadenas de formato](#format-strings)del control. Opcionalmente, el control muestra una casilla. Cuando se activa, se puede recuperar el valor del control; de lo contrario, se considera que el control no está inicializado.

En la ilustración siguiente se muestra una ventana que contiene tres controles de selector de fecha. El primer control selector de fecha se creó con el estilo [**DTS \_ SHOWNONE**](date-and-time-picker-control-styles.md) , el segundo con el estilo de actualización [**DTS \_**](date-and-time-picker-control-styles.md) y el tercero sin estilos especiales. En el tercer control, el usuario hizo clic en la flecha hacia abajo para mostrar el calendario.

![captura de pantalla de una ventana que muestra tres estilos de controles de selector de fecha](images/dtpdatepick.png)

En la ilustración siguiente se muestra una ventana con tres controles que contienen la hora.

El primer control se ha creado con el estilo [**DTS \_ hora**](date-and-time-picker-control-styles.md) y muestra la hora en el tiempo predeterminado, que consta de cuatro campos. El usuario puede escribir un valor válido en cualquiera de estos campos, o seleccionar el campo y cambiar el valor mediante el control de flechas o las teclas de dirección.

El segundo control muestra un conjunto de formatos personalizado mediante el uso de [**DateTime \_ SetFormat**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setformat). Al igual que con el primer control, el usuario puede cambiar los campos de hora escribiendo o usando las teclas de dirección. El día de la semana se puede cambiar seleccionando una fecha en el calendario que se abre cuando el usuario hace clic en la flecha hacia abajo.

El tercer control muestra cómo se puede Agregar texto arbitrario al control. El usuario puede seleccionar una hora (de 1 a 24) escribiendo, usando las teclas de dirección o el control de flechas.

![captura de pantalla de una ventana que muestra tres controles que contienen la hora](images/dtpdatetimepick.png)

El control de DTP actualiza automáticamente la información interna en función de la entrada del usuario. El control reconoce lo siguiente como entrada válida.



| Categoría de entrada | Descripción                                                                                                                                                                                                                                                                                                                                                                  |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Teclas de dirección     | El control acepta teclas de dirección para navegar por los campos del control y cambiar los valores. El usuario puede presionar las teclas o para desplazarse por el control si el usuario intenta moverse más allá del último campo en una dirección determinada, el foco de teclado "se ajusta" al campo en el lado opuesto del control. Las claves y cambian los valores del campo actual incrementalmente. |
| Finalizar y Inicio   | El control acepta las \_ claves virtuales VK end y VK \_ Home para cambiar el valor del campo actual por los límites superior e inferior, respectivamente.                                                                                                                                                                                                                          |
| Teclas de función  | La clave activa el modo de edición. La clave hace que el control muestre un control de calendario de mes desplegable (también lo hace).                                                                                                                                                                                                                                          |
| Números        | El control acepta la entrada numérica en segmentos de dos caracteres. Si el valor especificado por el usuario no es válido (como establecer el mes en 14), el control lo rechaza y restablece el valor anterior.                                                                                                                                                                |
| Más y menos | El control acepta las \_ teclas virtuales VK Add y VK \_ resta del teclado numérico para aumentar y disminuir el valor en el campo actual.                                                                                                                                                                                                                             |



 

Los controles de DTP que no usan el estilo de la tecla de dirección [**DTS \_**](date-and-time-picker-control-styles.md) muestran un botón de flecha. Si el usuario hace clic en este botón, se despliega un control de calendario mensual. El usuario puede seleccionar una fecha concreta haciendo clic en un área del calendario.

## <a name="date-and-time-picker-control-styles-and-formats"></a>Estilos y formatos del control selector de fecha y hora

Los controles de selector de fecha y hora (DTP) tienen varios [estilos de control de selector de fecha y hora](date-and-time-picker-control-styles.md) que determinan la apariencia y el comportamiento de un control. Especifique el estilo al crear el control con el parámetro *dwStyle* de [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). Para recuperar o cambiar el estilo de ventana después de haber creado el control, use [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) y [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).

### <a name="preset-formats"></a>Formatos preestablecidos

Hay tres formatos preestablecidos disponibles para mostrar la fecha y otro para mostrar la hora. Establezca estos formatos eligiendo uno de los siguientes estilos de ventana.



|                                                                                                       |                                                            |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| [**\_LONGDATEFORMAT DTS**](date-and-time-picker-control-styles.md)                 | La presentación tendrá el siguiente aspecto: "viernes, 19 de abril de 1996".      |
| [**\_SHORTDATEFORMAT DTS**](date-and-time-picker-control-styles.md)               | La presentación tendrá el siguiente aspecto: "4/19/96".                     |
| [**\_SHORTDATECENTURYFORMAT DTS**](date-and-time-picker-control-styles.md) | **Versión 5,80**. La presentación tendrá el siguiente aspecto: "4/19/1996". |
| [**\_hora DTS**](date-and-time-picker-control-styles.md)                         | La presentación tendrá el siguiente aspecto: "5:31:42 PM".                  |



 

### <a name="custom-formats"></a>Formatos personalizados

Un control de DTP se basa en una cadena de formato para determinar cómo mostrará los campos de información. Si los formatos preestablecidos no son suficientes, puede crear un formato personalizado definiendo su propia cadena de formato. Los formatos personalizados proporcionan mayor flexibilidad para una aplicación. Permiten especificar el orden en el que el control mostrará los campos de información. Puede incluir el texto del cuerpo y los campos de devolución de llamada para solicitar información al usuario. Una vez creada la cadena, se asigna al control de DTP con un mensaje [**DTM \_ SETFORMAT**](dtm-setformat.md) .

### <a name="format-strings"></a>Cadenas de formato

Una cadena de formato de DTP se compone de una serie de elementos que representan un fragmento de información determinado y definen su formato de presentación. Los elementos se mostrarán en el orden en que aparecen en la cadena de formato.

Los elementos con formato de fecha y hora se reemplazarán por la fecha y hora reales. Se definen mediante los siguientes grupos de caracteres.



| Elemento | Descripción                                                                       |
|---------|-----------------------------------------------------------------------------------|
| "d"     | Día de uno o dos dígitos.                                                        |
| "dd"    | Día de dos dígitos. Los valores de día de un solo dígito están precedidos por un cero.                |
| "ddd"   | Abreviatura de día de la semana de tres caracteres.                                         |
| "dddd"  | Nombre completo del día de la semana.                                                            |
| "h"     | Hora de una o dos dígitos en formato de 12 horas.                                     |
| "hh"    | Hora de dos dígitos en formato de 12 horas. Los valores de un solo dígito van precedidos de un cero. |
| "H"     | Hora de una o dos dígitos en formato de 24 horas.                                     |
| "HH"    | Hora de dos dígitos en formato de 24 horas. Los valores de un solo dígito van precedidos de un cero. |
| "m"     | Minuto de uno o dos dígitos.                                                     |
| "mm"    | Minuto de dos dígitos. Los valores de un solo dígito van precedidos de un cero.                 |
| "M"     | El número de mes de uno o dos dígitos.                                               |
| "MM"    | Número del mes de dos dígitos. Los valores de un solo dígito van precedidos de un cero.           |
| "MMM"   | Abreviatura del mes de tres caracteres.                                           |
| "MMMM"  | Nombre completo del mes.                                                              |
| "t"     | La abreviatura de AM/PM de una letra (es decir, AM se muestra como "A").              |
| "tt"    | La abreviatura AM/PM de dos letras (es decir, AM se muestra como "AM").             |
| "yy"    | Los dos últimos dígitos del año (es decir, 1996 se mostrarían como "96").       |
| "yyyy"  | El año completo (es decir, 1996 se mostraría como "1996").                       |



 

Para que la información sea más legible, puede Agregar texto de cuerpo a la cadena de formato mediante su inclusión entre comillas simples. No es necesario que los espacios ni los signos de puntuación estén entre comillas.

> [!Note]  
> Los caracteres sin formato que no están delimitados por comillas simples darán lugar a una presentación imprevisible del control de DTP.

Por ejemplo, para mostrar la fecha actual con el formato "" hoy es: 04:22:31 martes, 23 de marzo de 1996 ", la cadena de formato es" "hoy es: ' HH ': ' HH ': ' dddd MMM DD ', ' AAAA '. Para incluir una comilla simple en el texto del cuerpo, use dos comillas simples consecutivas. Por ejemplo, "' ' no olvide ' MMM DD ', ' YYYY ' genera una salida similar a la siguiente: no olvide el 23 de marzo de 1996. No es necesario usar comillas con la coma, de modo que "' no olvide ' MMM DD, yyyy" también es válido y produce el mismo resultado.

### <a name="callback-fields"></a>Campos de devolución de llamada

Además de las cadenas de [formato](#format-strings) estándar y el texto del cuerpo, también puede definir ciertas partes de la presentación como [campos de devolución de llamada](#callback-fields). Estos campos se pueden usar para consultar información al usuario. Para declarar un campo de devolución de llamada, incluya uno o más caracteres "X" (código ASCII 88) en cualquier lugar de la cadena de formato. Puede crear campos de devolución de llamada que tengan una identidad única repitiendo el carácter "X". Por lo tanto, la cadena de formato "XX dddd MMM DD", "yyy XXX" contiene dos campos de devolución de llamada únicos: "XX" y "XXX". Al igual que otros campos de control de DTP, los campos de devolución de llamada se muestran en orden de izquierda a derecha en función de su ubicación en la cadena de formato.

Cuando el control de DTP analiza la cadena de formato y encuentra un campo de devolución de llamada, envía el [ \_ formato DTN](dtn-format.md) y los códigos de notificación [DTN \_ FORMATQUERY](dtn-formatquery.md) . El elemento de cadena de formato correspondiente al campo de devolución de llamada se incluye con las notificaciones para permitir que la aplicación receptora determine qué campo de devolución de llamada se está consultando. El propietario del control debe responder a estas notificaciones para asegurarse de que la información personalizada se muestre correctamente.

## <a name="date-and-time-picker-control-notification-messages"></a>Mensajes de notificación del control de selector de fecha y hora

Un control de selector de fecha y hora (DTP) envía códigos de notificación cuando recibe entradas o procesos de usuario y reacciona a los campos de devolución de llamada. El elemento primario del control recibe estos códigos de notificación en forma de mensajes de [**\_ notificación de WM**](wm-notify.md) .

Los siguientes códigos de notificación se utilizan con controles de DTP.



| Código de notificación                             | Descripción                                                                                                                                                                                                       |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DTN \_ primer plano](dtn-closeup.md)               | Indica que el calendario del mes desplegable está a punto de quitarse.                                                                                                                                               |
| [DTN \_ DATETIMECHANGE](dtn-datetimechange.md) | Indica un cambio en el control de DTP.                                                                                                                                                                          |
| [\_lista desplegable DTN](dtn-dropdown.md)             | Indica que el calendario del mes desplegable está a punto de mostrarse.                                                                                                                                             |
| [\_formato DTN](dtn-format.md)                 | Solicita que el texto se muestre en una parte de la cadena de formato que se describe como un campo de devolución de llamada.                                                                                                                         |
| [DTN \_ FORMATQUERY](dtn-formatquery.md)       | Solicita información sobre el tamaño máximo permitido del texto que se va a mostrar en un campo de devolución de llamada.                                                                                                            |
| [DTN \_ USERSTRING](dtn-userstring.md)         | Señala el final de la operación de edición de un usuario en el control. Esta notificación se envía solo mediante controles de DTP que usan el estilo [**\_ APPCANPARSE de DTS**](date-and-time-picker-control-styles.md) . |
| [DTN \_ WMKEYDOWN](dtn-wmkeydown.md)           | Indica que el usuario ha presionado una tecla en un campo de devolución de llamada del control de DTP.                                                                                                                                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de control de selector de fecha y hora](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 