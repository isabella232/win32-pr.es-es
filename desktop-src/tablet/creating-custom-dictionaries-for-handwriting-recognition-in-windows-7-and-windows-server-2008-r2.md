---
description: En esta sección se explica cómo crear un diccionario personalizado para el reconocimiento de escritura a mano.
ms.assetid: 83abf534-740c-44a3-bbd4-babb54f2930e
title: Creación de diccionarios personalizados para el reconocimiento de escritura a mano en Windows 7 y Windows Server 2008 R2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fe391125b21bfe35a9e1a69be6258e1643b424e
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883891"
---
# <a name="creating-custom-dictionaries-for-handwriting-recognition-in-windows-7-and-windows-server-2008-r2"></a>Creación de diccionarios personalizados para el reconocimiento de escritura a mano en Windows 7 y Windows Server 2008 R2

En esta sección se explica cómo crear un diccionario personalizado para el reconocimiento de escritura a mano.

En el sistema operativo Windows 7 y el sistema operativo Windows Server 2008 R2, la precisión del reconocimiento de escritura a mano se puede mejorar significativamente mediante el uso de diccionarios personalizados. Estos diccionarios complementan o reemplazan los diccionarios del sistema que se usan para la escritura a mano. La compatibilidad con el reconocimiento de escritura a mano se proporciona a través Servicios de Escritura con lápiz y Escritura a mano característica que debe habilitarse a través de Administrador del servidor.

> [!Note]  
> Los diccionarios personalizados solo se pueden instalar para un idioma si está instalado el reconocedor de escritura a mano para ese idioma.

 

Hay dos pasos básicos para configurar un diccionario personalizado para la escritura a mano:

-   Compile una lista de palabras. La compilación crea un archivo de diccionario personalizado compilado (.hwrdict).
-   Instale el diccionario personalizado compilado.

## <a name="compiling-a-word-list"></a>Compilar una lista de palabras

La lista de palabras que se va a compilar debe estar en formato de texto sin formato y debe guardarse mediante una codificación Unicode. Otras codificaciones no funcionarán. Cada línea del archivo de texto se toma como una sola entrada en el diccionario. Se permiten entradas de unidades de varias palabras que contienen uno o varios espacios. Se omiten los espacios al principio o al final de una línea.

Un diccionario personalizado se compila desde una línea de comandos. Para compilar un diccionario, abra una ventana de comandos, vaya a la carpeta que contiene la lista de palabras y, a continuación, ejecute HwrComp.exe con las opciones de línea de comandos que desea usar.

En el ejemplo siguiente se muestra la sintaxis de uso para las opciones de línea de comandos.

``` syntax
Usage: hwrcomp       [-lang <localename>] [-type <type>]
    [-comment <comment>]
    [-o <dictfile.hwrdict>]
    <inputfile>
     
```

