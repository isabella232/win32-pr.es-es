---
title: Configuración de restaurar sistema
description: Restaurar sistema utiliza Instrumental de administración de Windows (WMI) para proporcionar una forma de configurar y usar su funcionalidad con scripts. Expone dos clases, SystemRestore y SystemRestoreConfig, en el \\ espacio de nombres predeterminado raíz.
ms.assetid: b510c5b7-71ec-47f9-b567-45fde8c79f57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 323f75cd80f7838e643922d8b9ffa7bf2b121945
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420953"
---
# <a name="configuring-system-restore"></a>Configuración de restaurar sistema

Restaurar sistema utiliza [instrumental de administración de Windows](/windows/desktop/WmiSdk/wmi-start-page) (WMI) para proporcionar una forma de configurar y usar su funcionalidad con scripts. Expone dos clases, [**SystemRestore**](systemrestore.md) y [**SystemRestoreConfig**](systemrestoreconfig.md), en el \\ espacio de nombres predeterminado raíz.

La clase [**SystemRestore**](systemrestore.md) proporciona métodos para las siguientes tareas:

-   Deshabilitación y habilitación de la supervisión
-   Enumerar los puntos de restauración disponibles
-   Iniciar una restauración en el sistema local
-   Recuperar el estado de la última restauración del sistema

La clase [**SystemRestoreConfig**](systemrestoreconfig.md) proporciona propiedades para controlar la frecuencia de creación de puntos de restauración programados y la cantidad de espacio en disco consumido por restaurar sistema en cada unidad.

Se puede tener acceso a ambas clases de forma remota mediante técnicas WMI estándar. Para obtener una descripción completa de WMI, consulte [instrumental de administración de Windows](/windows/desktop/WmiSdk/wmi-start-page).

 

 