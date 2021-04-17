---
description: La acción InstallFiles copia los archivos especificados en la tabla de archivos del directorio de origen en el directorio de destino.
ms.assetid: 187ad82f-13f5-4ea3-913c-2ae7561a6ee6
title: InstallFiles (acción)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c2a0206ec5a64974f27375e175f25ce1888b430
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666732"
---
# <a name="installfiles-action"></a>InstallFiles (acción)

La acción InstallFiles copia los archivos especificados en la tabla de archivos del directorio de origen en el directorio de destino.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción InstallFiles debe aparecer después de la acción [InstallValidate](installvalidate-action.md) y antes de cualquier acción dependiente de archivos.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción                      |
|-------|-------------------------------------------------|
| \[1\] | Identificador del archivo instalado.                   |
| \[6\] | Tamaño del archivo instalado en bytes.                |
| \[9\] | Identificador del directorio que contiene el archivo instalado. |



 

## <a name="remarks"></a>Observaciones

La acción InstallFiles opera en los archivos especificados en la [tabla File](file-table.md). Cada archivo se instala en función del estado de instalación del componente asociado del archivo en la [tabla de componentes](component-table.md). Solo se pueden copiar los archivos cuyos componentes se resuelven en el estado **msiInstallStatelocal** .

La acción InstallFiles implementa las siguientes columnas de la tabla File.

-   La columna FileName especifica el nombre del archivo de destino.
-   La columna version especifica la versión del archivo.
-   La columna atributos especifica los bits del indicador de atributo de instalación y archivo.
-   La columna archivo especifica el token de archivo único.
-   La columna archivo especifica el tamaño de archivo sin comprimir en bytes.
-   La columna Language especifica el identificador de idioma del archivo.
-   La columna Sequence especifica el número de secuencia en el medio.

La acción InstallFiles implementa las siguientes columnas de la tabla de componentes.

-   La \_ columna Directory especifica una referencia a un elemento de [tabla de directorio](directory-table.md) .
-   La columna componente especifica un nombre único para el elemento de componente.

El archivo especificado solo se copia si se cumple una de las siguientes condiciones:

-   El archivo no está instalado actualmente en el equipo local.
-   El archivo está en el equipo local, pero tiene un número de versión inferior al del archivo en la [tabla de archivos](file-table.md).
-   El archivo está en el equipo local, pero no hay ningún número de versión asociado.

El directorio de origen de cada archivo que se va a copiar viene determinado por el sourceMode, que a su vez depende del valor de la columna Cabinet de la tabla de medios. Para obtener una descripción completa del modo de origen, vea la [tabla de medios](media-table.md).

Si el directorio de origen de un archivo que se va a copiar reside en un medio extraíble, como un disquete o un CD-ROM, la acción InstallFiles comprueba que se inserte el medio de origen adecuado antes de intentar copiar el archivo. InstallFiles busca medios del mismo tipo extraíble con una etiqueta de [*volumen*](v-gly.md) que coincida con el valor especificado en la columna VolumeLabel de la tabla de medios. Si se encuentra un volumen montado coincidente, el proceso de copia de archivos continúa. Si no se encuentra ninguna coincidencia, un cuadro de diálogo solicita al usuario que inserte el medio adecuado. En este caso, el cuadro de diálogo utiliza el nombre de medio que se encuentra en la columna DiskPrompt de la tabla de medios como parte del mensaje.

Se debe tener cuidado porque la acción InstallFiles puede eliminar un archivo original y no reemplazarlo. Esto sucede cuando la acción InstallFiles experimenta un error al reemplazar un archivo más antiguo y el usuario elige omitir el error. El comportamiento predeterminado del instalador es eliminar un archivo antiguo antes de asegurarse de que el nuevo archivo se copia correctamente.

Para consultar las reglas de control de versiones de archivo que usa el instalador, consulte [reglas de control de versiones de archivos](file-versioning-rules.md).

 

 



