---
description: Referencia administrada para las clases de comandos de Windows PowerShell de WMI
ms.assetid: 30e77956-8428-4259-9218-b93f143fd987
ms.tgt_platform: multiple
title: Referencia administrada para las clases de comandos de Windows PowerShell de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb309a9ca421a3966f84ba1ae825bd0c81eee8ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697541"
---
# <a name="managed-reference-for-wmi-windows-powershell-command-classes"></a><span data-ttu-id="fd31c-103">Referencia administrada para las clases de comandos de Windows PowerShell de WMI</span><span class="sxs-lookup"><span data-stu-id="fd31c-103">Managed Reference for WMI Windows PowerShell Command Classes</span></span>

<span data-ttu-id="fd31c-104">Windows PowerShell implementa la funcionalidad de Instrumental de administración de Windows (WMI) a través de un conjunto de cmdlets.</span><span class="sxs-lookup"><span data-stu-id="fd31c-104">Windows PowerShell implements Windows Management Instrumentation (WMI) functionality through a set of cmdlets.</span></span> <span data-ttu-id="fd31c-105">Puede usar estos cmdlets para completar las tareas de un extremo a otro que son necesarias para administrar equipos locales y remotos.</span><span class="sxs-lookup"><span data-stu-id="fd31c-105">You can use these cmdlets to complete the end-to-end tasks that are necessary to manage local and remote computers.</span></span>

