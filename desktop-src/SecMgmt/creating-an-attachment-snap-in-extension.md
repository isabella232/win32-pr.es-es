---
description: Una extensión de complemento de datos adjuntos proporciona una interfaz que los usuarios pueden usar para cambiar las opciones de configuración específicas del servicio.
ms.assetid: 6f2dc372-dee4-4793-b943-395c0587ed5e
title: Crear una extensión de complemento de datos adjuntos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1a4cd4ccecf7fba6e33062fd2bb4df810316f2d66d42165ca207d855a14f961
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118894835"
---
# <a name="creating-an-attachment-snap-in-extension"></a>Crear una extensión de complemento de datos adjuntos

Una extensión de complemento de datos adjuntos proporciona una interfaz que los usuarios pueden usar para cambiar las opciones de configuración específicas del servicio. La extensión de complemento de datos adjuntos debe cumplir los requisitos de MMC para ser una extensión de complemento válida. Para obtener más información sobre esos requisitos, consulte la [documentación Microsoft Management Console](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) datos.

Además de las interfaces requeridas por MMC, una extensión de complemento de datos adjuntos debe implementar la interfaz COM [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo). Los complementos de configuración de seguridad llaman a métodos de esta interfaz para determinar si los datos de configuración han cambiado y, si es así, para actualizar la base de datos de seguridad. El complemento de datos adjuntos debe almacenar los cambios de configuración hasta que los complementos de configuración de seguridad recuperen esos datos.

Una extensión de complemento de datos adjuntos debe proporcionar la siguiente funcionalidad:

-   [Mostrar información de configuración y análisis](displaying-configuration-and-analysis-information.md)
-   [Modificar la información de configuración en el Interfaz de usuario](modifying-configuration-information-in-the-user-interface.md)
-   [Modificar la información de configuración en la base de datos de seguridad](modifying-configuration-information-in-the-database.md)

Para ayudar a la extensión de complemento a realizar estas tareas, los complementos de configuración de seguridad implementan una interfaz COM, [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata), que proporciona métodos a los que puede llamar la extensión de complemento para inicializarse y consultar información de la base de datos de seguridad.

Después de crear la extensión de complemento de datos adjuntos, debe registrarla con los complementos de configuración de seguridad, tal y como se describe en Registro de una extensión de complemento [de datos adjuntos](registering-an-attachment-snap-in-extension.md).

 

 
