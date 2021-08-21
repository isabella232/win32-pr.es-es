---
description: Funciones usadas en la administración de directorios.
ms.assetid: 5517b0e7-2264-4173-8e10-ff7626458bfa
title: Funciones de administración de directorios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2042b7fc4cc7f6af64c3c0eba0938b3f5d78e7b551981e1cc820b38000b1d745
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150443"
---
# <a name="directory-management-functions"></a>Funciones de administración de directorios

Las siguientes funciones se usan en la administración de directorios.

## <a name="in-this-section"></a>En esta sección



| Función                                                                      | Descripción                                                                                                                                                               |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya)<br/>                         | Crea un directorio nuevo.<br/>                                                                                                                                       |
| [**CreateDirectoryEx**](/windows/desktop/api/WinBase/nf-winbase-createdirectoryexa)<br/>                     | Crea un nuevo directorio con los atributos de un directorio de plantilla especificado.<br/>                                                                                 |
| [**CreateDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-createdirectorytransacteda)<br/>     | Crea un nuevo directorio como una operación de transacción, con los atributos de un directorio de plantilla especificado.<br/>                                                      |
| [**FindCloseChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findclosechangenotification)<br/> | Detiene la supervisión del identificador de notificación de cambios.<br/>                                                                                                                   |
| [**FindFirstChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa)<br/> | Crea un identificador de notificación de cambios y configura las condiciones iniciales del filtro de notificación de cambios.<br/>                                                                |
| [**FindNextChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findnextchangenotification)<br/>   | Solicita que el sistema operativo señale una notificación de cambio la próxima vez que detecte un cambio adecuado.<br/>                                         |
| [**GetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-getcurrentdirectory)<br/>                 | Recupera el directorio actual del proceso actual.<br/>                                                                                                       |
| [**ReadDirectoryChangesExW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesexw)<br/>         | Recupera información que describe los cambios dentro del directorio especificado, que puede incluir información extendida si se especifica ese tipo de información.<br/> |
| [**ReadDirectoryChangesW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)<br/>             | Recupera información que describe los cambios en el directorio especificado.<br/>                                                                               |
| [**RemoveDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-removedirectorya)<br/>                         | Elimina un directorio vacío existente.<br/>                                                                                                                           |
| [**RemoveDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda)<br/>     | Elimina un directorio vacío existente como una operación de transacción.<br/>                                                                                                 |
| [**SetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory)<br/>                 | Cambia el directorio actual del proceso actual.<br/>                                                                                                         |



 

 

 




