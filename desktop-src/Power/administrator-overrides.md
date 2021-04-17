---
description: Invalidaciones de administrador
ms.assetid: 25b6ce86-52c8-4f7f-97af-86b2eaf3e9af
title: Invalidaciones de administrador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c43e16c9aa3eb3ab9fd5ee7c8d17b9bb4536315
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667234"
---
# <a name="administrator-overrides"></a><span data-ttu-id="44969-103">Invalidaciones de administrador</span><span class="sxs-lookup"><span data-stu-id="44969-103">Administrator Overrides</span></span>

<span data-ttu-id="44969-104">Windows tiene una sola lista de control de acceso (ACL) predeterminada en todos los objetos de directiva de energía.</span><span class="sxs-lookup"><span data-stu-id="44969-104">Windows has a single default access control list (ACL) on all power policy objects.</span></span> <span data-ttu-id="44969-105">La ACL concede permisos de lectura, escritura y modificación a los miembros del grupo usuarios autenticados.</span><span class="sxs-lookup"><span data-stu-id="44969-105">The ACL grants read, write, and change permissions to members of the Authenticated Users group.</span></span> <span data-ttu-id="44969-106">A todos los demás usuarios se les concede el permiso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="44969-106">All other users are granted read-only permission.</span></span> <span data-ttu-id="44969-107">Las aplicaciones que llaman a funciones de la Directiva de energía pueden determinar si un usuario tiene permisos para una configuración de energía especificada mediante la función [**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) .</span><span class="sxs-lookup"><span data-stu-id="44969-107">Applications that call power policy functions can determine whether a user has permissions for a specified power setting by using the [**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) function.</span></span>

<span data-ttu-id="44969-108">La configuración de energía se puede invalidar mediante directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="44969-108">Power settings may be overridden via Group Policy.</span></span> <span data-ttu-id="44969-109">Las invalidaciones se pueden establecer mediante la Directiva de grupo de dominio o la Directiva de grupo local.</span><span class="sxs-lookup"><span data-stu-id="44969-109">Overrides can be set through domain group policy or local group policy.</span></span> <span data-ttu-id="44969-110">[**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) informará si una configuración de energía especificada tiene una invalidación de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="44969-110">[**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) will report if a specified power setting has a group policy override.</span></span>

<span data-ttu-id="44969-111">La herramienta de línea de comandos **PowerCfg.exe** muestra un mensaje de error cuando no se puede completar un comando porque el usuario no tiene permisos para cambiar la configuración de energía o porque la configuración de energía tiene una invalidación de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="44969-111">The command line tool **PowerCfg.exe** displays an error message when a command cannot be completed either because the user did not have permissions to change the power setting or because the power setting has a group policy override.</span></span>

<span data-ttu-id="44969-112">La aplicación opciones de energía del panel de control no admite la configuración de permisos de acceso a directivas de energía.</span><span class="sxs-lookup"><span data-stu-id="44969-112">The Power Options application in Control Panel does not provide support for configuring power policy access permissions.</span></span> <span data-ttu-id="44969-113">El cambio de permisos debe realizarse a través de **PowerCfg.exe**.</span><span class="sxs-lookup"><span data-stu-id="44969-113">Changing permissions must be done via **PowerCfg.exe**.</span></span>

 

 



