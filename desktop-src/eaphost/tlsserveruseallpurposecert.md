---
title: TlsServerUseAllPurposeCert
description: La clave del registro TlsServerUseAllPurposeCert determina si se usan certificados para la autenticación EAP-TLS.
ms.assetid: a672cecb-6bba-4ba6-b362-f6d5a220184b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b7cb767a8f6c8f40b377cca84d948b384170486
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "104358531"
---
# <a name="tlsserveruseallpurposecert"></a>TlsServerUseAllPurposeCert

La clave del registro TlsServerUseAllPurposeCert determina si se usan certificados para la autenticación EAP-TLS.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   TlsServerUseAllPurposeCert = value
```

## <a name="remarks"></a>Observaciones

Se trata de un valor de **Registro \_ DWORD** .



| Value        | Descripción                                                                                                      |
|--------------|------------------------------------------------------------------------------------------------------------------|
| 1            | Los certificados para todos los propósitos del almacén de certificados del cliente o del servidor se seleccionan para la autenticación PEAP.     |
| Otros valores | Los certificados de todos los propósitos del almacén de certificados del cliente o del servidor no se seleccionan para la autenticación PEAP. |



 

Si este valor del registro no está presente, se seleccionan los certificados de todos los propósitos en el almacén de certificados del cliente o del servidor para la autenticación EAP-TLS.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración del registro de EAPHost](eaphost-registry-settings.md)
</dt> </dl>

 

 




