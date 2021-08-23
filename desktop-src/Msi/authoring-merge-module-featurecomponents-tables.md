---
description: Se requiere una tabla FeatureComponents en blanco en cada módulo de combinación. Esta tabla vacía proporciona un esquema para la herramienta de combinación si el archivo .msi destino no tiene su propia tabla FeatureComponents.
ms.assetid: 19463fc7-8362-4943-8907-22c38f66fe25
title: Creación de características de módulo de mezclaComponentes Tablas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52b2da3e25d84f4f10edad6566edeba5a10d43c5617340d40c733aa23d31f4b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650305"
---
# <a name="authoring-merge-module-featurecomponents-tables"></a>Creación de características de módulo de mezclaComponentes Tablas

Se requiere [una tabla FeatureComponents](featurecomponents-table.md) en blanco en cada módulo de combinación. Esta tabla vacía proporciona un esquema para la herramienta de combinación si el archivo .msi destino no tiene su propia tabla FeatureComponents.

Si y solo si no hay ninguna tabla FeatureComponents en el archivo .msi destino, la herramienta de combinación usa la tabla en blanco proporcionada en el módulo. En este caso, la herramienta de combinación crea una tabla duplicada en el archivo .msi de destino y agrega filas que asocian los nuevos componentes del módulo de combinación a las características del paquete de instalación de la aplicación.

 

 



