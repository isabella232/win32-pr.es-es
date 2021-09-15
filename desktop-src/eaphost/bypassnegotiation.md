---
title: BypassNegotiation
description: La clave del Registro BypassNegotiation determina si se produce la negociación de funcionalidades entre el servidor y el cliente o si se usan opciones configuradas previamente.
ms.assetid: 51e21e9c-d6cb-454b-9584-3f48d76a649a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9fdf883249fc5af7a37be83bb153a670295ba1d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568817"
---
# <a name="bypassnegotiation"></a>BypassNegotiation

La clave del Registro BypassNegotiation determina si se produce la negociación de funcionalidades entre el servidor y el cliente o si se usan opciones configuradas previamente.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   BypassNegotiation = value
```

## <a name="remarks"></a>Observaciones

Se trata de **un valor \_ REG DWORD.**



| Value   | Descripción                                                                                                                                                                                          |
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0       | Capacidades de EAP de negociación de servidor y cliente.                                                                                                                                                        |
| Distinto | El servidor y el cliente no negocian las funcionalidades de EAP. El servidor y el cliente usan el valor de clave del Registro [AssumePhase2Fragmentation](assumephase2fragmentation.md) para buscar las funcionalidades de la otra parte. |



 

Si este valor del Registro no está presente, el servidor y el cliente negocian las funcionalidades de EAP.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[EapHost Registry Configuración](eaphost-registry-settings.md)
</dt> </dl>

 

 




