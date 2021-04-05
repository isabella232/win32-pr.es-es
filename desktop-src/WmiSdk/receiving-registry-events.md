---
description: El proveedor del registro del sistema intenta enviar una notificación para cada evento que se produce.
ms.assetid: 51ef0ccb-02d5-4dac-9c71-a7f4e25a0d00
ms.tgt_platform: multiple
title: Recibir eventos del registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87f0da8c039f83e3d4eb1f51d6b6707d0edd6b3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082395"
---
# <a name="receiving-registry-events"></a>Recibir eventos del registro

El proveedor del registro del sistema intenta enviar una notificación para cada evento que se produce. Sin embargo, el proveedor del registro del sistema no garantiza que el consumidor reciba todos los eventos o todos ellos. La excepción es que el proveedor del registro del sistema garantiza que un consumidor recibirá una notificación por cada registro de eventos.

Por ejemplo, supongamos que un consumidor se registra para dos eventos de cambio de árbol y solicita una notificación para las instancias de [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) . Cada registro tiene el mismo valor de Hive (subárbol) pero un valor de RootPath diferente. Si las claves en ambas rutas cambian varias veces, el proveedor del registro del sistema garantiza que el consumidor recibirá una notificación para cada ruta de acceso. Dependiendo del tiempo de respuesta del registro y del proveedor del registro del sistema, el consumidor puede recibir tantas notificaciones como repeticiones de eventos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registrar eventos del registro del sistema](registering-for-system-registry-events.md)
</dt> </dl>

 

 
