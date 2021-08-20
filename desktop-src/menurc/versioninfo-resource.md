---
title: Recurso VERSIONINFO
description: Define un recurso de información de versión. El recurso contiene dicha información sobre el archivo como su número de versión, su sistema operativo previsto y su nombre de archivo original. El recurso está pensado para usarse con las funciones de información de versión.
ms.assetid: be4fbf3d-ca30-4de1-b17a-691a316edfad
keywords:
- Menús de recursos VERSIONINFO y otros recursos
topic_type:
- apiref
api_name:
- VERSIONINFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6708b4fefc564685a9989140e5f07dd20714e8bbcb60c53710f43cbfee4aa7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971874"
---
# <a name="versioninfo-resource"></a>Recurso VERSIONINFO

Define un recurso de información de versión. El recurso contiene dicha información sobre el archivo como su número de versión, su sistema operativo previsto y su nombre de archivo original. El recurso está pensado para usarse con las funciones [de información de versión.](./version-information.md)

Hay dos maneras de dar formato a **una instrucción VERSIONINFO:**

``` syntax
versionID VERSIONINFO fixed-info  { block-statement . . . }
```

\- O bien

``` syntax
versionID VERSIONINFO 
fixed-info
BEGIN
block-statement
. . .
END
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="versionID"></span><span id="versionid"></span><span id="VERSIONID"></span>*versionID*
</dt> <dd>

Identificador de recurso de información de versión. Este valor debe ser 1.

</dd> <dt>

<span id="fixed-info"></span><span id="FIXED-INFO"></span>*fixed-info*
</dt> <dd>

Información de versión, como la versión del archivo y el sistema operativo previsto. Este parámetro consta de las siguientes instrucciones.



| .                         | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Versión de FILEVERSION**          | Número de versión binaria del archivo. La *versión* consta de dos enteros de 32 bits, definidos por cuatro enteros de 16 bits. Por ejemplo, "FILEVERSION 3,10,0,61" se traduce en dos palabras dobles: 0x0003000a y 0x0000003d, en ese orden. Por lo *tanto,* si la versión se define mediante los valores **DWORD** *dw1* y *dw2*, deben aparecer en la **instrucción FILEVERSION** de la siguiente manera: `HIWORD(dw1)` , , , `LOWORD(dw1)` `HIWORD(dw2)` `LOWORD(dw2)` . |
| **Versión de PRODUCTVERSION**       | Número de versión binaria del producto con el que se distribuye el archivo. El *parámetro* version es dos enteros de 32 bits, definidos por cuatro enteros de 16 bits. Para obtener más información sobre *la versión*, vea la descripción **de FILEVERSION.**                                                                                                                                                                                                           |
| **FILEFLAGSMASK** *fileflagsmask* | Indica qué bits de la **instrucción FILEFLAGS** son válidos. En el caso de las Windows de 16 bits, este valor es 0x3f.                                                                                                                                                                                                                                                                                                                                          |
| **FileFLAGS** *fileflags*         | Atributos del archivo.                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **FILEOS** *fileos*               | Sistema operativo para el que se diseñó este archivo. El *parámetro fileos* puede ser uno de los valores del sistema operativo especificados en la sección Comentarios.                                                                                                                                                                                                                                                                                               |
| **FileTYPE filetype**            | Tipo general de archivo. El *parámetro filetype* puede ser uno de los valores de tipo de archivo enumerados en la sección Comentarios.                                                                                                                                                                                                                                                                                                                                |
| **Subtipo FILESUBTYPE**          | Función del archivo. El *parámetro de subtipo* es cero a menos que el parámetro *filetype* de la instrucción **FILETYPE** sea VFT \_ DRV, VFT FONT o \_ VFT \_ VXD. Para obtener una lista de valores de subtipo de archivo, vea la sección Comentarios.                                                                                                                                                                                                                            |



 

</dd> <dt>

<span id="block-statement"></span><span id="BLOCK-STATEMENT"></span>*block-statement*
</dt> <dd>

Especifica uno o varios bloques de información de versión. Un bloque puede contener información de cadena o información de variables. Para obtener más información, [**vea StringFileInfo Block**](stringfileinfo-block.md) o [**VarFileInfo Block**](varfileinfo-block.md).

</dd> </dl>

## <a name="remarks"></a>Comentarios

Para usar las constantes especificadas con la **instrucción VERSIONINFO,** debe incluir el archivo de encabezado Winver.h o Windows.h en el archivo de definición de recursos.

En la lista siguiente se describen los parámetros utilizados en la **instrucción VERSIONINFO:**

<dl> <dt>

<span id="fileflags"></span><span id="FILEFLAGS"></span>*fileflags*
</dt> <dd>

Combinación de los valores siguientes.



| Value                      | Descripción                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **VS \_ FF \_ DEBUG**          | El archivo contiene información de depuración o se compila con las características de depuración habilitadas.                                                                                                                                                                                         |
| **VS \_ FF \_ PATCHED**        | El archivo se ha modificado y no es idéntico al archivo de envío original del mismo número de versión.                                                                                                                                                                       |
| **VERSIÓN PRELIMINAR DE VS \_ FF \_**     | El archivo es una versión de desarrollo, no un producto publicado comercialmente.                                                                                                                                                                                                         |
| **VS \_ FF \_ PRIVATEBUILD**   | El archivo no se creó mediante procedimientos de versión estándar. Si se proporciona este valor, el [**bloque StringFileInfo**](stringfileinfo-block.md) debe contener una **cadena PrivateBuild.**                                                                                              |
| **VS \_ FF \_ SPECIALBUILD**   | El archivo lo creó la empresa original mediante procedimientos de versión estándar, pero es una variación del archivo estándar del mismo número de versión. Si se proporciona este valor, el bloque de bloque [ **StringFileInfo**](stringfileinfo-block.md) debe contener una **cadena SpecialBuild.** |
| **VS \_ FFI \_ FILEFLAGSMASK** | Combinación de todos los valores anteriores.                                                                                                                                                                                                                                  |



 

</dd> <dt>

<span id="fileos"></span><span id="FILEOS"></span>*fileos*
</dt> <dd>

Uno de los siguientes valores.



| Valor                   | Descripción                                                      |
|-------------------------|------------------------------------------------------------------|
| **NO \_ SE CONOCE LA**        | Se desconoce el sistema operativo para el que se diseñó el archivo. |
| **\_2017**            | El archivo se diseñó para MS-DOS.                                    |
| **NOCIONES \_ NT**             | El archivo se diseñó para archivos de 32 Windows.                            |
| **PARA WINDOWS \_ \_ 16**    | El archivo se diseñó para archivos de 16 Windows.                            |
| **PARA WINDOWS 32 DE LA VERSIÓN \_ \_ 32**    | El archivo se diseñó para archivos de 32 Windows.                            |
| **16 DE AGOSTO \_ \_ DE 2016** | El archivo se diseñó para archivos de 16 Windows que se ejecutan con MS-DOS.        |
| **SEGO \_ DOS \_ WINDOWS32** | El archivo se diseñó para archivos de 32 Windows se ejecuta con MS-DOS.        |
| **SE \_ NT \_ WINDOWS32**  | El archivo se diseñó para archivos de 32 Windows.                            |



 

Los valores 0x00002L, 0x00003L, 0x20000L y 0x30000L están reservados.

</dd> <dt>

<span id="filetype"></span><span id="FILETYPE"></span>*Eltipo*
</dt> <dd>

Uno de los siguientes valores.



| Valor                | Descripción                                                                                                                 |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------|
| **VFT \_ UNKNOWN**     | El tipo de archivo es desconocido.                                                                                                       |
| **APLICACIÓN \_ VFT**         | El archivo contiene una aplicación.                                                                                               |
| **DLL \_ de VFT**         | El archivo contiene una biblioteca de vínculos dinámicos (DLL).                                                                                 |
| **VFT \_ DRV**         | El archivo contiene un controlador de dispositivo. Si *filetype* es **VFT \_ DRV,** *el subtipo* contiene una descripción más específica del controlador. |
| **FUENTE \_ VFT**        | El archivo contiene una fuente. Si *filetype* es VFT \_ FONT, *el subtipo* contiene una descripción más específica de la fuente.               |
| **VFT \_ VXD**         | El archivo contiene un dispositivo virtual.                                                                                             |
| **BIBLIOTECA ESTÁTICA DE VFT \_ \_** | El archivo contiene una biblioteca de vínculos estáticos.                                                                                        |



 

Todos los demás valores están reservados para su uso por Parte de Microsoft.

</dd> <dt>

<span id="subtype"></span><span id="SUBTYPE"></span>*Subtipo*
</dt> <dd>

Información adicional sobre el tipo de archivo.

Si *filetype* especifica **VFT \_ DRV,** este parámetro puede ser uno de los valores siguientes.



| Value                             | Descripción                               |
|-----------------------------------|-------------------------------------------|
| **VFT2 \_ UNKNOWN**                 | El tipo de controlador es desconocido.                   |
| **VFT2 \_ DRV \_ COMM**               | El archivo contiene un controlador de comunicaciones.    |
| **IMPRESORA \_ DRV VFT2 \_**            | El archivo contiene un controlador de impresora.           |
| **TECLADO \_ DRV de VFT2 \_**           | El archivo contiene un controlador de teclado.          |
| **LENGUAJE \_ DRV VFT2 \_**           | El archivo contiene un controlador de lenguaje.          |
| **VFT2 \_ DRV \_ DISPLAY**            | El archivo contiene un controlador para mostrar.           |
| **MOUSE DE \_ DRV de VFT2 \_**              | El archivo contiene un controlador del mouse.             |
| **VFT2 \_ DRV \_ NETWORK**            | El archivo contiene un controlador de red.           |
| **VFT2 \_ DRV \_ SYSTEM**             | El archivo contiene un controlador del sistema.            |
| **VFT2 \_ DRV \_ INSTALABLE**        | El archivo contiene un controlador instalable.      |
| **VFT2 \_ DRV \_ SOUND**              | El archivo contiene un controlador de sonido.             |
| **IMPRESORA CON VERSIONES \_ DRV VFT2 \_ \_** | El archivo contiene un controlador de impresora con versiones. |



 

Si *filetype* especifica **VFT \_ FONT,** este parámetro puede ser uno de los valores siguientes.



| Value                    | Descripción                    |
|--------------------------|--------------------------------|
| **VFT2 \_ UNKNOWN**        | El tipo de fuente es desconocido.          |
| **TRAMA DE FUENTE \_ VFT2 \_**   | El archivo contiene una fuente de trama.   |
| **VECTOR DE FUENTE \_ VFT2 \_**   | El archivo contiene una fuente vectorial.   |
| **VFT2 \_ FONT \_ TRUETYPE** | El archivo contiene una fuente TrueType. |



 

Si *filetype* especifica VFT VXD, este parámetro debe ser el identificador de dispositivo \_ virtual incluido en el bloque de control de dispositivo virtual.

Todos *los valores de subtipo* que no aparecen aquí están reservados para su uso por Parte de Microsoft.

</dd> <dt>

<span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*
</dt> <dd>

Uno de los siguientes códigos de idioma.



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
| 0x0414 | ¿Noruego? Bokmal  | 0x100C | Francés suizo              |
| 0x0810 | Italiano italiano italiano       | 0x0816 | Portugués (Portugal)     |
| 0x0813 | Neerlandés neerland       | 0x081A | Serbo-Croatian (cirílico) |
| 0x0814 | ¿Noruego? Nynorsk |        |                           |



 

</dd> <dt>

<span id="charsetID"></span><span id="charsetid"></span><span id="CHARSETID"></span>*charsetID*
</dt> <dd>

Uno de los siguientes identificadores de juego de caracteres.



| Decimal | Hexadecimal | Juego de caracteres              |
|---------|-------------|----------------------------|
| 0       | 0000        | ASCII de 7 bits                |
| 932     | 03A4        | Japón (Mayús ? JIS X-0208) |
| 949     | 03B5        | Corea (Mayús ? KSC 5601)   |
| 950     | 03B6        | Taiwán (Big5)              |
| 1200    | 04B0        | Unicode                    |
| 1250    | 04E2        | Latin-2 (Europa oriental) |
| 1251    | 04E3        | Cirílico                   |
| 1252    | 04E4        | Multilingüe               |
| 1253    | 04E5        | Griego                      |
| 1254    | 04E6        | Turco                    |
| 1255    | 04E7        | Hebreo                     |
| 1256    | 04E8        | Árabe                     |



 

</dd> <dt>

<span id="string-name"></span><span id="STRING-NAME"></span>*string-name*
</dt> <dd>

Uno de los siguientes nombres predefinidos.



| Nombre                 | Descripción                                                                                                                                                                                                                                                                                                 |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Comentarios**         | Información adicional que se debe mostrar con fines de diagnóstico.                                                                                                                                                                                                                                    |
| **CompanyName**      | ¿Empresa que produjo el archivo? por ejemplo, "Microsoft Corporation" o "Standard Microsystems Corporation, Inc". Esta cadena es obligatoria.                                                                                                                                                                   |
| **FileDescription**  | Descripción del archivo que se va a presentar a los usuarios. Esta cadena puede mostrarse en un cuadro de lista cuando el usuario elige los archivos para instalar, por ejemplo, "Keyboard Driver for AT-Style Keyboards". Esta cadena es obligatoria.                                                                                            |
| **FileVersion**      | ¿Número de versión del archivo?, por ejemplo, "3.10" o "5.00.RC2". Esta cadena es obligatoria.                                                                                                                                                                                                                      |
| **InternalName**     | Nombre interno del archivo, si existe, por ejemplo, un nombre de módulo si el archivo es una biblioteca de vínculos dinámicos. Si el archivo no tiene ningún nombre interno, esta cadena debe ser el nombre de archivo original, sin extensión. Esta cadena es obligatoria.                                                                       |
| **LegalCopyright**   | Avisos de copyright que se aplican al archivo. Esto debe incluir el texto completo de todos los avisos, símbolos legales, fechas de copyright, y así sucesivamente. Esta cadena es opcional.                                                                                                                                             |
| **LegalTrademarks**  | Marcas comerciales y marcas comerciales registradas que se aplican al archivo. Esto debe incluir el texto completo de todos los avisos, símbolos legales, números de marcas comerciales, etc. Esta cadena es opcional.                                                                                                                        |
| **OriginalFilename** | Nombre original del archivo, sin incluir una ruta de acceso. Esta información permite a una aplicación determinar si un usuario ha cambiado el nombre de un archivo. El formato del nombre depende del sistema de archivos para el que se creó el archivo. Esta cadena es obligatoria.                                                 |
| **PrivateBuild**     | Información sobre una versión privada del archivo, por ejemplo, "Built by TESTER1 on \\ TESTBED". Esta cadena solo debe estar presente si se especifica **\_ VS FF \_ PRIVATEBUILD** en el *parámetro fileflags* del bloque raíz.                                                                                   |
| **ProductName**      | Nombre del producto con el que se distribuye el archivo. Esta cadena es obligatoria.                                                                                                                                                                                                                            |
| **ProductVersion**   | Versión del producto con el que se distribuye el archivo, por ejemplo, "3.10" o "5.00.RC2". Esta cadena es obligatoria.                                                                                                                                                                                       |
| **SpecialBuild**     | Texto que indica en qué se diferencia esta versión del archivo de la versión estándar, por ejemplo, "Compilación privada para TESTER1 que resuelve problemas del mouse en equipos M250 y M250E". Esta cadena solo debe estar presente si se especifica **VS \_ FF \_ SPECIALBUILD** en el *parámetro fileflags* del bloque raíz. |



 

</dd> </dl>

Algunos atributos también se admiten por compatibilidad con versiones anteriores. Para más información, consulte [Atributos de recursos comunes.](common-resource-attributes.md)

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se define **un recurso VERSIONINFO:**

``` syntax
#define VER_FILEVERSION             3,10,349,0
#define VER_FILEVERSION_STR         "3.10.349.0\0"

