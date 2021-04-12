---
description: Una aplicación puede crear y eliminar directorios mediante programación.
ms.assetid: 52d1d8a8-e5a7-44f5-9bf2-2a496ef79d32
title: Crear y eliminar directorios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 140547594271e13bc78bfa78336f167f228879a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155300"
---
# <a name="creating-and-deleting-directories"></a>Crear y eliminar directorios

Una aplicación puede crear y eliminar directorios mediante programación.

Para crear un nuevo directorio, use la función [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya), [**CreateDirectoryEx**](/windows/desktop/api/WinBase/nf-winbase-createdirectoryexa)o [**CreateDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-createdirectorytransacteda) . A un directorio se le asigna el nombre especificado cuando se crea. Las convenciones para asignar nombres a un directorio siguen las convenciones de nomenclatura de un archivo. Para obtener una descripción de estas convenciones, vea [asignar un nombre a un archivo](naming-a-file.md).

Para eliminar un directorio existente, use la función [**RemoveDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-removedirectorya) o [**RemoveDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda) . Antes de quitar un directorio, debe asegurarse de que el directorio está vacío y de que tiene el privilegio de eliminación de acceso para el directorio. Para hacer esto último, llame a la función [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) .

 

 
