---
description: En este tema se describen dos utilidades que se usan para compilar aplicaciones DE LAN.
ms.assetid: 8ba94001-fc46-41e0-a071-0dc500a20753
title: Utilidades de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f755362a6b4d751ecaa1c8a43f75b5617db0ceb59d46bd8124ba06ae3f919ab9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040475"
---
# <a name="resource-utilities"></a>Utilidades de recursos

En este tema se describen dos utilidades que se usan para compilar aplicaciones DE LAN. Aunque MUIRCT es una herramienta específica de MUI, TAMBIÉN usa la utilidad estándar Windows compilador RC. Las instrucciones para usar estas utilidades se proporcionan [en Localización de recursos y Creación de la aplicación](localizing-resources-and-building-the-application.md).

## <a name="muirct-utility"></a>Utilidad MUIRCT

MUIRCT (Muirct.exe) es una utilidad de línea de comandos para dividir un archivo ejecutable estándar en un archivo LN y archivos de recursos específicos del lenguaje (es decir, localizables). Cada uno de los archivos resultantes contiene datos de configuración de recursos para la asociación de archivos. MUIRCT se incluye en el SDK de Microsoft Windows para Windows Vista.

> [!Note]  
> A partir Windows Vista, el cargador de recursos win32 se actualiza para cargar recursos desde archivos específicos del lenguaje, así como desde archivos LN.

 

### <a name="muirct-usages"></a>Usos de MUIRCT

1.  Divida el archivo binario en el archivo binario principal y en el archivo de \_ configuración rc.

    `Muirct -q rc_config [-c checksum_file [-b LangID]] [-x LangID] [-g LangId]     [-f] [-m] [-v level] source_file [output_LN_file] [output_MUI_file]`

2.  Extraiga la suma de comprobación del archivo de \_ suma de comprobación e insértela en el archivo de \_ salida.

    `Muirct -c checksum_file [-b LangID] -e output_file`

3.  Calcule la suma de comprobación en función del archivo de \_ suma de comprobación e insértela en el archivo de \_ salida.

    `Muirct  -c checksum_file [-b LangID] -q rc_config  -z output_file`

4.  Volcado del contenido de los datos de configuración de recursos desde el archivo de \_ entrada.

    `Muirct -d input_file`

### <a name="muirct-syntax"></a>Sintaxis de MUIRCT

