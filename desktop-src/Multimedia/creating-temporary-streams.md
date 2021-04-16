---
title: Crear secuencias temporales
description: Crear secuencias temporales
ms.assetid: 8fe75ae1-0111-4b02-a00d-1ef2ca462452
keywords:
- AVIStreamCreate función)
- AVIStreamRelease función)
- AVIMakeCompressedStream función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209259f46e25275094dcd1eb5eeddd4f336ee906
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486759"
---
# <a name="creating-temporary-streams"></a>Crear secuencias temporales

Las secuencias temporales pueden ser beneficiosas de varias maneras. Puede usar una secuencia temporal como flujo de trabajo, por ejemplo, al cambiar el formato de la secuencia. O bien, puede crear una secuencia temporal para almacenar partes de otros flujos que se han copiado.

Puede crear una secuencia en memoria que no está asociada a ningún archivo mediante la función [**AVIStreamCreate**](/windows/desktop/api/Vfw/nf-vfw-avistreamcreate) . Esta función devuelve la dirección de la interfaz a la nueva secuencia en una ubicación especificada y la usan internamente otras funciones que crean secuencias temporales.

Puede crear un flujo comprimido a partir de una secuencia sin comprimir mediante la función [**AVIMakeCompressedStream**](/windows/desktop/api/Vfw/nf-vfw-avimakecompressedstream) . Identifique la secuencia que se va a comprimir, el método de compresión y las opciones de compresión, y el controlador del nuevo flujo.

Cuando termine de usar una secuencia creada con **AVIStreamCreate** o **AVIMakeCompressedStream**, cierre la secuencia mediante la función [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) . **AVIStreamRelease** libera los recursos utilizados por la secuencia temporal.

 

 




