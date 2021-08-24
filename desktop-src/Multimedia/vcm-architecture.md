---
title: Arquitectura de VCM
description: Arquitectura de VCM
ms.assetid: cb0b036d-b8b1-4611-965f-08f932dbddb7
keywords:
- Vídeo de Windows (VFW),arquitectura de VCM
- VFW (vídeo para Windows),arquitectura de VCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7676fe7786b8674ddca957a75c33336294b65a9df18d53fe4b9c7f493092b66f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135603"
---
# <a name="vcm-architecture"></a>Arquitectura de VCM

VCM es un intermediario entre una aplicación y los controladores de compresión y descompresión. Los controladores de compresión y descompresión comprimen y descomprimen fotogramas individuales de datos.

Cuando una aplicación realiza una llamada a VCM, VCM traduce la llamada en un mensaje. El mensaje se envía mediante la función [**ICSendMessage**](/windows/desktop/api/Vfw/nf-vfw-icsendmessage) al descomprimidor o descomprimido adecuado, que comprime o descomprime los datos. VCM recibe el valor devuelto del controlador de compresión o descompresión y, a continuación, devuelve el control a la aplicación.

Si se define una macro para un mensaje, la macro se expande a una llamada de función **ICSendMessage** que proporciona los parámetros adecuados para ese mensaje. Si se define una macro para un mensaje, la aplicación debe usarla en lugar del mensaje. En esta información general, estas macros siguen los mensajes entre paréntesis.

 

 




