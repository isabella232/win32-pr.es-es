---
title: Trabajar con entradas
description: Trabajar con entradas
ms.assetid: 72daa7ca-4264-46bf-91ac-8b95fdbfd41c
keywords:
- SDK de Windows Media Format, trabajar con entradas
- Advanced Systems Format (ASF), trabajar con entradas
- ASF (formato de sistemas avanzados), trabajar con entradas
- perfiles, trabajar con entradas
- flujos, trabajar con entradas
- códecs, trabajar con entradas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94e7016b5304b0d77e130b68d9a9feef15ffe54d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486719"
---
# <a name="working-with-inputs"></a>Trabajar con entradas

Del mismo modo que la configuración de la secuencia adecuada en el perfil es necesaria para que el códec pueda comprimir un flujo, también debe asegurarse de que el tipo de medio sin comprimir que se pasa al escritor se describe con precisión. Cada códec de Windows Media tiene asociado un tipo de entrada predeterminado, pero se admiten varios tipos de entrada. Puede examinar las entradas admitidas y seleccionar la que coincida con los datos. El proceso de trabajo con entradas se resume en los pasos siguientes:

1.  Cuando se carga un perfil para que lo use el escritor, el objeto de escritor asigna un número de entrada para cada conexión del perfil. Para obtener más información acerca de la carga de perfiles para el escritor, consulte [para usar perfiles con el escritor](to-use-profiles-with-the-writer.md). A menos que use la exclusión mutua por velocidad de bits, existe una conexión para cada flujo. Las secuencias que se excluyen mutuamente con la velocidad de bits comparten una única conexión.
2.  La aplicación debe identificar los números de entrada del archivo. Para obtener más información acerca de la identificación de números de entrada, consulte [para identificar entradas por número](to-identify-inputs-by-number.md).
3.  Para cada entrada, debe asegurarse de que el formato de entrada coincide con los datos. Puede enumerar los formatos de entrada admitidos por el SDK. Para obtener más información, vea [para enumerar los formatos de entrada](to-enumerate-input-formats.md). No se pueden enumerar los formatos de entrada de secuencias o flujos arbitrarios que ya están comprimidos. Para obtener más información sobre estos casos especiales, consulte [entradas de secuencias arbitrarias y precomprimidas](arbitrary-and-precompressed-stream-inputs.md).
4.  Asigne el formato de entrada correcto para cada conexión. Para obtener más información, vea [asignar formatos de entrada](assigning-input-formats.md).
5.  Algunas características de los códecs y del escritor se configuran en el momento de la codificación en lugar de en el perfil. Para configurar estas características, debe usar la configuración de entrada. Para obtener más información, vea [para establecer la configuración de entrada](to-set-input-settings.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Escribir archivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




