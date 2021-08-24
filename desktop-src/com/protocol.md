---
title: Protocolo
description: Indica que esta clase OLE 2 se puede insertar en contenedores OLE 1.
ms.assetid: 320dff51-ac27-42f3-8c0f-353b29e289d9
keywords:
- Com de clave del Registro de protocolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7721e4f90a122fcbc519163d80c1e8e549f2b6aa05526d33d9693783abd1276a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130027"
---
# <a name="protocol"></a>Protocolo

Indica que esta clase OLE 2 se puede insertar en contenedores OLE 1.

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

## <a name="remarks"></a>Comentarios

La **entrada StdFileEditing especifica** información de compatibilidad de OLE 1. Solo debe estar presente si los objetos de esta clase se pueden insertar en contenedores OLE 1.

**Server** especifica la ruta de acceso completa a la aplicación de servidor OLE 2 y **Verbo** especifica los verbos. El verbo 0 es el verbo principal y los verbos adicionales se deben numerar consecutivamente.

 

 




