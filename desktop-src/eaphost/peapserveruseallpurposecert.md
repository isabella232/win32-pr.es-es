---
title: PeapServerUseAllPurposeCert
description: La clave del Registro PeapServerUseAllPurposeCert determina si se usan certificados de uso completo para la autenticación peap.
ms.assetid: e239fb88-4bf3-49b6-a95c-67a8c060a50d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc90f083f9020ad02960d7620a2ab54706df203e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127240776"
---
# <a name="peapserveruseallpurposecert"></a>PeapServerUseAllPurposeCert

La clave del Registro PeapServerUseAllPurposeCert determina si se usan certificados de uso completo para la autenticación peap.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   PeapServerUseAllPurposeCert = value
```

## <a name="remarks"></a>Observaciones

Se trata de **un valor \_ REG DWORD.**



| Value        | Descripción                                                                                                      |
|--------------|------------------------------------------------------------------------------------------------------------------|
| 1            | Los certificados de uso completo del almacén de certificados del cliente o del servidor se seleccionan para la autenticación PEAP.     |
| Otros valores | Los certificados de uso completo del almacén de certificados del cliente o del servidor no están seleccionados para la autenticación PEAP. |



 

Si este valor del Registro no está presente, se seleccionan certificados de uso general en el almacén de certificados del cliente o del servidor para la autenticación PEAP.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[EapHost Registry Configuración](eaphost-registry-settings.md)
</dt> </dl>

 

 