MUIRCT puede tomar la dirección de los modificadores de línea de comandos o de un archivo de configuración de recursos, especificado mediante el modificador -q.


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
<td>-h|-?</td>
<td>Muestra la pantalla de ayuda.</td>
</tr>
<tr class="even">
<td>-c</td>
<td>Especifica el valor de entrada checksum_file del que se va a extraer o calcular la suma de comprobación de recursos. Checksum_file debe ser un archivo binario Win32 que contenga recursos localizables. Si checksum_file recursos para más de un idioma, se debe usar el modificador -b para especificar cuál de ellos se debe usar; de lo contrario, se produce un error en MUIRCT. <br/></td>
</tr>
<tr class="odd">
<td>-b</td>
<td>Especifica el idioma que se va a usar cuando el checksum_file especificado con -c contiene recursos en varios idiomas. Este modificador solo se puede usar junto con el modificador -c. El identificador de idioma puede estar en formato decimal o hexadecimal. Se produce un error en MUIRCT si el checksum_file contiene recursos en varios idiomas y no se especifica -b o si el idioma especificado por el modificador -b no se encuentra en el checksum_file. <br/></td>
</tr>
<tr class="even">
<td>-g</td>
<td>Especifica el identificador de idioma que se va a incluir como el idioma de reserva final en la sección de datos de configuración de recursos del archivo LN. Si el cargador de recursos no puede cargar un archivo .csv solicitado desde los idiomas de interfaz de usuario preferidos del subproceso, usa el último idioma de reserva como último intento. El valor LangID se puede especificar en formato decimal o hexadecimal. Por ejemplo, el inglés (Estados Unidos) se puede especificar mediante -g 0x409 o -g 1033. <br/></td>
</tr>
<tr class="odd">
<td>-q</td>
<td>Especifica que el source_file se va a dividir en el output_LN_file y el output_MUI_file según el diseño rc_config archivo. El rc_config archivo es un archivo con formato XML que especifica qué recursos se extraerán en el archivo .csv y cuáles se van a dejar en el archivo LN. El rc_config puede especificar la distribución de tipos de recursos y elementos con nombre individuales entre el output_LN_file y output_MUI_file. El source_file debe ser un binario win32 que contenga recursos en un solo idioma; de lo contrario, se produce un error en MUIRCT. MUIRCT no divide el archivo si es independiente del idioma, lo que se indica al tener solo el valor de identificador de idioma 0 en el archivo. Los output_LN_file y output_mui_file son los nombres del archivo neutral del lenguaje y .csv en el que se divide el source_file. Estos nombres de archivo son opcionales. Si no se especifican, MUIRCT anexa las extensiones .ln y .mui a source_file. Normalmente debe quitar la extensión &quot; .ln &quot; antes de implementar el archivo. MUIRCT asocia el output_LN_file y output_MUI_file calculando una suma de comprobación basada en el nombre de source_file y la versión del archivo e insertando el resultado en la sección de configuración de recursos de cada archivo de salida. Cuando se usa junto con el modificador -c, el modificador -q tiene prioridad. Si el archivo rc_config proporcionado con el modificador -q contiene una suma de comprobación MUIRCT omite el modificador -c e inserta el valor de suma de comprobación del valor , rc_config en los archivos LN y .mui. Si no se encuentra ningún valor de suma de comprobación en el rc_config, MUIRCT calcula la suma de comprobación de recursos en función del comportamiento del modificador -c. <br/></td>
</tr>
<tr class="even">
<td>-v</td>
<td>Especifica el nivel de detalle para el registro. Especifique 1 para imprimir todos los mensajes de error básicos y los resultados de la operación. Especifique 2 para incluir también la información de recursos (tipo, nombre, identificador de idioma) incluida en el archivo .mime y el archivo LN. El valor predeterminado es -v 1. <br/></td>
</tr>
<tr class="odd">
<td>-X</td>
<td>Especifica el identificador de idioma con el que MUIRCT marca todos los tipos de recursos agregados a la sección de recursos del archivo .csv. El valor LangID se puede especificar en formato decimal o hexadecimal. Por ejemplo, el inglés (Estados Unidos) se puede especificar mediante -x 0x409 o -x 1033. <br/></td>
</tr>
<tr class="even">
<td>-E</td>
<td>Extrae la suma de comprobación de recursos contenida en el checksum_file proporcionado con el modificador -c y la inserta en el output_file. Cuando se especifica -e, MUIRCT omite todos los modificadores distintos del modificador -c. En este caso, checksum_file debe ser un archivo binario win32 que contenga una sección de datos de configuración de recursos con un valor de suma de comprobación. El output_file debe ser un archivo LN existente o un archivo .csv. <br/></td>
</tr>
<tr class="odd">
<td>-Z</td>
<td>Calcula e inserta datos de suma de comprobación de recursos en el archivo de salida especificado. MUIRCT basa el cálculo de suma de comprobación en la entrada proporcionada con el modificador -c y el modificador -b opcional. Si especifica un archivo de salida para el modificador -z que no existe, MUIRCT se cierra con un error.<br/> Ejemplo: calcula la suma de comprobación en función de los recursos localizables Notepad.exe e inserta la suma de comprobación en el archivo de Notepad2.exe.<br/> <code>muirct -c notepad.exe -q myprog.rcconfig -z notepad2.exe</code><br/></td>
</tr>
<tr class="even">
<td>-f</td>
<td>Permite crear un archivo .csv con el recurso de versión como único recurso localizable. De forma predeterminada, MUIRCT no lo permite.<br/></td>
</tr>
<tr class="odd">
<td>-d</td>
<td>Busca y muestra datos de configuración de recursos incrustados en el archivo de origen. Al especificar este modificador, MUIRCT omite todas las demás opciones de línea de comandos.<br/></td>
</tr>
<tr class="even">
<td>-M</td>
<td>Especifica el número de versión que se usará al calcular la suma de comprobación para asociar output_LN_file y output_MUI_file. <br/></td>
</tr>
<tr class="odd">
<td>source_filename</td>
<td>Nombre del archivo de origen binario localizado; no se pueden usar caracteres comodín. Este archivo solo puede contener recursos en un idioma. Si hay recursos en varios idiomas en el archivo, se produce un error en MUIRCT, a menos que se utilice el modificador -b. Si el archivo contiene recursos con identificadores de idioma que solo tienen el valor 0, MUIRCT no divide el archivo porque un identificador de idioma de 0 indica un idioma neutro.<br/> Para el modificador -d, source_filename es un archivo LN o un archivo de recursos específico del lenguaje para el que MUIRCT va a mostrar datos de configuración de recursos. <br/></td>
</tr>
<tr class="even">
<td>language_neutral_filename</td>
<td>Opcional. Nombre del archivo LN. Si no especifica el nombre de este archivo, MUIRCT anexa un segundo archivo de extensión .ln al nombre del archivo de origen que se usará como nombre de archivo &quot; &quot; neutro en el idioma. Normalmente debe quitar la extensión &quot; .ln &quot; antes de implementar el archivo.
<blockquote>
[!Note]<br />
El archivo LN no debe contener cadenas ni menús. Debe quitarlos manualmente.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>mui_filename</td>
<td>Opcional. Nombre del archivo de recursos específico del lenguaje. Si no especifica un nombre, MUIRCT anexa una segunda extensión .csv al nombre de archivo de origen que se va a usar &quot; &quot; como nombre de archivo. Normalmente, MUIRCT crea un archivo de recursos específico del lenguaje. Sin embargo, no crea un archivo de recursos si existe alguna de las condiciones siguientes:<br/>
<ul>
<li>No hay recursos localizables en el archivo binario original.</li>
<li>El único idioma de recursos que se encuentra en el archivo binario original es el idioma neutro.</li>
<li>El archivo binario original tiene recursos para más de un idioma, sin contar el idioma neutro. Si el archivo binario contiene recursos para dos idiomas y uno de ellos es el idioma neutro, la utilidad considera que el archivo es monolingüe y crea un archivo de recursos específico del lenguaje si hay recursos localizables.</li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="muirct-language-output"></a>Salida del lenguaje MUIRCT

