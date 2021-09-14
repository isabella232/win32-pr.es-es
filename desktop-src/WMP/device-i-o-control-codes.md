---
title: Códigos de control de E/S de dispositivo
description: Códigos de control de E/S de dispositivo
ms.assetid: 46a5d166-ca8d-42df-9455-145332437153
keywords:
- Reproductor de Windows Media,códigos de control de E/S de dispositivo
- Reproductor de Windows Media,códigos de control
- Windows Archivos Administrador de dispositivos
- códigos de control de E/S de dispositivo
- códigos de control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69c00e235ce0f0e68e98f4f0e37221eac0903682
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068465"
---
# <a name="device-io-control-codes"></a>Códigos de control de E/S de dispositivo

Reproductor de Windows Media 10 o posterior define los Windows de control Administrador de dispositivos de E/S del dispositivo. La tabla siguiente contiene los códigos de control y sus descripciones.



| Código de control de E/S                      | Value      | Descripción                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **IOCTL \_ WMP \_ METADATA \_ ROUND \_ TRIP** | 0x31504d57 | Administra la transferencia de información sobre los cambios que se produjeron en los valores de metadatos. Consulte [Extensiones de dispositivo para la transferencia acelerada de metadatos.](device-extensions-for-accelerated-metadata-transfer.md)                                                                                                                                                                          |
| **EL DISPOSITIVO \_ IOCTL WMP \_ SE PUEDE \_ \_ SINCRONIZAR**     | 0x32504d57 | Indica si un dispositivo portátil admite la sincronización automática. Reproductor de Windows Media 10 o posterior no proporciona ningún búfer de entrada. El búfer de salida debe devolver un **valor DWORD.** Un valor de 1 significa que el dispositivo admite la sincronización. Un valor de 0 significa que el dispositivo no admite la sincronización automática.<br/> Vea Comentarios para obtener más información.<br/> |



 

## <a name="remarks"></a>Observaciones

Estos códigos de control se definen en wmpdevices.h.

Si el dispositivo no admite **IOCTL \_ WMP \_ DEVICE CAN \_ \_ SYNC**, Reproductor de Windows Media 10 o posterior supone que el dispositivo admite la sincronización automática. Tenga en cuenta que aunque este valor puede no permitir la sincronización automática, hay criterios adicionales que se usan para determinar si el dispositivo admite la sincronización automática.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Extensiones de dispositivo para la transferencia acelerada de metadatos**](device-extensions-for-accelerated-metadata-transfer.md)
</dt> <dt>

[**Reproductor de Windows Media**](windows-media-player.md)
</dt> </dl>

 

 





