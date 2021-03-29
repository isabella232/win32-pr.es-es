---
title: Recurso VERSIONINFO
description: Define un recurso de información de versión. El recurso contiene información sobre el archivo como su número de versión, su sistema operativo previsto y su nombre de archivo original. El recurso está diseñado para usarse con las funciones de información de versión.
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
ms.openlocfilehash: 9248abe18d07820ebefaa6d939f36f617f6cd07f
ms.sourcegitcommit: 25e1fa2b3641ae13b79e0afdf9cb7a168d99e009
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "104359501"
---
# <a name="versioninfo-resource"></a>Recurso VERSIONINFO

Define un recurso de información de versión. El recurso contiene información sobre el archivo como su número de versión, su sistema operativo previsto y su nombre de archivo original. El recurso está diseñado para usarse con las funciones de [información de versión](./version-information.md) .

Hay dos maneras de dar formato a una instrucción **versionInfo** :

``` syntax
versionID VERSIONINFO fixed-info  { block-statement . . . }
```

\- o -

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

<span id="fixed-info"></span><span id="FIXED-INFO"></span>*Fixed-info*
</dt> <dd>

Información de versión, como la versión del archivo y el sistema operativo previsto. Este parámetro consta de las siguientes instrucciones.



| .                         | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  *Versión* FILEVERSION         | Número de versión binaria del archivo. La *versión* consta de enteros de 2 32 bits, definidos por enteros de 4 16 bits. Por ejemplo, "FILEVERSION 3, 10, 0, 61" se traduce en dos palabras dobles: 0x0003000a y 0x0000003d, en ese orden. Por lo tanto, si la *versión* está definida por los valores **DWORD** *DW1* y *Dw2*, deben aparecer en la instrucción **FILEVERSION** de la siguiente manera: `HIWORD(dw1)` , `LOWORD(dw1)` , `HIWORD(dw2)` , `LOWORD(dw2)` . |
|  *Versión* de PRODUCTVERSION      | Número de versión binaria del producto con el que se distribuye el archivo. El parámetro *version* es un entero de 2 32 bits, definido por enteros de 4 16 bits. Para obtener más información acerca de la versión, consulte la **Descripción de la** versión de la *versión*.                                                                                                                                                                                                           |
| **FILEFLAGSMASK** *FILEFLAGSMASK* | Indica qué bits de la instrucción **FILEFLAGS** son válidos. En Windows de 16 bits, este valor es 0x3F.                                                                                                                                                                                                                                                                                                                                          |
| **FILEFLAGS** *FILEFLAGS*         | Atributos del archivo.                                                                                                                                                                                                                                                                                                                                                                                                                         |
|  *Archivos* de archivos               | Sistema operativo para el que se diseñó este archivo. El parámetro *Fileos* puede ser uno de los valores del sistema operativo que se indican en la sección Comentarios.                                                                                                                                                                                                                                                                                               |
|  *Filetype* filetype           | Tipo general de archivo. El parámetro *filetype* puede ser uno de los valores de tipo de archivo que se muestran en la sección Comentarios.                                                                                                                                                                                                                                                                                                                                |
| Subtipo **FILESUBTYPE**          | Función del archivo. El parámetro *SubType* es cero a menos que el parámetro *filetype* de la instrucción **FILETYPE** sea VFT \_ drv, VFT \_ Font o VFT \_ vxd. Para obtener una lista de valores de subtipo de archivo, consulte la sección Comentarios.                                                                                                                                                                                                                            |



 

</dd> <dt>

<span id="block-statement"></span><span id="BLOCK-STATEMENT"></span>*Block-Statement*
</dt> <dd>

