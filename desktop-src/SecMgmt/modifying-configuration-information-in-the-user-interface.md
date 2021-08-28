---
description: Una extensión de complemento de datos adjuntos debe permitir al usuario modificar la información de configuración sobre el servicio.
ms.assetid: fb36fcce-5a69-49cd-8cd3-b0b048f2f566
title: Modificar la información de configuración en el Interfaz de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 414e2ab1475ec1c3241d60b96d182a522c299a9f5cf6134f50339c2088c99d9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005123"
---
# <a name="modifying-configuration-information-in-the-user-interface"></a>Modificar la información de configuración en el Interfaz de usuario

Una extensión de complemento de datos adjuntos debe permitir al usuario modificar la información de configuración sobre el servicio. La extensión del complemento de datos adjuntos debe almacenar la información modificada hasta que el complemento Configuración de seguridad llame a métodos de la interfaz [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) para recuperar la información.

Para evitar pérdidas de memoria, libre memoria asignada por la extensión de complemento mediante una llamada a [**ISceSvcAttachmentPersistInfo::FreeBuffer**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentpersistinfo-freebuffer).

 

 



