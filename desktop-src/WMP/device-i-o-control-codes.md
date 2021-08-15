---
title: Códigos de control de E/S de dispositivo
description: Códigos de control de E/S de dispositivo
ms.assetid: 46a5d166-ca8d-42df-9455-145332437153
keywords:
- Reproductor de Windows Media,códigos de control de E/S de dispositivo
- Reproductor de Windows Media,códigos de control
- Windows Media Administrador de dispositivos
- códigos de control de E/S de dispositivo
- códigos de control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63d610b396125cf190764b53106ca6535a214e2c8166f4e69de884c113fd77ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117935854"
---
# <a name="device-io-control-codes"></a>Códigos de control de E/S de dispositivo

Reproductor de Windows Media 10 o posterior define códigos de control de E/S Administrador de dispositivos dispositivo Windows Media. La tabla siguiente contiene los códigos de control y sus descripciones.



| Código de control de E/S                      | Valor      | Descripción                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **IOCTL \_ WMP \_ METADATA \_ ROUND \_ TRIP** | 0x31504d57 | Administra la transferencia de información sobre los cambios que se produjeron en los valores de metadatos. Consulte [Extensiones de dispositivo para la transferencia acelerada de metadatos.](device-extensions-for-accelerated-metadata-transfer.md)                                                                                                                                                                          |
| **EL DISPOSITIVO \_ IOCTL WMP \_ PUEDE \_ \_ SINCRONIZARSE**     | 0x32504d57 | Indica si un dispositivo portátil admite la sincronización automática. Reproductor de Windows Media 10 o posterior no proporciona ningún búfer de entrada. El búfer de salida debe devolver un **valor DWORD.** Un valor de 1 significa que el dispositivo admite la sincronización. Un valor de 0 significa que el dispositivo no admite la sincronización automática.<br/> Vea Comentarios para obtener más información.<br/> |



 

## <a name="remarks"></a>Comentarios

Estos códigos de control se definen en wmpdevices.h.

Si el dispositivo no admite **IOCTL \_ WMP \_ DEVICE CAN \_ \_ SYNC**, Reproductor de Windows Media 10 o posterior supone que el dispositivo admite la sincronización automática. Tenga en cuenta que aunque este valor puede no permitir la sincronización automática, hay criterios adicionales que se usan para determinar si el dispositivo admite la sincronización automática.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Extensiones de dispositivo para la transferencia acelerada de metadatos**](device-extensions-for-accelerated-metadata-transfer.md)
</dt> <dt>

[**Reproductor de Windows Media**](windows-media-player.md)
</dt> </dl>

 

 





