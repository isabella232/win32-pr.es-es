---
description: Búsqueda de archivos de ensamblado
ms.assetid: 6e6c1104-5cde-4c07-9ee2-d87062675dac
title: Búsqueda de archivos de ensamblado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7be73b162ea41fd9eeb0a042a1fc2e202b8115
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171270"
---
# <a name="searching-for-assembly-files"></a>Búsqueda de archivos de ensamblado

Los contextos de activación pueden ayudar al cargador a encontrar archivos de ensamblado. Cuando el cargador busca un archivo para cargar por nombre, primero busca archivos con el nombre especificado al que hacen referencia los ensamblados que son miembros del contexto de activación activo actualmente. Una llamada a [**SearchPath también**](/windows/desktop/api/processenv/nf-processenv-searchpathw) busca estos archivos en primer lugar. Los archivos que tienen el nombre especificado y el contexto de activación actual se encuentran y cargan antes que los archivos con el nombre en el directorio local o en la variable de entorno PATH. Esto significa que al crear manifiestos, debe enumerar todos los archivos que planea usar con **SearchPath,** [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)o importaciones estáticas.

Tenga en cuenta que estos archivos no se encuentran automáticamente cuando se [**usa CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) u otras funciones que no buscan archivos. Para usar estos archivos con **CreateFile,** use [**SearchPath**](/windows/desktop/api/processenv/nf-processenv-searchpathw) primero para buscar la ruta de acceso al archivo aislado y, a continuación, use **CreateFile** en la ruta de acceso devuelta.

Este método de búsqueda de archivos ayuda a mantener las aplicaciones aisladas separadas porque varios archivos con el mismo nombre solo pueden diferir por su asociación con ensamblados de números de versión diferentes. El sistema operativo puede encontrar el archivo correcto que se usará durante las operaciones de archivo.

Si un archivo DLL se carga de esta manera mediante [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya), se llama al punto de entrada de ese archivo DLL (DllMain) mientras el contexto de activación original se mantiene activo, excepto si el propio archivo DLL contiene un manifiesto en un identificador de recurso determinado (ID. de RECURSO DE MANIFIESTO ISOLATIONAWARE, \_ o \_ \_ 2)

 

 
