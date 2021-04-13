---
title: VCM (arquitectura)
description: VCM (arquitectura)
ms.assetid: cb0b036d-b8b1-4611-965f-08f932dbddb7
keywords:
- Vídeo para Windows (VFW), arquitectura VCM
- VFW (vídeo para Windows), VCM Architecture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89b672c86053086f63127aae586517fac4906326
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357367"
---
# <a name="vcm-architecture"></a>VCM (arquitectura)

VCM es un intermediario entre una aplicación y controladores de compresión y descompresión. Los controladores de compresión y descompresión comprimen y descomprimen tramas de datos individuales.

Cuando una aplicación realiza una llamada a VCM, VCM traduce la llamada en un mensaje. El mensaje se envía mediante la función [**ICSendMessage**](/windows/desktop/api/Vfw/nf-vfw-icsendmessage) al compresor o descompresor adecuado, que comprime o descomprime los datos. VCM recibe el valor devuelto del controlador de compresión o descompresión y, a continuación, devuelve el control a la aplicación.

Si se define una macro para un mensaje, la macro se expande a una llamada de función **ICSendMessage** que proporciona los parámetros adecuados para ese mensaje. Si se define una macro para un mensaje, la aplicación debe utilizarla en lugar del mensaje. En esta información general, estas macros siguen los mensajes entre paréntesis.

 

 




