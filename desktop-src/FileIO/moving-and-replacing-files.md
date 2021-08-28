---
description: Consideraciones para mover y reemplazar archivos mediante las funciones CopyFileEx, CreateFile, Replacefile y MoveFileEx.
ms.assetid: 4872af0d-42e8-4576-9aa9-4b8671375f2e
title: Mover y reemplazar archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35c78085865006d1dfbbe322239c4704d215d038897b81d1f139d66d06f65bbc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696016"
---
# <a name="moving-and-replacing-files"></a>Mover y reemplazar archivos

Para poder realizar una operación de copia, el archivo de origen debe cerrarse o abrirse solo para lectura. Ningún subproceso puede tener abierto el archivo de código fuente para escritura. Para copiar un archivo existente en uno nuevo, use la [**función CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile) o [**CopyFileEx.**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) Las aplicaciones pueden especificar si **CopyFile y** **CopyFileEx** producirán un error si el archivo de destino ya existe. Si el archivo de destino existe y está abierto, se debe haber abierto con los permisos de uso compartido aplicables. Para obtener más información, vea [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea).

La [**función CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) también permite a una aplicación especificar la dirección de una función de devolución de llamada (vea [**CopyProgressRoutine)**](/windows/desktop/api/WinBase/nc-winbase-lpprogress_routine)a la que se llama cada vez que se copia otra parte del archivo. La aplicación puede usar esta información para mostrar un indicador que muestra el número total de bytes copiados como porcentaje del tamaño total del archivo.

La [**función ReplaceFile**](/windows/desktop/api/WinBase/nf-winbase-replacefilea) reemplaza un archivo por otro, con la opción de crear una copia de seguridad del archivo original. La función conserva los atributos del archivo original, como su hora de creación, acl y atributo de cifrado.

También se debe cerrar un archivo para que una aplicación pueda moverlo. Las [**funciones MoveFile**](/windows/desktop/api/WinBase/nf-winbase-movefile) [**y MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa) copian un archivo existente en una nueva ubicación y eliminan el original.

La [**función MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa) también permite a una aplicación especificar cómo mover el archivo. La función puede reemplazar un archivo existente, mover un archivo entre volúmenes y retrasar el traslado del archivo hasta que se reinicie el sistema operativo.

 

 



