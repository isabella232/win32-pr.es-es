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
ms.openlocfilehash: 209259f46e25275094dcd1eb5eeddd4f336ee906
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372163"
---
# <a name="creating-temporary-streams"></a>Creación de una Secuencias

Los flujos temporales pueden ser beneficiosos de varias maneras. Puede usar una secuencia temporal como flujo de trabajo, por ejemplo, al cambiar el formato de secuencia. O bien, puede crear una secuencia temporal para contener partes de otras secuencias que se han copiado.

Puede crear una secuencia en memoria que no esté asociada a ningún archivo mediante la [**función AVIStreamCreate.**](/windows/desktop/api/Vfw/nf-vfw-avistreamcreate) Esta función devuelve la dirección de la interfaz a la nueva secuencia en una ubicación especificada y la usan internamente otras funciones que crean flujos temporales.

Puede crear una secuencia comprimida a partir de una secuencia sin comprimir mediante la [**función AVIMakeCompressedStream.**](/windows/desktop/api/Vfw/nf-vfw-avimakecompressedstream) Identifique la secuencia que se va a comprimir, el método de compresión y las opciones de compresión, y el controlador de la nueva secuencia.

Cuando termine de usar una secuencia creada con **AVIStreamCreate** o **AVIMakeCompressedStream,** cierre la secuencia mediante la [**función AVIStreamRelease.**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) **AVIStreamRelease libera** los recursos que usa la secuencia temporal.

 

 




