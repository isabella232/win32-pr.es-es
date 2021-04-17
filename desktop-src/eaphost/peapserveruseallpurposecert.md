---
title: PeapServerUseAllPurposeCert
description: La clave del registro PeapServerUseAllPurposeCert determina si se usan certificados para la autenticación PEAP.
ms.assetid: e239fb88-4bf3-49b6-a95c-67a8c060a50d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc90f083f9020ad02960d7620a2ab54706df203e
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "104358538"
---
# <a name="peapserveruseallpurposecert"></a>PeapServerUseAllPurposeCert

La clave del registro PeapServerUseAllPurposeCert determina si se usan certificados para la autenticación PEAP.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   PeapServerUseAllPurposeCert = value
```

## <a name="remarks"></a>Observaciones

Se trata de un valor de **Registro \_ DWORD** .



| Value        | Descripción                                                                                                      |
|--------------|------------------------------------------------------------------------------------------------------------------|
| 1            | Los certificados para todos los propósitos del almacén de certificados del cliente o del servidor se seleccionan para la autenticación PEAP.     |
| Otros valores | Los certificados de todos los propósitos del almacén de certificados del cliente o del servidor no se seleccionan para la autenticación PEAP. |



 

Si este valor del registro no está presente, se seleccionan los certificados de todos los propósitos en el almacén de certificados del cliente o del servidor para la autenticación PEAP.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración del registro de EAPHost](eaphost-registry-settings.md)
</dt> </dl>

 

 




