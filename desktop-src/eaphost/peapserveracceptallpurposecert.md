---
title: PeapServerAcceptAllPurposeCert
description: La clave del Registro PeapServerAcceptAllPurposeCert determina si se aceptan certificados de uso completo para la autenticación peap.
ms.assetid: 59C58459-7735-4733-9F95-646864802D70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d568ef2cf3e7fd5eeeaa650e5e6e4fd32a8e1c8d6baa0ed91434a5c0aa60ee0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118784687"
---
# <a name="peapserveracceptallpurposecert"></a>PeapServerAcceptAllPurposeCert

La clave del Registro PeapServerAcceptAllPurposeCert determina si se aceptan certificados de uso completo para la autenticación peap.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   PeapServerAcceptAllPurposeCert = value
```

## <a name="remarks"></a>Observaciones

Se trata de **un valor \_ REG DWORD.**



| Value        | Descripción                                                                                                 |
|--------------|-------------------------------------------------------------------------------------------------------------|
| 1            | El servidor y el cliente aceptan certificados de uso general enviados por la otra parte para la autenticación EAP-TLS.       |
| Otros valores | El servidor y el cliente no aceptan certificados de uso general enviados por la otra parte para la autenticación EAP-TLS |



 

Si este valor del Registro no está presente, el servidor y el cliente aceptan certificados de uso general enviados por la otra parte para la autenticación PEAP.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[EapHost Registry Configuración](eaphost-registry-settings.md)
</dt> </dl>

 

 




