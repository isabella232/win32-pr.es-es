---
description: La función phoneClose cierra el dispositivo de teléfono especificado.
ms.assetid: 7607d779-0715-48a3-a4f2-bcf07026d7c5
title: Cerrar el dispositivo Teléfono dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f137004e63b4b377e9ee88266d11f9c2b21d0af7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127374806"
---
# <a name="closing-the-phone-device"></a>Cerrar el dispositivo Teléfono dispositivo

La [**función phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) cierra el dispositivo de teléfono especificado. El dispositivo telefónico también se puede cerrar forzadamente después de que el usuario haya modificado la configuración de ese teléfono o su controlador. Si el usuario desea que los cambios de configuración sean efectivos inmediatamente (en lugar de después del siguiente reinicio del sistema) y afectan a la vista actual de la aplicación del dispositivo (por ejemplo, un cambio en las funcionalidades del dispositivo), un proveedor de servicios puede cerrar forzadamente el dispositivo telefónico.

Estos mensajes también se pueden enviar sin solicitados como resultado de que el dispositivo de teléfono se reclame de alguna otra manera. Por lo tanto, una aplicación debe estar preparada para controlar los mensajes [**PHONE \_ CLOSE no**](phone-close.md) solicitados. En el momento en que se cierra el dispositivo telefónico, se suprimen las respuestas asincrónicas pendientes relativas a ese dispositivo.

 

 



