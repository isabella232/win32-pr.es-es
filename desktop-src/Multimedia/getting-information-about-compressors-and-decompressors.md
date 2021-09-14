---
title: Obtener información sobre los descompresores y los descomprimir
description: Obtener información sobre los descompresores y los descomprimir
ms.assetid: bb9773dc-a706-40e6-8703-1cd47101992c
keywords:
- Administrador de compresión de vídeo (VCM), obtención de información sobre los resaltes
- VCM (administrador de compresión de vídeo), obtención de información sobre los resaltes
- Función ICGetInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c619d13559d99b570af200298f29fcd8238c7d4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069534"
---
# <a name="getting-information-about-compressors-and-decompressors"></a>Obtener información sobre los descompresores y los descomprimir

Para obtener información general sobre un descomprimidor o descompresión, la aplicación puede usar la [**función ICGetInfo.**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) Esta función rellena una estructura [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) con información sobre el descomprimidor o el descompresión. La aplicación debe asignar la memoria para la **estructura ICINFO** y pasar un puntero a ella **en ICGetInfo**. A menos que la aplicación busque un descompresión o un descompresión determinados, las marcas de la estructura **ICINFO** proporcionan la información más útil sobre las funcionalidades de un descomprimidor o descompresión.

Para obtener la velocidad de fotogramas clave predeterminada y el valor de calidad predeterminado de un descomprimidor o descompresión, la aplicación puede enviar los mensajes [**ICM \_ GETDEFAULTKEYFRAMERATE**](icm-getdefaultkeyframerate.md) y [**ICM \_ GETDEFAULTQUALITY**](icm-getdefaultquality.md) (o usar las macros [**ICGetDefaultKeyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) e [**ICGetDefaultQuality).**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality)

Para determinar el mejor formato de presentación de un descomprimidor o descompresión, la aplicación puede usar la [**función ICGetDisplayFormat.**](/windows/desktop/api/Vfw/nf-vfw-icgetdisplayformat)

Para determinar si un descomprimidor o descomprimido puede mostrar un cuadro de diálogo Acerca de, envíe el mensaje ICM [**\_ ACERCA**](icm-about.md) de (o use la macro [**ICQueryAbout).**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) También puede mostrar el cuadro de diálogo Acerca de de un descomprimidor o descomprimidor enviando el mensaje ABOUT de ICM y cambiando el valor del parámetro \_ *wParam* (o mediante la macro [**ICAbout).**](/windows/desktop/api/Vfw/nf-vfw-icabout)

 

 




