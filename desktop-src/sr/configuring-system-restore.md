---
title: Configuración de Restaurar sistema
description: Restaurar sistema usa Windows Management Instrumentation (WMI) para proporcionar una manera de configurar y usar su funcionalidad mediante scripts. Expone dos clases, SystemRestore y SystemRestoreConfig, en el espacio de \\ nombres predeterminado raíz.
ms.assetid: b510c5b7-71ec-47f9-b567-45fde8c79f57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac5627233d22025d8cead43f9fc31323ae13f85ff2ec7bde0ebfa07e171c1f82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968054"
---
# <a name="configuring-system-restore"></a>Configuración de Restaurar sistema

Restaurar sistema usa [Windows Management Instrumentation](/windows/desktop/WmiSdk/wmi-start-page) (WMI) para proporcionar una manera de configurar y usar su funcionalidad mediante scripts. Expone dos clases, [**SystemRestore**](systemrestore.md) y [**SystemRestoreConfig,**](systemrestoreconfig.md)en el espacio de \\ nombres predeterminado raíz.

La [**clase SystemRestore**](systemrestore.md) proporciona métodos para las tareas siguientes:

-   Deshabilitación y habilitación de la supervisión
-   Enumeración de los puntos de restauración disponibles
-   Inicio de una restauración en el sistema local
-   Recuperación del estado de la última restauración del sistema

La [**clase SystemRestoreConfig**](systemrestoreconfig.md) proporciona propiedades para controlar la frecuencia de creación de puntos de restauración programados y la cantidad de espacio en disco consumido por Restaurar sistema en cada unidad.

Se puede acceder a ambas clases de forma remota mediante técnicas WMI estándar. Para obtener una descripción completa de WMI, [vea Windows Management Instrumentation](/windows/desktop/WmiSdk/wmi-start-page).

 

 