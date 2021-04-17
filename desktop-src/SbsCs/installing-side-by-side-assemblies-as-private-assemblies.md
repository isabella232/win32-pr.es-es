---
description: Para instalar ensamblados en paralelo como ensamblados privados, puede instalar el ensamblado como un componente de un paquete del instalador.
ms.assetid: 1cfd836f-a1b9-4339-8756-5488c88b3c2b
title: Instalar ensamblados en paralelo como ensamblados privados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7719a9887f9e92d81e2ad65fe2e75424f0b6957
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652393"
---
# <a name="installing-side-by-side-assemblies-as-private-assemblies"></a><span data-ttu-id="2ceba-103">Instalar ensamblados en paralelo como ensamblados privados</span><span class="sxs-lookup"><span data-stu-id="2ceba-103">Installing Side-by-side Assemblies as Private Assemblies</span></span>

<span data-ttu-id="2ceba-104">Para instalar [ensamblados en paralelo](about-side-by-side-assemblies-.md) como [ensamblados privados](/windows/desktop/Msi/private-assemblies), puede instalar el ensamblado como un componente de un paquete del instalador.</span><span class="sxs-lookup"><span data-stu-id="2ceba-104">To install [side-by-side assemblies](about-side-by-side-assemblies-.md) as [private assemblies](/windows/desktop/Msi/private-assemblies), you can install the assembly as a component of an installer package.</span></span> <span data-ttu-id="2ceba-105">Puede ser el mismo paquete de instalación que se usa para instalar o actualizar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2ceba-105">This can be the same installation package used to install or update your application.</span></span> <span data-ttu-id="2ceba-106">Se necesita Windows Installer versión 2,0 o posterior para instalar los ensamblados.</span><span class="sxs-lookup"><span data-stu-id="2ceba-106">Windows Installer version 2.0 or later is required to install assemblies.</span></span> <span data-ttu-id="2ceba-107">Para obtener más información, vea el SDK de [Windows Installer](../msi/windows-installer-portal.md) y las secciones de [instalación de ensamblados Win32](../msi/installation-of-win32-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="2ceba-107">For more information, see the [Windows Installer](../msi/windows-installer-portal.md) SDK and the sections under [Installation of Win32 Assemblies](../msi/installation-of-win32-assemblies.md).</span></span>

<span data-ttu-id="2ceba-108">Como alternativa, puede usar el instalador para copiar un ensamblado privado y un manifiesto en la misma carpeta que el archivo ejecutable de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2ceba-108">As an alternative, you can use the installer to copy a private assembly and manifest into the same folder as the application's executable file.</span></span>

 

 
