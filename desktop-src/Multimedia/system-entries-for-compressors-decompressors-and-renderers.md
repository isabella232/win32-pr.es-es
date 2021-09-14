---
title: Entradas del sistema para descompresión, descompresión y representadores
description: Entradas del sistema para descompresión, descompresión y representadores
ms.assetid: b27bbd5b-a218-49bb-b179-b24ce39869a1
keywords:
- Vídeo para Windows (VFW), entradas del sistema de refrigeración
- VFW (vídeo para Windows), entradas del sistema de refrigeración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b46d9c6fd8974511698bcb687c580e68be3757ee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127260743"
---
# <a name="system-entries-for-compressors-decompressors-and-renderers"></a>Entradas del sistema para descompresión, descompresión y representadores

El sistema usa entradas en el Registro para buscar controladores de VCM. Estas entradas tienen el formato de dos códigos de cuatro caracteres separados por un punto. El sistema define el primer código de cuatro caracteres y puede ser uno de los siguientes:



| Código de cuatro caracteres | Descripción                               |
|---------------------|-------------------------------------------|
| "VIDC"              | Identifica los descomprimores y los descompresión. |
| "VIDS"              | Identifica los representadores de secuencias de vídeo.        |
| "TXTS"              | Identifica los representadores de flujo de texto.         |
| "AUDS"              | Identifica los controladores de secuencias de audio.         |



 

Los representadores personalizados pueden definir sus propios códigos de cuatro caracteres.

El controlador define el segundo código de cuatro caracteres. Normalmente, el segundo código de cuatro caracteres corresponde al tipo de datos que el controlador puede controlar.

Al abrir un controlador de VCM, una aplicación especifica el tipo de controlador y el tipo de controlador de datos que necesita. Normalmente, esta información procede del encabezado de secuencia. El sistema intenta abrir el controlador de datos especificado, pero si se produce un error, el sistema busca en el Registro un controlador que tenga el controlador necesario.

Al buscar el controlador, el sistema intenta hacer coincidir los códigos de cuatro caracteres especificados para el tipo de controlador y el controlador de datos con los especificados en la entrada del controlador. Por ejemplo, si una aplicación especifica el MSSQ, el sistema busca en el Registro la entrada del controlador VIDC.MSSQ. Si no encuentra una coincidencia, abre cada controlador correspondiente al tipo de controlador y busca uno que pueda controlar el tipo de datos que la aplicación especifica. En el ejemplo anterior, si el sistema no encuentra VIDC.MSSQ, abriría todos los controladores con el código de cuatro caracteres "VIDC" y buscaría uno que pueda controlar los datos.

 

 




