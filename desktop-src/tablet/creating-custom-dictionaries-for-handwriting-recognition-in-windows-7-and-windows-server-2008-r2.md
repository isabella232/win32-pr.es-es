---
description: En esta sección se explica cómo crear un diccionario personalizado para el reconocimiento de escritura a mano.
ms.assetid: 83abf534-740c-44a3-bbd4-babb54f2930e
title: Crear diccionarios personalizados para el reconocimiento de escritura a mano en Windows 7 y Windows Server 2008 R2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80b9b7b5a1d9dfadddd83825aea7d6f676439999
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696209"
---
# <a name="creating-custom-dictionaries-for-handwriting-recognition-in-windows-7-and-windows-server-2008-r2"></a>Crear diccionarios personalizados para el reconocimiento de escritura a mano en Windows 7 y Windows Server 2008 R2

En esta sección se explica cómo crear un diccionario personalizado para el reconocimiento de escritura a mano.

En el sistema operativo Windows 7 y el sistema operativo Windows Server 2008 R2, la precisión del reconocimiento de escritura a mano se puede mejorar significativamente mediante el uso de diccionarios personalizados. Estos diccionarios complementan o reemplazan diccionarios del sistema usados para escritura a mano. La compatibilidad con el reconocimiento de escritura a mano se proporciona a través de la característica Servicios de Escritura con lápiz y Escritura a mano que debe habilitarse a través de Administrador del servidor.

> [!Note]  
> Los diccionarios personalizados solo se pueden instalar para un idioma si el reconocedor de escritura a mano para ese idioma está instalado.

 

Hay dos pasos básicos para configurar un diccionario personalizado para escritura a mano:

-   Compilar una lista de palabras. La compilación crea un archivo de diccionario personalizado (. hwrdict) compilado.
-   Instale el diccionario personalizado compilado.

## <a name="compiling-a-word-list"></a>Compilar una lista de palabras

La lista de palabras que se va a compilar debe estar en formato de texto sin formato y debe guardarse con una codificación Unicode. Otras codificaciones no funcionarán. Cada línea del archivo de texto se toma como una sola entrada en el diccionario. Se permiten las entradas de unidades multipalabra que contienen uno o varios espacios. Se omiten los espacios al principio o al final de una línea.

Un diccionario personalizado se compila desde una línea de comandos. Para compilar un diccionario, abra una ventana de comandos, navegue hasta la carpeta que contiene la lista de palabras y, a continuación, ejecute HwrComp.exe con las opciones de línea de comandos que desea utilizar.

En el ejemplo siguiente se muestra la sintaxis de uso de las opciones de la línea de comandos.

``` syntax
Usage: hwrcomp       [-lang <localename>] [-type <type>]
    [-comment <comment>]
    [-o <dictfile.hwrdict>]
    <inputfile>
     
```

