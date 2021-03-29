---
title: Enumeración de formato de entrada
description: Enumeración de formato de entrada
ms.assetid: 75264598-0226-435a-b71f-6997ff0fcaff
keywords:
- SDK de Windows Media Format, enumeraciones de formato de entrada
- Windows Media Format SDK, enumerar formatos de entrada
- Advanced Systems Format (ASF), enumeraciones de formato de entrada
- ASF (formato de sistemas avanzados), enumeraciones de formato de entrada
- Advanced Systems Format (ASF), enumerar formatos de entrada
- ASF (formato de sistemas avanzados), enumerar formatos de entrada
- enumeraciones de formato de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e853aeeac5ca470f1b33b611b287cba8fa025dc0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104487010"
---
# <a name="input-format-enumeration"></a>Enumeración de formato de entrada

El objeto de escritor obtiene la información de formato de secuencia del perfil que le asigna. La información de configuración de secuencia de un perfil proporciona al escritor toda la información que necesita sobre cómo se escriben los datos en el archivo. El perfil no proporciona al escritor información sobre el formato de los ejemplos de entrada que proporciona la aplicación. Los formatos de entrada serán desconocidos únicamente para las secuencias comprimidas con uno de los códecs de Windows Media. las entradas de tipos de flujo arbitrarios son predecibles en función de la información del perfil.

El objeto de escritor puede comunicarse con el códec de una secuencia para determinar los tipos de entrada que se pueden utilizar. Se proporcionan métodos para enumerar los posibles tipos de entrada. Siempre debe buscar el tipo de entrada que coincida con los medios de entrada mediante la enumeración de los tipos admitidos en lugar de establecer las propiedades de los medios de entrada manualmente. Para obtener más información, vea [para enumerar los formatos de entrada](to-enumerate-input-formats.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características de escritura de archivos**](file-writing-features.md)
</dt> <dt>

[**Trabajar con entradas**](working-with-inputs.md)
</dt> </dl>

 

 




