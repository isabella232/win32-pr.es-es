---
title: Configuración de descompresión y descompresión
description: Configuración de descompresión y descompresión
ms.assetid: 677241d2-3ddd-423a-a1e7-b5fa3ce0a4eb
keywords:
- Administrador de compresión de vídeo (VCM), configuración de ingerentes
- VCM (administrador de compresión de vídeo), configuración de ingerentes
- ICM_CONFIGURE mensaje
- ICQueryConfigure macro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8905ea35d65fc3eda3ddee130039503d8e26555665aae9efa517cb399349475
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144987"
---
# <a name="compressor-and-decompressor-configuration"></a>Configuración de descompresión y descompresión

La aplicación puede configurar el descomprimidor o el descomprimido automáticamente, o bien puede permitir que el usuario los configure. Si es práctico, permita al usuario configurar el descomprimidor o el descomprimidor. esto le libera de considerar todas las opciones para el descomprimidor o el descomprimidor.

El usuario puede configurar el descomprimidor o el descomprimido mediante un cuadro de diálogo de configuración. Puede enviar el mensaje [**\_ ICM CONFIGURE**](icm-configure.md) a VCM (o usar la macro [**ICQueryConfigure)**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) para determinar si un descomprimidor o un descomprimidor pueden mostrar un cuadro de diálogo de configuración. Si es así, envíe el ICM \_ CONFIGURE (o use la macro [**ICConfigure)**](/windows/desktop/api/Vfw/nf-vfw-icconfigure) para mostrarlo.

La aplicación puede enviar los mensajes [**\_ ICM GETSTATE**](icm-getstate.md) y [**ICM \_ SETSTATE**](icm-setstate.md) (o usar las macros [**ICGetStateSize,**](/windows/desktop/api/Vfw/nf-vfw-icgetstatesize) [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate)e [**ICSetState)**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) para obtener y establecer el estado de un descomprimidor o un descompresión. Si la aplicación crea o modifica el estado, debe obtener el diseño de los datos de descompresión o descompresión antes de restaurar su estado. Como alternativa, si la aplicación obtiene el estado de un descomprimido o un descomprimidor y lo usa para restaurar el estado en una sesión posterior, debe asegurarse de que solo restaura la información de estado obtenida del descomprimidor o el descompresión que está usando actualmente.

 

 




