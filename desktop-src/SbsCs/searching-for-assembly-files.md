---
description: Buscar archivos de ensamblado
ms.assetid: 6e6c1104-5cde-4c07-9ee2-d87062675dac
title: Buscar archivos de ensamblado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7be73b162ea41fd9eeb0a042a1fc2e202b8115
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278597"
---
# <a name="searching-for-assembly-files"></a>Buscar archivos de ensamblado

Los contextos de activación pueden ayudar al cargador a encontrar archivos de ensamblado. Cuando el cargador busca un archivo para cargarlo por nombre, busca primero los archivos con el nombre especificado a los que hacen referencia los ensamblados que son miembros del contexto de activación actualmente activo. Una llamada a [**SearchPath**](/windows/desktop/api/processenv/nf-processenv-searchpathw) también busca primero estos archivos. Los archivos que tienen el nombre especificado y el contexto de activación actual se encuentran y cargan antes que los archivos con el nombre en el directorio local o en la variable de entorno PATH. Esto significa que cuando se crean manifiestos, es necesario enumerar todos los archivos que se van a usar con las importaciones de **SearchPath**, [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)o static.

Tenga en cuenta que estos archivos no se encuentran automáticamente al usar [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) u otras funciones que no buscan archivos. Para usar estos archivos con **CreateFile**, use [**SearchPath**](/windows/desktop/api/processenv/nf-processenv-searchpathw) primero para buscar la ruta de acceso al archivo aislado y, a continuación, use **CreateFile** en la ruta de acceso devuelta.

Este método de búsqueda de archivos ayuda a mantener las aplicaciones aisladas por separado porque varios archivos con el mismo nombre pueden diferir solo en función de su asociación con ensamblados de números de versión diferentes. El sistema operativo puede encontrar el archivo correcto que se debe usar durante las operaciones de archivo.

Si se carga un archivo DLL de esta manera mediante [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya), se llama al punto de entrada (DllMain) del archivo dll mientras el contexto de activación original se mantiene activo, excepto si el propio archivo dll contiene un manifiesto en un determinado identificador de recurso ( \_ identificador de recurso del manifiesto ISOLATIONAWARE \_ \_ o 2)

 

 
