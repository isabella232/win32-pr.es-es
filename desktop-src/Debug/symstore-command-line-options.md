---
description: Los siguientes formularios de sintaxis son compatibles con las transacciones de SymStore. El primer parámetro siempre debe ser add o del. El orden de los demás parámetros no importa.
ms.assetid: d6d10adb-cb17-4ce3-b0e5-493b313ebdba
title: Opciones de Command-Line SymStore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc166ab82fc40ad11eb9b014a003dc793f3bb7cc1d70792370bd175c68802417
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119572985"
---
# <a name="symstore-command-line-options"></a>Opciones de Command-Line SymStore

Los siguientes formularios de sintaxis son compatibles con las transacciones de SymStore. El primer parámetro siempre debe ser add o del. El orden de los demás parámetros no importa.

**symstore add** \[ **/l** **/o** **/p** **/r** **/compress** \] \[ **-:MSG** *Message* \] \[ **-:REL** \] \[ **-:NOREFS** \] **/f** File **/s** *Store*  **/t** *Product* \[ **/v** *Version* \] \[ **/c** *Comment* \] \[ **/d** *LogFile*\]

**symstore add** \[ **/a** **/l** **/o** **/p** **/r** \] \[ **-:REL** \] \[ **-:NOREFS** \] **/g** *Share* **/f** *File* **/x** *IndexFile* \[ **/d** *LogFile*\]

**symstore add** \[ **/o** **/compress** \] \[ **/p** \[ **-:MSG** \| *Message* \] \[ **-:REL** \] \[ **-:NOREFS** \] \] **/y** *IndexFile* **/g** *Share* **/s** *Store* **/t** *Product* \[ **/v** *Version* \] \[ **/c** *Comment* \] \[ **/d** *LogFile*\]

**consulta de symstore** \[ **/o** **/r** \] **/f** *File* **/s** *Store* \[ **/d** *LogFile*\]

**symstore del** **/i** *ID* **/s** *Store* \[ **/o** \] \[ **/d** *LogFile*\]

**symstore** **/?**



| Parámetro      | Significado                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /a             | Hace que SymStore anexe nueva información de indexación a un archivo de índice existente. (Esta opción solo se usa con la opción /x).                                                                                                                                                                                                                                                                                 |
| /c *(Comentario)*   | Especifica un comentario para la transacción.                                                                                                                                                                                                                                                                                                                                                                     |
| /compress      | Hace que SymStore cree una versión comprimida de cada archivo copiado en el almacén de símbolos en lugar de usar una copia sin comprimir del archivo. Esta opción solo es válida cuando se almacenan archivos y no punteros, y no se puede usar con la opción /p.                                                                                                                                                              |
| /d *LogFile*   | Especifica un archivo de registro que se usará para la salida del comando. Si no se incluye, la información de transacción y otros resultados se envían a stdout.                                                                                                                                                                                                                                                                     |
| /f *File*      | Especifica una o varias rutas de acceso de archivo (o directorios) que se agregarán. Si una ruta de acceso de archivo especificada comienza con un símbolo "@", se espera un archivo de respuesta que contenga una lista de archivos que se van [a](../midl/response-files.md) agregar (una ruta de acceso de archivo por línea).                                                                                                                                             |
| /g *Recurso compartido*     | Especifica el servidor y el recurso compartido donde se almacenaron originalmente los archivos de símbolos. Cuando se usa con /f, *El* recurso compartido debe ser idéntico al principio del *especificador* de archivo. Cuando se usa con /y, *Compartir* debe ser la ubicación de los archivos de símbolos originales (no el archivo de índice). Esto le permite cambiar más adelante esta parte de la ruta de acceso del archivo en caso de que mueva los archivos de símbolos a otro servidor y recurso compartido. |
| /i *ID*        | Especifica la cadena de identificador de transacción.                                                                                                                                                                                                                                                                                                                                                                         |
| /l             | Permite que el archivo esté en un directorio local en lugar de en una ruta de acceso de red. (Esta opción solo se usa con la opción /p).                                                                                                                                                                                                                                                                                        |
| /o             | Hace que SymStore muestre una salida detallada.                                                                                                                                                                                                                                                                                                                                                                   |
| /p             | Hace que SymStore almacene un puntero al archivo, en lugar del propio archivo.                                                                                                                                                                                                                                                                                                                                 |
| /r             | Hace que SymStore agregue archivos o directorios de forma recursiva.                                                                                                                                                                                                                                                                                                                                                     |
| /s *Store*     | Especifica el directorio raíz del almacén de símbolos.                                                                                                                                                                                                                                                                                                                                                           |
| /t *Product*   | Especifica el nombre del producto.                                                                                                                                                                                                                                                                                                                                                                           |
| Versión de */v*   | Especifica la versión del producto.                                                                                                                                                                                                                                                                                                                                                                        |
| /x *IndexFile* | Hace que SymStore no almacene los archivos de símbolos reales. En su lugar, SymStore registra información en *IndexFile que* permitirá que SymStore acceda a los archivos de símbolos más adelante.                                                                                                                                                                                                                         |
| /y *IndexFile* | Hace que SymStore lea los datos de un archivo creado con /x.                                                                                                                                                                                                                                                                                                                                                |
| -:MSG Message  | Agrega el mensaje especificado a cada archivo. (Esta opción solo se puede usar cuando se usa /p).                                                                                                                                                                                                                                                                                                                     |
| -:REL          | Permite que las rutas de acceso de los punteros de archivo sean relativas. Esta opción implica la opción /l. (Esta opción solo se puede usar cuando se usa /p).                                                                                                                                                                                                                                                                     |
| -:NOREFS       | Omite la creación de archivos de puntero de referencia para los archivos y punteros que se almacenan. Esta opción solo es válida durante la creación inicial de un almacén de símbolos si el almacén que se va a cambiar se creó con esta opción.                                                                                                                                                                                      |
| /?             | Muestra el texto de ayuda del comando SymStore.                                                                                                                                                                                                                                                                                                                                                                 |



 

 

 



