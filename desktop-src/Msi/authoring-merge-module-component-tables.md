---
description: Se requiere una tabla De componentes en cada módulo de combinación.
ms.assetid: ef4a0678-bf6b-47c9-89e8-40e12da52d9b
title: Creación de tablas de componentes de módulo de mezcla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46557541b3a6b89841fe3e26cef7c00e59dc3911
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159046"
---
# <a name="authoring-merge-module-component-tables"></a>Creación de tablas de componentes de módulo de mezcla

Se [requiere una tabla](component-table.md) De componentes en cada módulo de combinación. Esta tabla contiene un registro para cada componente entregado por el módulo de mezcla al archivo de .msi destino. Tenga en cuenta que cada uno de estos componentes también debe especificarse en la tabla [ModuleComponents](modulecomponents-table.md) descrita en [Creación de tablas moduleComponents](authoring-modulecomponents-tables.md).

Use la convención de nomenclatura estándar al escribir nombres en la columna Componente para asegurarse de que el identificador de cada componente es único para todos los módulos de mezcla y bases de datos de instalación. Para obtener más información, vea [Naming Primary Keys in Merge Module Databases](naming-primary-keys-in-merge-module-databases.md).

Complete los campos restantes de cada registro como se describe para una base de datos de instalación en [la tabla Component](component-table.md). Los componentes agregados a un paquete por un módulo de combinación deben cumplir las directrices para los componentes Windows instalador válidos que se describen en las secciones siguientes:

-   [Windows Componentes del instalador](windows-installer-components.md)
-   [Organización de aplicaciones en componentes](organizing-applications-into-components.md)

 

 



