---
title: BypassNegotiation
description: La clave del registro BypassNegotiation determina si se produce la negociación de funciones entre el servidor y el cliente, o si se usan los valores preconfigurados.
ms.assetid: 51e21e9c-d6cb-454b-9584-3f48d76a649a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9fdf883249fc5af7a37be83bb153a670295ba1d
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "104420047"
---
# <a name="bypassnegotiation"></a>BypassNegotiation

La clave del registro BypassNegotiation determina si se produce la negociación de funciones entre el servidor y el cliente, o si se usan los valores preconfigurados.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   BypassNegotiation = value
```

## <a name="remarks"></a>Observaciones

Se trata de un valor de **Registro \_ DWORD** .



| Value   | Descripción                                                                                                                                                                                          |
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0       | El servidor y el cliente negocian las capacidades de EAP.                                                                                                                                                        |
| distinto | El servidor y el cliente no negocian las funcionalidades de EAP. El servidor y el cliente usan el valor de la clave del registro [AssumePhase2Fragmentation](assumephase2fragmentation.md) para encontrar las capacidades de la otra parte. |



 

Si este valor del registro no está presente, el servidor y el cliente negocian las capacidades de EAP.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración del registro de EAPHost](eaphost-registry-settings.md)
</dt> </dl>

 

 




