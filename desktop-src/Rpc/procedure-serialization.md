---
title: Serialización de procedimientos
description: Cuando se usa la serialización de procedimientos, un procedimiento se etiqueta con el atributo \ encode \ o \ decode \. En lugar de generar el código auxiliar remoto habitual, el compilador genera un código auxiliar de serialización para la rutina.
ms.assetid: 98367b00-696b-44c4-a747-92ecac34ba1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77696761a9aa5fe1471e9ebf24a57303b15d0ff3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104424144"
---
# <a name="procedure-serialization"></a>Serialización de procedimientos

Cuando se utiliza la serialización de procedimientos, un procedimiento se etiqueta con el atributo de \[ [**codificación**](/windows/desktop/Midl/encode) \] o \[ [**descodificación**](/windows/desktop/Midl/decode) \] . En lugar de generar el código auxiliar remoto habitual, el compilador genera un código auxiliar de serialización para la rutina.

Del mismo modo que un procedimiento remoto debe usar un identificador de enlace para realizar una llamada remota, un procedimiento de serialización debe utilizar un identificador de serialización para usar los servicios de serialización. Si no se especifica un identificador de serialización, se utiliza un identificador implícito predeterminado para dirigir la llamada. Por otro lado, si se especifica el identificador de serialización, ya sea como un [**argumento \_ de identificador**](/windows/desktop/Midl/handle-t) explícito de la rutina o mediante el \[ atributo de [**\_ identificador explícito**](/windows/desktop/Midl/explicit-handle) \] , debe pasar un identificador válido como argumento de la llamada. Para obtener información adicional sobre cómo crear un identificador de serialización válido, vea [identificadores de serialización](serialization-handles.md), [ejemplos de codificación de búfer fija](fixed-buffer-serialization.md)y [ejemplos de codificación incremental](examples-of-incremental-encoding.md).

> [!Note]
> Microsoft RPC permite mezclar procedimientos remotos y de serialización en una interfaz. Sin embargo, tenga cuidado al hacerlo.
> 
> En el caso de los procedimientos remotos con identificadores de enlace implícitos, el compilador MIDL genera una variable de identificador global del identificador de tipo [**\_ t**](/windows/desktop/Midl/handle-t). Los procedimientos y tipos con identificadores de serialización implícitos usan esta misma variable de identificador global.
> 
> En el caso de los identificadores implícitos, el identificador implícito global debe establecerse en un identificador de enlace válido antes de una llamada remota. El identificador implícito debe establecerse en un identificador de serialización válido antes de una llamada de serialización. Por lo tanto, un procedimiento no puede ser remoto ni serializado. Debe ser uno u otro.

 

 

 