#define VER_PRODUCTVERSION          3,10,0,0
#define VER_PRODUCTVERSION_STR      "3.10\0"

#ifndef DEBUG
#define VER_DEBUG                   0
#else
#define VER_DEBUG                   VS_FF_DEBUG
#endif

VS_VERSION_INFO VERSIONINFO
FILEVERSION     VER_FILEVERSION
PRODUCTVERSION  VER_PRODUCTVERSION
FILEFLAGSMASK   VS_FFI_FILEFLAGSMASK
FILEFLAGS       (VER_PRIVATEBUILD|VER_PRERELEASE|VER_DEBUG)
FILEOS          VOS__WINDOWS32
FILETYPE        VFT_DLL
FILESUBTYPE     VFT2_UNKNOWN
BEGIN
    BLOCK "StringFileInfo"
    BEGIN
        BLOCK "040904E4"
        BEGIN
            VALUE "CompanyName",      VER_COMPANYNAME_STR
            VALUE "FileDescription",  VER_FILEDESCRIPTION_STR
            VALUE "FileVersion",      VER_FILEVERSION_STR
            VALUE "InternalName",     VER_INTERNALNAME_STR
            VALUE "LegalCopyright",   VER_LEGALCOPYRIGHT_STR
            VALUE "LegalTrademarks1", VER_LEGALTRADEMARKS1_STR
            VALUE "LegalTrademarks2", VER_LEGALTRADEMARKS2_STR
            VALUE "OriginalFilename", VER_ORIGINALFILENAME_STR
            VALUE "ProductName",      VER_PRODUCTNAME_STR
            VALUE "ProductVersion",   VER_PRODUCTVERSION_STR
        END
    END

    BLOCK "VarFileInfo"
    BEGIN
        /* The following line should only be modified for localized versions.     */
        /* It consists of any number of WORD,WORD pairs, with each pair           */
        /* describing a language,codepage combination supported by the file.      */
        /*                                                                        */
        /* For example, a file might have values "0x409,1252" indicating that it  */
        /* supports English language (0x409) in the Windows ANSI codepage (1252). */

        VALUE "Translation", 0x409, 1252

    END
END
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Uso de información de versión](./using-version-information.md)
</dt> <dt>

[Información de versión](./version-information.md)
</dt> </dl>

 

 