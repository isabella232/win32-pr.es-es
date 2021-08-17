---
title: Cambiar marcas de notificación
description: Cambiar marcas de notificación
ms.assetid: 1f1aef71-a2b7-49ad-a0bc-f61f10b701c9
keywords:
- Change
- Cambiar marcas de notificación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f5311e3313bf23c92972395143d288483181e7a69212115082a2f150d7d1bb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791839"
---
# <a name="change-notification-flags"></a>Cambiar marcas de notificación



| Constante                         | Value      | Descripción                                                                                                                                                           |
|----------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TIPOS DE CAMBIO NUM DE RTM \_ \_ \_          | 3          | Especifica el número de tipos de cambio que usa actualmente el administrador de tablas de enrutamiento.                                                                            |
| TIPO DE \_ CAMBIO RTM \_ \_ ALL           | 0x0001     | Notifica al cliente cualquier cambio en un destino.                                                                                                                   |
| MEJOR CAMBIO \_ DE \_ TIPO DE \_ RTM          | 0x0002     | Notifica al cliente los cambios en la mejor ruta o cuando cambia la mejor ruta.                                                                                     |
| REENVÍO DE TIPO \_ \_ DE CAMBIO \_ DE RTM    | 0x0004     | Notifica al cliente los mejores cambios de ruta que afectan al reenvío (por ejemplo, los cambios de próximo salto).                                                                      |
| RTM \_ NOTIFY \_ ONLY \_ MARKED \_ DESTS | 0x00010000 | Notifica al cliente los cambios en los destinos que el cliente ha marcado. Si no se especifica esta marca, se envían mensajes de notificación de cambio para todos los destinos. |



 

 

 




