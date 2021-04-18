---
description: Una extensión de complemento de datos adjuntos proporciona una interfaz que los usuarios pueden usar para cambiar la configuración específica del servicio.
ms.assetid: 6f2dc372-dee4-4793-b943-395c0587ed5e
title: Crear una extensión de complemento de datos adjuntos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 513c982acc7e5285f3b4d1510f18b7eb6c9fe1d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688028"
---
# <a name="creating-an-attachment-snap-in-extension"></a>Crear una extensión de complemento de datos adjuntos

Una extensión de complemento de datos adjuntos proporciona una interfaz que los usuarios pueden usar para cambiar la configuración específica del servicio. La extensión del complemento de datos adjuntos debe cumplir los requisitos de MMC para ser una extensión de complemento válida. Para obtener más información sobre estos requisitos, consulte la documentación de [Microsoft Management Console](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) .

Además de las interfaces requeridas por MMC, una extensión de complemento de datos adjuntos debe implementar la interfaz COM [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo). Los complementos de configuración de seguridad llaman a los métodos de esta interfaz para determinar si los datos de configuración han cambiado y, en caso afirmativo, actualizar la base de datos de seguridad. El complemento de datos adjuntos debe almacenar los cambios de configuración hasta que los complementos de configuración de seguridad recuperen los datos.

Una extensión de complemento de datos adjuntos debe proporcionar la funcionalidad siguiente:

-   [Mostrar información de configuración y análisis](displaying-configuration-and-analysis-information.md)
-   [Modificar la información de configuración en la interfaz de usuario](modifying-configuration-information-in-the-user-interface.md)
-   [Modificar la información de configuración en la base de datos de seguridad](modifying-configuration-information-in-the-database.md)

Para ayudar a la extensión del complemento a realizar estas tareas, los complementos de configuración de seguridad implementan una interfaz COM, [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata), que proporciona métodos a los que puede llamar la extensión del complemento para inicializarse y consultar información de la base de datos de seguridad.

Después de crear la extensión del complemento de datos adjuntos, debe registrarla con los complementos de configuración de seguridad, tal y como se describe en [registrar una extensión de complemento de datos adjuntos](registering-an-attachment-snap-in-extension.md).

 

 
