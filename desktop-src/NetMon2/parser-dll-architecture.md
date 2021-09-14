---
description: La arquitectura del archivo DLL del analizador debe proporcionar las características que se muestran en la ilustración siguiente.
ms.assetid: 2da5d4bc-a219-47b5-8522-1237f7bcac16
title: Arquitectura dll del analizador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7852029a892d8b74c954cbc2d7341fcaf29032fb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362145"
---
# <a name="parser-dll-architecture"></a>Arquitectura dll del analizador

La arquitectura del archivo DLL del analizador debe proporcionar las características que se muestran en la ilustración siguiente. Tenga en cuenta que algunas características requieren la implementación de solo un punto de entrada. Sin embargo, si el archivo DLL del analizador admite varios protocolos, la característica requiere la implementación de varios puntos de entrada.

![características dll del analizador](images/parserarchitecture1.png)



| Para información acerca de                                                  | Vea                                                                    |
|------------------------------------------------------------------------|------------------------------------------------------------------------|
| Cómo implementar funciones de exportación de DLL del analizador.                          | [Escribir un analizador de protocolos](writing-a-protocol-parser.md)             |
| Funciones y estructuras específicas que usan los analizadores: temas de referencia. | [Funciones y estructuras del analizador](parser-functions-and-structures.md) |



 

 

 



