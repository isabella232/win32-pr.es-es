---
description: Las funciones de instalación pueden generar cuadros de diálogo para controlar situaciones de instalación comunes y recopilar información del usuario.
ms.assetid: 0bff17a6-590d-4410-9ed1-0a655d94caad
title: Acerca de la solicitud de disco y el control de errores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f9aa7a43cc0efd81f066872a55cde20b66bb13d1c117153606f4b9fe2dd2e58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887968"
---
# <a name="about-disk-prompting-and-error-handling"></a>Acerca de la solicitud de disco y el control de errores

Aunque las funciones de instalación no proporcionan una interfaz de usuario, hay cuatro funciones de configuración que generan cuadros de diálogo para controlar situaciones de instalación comunes y recopilar información del usuario. Estos son: [**SetupPromptForDisk,**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska) [**SetupCopyError,**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora) [**SetupRenameError**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora)y [**SetupDeleteError.**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora)

Las rutinas de devolución de llamada pueden llamar a estas funciones para crear cuadros de diálogo que le ayudarán a procesar las notificaciones enviadas por otras funciones de instalación, como [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) [**y SetupInstallFile.**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)

La [**función SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska) solicita al usuario que inserte medios extraíbles, especifique una nueva ruta de acceso de origen o cancele la instalación. La aplicación puede ofrecer opciones adicionales al usuario, en función de las marcas especificadas cuando se llama a la función. Entre ellas se incluyen la omisión del archivo actual o la exploración de una nueva ruta de acceso de origen.

Las tres funciones, [**SetupCopyError**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora), [**SetupRenameError**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora)y [**SetupDeleteError,**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora)crean cuadros de diálogo que interactúan con el usuario para recopilar información del usuario sobre cómo continuar cuando se ha producido un error.

La [**función SetupCopyError**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora) genera un cuadro de diálogo que pregunta al usuario cómo recuperarse de un error de copia. El usuario puede especificar una nueva ruta de acceso de origen para la operación de copia o cancelar la instalación. Según las marcas especificadas durante la llamada a **SetupCopyError,** el usuario también puede buscar una nueva ruta de acceso de origen, ver los detalles del error o omitir el archivo actual.

Un cuadro de diálogo que pregunta al usuario cómo procesar los errores que se producen durante una operación de cambio de nombre de archivo se puede generar mediante una llamada a [**SetupRenameError**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora). Con este cuadro de diálogo, el usuario tiene la oportunidad de reintentar la operación, omitir la operación de cambio de nombre actual o anularla.

La [**función SetupDeleteError**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora) genera un cuadro de diálogo que puede recopilar entradas sobre cómo el usuario desea controlar un error que se produjo durante una operación de eliminación de archivos. El usuario tiene las opciones para reintentar la operación, omitir la operación de eliminación actual o anularla.

La rutina de devolución de llamada de cola predeterminada, [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka), usa las cuatro funciones mencionadas anteriormente para generar partes de su interfaz de usuario y para controlar los errores y solicitar nuevos medios.

 

 



