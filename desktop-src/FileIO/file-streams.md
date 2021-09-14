---
description: En el sistema de archivos NTFS, las secuencias contienen los datos que se escriben en un archivo y que proporciona más información sobre un archivo que atributos y propiedades.
ms.assetid: 41dda6f1-a6d1-4e76-94f3-a72f9e491bee
title: Archivos Secuencias (sistemas de archivos locales)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a934a51225a886e3d5a7de4d9e1e91900fab460
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069946"
---
# <a name="file-streams-local-file-systems"></a>Archivos Secuencias (sistemas de archivos locales)

Una secuencia es una secuencia de bytes. En el sistema de archivos NTFS, las secuencias contienen los datos que se escriben en un archivo y que proporciona más información sobre un archivo que atributos y propiedades. Por ejemplo, puede crear una secuencia que contenga palabras clave de búsqueda o la identidad de la cuenta de usuario que crea un archivo.

Cada secuencia asociada a un archivo tiene su propio tamaño de asignación, tamaño real y longitud de datos válida:

-   El tamaño de asignación es la cantidad de espacio en disco que se reserva para una secuencia.
-   El tamaño real es el número de bytes que usa un autor de la llamada.
-   La longitud de datos válida (VDL) es el número de bytes que se inicializan a partir del tamaño de asignación de la secuencia.

Cada secuencia también mantiene su propio estado para la compresión, el cifrado y la dispersa. El atributo **FILE \_ ATTRIBUTE \_ SPARSE \_ FILE** del archivo se establece en el miembro **dwFileAttributes** de la estructura FIND DATA de [**WIN32 \_ \_**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) devuelta por las funciones [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa)y [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) si alguna vez se ha dispersado alguna de las secuencias. [**GetFileAttributes,**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) [**GetFileAttributesEx,**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) [**GetFileAttributesTransacted,**](/windows/desktop/api/WinBase/nf-winbase-getfileattributestransacteda) [**GetFileInformationByHandle**](/windows/desktop/api/FileAPI/nf-fileapi-getfileinformationbyhandle)y [**GetFileInformationByHandleEx**](/windows/desktop/api/WinBase/nf-winbase-getfileinformationbyhandleex) devuelven el estado disperso del flujo de datos predeterminado si no se especifica ninguna secuencia.

No hay horas de archivo asociadas a una secuencia. Las horas de archivo de un archivo se actualizan cuando se actualiza cualquier secuencia de un archivo.

Los bloqueos oportunistas se mantienen por secuencia. Los modos de uso compartido también se mantienen por secuencia. Cuando se solicita acceso de eliminación en un archivo, el sistema operativo comprueba si hay acceso de eliminación en todas las secuencias abiertas de un archivo. Si otro proceso ha abierto una secuencia sin el permiso **FILE \_ SHARE \_ DELETE,** no puede abrir el archivo para el acceso de eliminación.

Si un archivo que se copia tiene un flujo de datos y se usa el redirector de red, el archivo solo se puede copiar si el cliente tiene el permiso de lectura y el permiso de lectura de atributos.

## <a name="naming-conventions-for-streams"></a>Convenciones de nomenclatura para Secuencias

Cuando se especifica desde la línea de comandos del shell de Windows, el nombre completo de una secuencia es "*filename*:*nombre* de secuencia *:* tipo de flujo ", como en el ejemplo siguiente: "myfile.dat:stream1:$DATA".

Los caracteres que son válidos para un nombre de archivo también son válidos para el nombre de secuencia, incluidos los espacios. Para obtener más información, [vea Asignar un nombre a un archivo.](naming-a-file.md) El tipo de secuencia (también denominado código de tipo de atributo) es interno del sistema de archivos NTFS. Por lo tanto, los usuarios no pueden crear nuevos tipos de secuencia, pero pueden abrir los tipos de sistema de archivos NTFS existentes. Los valores del especificador de tipo de flujo siempre comienzan con el símbolo de signo de dólar ($). Consulte a continuación una lista de tipos de flujo.

De forma predeterminada, el flujo de datos predeterminado no tiene nombre. Para especificar completamente el flujo de datos predeterminado, use *"filename*::$DATA", donde $DATA es el tipo de flujo. Es el equivalente de "*filename*". Puede crear una secuencia con nombre en el archivo mediante las [convenciones de nomenclatura de archivos](naming-a-file.md). Tenga en cuenta que "$DATA" es un nombre de flujo legal. Por ejemplo, el nombre completo de una secuencia denominada "$DATA" en un archivo denominado "*sample*" sería "*sample*:$DATA:$DATA". Si creó una secuencia denominada "bar" en el mismo archivo, su nombre completo sería *"sample*:bar:$DATA".

