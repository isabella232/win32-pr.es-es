---
title: OverrideEAPCertificateSelection
description: La clave del Registro OverrideEAPCertificateSelection determina si el cliente invalidará el comportamiento predeterminado de selección de certificados de tarjeta inteligente y proporcionará al usuario más certificados entre los que elegir.
ms.assetid: 469FECA9-FF2A-46B1-9370-0FF28EF2FB33
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d93efec6968fb27b0d27d88c696101815f0b48c36c100f78092d5b559d4c0f7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118085919"
---
# <a name="overrideeapcertificateselection"></a>OverrideEAPCertificateSelection

La clave del Registro OverrideEAPCertificateSelection determina si el cliente invalidará el comportamiento predeterminado de selección de certificados de tarjeta inteligente y proporcionará al usuario más certificados entre los que elegir.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   OverrideEAPCertificateSelection = value
```

## <a name="remarks"></a>Comentarios

Se trata de **un valor \_ REG BINARY.**



| Valor | Descripción                                                                                                                                                                                          |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x000 | No invalide el comportamiento predeterminado.                                                                                                                                                                |
| 0x001 | Elija el último certificado adjunto de la tarjeta inteligente.                                                                                                                                            |
| 0x010 | Muestra todos los certificados de la interfaz de usuario de selección de certificados de la tarjeta inteligente.                                                                                                                          |
| 0x100 | Muestra todos los certificados de la interfaz de usuario de selección de certificados del Registro.                                                                                                                            |
| 0x101 | Muestra todos los certificados de la interfaz de usuario de selección de certificados del registro y el último certificado adjunto de la tarjeta inteligente. Muestra el último certificado adjunto de la tarjeta inteligente como seleccionado. |
| 0x110 | Muestra todos los certificados en la interfaz de usuario de selección de certificados del Registro y la tarjeta inteligente.                                                                                                         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[EapHost Registry Configuración](eaphost-registry-settings.md)
</dt> </dl>

 

 




