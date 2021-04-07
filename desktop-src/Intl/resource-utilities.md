---
description: En este tema se describen dos utilidades que se usan para crear aplicaciones de MUI.
ms.assetid: 8ba94001-fc46-41e0-a071-0dc500a20753
title: Utilidades de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550cf283779a57bc5ca35f88d336646b061c3f1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002568"
---
# <a name="resource-utilities"></a>Utilidades de recursos

En este tema se describen dos utilidades que se usan para crear aplicaciones de MUI. Aunque MUIRCT es una herramienta específica de MUI, MUI también usa la utilidad del compilador estándar de Windows RC. Se proporcionan instrucciones para el uso de estas utilidades en [localizar recursos y compilar la aplicación](localizing-resources-and-building-the-application.md).

## <a name="muirct-utility"></a>Utilidad MUIRCT

MUIRCT (Muirct.exe) es una utilidad de línea de comandos para dividir un archivo ejecutable estándar en un archivo LN y archivos de recursos específicos del lenguaje (es decir, localizables). Cada uno de los archivos resultantes contiene datos de configuración de recursos para la Asociación de archivos. MUIRCT se incluye en el Microsoft Windows SDK para Windows Vista.

> [!Note]  
> A partir de Windows Vista, el cargador de recursos de Win32 se actualiza para cargar recursos desde archivos específicos del idioma, así como desde archivos LN.

 

### <a name="muirct-usages"></a>Usos de MUIRCT

1.  Divida el binario en el archivo binario principal y mui basado en el \_ archivo de configuración RC.

    `Muirct -q rc_config [-c checksum_file [-b LangID]] [-x LangID] [-g LangId]     [-f] [-m] [-v level] source_file [output_LN_file] [output_MUI_file]`

2.  Extrae la suma de comprobación del archivo de suma de comprobación \_ e insértela en el archivo de salida \_ .

    `Muirct -c checksum_file [-b LangID] -e output_file`

3.  Calcula la suma de comprobación basada en el archivo de suma de comprobación \_ e insértela en el archivo de salida \_ .

    `Muirct  -c checksum_file [-b LangID] -q rc_config  -z output_file`

4.  Vuelca el contenido de datos de configuración de recursos del archivo de entrada \_ .

    `Muirct -d input_file`

### <a name="muirct-syntax"></a>Sintaxis de MUIRCT

MUIRCT puede tomar la dirección de los modificadores de línea de comandos y/o de un archivo de configuración de recursos, especificado mediante el modificador-q.


```C++
muirct [-h|-?] [ -c checksum_file] [-b langid]  ]
     [-g langid] [-q resource configuration file<RCF>] [-v level] [-x langid]
     [-e output_file]  [-z output_file] [-f] [-d MUI'ized file] [-m file_version]

source_filename [language_neutral_filename] [mui_filename]
```



