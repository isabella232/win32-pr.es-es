---
description: Al instalar un ensamblado en una ubicación aislada para una aplicación específica, la aplicación debe especificarse en la \_ columna aplicación de archivo de la tabla MsiAssembly.
ms.assetid: 8d7fc09c-1017-4a30-be00-b7b0e5f2a057
title: Instalar y quitar ensamblados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f44dee05940ab3c05e97a7145f9b2363226bb07c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279345"
---
# <a name="installing-and-removing-assemblies"></a>Instalar y quitar ensamblados

Al instalar un ensamblado en una ubicación aislada para una aplicación específica, la aplicación debe especificarse en la \_ columna aplicación de archivo de la [tabla MsiAssembly](msiassembly-table.md). Este campo es una clave en la [tabla de archivos](file-table.md). El instalador usa la estructura de directorios que se especifica en la [tabla del directorio](directory-table.md) para instalar el ensamblado en el mismo directorio que el componente que contiene este archivo.

Al instalar un ensamblado en la caché global de ensamblados, el valor de la \_ columna aplicación de archivo de la [tabla MsiAssembly](msiassembly-table.md) debe ser null.

En las secciones siguientes se describe la instalación de Win32 y los ensamblados de Common Language Runtime:

-   [Instalación de ensamblados Win32](installation-of-win32-assemblies.md)
-   [Instalación de ensamblados de Common Language Runtime](installation-of-common-language-runtime-assemblies.md)

 

 



