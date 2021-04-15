---
title: PeapServerAcceptAllPurposeCert
description: La clave del registro PeapServerAcceptAllPurposeCert determina si se aceptan certificados para la autenticación PEAP.
ms.assetid: 59C58459-7735-4733-9F95-646864802D70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b291696c6bee90b4f980d8f96ad96faf40fe3376
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "105695518"
---
# <a name="peapserveracceptallpurposecert"></a>PeapServerAcceptAllPurposeCert

La clave del registro PeapServerAcceptAllPurposeCert determina si se aceptan certificados para la autenticación PEAP.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   PeapServerAcceptAllPurposeCert = value
```

## <a name="remarks"></a>Observaciones

Se trata de un valor de **Registro \_ DWORD** .



| Value        | Descripción                                                                                                 |
|--------------|-------------------------------------------------------------------------------------------------------------|
| 1            | El servidor y el cliente aceptan certificados para todos los fines enviados por la otra parte para la autenticación EAP-TLS.       |
| Otros valores | El servidor y el cliente no aceptan certificados para todos los fines enviados por la otra parte para la autenticación EAP-TLS |



 

Si este valor del registro no está presente, el servidor y el cliente aceptan los certificados de propósito único enviados por la otra parte para la autenticación PEAP.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración del registro de EAPHost](eaphost-registry-settings.md)
</dt> </dl>

 

 




