---
title: Códigos de control de e/s de dispositivo
description: Códigos de control de e/s de dispositivo
ms.assetid: 46a5d166-ca8d-42df-9455-145332437153
keywords:
- Media Player de Windows, códigos de control de e/s de dispositivo
- Media Player de Windows, códigos de control
- Administrador de dispositivos de Windows Media
- códigos de control de e/s de dispositivo
- códigos de control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69c00e235ce0f0e68e98f4f0e37221eac0903682
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695399"
---
# <a name="device-io-control-codes"></a>Códigos de control de e/s de dispositivo

Windows Media Player 10 o posterior define los códigos de control de e/s de dispositivo de Windows Media Administrador de dispositivos. La tabla siguiente contiene los códigos de control y sus descripciones.



| Código de control de e/s                      | Value      | Descripción                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_viaje de \_ ida y \_ vuelta de metadatos de ioctl WMP \_** | 0x31504d57 | Administra la transferencia de información sobre los cambios que se produjeron en los valores de metadatos. Consulte [extensiones de dispositivo para la transferencia de metadatos acelerada](device-extensions-for-accelerated-metadata-transfer.md).                                                                                                                                                                          |
| **se \_ \_ \_ puede \_ sincronizar el dispositivo WMP de ioctl**     | 0x32504d57 | Indica si un dispositivo portátil admite la sincronización automática. Windows Media Player 10 o posterior no proporciona ningún búfer de entrada. El búfer de salida debe devolver un valor **DWORD** . Un valor de 1 significa que el dispositivo admite la sincronización. Un valor de 0 significa que el dispositivo no admite la sincronización automática.<br/> Vea Comentarios para obtener más información.<br/> |



 

## <a name="remarks"></a>Observaciones

Estos códigos de control se definen en wmpdevices. h.

Si el dispositivo no es compatible con el dispositivo WMP de IOCTL que se **\_ \_ \_ puede \_ sincronizar**, Windows Media Player 10 o posterior supone que el dispositivo admite la sincronización automática. Tenga en cuenta que, aunque este valor puede impedir la sincronización automática, se usan criterios adicionales para determinar si el dispositivo admite la sincronización automática.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Extensiones de dispositivo para la transferencia de metadatos acelerada**](device-extensions-for-accelerated-metadata-transfer.md)
</dt> <dt>

[**Reproductor de Windows Media**](windows-media-player.md)
</dt> </dl>

 

 





