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
# <a name="installing-and-removing-assemblies"></a><span data-ttu-id="18030-103">Instalar y quitar ensamblados</span><span class="sxs-lookup"><span data-stu-id="18030-103">Installing and Removing Assemblies</span></span>

<span data-ttu-id="18030-104">Al instalar un ensamblado en una ubicación aislada para una aplicación específica, la aplicación debe especificarse en la \_ columna aplicación de archivo de la [tabla MsiAssembly](msiassembly-table.md).</span><span class="sxs-lookup"><span data-stu-id="18030-104">When installing an assembly to an isolated location for a specific application, the application must be specified in the File\_Application column of the [MsiAssembly table](msiassembly-table.md).</span></span> <span data-ttu-id="18030-105">Este campo es una clave en la [tabla de archivos](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="18030-105">This field is a key into the [File table](file-table.md).</span></span> <span data-ttu-id="18030-106">El instalador usa la estructura de directorios que se especifica en la [tabla del directorio](directory-table.md) para instalar el ensamblado en el mismo directorio que el componente que contiene este archivo.</span><span class="sxs-lookup"><span data-stu-id="18030-106">The installer uses the directory structure that is specified in the [Directory table](directory-table.md) to install the assembly into the same directory as the component that contains this file.</span></span>

<span data-ttu-id="18030-107">Al instalar un ensamblado en la caché global de ensamblados, el valor de la \_ columna aplicación de archivo de la [tabla MsiAssembly](msiassembly-table.md) debe ser null.</span><span class="sxs-lookup"><span data-stu-id="18030-107">When installing an assembly to the global assembly cache, the value in the File\_Application column of the [MsiAssembly Table](msiassembly-table.md) must be Null.</span></span>

<span data-ttu-id="18030-108">En las secciones siguientes se describe la instalación de Win32 y los ensamblados de Common Language Runtime:</span><span class="sxs-lookup"><span data-stu-id="18030-108">The following sections describe the installation of Win32 and common language runtime assemblies:</span></span>

-   [<span data-ttu-id="18030-109">Instalación de ensamblados Win32</span><span class="sxs-lookup"><span data-stu-id="18030-109">Installation of Win32 Assemblies</span></span>](installation-of-win32-assemblies.md)
-   [<span data-ttu-id="18030-110">Instalación de ensamblados de Common Language Runtime</span><span class="sxs-lookup"><span data-stu-id="18030-110">Installation of Common Language Runtime Assemblies</span></span>](installation-of-common-language-runtime-assemblies.md)

 

 



