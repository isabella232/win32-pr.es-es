---
description: Una lista de posibles razones por las que un Windows Installer desinstalación no pudo quitar todos los archivos de una aplicación.
ms.assetid: 0a856f0f-a829-478e-a83b-dade7b05b4f2
title: Quitar archivos en desuso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d5eeceb45c2139d146c32bdf9917e41885688df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667669"
---
# <a name="removing-stranded-files"></a><span data-ttu-id="ad18b-103">Quitar archivos en desuso</span><span class="sxs-lookup"><span data-stu-id="ad18b-103">Removing Stranded Files</span></span>

<span data-ttu-id="ad18b-104">Si un archivo que se debe haber quitado del equipo del usuario permanece instalado después de ejecutar una desinstalación, es posible que el instalador no esté quitando el componente que contiene el archivo por una o varias de las razones siguientes:</span><span class="sxs-lookup"><span data-stu-id="ad18b-104">If a file that should have been removed from the user's computer remains installed after running an uninstall, the installer may not be removing the component containing the file for one or more of the following reasons:</span></span>

-   <span data-ttu-id="ad18b-105">Se estableció el bit msidbComponentAttributesPermanent para el componente en la columna Attributes de la [tabla Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="ad18b-105">The msidbComponentAttributesPermanent bit was set for the component in the Attributes column of the [Component table](component-table.md).</span></span>
-   <span data-ttu-id="ad18b-106">No se especificó ningún valor para el componente en la columna ComponentId de la tabla de componentes.</span><span class="sxs-lookup"><span data-stu-id="ad18b-106">No value was entered for the component in the ComponentId column of the Component table.</span></span>
-   <span data-ttu-id="ad18b-107">El componente lo usa otra aplicación o característica que todavía está instalada.</span><span class="sxs-lookup"><span data-stu-id="ad18b-107">The component is used by another application or feature that is still installed.</span></span>
-   <span data-ttu-id="ad18b-108">Existe una condición especificada en la tabla de [condiciones](condition-table.md) que habilita una característica durante la instalación y deshabilita la característica durante la desinstalación.</span><span class="sxs-lookup"><span data-stu-id="ad18b-108">There is a condition specified in the [Condition](condition-table.md) table that enables a feature during installation and disables the feature during uninstallation.</span></span>
-   <span data-ttu-id="ad18b-109">El archivo de clave del componente tiene un recuento de referencias anterior en **HKLM** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **SharedDLLs**.</span><span class="sxs-lookup"><span data-stu-id="ad18b-109">The key file for the component has a previous reference count under **HKLM**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**SharedDLLs**.</span></span>
-   <span data-ttu-id="ad18b-110">El componente se instala en la carpeta del sistema y cualquier archivo del componente tiene un recuento de referencias anterior en **HKLM** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **SharedDLLs**.</span><span class="sxs-lookup"><span data-stu-id="ad18b-110">The component is installed in the System folder and any file in the component has a previous reference count under **HKLM**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**SharedDLLs**.</span></span>
-   <span data-ttu-id="ad18b-111">El Windows Installer no quita los archivos ni las claves del registro que estén protegidos por [protección de recursos de Windows](../wfp/windows-resource-protection-portal.md) (WRP).</span><span class="sxs-lookup"><span data-stu-id="ad18b-111">The Windows Installer does not remove any files or registry keys that are protected by [Windows Resource Protection](../wfp/windows-resource-protection-portal.md) (WRP).</span></span> <span data-ttu-id="ad18b-112">Para obtener más información, vea [usar Windows Installer y protección de recursos de Windows](windows-resource-protection-on-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="ad18b-112">For more information, see [Using Windows Installer and Windows Resource Protection](windows-resource-protection-on-windows-vista.md).</span></span> <span data-ttu-id="ad18b-113">En Windows Server 2003, Windows XP y Windows 2000, el instalador no quita los archivos protegidos por protección de archivos de Windows (WFP).</span><span class="sxs-lookup"><span data-stu-id="ad18b-113">On Windows Server 2003, Windows XP, and Windows 2000, the installer does not remove any files that are protected by Windows File Protection (WFP).</span></span> <span data-ttu-id="ad18b-114">Si la clave del registro o el archivo de ruta de acceso de la clave de un componente están protegidos por WFP o WRP, el instalador no quita el componente.</span><span class="sxs-lookup"><span data-stu-id="ad18b-114">If a component's key path file or registry key is protected by WFP or WRP, the installer does not remove the component.</span></span>
    > [!Note]  
    > <span data-ttu-id="ad18b-115">Dado que Windows Installer no instala, actualiza o quita ningún recurso que esté protegido por WRP, no debe incluir recursos protegidos en un paquete de instalación.</span><span class="sxs-lookup"><span data-stu-id="ad18b-115">Because Windows Installer does not install, update, or remove any resource that is protected by WRP, you should not include protected resources in an installation package.</span></span> <span data-ttu-id="ad18b-116">En su lugar, use solo los [mecanismos de sustitución de recursos admitidos](../wfp/supported-file-replacement-mechanisms.md) que se describen en la sección [protección de recursos de Windows](../wfp/windows-resource-protection-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="ad18b-116">Instead, use only the [supported resource replacement mechanisms](../wfp/supported-file-replacement-mechanisms.md) described in the [Windows Resource Protection](../wfp/windows-resource-protection-portal.md) section.</span></span>

     

 

 
