---
description: Al instalar un ensamblado en una ubicación aislada para una aplicación específica, la aplicación debe especificarse en la columna Aplicación de archivo \_ de la tabla MsiAssembly.
ms.assetid: 8d7fc09c-1017-4a30-be00-b7b0e5f2a057
title: Instalación y eliminación de ensamblados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0117c29a9bcc49a549529a6e05f1124236cb845d9b7792d7bcbda143fd6d08e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043435"
---
# <a name="installing-and-removing-assemblies"></a>Instalación y eliminación de ensamblados

Al instalar un ensamblado en una ubicación aislada para una aplicación específica, la aplicación debe especificarse en la columna Aplicación de archivo \_ de la [tabla MsiAssembly](msiassembly-table.md). Este campo es una clave en la [tabla File](file-table.md). El instalador usa la estructura de directorios especificada en la tabla [Directory](directory-table.md) para instalar el ensamblado en el mismo directorio que el componente que contiene este archivo.

Al instalar un ensamblado en la caché global de ensamblados, el valor de la columna Aplicación de archivo de la \_ [tabla MsiAssembly](msiassembly-table.md) debe ser Null.

En las secciones siguientes se describe la instalación de ensamblados de Win32 y Common Language Runtime:

-   [Instalación de ensamblados Win32](installation-of-win32-assemblies.md)
-   [Instalación de ensamblados de Common Language Runtime](installation-of-common-language-runtime-assemblies.md)

 

 