**Modificadores y argumentos**



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>-h |-?</td>
<td>Muestra la pantalla de ayuda.</td>
</tr>
<tr class="even">
<td>-c</td>
<td>Especifica la checksum_file de entrada de la que se va a extraer o calcular la suma de comprobación de recursos. Checksum_file debe ser un archivo binario de Win32 que contenga recursos localizables. Si checksum_file contiene recursos para más de un idioma, se debe usar el modificador-b para especificar cuáles de ellos se deben usar; de lo contrario, se producirá un error MUIRCT. <br/></td>
</tr>
<tr class="odd">
<td>-b</td>
<td>Especifica el idioma que se usará cuando el checksum_file especificado con-c contenga recursos en varios idiomas. Este modificador solo se puede usar junto con el modificador-c. El identificador de idioma puede estar en formato decimal o hexadecimal. MUIRCT produce un error si el checksum_file contiene recursos en varios idiomas y no se especifica-b o si no se encuentra el idioma especificado por el modificador-b en el checksum_file. <br/></td>
</tr>
<tr class="even">
<td>-g</td>
<td>Especifica el identificador de idioma que se va a incluir como idioma de reserva final en la sección de datos de configuración de recursos del archivo LN. Si el cargador de recursos no puede cargar un archivo. mui solicitado de los idiomas de interfaz de usuario preferidos del subproceso, utiliza el idioma de reserva final como último intento. El valor LangID se puede especificar en formato decimal o hexadecimal. Por ejemplo, el inglés (Estados Unidos) puede especificarse mediante-g 0xC0A o-g 1033. <br/></td>
</tr>
<tr class="odd">
<td>-q</td>
<td>Especifica que el source_file se va a dividir en el output_LN_file y el output_MUI_file según el diseño del archivo de rc_config. El archivo rc_config es un archivo con formato XML que especifica los recursos que se extraerán en el archivo. mui y que se dejarán en el archivo LN. El rc_config puede especificar la distribución de tipos de recursos y elementos individuales con nombre entre el output_LN_file y el output_MUI_file. El source_file debe ser un archivo binario de Win32 que contenga recursos en un solo lenguaje; de lo contrario, MUIRCT producirá un error. MUIRCT no divide el archivo si es independiente del idioma, lo que se indica con el valor 0 de identificador de idioma en el archivo. Los output_LN_file y output_mui_file son los nombres del archivo neutro y. MUI en el que se divide el source_file. Estos nombres de archivo son opcionales. Si no se especifican, MUIRCT anexa las extensiones. LN y. mui a source_file. Normalmente, debe quitar la &quot; extensión. LN &quot; antes de implementar el archivo. MUIRCT asocia el output_LN_file y output_MUI_file calculando una suma de comprobación basada en el nombre de la source_file y la versión del archivo e insertando el resultado en la sección de configuración de recursos de cada archivo de salida. Cuando se usa junto con el modificador-c, el modificador-q tiene prioridad. Si el archivo de rc_config proporcionado con el modificador-q contiene una suma de comprobación MUIRCT omite el modificador-c e inserta el valor de la suma de comprobación del valor, rc_config archivo en los archivos LN y. MUI. Si no se encuentra ningún valor de suma de comprobación en el rc_config, MUIRCT calcula la suma de comprobación de recursos según el comportamiento del modificador-c. <br/></td>
</tr>
<tr class="even">
<td>-v</td>
<td>Especifica el nivel de detallados para el registro. Especifique 1 para imprimir todos los mensajes de error básicos y los resultados de la operación. Especifique 2 para incluir también la información de recursos (tipo, nombre, identificador de idioma) incluida en el archivo. mui y en el archivo LN. El valor predeterminado es-v 1 <br/></td>
</tr>
<tr class="odd">
<td>-X</td>
<td>Especifica el identificador de idioma con el que MUIRCT marca todos los tipos de recursos agregados a la sección de recursos del archivo. MUI. El valor LangID se puede especificar en formato decimal o hexadecimal. Por ejemplo, el inglés (Estados Unidos) se puede especificar mediante-x 0xC0A o-x 1033. <br/></td>
</tr>
<tr class="even">
<td>-E</td>
<td>Extrae la suma de comprobación de recursos contenida en el checksum_file proporcionado con el modificador-c y lo inserta en el output_file especificado. Cuando se especifica-e, MUIRCT omite todos los modificadores distintos del modificador-c. En este caso, el checksum_file debe ser un archivo binario de Win32 que contenga una sección de datos de configuración de recursos con un valor de suma de comprobación. El output_file debe ser un archivo LN o. mui existente. <br/></td>
</tr>
<tr class="odd">
<td>-Z</td>
<td>Calcula e inserta los datos de la suma de comprobación de recursos en el archivo de salida especificado. MUIRCT basa el cálculo de suma de comprobación en la entrada proporcionada con el modificador-c y el modificador opcional-b. Si especifica un archivo de salida para el modificador-z que no existe, MUIRCT se cierra con un error.<br/> Ejemplo: calcula la suma de comprobación basada en recursos localizables de Notepad.exe e inserta la suma de comprobación en el archivo de salida Notepad2.exe.<br/> <code>muirct -c notepad.exe -q myprog.rcconfig -z notepad2.exe</code><br/></td>
</tr>
<tr class="even">
<td>-f</td>
<td>Permite crear un archivo. mui con el recurso de versión que es el único recurso traducible. De forma predeterminada, MUIRCT no lo permite.<br/></td>
</tr>
<tr class="odd">
<td>-d</td>
<td>Busca y muestra los datos de configuración de recursos incrustados en el archivo de código fuente. Cuando se especifica este modificador, MUIRCT omite todas las demás opciones de la línea de comandos.<br/></td>
</tr>
<tr class="even">
<td>-M</td>
<td>Especifica el número de versión que se va a utilizar al calcular la suma de comprobación para asociar el output_LN_file y output_MUI_file. <br/></td>
</tr>
<tr class="odd">
<td>source_filename</td>
<td>Nombre del archivo de origen binario localizado; no se pueden usar caracteres comodín. Este archivo solo puede contener recursos en un idioma. Si hay recursos en varios idiomas en el archivo, MUIRCT produce un error, a menos que se use el modificador-b. Si el archivo contiene recursos con identificadores de idioma que solo tienen el valor 0, MUIRCT no divide el archivo porque un identificador de idioma de 0 indica un idioma neutro.<br/> En el caso del modificador-d, source_filename es un archivo LN o un archivo de recursos específico del lenguaje para el que MUIRCT va a mostrar los datos de configuración de recursos. <br/></td>
</tr>
<tr class="even">
<td>language_neutral_filename</td>
<td>Opcional. Nombre del archivo LN. Si no especifica el nombre de este archivo, MUIRCT anexa una segunda extensión &quot; . LN &quot; al nombre del archivo de código fuente que se va a usar como nombre de archivo independiente del idioma. Normalmente, debe quitar la &quot; extensión. LN &quot; antes de implementar el archivo.
<blockquote>
[!Note]<br />
El archivo LN no debe contener cadenas ni menús. Debe quitarlas manualmente.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>mui_filename</td>
<td>Opcional. Nombre del archivo de recursos específico del idioma. Si no especifica un nombre, MUIRCT anexa una segunda extensión &quot; . mui &quot; al nombre del archivo de código fuente que se va a usar como nombre de archivo. Normalmente, MUIRCT crea un archivo de recursos específico del lenguaje. Sin embargo, no crea un archivo de recursos si se cumple alguna de las condiciones siguientes:<br/>
<ul>
<li>No hay recursos localizables en el archivo binario original.</li>
<li>El único lenguaje de recursos que se encuentra en el archivo binario original es el idioma neutro.</li>
<li>El archivo binario original tiene recursos para más de un idioma, sin contar el idioma neutro. Si el archivo binario contiene recursos para dos idiomas y uno de ellos es el idioma neutro, la utilidad considera que el archivo es Monolingual y crea un archivo de recursos específico del idioma si hay recursos localizables.</li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="muirct-language-output"></a>Salida del lenguaje MUIRCT

