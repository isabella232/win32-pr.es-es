---
title: Establecer y rellenar montones de descriptores
description: Los tipos de montón descriptor que se pueden establecer en una lista de comandos son aquellos que contienen descriptores para los que se pueden usar tablas de descriptor (como máximo una de cada cada vez).
ms.assetid: F0FF3D7C-1DAC-48C3-B47D-0378BE369F37
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0e3a1b6c4863827e1d8e1bdfb33a0a64420211d
ms.sourcegitcommit: 584b35959515bc5e4a104e8cf5270513f146f590
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/03/2019
ms.locfileid: "104549101"
---
# <a name="setting-and-populating-descriptor-heaps"></a>Establecer y rellenar montones de descriptores

Los tipos de montón descriptor que se pueden establecer en una lista de comandos son aquellos que contienen descriptores para los que se pueden usar tablas de descriptor (como máximo una de cada cada vez).

-   [Configuración de montones de descriptor](#setting-and-populating-descriptor-heaps)
-   [Rellenar montones de descriptores](#populating-descriptor-heaps)
-   [Temas relacionados](#related-topics)

## <a name="setting-descriptor-heaps"></a>Configuración de montones de descriptor

Los tipos de montón de descriptor que se pueden establecer en una lista de comandos son:

``` syntax
D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV
D3D12_DESCRIPTOR_HEAP_TYPE_SAMPLER
```

Los montones que se establecen en la lista de comandos también se deben haber creado como sombreador visible. Hay tres tipos de lista de comandos: directo, AGRUPAción y proceso.

Una vez establecido un montón de descriptores en una lista de comandos, las llamadas subsiguientes que definen las tablas de descriptores hacen referencia al montón descriptor actual. El estado de la tabla de descriptores es undefined al principio de una lista de comandos y los montones de descriptores se cambian en una lista de comandos. Establecer el mismo montón de descriptor redundante no hace que la configuración de la tabla de descriptores sea indefinida.

En una agrupación, por el contrario, los montones de descriptor solo se pueden establecer una vez (las llamadas redundantes que establecen el mismo montón dos veces no producen un error). de lo contrario, el comportamiento es indefinido. Los montones de descriptores que se establecen deben coincidir con el estado cuando cualquier lista de comandos llama a la agrupación; de lo contrario, el comportamiento es indefinido. Esto permite a los paquetes heredar y editar la configuración de la tabla de descriptores de la lista de comandos. Los paquetes que no cambian las tablas de descriptores (solo los heredan) no necesitan establecer un montón de descriptores en absoluto y simplemente heredan de la lista de comandos que realiza la llamada.

Cuando se establecen montones de descriptor (mediante [**ID3D12GraphicsCommandList:: SetDescriptorHeaps**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)), todos los montones que se usan se establecen en una única llamada (y todos los montones establecidos previamente no están establecidos por la llamada). Como máximo, se puede establecer en la llamada un montón de cada tipo enumerado anteriormente.

## <a name="populating-descriptor-heaps"></a>Rellenar montones de descriptores

Después de que una aplicación haya creado un montón de descriptores, puede usar métodos en el dispositivo para generar los descriptores directamente en el montón o en los descriptores de copia de un lugar a otro.

El contenido inicial de la memoria del montón de descriptores es indefinido, por lo que pedir a la GPU o al controlador que haga referencia a la memoria no inicializada para la representación puede producir resultados indefinidos, como un restablecimiento del dispositivo.

Si la aplicación configura un montón de descriptores para que sea visible para la CPU, la CPU puede llamar a métodos para crear descriptores en el montón y copiar desde el lugar (incluidos entre montones) de forma inmediata y gratuita. Si el montón se ha configurado como SHADER_VISIBLE, no se permite la lectura de la CPU.



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Montones de descriptores](descriptor-heaps.md)
</dt> </dl>

 

 




