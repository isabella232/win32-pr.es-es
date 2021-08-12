---
description: Limitaciones de seguridad en el modo de grupo de trabajo
ms.assetid: 05c0aba7-b94b-49d4-a0fc-1ff0a23550b3
title: Limitaciones de seguridad en el modo de grupo de trabajo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1af613b8de16b99090bcdb02bde0015d01312df3d642c895d61ef59ff80873eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546288"
---
# <a name="security-limitations-in-workgroup-mode"></a>Limitaciones de seguridad en el modo de grupo de trabajo

La [configuración del grupo de trabajo de Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) no permite que el servicio de componentes en cola de COM+ admita la seguridad de la aplicación. Si ha instalado Message **Queuing** con la configuración del grupo de trabajo, debe deshabilitar la  seguridad en cada aplicación en cola a la  que se accede en esta configuración seleccionando No autenticar mensajes en la pestaña Cola del cuadro de diálogo Propiedades de la aplicación COM+, mediante la herramienta administrativa Servicios de componentes. [](specifying-the-authentication-protocol.md) Esto solo debe hacerse en una red de confianza y debe realizarse tanto en el cliente como en el servidor si la aplicación ya se ha exportado.

 

 



