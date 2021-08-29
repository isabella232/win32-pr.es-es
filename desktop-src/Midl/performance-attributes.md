---
title: Atributos de rendimiento
description: Use los atributos siguientes en un archivo IDL para reducir el tamaño del código auxiliar o mejorar el rendimiento.
ms.assetid: 0f23265e-7f3e-4a15-ac3b-1d852a8110eb
keywords:
- IDL MIDL, atributos, rendimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f784bc534fd1dd7f160eaccb87a2853d491237db915245d4f36823e1ceb559ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869465"
---
# <a name="performance-attributes"></a>Atributos de rendimiento

Use los atributos siguientes en un archivo IDL para reducir el tamaño del código auxiliar o mejorar el rendimiento.



| Atributo                             | Uso                                                                                                                                                |
|---------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ignorar**](ignore.md)              | Designa que un puntero contenido en una estructura o unión y el objeto indicado por el puntero no se va a transmitir.                        |
| [**Local**](local.md)                | Designa una función local para la aplicación para la que MIDL no necesita generar código auxiliar.                                           |
| [**wire \_ marshal**](wire-marshal.md) | Define un tipo de datos como un tipo más sencillo para la transmisión a través de una red y permite implementar rutinas de serialización y desmarque para el tipo. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Atributos de ACF de administración de memoria](memory-management-acf-attributes.md)
</dt> <dt>

[Atributos ACF de optimización de código auxiliar](stub-optimization-acf-attributes.md)
</dt> </dl>

 

 




