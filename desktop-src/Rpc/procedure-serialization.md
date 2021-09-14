---
title: Serialización de procedimientos
description: Cuando se usa la serialización de procedimientos, un procedimiento se etiqueta con el atributo \ encode\ o \ decode\. En lugar de generar el código auxiliar remoto habitual, el compilador genera un código auxiliar de serialización para la rutina.
ms.assetid: 98367b00-696b-44c4-a747-92ecac34ba1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77696761a9aa5fe1471e9ebf24a57303b15d0ff3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361924"
---
# <a name="procedure-serialization"></a>Serialización de procedimientos

Cuando se usa la serialización de procedimientos, un procedimiento se etiqueta con el atributo \[ [**de codificación**](/windows/desktop/Midl/encode) \] o \[ [**descodificación.**](/windows/desktop/Midl/decode) \] En lugar de generar el código auxiliar remoto habitual, el compilador genera un código auxiliar de serialización para la rutina.

Del mismo modo que un procedimiento remoto debe usar un identificador de enlace para realizar una llamada remota, un procedimiento de serialización debe usar un identificador de serialización para usar servicios de serialización. Si no se especifica un identificador de serialización, se usa un identificador implícito predeterminado para dirigir la llamada. Por otro lado, si se especifica el identificador de serialización, ya sea como argumento [**\_ t**](/windows/desktop/Midl/handle-t) de identificador explícito de la rutina o mediante el atributo handle explícito, debe pasar un identificador válido como argumento de la \[ [**\_**](/windows/desktop/Midl/explicit-handle) \] llamada. Para obtener información adicional sobre cómo crear un identificador [](fixed-buffer-serialization.md)de serialización válido, vea Identificadores de serialización [,](serialization-handles.md)Ejemplos de codificación de búfer fija y Ejemplos [de codificación incremental](examples-of-incremental-encoding.md).

> [!Note]
> Rpc de Microsoft permite que los procedimientos remotos y de serialización se mezclen en una interfaz. Sin embargo, tenga cuidado al hacerlo.
> 
> Para los procedimientos remotos con identificadores de enlace implícitos, el compilador MIDL genera una variable de identificador global de tipo [**handle \_ t**](/windows/desktop/Midl/handle-t). Los procedimientos y tipos con identificadores de serialización implícitos usan esta misma variable de identificador global.
> 
> Para los identificadores implícitos, el identificador implícito global debe establecerse en un identificador de enlace válido antes de una llamada remota. El identificador implícito debe establecerse en un identificador de serialización válido antes de una llamada de serialización. Por lo tanto, un procedimiento no puede ser remoto ni serializado. Debe ser uno u otro.

 

 

 