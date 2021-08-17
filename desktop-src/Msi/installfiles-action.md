---
description: La acción InstallFiles copia los archivos especificados en la tabla File del directorio de origen al directorio de destino.
ms.assetid: 187ad82f-13f5-4ea3-913c-2ae7561a6ee6
title: Acción InstallFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8df2a62deb253314e84e72cd84e88052f1175db7451807c3f266542e29c10c7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118629936"
---
# <a name="installfiles-action"></a>Acción InstallFiles

La acción InstallFiles copia los archivos especificados en la tabla File del directorio de origen al directorio de destino.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción InstallFiles debe ir después de [la acción InstallValidate](installvalidate-action.md) y antes de cualquier acción dependiente del archivo.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción                      |
|-------|-------------------------------------------------|
| \[1\] | Identificador del archivo instalado.                   |
| \[6\] | Tamaño del archivo instalado en bytes.                |
| \[9\] | Identificador del directorio que contiene el archivo instalado. |



 

## <a name="remarks"></a>Comentarios

La acción InstallFiles funciona en los archivos especificados en la [tabla File](file-table.md). Cada archivo se instala en función del estado de instalación del componente asociado del archivo en la [tabla Component](component-table.md). Solo los archivos cuyos componentes se resuelven en **el estado msiInstallStatelocal** son aptos para la copia.

La acción InstallFiles implementa las siguientes columnas de la tabla File.

-   La columna FileName especifica el nombre del archivo de destino.
-   La columna Versión especifica la versión del archivo.
-   La columna Atributos especifica los bits de marca de atributo de instalación y archivo.
-   La columna Archivo especifica el token de archivo único.
-   La columna FileSize especifica el tamaño de archivo sin comprimir en bytes.
-   La columna Idioma especifica el identificador de idioma del archivo.
-   La columna Secuencia especifica el número de secuencia en los medios.

La acción InstallFiles implementa las siguientes columnas de la tabla Component.

-   La columna \_ Directory especifica una referencia a un elemento de tabla [Directory.](directory-table.md)
-   La columna Componente especifica un nombre único para el elemento de componente.

El archivo especificado solo se copia si se cumple una de las siguientes condiciones:

-   El archivo no está instalado actualmente en el equipo local.
-   El archivo está en el equipo local, pero tiene un número de versión inferior al archivo de la [tabla File](file-table.md).
-   El archivo está en el equipo local, pero no hay ningún número de versión asociado.

El directorio de origen de cada archivo que se va a copiar viene determinado por sourceMode, que a su vez depende del valor de la columna Gabinete de la tabla Media. Para obtener una explicación completa del modo de origen, vea la [tabla Multimedia](media-table.md).

Si el directorio de origen de un archivo que se va a copiar reside en medios extraíbles, como un disquete o CD-ROM, la acción InstallFiles comprueba que se insertan los medios de origen adecuados antes de intentar copiar el archivo. InstallFiles busca medios del mismo tipo extraíble [](v-gly.md) con una etiqueta de volumen que coincida con el valor especificado en la columna VolumeLabel de la tabla Media. Si se encuentra un volumen montado correspondiente, el proceso de copia de archivos continúa. Si no se encuentra ninguna coincidencia, un cuadro de diálogo solicita al usuario que inserte el medio adecuado. En este caso, el cuadro de diálogo usa el nombre de medio que se encuentra en la columna DiskPrompt de la tabla Media como parte del símbolo del sistema.

Debe tener cuidado porque la acción InstallFiles puede eliminar un archivo original y no reemplazarlo. Esto ocurre cuando la acción InstallFiles experimenta un error al reemplazar un archivo anterior y el usuario elige omitir el error. El comportamiento predeterminado del instalador es eliminar un archivo antiguo antes de asegurarse de que el nuevo archivo se copia correctamente.

Para obtener las reglas de control de versiones de archivos que usa el instalador, vea [Reglas de control de versiones de archivos](file-versioning-rules.md).

 

 



