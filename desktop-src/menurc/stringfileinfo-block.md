---
title: StringFileInfo BLOCK (instrucción)
description: Describe la forma del bloque de información de cadena.
ms.assetid: d5edf638-b70a-44d0-a43a-89d4d21e679f
keywords:
- Menús de instrucción StringFileInfo BLOCK y otros recursos
topic_type:
- apiref
api_name:
- StringFileInfo BLOCK
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 468257d0b8b8b53f3168e8e11e2f649b8354d50a76d3c2a010b98d245472aad0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886775"
---
# <a name="stringfileinfo-block-statement"></a>StringFileInfo BLOCK (instrucción)

Define un bloque de información de cadena.

``` syntax
BLOCK "StringFileInfo" { BLOCK "lang-charset" {VALUE "string-name", "value" . . . }}
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lang-charset"></span><span id="LANG-CHARSET"></span>*lang-charset*
</dt> <dd>

Par de identificadores de idioma y juego de caracteres. Es una cadena hexadecimal que consta de la concatenación del idioma y los identificadores de juego de caracteres especificados en la sección Comentarios.

</dd> <dt>

<span id="string-name"></span><span id="STRING-NAME"></span>*string-name*
</dt> <dd>

Nombre de un valor del bloque y puede ser uno de los nombres predefinidos especificados en la sección Comentarios.

</dd> <dt>

<span id="value"></span><span id="VALUE"></span>*Valor*
</dt> <dd>

Cadena de caracteres que especifica el valor del nombre de cadena correspondiente. Se puede dar más de una instrucción **VALUE.**

</dd> </dl>

## <a name="remarks"></a>Comentarios

El *parámetro lang-charset* especifica uno de los siguientes códigos de idioma.



| Código   | Idioma            | Código   | Idioma                  |
|--------|---------------------|--------|---------------------------|
| 0x0401 | Árabe              | 0x0415 | Polaco                    |
| 0x0402 | Búlgaro           | 0x0416 | Portugués (Brasil)       |
| 0x0403 | Catalán             | 0x0417 | Rhaeto-Romanic            |
| 0x0404 | Chino tradicional | 0x0418 | Rumano                  |
| 0x0405 | Checo               | 0x0419 | Ruso                   |
| 0x0406 | Danés              | 0x041A | Croato-Serbian (latino)    |
| 0x0407 | Alemán              | 0x041B | Eslovaco                    |
| 0x0408 | Griego               | 0x041C | Albanés                  |
| 0x0409 | Inglés de EE. UU.        | 0x041D | Sueco                   |
| 0x040A | Español en español   | 0x041E | Tailandés                      |
| 0x040B | Finés             | 0x041F | Turco                   |
| 0x040C | Francés              | 0x0420 | Urdu                      |
| 0x040D | Hebreo              | 0x0421 | Bahasa                    |
| 0x040E | Húngaro           | 0x0804 | Chino simplificado        |
| 0x040F | Islandés           | 0x0807 | Alemán suizo              |
| 0x0410 | Italiano             | 0x0809 | Reino Unido Inglés              |
| 0x0411 | Japonés            | 0x080A | Español (México)          |
| 0x0412 | Coreano              | 0x080C | Francés belga            |
| 0x0413 | Neerlandés               | 0x0C0C | Francés canadiense           |
| 0x0414 | Noruego: Bokmal  | 0x100C | Francés suizo              |
| 0x0810 | Italiano de Suiza       | 0x0816 | Portugués (Portugal)     |
| 0x0813 | Neerlandés neerlandés de origen neerlandés       | 0x081A | Serbo-Croatian (cirílico) |
| 0x0814 | Noruego : Nyno norwegian | ?      | ?                         |



 

El *parámetro lang-charset* también especifica uno de los siguientes identificadores de juego de caracteres.



| Identificador | Juego de caracteres              |
|------------|----------------------------|
| 0          | ASCII de 7 bits                |
| 932        | Japón (Shift – JIS X-0208) |
| 949        | Corea (Mayús – KSC 5601)   |
| 950        | Taiwán (Big5)              |
| 1200       | Unicode                    |
| 1250       | Latino 2 (Europa del Este) |
| 1251       | Cirílico                   |
| 1252       | Multilingüe               |
| 1253       | Griego                      |
| 1254       | Turco                    |
| 1255       | Hebreo                     |
| 1256       | Árabe                     |



 

El *parámetro string-name* especifica uno de los siguientes nombres predefinidos.



| Nombre                 | Descripción                                                                                                                                                                                                                                                                                                 |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Comentarios**         | Información adicional que se debe mostrar con fines de diagnóstico.                                                                                                                                                                                                                                    |
| **CompanyName**      | Empresa que produjo el archivo, por ejemplo, "Microsoft Corporation" o "Standard Microsystems Corporation, Inc". Esta cadena es obligatoria.                                                                                                                                                                   |
| **FileDescription**  | Descripción del archivo que se va a presentar a los usuarios. Esta cadena puede mostrarse en un cuadro de lista cuando el usuario elige los archivos que se instalarán, por ejemplo, "Keyboard Driver for AT-Style Keyboards". Esta cadena es obligatoria.                                                                                            |
| **FileVersion**      | Número de versión del archivo, por ejemplo, "3.10" o "5.00.RC2". Esta cadena es obligatoria.                                                                                                                                                                                                                      |
| **InternalName**     | Nombre interno del archivo, si existe, por ejemplo, un nombre de módulo si el archivo es una biblioteca de vínculos dinámicos. Si el archivo no tiene ningún nombre interno, esta cadena debe ser el nombre de archivo original, sin extensión. Esta cadena es obligatoria.                                                                       |
| **LegalCopyright**   | Avisos de copyright que se aplican al archivo. Esto debe incluir el texto completo de todos los avisos, símbolos legales, fechas de copyright, y así sucesivamente. Esta cadena es opcional.                                                                                                                                             |
| **LegalTrademarks**  | Marcas comerciales y marcas comerciales registradas que se aplican al archivo. Esto debe incluir el texto completo de todos los avisos, símbolos legales, números de marcas comerciales, etc. Esta cadena es opcional.                                                                                                                        |
| **OriginalFilename** | Nombre original del archivo, sin incluir una ruta de acceso. Esta información permite a una aplicación determinar si un usuario ha cambiado el nombre de un archivo. El formato del nombre depende del sistema de archivos para el que se creó el archivo. Esta cadena es obligatoria.                                                 |
| **PrivateBuild**     | Información sobre una versión privada del archivo, por ejemplo, "Built by TESTER1 on \\ TESTBED". Esta cadena solo debe estar presente si se especifica **\_ VS FF \_ PRIVATEBUILD** en el *parámetro fileflags* del bloque raíz.                                                                                   |
| **ProductName**      | Nombre del producto con el que se distribuye el archivo. Esta cadena es obligatoria.                                                                                                                                                                                                                            |
| **ProductVersion**   | Versión del producto con el que se distribuye el archivo, por ejemplo, "3.10" o "5.00.RC2". Esta cadena es obligatoria.                                                                                                                                                                                       |
| **SpecialBuild**     | Texto que especifica cómo difiere esta versión del archivo de la versión estándar, por ejemplo, "Compilación privada para TESTER1 que resuelve problemas del mouse en equipos M250 y M250E". Esta cadena solo debe estar presente si se especifica **VS \_ FF \_ SPECIALBUILD** en el *parámetro fileflags* del bloque raíz. |



 

 

 




