---
title: Conceptos básicos sobre el descompresión y el descompresión
description: Conceptos básicos sobre el descompresión y el descompresión
ms.assetid: 49a958c1-1798-4c6c-913c-5bf5869f926b
keywords:
- Administrador de compresión de vídeo (VCM), apertura de las cámaras
- VCM (administrador de compresión de vídeo), apertura de ingerciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1969748949aeb023f889bc651ccd028f19c3e18fe6cf1ba088b4f4ec29292f35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144998"
---
# <a name="compressor-and-decompressor-basics"></a>Conceptos básicos sobre el descompresión y el descompresión

Para abrir y localizar un resalte, puede usar las [**funciones ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) [**e ICOpen.**](/windows/desktop/api/Vfw/nf-vfw-icopen) Puede usar **ICLocate para** buscar un conjunto de un tipo específico y obtener un identificador de él para su uso en otras funciones de VCM. Para abrir un resalte, puede usar **ICOpen**. La aplicación usa el identificador devuelto por esta función para identificar el objeto abierto cuando usa otras funciones de VCM.

Para abrir y buscar un descompresión, las aplicaciones pueden usar las macros [**ICDecompressOpen**](/windows/desktop/api/Vfw/nf-vfw-icdecompressopen) [**e ICDrawOpen.**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen) Estas macros usan **ICLocate para** la operación.

Cuando la aplicación haya terminado de usar un descompresión o un descompresión, debe cerrarla para liberar los recursos usados para la compresión o descompresión. La aplicación puede usar la [**función ICClose**](/windows/desktop/api/Vfw/nf-vfw-icclose) para cerrar el descomprimidor o el descompresión.

Además, la aplicación puede enumerar los descomprimidores o descompresión de un sistema mediante la [**función ICInfo.**](/windows/desktop/api/Vfw/nf-vfw-icinfo)

> [!Note]  
> El encabezado de secuencia de un archivo AVI contiene información sobre el tipo de secuencia y el controlador específico de esa secuencia. Dentro del encabezado de flujo, los **miembros fccType** y **fccHandler** identifican el tipo de flujo y el controlador de flujo especificado para la secuencia.

 

 

 




