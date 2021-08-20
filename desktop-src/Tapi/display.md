---
description: TAPI proporciona acceso a una pantalla de teléfonos.
ms.assetid: f6017ecc-b2a0-4a92-8c28-ce7411f8dd84
title: Mostrar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae87b68b9d7d810688b15de095d3cc6b9749df8d83f8adf41047c8c1560ac938
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117945618"
---
# <a name="display"></a>Mostrar

TAPI proporciona acceso a la pantalla de un teléfono. La presentación se modela como un área alfanumérica con filas y columnas. Las funcionalidades del dispositivo de un teléfono indican el tamaño de la presentación de un teléfono como el número de filas y el número de columnas. Ambos números son cero si el dispositivo telefónico no tiene una pantalla. Use [**phoneSetDisplay para**](/windows/desktop/api/Tapi/nf-tapi-phonesetdisplay) escribir información en la pantalla de un dispositivo de teléfono abierto y [**phoneGetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonegetdisplay) para recuperar el contenido actual de la pantalla de un teléfono.

Cuando se cambia la presentación de un dispositivo de teléfono, se envía un mensaje [**PHONE \_ STATE**](phone-state.md) a la función de aplicación para notificar a la aplicación el cambio de estado. Los parámetros de este mensaje proporcionan una indicación del cambio.

 

 



