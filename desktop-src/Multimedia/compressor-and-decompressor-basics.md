---
title: Conceptos básicos sobre el descompresión y el descompresión
description: Conceptos básicos sobre el descompresión y el descompresión
ms.assetid: 49a958c1-1798-4c6c-913c-5bf5869f926b
keywords:
- Administrador de compresión de vídeo (VCM), apertura de las cámaras
- VCM (administrador de compresión de vídeo), apertura de ingerciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b51e0221c495d5e2d0782f4e56e0778c0d2462
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372086"
---
# <a name="compressor-and-decompressor-basics"></a>Conceptos básicos sobre el descompresión y el descompresión

Para abrir y localizar un resalte, puede usar las [**funciones ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) [**e ICOpen.**](/windows/desktop/api/Vfw/nf-vfw-icopen) Puede usar **ICLocate para** buscar un conjunto de un tipo específico y obtener un identificador de él para su uso en otras funciones de VCM. Para abrir una ventana, puede usar **ICOpen**. La aplicación usa el identificador devuelto por esta función para identificar el objeto abierto cuando usa otras funciones de VCM.

Para abrir y buscar un descompresión, las aplicaciones pueden usar las macros [**ICDecompressOpen**](/windows/desktop/api/Vfw/nf-vfw-icdecompressopen) [**e ICDrawOpen.**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen) Estas macros usan **ICLocate para** la operación.

Cuando la aplicación haya terminado de usar un descompresión o un descompresión, debe cerrarla para liberar los recursos usados para la compresión o descompresión. La aplicación puede usar la [**función ICClose**](/windows/desktop/api/Vfw/nf-vfw-icclose) para cerrar el descomprimidor o el descompresión.

Además, la aplicación puede enumerar los descompresores o los descompresión de un sistema mediante la [**función ICInfo.**](/windows/desktop/api/Vfw/nf-vfw-icinfo)

> [!Note]  
> El encabezado de secuencia de un archivo AVI contiene información sobre el tipo de secuencia y el controlador específico de esa secuencia. Dentro del encabezado de flujo, los **miembros fccType** y **fccHandler** identifican el tipo de flujo y el controlador de flujo especificado para la secuencia.

 

 

 




