---
title: Trabajar con entradas
description: Trabajar con entradas
ms.assetid: 72daa7ca-4264-46bf-91ac-8b95fdbfd41c
keywords:
- Windows SDK de formato multimedia, trabajar con entradas
- Formato de sistemas avanzados (ASF), trabajar con entradas
- ASF (formato de sistemas avanzados), trabajar con entradas
- perfiles, trabajar con entradas
- flujos, trabajar con entradas
- códecs, trabajar con entradas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54a922338ce8c26e30851c630a0174348522d8c08eec2d547ed2a468e3fa80cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928455"
---
# <a name="working-with-inputs"></a>Trabajar con entradas

Del mismo modo que se requiere la configuración de secuencia adecuada en el perfil para obtener el códec para comprimir una secuencia, también debe asegurarse de que el tipo de medio sin comprimir que pasa al escritor se describe con precisión. Cada códec Windows media tiene un tipo de entrada predeterminado asociado, pero se admiten varios tipos de entrada. Puede examinar las entradas admitidas y seleccionar la que coincida con los datos. El proceso de trabajar con entradas se resume en los pasos siguientes:

1.  Al cargar un perfil para que lo use el escritor, el objeto de escritor asigna un número de entrada para cada conexión del perfil. Para obtener más información sobre la carga de perfiles para el escritor, vea [Para usar perfiles con el escritor](to-use-profiles-with-the-writer.md). A menos que use la exclusión mutua por velocidad de bits, hay una conexión para cada secuencia. Secuencias que se excluyen mutuamente por la velocidad de bits comparten una sola conexión.
2.  La aplicación debe identificar los números de entrada del archivo. Para obtener más información sobre cómo identificar números de entrada, vea [Para identificar entradas por número.](to-identify-inputs-by-number.md)
3.  Para cada entrada, debe asegurarse de que el formato de entrada coincide con los datos. Puede enumerar los formatos de entrada admitidos por el SDK. Para obtener más información, vea [Para enumerar formatos de entrada.](to-enumerate-input-formats.md) No se pueden enumerar los formatos de entrada de secuencias arbitrarias o secuencias que ya están comprimidas. Para obtener más información sobre estos casos especiales, vea [Entradas de flujo arbitrarias y precomprimidas.](arbitrary-and-precompressed-stream-inputs.md)
4.  Asigne el formato de entrada correcto para cada conexión. Para obtener más información, vea [Asignación de formatos de entrada.](assigning-input-formats.md)
5.  Algunas características de códec y escritor se configuran en tiempo de codificación en lugar de en el perfil. Para configurar estas características, debe usar la configuración de entrada. Para obtener más información, vea [Para establecer la entrada Configuración](to-set-input-settings.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Escritura de archivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




