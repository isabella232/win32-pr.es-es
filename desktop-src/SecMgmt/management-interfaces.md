---
description: Enumera las interfaces proporcionadas por el motor de datos adjuntos.
ms.assetid: 451587bd-a7ab-446b-b647-be98de251915
title: Interfaces de administración de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b3a205757a3bf324a5308a5f6fbc3d63374b4af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688249"
---
# <a name="security-management-interfaces"></a>Interfaces de administración de seguridad

Esta sección contiene páginas de referencia para los siguientes grupos de interfaces:

-   [Interfaces del motor de datos adjuntos](#attachment-engine-interfaces)

## <a name="attachment-engine-interfaces"></a>Interfaces del motor de datos adjuntos



| Interfaz                                                            | Descripción                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata)               | Recupera datos de configuración y análisis sobre un servicio de seguridad especificado de los complementos de configuración de seguridad. Los complementos de configuración de seguridad exponen esta interfaz, que las extensiones de complemento de datos adjuntos llaman a la información de configuración o análisis de consulta.                                                 |
| [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) | Recupera información de configuración o análisis modificada de un complemento de datos adjuntos. Los complementos de configuración de seguridad llaman a esta interfaz para recuperar cualquier información modificada de la extensión del complemento de datos adjuntos. A continuación, el complemento configuración de seguridad almacena estos datos de forma adecuada en la base de datos de seguridad. |



 

Para obtener más información sobre las interfaces COM que se deben implementar mediante extensiones de complemento, consulte la documentación de [Microsoft Management Console](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) .

 

 
