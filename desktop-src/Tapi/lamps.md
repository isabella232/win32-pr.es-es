---
description: Las bombillas de un dispositivo de teléfono se pueden encender en una variedad de modos de iluminación diferentes.
ms.assetid: d8e8ef57-9faa-4122-b99a-3956362cd9d8
title: Lámparas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 150e499dbd66ca772d35855c4cdb086bbb1ecc12617f55bcd33dccf8435e8771
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117762290"
---
# <a name="lamps"></a>Lámparas

Las bombillas de un dispositivo de teléfono se pueden encender en una variedad de modos de iluminación diferentes. A diferencia de los patrones de anillo, los modos de bombilla son más uniformes entre los conjuntos de teléfonos de distintos proveedores. La API define un conjunto común de modos de bombilla. Una bombilla identificada por su identificador de botón de bombilla se puede encender en un modo de bombilla determinado. También se puede consultar una bombilla para su modo de bombilla actual.

Las funciones TAPI que se usan para las bombillas son [**phoneSetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonesetlamp), que enciende una bombilla en un dispositivo de teléfono abierto especificado en un modo de iluminación de bombilla determinado, y [**phoneGetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonegetlamp), que devuelve el modo de la bombilla actual de la bombilla especificada.

Cuando se cambia una bombilla de un dispositivo de teléfono, se envía un mensaje [**PHONE \_ STATE**](phone-state.md) a la aplicación para notificar a la aplicación sobre el cambio de estado. Los parámetros de este mensaje proporcionan una indicación del cambio.

 

 



