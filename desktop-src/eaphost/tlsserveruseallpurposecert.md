---
title: TlsServerUseAllPurposeCert
description: La clave del Registro TlsServerUseAllPurposeCert determina si se usan certificados de uso completo para la autenticación EAP-TLS.
ms.assetid: a672cecb-6bba-4ba6-b362-f6d5a220184b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b7cb767a8f6c8f40b377cca84d948b384170486
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127358998"
---
# <a name="tlsserveruseallpurposecert"></a>TlsServerUseAllPurposeCert

La clave del Registro TlsServerUseAllPurposeCert determina si se usan certificados de uso completo para la autenticación EAP-TLS.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   TlsServerUseAllPurposeCert = value
```

## <a name="remarks"></a>Observaciones

Se trata de **un valor \_ REG DWORD.**



| Value        | Descripción                                                                                                      |
|--------------|------------------------------------------------------------------------------------------------------------------|
| 1            | Los certificados de uso completo del almacén de certificados del cliente o del servidor se seleccionan para la autenticación PEAP.     |
| Otros valores | Los certificados de uso completo del almacén de certificados del cliente o del servidor no están seleccionados para la autenticación PEAP. |



 

Si este valor del Registro no está presente, se seleccionan certificados de uso general en el almacén de certificados del cliente o del servidor para la autenticación EAP-TLS.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[EapHost Registry Configuración](eaphost-registry-settings.md)
</dt> </dl>

 

 