### <a name="explanation-of-options"></a>Explicación de las opciones



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Parámetro</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>-lang <localename></td>
<td>Nombre de configuración regional especificado que se ha asignado al archivo de diccionario personalizado compilado. El argumento <localename> tiene el formato Language-region. Un ejemplo de esto es en-US, que indica el idioma Inglés de la región de Estados Unidos. Para obtener ejemplos de este formulario, consulte [constantes y cadenas de identificador de idioma](/windows/desktop/Intl/language-identifier-constants-and-strings). Los siguientes idiomas son compatibles con Windows 7 y Windows Server 2008 R2 gracias a esta característica: en-US, en-GB, en-CA, en-AU, de-DE, de-CH, fr-FR, es-ES, es-MX, es-AR, it-IT, nl-NL, nl-is, pt-BR, pt-PT, da-DK, SV-SE, NB-NO, NN-NO, fi-FI, pl-PL, CS-CZ, ru-RU, RO-RO, Sr-Latn-CS, Sr-Cyrl-CS, CA-ES y hr-HR.<br/></td>
</tr>
<tr class="even">
<td>-Type <type></td>
<td>El argumento de opción <type> es una concatenación de cadena única del uso del recurso como la lista de palabras principales (principal) o como un complemento de la lista de palabras principales (secundaria) seguida del nombre de lista de palabras real al que se aplica el recurso (como diccionario o apellidos). Estos son los valores posibles:
<ul>
<li>PRIMARY-CITYNAME-LIST</li>
<li>PRIMARY-COUNTRYNAME-LIST</li>
<li>PRIMARY-COUNTRYSHORTNAME-LIST</li>
<li>DICCIONARIO PRINCIPAL</li>
<li>PRIMARY-GIVENNAME-LIST</li>
<li>PRIMARY-STATEORPROVINCE-LIST</li>
<li>PRIMARY-STREETNAME-LIST</li>
<li>LISTA DE PRINCIPALES APELLIDOS</li>
<li>SECUNDARIO-CITYNAME-LIST</li>
<li>SECUNDARIO-COUNTRYNAME-LIST</li>
<li>SECUNDARIO-COUNTRYSHORTNAME-LIST</li>
<li>DICCIONARIO SECUNDARIO</li>
<li>SECUNDARIO-EMAILSMTP-LIST</li>
<li>SECUNDARIO-EMAILUSERNAME-LIST</li>
<li>SECUNDARIA-GIVENNAME-LIST</li>
<li>SECUNDARIO-STATEORPROVINCE-LIST</li>
<li>SECUNDARIO-STREETNAME-LIST</li>
<li>LISTA DE APELLIDOS SECUNDARIOS</li>
<li>LISTA DE DIRECCIONES URL SECUNDARIAS</li>
</ul>
Si un valor de tipo comienza con el prefijo PRIMAry, el Diccionario compilado, una vez instalado, reemplazará el Diccionario del sistema para ese idioma. El valor del diccionario PRIMAry-DICTIONARY representa el Diccionario del sistema principal para un idioma.
<blockquote>
[!Note]<br />
Reemplazar un diccionario del sistema no hace nada en el contenido del Diccionario del sistema original, ya que el reemplazo solo está en vigor hasta que se haya quitado el diccionario personalizado.
</blockquote>
<br/> Si un valor de tipo comienza con el prefijo secundario, el Diccionario compilado complementará el Diccionario del sistema sin reemplazarlo.</td>
</tr>
<tr class="odd">
<td>-Comentario <comment></td>
<td>El comentario especificado se compila en el archivo del diccionario. El comentario debe ser una cadena única y no tener más de 64 caracteres.</td>
</tr>
<tr class="even">
<td>-o <dictfile.hwrdict></td>
<td>La salida se escribe en el nombre de archivo especificado por <dictfile.hwrdict> .<br/> Si falta esta opción, el nombre del archivo de salida se deriva del nombre del archivo de entrada original, con la extensión de archivo de entrada reemplazada por. hwrdict.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="defaults"></a>Valores predeterminados

Si no se especifican parámetros, los valores de opción predeterminados son

-lang <current input language> -tipo secundario-Diccionario

### <a name="examples"></a>Ejemplos

El siguiente compila el archivo de entrada mylist1.txt, aplica los valores de opción predeterminados y crea el archivo de salida mylist1. hwrdict.

``` syntax
hwrcomp mylist1.txt
```

En cambio, el siguiente compila mylist1.txt en myrsrc1. hwrdict, pero asigna "English (EE. UU.)" (en-US) como el idioma y el Diccionario secundario como tipo.

``` syntax
hwrcomp -lang en-US -type SECONDARY-DICTIONARY -o myrsrc1 mylist1.txt 
```

## <a name="installing-a-compiled-custom-dictionary"></a>Instalación de un diccionario personalizado compilado

HwrComp.exe crea un archivo. hwrdict, que se encuentra en un formato binario que puede usar un reconocedor de escritura a mano. Este archivo se puede instalar en cualquier equipo que ejecute Windows 7 o Windows Server 2008 R2 y que admita el reconocimiento de escritura a mano. Un diccionario se instala solo para el usuario actual o para todos los usuarios de un equipo.

Un archivo de diccionario personalizado compilado se puede instalar desde la línea de comandos mediante el HwrReg.exe de herramientas. Esta herramienta es útil si desea invalidar algunos de los valores de configuración que se compilan en el archivo o son los valores predeterminados. Hay dos maneras de ejecutar HwrReg.exe: en modo de comprobación e instalación y en modo de lista/eliminación.

### <a name="running-hwrregexe-in-checkinstall-mode"></a>Ejecutar HwrReg.exe en modo de comprobación/instalación

