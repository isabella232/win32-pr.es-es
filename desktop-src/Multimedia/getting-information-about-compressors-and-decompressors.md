---
title: Obtener información acerca de los compresores y descompresores
description: Obtener información acerca de los compresores y descompresores
ms.assetid: bb9773dc-a706-40e6-8703-1cd47101992c
keywords:
- Administrador de compresión de vídeo (VCM), obtener información sobre los compresores
- VCM (Administrador de compresión de vídeo), obtener información sobre los compresores
- ICGetInfo función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c619d13559d99b570af200298f29fcd8238c7d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994273"
---
# <a name="getting-information-about-compressors-and-decompressors"></a>Obtener información acerca de los compresores y descompresores

Para obtener información general sobre un compresor o descompresor, la aplicación puede usar la función [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) . Esta función rellena una estructura [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) con información sobre el compresor o descompresor. La aplicación debe asignar la memoria de la estructura **ICINFO** y pasar un puntero a ella en **ICGetInfo**. A menos que la aplicación busque un compresor o descompresor determinado, las marcas de la estructura **ICINFO** proporcionan la información más útil sobre las capacidades de un compresor o descompresor.

Para obtener la velocidad de fotogramas clave y el valor de calidad predeterminados de un compresor o descompresor, la aplicación puede enviar los mensajes [**ICM \_ GETDEFAULTKEYFRAMERATE**](icm-getdefaultkeyframerate.md) y [**ICM \_ GETDEFAULTQUALITY**](icm-getdefaultquality.md) (o usar las macros [**ICGetDefaultKeyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) y [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) ).

Para determinar el mejor formato de presentación de un compresor o descompresor, la aplicación puede usar la función [**ICGetDisplayFormat**](/windows/desktop/api/Vfw/nf-vfw-icgetdisplayformat) .

Para determinar si un compresor o descompresor puede mostrar un cuadro de diálogo acerca de, envíe el mensaje [**ICM \_ About**](icm-about.md) (o use la macro [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) ). También puede mostrar el cuadro de diálogo acerca de de un compresor o descompresor enviando el \_ mensaje ICM about y cambiando el valor del parámetro *wParam* (o mediante la macro [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) ).

 

 




