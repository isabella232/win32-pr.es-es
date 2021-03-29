---
title: Instalación del controlador de archivos y secuencias
description: Instalación del controlador de archivos y secuencias
ms.assetid: 8d007ea4-b75a-4b3f-965f-8091fcd4cb2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be94137df69ed35b57b1b8fbeb5c9640dd7636d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779134"
---
# <a name="file-and-stream-handler-installation"></a>Instalación del controlador de archivos y secuencias

La biblioteca AVIFile usa controladores de archivos y secuencias instalados para leer y escribir archivos AVI y secuencias. Un controlador se instala cuando reside en el directorio del sistema de Windows y el registro contiene la siguiente información necesaria para describir e identificar un controlador:

-   Identificador de clase de 16 bytes para el controlador
-   Breve descripción del controlador
-   Nombre del archivo que contiene el controlador.
-   La extensión de archivo que un controlador de archivos puede procesar.
-   Acceso a archivos y otras propiedades asociadas a un controlador de archivos
-   Códigos de cuatro caracteres que identifican los tipos de secuencia que un controlador de flujo puede procesar

La biblioteca AVIFile consulta al registro los controladores que son externos a una aplicación al abrir archivos y obtener acceso a secuencias. El resultado de una consulta correcta devuelve el nombre de archivo de un controlador que puede procesar el tipo de archivo o de secuencia especificado en la consulta. El registro muestra cada controlador mediante la creación de tres entradas que tienen el siguiente formato:


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



Estas entradas se componen de las siguientes partes.



| Parte                                   | Descripción                                                                                                                                                                              |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_clase HKEY \_ raíz                    | Identifica la entrada raíz del registro.                                                                                                                                               |
| Clsid                                  | Identifica esta entrada como un identificador de clase.                                                                                                                                             |
| {00010023-0000-0000-C000-000000000046} | Especifica un identificador de interfaz (IID) o un identificador de clase. Este valor es un identificador único de 16 bytes. (También se puede hacer referencia al identificador como un GUID o un UUID en otros manuales). |
| Lector/escritor de archivos de onda                | Especifica una cadena para describir el controlador. Esta cadena se puede mostrar en cuadros de diálogo para seleccionar secuencias y controladores de archivos.                                                         |
| InProcServer32                         | Especifica el archivo (en este ejemplo, WAVEFILE.DLL) que se puede cargar para controlar esta clase.                                                                                              |
| AVIFile                                | Especifica las propiedades de un controlador de archivos. En este ejemplo, el controlador puede leer y escribir en un archivo AVI.                                                                              |



 

Un controlador de archivos puede tener una o varias de sus propiedades almacenadas en el registro. Las constantes siguientes identifican las propiedades asociadas actualmente a un archivo.



| Constante                        | Descripción                                                          |
|---------------------------------|----------------------------------------------------------------------|
| AVIFILEHANDLER \_ CANACCEPTNONRGB | Indica que un controlador de archivos puede procesar datos de imagen distintos de RGB. |
| AVIFILEHANDLER \_ CANREAD         | Indica que un controlador de archivos puede abrir un archivo con acceso de lectura.      |
| AVIFILEHANDLER \_ CANWRITE        | Indica que un controlador de archivos puede abrir un archivo con acceso de escritura.     |



 

Al crear un archivo o un controlador de secuencias, puede obtener un nuevo identificador ejecutando UUIDGEN.EXE. Utilice siempre UUIDGEN.EXE para crear un nuevo identificador. El número hexadecimal de 16 bytes creado por este archivo ejecutable identificará de forma única el controlador.

La biblioteca AVIFile usa entradas adicionales en el registro para identificar un identificador de clase basado en la extensión de archivo que un controlador de archivos puede procesar o un código de cuatro caracteres que un controlador de archivo o secuencia puede procesar. Por ejemplo, las siguientes entradas asocian un identificador de clase a la extensión de archivo. WAV y el código de cuatro caracteres "WAVE":


```C++
[HKEY_CLASSES_ROOT\AVIFile\Extensions\WAV] 
@="{00010023-0000-0000-C000-000000000046}" 
[HKEY_CLASSES_ROOT\AVIFile\RIFFHandlers\WAVE] 
@="{00010023-0000-0000-C000-000000000046}" 
 
```



Estas entradas se componen de las siguientes partes.



| Parte                                   | Descripción                                                                                       |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| \_clase HKEY \_ raíz                    | Identifica la entrada raíz del registro.                                                        |
| AVIFile                                | Identifica esta entrada como una entrada utilizada por AVIFile.                                                |
| Extensiones                             | Especifica la extensión de archivo (en este ejemplo,. WAV) que un controlador de archivos puede procesar.             |
| RIFFHandlers                           | Especifica el código de cuatro caracteres (en este ejemplo, "WAVE") que un controlador de archivo o secuencia puede procesar. |
| {00010023-0000-0000-C000-000000000046} | Especifica un identificador de interfaz (IID) o un identificador de clase.                                      |



 

Si distribuye la secuencia o el controlador de archivo sin una aplicación de instalación para instalarlo en el sistema del usuario, debe incluir un. Archivo REG para que el usuario pueda instalar el controlador. El usuario utilizará el editor del registro para crear entradas del registro para el flujo o el controlador de archivos.

En el ejemplo siguiente se muestra el contenido de un típico. Archivo REG. La primera entrada del ejemplo siguiente es la cadena descriptiva del controlador. La segunda entrada identifica el archivo que contiene el controlador. La tercera entrada identifica las propiedades del controlador de archivos (en este caso, acceso de solo lectura a los archivos). La cuarta entrada asocia el tipo de archivo que procesa el controlador (en este caso, los archivos con. Extensión de nombre de archivo JPG) con el identificador de clase.


```C++
[HKEY_CLASSES_ROOT\Clsid\{5C2B8200-E2C8-1068-B1CA-6066188C6002}] 
@="JFIF (JPEG) Files" 
[HKEY_CLASSES_ROOT\Clsid\{5C2B8200-E2C8-1068-B1CA-6066188C6002}]\InprocServer32] 
@="jfiffile.dll" 
[HKEY_CLASSES_ROOT\AVIFile\Extensions\JPG] 
@="{5C2B8200-E2C8-1068-B1CA-6066188C6002}" 
 
```



Al crear este archivo, guárdelo con un. REG extensión para identificarla como un archivo de actualización para el registro. Además, sustituya un IID único para el código de 16 bytes que se usa en el ejemplo.

 

 