<span data-ttu-id="fd31c-106">Consulte [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="fd31c-106">See [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx) for more information.</span></span>

## <a name="wmi-powershell-classes"></a><span data-ttu-id="fd31c-107">Clases de PowerShell de WMI</span><span class="sxs-lookup"><span data-stu-id="fd31c-107">WMI PowerShell Classes</span></span>

<span data-ttu-id="fd31c-108">**Espacio de nombres**: Microsoft. PowerShell. Commands</span><span class="sxs-lookup"><span data-stu-id="fd31c-108">**Namespace**: Microsoft.PowerShell.Commands</span></span>

<span data-ttu-id="fd31c-109">**Ensamblado**: Microsoft. PowerShell. Commands. Management</span><span class="sxs-lookup"><span data-stu-id="fd31c-109">**Assembly**: Microsoft.PowerShell.Commands.Management</span></span>

<span data-ttu-id="fd31c-110">**Dll**: Microsoft.PowerShell.Commands.Management.dll</span><span class="sxs-lookup"><span data-stu-id="fd31c-110">**DLL**: Microsoft.PowerShell.Commands.Management.dll</span></span>

<span data-ttu-id="fd31c-111">Windows PowerShell implementa estas clases de comandos WMI.</span><span class="sxs-lookup"><span data-stu-id="fd31c-111">These WMI command classes are implemented by Windows PowerShell.</span></span> <span data-ttu-id="fd31c-112">Estas clases se incluyen en este kit de desarrollo de software (SDK) solo para integridad.</span><span class="sxs-lookup"><span data-stu-id="fd31c-112">These classes are included in this software development kit (SDK) for completeness only.</span></span> <span data-ttu-id="fd31c-113">Los miembros de estas clases no se pueden usar directamente, ni deben usarse para derivar otras clases.</span><span class="sxs-lookup"><span data-stu-id="fd31c-113">The members of these classes cannot be used directly, nor should they be used to derive other classes.</span></span>



| <span data-ttu-id="fd31c-114">Clase</span><span class="sxs-lookup"><span data-stu-id="fd31c-114">Class</span></span>                   | <span data-ttu-id="fd31c-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="fd31c-115">Description</span></span>                                                                                                                                                                                                                                 |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd31c-116">GetWmiObjectCommand</span><span class="sxs-lookup"><span data-stu-id="fd31c-116">GetWmiObjectCommand</span></span>     | <span data-ttu-id="fd31c-117">Obtiene instancias de clases WMI o información sobre las clases disponibles.</span><span class="sxs-lookup"><span data-stu-id="fd31c-117">Gets instances of WMI classes or information about the available classes.</span></span><br/> <span data-ttu-id="fd31c-118">Consulte el cmdlet [Get-WMIObject](/previous-versions//dd315295(v=technet.10)) para obtener ejemplos e información detallada sobre los parámetros.</span><span class="sxs-lookup"><span data-stu-id="fd31c-118">See the [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) cmdlet for examples and detailed information about the parameters.</span></span><br/> |
| <span data-ttu-id="fd31c-119">InvokeWmiMethod</span><span class="sxs-lookup"><span data-stu-id="fd31c-119">InvokeWmiMethod</span></span>         | <span data-ttu-id="fd31c-120">Llama a los métodos de WMI.</span><span class="sxs-lookup"><span data-stu-id="fd31c-120">Calls WMI methods.</span></span><br/> <span data-ttu-id="fd31c-121">Consulte el cmdlet [Invoke-WmiMethod](/previous-versions//dd315300(v=technet.10)) para obtener ejemplos e información detallada sobre los parámetros.</span><span class="sxs-lookup"><span data-stu-id="fd31c-121">See the [Invoke-WmiMethod](/previous-versions//dd315300(v=technet.10)) cmdlet for examples and detailed information about the parameters.</span></span><br/>                                                     |
| <span data-ttu-id="fd31c-122">RegisterWmiEventCommand</span><span class="sxs-lookup"><span data-stu-id="fd31c-122">RegisterWmiEventCommand</span></span> | <span data-ttu-id="fd31c-123">Se suscribe a un evento WMI.</span><span class="sxs-lookup"><span data-stu-id="fd31c-123">Subscribes to a WMI event.</span></span><br/> <span data-ttu-id="fd31c-124">Consulte el cmdlet [Register-WmiEvent](/previous-versions//dd315242(v=technet.10)) para obtener ejemplos e información detallada sobre los parámetros.</span><span class="sxs-lookup"><span data-stu-id="fd31c-124">See the [Register-WmiEvent](/previous-versions//dd315242(v=technet.10)) cmdlet for examples and detailed information about the parameters.</span></span><br/>                                            |
| <span data-ttu-id="fd31c-125">RemoveWmiObject</span><span class="sxs-lookup"><span data-stu-id="fd31c-125">RemoveWmiObject</span></span>         | <span data-ttu-id="fd31c-126">Elimina una instancia de una clase WMI existente.</span><span class="sxs-lookup"><span data-stu-id="fd31c-126">Deletes an instance of an existing WMI class.</span></span><br/> <span data-ttu-id="fd31c-127">Consulte el cmdlet [Remove-WMIObject](/previous-versions//dd347605(v=technet.10)) para obtener ejemplos e información detallada sobre los parámetros.</span><span class="sxs-lookup"><span data-stu-id="fd31c-127">See the [Remove-WmiObject](/previous-versions//dd347605(v=technet.10)) cmdlet for examples and detailed information about the parameters.</span></span><br/>                          |
| <span data-ttu-id="fd31c-128">SetWmiInstance</span><span class="sxs-lookup"><span data-stu-id="fd31c-128">SetWmiInstance</span></span>          | <span data-ttu-id="fd31c-129">Crea o actualiza una instancia de una clase WMI existente.</span><span class="sxs-lookup"><span data-stu-id="fd31c-129">Creates or updates an instance of an existing WMI class.</span></span><br/> <span data-ttu-id="fd31c-130">Consulte el cmdlet [set-WmiInstance](/previous-versions//dd315391(v=technet.10)) para obtener ejemplos e información detallada sobre los parámetros.</span><span class="sxs-lookup"><span data-stu-id="fd31c-130">See the [Set-WmiInstance](/previous-versions//dd315391(v=technet.10)) cmdlet for examples and detailed information about the parameters.</span></span><br/>                |



 

 

