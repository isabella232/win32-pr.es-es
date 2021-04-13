---
description: Si un paquete de Windows Installer instala o anuncia ensamblados, el instalador almacena información sobre esos ensamblados en el registro del sistema local.
ms.assetid: 1a6b0530-b5ad-49db-bc08-5b20d32420ef
title: Claves del registro de ensamblado escritas por Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bdd2ea7d290659fa9c1578d89be9a77dcc5cc10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545182"
---
# <a name="assembly-registry-keys-written-by-windows-installer"></a><span data-ttu-id="3e59a-103">Claves del registro de ensamblado escritas por Windows Installer</span><span class="sxs-lookup"><span data-stu-id="3e59a-103">Assembly Registry Keys Written by Windows Installer</span></span>

<span data-ttu-id="3e59a-104">Si un paquete de Windows Installer instala o anuncia ensamblados, el instalador almacena información sobre esos ensamblados en el registro del sistema local.</span><span class="sxs-lookup"><span data-stu-id="3e59a-104">If a Windows Installer package installs or advertises assemblies, the installer stores information about those assemblies in the local system registry.</span></span> <span data-ttu-id="3e59a-105">Tenga en cuenta que estas claves del registro solo están pensadas para que las use internamente Windows Installer y no deben depender de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3e59a-105">Please note that these registry keys are only intended to be used internally by Windows Installer and they should not be relied upon by your application.</span></span> <span data-ttu-id="3e59a-106">El contenido, la ubicación y la estructura de la información almacenada en estas claves están sujetos a cambios.</span><span class="sxs-lookup"><span data-stu-id="3e59a-106">The content, location, and structure of information stored in these keys is subject to change.</span></span> <span data-ttu-id="3e59a-107">Las aplicaciones deben basarse en [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) para administrar ensamblados.</span><span class="sxs-lookup"><span data-stu-id="3e59a-107">Applications should rely upon [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) to manage assemblies.</span></span>

<span data-ttu-id="3e59a-108">Los ensamblados se registran con los nombres de ensamblado.</span><span class="sxs-lookup"><span data-stu-id="3e59a-108">Assemblies are registered by their assembly names.</span></span> <span data-ttu-id="3e59a-109">Los nombres de los valores almacenados en las siguientes ubicaciones son los nombres de ensamblado.</span><span class="sxs-lookup"><span data-stu-id="3e59a-109">The names of the values stored in the following locations are the assembly names.</span></span> <span data-ttu-id="3e59a-110">Los valores reales son del tipo REG \_ multi \_ SZ y contienen datos usados por [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) para instalar o reparar ensamblados.</span><span class="sxs-lookup"><span data-stu-id="3e59a-110">The actual values are of the type REG\_MULTI\_SZ and contain data used by [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) to install or repair assemblies.</span></span>

## <a name="information-about-private-assemblies"></a><span data-ttu-id="3e59a-111">Información sobre ensamblados privados</span><span class="sxs-lookup"><span data-stu-id="3e59a-111">Information About Private Assemblies</span></span>

<span data-ttu-id="3e59a-112">Windows Installer almacena información acerca de los ensamblados privados que llevan Windows Installer paquetes que se han instalado como aplicaciones administradas por usuario en la siguiente clave del registro:</span><span class="sxs-lookup"><span data-stu-id="3e59a-112">Windows Installer stores information about private assemblies carried by Windows Installer packages that have been installed as managed per-user applications under the following registry key:</span></span>

<span data-ttu-id="3e59a-113">**HKLM** \\ **Software** \\ de **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Instalador** \\ de **Administrados** \\ **SID *_\\_* de usuario Instalador** \\ de **ensamblados** \\ \* *_ruta de acceso al archivo de configuración_* _</span><span class="sxs-lookup"><span data-stu-id="3e59a-113">**HKLM**\\**SOFTWARE**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Installer**\\**Managed**\\**_User SID_*_\\_\* Installer**\\**Assemblies**\\**_path to config file_* _</span></span>

<span data-ttu-id="3e59a-114">Windows Installer almacena información sobre los ensamblados privados que llevan Windows Installer paquetes que se han instalado por usuario en la siguiente clave del registro:</span><span class="sxs-lookup"><span data-stu-id="3e59a-114">Windows Installer stores information about private assemblies carried by Windows Installer packages that have been installed per-user under the following registry key:</span></span>

