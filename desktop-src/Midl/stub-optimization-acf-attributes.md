---
title: Atributos ACF de optimización de código auxiliar
description: Estos atributos permiten optimizar el tamaño y la velocidad del código auxiliar.
ms.assetid: 8c98b9ff-d91c-4a17-90c9-298f588e46c5
keywords:
- Los MIDL, atributos y optimización de código auxiliar de ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209490d6064d134a51492afee39c501059879bab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903343"
---
# <a name="stub-optimization-acf-attributes"></a>Atributos ACF de optimización de código auxiliar

Estos atributos permiten optimizar el tamaño y la velocidad del código auxiliar.



| Atributo                                    | Uso                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**código**](code.md)[**nocode**](nocode.md) | Use los atributos [**code**](code.md) y [**nocode**](nocode.md) juntos para evitar la generación de código auxiliar para las funciones no utilizadas. Aplique el atributo **nocode** al encabezado de la interfaz y aplique el atributo **code** a los procedimientos que va a implementar la aplicación cliente. El código auxiliar de cliente solo se generará para los procedimientos seleccionados.                                                                |
| [**optimiz**](optimize.md)                 | Permite ajustar el nivel de optimización que realiza el compilador MIDL al generar código auxiliar, especificando que se van a calcular las referencias de los datos mediante el método mixto o el método interpretado. Puede aplicar el atributo [**Optimize**](optimize.md) a una interfaz o a las funciones seleccionadas dentro de la interfaz. En cualquier caso, su uso invalidará las optimizaciones de la línea de comandos y los valores predeterminados que ya existan. |



 

 

 




