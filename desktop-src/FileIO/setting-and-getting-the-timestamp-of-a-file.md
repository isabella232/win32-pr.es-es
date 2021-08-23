---
description: Las aplicaciones pueden recuperar y establecer la fecha y hora en que se crea un archivo, se modifica por última vez o se accede por última vez mediante las funciones GetFileTime y SetFileTime.
ms.assetid: f8930be6-7c2a-4e50-a7a1-d25f6e2a3951
title: Establecer y obtener la marca de tiempo de un archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67e98bd87ae8224ecbebc46e5f9d0ed71ad3522097fb865afc0d16e53a828812
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015133"
---
# <a name="setting-and-getting-the-timestamp-of-a-file"></a>Establecer y obtener la marca de tiempo de un archivo

Las aplicaciones pueden recuperar y establecer la fecha y hora en que se crea un archivo, se modifica por última vez o se accede por última vez mediante las funciones [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) y [**SetFileTime.**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime) Para obtener más información, vea [File Times](/windows/desktop/SysInfo/file-times).

> [!Note]  
> No todos los sistemas de archivos pueden registrar los tiempos de creación y último acceso, y no todos los sistemas de archivos los registran de la misma manera. Por ejemplo, en el sistema de archivos FAT, la hora de creación tiene una resolución de 10 milisegundos, el tiempo de escritura tiene una resolución de 2 segundos y el tiempo de acceso tiene una resolución de 1 día (realmente, la fecha de acceso). El sistema de archivos NTFS retrasa la actualización a la hora de último acceso de un archivo hasta una hora después del último acceso.

 

 

 
