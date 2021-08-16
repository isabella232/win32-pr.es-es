---
title: Atributos ACF de optimización de código auxiliar
description: Estos atributos permiten optimizar el tamaño y la velocidad del código auxiliar.
ms.assetid: 8c98b9ff-d91c-4a17-90c9-298f588e46c5
keywords:
- MIDL de ACF, atributos, optimización de código auxiliar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f8386eb6a6077a994b6f9800ff237a9966e97bff5eb0d6d865ea313634790f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118383197"
---
# <a name="stub-optimization-acf-attributes"></a>Atributos ACF de optimización de código auxiliar

Estos atributos permiten optimizar el tamaño y la velocidad del código auxiliar.



| Atributo                                    | Uso                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**code**](code.md)[**nocode**](nocode.md) | Use el [**código y**](code.md) los atributos [**de codificación**](nocode.md) conjuntamente para evitar la generación de código auxiliar para las funciones no utilizadas. Aplique el **atributo nocode** al encabezado de interfaz y aplique el atributo **de** código a los procedimientos que implementará la aplicación cliente. El código auxiliar de cliente solo se generará para los procedimientos seleccionados.                                                                |
| [**Optimizar**](optimize.md)                 | Permite ajustar el nivel de optimización que realiza el compilador MIDL al generar código auxiliar, especificando que los datos se serializarán mediante el método de modo mixto o interpretado. Puede aplicar el atributo [**optimize**](optimize.md) a una interfaz o a funciones seleccionadas dentro de la interfaz. En cualquier caso, su uso invalidará las optimizaciones de línea de comandos y los valores predeterminados preexistentes. |



 

 

 




