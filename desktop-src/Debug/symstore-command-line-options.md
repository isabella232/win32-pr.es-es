---
description: Se admiten los siguientes formatos de sintaxis para las transacciones SymStore. El primer parámetro siempre debe ser Add o del. No importa el orden de los demás parámetros.
ms.assetid: d6d10adb-cb17-4ce3-b0e5-493b313ebdba
title: Opciones de Command-Line de SymStore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76b69cdca9ee74cf01041375f26b2e151dc3ec5d
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "104361988"
---
# <a name="symstore-command-line-options"></a>Opciones de Command-Line de SymStore

Se admiten los siguientes formatos de sintaxis para las transacciones SymStore. El primer parámetro siempre debe ser Add o del. No importa el orden de los demás parámetros.

**symstore agregar** \[ **/l** **/o** **/p** **/r** **/compress** \] \[ **-: msg** *Message* \] \[ **-: REL** \] \[ **-: NOREFS** \] **/f** *File* **/s** *Store* **/t** *Product* \[ **/v** *version* \] \[ **/c** *comment* \] \[ **/d** *logfile*\]

**symstore agregar** \[ **/a** **/l** **/o** **/p** **/r** \] \[ **-: REL** \] \[ **-: NOREFS** \] **/g** *share* **/f** *File* **/x** *IndexFile* \[ **/d** *logfile*\]

**symstore agregar** \[ **/o** **/compress** \] \[ **/p** \[ **-: msg** \| *Message* \] \[ **-: REL** \] \[ **-: NOREFS** \] \] **/y** *IndexFile* **/g** *share* **/s** *Store* **/t** *Product* \[ **/v** *version* \] \[ **/c** *comment* \] \[ **/d** *logfile*\]

**consulta symstore** \[ **/o** **/r** \] **/f** *File* **/s** *Store* \[ **/d** *logfile*\]

**symstore del** **/i** *ID* **/s** *Store* \[ **/o** \] \[ **/d** *logfile*\]

**symstore** **/?**



| Parámetro      | Significado                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /a             | Hace que SymStore Anexe información de indización nueva a un archivo de índice existente. (Esta opción solo se usa con la opción/x).                                                                                                                                                                                                                                                                                 |
| /c *Comentario*   | Especifica un comentario para la transacción.                                                                                                                                                                                                                                                                                                                                                                     |
| /compress      | Hace que SymStore cree una versión comprimida de cada archivo copiado en el almacén de símbolos en lugar de usar una copia sin comprimir del archivo. Esta opción solo es válida cuando se almacenan archivos y no punteros, y no se puede usar con la opción/p.                                                                                                                                                              |
| /d *logfile*   | Especifica un archivo de registro que se usará para la salida del comando. Si no se incluye, la información de la transacción y otros resultados se envían a stdout.                                                                                                                                                                                                                                                                     |
| /f ( *archivo* )      | Especifica una o más rutas de acceso de archivo (o directorios) que se van a agregar. Si una ruta de acceso de archivo especificada comienza con un símbolo ' @ ', se espera un [archivo de respuesta](../midl/response-files.md) que contenga una lista de archivos que se van a agregar (una ruta de acceso de archivo por línea).                                                                                                                                             |
| /g *compartir*     | Especifica el servidor y el recurso compartido donde se almacenaron originalmente los archivos de símbolos. Cuando se usa con/f, el *recurso compartido* debe ser idéntico al principio del especificador de *archivo* . Cuando se usa con/y, *share* debe ser la ubicación de los archivos de símbolos originales (no el archivo de índice). Esto le permite cambiar posteriormente esta parte de la ruta de acceso del archivo en caso de que mueva los archivos de símbolos a un servidor y un recurso compartido distintos. |
| /i *ID*        | Especifica la cadena del identificador de la transacción.                                                                                                                                                                                                                                                                                                                                                                         |
| /l             | Permite que el archivo esté en un directorio local en lugar de una ruta de acceso de red. (Esta opción solo se usa con la opción/p).                                                                                                                                                                                                                                                                                        |
| /o             | Hace que SymStore muestre la salida detallada.                                                                                                                                                                                                                                                                                                                                                                   |
| /p             | Hace que SymStore almacene un puntero al archivo, en lugar del propio archivo.                                                                                                                                                                                                                                                                                                                                 |
| /r             | Hace que SymStore agregue archivos o directorios de forma recursiva.                                                                                                                                                                                                                                                                                                                                                     |
| /s *tienda*     | Especifica el directorio raíz del almacén de símbolos.                                                                                                                                                                                                                                                                                                                                                           |
| /t *producto*   | Especifica el nombre del producto.                                                                                                                                                                                                                                                                                                                                                                           |
| /v *versión*   | Especifica la versión del producto.                                                                                                                                                                                                                                                                                                                                                                        |
| /x *IndexFile* | Hace que SymStore no almacene los archivos de símbolos reales. En su lugar, SymStore registra información en el *IndexFile* que permitirá a SymStore tener acceso a los archivos de símbolos más adelante.                                                                                                                                                                                                                         |
| /y *IndexFile* | Hace que SymStore Lea los datos de un archivo creado con/x.                                                                                                                                                                                                                                                                                                                                                |
| -: Mensaje MSG  | Agrega el mensaje especificado a cada archivo. (Esta opción solo se puede usar cuando se usa/p).                                                                                                                                                                                                                                                                                                                     |
| -: REL          | Permite que las rutas de acceso de los punteros de archivo sean relativas. Esta opción implica la opción/l. (Esta opción solo se puede usar cuando se usa/p).                                                                                                                                                                                                                                                                     |
| -:NOREFS       | Omite la creación de archivos de puntero de referencia para los archivos y punteros que se están almacenando. Esta opción solo es válida durante la creación inicial de un almacén de símbolos si el almacén que se está cambiando se creó con esta opción.                                                                                                                                                                                      |
| /?             | Muestra el texto de ayuda para el comando SymStore.                                                                                                                                                                                                                                                                                                                                                                 |



 

 

 



