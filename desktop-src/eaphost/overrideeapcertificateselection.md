---
title: OverrideEAPCertificateSelection
description: La clave del registro OverrideEAPCertificateSelection determina si el cliente invalidará el comportamiento de la selección de certificados de tarjeta inteligente predeterminada y proporcionará al usuario más certificados entre los que elegir.
ms.assetid: 469FECA9-FF2A-46B1-9370-0FF28EF2FB33
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d958eeeffba96e7a060ee4dd3edaf8a9935a15d1
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "103904328"
---
# <a name="overrideeapcertificateselection"></a>OverrideEAPCertificateSelection

La clave del registro OverrideEAPCertificateSelection determina si el cliente invalidará el comportamiento de la selección de certificados de tarjeta inteligente predeterminada y proporcionará al usuario más certificados entre los que elegir.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   OverrideEAPCertificateSelection = value
```

## <a name="remarks"></a>Observaciones

Se trata de un valor **\_ binario de registro** .



| Value | Descripción                                                                                                                                                                                          |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x000 | No invalide el comportamiento predeterminado.                                                                                                                                                                |
| 0x001 | Elija el último certificado adjunto de la tarjeta inteligente.                                                                                                                                            |
| 0x010 | Muestra todos los certificados en la interfaz de usuario de selección de certificados de la tarjeta inteligente.                                                                                                                          |
| 0x100 | Muestra todos los certificados en la interfaz de usuario de selección de certificados del registro.                                                                                                                            |
| 0x101 | Muestra todos los certificados de la interfaz de usuario de selección de certificados del registro y el último certificado adjunto de la tarjeta inteligente. Muestra el último certificado adjunto de la tarjeta inteligente como seleccionado. |
| 0x110 | Muestra todos los certificados en la interfaz de usuario de selección de certificados del registro y la tarjeta inteligente.                                                                                                         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración del registro de EAPHost](eaphost-registry-settings.md)
</dt> </dl>

 

 