Especifica uno o más bloques de información de versión. Un bloque puede contener información de cadena o información de variables. Para obtener más información, vea bloque [**StringFileInfo**](stringfileinfo-block.md) o [**bloque VarFileInfo**](varfileinfo-block.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para usar las constantes especificadas con la instrucción **versionInfo** , debe incluir el archivo de encabezado winver. h o Windows. h en el archivo de definición de recursos.

En la lista siguiente se describen los parámetros que se usan en la instrucción **versionInfo** :

<dl> <dt>

<span id="fileflags"></span><span id="FILEFLAGS"></span>*fileflags*
</dt> <dd>

Una combinación de los valores siguientes.



| Value                      | Descripción                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **depuración de VS \_ FF \_**          | El archivo contiene información de depuración o se compila con las características de depuración habilitadas.                                                                                                                                                                                         |
| **VS \_ FF \_ revisado**        | El archivo se ha modificado y no es idéntico al archivo de envío original del mismo número de versión.                                                                                                                                                                       |
| **\_ \_ versión preliminar de vs FF**     | El archivo es una versión de desarrollo, no un producto publicado comercialmente.                                                                                                                                                                                                         |
| **VS \_ FF \_ PRIVATEBUILD**   | El archivo no se compiló con procedimientos estándar de versión. Si se especifica este valor, el [**bloque StringFileInfo**](stringfileinfo-block.md) debe contener una cadena **PrivateBuild** .                                                                                              |
| **VS \_ FF \_ SPECIALBUILD**   | El archivo fue creado por la empresa original mediante procedimientos estándar de versión, pero es una variación del archivo estándar del mismo número de versión. Si se especifica este valor, el bloque de [bloque **StringFileInfo**](stringfileinfo-block.md) debe contener una cadena **SpecialBuild** . |
| **VS \_ FFI \_ FILEFLAGSMASK** | Combinación de todos los valores anteriores.                                                                                                                                                                                                                                  |



 

</dd> <dt>

<span id="fileos"></span><span id="FILEOS"></span>*archivos*
</dt> <dd>

Uno de los siguientes valores.



| Valor                   | Descripción                                                      |
|-------------------------|------------------------------------------------------------------|
| **VOS \_ desconocido**        | El sistema operativo para el que se diseñó el archivo es desconocido. |
| **VOS \_ dos**            | El archivo se diseñó para MS-DOS.                                    |
| **VOS \_ NT**             | El archivo se diseñó para Windows de 32 bits.                            |
| **VOS \_ \_ WINDOWS16**    | El archivo se diseñó para Windows de 16 bits.                            |
| **VOS \_ \_ WINDOWS32**    | El archivo se diseñó para Windows de 32 bits.                            |
| **VOS \_ dos \_ WINDOWS16** | El archivo se diseñó para Windows de 16 bits que se ejecuta con MS-DOS.        |
| **VOS \_ dos \_ WINDOWS32** | El archivo se diseñó para Windows de 32 bits que se ejecuta con MS-DOS.        |
| **VOS \_ NT \_ WINDOWS32**  | El archivo se diseñó para Windows de 32 bits.                            |



 

Los valores 0x00002L, 0x00003L, 0x20000L y 0x30000L están reservados.

</dd> <dt>

<span id="filetype"></span><span id="FILETYPE"></span>*filetype*
</dt> <dd>

Uno de los siguientes valores.



| Valor                | Descripción                                                                                                                 |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------|
| **VFT \_ desconocido**     | No se conoce el tipo de archivo.                                                                                                       |
| **\_aplicación VFT**         | El archivo contiene una aplicación.                                                                                               |
| **\_dll VFT**         | El archivo contiene una biblioteca de vínculos dinámicos (DLL).                                                                                 |
| **VFT \_ DRV**         | El archivo contiene un controlador de dispositivo. Si *filetype* es **VFT \_ DRV**, *SubType* contiene una descripción más específica del controlador. |
| **\_fuente VFT**        | El archivo contiene una fuente. Si *filetype* es VFT \_ Font, *SubType* contiene una descripción más específica de la fuente.               |
| **VXD de VFT \_**         | El archivo contiene un dispositivo virtual.                                                                                             |
| **\_biblioteca estática \_ VFT** | El archivo contiene una biblioteca de vínculos estáticos.                                                                                        |



 

Todos los demás valores están reservados para su uso por parte de Microsoft.

</dd> <dt>

<span id="subtype"></span><span id="SUBTYPE"></span>*subtipo*
</dt> <dd>

Información adicional sobre el tipo de archivo.

Si *filetype* especifica **VFT \_ DRV**, este parámetro puede ser uno de los valores siguientes.



| Value                             | Descripción                               |
|-----------------------------------|-------------------------------------------|
| **VFT2 \_ desconocido**                 | No se conoce el tipo de controlador.                   |
| **VFT2 \_ DRV \_ COMM**               | El archivo contiene un controlador de comunicaciones.    |
| **\_Impresora VFT2 DRV \_**            | El archivo contiene un controlador de impresora.           |
| **\_Teclado VFT2 DRV \_**           | El archivo contiene un controlador de teclado.          |
| **Idioma de VFT2 \_ DRV \_**           | El archivo contiene un controlador de idioma.          |
| **Pantalla de VFT2 \_ DRV \_**            | El archivo contiene un controlador de pantalla.           |
| **\_Mouse VFT2 DRV \_**              | El archivo contiene un controlador de mouse.             |
| **\_Red VFT2 DRV \_**            | El archivo contiene un controlador de red.           |
| **\_Sistema VFT2 DRV \_**             | El archivo contiene un controlador del sistema.            |
| **VFT2 \_ DRV \_ instalable**        | El archivo contiene un controlador instalable.      |
| **\_Sonido VFT2 DRV \_**              | El archivo contiene un controlador de sonido.             |
| **\_Impresora con \_ versión VFT2 \_ DRV** | El archivo contiene un controlador de impresora con versión. |



 

Si *filetype* especifica **la \_ fuente VFT**, este parámetro puede ser uno de los valores siguientes.



| Value                    | Descripción                    |
|--------------------------|--------------------------------|
| **VFT2 \_ desconocido**        | Tipo de fuente desconocido.          |
| **\_Trama de fuente VFT2 \_**   | El archivo contiene una fuente de trama.   |
| **\_Vector de fuente VFT2 \_**   | El archivo contiene una fuente de vector.   |
| **VFT2 \_ fuente \_ TrueType** | El archivo contiene una fuente TrueType. |



 

Si *filetype* especifica VFT \_ VXD, este parámetro debe ser el identificador del dispositivo virtual incluido en el bloque de control del dispositivo virtual.

Todos los valores de *subtipo* que no se enumeran aquí están reservados para su uso por parte de Microsoft.

</dd> <dt>

<span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*ididioma*
</dt> <dd>

Uno de los siguientes códigos de idioma.



| Código   | Idioma            | Código   | Idioma                  |
|--------|---------------------|--------|---------------------------|
| 0x0401 | Árabe              | 0x0415 | Polaco                    |
| 0x0402 | Búlgaro           | 0x0416 | Portugués (Brasil)       |
| 0x0403 | Catalán             | 0x0417 | Rhaeto-Romanic            |
| 0x0404 | Chino tradicional | 0x0418 | Rumano                  |
| 0x0405 | Checo               | 0x0419 | Ruso                   |
| 0x0406 | Danés              | 0x041A | Croato-Serbian (Latín)    |
| 0x0407 | Alemán              | 0x041B | Eslovaco                    |
| 0x0408 | Griego               | 0x041C | Albanés                  |
| 0x0409 | Inglés de EE. UU.        | 0x041D | Sueco                   |
| 0x040A | Castilian Español   | 0x041E | Tailandés                      |
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
| 0x0810 | Italiano suizo       | 0x0816 | Portugués (Portugal)     |
| 0x0813 | Holandés belga       | 0x081A | Serbo-Croatian (cirílico) |
| 0x0814 | ¿Noruego? Nynorsk |        |                           |



 

</dd> <dt>

<span id="charsetID"></span><span id="charsetid"></span><span id="CHARSETID"></span>*charsetID*
</dt> <dd>

Uno de los siguientes identificadores de juego de caracteres.



| Decimal | Hexadecimal | Juego de caracteres              |
|---------|-------------|----------------------------|
| 0       | 0000        | ASCII de 7 bits                |
| 932     | 03A4        | Japón (Shift? JIS X-0208) |
| 949     | 03B5        | Corea (Shift? KSC 5601)   |
| 950     | 03B6        | Taiwán (Big5)              |
| 1200    | 04B0        | Unicode                    |
| 1250    | 04E2        | Latín-2 (Europa Oriental) |
| 1251    | 04E3        | Cirílico                   |
| 1252    | 04E4        | Entornos               |
| 1253    | 04E5        | Griego                      |
| 1254    | 04E6        | Turco                    |
| 1255    | 04E7        | Hebreo                     |
| 1256    | 04E8        | Árabe                     |



 

</dd> <dt>

<span id="string-name"></span><span id="STRING-NAME"></span>*nombre de cadena*
</dt> <dd>

Uno de los siguientes nombres predefinidos.



| Nombre                 | Descripción                                                                                                                                                                                                                                                                                                 |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Comentarios**         | Información adicional que se debe mostrar con fines de diagnóstico.                                                                                                                                                                                                                                    |
| **Compañía**      | ¿Compañía que generó el archivo? por ejemplo, "Microsoft Corporation" o "Standard Microsystems Corporation, Inc." Esta cadena es obligatoria.                                                                                                                                                                   |
| **FileDescription**  | Descripción del archivo que se va a presentar a los usuarios. Esta cadena se puede mostrar en un cuadro de lista cuando el usuario elige los archivos que se van a instalar. por ejemplo, "controlador de teclado para AT-Style teclados". Esta cadena es obligatoria.                                                                                            |
| **FileVersion**      | Número de versión del archivo, por ejemplo, "3,10" o "5,00. RC2". Esta cadena es obligatoria.                                                                                                                                                                                                                      |
| **InternalName**     | Nombre interno del archivo, si existe uno, por ejemplo, un nombre de módulo si el archivo es una biblioteca de vínculos dinámicos. Si el archivo no tiene ningún nombre interno, esta cadena debe ser el nombre de archivo original, sin extensión. Esta cadena es obligatoria.                                                                       |
| **LegalCopyright**   | Avisos de copyright que se aplican al archivo. Esto debe incluir el texto completo de todos los avisos, símbolos legales, fechas de copyright, etc. Esta cadena es opcional.                                                                                                                                             |
| **LegalTrademarks**  | Marcas comerciales y marcas registradas que se aplican al archivo. Esto debe incluir el texto completo de todos los avisos, símbolos legales, números de marcas comerciales, etc. Esta cadena es opcional.                                                                                                                        |
| **OriginalFilename** | Nombre original del archivo, sin incluir una ruta de acceso. Esta información permite que una aplicación determine si un usuario ha cambiado el nombre de un archivo. El formato del nombre depende del sistema de archivos para el que se creó el archivo. Esta cadena es obligatoria.                                                 |
| **PrivateBuild**     | Información sobre una versión privada del archivo, por ejemplo, "compilado por TESTER1 en \\ TESTBED". Esta cadena solo debe estar presente si **vs \_ FF \_ PRIVATEBUILD** se especifica en el parámetro *fileflags* del bloque raíz.                                                                                   |
| **ProductName**      | Nombre del producto con el que se distribuye el archivo. Esta cadena es obligatoria.                                                                                                                                                                                                                            |
| **ProductVersion**   | Versión del producto con la que se distribuye el archivo, por ejemplo, "3,10" o "5,00. RC2". Esta cadena es obligatoria.                                                                                                                                                                                       |
| **SpecialBuild**     | Texto que indica el modo en que esta versión del archivo difiere de la versión estándar. por ejemplo, "compilación privada para la solución de problemas del mouse en equipos M250 y M250E". Esta cadena solo debe estar presente si **vs \_ FF \_ SPECIALBUILD** se especifica en el parámetro *fileflags* del bloque raíz. |



 

</dd> </dl>

Algunos atributos también se admiten por razones de compatibilidad con versiones anteriores. Para obtener más información, vea [atributos comunes de recursos](common-resource-attributes.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se define un recurso **versionInfo** :

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

[Usar información de versión](./using-version-information.md)
</dt> <dt>

[Información de versión](./version-information.md)
</dt> </dl>

 

 