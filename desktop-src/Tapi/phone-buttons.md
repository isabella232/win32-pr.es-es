---
description: TAPI modela los botones y las bombillas de los teléfonos como pares de botones y bombillas.
ms.assetid: e4c50bd6-a256-407f-af3b-b24383a30ea0
title: Teléfono Botones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e72288133615b19e622434b8727608aaec9a9136dd58eaa03e339708c42a13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774165"
---
# <a name="phone-buttons"></a>Teléfono Botones

TAPI modela los botones y las bombillas de un teléfono como pares de botones y bombillas. Un botón sin ninguna bombilla junto a él o una bombilla sin botón se especifica mediante un indicador "ficticio" para la bombilla o el botón que falta. Un botón con varias bombillas se modela mediante el uso de varios pares de botones y bombillas.

La información asociada a un botón de teléfono se puede establecer y recuperar. Cuando se presiona un botón, se envía un [**mensaje \_ PHONE BUTTON**](phone-button.md) a la función de aplicación. Los parámetros de este mensaje son un identificador para el dispositivo telefónico y el identificador de la bombilla de botón del botón que se presionó. A los botones del teclado "0" a "9", "" y "" se les asignan los identificadores fijos de la bombilla de botón del 0 al \* \# 11.

Las funciones asociadas a los botones son [**phoneSetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonesetbuttoninfo), que establece la información asociada a un botón en un dispositivo de teléfono, y [**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo), que devuelve información asociada a un botón en un dispositivo telefónico. El mensaje PHONE BUTTON se envía a una aplicación cuando se presiona un \_ botón en el teléfono.

La información asociada a un botón no tiene ningún significado semántico en lo que respecta a TAPI. Es útil para aplicaciones específicas del dispositivo que comprenden el significado de esta información para un dispositivo telefónico determinado o para mostrarla al usuario, como la ayuda en línea.

 

 



