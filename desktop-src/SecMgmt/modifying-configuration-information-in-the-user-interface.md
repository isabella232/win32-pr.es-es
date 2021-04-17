---
description: Una extensión de complemento de datos adjuntos debe permitir al usuario modificar la información de configuración sobre el servicio.
ms.assetid: fb36fcce-5a69-49cd-8cd3-b0b048f2f566
title: Modificación de la información de configuración en la interfaz de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c6158d76d0f5114bd2d7b483e0af3d00f8f2439
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668311"
---
# <a name="modifying-configuration-information-in-the-user-interface"></a>Modificación de la información de configuración en la interfaz de usuario

Una extensión de complemento de datos adjuntos debe permitir al usuario modificar la información de configuración sobre el servicio. La información modificada debe almacenarse mediante la extensión del complemento de datos adjuntos hasta que el complemento configuración de seguridad llame a los métodos de la interfaz [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) para recuperar la información.

Para evitar pérdidas de memoria, libere la memoria asignada por la extensión del complemento llamando a [**ISceSvcAttachmentPersistInfo:: FreeBuffer**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentpersistinfo-freebuffer).

 

 



