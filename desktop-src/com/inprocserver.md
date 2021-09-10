---
title: InprocServer
description: Especifica la ruta de acceso al archivo DLL del servidor en proceso.
ms.assetid: f14cc8f7-e93e-4db8-8b0d-ea77a6301f33
keywords:
- Com de clave del Registro InprocServer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5682693d711f734bbc60def8a711f11e2bad0ef9
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369464"
---
# <a name="inprocserver"></a>InprocServer

Especifica la ruta de acceso al archivo DLL del servidor en proceso.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocServer
         (Default) = path
```

## <a name="remarks"></a>Observaciones

La **entrada InprocServer** es relativamente poco frecuente para las clases insertables.

Los servidores en proceso se registran actualmente mediante la entrada del Registro **InprocServer.** Los servidores en proceso de 32 y 64 bits deben usar la [**entrada InprocServer32.**](inprocserver32.md) Si un contenedor busca en el Registro un servidor en proceso, la versión de 16 bits tiene prioridad con un contenedor de 16 bits y la versión de 32 bits tiene prioridad con un contenedor de 32 bits.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**InprocServer32**](inprocserver32.md)
</dt> </dl>

 

 




