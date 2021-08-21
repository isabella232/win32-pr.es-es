---
title: TlsServerUseAllPurposeCert
description: La clave del Registro TlsServerUseAllPurposeCert determina si se usan certificados de uso completo para la autenticación EAP-TLS.
ms.assetid: a672cecb-6bba-4ba6-b362-f6d5a220184b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af2f9d47b4e80409c27c71fe3655a1d3266571e0f8a8dd757e5334b0ef9fec40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118085700"
---
# <a name="tlsserveruseallpurposecert"></a>TlsServerUseAllPurposeCert

La clave del Registro TlsServerUseAllPurposeCert determina si se usan certificados de uso completo para la autenticación EAP-TLS.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   TlsServerUseAllPurposeCert = value
```

## <a name="remarks"></a>Comentarios

Se trata de **un valor \_ REG DWORD.**



| Valor        | Descripción                                                                                                      |
|--------------|------------------------------------------------------------------------------------------------------------------|
| 1            | Los certificados de uso completo del almacén de certificados del cliente o del servidor se seleccionan para la autenticación PEAP.     |
| Otros valores | Los certificados de uso completo del almacén de certificados del cliente o del servidor no están seleccionados para la autenticación PEAP. |



 

Si este valor del Registro no está presente, se seleccionan certificados de uso general en el almacén de certificados del cliente o del servidor para la autenticación EAP-TLS.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[EapHost Registry Configuración](eaphost-registry-settings.md)
</dt> </dl>

 

 




