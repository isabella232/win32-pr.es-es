---
description: Una extensión de complemento de datos adjuntos debe permitir al usuario modificar la información de configuración sobre el servicio.
ms.assetid: fb36fcce-5a69-49cd-8cd3-b0b048f2f566
title: Modificar la información de configuración en el Interfaz de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c6158d76d0f5114bd2d7b483e0af3d00f8f2439
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073599"
---
# <a name="modifying-configuration-information-in-the-user-interface"></a>Modificar la información de configuración en el Interfaz de usuario

Una extensión de complemento de datos adjuntos debe permitir al usuario modificar la información de configuración sobre el servicio. La extensión del complemento de datos adjuntos debe almacenar la información modificada hasta que el complemento Configuración de seguridad llame a métodos de la interfaz [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) para recuperar la información.

Para evitar pérdidas de memoria, la extensión de complemento asigna memoria libre mediante una llamada a [**ISceSvcAttachmentPersistInfo::FreeBuffer**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentpersistinfo-freebuffer).

 

 



