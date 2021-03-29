---
title: Entradas del sistema para compresores, descompresores y representadores
description: Entradas del sistema para compresores, descompresores y representadores
ms.assetid: b27bbd5b-a218-49bb-b179-b24ce39869a1
keywords:
- Vídeo para Windows (VFW), entradas del sistema compresores
- VFW (vídeo para Windows), entradas del sistema compresores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b46d9c6fd8974511698bcb687c580e68be3757ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778835"
---
# <a name="system-entries-for-compressors-decompressors-and-renderers"></a>Entradas del sistema para compresores, descompresores y representadores

El sistema utiliza las entradas del registro para buscar los controladores VCM. Estas entradas tienen el formato de códigos de 2 4 caracteres separados por un punto. El sistema define el primer código de cuatro caracteres y puede ser uno de los siguientes:



| Código de cuatro caracteres | Descripción                               |
|---------------------|-------------------------------------------|
| VIDC              | Identifica los compresores y descompresores. |
| VID              | Identifica los representadores de flujos de vídeo.        |
| "TXTS"              | Identifica los representadores de flujo de texto.         |
| "AUDS"              | Identifica los controladores de secuencias de audio.         |



 

Los representadores personalizados pueden definir sus propios códigos de cuatro caracteres.

El controlador define el segundo código de cuatro caracteres. Normalmente, el segundo código de cuatro caracteres corresponde al tipo de datos que el controlador puede controlar.

Al abrir un controlador VCM, una aplicación especifica el tipo de controlador y el tipo de controlador de datos que necesita. Normalmente, esta información procede del encabezado de flujo. El sistema intenta abrir el controlador de datos especificado, pero si se produce un error, el sistema busca en el registro un controlador que tenga el controlador necesario.

Al buscar el controlador, el sistema intenta coincidir con los códigos de cuatro caracteres especificados para el tipo de controlador y el controlador de datos con los especificados en la entrada del controlador. Por ejemplo, si una aplicación especifica el compresor MSSQ, el sistema busca en el registro la entrada del controlador VIDC. MSSQ. Si no encuentra ninguna coincidencia, abre cada controlador correspondiente al tipo de controlador y localiza una que puede controlar el tipo de datos que la aplicación especifica. En el ejemplo anterior, si el sistema no encontró VIDC. MSSQ, abriría todos los controladores con el código de cuatro caracteres "VIDC" y buscaría uno que pueda controlar los datos.

 

 




