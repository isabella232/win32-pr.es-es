---
title: Configuración y relleno de los montones de descriptores
description: Los tipos de montón de descriptores que se pueden establecer en una lista de comandos son aquellos que contienen descriptores para los que se pueden usar tablas de descriptores (como máximo una de cada una a la vez).
ms.assetid: F0FF3D7C-1DAC-48C3-B47D-0378BE369F37
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0e3a1b6c4863827e1d8e1bdfb33a0a64420211d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072875"
---
# <a name="setting-and-populating-descriptor-heaps"></a>Configuración y relleno de los montones de descriptores

Los tipos de montón de descriptores que se pueden establecer en una lista de comandos son aquellos que contienen descriptores para los que se pueden usar tablas de descriptores (como máximo una de cada una a la vez).

-   [Configuración de montones de descriptores](#setting-and-populating-descriptor-heaps)
-   [Rellenar montones de descriptores](#populating-descriptor-heaps)
-   [Temas relacionados](#related-topics)

## <a name="setting-descriptor-heaps"></a>Configuración de montones de descriptores

Los tipos de montón de descriptores que se pueden establecer en una lista de comandos son:

``` syntax
D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV
D3D12_DESCRIPTOR_HEAP_TYPE_SAMPLER
```

Los montones que se establecen en la lista de comandos también se deben haber creado como sombreadores visibles. Hay tres tipos de lista de comandos: DIRECT, BUNDLE y COMPUTE.

Después de establecer un montón de descriptores en una lista de comandos, las llamadas posteriores que definen tablas de descriptores hacen referencia al montón de descriptores actual. El estado de la tabla de descriptores no está definido al principio de una lista de comandos y después de cambiar los montones de descriptores en una lista de comandos. Establecer de forma redundante el mismo montón de descriptores no hace que la configuración de la tabla de descriptores sea indefinido.

En una agrupación, por el contrario, los montones de descriptores solo se pueden establecer una vez (las llamadas redundantes que establecen el mismo montón dos veces no producen un error); de lo contrario, el comportamiento es indefinido. Los montones de descriptores que se establecen deben coincidir con el estado cuando cualquier lista de comandos llama a la agrupación; de lo contrario, el comportamiento es indefinido. Esto permite a los paquetes heredar y editar la configuración de la tabla de descriptores de la lista de comandos. Los paquetes que no cambian las tablas de descriptores (solo heredan) no necesitan establecer un montón de descriptores y simplemente heredan de la lista de comandos de llamada.

Cuando se establecen montones de descriptores (mediante [**ID3D12GraphicsCommandList::SetDescriptorHeaps),**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)todos los montones que se usan se establecen en una sola llamada (y la llamada no establece todos los montones establecidos previamente). Como máximo, se puede establecer un montón de cada tipo enumerado anteriormente en la llamada.

## <a name="populating-descriptor-heaps"></a>Rellenar montones de descriptores

Una vez que una aplicación ha creado un montón de descriptores, puede usar métodos en el dispositivo para generar descriptores directamente en el montón o copiar descriptores de un lugar a otro.

El contenido inicial de la memoria del montón de descriptores es indefinido, por lo que pedir a la GPU o al controlador que haga referencia a la memoria no inicializada para la representación puede provocar resultados indefinidos, como un restablecimiento del dispositivo.

Si la aplicación configura un montón de descriptores para que sea visible para la CPU, la CPU puede llamar a métodos para crear descriptores en el montón y copiar de un lugar a otro (incluidos los montones) de forma inmediata y libre en subprocesos. Si el montón se ha configurado como SHADER_VISIBLE, no se permite la lectura por parte de la CPU.



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Montones de descriptores](descriptor-heaps.md)
</dt> </dl>

 

 




