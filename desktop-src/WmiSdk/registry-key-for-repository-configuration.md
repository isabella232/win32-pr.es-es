---
description: Instrumental de administración de Windows (WMI) tiene una nueva clave del registro para habilitar o deshabilitar la característica de repositorio de restauración.
ms.assetid: 6c93fc40-b5d8-42da-9d02-7fa04fce3f65
ms.tgt_platform: multiple
title: Clave del registro para la configuración del repositorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed981da7c0540378746c78fecceefab8fc62559b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706096"
---
# <a name="registry-key-for-repository-configuration"></a><span data-ttu-id="74b29-103">Clave del registro para la configuración del repositorio</span><span class="sxs-lookup"><span data-stu-id="74b29-103">Registry Key for Repository Configuration</span></span>

<span data-ttu-id="74b29-104">Instrumental de administración de Windows (WMI) tiene una nueva clave del registro para habilitar o deshabilitar la característica de repositorio de restauración.</span><span class="sxs-lookup"><span data-stu-id="74b29-104">Windows Management Instrumentation (WMI) has a new registry key to enable or disable the AutoRestore repository feature..</span></span> <span data-ttu-id="74b29-105">Para obtener más información acerca de la restauración del repositorio WMI, vea [copia de seguridad o restauración del repositorio WMI](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731460(v=ws.11)).</span><span class="sxs-lookup"><span data-stu-id="74b29-105">For more information on restoring the WMI repository, see [Backup or Restore WMI Repository](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731460(v=ws.11)).</span></span>

<span data-ttu-id="74b29-106">En Windows 7, el comportamiento predeterminado es la restauración automática de un repositorio a partir de una versión de copia de seguridad si se detecta un daño en el repositorio.</span><span class="sxs-lookup"><span data-stu-id="74b29-106">In Windows 7, the default behavior is to auto-restore a repository from a backed-up version if a repository corruption is detected.</span></span> <span data-ttu-id="74b29-107">WMI proporciona el valor del registro **AutoRestoreEnabled** para deshabilitar esta característica.</span><span class="sxs-lookup"><span data-stu-id="74b29-107">WMI provides the **AutoRestoreEnabled** registry value to disable this feature.</span></span>

<span data-ttu-id="74b29-108">Las claves del registro para WMI se encuentran en el registro en **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ .</span><span class="sxs-lookup"><span data-stu-id="74b29-108">The registry keys for WMI are located in the registry at **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\.</span></span>

<dl> <dt>

<span data-ttu-id="74b29-109"><span id="AutoRestoreEnabled"></span><span id="autorestoreenabled"></span><span id="AUTORESTOREENABLED"></span>**AutoRestoreEnabled**</span><span class="sxs-lookup"><span data-stu-id="74b29-109"><span id="AutoRestoreEnabled"></span><span id="autorestoreenabled"></span><span id="AUTORESTOREENABLED"></span>**AutoRestoreEnabled**</span></span>
</dt> <dd>

<span data-ttu-id="74b29-110">Permite al usuario determinar si se usa o no la característica de repositorio de restauración.</span><span class="sxs-lookup"><span data-stu-id="74b29-110">Enables the user to determine whether or not to use the AutoRestore repository feature.</span></span> <span data-ttu-id="74b29-111">De forma predeterminada, esta clave se establece en 1 y está habilitada la característica de repositorio de restauración.</span><span class="sxs-lookup"><span data-stu-id="74b29-111">By default this key is set to 1 and the AutoRestore Repository feature is enabled.</span></span>

<span data-ttu-id="74b29-112">Las siguientes opciones son posibles:</span><span class="sxs-lookup"><span data-stu-id="74b29-112">The following settings are possible:</span></span>

<dl> <dt>

<span data-ttu-id="74b29-113"><span id="0"></span>0</span><span class="sxs-lookup"><span data-stu-id="74b29-113"><span id="0"></span>0</span></span>
</dt> <dd>

<span data-ttu-id="74b29-114">Disabled</span><span class="sxs-lookup"><span data-stu-id="74b29-114">Disabled</span></span>

</dd> <dt>

