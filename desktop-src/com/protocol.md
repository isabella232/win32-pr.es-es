---
title: Protocolo
description: Indica que esta clase OLE 2 se puede insertar en contenedores OLE 1.
ms.assetid: 320dff51-ac27-42f3-8c0f-353b29e289d9
keywords:
- Com de clave del Registro de protocolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 176cb3fce826a6416270fc35a902621521341e6a
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369480"
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

## <a name="remarks"></a>Observaciones

La **entrada StdFileEditing especifica** información de compatibilidad de OLE 1. Solo debe estar presente si los objetos de esta clase se pueden insertar en contenedores OLE 1.

**Server** especifica la ruta de acceso completa a la aplicación de servidor OLE 2 y **Verbo** especifica los verbos. El verbo 0 es el verbo principal y los verbos adicionales se deben numerar consecutivamente.

 

 




