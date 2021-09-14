---
title: Auto
description: Determina si el depurador se inicia automáticamente cuando se envía una notificación RPC COM.
ms.assetid: e05ae7cb-79d1-4543-aef3-9397548c2030
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23c7730c3c6e0fe9dc01b43a7c4f9621897f9f16
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360875"
---
# <a name="auto"></a>Auto

Determina si el depurador se inicia automáticamente cuando se envía una notificación RPC COM.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\DebugObjectRPCEnabled\AeDebug
   Auto = value
```

## <a name="remarks"></a>Observaciones

Se trata de **un valor REG \_ WORD.**



| Value | Descripción                    |
|-------|--------------------------------|
| 1     | Inicie automáticamente el depurador. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> <dt>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)
</dt> <dt>

[**ORPC \_ DBG \_ ALL**](orpc-dbg-all.md)
</dt> </dl>

 

 




