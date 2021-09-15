---
description: Es posible que un solo teléfono pueda hacer anillos con distintos modos de anillo.
ms.assetid: c5ddcb3c-183c-4f97-9429-977d5cc32668
title: Anillo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f671aac6ead1938ff5b35ecb4996e4bc072a66d4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474687"
---
# <a name="ring"></a>Anillo

Es posible que un solo teléfono pueda hacer anillos con distintos modos de anillo. Dada la amplia variedad de modos de anillo disponibles, los modos de anillo se identifican por medio de su número de modo de anillo. Un número de modo de anillo oscila entre cero y el número de modos de anillo disponibles menos uno.

Las funciones que una aplicación usaría para controlar los modos de anillo de un dispositivo de teléfono son [**phoneSetRing**](/windows/desktop/api/Tapi/nf-tapi-phonesetring), que llama a un dispositivo de teléfono abierto según un modo de anillo determinado, y [**phoneGetRing**](/windows/desktop/api/Tapi/nf-tapi-phonegetring), que devuelve el modo de anillo actual de un dispositivo telefónico abierto.

Cuando se cambia el modo de anillo de un dispositivo de teléfono, se envía un mensaje [**PHONE \_ STATE**](phone-state.md) a la aplicación para notificar a la aplicación sobre el cambio de estado. Los parámetros de este mensaje proporcionan una indicación del cambio.

 

 