Al crear y trabajar con archivos que tienen nombres de un solo carácter, antefise el nombre de archivo con un punto seguido de una barra diagonal inversa (. o use un nombre de ruta de \) acceso completo. La razón para hacerlo es que Windows nombres de archivo de un carácter como letras de unidad. Cuando se especifica una letra de unidad con una ruta de acceso relativa, dos puntos separa la letra de unidad de la ruta de acceso. Cuando hay ambigüedad sobre si un nombre de un solo carácter es una letra de unidad o un nombre de archivo, Windows supone que es una letra de unidad si la cadena que sigue a los dos puntos es una ruta de acceso válida, incluso si la letra de unidad no es válida.

## <a name="stream-types"></a>Tipos de secuencia

A continuación se muestra la lista de tipos de flujo NTFS, también denominados códigos de tipo de atributo. Algunos de los tipos de flujo son internos de NTFS y su formato no está documentado.



| Tipo de secuencia                | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ::$ATTRIBUTE \_ LIST         | Contiene una lista de todos los atributos que forma el archivo e identifica dónde se encuentra cada atributo.                                                                                                                                                                                                                                                                                                                                          |
| ::$BITMAP                  | Mapa de bits utilizado por los índices para administrar el espacio libre del árbol b para un directorio. El árbol b se administra en fragmentos de 4 KB (independientemente del tamaño del clúster) y se usa para administrar la asignación de estos fragmentos. Este tipo de flujo está presente en todos los directorios.                                                                                                                                                                                           |
| ::$DATA                    | Flujo de datos. El flujo de datos predeterminado no tiene ningún nombre. Los flujos de datos se pueden enumerar mediante las [**funciones FindFirstStreamW**](/windows/desktop/api/fileapi/nf-fileapi-findfirststreamw) [**y FindNextStreamW.**](/windows/desktop/api/fileapi/nf-fileapi-findnextstreamw)                                                                                                                                                                                                                                                |
| ::$EA                      | Contiene datos de atributos extendidos.|
| ::$EA \_ INFORMATION         | Contiene información de compatibilidad sobre los atributos extendidos.                                                                                                                                                                                                                                                                                                                                                                                      |
| ::$FILE \_ NAME              | Nombre del archivo, en caracteres Unicode. Esto incluye el nombre corto del archivo, así como los vínculos duros.                                                                                                                                                                                                                                                                                                                                 |
| ::$INDEX \_ ALLOCATION       | Tipo de secuencia de un directorio. Se usa para implementar la asignación de nombres de archivo para directorios grandes. Esta secuencia representa el propio directorio y contiene todos los datos del directorio. Los cambios en las secuencias de este tipo se registran en el diario de cambios NTFS. El nombre de flujo predeterminado de un tipo de flujo ALLOCATION de $INDEX es $I 30, por lo que \_ "*DirName*", "*DirName*::$INDEX ALLOCATION" y \_ "*DirName*:$I 30:$INDEX \_ ALLOCATION" son equivalentes. |
| ::$INDEX \_ ROOT             | Esta secuencia representa la raíz del árbol b de un índice. Este tipo de flujo está presente en todos los directorios.                                                                                                                                                                                                                                                                                                                                           |
| ::$LOGGED DE \_ UTILIDAD \_ | Similar a ::$DATA pero las operaciones se registran en el diario de cambios NTFS. Usado por EFS y [NTFS transaccional (TxF).](transactional-ntfs-portal.md) El par ":*StreamName*:$*StreamType*" para EFS es ":$EFS:$LOGGED UTILITY STREAM" y para \_ \_ TxF es ":$TXF \_ DATA:$LOGGED \_ UTILITY \_ STREAM".                                                                                                                                                    |
| ::$OBJECT \_ ID              | Identificador de 16 bytes que se usa para identificar el archivo para el servicio de seguimiento de vínculos.                                                                                                                                                                                                                                                                                                                                                                           |
| ::$REPARSE \_ POINT          | Datos [de punto de reanción.](reparse-points.md)|



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de Secuencias](using-streams.md)
</dt> </dl>

 

 



