---
title: PeapServerUseAllPurposeCert
description: La clave del Registro PeapServerUseAllPurposeCert determina si se usan certificados de uso completo para la autenticación peap.
ms.assetid: e239fb88-4bf3-49b6-a95c-67a8c060a50d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a5086a0067bab70a0e222def34d1adf236b37127c0d1ff6c91ac83b8b28c73c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042823"
---
# <a name="peapserveruseallpurposecert"></a>PeapServerUseAllPurposeCert

La clave del Registro PeapServerUseAllPurposeCert determina si se usan certificados de uso completo para la autenticación peap.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   PeapServerUseAllPurposeCert = value
```

## <a name="remarks"></a>Comentarios

Se trata de **un valor \_ REG DWORD.**



| Valor        | Descripción                                                                                                      |
|--------------|------------------------------------------------------------------------------------------------------------------|
| 1            | Los certificados de uso completo del almacén de certificados del cliente o del servidor se seleccionan para la autenticación PEAP.     |
| Otros valores | Los certificados de uso completo del almacén de certificados del cliente o del servidor no están seleccionados para la autenticación PEAP. |



 

Si este valor del Registro no está presente, se seleccionan certificados de uso general en el almacén de certificados del cliente o del servidor para la autenticación PEAP.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[EapHost Registry Configuración](eaphost-registry-settings.md)
</dt> </dl>

 

 




