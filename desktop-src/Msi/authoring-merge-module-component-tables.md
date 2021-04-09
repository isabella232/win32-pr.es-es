---
description: En cada módulo de combinación se requiere una tabla de componentes.
ms.assetid: ef4a0678-bf6b-47c9-89e8-40e12da52d9b
title: Crear tablas de componentes de módulo de combinación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46557541b3a6b89841fe3e26cef7c00e59dc3911
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082545"
---
# <a name="authoring-merge-module-component-tables"></a>Crear tablas de componentes de módulo de combinación

En cada módulo de combinación se requiere una [tabla de componentes](component-table.md) . Esta tabla contiene un registro para cada componente entregado por el módulo de combinación en el archivo. msi de destino. Tenga en cuenta que cada uno de estos componentes también debe especificarse en la [tabla ModuleComponents](modulecomponents-table.md) que se describe en [creación de tablas ModuleComponents](authoring-modulecomponents-tables.md).

Use la Convención de nomenclatura estándar al escribir nombres en la columna componente para asegurarse de que el identificador de cada componente es único para todos los módulos de combinación y bases de datos de instalación. Para obtener más información, vea [asignar nombres a las claves principales en las bases de datos de módulos de combinación](naming-primary-keys-in-merge-module-databases.md).

Complete los campos restantes en cada registro, tal como se describe en una base de datos de instalación en la [tabla de componentes](component-table.md). Los componentes que se agregan a un paquete mediante un módulo de combinación deben cumplir las directrices de los componentes de Windows Installer válidos que se describen en las siguientes secciones:

-   [Componentes de Windows Installer](windows-installer-components.md)
-   [Organizar aplicaciones en componentes](organizing-applications-into-components.md)

 

 



