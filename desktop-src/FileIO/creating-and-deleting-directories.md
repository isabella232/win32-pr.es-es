---
description: Una aplicación puede crear y eliminar directorios mediante programación.
ms.assetid: 52d1d8a8-e5a7-44f5-9bf2-2a496ef79d32
title: Creación y eliminación de directorios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 862907ad3adef3a4502961820a6f5ffcb1cd932541b03226854d81372ca6e13f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119533745"
---
# <a name="creating-and-deleting-directories"></a>Creación y eliminación de directorios

Una aplicación puede crear y eliminar directorios mediante programación.

Para crear un directorio, use la [**función CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya), [**CreateDirectoryEx**](/windows/desktop/api/WinBase/nf-winbase-createdirectoryexa)o [**CreateDirectoryTransacted.**](/windows/desktop/api/WinBase/nf-winbase-createdirectorytransacteda) A un directorio se le da el nombre especificado cuando se crea. Las convenciones para asignar un nombre a un directorio siguen las convenciones para asignar un nombre a un archivo. Para obtener una descripción de estas convenciones, vea [Asignación de nombres a un archivo.](naming-a-file.md)

Para eliminar un directorio existente, use la [**función RemoveDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-removedirectorya) [**o RemoveDirectoryTransacted.**](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda) Antes de quitar un directorio, debe asegurarse de que el directorio está vacío y de que tiene el privilegio de acceso de eliminación para el directorio. Para ello, llame a la [**función GetSecurityInfo.**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo)

 

 
