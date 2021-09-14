---
description: El Windows instala ensamblados de Common Language Runtime en la caché global de ensamblados mediante microsoft .NET Framework.
ms.assetid: 21d535d5-f05b-411a-8719-2662e6046fbd
title: Instalación de ensamblados en la caché global de ensamblados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 719be313ad74374950092936bbd6124da779a0db
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171785"
---
# <a name="installation-of-assemblies-to-the-global-assembly-cache"></a>Instalación de ensamblados en la caché global de ensamblados

El Windows instala ensamblados de Common Language Runtime en la caché global de ensamblados mediante microsoft .NET Framework. Al instalar ensamblados en la caché global de ensamblados, el instalador no puede usar la misma estructura de directorios y reglas de versión de archivo que usa al instalar componentes Windows Installer. Los componentes Windows installer normales se pueden instalar en varias ubicaciones de directorio mediante productos diferentes. Los ensamblados solo pueden existir una vez en la caché de ensamblados. Cada ensamblado se agrega y quita de la caché de ensamblados como un conjunto indivisible; por lo tanto, todos los archivos que componen un ensamblado siempre se instalan o se quitan juntos.

El costo de disco de los componentes Windows installer y los ensamblados de Common Language Runtime se calculan de forma diferente. El costo total de disco de un componente Windows installer incluye los costos locales, los costos de origen y los costos de eliminación. Para obtener más información, vea [File Costing](file-costing.md). Este método no se puede usar para costar ensamblados de Common Language Runtime porque pueden tener clientes que no sean Windows Installer. El costo de los ensamblados de Common Language Runtime debe determinarse mediante la consulta de Microsoft .NET Framework Common Language Runtime.

El Windows usa un proceso transaccional de dos pasos para instalar productos que contienen ensamblados de Common Language Runtime. Esto permite la reversión de la instalación y eliminación de ensamblados. Para obtener más información, vea [Reversión de ensamblados en la caché global de ensamblados.](rollback-of-assemblies-in-the-global-assembly-cache.md)

Tenga en cuenta que los ensamblados instalados en la [](installation-context.md) caché global de ensamblados por una instalación en el contexto de instalación por usuario no están protegidos por Windows File Protection. Los ensamblados que se instalan en la caché global de ensamblados mediante una instalación en el contexto de instalación por equipo están protegidos [por Windows Resource Protection](../wfp/windows-resource-protection-portal.md).

 

 
