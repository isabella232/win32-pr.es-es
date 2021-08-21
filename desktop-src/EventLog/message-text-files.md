---
description: Los mensajes se definen en un archivo de texto de mensaje. El compilador de mensajes asigna números a cada mensaje y genera un archivo de incluyeción de C/C++ que la aplicación puede usar para tener acceso a un mensaje mediante una constante simbólica.
ms.assetid: 99fbb3d6-6fde-4162-b0b9-99a1cdf0b8f8
title: Archivos de texto de mensaje
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 818210cfe58fb8eafe939c70a2a57b358e306bb9bc072a64abebbec5ca41c266
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118151481"
---
# <a name="message-text-files"></a>Archivos de texto de mensaje

Los mensajes se definen en un archivo de texto de mensaje. El compilador de mensajes asigna números a cada mensaje y genera un archivo de incluyeción de C/C++ que la aplicación puede usar para tener acceso a un mensaje mediante una constante simbólica.

La sintaxis general de las instrucciones de un archivo de texto de mensaje es la siguiente:

*palabra clave* = *value*

Los espacios alrededor del signo igual se omiten y el valor está delimitado por espacios en blanco (incluidos los saltos de línea) del siguiente par palabra clave-valor. Las mayúsculas y minúsculas se omiten al comparar con nombres de palabra clave. La  parte del valor puede ser una constante de entero numérico mediante la sintaxis de C/C++, un nombre de símbolo que sigue las reglas para los identificadores de C/C++ o un nombre de archivo con 8 caracteres o menos, sin puntos.

Para obtener un archivo de mensaje de ejemplo, vea [Archivo de texto de mensaje de ejemplo](sample-message-text-file.md).

## <a name="comments"></a>Comentarios

