---
description: La arquitectura de la DLL del analizador debe proporcionar las características que se muestran en la siguiente ilustración.
ms.assetid: 2da5d4bc-a219-47b5-8522-1237f7bcac16
title: Arquitectura de DLL de analizador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7852029a892d8b74c954cbc2d7341fcaf29032fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104498143"
---
# <a name="parser-dll-architecture"></a>Arquitectura de DLL de analizador

La arquitectura de la DLL del analizador debe proporcionar las características que se muestran en la siguiente ilustración. Tenga en cuenta que algunas características requieren la implementación de un solo punto de entrada. Sin embargo, si el archivo DLL del analizador admite varios protocolos, la característica requiere la implementación de varios puntos de entrada.

![características de dll de analizador](images/parserarchitecture1.png)



| Para información acerca de                                                  | Vea                                                                    |
|------------------------------------------------------------------------|------------------------------------------------------------------------|
| Cómo implementar funciones de exportación de DLL de analizador.                          | [Escritura de un analizador de protocolos](writing-a-protocol-parser.md)             |
| Funciones y estructuras específicas que los analizadores usan: temas de referencia. | [Funciones y estructuras del analizador](parser-functions-and-structures.md) |



 

 

 



