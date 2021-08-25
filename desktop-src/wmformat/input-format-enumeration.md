---
title: Enumeración de formato de entrada
description: Enumeración de formato de entrada
ms.assetid: 75264598-0226-435a-b71f-6997ff0fcaff
keywords:
- Windows SDK de formato multimedia, enumeraciones de formato de entrada
- Windows SDK de formato multimedia, enumeración de formatos de entrada
- Formato de sistemas avanzados (ASF), enumeraciones de formato de entrada
- ASF (formato de sistemas avanzados), enumeraciones de formato de entrada
- Formato de sistemas avanzados (ASF), enumeración de formatos de entrada
- ASF (formato de sistemas avanzados), enumeración de formatos de entrada
- enumeraciones de formato de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a261b2edae285a970bead5d039c4e85076530eb363aa025289b75ec56618406
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809045"
---
# <a name="input-format-enumeration"></a>Enumeración de formato de entrada

El objeto de escritor obtiene información de formato de secuencia del perfil que se le proporciona. La información de configuración de secuencias de un perfil proporciona al escritor toda la información que necesita sobre cómo se escribirán los datos en el archivo. El perfil no proporciona al escritor ninguna información sobre el formato de los ejemplos de entrada que la aplicación proporciona. Los formatos de entrada solo serán desconocidos para las secuencias comprimidas con uno de los códecs Windows media; Las entradas para tipos de secuencia arbitrarios son predecibles en función de la información del perfil.

El objeto de escritor puede comunicarse con el códec de una secuencia para determinar los tipos de entrada que se pueden usar. Se proporcionan métodos para enumerar los posibles tipos de entrada. Siempre debe encontrar el tipo de entrada que coincida con los medios de entrada enumerando los tipos admitidos en lugar de establecer manualmente las propiedades de los medios de entrada. Para obtener más información, vea [Para enumerar formatos de entrada.](to-enumerate-input-formats.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características de escritura de archivos**](file-writing-features.md)
</dt> <dt>

[**Trabajar con entradas**](working-with-inputs.md)
</dt> </dl>

 

 