<span data-ttu-id="3e59a-115">_*HKCU **\\** software **\\** Microsoft **\\** Installer **\\** ensamblados **\\** _ruta de acceso al archivo de configuración_*_</span><span class="sxs-lookup"><span data-stu-id="3e59a-115">_*HKCU **\\** Software **\\** Microsoft **\\** Installer **\\** Assemblies **\\**_path to config file_*_</span></span>

<span data-ttu-id="3e59a-116">Windows Installer almacena información sobre los ensamblados privados que llevan Windows Installer paquetes y que se instalan por equipo en la siguiente clave del registro:</span><span class="sxs-lookup"><span data-stu-id="3e59a-116">Windows Installer stores information about private assemblies carried by Windows Installer packages and installed per-machine under the following registry key:</span></span>

<span data-ttu-id="3e59a-117">_*HKLM **\\** **\\** **\\** instalación de clases **\\** de software ensamblados **\\** _ruta de acceso al archivo de configuración_*_</span><span class="sxs-lookup"><span data-stu-id="3e59a-117">_*HKLM **\\** SOFTWARE **\\** Classes **\\** Installer **\\** Assemblies **\\**_path to config file_*_</span></span>

## <a name="information-about-global-or-shared-assemblies"></a><span data-ttu-id="3e59a-118">Información sobre ensamblados globales o compartidos</span><span class="sxs-lookup"><span data-stu-id="3e59a-118">Information About Global or Shared Assemblies</span></span>

<span data-ttu-id="3e59a-119">Windows Installer almacena información sobre los ensamblados compartidos que llevan Windows Installer paquetes que se han instalado como aplicaciones administradas por usuario en la siguiente clave del registro:</span><span class="sxs-lookup"><span data-stu-id="3e59a-119">Windows Installer stores information about shared assemblies carried by Windows Installer packages that have been installed as managed per-user applications under the following registry key:</span></span>

<span data-ttu-id="3e59a-120">_*HKLM **\\** SOFTWARE **\\** Microsoft **\\** Windows **\\** CurrentVersion **\\** Installer **\\** Managed **\\** _User SID_*_ \\ _ *Installer **\\** assemblies **\\** global*\*</span><span class="sxs-lookup"><span data-stu-id="3e59a-120">_*HKLM **\\** SOFTWARE **\\** Microsoft **\\** Windows **\\** CurrentVersion **\\** Installer **\\** Managed **\\**_User SID_*_\\_ *Installer **\\** Assemblies **\\** Global*\*</span></span>

<span data-ttu-id="3e59a-121">Windows Installer almacena información sobre los ensamblados compartidos que llevan Windows Installer paquetes que se han instalado por usuario en la siguiente clave del registro:</span><span class="sxs-lookup"><span data-stu-id="3e59a-121">Windows Installer stores information about shared assemblies carried by Windows Installer packages that have been installed per-user under the following registry key:</span></span>

<span data-ttu-id="3e59a-122">**HKCU** \\ **Software** \\ de **Microsoft** \\ **Instalador** \\ de **Ensamblados** \\ **Nivel global**</span><span class="sxs-lookup"><span data-stu-id="3e59a-122">**HKCU**\\**Software**\\**Microsoft**\\**Installer**\\**Assemblies**\\**Global**</span></span>

<span data-ttu-id="3e59a-123">Windows Installer almacena información sobre los ensamblados compartidos que llevan Windows Installer paquetes y que se instalan por equipo en la siguiente clave del registro:</span><span class="sxs-lookup"><span data-stu-id="3e59a-123">Windows Installer stores information about shared assemblies carried by Windows Installer packages and installed per-machine under the following registry key:</span></span>

<span data-ttu-id="3e59a-124">**HKLM** \\ **Software** \\ de **Clases** \\ de **Instalador** \\ de **Ensamblados** \\ **Nivel global**</span><span class="sxs-lookup"><span data-stu-id="3e59a-124">**HKLM**\\**SOFTWARE**\\**Classes**\\**Installer**\\**Assemblies**\\**Global**</span></span>

 

 



