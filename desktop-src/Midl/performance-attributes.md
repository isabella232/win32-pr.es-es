---
title: Atributos de rendimiento
description: Use los atributos siguientes en un archivo IDL para reducir el tamaño del código auxiliar o mejorar el rendimiento.
ms.assetid: 0f23265e-7f3e-4a15-ac3b-1d852a8110eb
keywords:
- MIDL, atributos y rendimiento de IDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afbfa518b400d237c9fd3789f61b7e74a0c38276
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076361"
---
# <a name="performance-attributes"></a>Atributos de rendimiento

Use los atributos siguientes en un archivo IDL para reducir el tamaño del código auxiliar o mejorar el rendimiento.



| Atributo                             | Uso                                                                                                                                                |
|---------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**omitir**](ignore.md)              | Designa que un puntero contenido en una estructura o Unión y el objeto indicado por el puntero no se va a transmitir.                        |
| [**localizar**](local.md)                | Designa una función que es local para la aplicación para la que MIDL no necesita generar código auxiliar.                                           |
| [**\_serialización de cable**](wire-marshal.md) | Define un tipo de datos como un tipo más simple para la transmisión a través de una red y le permite implementar la serialización y la desserialización de rutinas para el tipo. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Atributos ACF de administración de memoria](memory-management-acf-attributes.md)
</dt> <dt>

[Atributos ACF de optimización de código auxiliar](stub-optimization-acf-attributes.md)
</dt> </dl>

 

 




