---
description: TAPI modela los botones y las lámparas de un teléfono como pares de luces de botón.
ms.assetid: e4c50bd6-a256-407f-af3b-b24383a30ea0
title: Botones de teléfono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee3e65c34096c0cf043b85d80c9c726c6bef982d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812482"
---
# <a name="phone-buttons"></a>Botones de teléfono

TAPI modela los botones y las lámparas de un teléfono como pares de luces de botón. Un botón sin luz junto a él o una lámpara sin botón se especifica mediante un indicador "ficticio" para el botón o lámpara que falta. Un botón con varias lámparas se modela con varios pares de luz de botón.

La información asociada a un botón de teléfono se puede establecer y recuperar. Cuando se presiona un botón, se envía un mensaje de [**\_ botón de teléfono**](phone-button.md) a la función de aplicación. Los parámetros de este mensaje son un identificador del dispositivo telefónico y el identificador de la lámpara de botón del botón que se presionó. A los botones del teclado numérico ' 0 ' a ' 9 ', ' \* ' y ' \# ' se les asignan los identificadores de luz de botón fijos del 0 al 11.

Las funciones asociadas a los botones son [**phoneSetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonesetbuttoninfo), que establece la información asociada a un botón en un dispositivo telefónico y [**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo), que devuelve información asociada a un botón en un dispositivo telefónico. El mensaje del botón del teléfono \_ se envía a una aplicación cuando se presiona un botón del teléfono.

La información asociada a un botón no tiene ningún significado semántico en lo que se refiere a TAPI. Resulta útil para aplicaciones específicas del dispositivo que entienden el significado de esta información para un dispositivo telefónico determinado, o para que se muestre al usuario, como la ayuda en línea.

 

 



