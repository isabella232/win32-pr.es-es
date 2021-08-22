---
title: Generación del UUID
description: El primer paso para definir la interfaz es usar la utilidad uuidgen para generar un identificador único universal (UUID).
ms.assetid: 870641b7-affc-4de4-bc7f-4c8ca2873fb6
keywords:
- Llamada a procedimiento remoto RPC, tareas, generación del UUID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21c1fbb257a4ce41a4fc0159f703a01705b4dd5926356d7850ec4ce1e0d2e002
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929532"
---
# <a name="generating-the-uuid"></a>Generación del UUID

El primer paso para definir la interfaz es usar la **utilidad uuidgen** para generar un identificador único universal (UUID). Un UUID permite que las aplicaciones cliente y servidor se identifiquen entre sí. La **utilidad uuidgen** (Uuidgen.exe) se instala automáticamente al instalar el Kit de desarrollo de software (SDK) de plataforma.

El comando siguiente genera un UUID y crea un archivo de plantilla denominado Hello.idl.

**uuidgen /i /ohello.idl**

La plantilla hello.idl tendrá este aspecto (con un UUID diferente, por supuesto).

``` syntax
[
    uuid(7a98c250-6808-11cf-b73b-00aa00b677a7),
    version(1.0)
]
interface INTERFACENAME
{
 
}
```

 

 




