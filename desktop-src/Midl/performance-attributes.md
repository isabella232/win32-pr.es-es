---
title: Atributos de rendimiento
description: Use los atributos siguientes en un archivo IDL para reducir el tamaño del código auxiliar o mejorar el rendimiento.
ms.assetid: 0f23265e-7f3e-4a15-ac3b-1d852a8110eb
keywords:
- IDL MIDL, atributos, rendimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afbfa518b400d237c9fd3789f61b7e74a0c38276
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159423"
---
# <a name="performance-attributes"></a>Atributos de rendimiento

Use los atributos siguientes en un archivo IDL para reducir el tamaño del código auxiliar o mejorar el rendimiento.



| Atributo                             | Uso                                                                                                                                                |
|---------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ignorar**](ignore.md)              | Designa que no se va a transmitir un puntero contenido en una estructura o unión y el objeto indicado por el puntero.                        |
| [**Local**](local.md)                | Designa una función que es local para la aplicación para la que MIDL no necesita generar código auxiliar.                                           |
| [**wire \_ marshal**](wire-marshal.md) | Define un tipo de datos como un tipo más sencillo para la transmisión a través de una red y permite implementar rutinas de serialización y desmarque para el tipo. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Atributos ACF de administración de memoria](memory-management-acf-attributes.md)
</dt> <dt>

[Atributos ACF de optimización de código auxiliar](stub-optimization-acf-attributes.md)
</dt> </dl>

 

 