MUIRCT elige el valor de atributo "UltimateFallbackLanguage" para insertar en los datos de configuración de recursos de archivo LN según el siguiente orden, de la prioridad más alta a la más baja:

1.  Atributo "UltimateFallbackLanguage" en el archivo de configuración de recursos de origen, si se pasa uno como entrada.
2.  El idioma especificado con el modificador-g.
3.  Idioma del archivo de entrada.

MUIRCT elige el valor de atributo "Language" que se va a insertar en los datos de configuración de recursos de archivos. mui según el siguiente orden:

1.  atributo "Language" en el archivo de configuración de recursos de origen, si se pasa uno como entrada.
2.  El idioma especificado por el modificador-x (Force Language).
3.  Idioma del archivo de entrada.

### <a name="muirct-checksum-handling"></a>Control de suma de comprobación MUIRCT

Normalmente, el sistema operativo calcula la suma de comprobación de los recursos específicos del idioma de un archivo, a menos que se especifique la suma de comprobación a través de un archivo de configuración de recursos. Siempre que la suma de comprobación sea la misma para el archivo LN y todos los archivos de recursos específicos del idioma asociados, y el atributo de idioma en la configuración de recursos en la coincidencia con el lenguaje LN y el idioma, el cargador de recursos puede cargar los recursos correctamente.

MUIRCT admite varios métodos para colocar las sumas de comprobación adecuadas en los datos de configuración de recursos:

