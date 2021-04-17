---
description: Algunos conjuntos de teléfonos admiten la noción de descargar datos desde o cargar datos en el dispositivo telefónico, lo que permite que el conjunto de teléfonos se programe de varias maneras.
ms.assetid: 5734107d-8104-4d8a-b3f7-3cc2a48f71ca
title: Áreas de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81376549c63b4fcea92f705246cd58161faeac94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677814"
---
# <a name="data-areas"></a>Áreas de datos

Algunos conjuntos de teléfonos admiten la noción de descargar datos desde o cargar datos en el dispositivo telefónico, lo que permite que el conjunto de teléfonos se programe de varias maneras. TAPI modela estos conjuntos de teléfonos como una o varias áreas de descarga o carga. Cada área se identifica mediante un número comprendido entre cero y el número de áreas de datos disponibles en el teléfono menos uno. Los tamaños de cada área pueden variar. El formato de los propios datos es específico del dispositivo.

La función [**phoneSetData**](/windows/desktop/api/Tapi/nf-tapi-phonesetdata) de TAPI descarga un búfer de datos en un área de datos determinada en el dispositivo telefónico, y la función [**phoneGetData**](/windows/desktop/api/Tapi/nf-tapi-phonegetdata) carga el contenido de un área de datos determinada en el dispositivo teléfono en un búfer.

Cuando se cambia un área de datos de un dispositivo telefónico, se envía un mensaje de [**\_ Estado de teléfono**](phone-state.md) a la aplicación para notificar a la aplicación sobre el cambio de estado. Los parámetros de este mensaje proporcionan una indicación del cambio.

 

 



