---
title: PeapServerAcceptAllPurposeCert
description: La clave del Registro PeapServerAcceptAllPurposeCert determina si se aceptan certificados de uso completo para la autenticación peap.
ms.assetid: 59C58459-7735-4733-9F95-646864802D70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b291696c6bee90b4f980d8f96ad96faf40fe3376
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127240777"
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

 

 




