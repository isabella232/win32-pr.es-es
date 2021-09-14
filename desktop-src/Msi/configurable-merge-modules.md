---
description: Los módulos de combinación (archivos .msm) se pueden crear para contener atributos que el consumidor puede configurar del módulo de combinación.
ms.assetid: 461436f0-3a91-4a49-934a-f975bf13df40
title: Módulos de combinación configurables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 716688d947ae84279dc3409bf97abe4eb58a69d0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158810"
---
# <a name="configurable-merge-modules"></a>Módulos de combinación configurables

Los módulos de combinación (archivos .msm) se pueden crear para contener atributos que el consumidor puede configurar del módulo de combinación. Esto permite que el módulo de mezcla se configure en el momento en que el usuario final combina e instala el paquete de instalación y el módulo. Los módulos de combinación configurables Mergemod.dll la versión 2.0, pero se pueden ejecutar en cualquier versión Windows Instalador.

La implementación de módulos de combinación configurables consta de dos partes. En primer lugar, al crear el módulo de mezcla (archivo .msm), el autor del módulo de mezcla agrega información a la base de datos del módulo que especifica qué elementos se pueden modificar y cómo el usuario del módulo puede configurar estos elementos. El autor agrega entradas [](merge-module-database-tables.md) a las tablas de base de datos de módulos de mezcla que están reservadas para información configurable (tabla[ModuleConfiguration](moduleconfiguration-table.md) y [tabla ModuleSubstitution),](modulesubstitution-table.md)actualiza la tabla [ \_ Validation](-validation-table.md)y agrega entradas para las tablas de módulos de combinación configurables a la [tabla ModuleIgnoreTable](moduleignoretable-table.md). Las adiciones a la tabla ModuleIgnore son necesarias para que el módulo sea compatible con Mergemod.dll versiones anteriores a la 2.0.

En segundo lugar, al combinar el módulo en un paquete de instalación (.msi archivo), el usuario final del módulo usa una herramienta de combinación. La herramienta de combinación llama a Mergemod.dll para exponer la información de configuración del módulo a una herramienta de configuración de cliente. La herramienta de configuración puede interactuar con el usuario final, pero no es necesaria para exponer todas las opciones de configuración posibles. Si el usuario rechaza proporcionar una selección para un elemento configurable, el módulo puede proporcionar un valor predeterminado. Una vez que el usuario proporciona a la herramienta de configuración sus selecciones, la herramienta de combinación llama a Mergemod.dll para realizar la combinación.

Los módulos de combinación configurables son totalmente compatibles con herramientas anteriores a Mergemod.dll versión 2.0. En estos casos, la herramienta usa los valores predeterminados del módulo.

Para obtener más información, vea [Usar módulos de combinación configurables.](using-configurable-merge-modules.md)

 

 



