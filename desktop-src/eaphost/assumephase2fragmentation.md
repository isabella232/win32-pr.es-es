---
title: AssumePhase2Fragmentation
description: La clave del Registro AssumePhase2Fragmentation determina si el servidor y el cliente asumen la fragmentación de la fase 2.
ms.assetid: 3d6ececf-8871-4038-9706-4da57857d25a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b0fa35692ec3ac741e2bd2fdb43607dfe1cb948
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568893"
---
# <a name="assumephase2fragmentation"></a>AssumePhase2Fragmentation

La clave del Registro AssumePhase2Fragmentation determina si el servidor y el cliente asumen la fragmentación de la fase 2.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   AssumePhase2Fragmentation = value
```

## <a name="remarks"></a>Observaciones

Se trata de **un valor \_ REG DWORD.**



| Value   | Descripción                                                                                                  |
|---------|--------------------------------------------------------------------------------------------------------------|
| 0       | El servidor y el cliente asumen que la otra parte no es capaz de fragmentar la fase 2 durante la autenticación peap. |
| Distinto | El servidor y el cliente asumen que la otra parte es capaz de fragmentar la fase 2 durante la autenticación peap.     |



 

Si este valor del Registro no está presente, el servidor y el cliente asumen que la otra parte es capaz de fragmentar la fase 2 durante la autenticación PEAP.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[EapHost Registry Configuración](eaphost-registry-settings.md)
</dt> </dl>

 

 




