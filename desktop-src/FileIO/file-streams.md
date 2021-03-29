---
description: En el sistema de archivos NTFS, las secuencias contienen los datos que se escriben en un archivo y que proporcionan más información sobre un archivo que los atributos y las propiedades.
ms.assetid: 41dda6f1-a6d1-4e76-94f3-a72f9e491bee
title: Secuencias de archivo (sistemas de archivos locales)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a934a51225a886e3d5a7de4d9e1e91900fab460
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812523"
---
# <a name="file-streams-local-file-systems"></a>Secuencias de archivo (sistemas de archivos locales)

Una secuencia es una secuencia de bytes. En el sistema de archivos NTFS, las secuencias contienen los datos que se escriben en un archivo y que proporcionan más información sobre un archivo que los atributos y las propiedades. Por ejemplo, puede crear una secuencia que contenga palabras clave de búsqueda o la identidad de la cuenta de usuario que crea un archivo.

Cada flujo que está asociado a un archivo tiene su propio tamaño de asignación, el tamaño real y la longitud de datos válida:

-   El tamaño de asignación es la cantidad de espacio en disco que se reserva para un flujo.
-   El tamaño real es el número de bytes que usa un llamador.
-   La longitud de datos válida (VDL) es el número de bytes que se inicializan a partir del tamaño de asignación de la secuencia.

Cada flujo también mantiene su propio estado de compresión, cifrado y dispersión. El atributo de archivo **\_ \_ \_ disperso de atributo de archivo** del archivo se establece en el miembro **dwFileAttributes** de la estructura de datos de [**\_ búsqueda \_ de Win32**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) devuelta por las funciones [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa)y [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) si alguna de las secuencias ha sido dispersa. [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa), [**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa), [**GetFileAttributesTransacted**](/windows/desktop/api/WinBase/nf-winbase-getfileattributestransacteda), [**GetFileInformationByHandle**](/windows/desktop/api/FileAPI/nf-fileapi-getfileinformationbyhandle)y [**GetFileInformationByHandleEx**](/windows/desktop/api/WinBase/nf-winbase-getfileinformationbyhandleex) devuelven el estado disperso del flujo de datos predeterminado si no se especifica ningún flujo.

No hay ningún tiempo de archivo asociado a una secuencia. Las horas de archivo de un archivo se actualizan cuando se actualiza cualquier secuencia de un archivo.

Los bloqueos oportunistas se mantienen por secuencia. Los modos de uso compartido también se mantienen por secuencia. Cuando se solicita el acceso de eliminación en un archivo, el sistema operativo comprueba el acceso de eliminación en todas las secuencias abiertas en un archivo. Si otro proceso ha abierto una secuencia sin el permiso de **\_ \_ eliminación de recurso compartido de archivos** , no podrá abrir el archivo para el acceso de eliminación.

Si un archivo que se está copiando tiene un flujo de datos y se usa el redirector de red, el archivo solo se puede copiar si el cliente tiene el permiso de lectura y el permiso de atributos de lectura.

## <a name="naming-conventions-for-streams"></a>Convenciones de nomenclatura para flujos

Cuando se especifica desde la línea de comandos del shell de Windows, el nombre completo de una secuencia es "*filename*:*Stream Name*:*Stream Type*", como en el ejemplo siguiente: "Perfile. dat: stream1: $Data".

Los caracteres que son válidos para un nombre de archivo también son válidos para el nombre de la secuencia, incluidos los espacios. Para obtener más información, vea [asignar un nombre a un archivo](naming-a-file.md). El tipo de secuencia (también denominado código de tipo de atributo) es interno del sistema de archivos NTFS. Por lo tanto, los usuarios no pueden crear nuevos tipos de secuencias, pero pueden abrir tipos existentes del sistema de archivos NTFS. Los valores del especificador de tipo de flujo siempre empiezan con el símbolo de dólar ($). A continuación se muestra una lista de tipos de flujo.

De forma predeterminada, el flujo de datos predeterminado no tiene nombre. Para especificar por completo el flujo de datos predeterminado, use "*filename*:: $Data", donde $Data es el tipo de flujo. Es el equivalente de "*filename*". Puede crear una secuencia con nombre en el archivo mediante las [convenciones de nomenclatura de archivos](naming-a-file.md). Tenga en cuenta que "$DATA" es un nombre de flujo válido. Por ejemplo, el nombre completo de una secuencia denominada "$DATA" en un archivo denominado "*Sample*" sería "*Sample*: $Data: $Data". Si ha creado una secuencia denominada "bar" en el mismo archivo, su nombre completo sería "*Sample*: bar: $Data".

