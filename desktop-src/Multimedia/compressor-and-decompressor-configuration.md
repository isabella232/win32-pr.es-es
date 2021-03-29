---
title: Configuración del compresor y descompresor
description: Configuración del compresor y descompresor
ms.assetid: 677241d2-3ddd-423a-a1e7-b5fa3ce0a4eb
keywords:
- Administrador de compresión de vídeo (VCM), configurar compresores
- VCM (Administrador de compresión de vídeo), configurar compresores
- Mensaje ICM_CONFIGURE
- ICQueryConfigure (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38fbbeb852d09296e5be7929738c9d4d71f118e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994154"
---
# <a name="compressor-and-decompressor-configuration"></a>Configuración del compresor y descompresor

La aplicación puede configurar el compresor o descompresor automáticamente, o puede permitir que el usuario los configure. Si es práctico, permita que el usuario configure el compresor o descompresor; Esto le libera de tener en cuenta todas las opciones del compresor o descompresor.

El usuario puede configurar el compresor o descompresor mediante un cuadro de diálogo de configuración. Puede enviar el mensaje [**de \_ configuración de ICM**](icm-configure.md) a VCM (o utilizar la macro [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) ) para determinar si un compresor o descompresor puede mostrar un cuadro de diálogo de configuración. Si es así, envíe el \_ mensaje de configuración de ICM (o use la macro [**ICConfigure**](/windows/desktop/api/Vfw/nf-vfw-icconfigure) ) para mostrarlo.

La aplicación puede enviar los [**mensajes \_ ICM GETSTATE**](icm-getstate.md) y [**ICM \_ SETSTATE**](icm-setstate.md) (o usar las macros [**ICGetStateSize**](/windows/desktop/api/Vfw/nf-vfw-icgetstatesize), [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate)y [**ICSetState**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) ) para obtener y establecer el estado de un compresor o descompresor. Si la aplicación crea o modifica el estado, debe obtener el diseño de los datos del compresor o descompresor antes de restaurar su estado. O bien, si la aplicación obtiene el estado de un compresor o descompresor y lo usa para restaurar el estado en una sesión posterior, debe asegurarse de que solo se restaura la información de estado obtenida del compresor o descompresor que está usando actualmente.

 

 




