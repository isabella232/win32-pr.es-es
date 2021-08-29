---
title: Instalación del controlador de archivos y secuencias
description: Instalación del controlador de archivos y secuencias
ms.assetid: 8d007ea4-b75a-4b3f-965f-8091fcd4cb2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78ac1b08fb917ee27dc871082591a9118e6e2c40588bc9eb4961f41786c1fb9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119785415"
---
# <a name="file-and-stream-handler-installation"></a>Instalación del controlador de archivos y secuencias

La biblioteca AVIFile usa controladores de archivos y secuencias instalados para leer y escribir archivos y secuencias AVI. Se instala un controlador cuando reside en el directorio Windows SYSTEM y el Registro contiene la siguiente información necesaria para describir e identificar un controlador:

-   Identificador de clase de 16 bytes para el controlador
-   Breve descripción del controlador
-   Nombre del archivo que contiene el controlador
-   La extensión de archivo que un controlador de archivos puede procesar
-   Acceso a archivos y otras propiedades asociadas a un controlador de archivos
-   Códigos de cuatro caracteres que identifican los tipos de secuencia que puede procesar un controlador de secuencias

La biblioteca AVIFile consulta al Registro los controladores externos a una aplicación al abrir archivos y acceder a secuencias. El resultado de una consulta correcta devuelve el nombre de archivo de un controlador que puede procesar el archivo o el tipo de secuencia especificado en la consulta. El Registro enumera cada controlador mediante la creación de tres entradas que tienen el formato siguiente:


```C++
[HKEY_CLASSES_ROOT\Clsid\{00010023-0000-0000-C000-000000000046}] 
@="Wave File reader/writer" 
[HKEY_CLASSES_ROOT\Clsid\{00010023-0000-0000-C000- 
000000000046}\InprocServer32] 
@="wavefile.dll" 
"ThreadingModel"="Apartment" 
[HKEY_CLASSES_ROOT\Clsid\{00010023-0000-0000-C000- 
000000000046}\AVIFile] 
@="3" 
 
```



Estas entradas constan de las siguientes partes.



| Parte                                   | Descripción                                                                                                                                                                              |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RAÍZ DE CLASES HKEY \_ \_                    | Identifica la entrada raíz del registro.                                                                                                                                               |
| Clsid                                  | Identifica esta entrada como un identificador de clase.                                                                                                                                             |
| {00010023-0000-0000-C000-00000000046} | Especifica un identificador de interfaz (IID) o un identificador de clase. Este valor es un identificador único de 16 bytes. (El identificador también se puede denominar GUID o UUID en otros manuales). |
| Lector o escritor de archivos wave                | Especifica una cadena para describir el controlador. Esta cadena se puede mostrar en cuadros de diálogo para seleccionar controladores de secuencias y archivos.                                                         |
| InProcServer32                         | Especifica el archivo (en este ejemplo, WAVEFILE.DLL) que se puede cargar para controlar esta clase.                                                                                              |
| AVIFile                                | Especifica las propiedades de un controlador de archivos. En este ejemplo, el controlador puede leer y escribir en un archivo AVI.                                                                              |



 

Un controlador de archivos puede tener una o varias de sus propiedades almacenadas en el Registro. Las constantes siguientes identifican las propiedades asociadas actualmente a un archivo.



| Constante                        | Descripción                                                          |
|---------------------------------|----------------------------------------------------------------------|
| AVIFILEHANDLER \_ CANACCEPTNONRGB | Indica que un controlador de archivos puede procesar datos de imagen distintos de RGB. |
| AVIFILEHANDLER \_ CANREAD         | Indica que un controlador de archivos puede abrir un archivo con acceso de lectura.      |
| AVIFILEHANDLER \_ CANWRITE        | Indica que un controlador de archivos puede abrir un archivo con acceso de escritura.     |



 

Al crear un controlador de archivos o secuencias, puede obtener un nuevo identificador mediante la ejecución de UUIDGEN.EXE. Use siempre UUIDGEN.EXE para crear un nuevo identificador. El número hexadecimal de 16 bytes creado por este ejecutable identificará de forma única el controlador.

La biblioteca AVIFile usa entradas adicionales en el Registro para identificar un identificador de clase basado en la extensión de archivo que un controlador de archivos puede procesar o un código de cuatro caracteres que un controlador de archivos o secuencias puede procesar. Por ejemplo, las siguientes entradas asocian un identificador de clase a la extensión de archivo . WAV y el código de cuatro caracteres "WAVE":


```C++
[HKEY_CLASSES_ROOT\AVIFile\Extensions\WAV] 
@="{00010023-0000-0000-C000-000000000046}" 
[HKEY_CLASSES_ROOT\AVIFile\RIFFHandlers\WAVE] 
@="{00010023-0000-0000-C000-000000000046}" 
 
```



Estas entradas constan de las siguientes partes.



| Parte                                   | Descripción                                                                                       |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| RAÍZ DE CLASES HKEY \_ \_                    | Identifica la entrada raíz del registro.                                                        |
| AVIFile                                | Identifica esta entrada como una entrada utilizada por AVIFile.                                                |
| Extensiones                             | Especifica la extensión de archivo (en este ejemplo, . WAV) que un controlador de archivos puede procesar.             |
| RIFFHandlers                           | Especifica el código de cuatro caracteres (en este ejemplo, "WAVE") que un archivo o controlador de secuencias puede procesar. |
| {00010023-0000-0000-C000-00000000046} | Especifica un identificador de interfaz (IID) o un identificador de clase.                                      |



 

Si distribuye el controlador de secuencias o archivos sin una aplicación de instalación para instalarlo en el sistema del usuario, debe incluir un . Archivo REG para que el usuario pueda instalar el controlador. El usuario usará el editor del Registro para crear entradas del Registro para el controlador de secuencias o archivos.

En el ejemplo siguiente se muestra el contenido de un típico . Archivo REG. La primera entrada del ejemplo siguiente es la cadena descriptiva para el controlador. La segunda entrada identifica el archivo que contiene el controlador. La tercera entrada identifica las propiedades del controlador de archivos (en este caso, acceso de solo lectura a los archivos). La cuarta entrada asocia el tipo de archivo que procesa el controlador (en este caso, los archivos con una extensión de nombre .JPG nombre de archivo) con el identificador de clase.


```C++
[HKEY_CLASSES_ROOT\Clsid\{5C2B8200-E2C8-1068-B1CA-6066188C6002}] 
@="JFIF (JPEG) Files" 
[HKEY_CLASSES_ROOT\Clsid\{5C2B8200-E2C8-1068-B1CA-6066188C6002}]\InprocServer32] 
@="jfiffile.dll" 
[HKEY_CLASSES_ROOT\AVIFile\Extensions\JPG] 
@="{5C2B8200-E2C8-1068-B1CA-6066188C6002}" 
 
```



Al crear este archivo, guárdelo con . Extensión REG para identificarla como un archivo de actualización para el Registro. Además, sustituya un IID único por el código de 16 bytes usado en el ejemplo.

 

 




