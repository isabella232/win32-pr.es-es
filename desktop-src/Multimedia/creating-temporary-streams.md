---
title: Creación de una Secuencias
description: Creación de una Secuencias
ms.assetid: 8fe75ae1-0111-4b02-a00d-1ef2ca462452
keywords:
- Función AVIStreamCreate
- Función AVIStreamRelease
- Función AVIMakeCompressedStream
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c33ce8d4ec6fd88a7283588d35955432cbe01a4855565928dca83d40afa8b64f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119785705"
---
# <a name="creating-temporary-streams"></a>Creación de una Secuencias

Las secuencias temporales pueden ser beneficiosas de varias maneras. Puede usar una secuencia temporal como flujo de trabajo, por ejemplo, al cambiar el formato de la secuencia. O bien, puede crear una secuencia temporal para contener partes de otras secuencias que se han copiado.

Puede crear una secuencia en memoria que no esté asociada a ningún archivo mediante la [**función AVIStreamCreate.**](/windows/desktop/api/Vfw/nf-vfw-avistreamcreate) Esta función devuelve la dirección de la interfaz a la nueva secuencia en una ubicación especificada y la usan internamente otras funciones que crean flujos temporales.

Puede crear una secuencia comprimida a partir de una secuencia sin comprimir mediante la [**función AVIMakeCompressedStream.**](/windows/desktop/api/Vfw/nf-vfw-avimakecompressedstream) Identifique la secuencia que se va a comprimir, el método de compresión y las opciones de compresión, y el controlador de la nueva secuencia.

Cuando termine de usar una secuencia creada con **AVIStreamCreate** o **AVIMakeCompressedStream,** cierre la secuencia mediante la [**función AVIStreamRelease.**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) **AVIStreamRelease libera** los recursos que usa la secuencia temporal.

 

 