Las líneas de comentario se permiten en el archivo de texto del mensaje. Punto y coma (;) comienza un comentario que termina al final de la línea. Siga el punto y coma con un indicador de comentario de una sola línea de C/C++ (//) para que el archivo de encabezado generado por el compilador de mensajes se compile en la aplicación.

``` syntax
;// This is a single-line comment.
```

Para un comentario de bloque, comience cada línea con un punto y coma y, a continuación, coloque un indicador de comentario de bloque abierto de C/C++ (/ ) después del punto y coma en la primera línea y el indicador de comentario de bloque de cierre ( /) después del punto y coma en la última \* \* línea.

``` syntax
;/* This is a block comment.
;   It spans multiple lines.
;*/
```

## <a name="header-section"></a>Sección de encabezado

El archivo de texto del mensaje contiene un encabezado que define los nombres y los identificadores de idioma que las definiciones de mensaje usan en el cuerpo del archivo. El encabezado contiene cero o más de las siguientes instrucciones.



| Sintaxis de instrucciones                           | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MessageIdTypedef=*type*                    | Tipo que se va a usar en la definición del mensaje como se indica a continuación: \# define *name* ((*type*)0x *nnnnnnnn )*<br/> El tipo debe ser lo suficientemente grande como para dar cabida a todo el código del mensaje, como **DWORD.** El tipo también puede ser un tipo definido en el código fuente de la aplicación. El valor predeterminado del *tipo* está vacío, por lo que no se usa ninguna conversión de tipo. <br/> Esta instrucción se puede especificar en el encabezado y con la frecuencia necesaria en la sección de definición del mensaje.<br/>                                                                                                                  |
| SeverityNames=(*name* = *number* \[ :*name* \] ) | Conjunto de nombres que se permiten para la gravedad en una definición de mensaje. Asociado a cada nombre de gravedad es un número que, cuando se desplaza a la izquierda por 30 bits, proporciona el patrón de bits a logical-OR con los valores de recurso e identificador de mensaje para formar el código del mensaje. Cualquier valor de gravedad que no cabe en 2 bits es un error. También se pueden dar nombres simbólicos a los códigos de gravedad. El valor predeterminado se define de la siguiente manera: SeverityNames=( Success=0x0 Informational=0x1 Warning=0x2 Error=0x3)<br/>                                                                      |
| FacilityNames=(*name* = *number* \[ :*name* \] ) | Conjunto de nombres que se permiten para los valores de la instalación en una definición de mensaje. Asociado a cada nombre de instalación es un número que, cuando se desplaza a la izquierda por 16 bits, proporciona el patrón de bits a logical-OR con los valores de gravedad e identificador de mensaje para formar el código del mensaje. Cualquier valor de la instalación que no cabe en 12 bits es un error. Esto permite códigos de instalación 4096; Los primeros 256 códigos están reservados para el uso del sistema. También se pueden dar nombres simbólicos a los códigos de instalación. El valor predeterminado se define de la siguiente manera: FacilityNames=( System=0x0FF Application=0xFFF)<br/> |
| LanguageNames=(*name* = *number*:*filename*) | Conjunto de nombres que se permiten para los valores de idioma en una definición de mensaje. El número se usa como identificador de idioma en la tabla de recursos. El archivo especificado contiene los mensajes para ese idioma. Normalmente es un archivo .bin generado por el compilador de mensajes.<br/> Un valor de ejemplo es: LanguageNames=(English=0x409:MSG00409)<br/> Para obtener una lista de identificadores de idioma, vea <https://go.microsoft.com/fwlink/p/?linkid=190280> .<br/>                                                                                                                    |
| OutputBase=*number*                        | Base de salida para las constantes de mensaje que el compilador de mensajes escribe en el archivo de encabezado. Si está presente, este valor invalida el modificador -d. Este número puede ser 10 (decimal) o 16 (hexadecimal).                                                                                                                                                                                                                                                                                                                                                                                   |



 

## <a name="message-definitions"></a>Definiciones de mensaje

Un archivo de texto de mensaje contiene cero o más definiciones de mensaje después de la sección de encabezado. En la tabla siguiente se describen las instrucciones message-definition. La instrucción MessageId marca el principio de la definición del mensaje. Las instrucciones Severity y Facility son opcionales.



| Sintaxis de instrucciones                  | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MessageId= \[ *number* \| + *number*\] | Identificador del mensaje. Esta instrucción es necesaria, aunque el valor es opcional. Si no se especifica ningún valor, el valor utilizado es el valor anterior de la instalación, más uno. Si el valor se especifica con un signo más, el valor usado es el valor anterior de la instalación, más el número después del signo más. Cualquier valor especificado debe caber en 16 bits. Para más información sobre cómo se forma el valor del mensaje a partir de la gravedad, la instalación y el identificador del mensaje, consulte el diagrama de Winerror.h. Este archivo de encabezado define códigos de error para el sistema.<br/> |
| Severity=*name*                   | Uno de los valores especificados por SeverityNames en el encabezado . Esta instrucción es opcional. Si no se especifica ningún valor, el valor utilizado es el último valor especificado para una definición de mensaje. El valor predeterminado para la primera definición de mensaje es `Severity=Success`<br/>                                                                                                                                                                                                                                                                                               |
| Facility=*name*                   | Uno de los valores especificados por FacilityNames en el encabezado . Esta instrucción es opcional. Si no se especifica ningún valor, el valor utilizado es el último valor especificado para una definición de mensaje. El valor predeterminado para la primera definición de mensaje es `Facility=Application`<br/>                                                                                                                                                                                                                                                                                           |
| SymbolicName=*name*               | Asocia una constante simbólica de C/C++ con el código del mensaje. Se usa en la definición del mensaje como se indica a continuación: \# define *name* ((*type*)0x *nnnnnnn*)<br/>                                                                                                                                                                                                                                                                                                                                                                                                     |
| OutputBase={*number*}             | Base de salida para las constantes de mensaje que el compilador de mensajes escribe en el archivo de encabezado. Si está presente, este valor invalida el modificador -d. Este número puede ser 10 (decimal) o 16 (hexadecimal).                                                                                                                                                                                                                                                                                                                                                                 |
| Language=*name*                   | Uno de los valores especificados por LanguageNames en el encabezado . Esta instrucción es opcional. Si no se especifica ningún valor, el valor utilizado es el último valor especificado para una definición de mensaje. El valor predeterminado para la primera definición de mensaje es el siguiente: `Language=English`<br/>                                                                                                                                                                                                                                                                                   |
| *texto del mensaje*                    | Texto del mensaje. Se incluye en el archivo binario del mensaje. También se incluye en el archivo de encabezado del bloque de comentarios que precede directamente a la definición del mensaje.                                                                                                                                                                                                                                                                                                                                                                                        |
| .                                 | El texto del mensaje finaliza con una nueva línea que contiene un único punto al principio de la línea.                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



 

Si la definición del mensaje incluye texto de mensaje para más de un idioma, cada idioma requiere su propia instrucción Language, texto del mensaje y terminar nueva línea con un punto. Por ejemplo:

``` syntax
MessageId=0x1
Severity=Error
Facility=Runtime
SymbolicName=MSG_BAD_COMMAND
Language=English
You have chosen an incorrect command.
.

Language=Japanese
<Japanese message string goes here>
.
```

Puede especificar las siguientes secuencias de escape para dar formato al texto del mensaje para que lo use el visor de eventos o la aplicación. El carácter de signo de porcentaje (%) comienza todas las secuencias de escape. Cualquier otro carácter que sigue a un signo de porcentaje se muestra sin el signo de porcentaje.

<dl> <dt>

<span id="_n__format_specifier__"></span><span id="_N__FORMAT_SPECIFIER__"></span>%*n* \[ ! *especificador \_ de formato*!\]
</dt> <dd>

Describe una inserción. Cada inserción es una entrada de la matriz Arguments de la [**función FormatMessage.**](/windows/desktop/api/winbase/nf-winbase-formatmessage) El valor *de n* puede ser un número entre 1 y 99. El especificador de formato es opcional. Si no se especifica ningún valor, el valor predeterminado es !s!. Para obtener información sobre el especificador de formato, [**vea wsprintf**](/windows/win32/api/winuser/nf-winuser-wsprintfa).

El especificador de formato puede \* usar para la precisión o el ancho. Cuando se especifica, consumen inserciones numeradas *n*+1 y *n*+2.

</dd> <dt>

<span id="_0"></span>%0
</dt> <dd>

Finaliza una línea de texto del mensaje sin un carácter de nueva línea final. Se puede usar para crear una línea larga o finalizar un mensaje de aviso sin un carácter de nueva línea final.

</dd> <dt>

<span id="_."></span>%.
</dt> <dd>

Genera un único punto. Se puede usar para mostrar un punto al principio de una línea, que de lo contrario finalizaría el texto del mensaje.

</dd> <dt>

<span id="__"></span>%!
</dt> <dd>

Genera un único signo de exclamación. Se puede usar para especificar un signo de exclamación inmediatamente después de una inserción.

</dd> <dt>

<span id="__"></span>%%
</dt> <dd>

Genera un signo de porcentaje único.

</dd> <dt>

<span id="_n"></span><span id="_N"></span>%n
</dt> <dd>

Genera un salto de línea duro cuando se produce al final de una línea. Esto se puede usar con [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) para asegurarse de que el mensaje se ajusta a un ancho determinado.

</dd> <dt>

<span id="_b"></span><span id="_B"></span>%b
</dt> <dd>

Genera un carácter de espacio. Esto se puede usar para garantizar un número adecuado de espacios finales en una línea.

</dd> <dt>

<span id="_r"></span><span id="_R"></span>%r
</dt> <dd>

Genera un retorno de carro duro sin un carácter de nueva línea final.

</dd> </dl>

 