### <a name="explanation-of-options"></a>Explicación de las opciones



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Parámetro</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>-lang &lt; localename&gt;</td>
<td>Nombre de configuración regional especificado asignado al archivo de diccionario personalizado compilado. El argumento &lt; localename &gt; tiene el formato language-REGION. Un ejemplo de esto es en-US, que significa el idioma inglés en Estados Unidos región. Para obtener ejemplos de este formulario, vea [Language Identifier Constants and Strings](/windows/desktop/Intl/language-identifier-constants-and-strings). Esta característica admite los siguientes idiomas para Windows 7 y Windows Server 2008 R2: en-US, en-GB, en-CA, en-AU, de-DE, de-CH, fr-FR, es-ES, es-MX, es-AR, it-IT, nl-NL, nl-BE, pt-BR, pt-PT, da-DK, sv-SE, nb-NO, nn-NO, fi-FI, pl-PL, cs-NB, ru-RU, ro-RO, sr-Latn-CS, sr-Cyrl-CS, ca-ES y hr-HR.<br/></td>
</tr>
<tr class="even">
<td>-type &lt; type&gt;</td>
<td>El tipo de argumento de opción es una concatenación de una sola cadena del uso del recurso como la lista de palabras principales (PRIMARY) o como complemento de la lista de palabras principales (SECONDARY) seguida del nombre real de la lista de palabras al que se aplica el recurso &lt; &gt; (por ejemplo, DICTIONARY o SURNAME). Estos son los valores posibles:
<ul>
<li>PRIMARY-CITYNAME-LIST</li>
<li>PRIMARY-COUNTRYNAME-LIST</li>
<li>PRIMARY-COUNTRYSHORTNAME-LIST</li>
<li>DICCIONARIO PRINCIPAL</li>
<li>PRIMARY-GIVENNAME-LIST</li>
<li>PRIMARY-STATEORPROVINCE-LIST</li>
<li>PRIMARY-STREETNAME-LIST</li>
<li>PRIMARY-SURNAME-LIST</li>
<li>SECONDARY-CITYNAME-LIST</li>
<li>SECONDARY-COUNTRYNAME-LIST</li>
<li>SECONDARY-COUNTRYSHORTNAME-LIST</li>
<li>DICCIONARIO SECUNDARIO</li>
<li>SECONDARY-EMAILSMTP-LIST</li>
<li>SECONDARY-EMAILUSERNAME-LIST</li>
<li>SECONDARY-GIVENNAME-LIST</li>
<li>SECONDARY-STATEORPROVINCE-LIST</li>
<li>SECONDARY-STREETNAME-LIST</li>
<li>SECONDARY-SURNAME-LIST</li>
<li>SECONDARY-URL-LIST</li>
</ul>
Si un valor de tipo comienza con el prefijo PRIMARY, el diccionario compilado, una vez instalado, reemplazará el diccionario del sistema para ese idioma. El valor PRIMARY-DICTIONARY representa el diccionario del sistema principal de un idioma.
<blockquote>
[!Note]<br />
Reemplazar un diccionario del sistema no hace nada en el contenido original del diccionario del sistema, ya que el reemplazo solo está en vigor hasta que se haya quitado el diccionario personalizado.
</blockquote>
<br/> Si un valor de tipo comienza con el prefijo SECONDARY, el diccionario compilado complementará el diccionario del sistema sin reemplazarlo.</td>
</tr>
<tr class="odd">
<td>-comment <comment></td>
<td>El comentario especificado se compila en el archivo de diccionario. El comentario debe ser una sola cadena y no tener más de 64 caracteres.</td>
</tr>
<tr class="even">
<td>-o <dictfile.hwrdict></td>
<td>La salida se escribe en el nombre de archivo especificado por <dictfile.hwrdict> .<br/> Si falta esta opción, el nombre del archivo de salida se deriva del nombre de archivo de entrada original, con la extensión de archivo de entrada reemplazada por .hwrdict.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="defaults"></a>Valores predeterminados

Si no se especifica ningún parámetro, los valores de opción predeterminados son

-lang <current input language> -type SECONDARY-DICTIONARY

### <a name="examples"></a>Ejemplos

A continuación se compila el archivo de mylist1.txt, se aplican los valores de opción predeterminados y se crea el archivo de salida mylist1.hwrdict.

``` syntax
hwrcomp mylist1.txt
```

En cambio, lo siguiente compila mylist1.txt en myrsrc1.hwrdict, pero asigna "Inglés (EE. UU.)" (en-US) como idioma y SECONDARY-DICTIONARY como tipo.

``` syntax
hwrcomp -lang en-US -type SECONDARY-DICTIONARY -o myrsrc1 mylist1.txt 
```

## <a name="installing-a-compiled-custom-dictionary"></a>Instalación de un diccionario personalizado compilado

HwrComp.exe crea un archivo .hwrdict, que está en un formato binario que puede ser usado por un reconocedor de escritura a mano. Este archivo se puede instalar en cualquier equipo que ejecute Windows 7 o Windows Server 2008 R2 que admita el reconocimiento de escritura a mano. Se instala un diccionario solo para el usuario actual o para todos los usuarios de una máquina.

Se puede instalar un archivo de diccionario personalizado compilado desde la línea de comandos mediante la herramienta HwrReg.exe. Esta herramienta es útil si desea invalidar algunos de los valores de configuración que se compilan en el archivo o son los valores predeterminados. Hay dos maneras de ejecutar HwrReg.exe: en modo de comprobación/instalación y en modo de lista o eliminación.

### <a name="running-hwrregexe-in-checkinstall-mode"></a>Ejecución HwrReg.exe en modo de comprobación/instalación

Este modo es para archivos de diccionario personalizados que aún no se han instalado. A continuación se muestra la sintaxis de uso para las opciones de línea de comandos.

``` syntax
Usage: hwrreg        [-check]
    [-lang <localename>] 
    [-scope {all|me}]
    [-noprompt] 
    <dictfile.hwrdict>
```

### <a name="explanation-of-options"></a>Explicación de las opciones



