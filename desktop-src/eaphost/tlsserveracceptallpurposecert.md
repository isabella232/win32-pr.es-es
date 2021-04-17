---
title: TlsServerAcceptAllPurposeCert
description: La clave del registro TlsServerAcceptAllPurposeCert determina si se aceptan certificados de todos los propósitos para la autenticación EAP-TLS.
ms.assetid: F0881397-5D8C-4C8F-8EB5-6D59454C55B7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6561418d8d9cb06fb9618e6b93189cbd28e408
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "105665769"
---
# <a name="tlsserveracceptallpurposecert"></a>TlsServerAcceptAllPurposeCert

La clave del registro TlsServerAcceptAllPurposeCert determina si se aceptan certificados de todos los propósitos para la autenticación EAP-TLS.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   TlsServerAcceptAllPurposeCert = value
```

## <a name="remarks"></a>Observaciones

Se trata de un valor de **Registro \_ DWORD** .



| Value        | Descripción                                                                                                 |
|--------------|-------------------------------------------------------------------------------------------------------------|
| 1            | El servidor y el cliente aceptan certificados para todos los fines enviados por la otra parte para la autenticación EAP-TLS.       |
| Otros valores | El servidor y el cliente no aceptan certificados para todos los fines enviados por la otra parte para la autenticación EAP-TLS |



 

Si este valor del registro no está presente, el servidor y el cliente aceptan los certificados de propósito único enviados por la otra entidad para la autenticación EAP-TLS.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración del registro de EAPHost](eaphost-registry-settings.md)
</dt> </dl>

 

 




