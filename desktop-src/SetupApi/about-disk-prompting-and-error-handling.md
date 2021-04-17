---
description: Las funciones de configuración pueden generar cuadros de diálogo para controlar situaciones de instalación comunes y recopilar información del usuario.
ms.assetid: 0bff17a6-590d-4410-9ed1-0a655d94caad
title: Acerca de la solicitud de disco y el control de errores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb6c171d1e479d5d16198ba6d632848ff152f4ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666435"
---
# <a name="about-disk-prompting-and-error-handling"></a>Acerca de la solicitud de disco y el control de errores

Aunque las funciones de instalación no proporcionan una interfaz de usuario, hay cuatro funciones de configuración que generan cuadros de diálogo para controlar situaciones de instalación comunes y recopilar información del usuario. Estos son: [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska), [**SetupCopyError**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora), [**SetupRenameError**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora)y [**SetupDeleteError**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora).

Las rutinas de devolución de llamada pueden llamar a estas funciones para crear cuadros de diálogo que ayuden a procesar las notificaciones enviadas por otras funciones de configuración, como [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) y [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea).

La función [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska) pide al usuario que inserte un medio extraíble, especifique una nueva ruta de acceso de origen o cancele la instalación. La aplicación puede ofrecer opciones adicionales al usuario, en función de las marcas especificadas cuando se llama a la función. Esto incluye omitir el archivo actual o buscar una nueva ruta de acceso de origen.

Las tres funciones, [**SetupCopyError**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora), [**SetupRenameError**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora)y [**SetupDeleteError**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora), crean cuadros de diálogo que interactúan con el usuario para recopilar información del usuario sobre cómo continuar cuando se produce un error.

La función [**SetupCopyError**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora) genera un cuadro de diálogo que pide al usuario Cómo recuperarse de un error de copia. El usuario puede especificar una nueva ruta de acceso de origen para la operación de copia o cancelar la instalación. En función de las marcas especificadas durante la llamada a **SetupCopyError**, es posible que el usuario también pueda buscar una nueva ruta de acceso de origen, ver los detalles del error u omitir el archivo actual.

Un cuadro de diálogo que pide al usuario Cómo procesar los errores que se producen durante una operación de cambio de nombre de archivo se puede generar mediante una llamada a [**SetupRenameError**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora). Con este cuadro de diálogo, el usuario tiene la oportunidad de reintentar la operación, omitir la operación de cambio de nombre actual o anular.

La función [**SetupDeleteError**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora) genera un cuadro de diálogo que puede recopilar información sobre cómo el usuario desea controlar un error que se produjo durante una operación de eliminación de archivos. Al usuario se le proporcionan las opciones para reintentar la operación, omitir la operación de eliminación actual o anular.

La rutina de devolución de llamada de cola predeterminada, [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka), usa las cuatro funciones anteriormente mencionadas para generar partes de la interfaz de usuario y controlar los errores y solicitar nuevos medios.

 

 



