---
description: Se requiere una tabla FeatureComponents en blanco en cada módulo de combinación. Esta tabla vacía proporciona un esquema para la herramienta de combinación si el archivo .msi destino no tiene su propia tabla FeatureComponents.
ms.assetid: 19463fc7-8362-4943-8907-22c38f66fe25
title: Creación de características de módulo de mezclaComponentes tablas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3522f32f91a66df93e9096bf9c528f8d00e11f6c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159044"
---
# <a name="authoring-merge-module-featurecomponents-tables"></a>Creación de características de módulo de mezclaComponentes tablas

Se requiere [una tabla FeatureComponents](featurecomponents-table.md) en blanco en cada módulo de combinación. Esta tabla vacía proporciona un esquema para la herramienta de combinación si el archivo .msi destino no tiene su propia tabla FeatureComponents.

Si y solo si no hay ninguna tabla FeatureComponents en el archivo .msi destino, la herramienta de combinación usa la tabla en blanco proporcionada en el módulo. En este caso, la herramienta de combinación crea una tabla duplicada en el archivo .msi de destino y agrega filas que asocian los nuevos componentes del módulo de mezcla a las características del paquete de instalación de la aplicación.

 

 



