---
description: En cada módulo de combinación se requiere una tabla FeatureComponents en blanco. Esta tabla vacía proporciona un esquema para la herramienta de combinación si el archivo. msi de destino no tiene su propia tabla FeatureComponents.
ms.assetid: 19463fc7-8362-4943-8907-22c38f66fe25
title: Crear tablas FeatureComponents de módulo de combinación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3522f32f91a66df93e9096bf9c528f8d00e11f6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667035"
---
# <a name="authoring-merge-module-featurecomponents-tables"></a>Crear tablas FeatureComponents de módulo de combinación

En cada módulo de combinación se requiere una [tabla FeatureComponents](featurecomponents-table.md) en blanco. Esta tabla vacía proporciona un esquema para la herramienta de combinación si el archivo. msi de destino no tiene su propia tabla FeatureComponents.

Si, y solo si, no hay ninguna tabla FeatureComponents en el archivo. msi de destino, la herramienta de combinación usa la tabla en blanco proporcionada en el módulo. En este caso, la herramienta de combinación crea una tabla duplicada en el archivo. msi de destino y agrega las filas que asocian los nuevos componentes del módulo de combinación a las características del paquete de instalación de la aplicación.

 

 



