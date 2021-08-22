---
title: Crear un archivo a partir de una Secuencias
description: Crear un archivo a partir de una Secuencias
ms.assetid: 5149a766-7809-42b7-8e5c-b67b847b9218
keywords:
- Función AVISave
- Función AVISaveV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a15a6ad3770f93bc2fb77dcb79975e1e9aa1fc8da7319e34c140baf488a69554
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498015"
---
# <a name="creating-a-file-from-existing-streams"></a>Crear un archivo a partir de una Secuencias

Una manera de crear un archivo que contiene flujos de datos es combinar secuencias existentes en un archivo nuevo. Las secuencias que proporcionan datos para el nuevo archivo pueden residir en memoria o en uno o varios archivos.

Puede compilar un archivo a partir de varias secuencias mediante la [**función AVISave.**](/windows/desktop/api/Vfw/nf-vfw-avisavea) Esta función crea un archivo y escribe en el archivo los flujos de datos especificados en su secuencia de llamada. La secuencia de llamada para **AVISave** usa un número variable de argumentos que incluyen interfaces para las secuencias combinadas en el nuevo archivo.

También puede combinar flujos de datos en un archivo nuevo mediante la [**función AVISaveV.**](/windows/desktop/api/Vfw/nf-vfw-avisaveva) Esta función proporciona la misma funcionalidad que **AVISave,** pero cuando se usa **AVISaveV,** la aplicación especifica los flujos de datos como una matriz, no como un número variable de argumentos.

Puede crear un cuadro de diálogo en el que el usuario pueda seleccionar la configuración de compresión para el nuevo archivo mediante la [**función AVISaveOptions.**](/windows/desktop/api/Vfw/nf-vfw-avisaveoptions) El cuadro de diálogo muestra la configuración de compresión actual y permite que el usuario las edite. Los cambios de configuración de compresión se almacenan [**en una estructura AVICOMPRESSOPTIONS.**](/windows/desktop/api/Vfw/ns-vfw-avicompressoptions)

También puede incluir una función de devolución de llamada con [**AVISave**](/windows/desktop/api/Vfw/nf-vfw-avisavea) y [**AVISaveV**](/windows/desktop/api/Vfw/nf-vfw-avisaveva) que la aplicación puede usar para mostrar el progreso de la escritura del archivo y, si es necesario, permitir que el usuario cancele la operación de guardado. Puede incluir la dirección de la función de devolución de llamada en la secuencia de llamada de **AVISave** **o AVISaveV**.

Puede permitir que el usuario seleccione un nombre de archivo para el nuevo archivo mediante la [**función GetSaveFileNamePreview.**](/windows/desktop/api/Vfw/nf-vfw-getsavefilenamepreviewa) Esta función muestra el cuadro de diálogo Guardar como en el que el usuario puede obtener una vista previa de la primera secuencia (normalmente la secuencia de vídeo) de un archivo AVI.

Puede crear un puntero de interfaz de archivo (y un archivo virtual) para un grupo de secuencias mediante la [**función AVIMakeFileFromStreams.**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) Otras funciones AVIFile pueden usar el puntero de interfaz de archivo devuelto por esta función para acceder a las secuencias del archivo virtual. Cuando termine de usar el archivo virtual, elimine el puntero de interfaz de archivo mediante la [**función AVIFileRelease.**](/windows/desktop/api/Vfw/nf-vfw-avifilerelease)

> [!Note]  
> Para minimizar la degradación de imágenes y audio, evite comprimir un archivo AVI más de una vez. Combine fragmentos de vídeo sin comprimir en el sistema de edición y, a continuación, comprima el producto final. Para obtener información sobre las opciones de compresión, vea [Administrador de compresión de vídeo](video-compression-manager.md).

 

 

 




