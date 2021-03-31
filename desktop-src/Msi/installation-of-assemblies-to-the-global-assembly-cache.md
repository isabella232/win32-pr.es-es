---
description: El Windows Installer instala Common Language Runtime ensamblados en la caché global de ensamblados mediante el marco de Microsoft .NET.
ms.assetid: 21d535d5-f05b-411a-8719-2662e6046fbd
title: Instalación de ensamblados en la caché global de ensamblados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 719be313ad74374950092936bbd6124da779a0db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275803"
---
# <a name="installation-of-assemblies-to-the-global-assembly-cache"></a>Instalación de ensamblados en la caché global de ensamblados

El Windows Installer instala Common Language Runtime ensamblados en la caché global de ensamblados mediante el marco de Microsoft .NET. Al instalar ensamblados en la caché global de ensamblados, el instalador no puede usar la misma estructura de directorios y las mismas reglas de versión de archivo que usa al instalar los componentes de Windows Installer normales. Los componentes de Windows Installer normales pueden instalarse en varias ubicaciones de directorio por productos diferentes. Los ensamblados solo pueden existir una vez en la caché de ensamblados. Cada ensamblado se agrega y se quita de la caché de ensamblados como un entero indivisible. por lo tanto, todos los archivos que componen un ensamblado siempre se instalan o se quitan juntos.

El costo del disco de los componentes de Windows Installer normales y los ensamblados de Common Language Runtime se calculan de forma diferente. El costo total en disco de un componente de Windows Installer normal incluye los costos locales, los costos de origen y los costos de eliminación. Para obtener más información, consulte [costo de archivos](file-costing.md). Este método no se puede utilizar para costar Common Language Runtime ensamblados porque pueden tener clientes distintos de los Windows Installer. El costo de Common Language Runtime ensamblados se debe determinar consultando el Common Language Runtime de Microsoft .NET Framework.

En el Windows Installer se usa un proceso transaccional de dos pasos para instalar productos que contienen Common Language Runtime ensamblados. Esto permite la reversión de la instalación y eliminación de ensamblados. Para obtener más información, vea [reversión de ensamblados en la caché global de ensamblados](rollback-of-assemblies-in-the-global-assembly-cache.md).

Tenga en cuenta que la protección de archivos de Windows no protege los ensamblados instalados en la caché global de ensamblados mediante una instalación de en el [contexto de instalación](installation-context.md) por usuario. Los ensamblados que se instalan en la caché global de ensamblados mediante una instalación en el contexto de instalación por equipo están protegidos por [protección de recursos de Windows](../wfp/windows-resource-protection-portal.md).

 

 
