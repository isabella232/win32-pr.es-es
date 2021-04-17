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
# <a name="authoring-merge-module-featurecomponents-tables"></a><span data-ttu-id="f3c60-104">Crear tablas FeatureComponents de módulo de combinación</span><span class="sxs-lookup"><span data-stu-id="f3c60-104">Authoring Merge Module FeatureComponents Tables</span></span>

<span data-ttu-id="f3c60-105">En cada módulo de combinación se requiere una [tabla FeatureComponents](featurecomponents-table.md) en blanco.</span><span class="sxs-lookup"><span data-stu-id="f3c60-105">A blank [FeatureComponents table](featurecomponents-table.md) is required in every merge module.</span></span> <span data-ttu-id="f3c60-106">Esta tabla vacía proporciona un esquema para la herramienta de combinación si el archivo. msi de destino no tiene su propia tabla FeatureComponents.</span><span class="sxs-lookup"><span data-stu-id="f3c60-106">This empty table provides a schema for the merge tool if the target .msi file does not have its own FeatureComponents table.</span></span>

<span data-ttu-id="f3c60-107">Si, y solo si, no hay ninguna tabla FeatureComponents en el archivo. msi de destino, la herramienta de combinación usa la tabla en blanco proporcionada en el módulo.</span><span class="sxs-lookup"><span data-stu-id="f3c60-107">If, and only if, there is no FeatureComponents table in the target .msi file does the merge tool use the blank table provided in the module.</span></span> <span data-ttu-id="f3c60-108">En este caso, la herramienta de combinación crea una tabla duplicada en el archivo. msi de destino y agrega las filas que asocian los nuevos componentes del módulo de combinación a las características del paquete de instalación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f3c60-108">In this case, the merge tool creates a duplicate table in the target .msi file and adds rows that associate the new components in the merge module to the features in the application's installation package.</span></span>

 

 



