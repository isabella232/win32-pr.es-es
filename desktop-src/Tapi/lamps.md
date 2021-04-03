---
description: Las luces de un dispositivo telefónico se pueden iluminar en distintos modos de iluminación.
ms.assetid: d8e8ef57-9faa-4122-b99a-3956362cd9d8
title: Lámparas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e01005c282b7a86b4b8c8ee27348ba4cf8d43db9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083180"
---
# <a name="lamps"></a>Lámparas

Las luces de un dispositivo telefónico se pueden iluminar en distintos modos de iluminación. A diferencia de los modelos de timbre, los modos de lámpara son más uniformes en los juegos de teléfono de distintos proveedores. La API define un conjunto común de modos de lámpara. Una lámpara identificada por su identificador de botón de lámpara puede estar iluminada en un modo de lámpara determinado. También se puede consultar una lámpara para el modo de lámpara actual.

Las funciones TAPI que se usan para las lámparas son [**phoneSetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonesetlamp), que ilumina una lámpara en un dispositivo de teléfono abierto especificado en un modo de iluminación de lámpara determinado y [**phoneGetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonegetlamp), que devuelve el modo de lámpara actual de la lámpara especificada.

Cuando se cambia una lámpara de un dispositivo telefónico, se envía un mensaje de [**\_ Estado de teléfono**](phone-state.md) a la aplicación para notificar a la aplicación sobre el cambio de estado. Los parámetros de este mensaje proporcionan una indicación del cambio.

 

 



