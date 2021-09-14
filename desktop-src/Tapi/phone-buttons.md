---
description: TAPI modela los botones y las bombillas de los teléfonos como pares de botones y bombillas.
ms.assetid: e4c50bd6-a256-407f-af3b-b24383a30ea0
title: Teléfono Botones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee3e65c34096c0cf043b85d80c9c726c6bef982d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071104"
---
# <a name="phone-buttons"></a>Teléfono Botones

TAPI modela los botones y las luces de un teléfono como pares de botones y bombillas. Un botón sin ninguna bombilla junto a él o una bombilla sin botón se especifica mediante un indicador "ficticio" para la bombilla o el botón que falta. Un botón con varias bombillas se modela mediante varios pares de botones y bombillas.

La información asociada a un botón de teléfono se puede establecer y recuperar. Cuando se presiona un botón, se envía un mensaje [**\_ PHONE BUTTON**](phone-button.md) a la función de aplicación. Los parámetros de este mensaje son un identificador para el dispositivo de teléfono y el identificador de la bombilla de botón del botón que se presionó. A los botones del teclado "0" a "9", "" y "" se les asignan los identificadores fijos de bombilla de botón del 0 al \* \# 11.

Las funciones asociadas a los botones son [**phoneSetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonesetbuttoninfo), que establece la información asociada a un botón en un dispositivo de teléfono, y [**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo), que devuelve información asociada a un botón en un dispositivo de teléfono. El mensaje \_ PHONE BUTTON se envía a una aplicación cuando se presiona un botón en el teléfono.

La información asociada a un botón no tiene ningún significado semántico en lo que respecta a TAPI. Es útil para aplicaciones específicas del dispositivo que comprenden el significado de esta información para un dispositivo telefónico determinado o para mostrarla al usuario, como la ayuda en línea.

 

 