1.  Cree un archivo ejecutable para cada lenguaje que contenga código y recursos. Después de esto, use MUIRCT para dividir cada uno de estos archivos en un archivo LN y un archivo de recursos específico del idioma. MUIRCT se ejecuta varias veces, una vez para generar un archivo de recursos para cada idioma. Puede realizar la compilación de las siguientes maneras:
    1.  Use el modificador-q para especificar un valor de suma de comprobación en el archivo de configuración de recursos. MUIRCT coloca este valor en todos los archivos LN y en los archivos de recursos específicos del idioma producidos. Debe adoptar una estrategia para elegir este valor, tal y como se describe más adelante en este tema.
    2.  Use el modificador-c (y, opcionalmente, el conmutador-b) para elegir un solo idioma con recursos a partir del cual MUIRCT extrae la suma de comprobación.
    3.  Use el modificador-z para elegir un solo idioma con recursos a partir del cual MUIRCT siempre extrae la suma de comprobación. Aplique esta suma de comprobación después de que los archivos se hayan creado con otros métodos.
2.  Cree un archivo ejecutable que contenga código y recursos para un solo lenguaje. Después de esto, use MUIRCT para dividir los recursos entre el archivo LN y el archivo de recursos específico del lenguaje. Por último, use una herramienta de localización binaria para modificar el archivo de recursos resultante para cada idioma.

La Convención más común para el tratamiento de sumas de comprobación consiste en basar la suma de comprobación en los recursos de inglés (Estados Unidos). Puede adoptar una Convención diferente, siempre que sea coherente para cada archivo LN. Por ejemplo, es absolutamente aceptable que una empresa de desarrollo de software base sus sumas de comprobación en el software que se basa en los recursos de francés (Francia) en lugar de los recursos en inglés (Estados Unidos), siempre que todas las aplicaciones tengan recursos en francés (Francia) en los que basar las sumas de comprobación. También es aceptable usar el archivo de configuración de recursos para asignar un valor hexadecimal arbitrario de hasta 16 dígitos hexadecimales como una suma de comprobación. Esta última estrategia impide el uso eficaz de los conmutadores-z,-c y-b de MUIRCT. Requiere la adopción de un método mediante [**GuidGen**](/previous-versions/windows/embedded/ms924300(v=msdn.10)) u otra herramienta para generar valores de suma de comprobación. Esta estrategia también requiere la configuración de una directiva para determinar cuándo se debe modificar el valor al agregar nuevos recursos localizables.

Para aplicar la suma de comprobación inglés (Estados Unidos) a todos los archivos, puede usar cualquiera de los métodos de control de suma de comprobación descritos anteriormente. Por ejemplo, puede generar el archivo LN y el archivo de recursos específico del lenguaje para inglés (Estados Unidos) y, a continuación, usar el modificador MUIRCT-d para obtener la suma de comprobación resultante. Puede copiar esta suma de comprobación en el archivo de configuración de recursos y usar el modificador-q con MUIRCT para aplicar la suma de comprobación a todos los demás archivos.

### <a name="use-of-a-resource-configuration-file-with-muirct"></a>Uso de un archivo de configuración de recursos con MUIRCT

Puede especificar los datos de configuración de recursos cuando se usa MUIRCT. Tanto si proporciona explícitamente un archivo de configuración de recursos como si no, cada archivo de recursos específico del lenguaje tiene datos de configuración de recursos, al igual que cualquier archivo LN con un archivo de recursos asociado. Por ejemplo:

-   Si usa el modificador-q para especificar un archivo de configuración de recursos, pero no hay recursos localizables en el archivo de origen de entrada, no se genera ningún archivo de recursos específico del idioma y el archivo LN resultante no contiene datos de configuración de recursos. Además, si el archivo de origen de entrada tiene recursos multilingües, MUIRCT no dividirá el archivo.

> [!Note]  
> Actualmente, el comportamiento de MUIRCT es incoherente cuando el elemento neutralResources del archivo de configuración de recursos no contiene elementos resourceType y el elemento localizedResources contiene cadenas y menús, por ejemplo. En tal caso, MUIRCT divide los recursos como se indica a continuación:
>
> -   Todos los recursos del binario original (incluidas las cadenas y los menús), además de los recursos de MUI, se colocan en el archivo LN.
> -   Las cadenas, los menús y los recursos de MUI se colocan en el archivo de recursos específico del idioma adecuado.

 

### <a name="examples-for-using-muirct"></a>Ejemplos de uso de MUIRCT

**Ejemplos de uso estándar**


```C++
muirct -q mui.MMF bar.exe barnew.exe barnew.exe.mui

muirct -d myprog.exe.mui
```



