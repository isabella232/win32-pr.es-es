---
title: TlsServerAcceptAllPurposeCert
description: La clave del Registro TlsServerAcceptAllPurposeCert determina si se aceptan certificados de uso completo para la autenticación EAP-TLS.
ms.assetid: F0881397-5D8C-4C8F-8EB5-6D59454C55B7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 804185773a948299aed3d8b8e2f581d8d8355d112720b66e860bd1f00b7fc3d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118085757"
---
# <a name="tlsserveracceptallpurposecert"></a>TlsServerAcceptAllPurposeCert

La clave del Registro TlsServerAcceptAllPurposeCert determina si se aceptan certificados de uso completo para la autenticación EAP-TLS.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   TlsServerAcceptAllPurposeCert = value
```

## <a name="remarks"></a>Comentarios

Se trata de **un valor \_ REG DWORD.**



| Valor        | Descripción                                                                                                 |
|--------------|-------------------------------------------------------------------------------------------------------------|
| 1            | El servidor y el cliente aceptan certificados de uso general enviados por la otra parte para la autenticación EAP-TLS.       |
| Otros valores | El servidor y el cliente no aceptan certificados de uso general enviados por la otra parte para la autenticación EAP-TLS |



 

Si este valor del Registro no está presente, el servidor y el cliente aceptan certificados de uso general enviados por la otra parte para la autenticación EAP-TLS.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[EapHost Registry Configuración](eaphost-registry-settings.md)
</dt> </dl>

 

 




