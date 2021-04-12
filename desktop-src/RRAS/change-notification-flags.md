---
title: Cambiar marcas de notificación
description: Cambiar marcas de notificación
ms.assetid: 1f1aef71-a2b7-49ad-a0bc-f61f10b701c9
keywords:
- Cambio
- Cambiar marcas de notificación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e6d3015be29c84b6b93b47b373d05f96f4388b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357176"
---
# <a name="change-notification-flags"></a>Cambiar marcas de notificación



| Constante                         | Value      | Descripción                                                                                                                                                           |
|----------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_tipos de \_ cambio de número RTM \_          | 3          | Especifica el número de tipos de cambios utilizados actualmente por el administrador de tablas de enrutamiento.                                                                            |
| tipo de cambio de RTM \_ \_ \_ All           | 0x0001     | Notifica al cliente cualquier cambio que se haya efectuado en un destino.                                                                                                                   |
| tipo de cambio de RTM \_ \_ \_ mejor          | 0x0002     | Notifica al cliente los cambios en la mejor ruta o cuando cambia la mejor ruta.                                                                                     |
| \_cambio de \_ \_ reenvío de tipos de RTM    | 0x0004     | Notifica al cliente los cambios de ruta más adecuados que afectan al reenvío (por ejemplo, los cambios en el próximo salto).                                                                      |
| RTM \_ notifica \_ solo \_ los \_ dests marcados | 0x00010000 | Notifica al cliente los cambios en los destinos que el cliente ha marcado. Si no se especifica esta marca, se envían los mensajes de notificación de cambios para todos los destinos. |



 

 

 




