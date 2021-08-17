---
description: Algunos conjuntos de teléfonos admiten la noción de descargar o cargar datos en el dispositivo telefónico, lo que permite programar el conjunto de teléfonos de varias maneras.
ms.assetid: 5734107d-8104-4d8a-b3f7-3cc2a48f71ca
title: Áreas de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed05d6233a8c8ed31a2d00d28970a517ef181f00689c7da34673d3044fffb4dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117946148"
---
# <a name="data-areas"></a>Áreas de datos

Algunos conjuntos de teléfonos admiten la noción de descargar o cargar datos en el dispositivo telefónico, lo que permite programar el conjunto de teléfonos de varias maneras. TAPI modela estos conjuntos de teléfonos como que tienen una o varias áreas de descarga o carga. Cada área se identifica mediante un número que oscila entre cero y el número de áreas de datos disponibles en el teléfono menos una. Los tamaños de cada área pueden variar. El formato de los propios datos es específico del dispositivo.

La función TAPI [**phoneSetData**](/windows/desktop/api/Tapi/nf-tapi-phonesetdata) descarga un búfer de datos en un área de datos determinada del dispositivo de teléfono y la función [**phoneGetData**](/windows/desktop/api/Tapi/nf-tapi-phonegetdata) carga el contenido de un área de datos determinada del dispositivo de teléfono en un búfer.

Cuando se cambia un área de datos de un dispositivo de teléfono, se envía un mensaje [**PHONE \_ STATE**](phone-state.md) a la aplicación para notificar a la aplicación sobre el cambio de estado. Los parámetros de este mensaje proporcionan una indicación del cambio.

 

 



