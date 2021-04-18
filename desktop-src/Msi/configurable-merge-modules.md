---
description: Los módulos de fusión mediante combinación (archivos. MSM) se pueden crear para contener atributos que son configurables por el consumidor del módulo de combinación.
ms.assetid: 461436f0-3a91-4a49-934a-f975bf13df40
title: Módulos de combinación configurables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 716688d947ae84279dc3409bf97abe4eb58a69d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669852"
---
# <a name="configurable-merge-modules"></a>Módulos de combinación configurables

Los módulos de fusión mediante combinación (archivos. MSM) se pueden crear para contener atributos que son configurables por el consumidor del módulo de combinación. Esto permite configurar el módulo de fusión mediante combinación en el momento en que el paquete de instalación y el módulo se combinan e instalan por el usuario final. Los módulos de combinación configurables requieren Mergemod.dll versión 2,0, pero se pueden ejecutar en cualquier versión de la Windows Installer.

La implementación de módulos de combinación configurables se compone de dos partes. En primer lugar, al crear el módulo de combinación (archivo. MSM), el autor del módulo de combinación agrega información a la base de datos del módulo que especifica qué elementos se pueden modificar y cómo puede configurar estos elementos el usuario del módulo. El autor agrega entradas a las [tablas de base de datos del módulo de combinación](merge-module-database-tables.md) que están reservadas para la información configurable (tabla[ModuleConfiguration](moduleconfiguration-table.md) y [tabla ModuleSubstitution](modulesubstitution-table.md)), actualiza la [ \_ tabla de validación](-validation-table.md)y agrega entradas para las tablas del módulo de combinación que se pueden configurar a la [tabla ModuleIgnoreTable](moduleignoretable-table.md). Las adiciones a la tabla ModuleIgnore son necesarias para que el módulo sea compatible con las versiones de Mergemod.dll anteriores a 2,0.

En segundo lugar, al combinar el módulo en un paquete de instalación (archivo. msi), el usuario final del módulo usa una herramienta de combinación. La herramienta de combinación llama Mergemod.dll para exponer la información de configuración del módulo a una herramienta de configuración de cliente. La herramienta de configuración puede interactuar con el usuario final, pero no es necesario exponer todas las opciones de configuración posibles. Si el usuario declina proporcionar una selección para un elemento configurable, el módulo puede proporcionar un valor predeterminado. Una vez que el usuario da su selección a la herramienta de configuración, la herramienta de combinación llama a Mergemod.dll para realizar la combinación.

Los módulos de combinación configurables son totalmente compatibles con las herramientas anteriores a Mergemod.dll versión 2,0. En estos casos, la herramienta utiliza los valores predeterminados en el módulo.

Para obtener más información, vea [uso de módulos de combinación configurables](using-configurable-merge-modules.md).

 

 



