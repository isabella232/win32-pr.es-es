---
title: Automático
description: Determina si el depurador se inicia automáticamente cuando se envía una notificación RPC de COM.
ms.assetid: e05ae7cb-79d1-4543-aef3-9397548c2030
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23c7730c3c6e0fe9dc01b43a7c4f9621897f9f16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704803"
---
# <a name="auto"></a>Automático

Determina si el depurador se inicia automáticamente cuando se envía una notificación RPC de COM.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\DebugObjectRPCEnabled\AeDebug
   Auto = value
```

## <a name="remarks"></a>Observaciones

Se trata de un valor de **\_ palabra de registro** .



| Value | Descripción                    |
|-------|--------------------------------|
| 1     | Iniciar el depurador automáticamente. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> <dt>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)
</dt> <dt>

[**ORPC \_ dbg \_ All**](orpc-dbg-all.md)
</dt> </dl>

 

 