**Ejemplo de salida de archivo LN con el modificador-d**

Este es un ejemplo de la salida de los datos de configuración de recursos de un archivo LN, Shell32.dll, mediante el modificador-d con MUIRCT:


```C++
Signature          -    fecdfecd
Length             -    148
RC Config Version  -    10000
FileType           -    11
SystemAttributes   -    100
UltimateFallback location    -  external
Service Checksum   -    14f44a8d86bef14af26d9a885964c935
Checksum           -    f5b3b7ab330439d6fcc07582c3afb613
MainNameTypes      -    AVI FTR ORDERSTREAM TYPELIB UIFILE XML MUI
MainIDTypes        -    1 2 3 12 14 16 24
MuiNameTypes       -    MUI
MuiIDTypes         -    2 3 4 5 6 9 14 16
UltimateFallbackLanguage   -   en-US
```



**Ejemplo de Language-Specific salida de archivo de recursos con el modificador-d**

Este es un ejemplo de la salida de datos de configuración de recursos de un archivo. MUI, Shell32.dll. MUI, con el modificador-d para MUIRCT:


```C++
Signature          -    fecdfecd
Length             -     c8
RC Config Version  -    10000
FileType           -    12
SystemAttributes   -    100
Service Checksum   -    14f44a8d86bef14af26d9a885964c935
Checksum           -    f5b3b7ab330439d6fcc07582c3afb613
MainNameTypes      -    MUI
MainIDTypes        -    2 3 4 5 6 9 14 16
Language           -    en-US
```



## <a name="rc-compiler-utility"></a>RC (utilidad del compilador)

RC Compiler (Rc.exe) es una utilidad de línea de comandos para compilar un archivo de script de definición de recursos (extensión. RC) en archivos de recursos (extensión. res). El compilador RC se incluye en el Windows SDK. En este documento solo se explica el uso del compilador RC con capacidades relacionadas con la MUI del cargador de recursos. Para obtener información completa sobre el compilador, vea [acerca de los archivos de recursos](../menurc/about-resource-files.md).

El compilador RC permite crear, desde un único conjunto de orígenes, un archivo LN y un archivo de recursos independiente del idioma. En el caso de MUIRCT, los archivos están asociados a los datos de configuración de recursos.

### <a name="rc-compiler-syntax-as-used-for-mui-resources"></a>RC sintaxis del compilador tal como se usa para recursos de MUI

Los modificadores del compilador RC se definen en detalle en [uso de RC](../menurc/using-rc-the-rc-command-line-.md). En esta sección solo se definen los modificadores que se usan para crear recursos de MUI. Recuerde que cada modificador distingue entre mayúsculas y minúsculas. Se supone que los tipos de recursos son independientes del idioma, a menos que se indique lo contrario.


```C++
rc [-h|-?] -fm mui_res_name [-q rc_config_file_name] [-g langid] [-g1 ] [-g2 version]
```



