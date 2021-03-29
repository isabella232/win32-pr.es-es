---
title: InprocServer
description: Especifica la ruta de acceso al archivo DLL de servidor en proceso.
ms.assetid: f14cc8f7-e93e-4db8-8b0d-ea77a6301f33
keywords:
- Clave del registro de InprocServer COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5682693d711f734bbc60def8a711f11e2bad0ef9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994215"
---
# <a name="inprocserver"></a>InprocServer

Especifica la ruta de acceso al archivo DLL de servidor en proceso.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocServer
         (Default) = path
```

## <a name="remarks"></a>Observaciones

La entrada **InprocServer** es relativamente inusual para las clases que se van a insertar.

Los servidores en proceso están registrados actualmente mediante la entrada del registro **InprocServer** . Los servidores en proceso de 32 y 64 bits deben usar la entrada [**InProcServer32**](inprocserver32.md) . Si un contenedor está buscando en el registro un servidor en proceso, la versión de 16 bits tiene prioridad con un contenedor de 16 bits y la versión de 32 bits tiene prioridad con un contenedor de 32 bits.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**InprocServer32**](inprocserver32.md)
</dt> </dl>

 

 