MUIRCT elige el valor del atributo "UltimateFallbackLanguage" para insertar en los datos de configuración de recursos del archivo LN en función del orden siguiente, de prioridad más alta a menor:

1.  Atributo "UltimateFallbackLanguage" en el archivo de configuración de recursos de origen, si se pasa uno como entrada.
2.  Idioma especificado con el modificador -g.
3.  Idioma del archivo de entrada.

MUIRCT elige el valor del atributo "language" que se va a insertar en los datos de configuración de recursos del archivo .mui en función del orden siguiente:

1.  Atributo "language" en el archivo de configuración de recursos de origen, si se pasa uno como entrada.
2.  Idioma especificado por el modificador -x (forzar idioma).
3.  Idioma del archivo de entrada.

### <a name="muirct-checksum-handling"></a>Control de suma de comprobación de MUIRCT

Normalmente, el sistema operativo calcula la suma de comprobación sobre los recursos específicos del idioma de un archivo, a menos que especifique la suma de comprobación a través de un archivo de configuración de recursos. Siempre que la suma de comprobación sea la misma para el archivo LN y todos los archivos de recursos específicos del lenguaje asociados, y el atributo de idioma en la configuración de recursos en el LN y la coincidencia dependiente del idioma, el cargador de recursos puede cargar correctamente los recursos.