**Modificadores y argumentos**



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>-h |-?</td>
<td>Muestra la pantalla de ayuda.</td>
</tr>
<tr class="even">
<td>-FM</td>
<td>Utiliza el archivo de recursos especificado para los recursos específicos del idioma. Normalmente, el compilador de recursos crea un archivo de recursos específico del lenguaje. Sin embargo, no crea el archivo si se cumple alguna de las condiciones siguientes:<br/>
<ul>
<li>No hay recursos localizables en el archivo. rc.</li>
<li>El único idioma de los recursos que se encuentra en el archivo. RC es el idioma neutro.</li>
<li>El archivo. rc tiene recursos para más de un idioma, sin contar el idioma neutro. Si el archivo. RC contiene recursos para dos idiomas y uno de ellos es el idioma neutro, el compilador considera que el archivo es Monolingual. Si hay recursos localizables, el compilador crea un archivo de recursos específico del lenguaje.</li>
</ul></td>
</tr>
<tr class="odd">
<td>-q</td>
<td>Usa el archivo de configuración de recursos especificado para obtener los tipos de recursos que se colocarán en el archivo de recursos específico del lenguaje y en el archivo LN. Para obtener más información, vea <a href="preparing-a-resource-configuration-file.md">preparar un archivo de configuración de recursos</a>. Como alternativa a este modificador, puede usar los modificadores-j y-k, pero es preferible usar un archivo de configuración de recursos. <br/> Mediante el uso del modificador-q con un archivo de configuración de recursos, puede implementar una división basada en elementos y proporcionar atributos que terminarán con la configuración de recursos binarios en el archivo de recursos LN y el idioma específico. Esta división no es posible mediante los modificadores-j y-k.
<blockquote>
[!Note]<br />
El proceso de división del compilador RC no funciona correctamente si se almacenan los recursos y la información de versión en distintos archivos de configuración de recursos. En este caso, el compilador RC no divide la información de versión. Por lo tanto, se produce un error del vinculador durante la vinculación del archivo de recursos específico del lenguaje porque el archivo no tiene recursos de versión.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td>-g</td>
<td>Especifica el identificador de <a href="language-identifiers.md">idioma de reserva</a> final en formato hexadecimal.<br/></td>
</tr>
<tr class="odd">
<td>-G1</td>
<td>Crea un archivo MUI. res aunque el recurso de versión sea el único contenido traducible. De forma predeterminada, el compilador RC no genera un archivo. res si la versión es el único recurso traducible.<br/></td>
</tr>
<tr class="even">
<td>-g2</td>
<td>Especifica el número de versión personalizado que se va a utilizar al calcular la suma de comprobación.<br/></td>
</tr>
<tr class="odd">
<td>mui_res_name</td>
<td>Archivo de recursos para recursos específicos del idioma.<br/></td>
</tr>
<tr class="even">
<td>rc_config_file_name</td>
<td>Archivo de configuración de recursos.<br/></td>
</tr>
<tr class="odd">
<td>langid</td>
<td>Identificador de idioma.<br/></td>
</tr>
<tr class="even">
<td>version</td>
<td>Número de versión personalizado, en un formato como &quot; 6.2.0.0 &quot; .<br/></td>
</tr>
</tbody>
</table>



 

### <a name="example-for-using-rc-compiler-to-build-mui-resources"></a>Ejemplo del uso del compilador RC para compilar recursos MUI

Para ilustrar la operación del compilador RC con recursos de MUI, vamos a examinar la siguiente línea de comandos para el archivo de recursos. RC:


```C++
rc -fm myfile_res.res -q myfile.rcconfig myfile.rc
```



Esta línea de comandos hace que el compilador de RC haga lo siguiente:

-   Cree el archivo de recursos específico del idioma file \_ res. res y un archivo de recursos independiente del idioma que se toma como valor predeterminado de archivo. res, según el nombre del archivo. rc.
-   Agregue los tipos de recursos 2 (elemento 5 6 7 8 9 10 11 12), 4, 5, 6, 9, 11, 16, 23, 240, 1024 MY \_ Type al archivo. res específico del idioma si están en el archivo. rc.
-   Agregue el tipo de recurso 16, junto con cualquier otro tipo de recurso que se describe en el archivo de recursos al archivo. res independiente del idioma y al archivo. res específico del idioma. Tenga en cuenta que, en este ejemplo, el tipo de recurso 16 se agrega en dos lugares.
-   Elija el valor del atributo "UltimateFallbackLanguage" para insertar en los datos de configuración de recursos de archivo LN según los criterios siguientes, ordenados de prioridad más alta a más bajo:
    -   El atributo "UltimateFallbackLanguage" en el archivo de configuración de recursos si se pasa uno como entrada.
    -   Valor del atributo Language que se va a insertar en los datos de configuración de recursos según el orden del lenguaje del compilador RC (idioma del archivo de recursos independiente del idioma y del idioma). Las consideraciones incluyen el idioma en el archivo. rc, el valor de idioma del modificador-GL y el identificador 0x0409 para inglés (Estados Unidos).

## <a name="remarks"></a>Observaciones

Si incluye cualquier tipo de recurso ICON (3), DIALOG (5), STRING (6) o VERSION (16) en el elemento neutralResources, tendrá que duplicar esa entrada en el elemento localizedResources del archivo de configuración de recursos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de la interfaz de usuario multilingüe](multilingual-user-interface-reference.md)
</dt> <dt>

[Administración de recursos de MUI](mui-resource-management.md)
</dt> <dt>

[Localizar recursos y compilar la aplicación](localizing-resources-and-building-the-application.md)
</dt> </dl>

 

 
