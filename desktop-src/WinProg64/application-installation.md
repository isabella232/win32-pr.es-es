---
title: Instalación de aplicaciones en sistemas de 64 bits
description: El Windows Installer de 64 bits puede instalar sin problemas aplicaciones basadas en MSI de 32 bits en Windows de 64 bits.
ms.assetid: fb9c5720-9906-4827-9daf-d7caa453e818
keywords:
- instalación de la aplicación 64 programación de Windows de bits
- instalación 64 programación de Windows de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13a5f8f623776ffa637718fc0d565f2c71a7b8e6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149406"
---
# <a name="application-installation-on-64-bit-systems"></a><span data-ttu-id="3da68-105">Instalación de aplicaciones en sistemas de 64 bits</span><span class="sxs-lookup"><span data-stu-id="3da68-105">Application Installation on 64-bit Systems</span></span>

<span data-ttu-id="3da68-106">El [Windows Installer de 64 bits](/windows/desktop/Msi/windows-installer-on-64-bit-operating-systems) puede instalar sin problemas aplicaciones basadas en MSI de 32 bits en Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="3da68-106">The [64-bit Windows Installer](/windows/desktop/Msi/windows-installer-on-64-bit-operating-systems) can seamlessly install 32-bit MSI-based applications on 64-bit Windows.</span></span> <span data-ttu-id="3da68-107">En el caso de las aplicaciones anteriores que usan un código auxiliar de 16 bits para iniciar un motor de instalación de 32 bits, Windows de 64 bits reconoce programas de instalador específicos de 16 bits y sustituye una versión de 32 bits por puerto.</span><span class="sxs-lookup"><span data-stu-id="3da68-107">For older applications that use a 16-bit stub to launch a 32-bit installation engine, 64-bit Windows recognizes specific 16-bit installer programs and substitutes a ported 32-bit version.</span></span>

<span data-ttu-id="3da68-108">las aplicaciones DOS de 16 bits, Windows u OS/2 suelen usar un código auxiliar de 16 bits para comprobar el tipo de máquina y, a continuación, iniciar un motor de instalación de 32 bits para realizar realmente la instalación.</span><span class="sxs-lookup"><span data-stu-id="3da68-108">16-bit DOS, Windows, or OS/2 applications often use a 16-bit stub to check the machine type, then launch a 32-bit installation engine to actually perform the installation.</span></span> <span data-ttu-id="3da68-109">Para habilitar la instalación de aplicaciones que usan esta técnica 64, Windows sustituye a las versiones de 32 bits de los siguientes programas de instalador de 16 bits:</span><span class="sxs-lookup"><span data-stu-id="3da68-109">To enable installation of applications that use this technique, 64-bit Windows substitutes 32-bit versions for the following 16-bit installer programs:</span></span>

* <span data-ttu-id="3da68-110">Programa de instalación de Microsoft para Windows 1,2</span><span class="sxs-lookup"><span data-stu-id="3da68-110">Microsoft Setup for Windows 1.2</span></span>  
* <span data-ttu-id="3da68-111">Programa de instalación de Microsoft para Windows 2,6</span><span class="sxs-lookup"><span data-stu-id="3da68-111">Microsoft Setup for Windows 2.6</span></span>  
* <span data-ttu-id="3da68-112">Programa de instalación de Microsoft para Windows 3,0</span><span class="sxs-lookup"><span data-stu-id="3da68-112">Microsoft Setup for Windows 3.0</span></span>  
* <span data-ttu-id="3da68-113">Programa de instalación de Microsoft para Windows 3,01</span><span class="sxs-lookup"><span data-stu-id="3da68-113">Microsoft Setup for Windows 3.01</span></span>  
* <span data-ttu-id="3da68-114">InstallShield 5. x</span><span class="sxs-lookup"><span data-stu-id="3da68-114">InstallShield 5.x</span></span>  

<span data-ttu-id="3da68-115">La lista de sustituciones se almacena en el registro con la siguiente clave: **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ NtVdm64**.</span><span class="sxs-lookup"><span data-stu-id="3da68-115">The list of substitutions is stored in the registry under the following key: **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows NT\\CurrentVersion\\NtVdm64**.</span></span>

> [!Note]  
> <span data-ttu-id="3da68-116">Este mecanismo solo se proporciona para la compatibilidad con aplicaciones de 32 bits que usan los programas de Microsoft Installer de 16 bits que se enumeran en este tema.</span><span class="sxs-lookup"><span data-stu-id="3da68-116">This mechanism is provided only for compatibility with 32-bit applications that use the 16-bit Microsoft installer programs listed in this topic.</span></span> <span data-ttu-id="3da68-117">No se admite la adición de programas de instalador de terceros.</span><span class="sxs-lookup"><span data-stu-id="3da68-117">Addition of third-party installer programs is not supported.</span></span>

 

> [!Note]  
> <span data-ttu-id="3da68-118">Este mecanismo no se incluye en Windows 10 en ARM.</span><span class="sxs-lookup"><span data-stu-id="3da68-118">This mechanism is not included on Windows 10 on ARM.</span></span>

 

 

 