MUIRCT admite varios métodos para colocar las sumas de comprobación adecuadas en los datos de configuración de recursos:

1.  Compile un archivo ejecutable para cada lenguaje, que contenga código y recursos. Después de esto, use MUIRCT para dividir cada uno de estos archivos en un archivo LN y un archivo de recursos específico del lenguaje. MUIRCT se ejecuta varias veces, una vez para generar un archivo de recursos para cada idioma. Puede realizar la compilación de las maneras siguientes:
    1.  Use el modificador -q para especificar un valor de suma de comprobación en el archivo de configuración de recursos. MUIRCT coloca este valor en todos los archivos LN y archivos de recursos específicos del lenguaje generados. Debe adoptar una estrategia para elegir este valor, como se describe más adelante en este tema.
    2.  Use el modificador -c (y, opcionalmente, el modificador -b) para elegir un solo idioma que tenga recursos de los que MUIRCT extraiga la suma de comprobación.
    3.  Use el modificador -z para elegir un único idioma que tenga recursos de los que MUIRCT siempre extraiga la suma de comprobación. Aplique esta suma de comprobación después de que los archivos se hayan creado mediante otros métodos.
2.  Compile un archivo ejecutable que contenga código y recursos para un solo lenguaje. Después, use MUIRCT para dividir los recursos entre el archivo LN y el archivo de recursos específico del lenguaje. Por último, use una herramienta de localización binaria para modificar el archivo de recursos resultante para cada idioma.

La convención más común para el control de suma de comprobación es basar la suma de comprobación en los recursos de inglés (Estados Unidos). Puede adoptar una convención diferente, siempre y cuando sea coherente para cada archivo LN. Por ejemplo, es perfectamente aceptable que una empresa de desarrollo de software base sus sumas de comprobación en el software que se basa en recursos de francés (Francia) en lugar de en inglés (Estados Unidos), siempre y cuando todas las aplicaciones tengan recursos de francés (Francia) en los que basar las sumas de comprobación. También es aceptable usar el archivo de configuración de recursos para asignar un valor hexadecimal arbitrario de hasta 16 dígitos hexadecimales como suma de comprobación. Esta última estrategia impide el uso efectivo de los modificadores -z, -c y -b de MUIRCT. Requiere la adopción de un método mediante [**GuidGen**](/previous-versions/windows/embedded/ms924300(v=msdn.10)) o alguna otra herramienta para generar valores de suma de comprobación. Esta estrategia también requiere que configure una directiva para determinar cuándo modificar el valor al agregar nuevos recursos localizables.

Para aplicar la suma de comprobación en inglés (Estados Unidos) a todos los archivos, puede usar cualquiera de los métodos de control de suma de comprobación descritos anteriormente. Por ejemplo, puede generar el archivo LN y el archivo de recursos específico del idioma para inglés (Estados Unidos) y, a continuación, usar el modificador MUIRCT -d para obtener la suma de comprobación resultante. Puede copiar esta suma de comprobación en el archivo de configuración de recursos y usar el modificador -q con MUIRCT para aplicar la suma de comprobación a todos los demás archivos.

### <a name="use-of-a-resource-configuration-file-with-muirct"></a>Uso de un archivo de configuración de recursos con MUIRCT

Puede especificar datos de configuración de recursos al usar MUIRCT. Independientemente de si proporciona explícitamente un archivo de configuración de recursos, cada archivo de recursos específico del lenguaje tiene datos de configuración de recursos, al igual que cualquier archivo LN con un archivo de recursos asociado. Por ejemplo:

-   Si usa el modificador -q para especificar un archivo de configuración de recursos, pero no hay recursos localizables en el archivo de origen de entrada, no se genera ningún archivo de recursos específico del lenguaje y el archivo LN resultante no contiene datos de configuración de recursos. Además, si el archivo de origen de entrada tiene recursos multilingües, MUIRCT no dividirá el archivo.