Este modo es para los archivos de diccionario personalizados que todavía no se han instalado. A continuación se muestra la sintaxis de uso de las opciones de la línea de comandos.

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
| -comprobar                   | El archivo de diccionario se comprueba sin instalarse. La opción check muestra el comentario del archivo, además de la información de registro que se utilizaría para instalar el archivo. Esta opción es útil para comprobar la información de registro antes de que se realice la instalación. <br/> Si falta esta opción, HwrReg.exe instala el diccionario personalizado.<br/>  |
|  lang <localename> | El archivo de diccionario se comprueba sin instalarse. La opción check muestra el comentario del archivo, además de la información de registro que se utilizaría para instalar el archivo. Esta opción es útil para comprobar la información de registro antes de que se realice la instalación. <br/> Si falta esta opción, HwrReg.exe instala el diccionario personalizado. <br/> |
|  ámbito {todo \| me}         | El diccionario personalizado se instala para todos los usuarios (ámbito todos) o solo para el usuario actual (ámbito me). La instalación de con el ámbito All requiere que el comando se ejecute en un símbolo del sistema con privilegios elevados. de lo contrario, se devolverá un código de error. <br/> Si falta esta opción, el ámbito de la instalación es solo el usuario actual.<br/>                          |
|  noprompt                | HwrReg.exe no solicita confirmación. Esto puede ser útil cuando se ejecuta hwrReg.exe desde un script. <br/>                                                                                                                                                                                                                                                                 |



 

En el ejemplo siguiente se instala el diccionario personalizado myrsrc1. hwrdict para el idioma "danés (Dinamarca)" (da DK), con el ámbito predeterminado del usuario actual.

``` syntax
hwrreg -lang da-DK myrsrc1.hwrdict 
```

### <a name="running-hwrregexe-in-listremove-mode"></a>Ejecutar HwrReg.exe en modo List/Remove

En este modo se enumeran o se quitan los diccionarios personalizados instalados. A continuación se muestra la sintaxis de uso de las opciones de la línea de comandos.

``` syntax
Usage: hwrreg        [-lang <localename>] 
    [-scope {all|me}] 
    [-type <type>]
    -list | -remove
```

### <a name="explanation-of-options"></a>Explicación de las opciones



| Parámetro                | Descripción                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  lang <localename> | Los diccionarios registrados solo para este nombre de configuración regional se muestran o se quitan. El argumento <localename> tiene la región de idioma del formulario. Para obtener ejemplos de este formulario, consulte [constantes y cadenas de identificador de idioma](/windows/desktop/Intl/language-identifier-constants-and-strings). <br/> Si falta esta opción, los diccionarios de todos los idiomas se muestran o se quitan.<br/> |
|  ámbito {todo \| me}         | El diccionario personalizado se instala para todos los usuarios (ámbito todos) o solo para el usuario actual (ámbito me). La instalación de con el ámbito All requiere que el comando se ejecute en un símbolo del sistema con privilegios elevados. de lo contrario, se devolverá un código de error. <br/> Si falta esta opción, el ámbito de la instalación es solo el usuario actual.<br/>                      |
|  automáticamente <type>       | Muestra o quita solo los diccionarios registrados con el tipo especificado.<br/> Si falta esta opción, todos los tipos de diccionario se enumeran o se quitan. La instalación o eliminación de un diccionario personalizado de otro tipo (como PRIMAry-COUNTRYNAME-LIST) puede afectar al reconocimiento de escritura a mano en otros contextos. <br/>                                              |
|  list                    | Enumera todos los diccionarios instalados que coinciden con las demás opciones.<br/> Si falta esta opción, se debe especificar la opción Remove.<br/>                                                                                                                                                                                                                          |
|  remove                  | Solicita la eliminación de cualquier Diccionario que coincida con las demás opciones.<br/> Si falta esta opción, se debe especificar la lista de opciones.<br/>                                                                                                                                                                                                                     |



 

### <a name="examples"></a>Ejemplos

A continuación se enumeran los diccionarios que tienen el idioma "inglés (EE. UU.)" (en Estados Unidos) y el tipo Diccionario primario y que están instalados solo para el usuario actual.

``` syntax
hwrreg -list -lang en-US -type PRIMARY-DICTIONARY
                  
```

Del mismo modo, el siguiente quita los diccionarios que coinciden con los mismos criterios.

``` syntax
hwrreg -remove -lang en-US -type PRIMARY-DICTIONARY
                  
```

## <a name="general-notes-on-custom-dictionaries"></a>Notas generales sobre diccionarios personalizados

-   Si instala dos diccionarios personalizados que tienen el mismo tipo, idioma y ámbito, la segunda instalación sobrescribirá el primero.
-   Si instala dos diccionarios personalizados con el mismo tipo y lenguaje, pero con ámbitos diferentes (uno para todos los usuarios y uno para el usuario actual), el Diccionario instalado para el usuario actual tiene prioridad y se omite el Diccionario instalado para todos los usuarios.

 