Al crear y trabajar con archivos que tienen nombres de caracteres de un solo carácter, anteponga al nombre de archivo un punto seguido de una barra diagonal inversa (. \) o use un nombre de ruta de acceso completo. La razón para ello es que Windows trata los nombres de archivo de un solo carácter como Letras de unidad. Cuando se especifica una letra de unidad con una ruta de acceso relativa, un signo de dos puntos separa la letra de unidad de la ruta de acceso. Cuando hay ambigüedad sobre si un nombre de un carácter es una letra de unidad o un nombre de archivo, Windows supone que es una letra de unidad si la cadena que sigue a los dos puntos es una ruta de acceso válida, aunque la letra de unidad no sea válida.

## <a name="stream-types"></a>Tipos de secuencias

A continuación se muestra la lista de tipos de secuencia de NTFS, también denominados códigos de tipo de atributo. Algunos de los tipos de secuencia son internos a NTFS y su formato no está documentado.



| Tipo de secuencia                | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| :: $ATTRIBUTE \_ lista         | Contiene una lista de todos los atributos que componen el archivo e identifica dónde se encuentra cada atributo.                                                                                                                                                                                                                                                                                                                                          |
| :: $BITMAP                  | Un mapa de bits que usan los índices para administrar el espacio disponible en el árbol b para un directorio. El árbol b se administra en fragmentos de 4 KB (independientemente del tamaño del clúster) y se usa para administrar la asignación de estos fragmentos. Este tipo de secuencia está presente en todos los directorios.                                                                                                                                                                                           |
| :: $DATA                    | Flujo de datos. El flujo de datos predeterminado no tiene nombre. Los flujos de datos se pueden enumerar mediante las funciones [**FindFirstStreamW**](/windows/desktop/api/fileapi/nf-fileapi-findfirststreamw) y [**FindNextStreamW**](/windows/desktop/api/fileapi/nf-fileapi-findnextstreamw) .                                                                                                                                                                                                                                                |
| :: $EA                      | Contiene datos de atributos extendidos.|
| :: $EA \_ información         | Contiene información de soporte técnico sobre los atributos extendidos.                                                                                                                                                                                                                                                                                                                                                                                      |
| :: $FILE \_ nombre              | Nombre del archivo, en caracteres Unicode. Esto incluye el nombre corto del archivo, así como los vínculos físicos.                                                                                                                                                                                                                                                                                                                                 |
| :: $INDEX \_ asignación       | El tipo de secuencia de un directorio. Se usa para implementar la asignación de nombres de archivo para directorios grandes. Esta secuencia representa el propio directorio y contiene todos los datos del directorio. Los cambios en las secuencias de este tipo se registran en el diario de cambios de NTFS. El nombre de flujo predeterminado de un \_ tipo de flujo de asignación $index es $I 30, por lo que "*dirname*", "*dirname*:: $index \_ Allocation" y "*dirname*: $I 30: $index \_ Allocation" son equivalentes. |
| :: $INDEX \_ raíz             | Esta secuencia representa la raíz del árbol b de un índice. Este tipo de secuencia está presente en todos los directorios.                                                                                                                                                                                                                                                                                                                                           |
| :: $LOGGED \_ secuencia de la utilidad \_ | Similar a:: $DATA pero las operaciones se registran en el diario de cambios de NTFS. Usado por EFS y [NTFS transaccional (TxF)](transactional-ntfs-portal.md). El par ":*nombredeflujo*: $*STREAMTYPE*" para EFS es ": $EFS: $logged \_ secuencia de utilidades \_ " y para TxF es ": $TxF \_ Data: $logged la secuencia de \_ utilidades \_ ".                                                                                                                                                    |
| :: $OBJECT \_ ID.              | IDENTIFICADOR de 16 bytes que se usa para identificar el archivo para el servicio de seguimiento de vínculos.                                                                                                                                                                                                                                                                                                                                                                           |
| :: $REPARSE \_ punto          | Los datos del [punto de reanálisis](reparse-points.md) .|



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar secuencias](using-streams.md)
</dt> </dl>

 

 