> [!Note]  
> Actualmente, el comportamiento de MUIRCT es incoherente cuando el elemento neutralResources del archivo de configuración de recursos no contiene elementos resourceType y el elemento localizedResources contiene cadenas y menús, por ejemplo. En tal caso, MUIRCT divide los recursos de la siguiente manera:
>
> -   Todos los recursos del binario original (incluidas las cadenas y los menús), además de los recursos de MUI, se colocan en el archivo LN.
> -   Las cadenas, los menús y los recursos de MUI se colocan en el archivo de recursos específico del lenguaje adecuado.

 

### <a name="examples-for-using-muirct"></a>Ejemplos de uso de MUIRCT

**Ejemplos de uso estándar**


```C++
muirct -q mui.MMF bar.exe barnew.exe barnew.exe.mui

muirct -d myprog.exe.mui
```



**Ejemplo de salida de archivo LN mediante el modificador -d**

Este es un ejemplo de la salida de datos de configuración de recursos de un archivo LN, Shell32.dll, mediante el modificador -d con MUIRCT:


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



**Ejemplo de Language-Specific salida del archivo de recursos mediante el modificador -d**

Este es un ejemplo de la salida de datos de configuración de recursos de un archivo .mui, Shell32.dll.mui, mediante el modificador -d para MUIRCT:


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



## <a name="rc-compiler-utility"></a>RC Compiler Utility

El compilador RC (Rc.exe) es una utilidad de línea de comandos para compilar un archivo de script de definición de recursos (extensión .rc) en archivos de recursos (extensión .res). El compilador RC se incluye en Windows SDK. En este documento solo se explica el uso del compilador RC con funcionalidades relacionadas con MUI del cargador de recursos. Para obtener información completa sobre el compilador, vea [Acerca de los archivos de recursos.](../menurc/about-resource-files.md)

Rc Compiler permite compilar, a partir de un único conjunto de orígenes, un archivo LN y un archivo de recursos independiente específico del lenguaje. En cuanto a MUIRCT, los archivos están asociados por datos de configuración de recursos.

### <a name="rc-compiler-syntax-as-used-for-mui-resources"></a>Sintaxis del compilador RC tal como se usa para los recursos de MUI

Los modificadores del compilador RC se definen en detalle en [Uso de RC.](../menurc/using-rc-the-rc-command-line-.md) En esta sección solo se definen los modificadores que se usan para compilar recursos de MUI. Recuerde que cada modificador no tiene en cuenta las mayúsculas y minúsculas. Se supone que los tipos de recursos son neutrales en el idioma, a menos que se indique lo contrario.


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
<td>-h|-?</td>
<td>Muestra la pantalla de ayuda.</td>
</tr>
<tr class="even">
<td>-fm</td>
<td>Usa el archivo de recursos especificado para recursos específicos del lenguaje. Normalmente, el compilador de recursos crea un archivo de recursos específico del lenguaje. Sin embargo, no crea el archivo si existe alguna de las condiciones siguientes:<br/>
<ul>
<li>No hay recursos localizables en el archivo .rc.</li>
<li>El único idioma de recursos que se encuentra en el archivo .rc es el idioma neutro.</li>
<li>El archivo .rc tiene recursos para más de un idioma, sin contar el idioma neutro. Si el archivo .rc contiene recursos para dos idiomas y uno de ellos es el idioma neutro, el compilador considera que el archivo es monolingüe. Si hay recursos localizables, el compilador crea un archivo de recursos específico del lenguaje.</li>
</ul></td>
</tr>
<tr class="odd">
<td>-q</td>
<td>Usa el archivo de configuración de recursos especificado para obtener los tipos de recursos que se colocarán en el archivo de recursos específico del lenguaje y el archivo LN. Para obtener más información, vea <a href="preparing-a-resource-configuration-file.md">Preparar un archivo de configuración de recursos.</a> Como alternativa a este modificador, puede usar los modificadores -j y -k, pero es preferible usar un archivo de configuración de recursos. <br/> Mediante el modificador -q con un archivo de configuración de recursos, puede implementar una división basada en elementos y proporcionar atributos que terminarán con la configuración de recursos binarios en el LN y el archivo de recursos específico del lenguaje. Esta división no es posible mediante los modificadores -j y -k.
<blockquote>
[!Note]<br />
El proceso de división del compilador RC no funciona correctamente si almacena recursos e información de versión en diferentes archivos de configuración de recursos. En este caso, el compilador RC no divide la información de versión. Por lo tanto, se produce un error del vinculador durante la vinculación del archivo de recursos específico del lenguaje porque el archivo no tiene recursos de versión.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td>-g</td>
<td>Especifica el identificador final <a href="language-identifiers.md">del lenguaje de reserva</a> en hexadecimal.<br/></td>
</tr>
<tr class="odd">
<td>-g1</td>
<td>Crea un archivo .res de MUI incluso si el recurso VERSION es el único contenido localizable. De forma predeterminada, el compilador rc no genera un archivo .res si VERSION es el único recurso localizable.<br/></td>
</tr>
<tr class="even">
<td>-g2</td>
<td>Especifica el número de versión personalizado que se usará al calcular la suma de comprobación.<br/></td>
</tr>
<tr class="odd">
<td>mui_res_name</td>
<td>Archivo de recursos para recursos específicos del lenguaje.<br/></td>
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



 

