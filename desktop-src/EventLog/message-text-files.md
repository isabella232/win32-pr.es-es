---
description: Los mensajes se definen en un archivo de texto de mensaje. El compilador de mensajes asigna números a cada mensaje y genera un archivo de inclusión de C/C++ que la aplicación puede utilizar para tener acceso a un mensaje mediante una constante simbólica.
ms.assetid: 99fbb3d6-6fde-4162-b0b9-99a1cdf0b8f8
title: Archivos de texto de mensaje
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e87547f44b0b556df4e3a2ffb67736b950321c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276377"
---
# <a name="message-text-files"></a>Archivos de texto de mensaje

Los mensajes se definen en un archivo de texto de mensaje. El compilador de mensajes asigna números a cada mensaje y genera un archivo de inclusión de C/C++ que la aplicación puede utilizar para tener acceso a un mensaje mediante una constante simbólica.

La sintaxis general de las instrucciones de un archivo de texto de mensaje es la siguiente:

*palabra clave* = *valor* de

Se omiten los espacios alrededor del signo igual y el valor está delimitado por un espacio en blanco (incluidos los saltos de línea) del siguiente par de palabra clave y valor. El caso se omite al comparar con los nombres de palabra clave. La parte del *valor* puede ser una constante de tipo entero numérica mediante la sintaxis de c/c++, un nombre de símbolo que sigue las reglas de los identificadores de c/c++ o un nombre de archivo con 8 caracteres o menos, sin puntos.

Para ver un archivo de mensaje de ejemplo, vea [archivo de texto de mensaje](sample-message-text-file.md)de ejemplo.

## <a name="comments"></a>Comentarios