| Parámetro                | Descripción                                                                                                                                                                                                                                                                                                                                                                        |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| -check                   | El archivo de diccionario se comprueba sin instalarse. La opción check muestra el comentario del archivo, además de la información de registro que se usaría para instalar el archivo. Esta opción es útil para comprobar la información de registro antes de realizar la instalación. <br/> Si falta esta opción, HwrReg.exe el diccionario personalizado.<br/>  |
|  lang &lt; localename&gt; | El archivo de diccionario se comprueba sin instalarse. La opción check muestra el comentario del archivo, además de la información de registro que se usaría para instalar el archivo. Esta opción es útil para comprobar la información de registro antes de realizar la instalación. <br/> Si falta esta opción, HwrReg.exe el diccionario personalizado. <br/> |
|  scope {all \| me}         | El diccionario personalizado se instala para todos los usuarios (ámbito all) o solo para el usuario actual (scope me). La instalación con ámbito requiere que el comando se ejecute en un símbolo del sistema con privilegios elevados. De lo contrario, se devolverá un código de error. <br/> Si falta esta opción, el ámbito de la instalación es solo el usuario actual.<br/>                          |
|  noprompt                | HwrReg.exe no solicita confirmación. Esto puede ser útil al ejecutar hwrReg.exe desde un script. <br/>                                                                                                                                                                                                                                                                 |



 

En el ejemplo siguiente se instala el diccionario personalizado myrsrc1.hwrdict para el idioma "Danés (Dinamarca)" (da DK), con el ámbito predeterminado solo del usuario actual.

``` syntax
hwrreg -lang da-DK myrsrc1.hwrdict 
```

### <a name="running-hwrregexe-in-listremove-mode"></a>Ejecución HwrReg.exe en modo de lista o eliminación

Este modo enumera o quita los diccionarios personalizados instalados. A continuación se muestra la sintaxis de uso para las opciones de línea de comandos.

``` syntax
Usage: hwrreg        [-lang <localename>] 
    [-scope {all|me}] 
    [-type <type>]
    -list | -remove
```

### <a name="explanation-of-options"></a>Explicación de las opciones



| Parámetro                | Descripción                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  lang &lt; localename&gt; | Los diccionarios registrados solo para este nombre de configuración regional se enumeran o quitan. El argumento &lt; localename &gt; tiene el idioma del formulario REGION. Para obtener ejemplos de este formulario, vea [Language Identifier Constants and Strings](/windows/desktop/Intl/language-identifier-constants-and-strings). <br/> Si falta esta opción, se muestran o quitan diccionarios para todos los idiomas.<br/> |
|  scope {all \| me}         | El diccionario personalizado se instala para todos los usuarios (ámbito all) o solo para el usuario actual (scope me). La instalación con ámbito requiere que el comando se ejecute en un símbolo del sistema con privilegios elevados. De lo contrario, se devolverá un código de error. <br/> Si falta esta opción, el ámbito de la instalación es solo el usuario actual.<br/>                      |
|  tipo &lt; de tipo&gt;       | Enumera o quita solo los diccionarios registrados con el tipo especificado.<br/> Si falta esta opción, se enumeran o quitan todos los tipos de diccionario. La instalación o eliminación de un diccionario personalizado de otro tipo (como PRIMARY-COUNTRYNAME-LIST) puede afectar al reconocimiento de escritura a mano en otros contextos. <br/>                                              |
|  list                    | Enumera todos los diccionarios instalados que coinciden con las demás opciones.<br/> Si falta esta opción, se debe especificar la opción remove.<br/>                                                                                                                                                                                                                          |
|  remove                  | Solicita la eliminación de cualquier diccionario que coincida con las demás opciones.<br/> Si falta esta opción, se debe especificar la lista de opciones.<br/>                                                                                                                                                                                                                     |



 

### <a name="examples"></a>Ejemplos

A continuación se enumeran los diccionarios que tienen el idioma "Inglés (EE. UU.)" (en EE. UU.) y el tipo DICCIONARIO PRINCIPAL y que están instalados solo para el usuario actual.

``` syntax
hwrreg -list -lang en-US -type PRIMARY-DICTIONARY
                  
```

De forma similar, lo siguiente quita los diccionarios que coinciden con los mismos criterios.

``` syntax
hwrreg -remove -lang en-US -type PRIMARY-DICTIONARY
                  
```

## <a name="general-notes-on-custom-dictionaries"></a>Notas generales sobre diccionarios personalizados

-   Si instala dos diccionarios personalizados que tienen el mismo tipo, idioma y ámbito, la segunda instalación sobrescribirá la primera.
-   Si instala dos diccionarios personalizados con el mismo tipo e idioma, pero con ámbitos diferentes (uno para todos los usuarios y otro para el usuario actual), el diccionario instalado para el usuario actual tiene prioridad y se omite el diccionario instalado para todos los usuarios.

 

