---
description: La arquitectura del archivo DLL del analizador debe proporcionar las características que se muestran en la ilustración siguiente.
ms.assetid: 2da5d4bc-a219-47b5-8522-1237f7bcac16
title: Arquitectura dll del analizador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb8b2c3ead77d5172bc57fa3bc1c8b6001b9c690cd254dc436ac93f504ddb732
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962874"
---
# <a name="parser-dll-architecture"></a>Arquitectura dll del analizador

La arquitectura del archivo DLL del analizador debe proporcionar las características que se muestran en la ilustración siguiente. Tenga en cuenta que algunas características requieren la implementación de solo un punto de entrada. Sin embargo, si el archivo DLL del analizador admite varios protocolos, la característica requiere la implementación de varios puntos de entrada.

![características dll del analizador](images/parserarchitecture1.png)



| Para información acerca de                                                  | Vea                                                                    |
|------------------------------------------------------------------------|------------------------------------------------------------------------|
| Cómo implementar funciones de exportación de DLL del analizador.                          | [Escribir un analizador de protocolos](writing-a-protocol-parser.md)             |
| Funciones y estructuras específicas que usan los analizadores: temas de referencia. | [Funciones y estructuras del analizador](parser-functions-and-structures.md) |



 

 

 



