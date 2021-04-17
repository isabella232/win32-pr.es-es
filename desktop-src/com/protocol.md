---
title: Protocolo
description: Indica que esta clase OLE 2 se va a insertar en contenedores OLE 1.
ms.assetid: 320dff51-ac27-42f3-8c0f-353b29e289d9
keywords:
- Clave del registro de protocolo COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 176cb3fce826a6416270fc35a902621521341e6a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714205"
---
# <a name="protocol"></a>Protocolo

Indica que esta clase OLE 2 se va a insertar en contenedores OLE 1.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   {ProgID}
      Protocol
         StdFileEditing
            Server = path
            Verb
               0 = verb1
               1 = verb2
               ...
```

## <a name="remarks"></a>Observaciones

La entrada **StdFileEditing** especifica la información de compatibilidad de OLE 1. Debe estar presente solo si los objetos de esta clase se pueden insertar en contenedores OLE 1.

**Server** especifica la ruta de acceso completa a la aplicación de servidor OLE 2 y **Verb** especifica los verbos. El verbo 0 es el verbo principal y los verbos adicionales se deben numerar consecutivamente.

 

 




