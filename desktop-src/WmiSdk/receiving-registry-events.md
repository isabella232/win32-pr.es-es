---
description: El proveedor del Registro del sistema intenta enviar una notificación por cada evento que se produzca.
ms.assetid: 51ef0ccb-02d5-4dac-9c71-a7f4e25a0d00
ms.tgt_platform: multiple
title: Recepción de eventos del Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d6f3c8f39be30beeb64e7c8d8ff7f1bacfba8a47b7f4bd0c70e7cf638bf726e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118817461"
---
# <a name="receiving-registry-events"></a>Recepción de eventos del Registro

El proveedor del Registro del sistema intenta enviar una notificación por cada evento que se produzca. Sin embargo, el proveedor del Registro del sistema no garantiza que el consumidor reciba todos o ninguno de los eventos. La excepción es que el proveedor del Registro del sistema garantiza que un consumidor recibirá una notificación por cada registro de eventos.

Por ejemplo, suponga que un consumidor se registra para dos eventos de cambio de árbol y solicita una notificación para las instancias [**de RegistryTreeChangeEvent.**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) Cada registro tiene el mismo valor de Hive (subárbol), pero un valor rootPath diferente. Si las claves de ambas rutas de acceso cambian varias veces, el proveedor del Registro del sistema garantiza que el consumidor recibirá una notificación para cada ruta de acceso. En función del tiempo de respuesta del registro y del proveedor del Registro del sistema, el consumidor puede recibir tantas notificaciones como se produzcan eventos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registro de eventos del Registro del sistema](registering-for-system-registry-events.md)
</dt> </dl>

 

 