Se permiten líneas de comentario en el archivo de texto del mensaje. Un punto y coma (;) comienza un comentario que finaliza al final de la línea. Siga el punto y coma con un indicador de comentario de una línea de C/C++ (//) para que el archivo de encabezado generado por el compilador de mensajes se compile en la aplicación.

``` syntax
;// This is a single-line comment.
```

Para un Comentario de bloque, empiece cada línea con un punto y coma y, a continuación, coloque un indicador de comentario de bloque abierto de C/C++ (/ \* ) detrás del punto y coma en la primera línea y el indicador de comentario de bloque de cierre ( \* /) después del punto y coma en la última línea.

``` syntax
;/* This is a block comment.
;   It spans multiple lines.
;*/
```

## <a name="header-section"></a>Sección de encabezado

El archivo de texto del mensaje contiene un encabezado que define los nombres e identificadores de idioma para que los usen las definiciones de mensaje en el cuerpo del archivo. El encabezado contiene cero o más de las instrucciones siguientes.



| Sintaxis de la instrucción                           | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MessageIdTypedef =*tipo*                    | Tipo que se va a usar en la definición del mensaje de la siguiente manera: \# definir *nombre* ((*tipo*) 0x *nnnnnnnn*)<br/> El tipo debe ser lo suficientemente grande como para contener el código de mensaje completo, como un **valor DWORD**. El tipo también puede ser un tipo definido en el código fuente de la aplicación. El valor predeterminado del *tipo* es vacío, por lo que no se usa ninguna conversión de tipo. <br/> Esta instrucción se puede especificar en el encabezado y tantas veces como sea necesario en la sección de definición de mensaje.<br/>                                                                                                                  |
| SeverityNames = (*nombre* = *número* \[ :*nombre* \] ) | Conjunto de nombres que se permiten para la gravedad en una definición de mensaje. Asociado con cada nombre de gravedad es un número que, cuando se desplaza a la izquierda 30 bits, proporciona el patrón de bits a Logical-OR con los valores de identificador de mensaje y de instalación para formar el código del mensaje. Cualquier valor de gravedad que no quepa en 2 bits es un error. También se pueden asignar nombres simbólicos a los códigos de gravedad. El valor predeterminado se define de la siguiente manera: SeverityNames = (Success = 0X0 informativo = 0x1 Warning = 0X2 error = 0X3)<br/>                                                                      |
| FacilityNames = (*nombre* = *número* \[ :*nombre* \] ) | Conjunto de nombres que se permiten para los valores de las instalaciones en una definición de mensaje. Asociado con cada nombre de recurso es un número que, cuando se desplaza a la izquierda por 16 bits, proporciona el patrón de bits a Logical-OR lógico con los valores de gravedad y de identificador de mensaje para formar el código de mensaje. Cualquier valor de instalación que no quepa en 12 bits es un error. Esto permite códigos de instalación de 4096; los primeros 256 códigos se reservan para uso del sistema. También se pueden asignar nombres simbólicos a los códigos de servicio. El valor predeterminado se define de la siguiente manera: FacilityNames = (System = 0x0FF Application = 0xFFF)<br/> |
| LanguageNames = (*nombre* = *número*: nombre de *archivo*) | Conjunto de nombres que se permiten para los valores de idioma en una definición de mensaje. El número se utiliza como identificador de idioma en la tabla de recursos. El archivo especificado contiene los mensajes para ese idioma. Normalmente es un archivo. bin generado por el compilador de mensajes.<br/> Un valor de ejemplo es: LanguageNames = (Inglés = 0xC0A: MSG00409)<br/> Para obtener una lista de los identificadores de idioma, vea <https://go.microsoft.com/fwlink/p/?linkid=190280> .<br/>                                                                                                                    |
| OutputBase =*número*                        | Base de salida de las constantes de mensaje que el compilador de mensajes escribe en el archivo de encabezado. Si está presente, este valor invalida el modificador-d. Este número puede ser 10 (decimal) o 16 (hexadecimal).                                                                                                                                                                                                                                                                                                                                                                                   |



 

## <a name="message-definitions"></a>Definiciones de mensaje

Un archivo de texto de mensaje contiene cero o más definiciones de mensaje después de la sección de encabezado. En la tabla siguiente se describen las instrucciones de definición de mensaje. La instrucción MessageId marca el principio de la definición del mensaje. Las instrucciones Severity y Facility son opcionales.



| Sintaxis de la instrucción                  | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MessageId = número \[ *número* \| + \] | Identificador del mensaje. Esta instrucción es obligatoria, aunque el valor es opcional. Si no se especifica ningún valor, el valor utilizado es el valor anterior de la instalación, más uno. Si el valor se especifica con un signo más, el valor utilizado es el valor anterior de la instalación, más el número después del signo más. Cualquier valor especificado debe ajustarse a 16 bits. Para obtener más información sobre cómo se forma el valor del mensaje desde la gravedad, el recurso y el identificador del mensaje, vea el diagrama en Winerror. h. Este archivo de encabezado define los códigos de error del sistema.<br/> |
| Gravedad =*nombre*                   | Uno de los valores especificados por SeverityNames en el encabezado. Esta instrucción es opcional. Si no se especifica ningún valor, el valor utilizado es el último valor especificado para una definición de mensaje. El valor predeterminado para la primera definición de mensaje es `Severity=Success`<br/>                                                                                                                                                                                                                                                                                               |
| Facility =*nombre*                   | Uno de los valores especificados por FacilityNames en el encabezado. Esta instrucción es opcional. Si no se especifica ningún valor, el valor utilizado es el último valor especificado para una definición de mensaje. El valor predeterminado para la primera definición de mensaje es `Facility=Application`<br/>                                                                                                                                                                                                                                                                                           |
| Nombresimbólico =*nombre*               | Asocia una constante simbólica de C/C++ con el código de mensaje. Se usa en la definición del mensaje de la siguiente manera: \# definir *nombre* ((*tipo*) 0x *nnnnnnnn*)<br/>                                                                                                                                                                                                                                                                                                                                                                                                     |
| OutputBase = {*número*}             | Base de salida para las constantes de mensaje que el compilador de mensajes escribe en el archivo de encabezado. Si está presente, este valor invalida el modificador-d. Este número puede ser 10 (decimal) o 16 (hexadecimal).                                                                                                                                                                                                                                                                                                                                                                 |
| Language =*nombre*                   | Uno de los valores especificados por LanguageNames en el encabezado. Esta instrucción es opcional. Si no se especifica ningún valor, el valor utilizado es el último valor especificado para una definición de mensaje. El valor predeterminado para la primera definición de mensaje es el siguiente: `Language=English`<br/>                                                                                                                                                                                                                                                                                   |
| *texto del mensaje*                    | Texto del mensaje. Se incluye en el archivo binario del mensaje. También se incluye en el archivo de encabezado del bloque de comentarios que precede directamente a la definición del mensaje.                                                                                                                                                                                                                                                                                                                                                                                        |
| .                                 | El texto del mensaje se termina en una nueva línea que contiene un solo punto al principio de la línea.                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



 

Si la definición del mensaje incluye texto de mensaje para más de un idioma, cada idioma requiere su propia instrucción de lenguaje, texto de mensaje y terminación de nueva línea con un punto. Por ejemplo:

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

Puede especificar las siguientes secuencias de escape para dar formato al texto del mensaje para su uso por parte del visor de eventos o de la aplicación. El carácter de signo de porcentaje (%) inicia todas las secuencias de escape. Cualquier otro carácter que siga a un signo de porcentaje se mostrará sin el signo de porcentaje.

<dl> <dt>

<span id="_n__format_specifier__"></span><span id="_N__FORMAT_SPECIFIER__"></span>%*n* \[ ! *\_ especificador de formato*!\]
</dt> <dd>

Describe una instrucción INSERT. Cada inserción es una entrada de la matriz arguments en la función [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) . El valor de *n* puede ser un número comprendido entre 1 y 99. El especificador de formato es opcional. Si no se especifica ningún valor, el valor predeterminado es! s!. Para obtener información sobre el especificador de formato, vea [**wsprintf**](/windows/win32/api/winuser/nf-winuser-wsprintfa).

El especificador de formato puede usar \* para la precisión o el ancho. Cuando se especifica, usan inserciones numeradas *n*+ 1 y *n*+ 2.

</dd> <dt>

<span id="_0"></span>%0
</dt> <dd>

Finaliza una línea de texto de mensaje sin un carácter de nueva línea final. Se puede usar para crear una línea larga o para terminar un mensaje de solicitud sin un carácter de nueva línea al final.

</dd> <dt>

<span id="_."></span>%.
</dt> <dd>

Genera un solo punto. Se puede usar para mostrar un punto al principio de una línea, que de lo contrario finalizaría el texto del mensaje.

</dd> <dt>

<span id="__"></span>%!
</dt> <dd>

Genera un único signo de exclamación. Se puede usar para especificar un punto de exclamación inmediatamente después de una inserción.

</dd> <dt>

<span id="__"></span>%%
</dt> <dd>

Genera un único signo de porcentaje.

</dd> <dt>

<span id="_n"></span><span id="_N"></span>% n
</dt> <dd>

Genera un salto de línea rígido cuando aparece al final de una línea. Se puede usar con [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) para asegurarse de que el mensaje se ajusta a un ancho determinado.

</dd> <dt>

<span id="_b"></span><span id="_B"></span>% b
</dt> <dd>

Genera un carácter de espacio. Se puede usar para garantizar un número adecuado de espacios finales en una línea.

</dd> <dt>

<span id="_r"></span><span id="_R"></span>% r
</dt> <dd>

Genera un retorno de carro rígido sin un carácter de nueva línea final.

</dd> </dl>

 

