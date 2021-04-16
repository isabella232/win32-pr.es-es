---
description: Instale los ensamblados Win32 convirtiéndolos en un componente de Microsoft Windows Installer paquete que instala o actualiza su aplicación.
ms.assetid: 09aecb55-ed45-45b3-b27a-d0946223392a
title: Instalación de ensamblados Win32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9d47847c0c69185a28fa41bbe5c5a05deec1e66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652505"
---
# <a name="installation-of-win32-assemblies"></a><span data-ttu-id="1fede-103">Instalación de ensamblados Win32</span><span class="sxs-lookup"><span data-stu-id="1fede-103">Installation of Win32 Assemblies</span></span>

<span data-ttu-id="1fede-104">Instale los ensamblados Win32 convirtiéndolos en un componente de Microsoft Windows Installer paquete que instala o actualiza su aplicación.</span><span class="sxs-lookup"><span data-stu-id="1fede-104">Install Win32 assemblies by making them a component of Microsoft Windows Installer package that installs or updates your application.</span></span> <span data-ttu-id="1fede-105">Al crear la tabla [MsiAssembly](msiassembly-table.md) y la [tabla MsiAssemblyName](msiassemblyname-table.md), se identifica el componente en la \_ columna componente como un ensamblado.</span><span class="sxs-lookup"><span data-stu-id="1fede-105">When you author the [MsiAssembly table](msiassembly-table.md) and [MsiAssemblyName table](msiassemblyname-table.md), this identifies the component in the Component\_ column as an assembly.</span></span> <span data-ttu-id="1fede-106">El instalador establecerá la propiedad [**MsiWin32AssemblySupport**](msiwin32assemblysupport.md) en la versión de archivo de Sxs.dll en los sistemas operativos que pueden admitir ensamblados Win32 y sin establecer esta propiedad en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="1fede-106">The installer will set the [**MsiWin32AssemblySupport**](msiwin32assemblysupport.md) property to the file version of Sxs.dll on operating systems that can support Win32 assemblies and not set this property otherwise.</span></span>

<span data-ttu-id="1fede-107">En Windows Vista y Windows XP, Windows Installer no escribe información de ensamblado en el registro.</span><span class="sxs-lookup"><span data-stu-id="1fede-107">In Windows Vista and Windows XP, Windows Installer does not write assembly information into the registry.</span></span> <span data-ttu-id="1fede-108">Además, se pueden utilizar ensamblados compartidos, ensamblados privados y ensamblados en paralelo.</span><span class="sxs-lookup"><span data-stu-id="1fede-108">In addition, shared assemblies, private assemblies, and side-by-side assemblies can be used.</span></span> <span data-ttu-id="1fede-109">Para obtener más información, vea [ensamblados compartidos](shared-assemblies.md), [ensamblados privados](private-assemblies.md)y [ensamblados en paralelo](side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="1fede-109">For information, see [Shared Assemblies](shared-assemblies.md), [Private Assemblies](private-assemblies.md), and [Side-by-Side Assemblies](side-by-side-assemblies.md).</span></span>

<span data-ttu-id="1fede-110">En las secciones siguientes se describe cómo crear un paquete de Windows Installer para instalar los ensamblados de Win32 como compartidos, privados o en paralelo en diferentes sistemas operativos Windows.</span><span class="sxs-lookup"><span data-stu-id="1fede-110">The following sections describe how to author a Windows Installer package to install Win32 assemblies as shared, private, or side-by-side on different Windows operating systems.</span></span>

-   [<span data-ttu-id="1fede-111">Instalación de ensamblados Win32 para el uso compartido en paralelo en Windows XP</span><span class="sxs-lookup"><span data-stu-id="1fede-111">Installing Win32 Assemblies for Side-by-Side Sharing on Windows XP</span></span>](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
-   [<span data-ttu-id="1fede-112">Instalar ensamblados Win32 para el uso privado de una aplicación en Windows XP</span><span class="sxs-lookup"><span data-stu-id="1fede-112">Installing Win32 Assemblies for the Private Use of an Application on Windows XP</span></span>](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)

 

 