<span data-ttu-id="74b29-115"><span id="1"></span>1</span><span class="sxs-lookup"><span data-stu-id="74b29-115"><span id="1"></span>1</span></span>
</dt> <dd>

<span data-ttu-id="74b29-116">habilitado</span><span class="sxs-lookup"><span data-stu-id="74b29-116">Enabled</span></span>

</dd> </dl> </dd> </dl>

<span data-ttu-id="74b29-117">El valor del registro **AutoRestoreEnabled** se puede modificar mediante el consola de administración de directivas de grupo (GPMC).</span><span class="sxs-lookup"><span data-stu-id="74b29-117">The **AutoRestoreEnabled** registry value can be modified by using the Group Policy Management Console (GPMC).</span></span> <span data-ttu-id="74b29-118">Para obtener más información, vea [consola de administración de directivas de grupo](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal).</span><span class="sxs-lookup"><span data-stu-id="74b29-118">For more information, see [Group Policy Management Console](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal).</span></span>

<span data-ttu-id="74b29-119">En este procedimiento se proporcionan detalles acerca de cómo habilitar o deshabilitar la característica de repositorio de restauración.</span><span class="sxs-lookup"><span data-stu-id="74b29-119">This procedure provides details about how to enable or disable the AutoRestore repository feature:</span></span>

<span data-ttu-id="74b29-120">**Para cambiar el valor predeterminado de la clave **AutoRestoreEnabled** mediante Directiva de grupo**</span><span class="sxs-lookup"><span data-stu-id="74b29-120">**To change the default value of the **AutoRestoreEnabled** key by using Group Policy**</span></span>

1.  <span data-ttu-id="74b29-121">Abra GPMC.</span><span class="sxs-lookup"><span data-stu-id="74b29-121">Open the GPMC.</span></span>
2.  <span data-ttu-id="74b29-122">Cree un objeto de directiva de grupo (GPO).</span><span class="sxs-lookup"><span data-stu-id="74b29-122">Create a Group Policy object (GPO).</span></span>
3.  <span data-ttu-id="74b29-123">Edite el GPO.</span><span class="sxs-lookup"><span data-stu-id="74b29-123">Edit the GPO.</span></span>
4.  <span data-ttu-id="74b29-124">Vaya a preferencias/configuración de Windows/registro.</span><span class="sxs-lookup"><span data-stu-id="74b29-124">Browse to Preferences/Windows Settings/Registry.</span></span>
5.  <span data-ttu-id="74b29-125">Haga clic con el botón derecho y seleccione **nuevo... Registro**.</span><span class="sxs-lookup"><span data-stu-id="74b29-125">Right-click and select **New... Registry**.</span></span> <span data-ttu-id="74b29-126">Esta acción presenta una interfaz de usuario donde puede especificar la información del registro.</span><span class="sxs-lookup"><span data-stu-id="74b29-126">This action presents a user interface where you can enter registry information.</span></span>
6.  <span data-ttu-id="74b29-127">Seleccione el comando de **actualización** .</span><span class="sxs-lookup"><span data-stu-id="74b29-127">Select the **Update** command.</span></span>
7.  <span data-ttu-id="74b29-128">Seleccione la siguiente ruta de acceso de clave del registro: **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ WBEM \\ CIMOM**.</span><span class="sxs-lookup"><span data-stu-id="74b29-128">Select the following registry key path: **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\WBEM\\CIMOM**.</span></span>
8.  <span data-ttu-id="74b29-129">En el campo **nombre** , escriba **AutoRestoreEnabled**.</span><span class="sxs-lookup"><span data-stu-id="74b29-129">In the **name** field, enter **AutoRestoreEnabled**.</span></span>
9.  <span data-ttu-id="74b29-130">En el campo de **datos** , escriba 0 para deshabilitar o 1 para habilitar la característica de repositorio de restauración.</span><span class="sxs-lookup"><span data-stu-id="74b29-130">In the **data** field, enter 0 to disable or 1 to enable the AutoRestore repository feature.</span></span>
10. <span data-ttu-id="74b29-131">Haga clic en Aceptar.</span><span class="sxs-lookup"><span data-stu-id="74b29-131">Click OK.</span></span>

 

 
