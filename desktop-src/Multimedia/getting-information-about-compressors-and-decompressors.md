---
title: Obtener información sobre los descomprimores y los descomprimores
description: Obtener información sobre los descomprimores y los descomprimores
ms.assetid: bb9773dc-a706-40e6-8703-1cd47101992c
keywords:
- Administrador de compresión de vídeo (VCM), obtención de información sobre los ingerentes
- VCM (administrador de compresión de vídeo), obtención de información sobre los resaltes
- Función ICGetInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 404b6acacd97b514edcf0328a8127f97152554015694eba3f8e5bf3b76214de3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678624"
---
# <a name="getting-information-about-compressors-and-decompressors"></a>Obtener información sobre los descomprimores y los descomprimores

Para obtener información general sobre un descompresión o un descomprimidor, la aplicación puede usar la [**función ICGetInfo.**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) Esta función rellena una estructura [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) con información sobre el descomprimidor o el descomprimidor. La aplicación debe asignar la memoria para la **estructura ICINFO** y pasar un puntero a ella en **ICGetInfo**. A menos que la aplicación busque un descompresión o un descompresión determinados, las marcas de la estructura **ICINFO** proporcionan la información más útil sobre las funcionalidades de un descomprimidor o descompresión.

Para obtener la velocidad de fotogramas clave predeterminada y el valor de calidad predeterminado de un descomprimidor o descompresión, la aplicación puede enviar los mensajes [**ICM \_ GETDEFAULTKEYFRAMERATE**](icm-getdefaultkeyframerate.md) y [**ICM \_ GETDEFAULTQUALITY**](icm-getdefaultquality.md) (o usar las macros [**ICGetDefaultKeyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) e [**ICGetDefaultQuality).**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality)

Para determinar el mejor formato de presentación de un descomprimidor o descompresión, la aplicación puede usar la [**función ICGetDisplayFormat.**](/windows/desktop/api/Vfw/nf-vfw-icgetdisplayformat)

Para determinar si un descomprimidor o un descomprimidor pueden mostrar un cuadro de diálogo Acerca de , envíe el mensaje ICM [**\_ ABOUT**](icm-about.md) (o use la macro [**ICQueryAbout).**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) También puede mostrar el cuadro de diálogo Acerca de de un descomprimidor o descomprimido enviando el mensaje ABOUT de ICM y cambiando el valor del parámetro \_ *wParam* (o mediante la macro [**ICAbout).**](/windows/desktop/api/Vfw/nf-vfw-icabout)

 

 




