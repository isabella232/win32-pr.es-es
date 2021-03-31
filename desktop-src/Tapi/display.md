---
description: TAPI proporciona acceso a una pantalla de teléfonos.
ms.assetid: f6017ecc-b2a0-4a92-8c28-ce7411f8dd84
title: Pantalla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5dd813297c1d4624bb37cea8d833f63bcebeeb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154341"
---
# <a name="display"></a>Pantalla

TAPI proporciona acceso a la pantalla de un teléfono. La presentación se modela como un área alfanumérica con filas y columnas. Las capacidades de dispositivo de un teléfono indican el tamaño de la pantalla de un teléfono como el número de filas y el número de columnas. Ambos números son cero si el dispositivo telefónico no tiene pantalla. Use [**phoneSetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonesetdisplay) para escribir información en la pantalla de un dispositivo telefónico abierto y [**phoneGetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonegetdisplay) para recuperar el contenido actual de la pantalla de un teléfono.

Cuando se cambia la presentación de un dispositivo telefónico, se envía un mensaje de [**\_ Estado de teléfono**](phone-state.md) a la función de aplicación para notificar a la aplicación sobre el cambio de estado. Los parámetros de este mensaje proporcionan una indicación del cambio.

 

 