### <a name="example-for-using-rc-compiler-to-build-mui-resources"></a>Ejemplo de uso del compilador RC para compilar recursos de MUI

Para ilustrar la operación del compilador RC con recursos de MUI, examinemos la siguiente línea de comandos para el archivo de recursos Myfile.rc:


```C++
rc -fm myfile_res.res -q myfile.rcconfig myfile.rc
```



Esta línea de comandos hace que el compilador rc haga lo siguiente:

-   Cree el archivo de recursos específico del lenguaje Myfile res.res y un archivo de recursos con idioma neutro que se ajuste de forma predeterminada a Myfile.res, en función del nombre del \_ archivo .rc.
-   Agregue los tipos de recursos 2 (elemento 5 6 7 8 9 10 11 12), 4, 5, 6, 9, 11, 16, 23, 240, 1024 MY TYPE al archivo .res específico del lenguaje si están en el \_ archivo .rc.
-   Agregue el tipo de recurso 16, junto con cualquier otro tipo de recurso descrito en el archivo de recursos al archivo .res neutro del idioma y al archivo .res específico del lenguaje. Tenga en cuenta que, en este ejemplo, el tipo de recurso 16 se agrega en dos lugares.
-   Elija el valor del atributo "UltimateFallbackLanguage" para insertar en los datos de configuración del recurso de archivo LN en función de los criterios siguientes, ordenados de prioridad más alta a menor:
    -   Atributo "UltimateFallbackLanguage" en el archivo de configuración de recursos si se pasa uno como entrada.
    -   Valor de atributo de lenguaje que se inserta en los datos de configuración de recursos en función del orden del lenguaje del compilador RC (idioma neutro del lenguaje y lenguaje específico del lenguaje del archivo de recursos). Las consideraciones incluyen el idioma en el archivo .rc, el valor de idioma del modificador -gl y el identificador 0x0409 para inglés (Estados Unidos).

## <a name="remarks"></a>Comentarios

Si incluye algún tipo de recurso ICON(3), DIALOG(5), STRING(6) o VERSION(16) en el elemento neutralResources, tendrá que duplicar esa entrada en el elemento localizedResources en el archivo de configuración de recursos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaz de usuario multilingüe Referencia](multilingual-user-interface-reference.md)
</dt> <dt>

[Administración de recursos de LAN](mui-resource-management.md)
</dt> <dt>

[Localización de recursos y creación de la aplicación](localizing-resources-and-building-the-application.md)
</dt> </dl>

 

 
