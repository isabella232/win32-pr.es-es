---
title: Arquitectura de VCM
description: Arquitectura de VCM
ms.assetid: cb0b036d-b8b1-4611-965f-08f932dbddb7
keywords:
- Vídeo para Windows (VFW), arquitectura de VCM
- VFW (vídeo para Windows),arquitectura de VCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89b672c86053086f63127aae586517fac4906326
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245673"
---
# <a name="vcm-architecture"></a>Arquitectura de VCM

VCM es un intermediario entre una aplicación y los controladores de compresión y descompresión. Los controladores de compresión y descompresión comprimen y descomprimen fotogramas individuales de datos.

Cuando una aplicación realiza una llamada a VCM, VCM traduce la llamada en un mensaje. El mensaje se envía mediante la función [**ICSendMessage**](/windows/desktop/api/Vfw/nf-vfw-icsendmessage) al descomprimidor o descompresión adecuado, que comprime o descomprime los datos. VCM recibe el valor devuelto del controlador de compresión o descompresión y, a continuación, devuelve el control a la aplicación.

Si se define una macro para un mensaje, la macro se expande a una llamada de función **ICSendMessage** que proporciona los parámetros adecuados para ese mensaje. Si se define una macro para un mensaje, la aplicación debe usarla en lugar del mensaje. En esta introducción, estas macros siguen los mensajes entre paréntesis.

 

 




