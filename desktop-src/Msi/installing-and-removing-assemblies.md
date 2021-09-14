---
description: Al instalar un ensamblado en una ubicación aislada para una aplicación específica, la aplicación debe especificarse en la columna Aplicación de archivo \_ de la tabla MsiAssembly.
ms.assetid: 8d7fc09c-1017-4a30-be00-b7b0e5f2a057
title: Instalar y quitar ensamblados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f44dee05940ab3c05e97a7145f9b2363226bb07c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072055"
---
# <a name="installing-and-removing-assemblies"></a>Instalar y quitar ensamblados

Al instalar un ensamblado en una ubicación aislada para una aplicación específica, la aplicación debe especificarse en la columna Aplicación de archivo de \_ la [tabla MsiAssembly](msiassembly-table.md). Este campo es una clave de la [tabla File](file-table.md). El instalador usa la estructura de directorios especificada en la tabla [Directory](directory-table.md) para instalar el ensamblado en el mismo directorio que el componente que contiene este archivo.

Al instalar un ensamblado en la caché global de ensamblados, el valor de la columna Aplicación de archivo de la \_ [tabla MsiAssembly](msiassembly-table.md) debe ser Null.

En las secciones siguientes se describe la instalación de ensamblados de Win32 y Common Language Runtime:

-   [Instalación de ensamblados win32](installation-of-win32-assemblies.md)
-   [Instalación de ensamblados de Common Language Runtime](installation-of-common-language-runtime-assemblies.md)

 

 



