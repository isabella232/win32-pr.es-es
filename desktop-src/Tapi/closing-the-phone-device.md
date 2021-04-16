---
description: La función phoneClose cierra el dispositivo de teléfono especificado.
ms.assetid: 7607d779-0715-48a3-a4f2-bcf07026d7c5
title: Cierre del dispositivo teléfono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f137004e63b4b377e9ee88266d11f9c2b21d0af7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543003"
---
# <a name="closing-the-phone-device"></a>Cierre del dispositivo teléfono

La función [**phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) cierra el dispositivo de teléfono especificado. El dispositivo telefónico también se puede cerrar forzosamente después de que el usuario haya modificado la configuración de ese teléfono o su controlador. Si el usuario desea que los cambios de configuración surtan efecto inmediatamente (en lugar de después del siguiente reinicio del sistema) y afectan a la vista actual del dispositivo (por ejemplo, un cambio en las capacidades del dispositivo), un proveedor de servicios puede forzar el cierre del dispositivo telefónico.

Estos mensajes también se pueden enviar de forma no solicitada como resultado de la recuperación del dispositivo telefónico de otra manera. Por lo tanto, una aplicación debe estar preparada para controlar mensajes de [**\_ cierre de teléfono**](phone-close.md) no solicitados. En el momento en que se cierra el dispositivo telefónico, se suprime cualquier respuesta asincrónica pendiente que pertenezca a ese dispositivo.

 

 



