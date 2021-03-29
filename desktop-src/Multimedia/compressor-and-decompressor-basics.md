---
title: Aspectos básicos del compresor y el descompresor
description: Aspectos básicos del compresor y el descompresor
ms.assetid: 49a958c1-1798-4c6c-913c-5bf5869f926b
keywords:
- Administrador de compresión de vídeo (VCM), abrir compresores
- VCM (Administrador de compresión de vídeo), abrir compresores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b51e0221c495d5e2d0782f4e56e0778c0d2462
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903428"
---
# <a name="compressor-and-decompressor-basics"></a>Aspectos básicos del compresor y el descompresor

Para abrir y buscar un compresor, puede usar las funciones [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) y [**ICOpen**](/windows/desktop/api/Vfw/nf-vfw-icopen) . Puede usar **ICLocate** para buscar un compresor de un tipo específico y obtener un identificador para usarlo en otras funciones VCM. Para abrir un compresor, puede usar **ICOpen**. La aplicación usa el identificador devuelto por esta función para identificar el compresor abierto cuando utiliza otras funciones VCM.

Para abrir y buscar un descompresor, las aplicaciones pueden usar las macros [**ICDecompressOpen**](/windows/desktop/api/Vfw/nf-vfw-icdecompressopen) y [**ICDrawOpen**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen) . Estas macros usan **ICLocate** para la operación.

Cuando la aplicación ha terminado de usar un compresor o descompresor, debe cerrarla para liberar los recursos utilizados para la compresión o la descompresión. La aplicación puede usar la función [**ICClose**](/windows/desktop/api/Vfw/nf-vfw-icclose) para cerrar el compresor o descompresor.

Además, la aplicación puede enumerar los compresores o descompresores en un sistema mediante la función [**ICInfo**](/windows/desktop/api/Vfw/nf-vfw-icinfo) .

> [!Note]  
> El encabezado de secuencia de un archivo AVI contiene información sobre el tipo de flujo y el controlador específico para ese flujo. Dentro del encabezado de flujo, los miembros **fccType** y **fccHandler** identifican el tipo de flujo y el controlador de secuencia especificado para la secuencia.

 

 

 




