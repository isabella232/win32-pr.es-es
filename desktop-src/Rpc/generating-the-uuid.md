---
title: Generar el UUID
description: El primer paso para definir la interfaz es usar la utilidad uuidgen para generar un identificador único universal (UUID).
ms.assetid: 870641b7-affc-4de4-bc7f-4c8ca2873fb6
keywords:
- RPC llamada a procedimiento remoto, tareas, generar el UUID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e263bfe21c4a564106c0d6328c0de891c18bca1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903435"
---
# <a name="generating-the-uuid"></a>Generar el UUID

El primer paso para definir la interfaz es usar la utilidad **uuidgen** para generar un identificador único universal (UUID). Un UUID permite que las aplicaciones cliente y servidor se identifiquen entre sí. La utilidad **uuidgen** (Uuidgen.exe) se instala automáticamente al instalar el kit de desarrollo de software (SDK) de la plataforma.

El siguiente comando genera un UUID y crea un archivo de plantilla denominado Hello. idl.

**uuidgen/i/ohello.idl**

La plantilla Hello. idl tendrá el siguiente aspecto (con un UUID diferente, por supuesto).

``` syntax
[
    uuid(7a98c250-6808-11cf-b73b-00aa00b677a7),
    version(1.0)
]
interface INTERFACENAME
{
 
}
```

 

 




