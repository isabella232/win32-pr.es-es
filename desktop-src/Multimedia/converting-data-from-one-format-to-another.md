---
title: Convertir datos de un formato a otro
description: Convertir datos de un formato a otro
ms.assetid: df995b7d-ac45-4964-a1b0-efd079c0c010
keywords:
- Administrador de compresión de audio (ACM), convertir datos
- ACM (Administrador de compresión de audio), convertir datos
- Ejemplos de ACM, convertir datos
- convertir datos
- acmStreamOpen función)
- acmStreamSize función)
- acmStreamPrepareHeader función)
- acmStreamConvert función)
- acmStreamUnprepareHeader función)
- acmStreamClose función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9645342aa9f19b2c31de77dc9d1031122ed0b2ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357042"
---
# <a name="converting-data-from-one-format-to-another"></a>Convertir datos de un formato a otro

ACM usa funciones de secuencia para admitir la conversión de formato de datos. Los convertidores en ACM cambian el formato, pero no el tipo de datos. Por ejemplo, un módulo de convertidor puede cambiar los datos de 44 kHz de 16 bits 44 a los datos de 8 bits y de 8 kHz.

Las siguientes funciones ACM admiten la conversión de formato de datos. Aparecen en el orden en el que normalmente los usaría.

-   La función [**acmStreamOpen**](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen) abre un flujo de conversión.
-   La función [**acmStreamSize**](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize) calcula el tamaño adecuado del búfer de origen o de destino.
-   La función [**acmStreamPrepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader) prepara los búferes de origen y de destino que se van a usar en una conversión.
-   La función [**acmStreamConvert**](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert) convierte los datos de un búfer de origen en el formato de destino, escribiendo los datos convertidos en el búfer de destino.
-   La función [**acmStreamUnprepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader) limpia los búferes de origen y de destino preparados por **acmStreamPrepareHeader**. Debe llamar a esta función antes de liberar los búferes de origen y de destino.
-   La función [**acmStreamClose**](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose) cierra una secuencia de conversión.

Al convertir datos, identifique primero el formato de origen y, a continuación, elija el formato de destino. La forma más fácil de hacerlo es mediante la función [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) , que muestra un cuadro de diálogo de selección de formato y devuelve la opción de formato del usuario.

Cuando conozca los formatos de origen y de destino, puede usar [**acmStreamOpen**](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen) para abrir una secuencia de conversión. A continuación, puede usar la función [**acmStreamSize**](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize) para determinar los tamaños de búfer adecuados.

El siguiente paso es preparar los búferes que se van a usar en la conversión mediante [**acmStreamPrepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader).

Para realizar la conversión, use [**acmStreamConvert**](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert) hasta que se hayan procesado todos los búferes. Una vez finalizada la conversión, use [**acmStreamUnprepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader) para limpiar los búferes y, a continuación, use [**acmStreamClose**](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose) para cerrar la secuencia de conversión.

 

 




