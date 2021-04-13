---
description: Los scripts pueden tener acceso a todas las clases WMI para objetos de hardware y software.
ms.assetid: dbb29bc8-a675-4538-99f4-00613c83eeaa
ms.tgt_platform: multiple
title: Acceso de script a WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd487c127c670f9ddee9596e44c4b2b9691ed880
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276141"
---
# <a name="scripting-access-to-wmi"></a><span data-ttu-id="79e2d-103">Acceso de script a WMI</span><span class="sxs-lookup"><span data-stu-id="79e2d-103">Scripting Access to WMI</span></span>

<span data-ttu-id="79e2d-104">Los scripts pueden tener acceso a todas las clases WMI para objetos de hardware y software.</span><span class="sxs-lookup"><span data-stu-id="79e2d-104">Scripts can access all WMI classes for hardware and software objects.</span></span> <span data-ttu-id="79e2d-105">Los scripts de Windows Script Host (WSH) pueden realizar operaciones en objetos del sistema de archivos, manipular impresoras de red o cambiar variables de entorno.</span><span class="sxs-lookup"><span data-stu-id="79e2d-105">Windows Script Host (WSH) scripts can perform operations on file system objects, manipulate network printers, or change environment variables.</span></span> <span data-ttu-id="79e2d-106">Puede encontrar una variedad de tareas de administrador e instrucciones breves sobre cómo realizarlas en WMI en [tareas WMI para scripts y aplicaciones](wmi-tasks-for-scripts-and-applications.md).</span><span class="sxs-lookup"><span data-stu-id="79e2d-106">You can find a variety of administrator tasks and brief guidance on how to accomplish them in WMI at [WMI Tasks for Scripts and Applications](wmi-tasks-for-scripts-and-applications.md).</span></span> <span data-ttu-id="79e2d-107">Para obtener más información y ejemplos, vea el [repositorio de scripts](https://www.microsoft.com/technet/scriptcenter/scripts/default.mspx)de TechNet ScriptCenter.</span><span class="sxs-lookup"><span data-stu-id="79e2d-107">For more information and examples, see the TechNet ScriptCenter [Script Repository](https://www.microsoft.com/technet/scriptcenter/scripts/default.mspx).</span></span>

<span data-ttu-id="79e2d-108">Si no está familiarizado con el scripting o con el scripting específico de WMI, consulte la sección TechNet ScriptCenter [Introducción](https://www.microsoft.com/technet/scriptcenter/hubs/start.mspx).</span><span class="sxs-lookup"><span data-stu-id="79e2d-108">If you are new to scripting or to WMI-specific scripting, see the TechNet ScriptCenter section [Getting Started](https://www.microsoft.com/technet/scriptcenter/hubs/start.mspx).</span></span>

<span data-ttu-id="79e2d-109">Con la [API de scripting para WMI](scripting-api-for-wmi.md), puede desarrollar scripts rápidos, sencillos o aplicaciones complejas.</span><span class="sxs-lookup"><span data-stu-id="79e2d-109">With the [Scripting API for WMI](scripting-api-for-wmi.md), you can develop quick, simple scripts or complex applications.</span></span> <span data-ttu-id="79e2d-110">Scripting ofrece la misma capacidad de obtener información o de configurar la mayoría de los objetos de una empresa como lo haría con una aplicación de C++ o C#.</span><span class="sxs-lookup"><span data-stu-id="79e2d-110">Scripting gives you the same capability of getting information or of configuring most objects in an enterprise as you would have through a C++ or C# application.</span></span> <span data-ttu-id="79e2d-111">Para obtener más información, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="79e2d-111">For more information, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="79e2d-112">No se puede escribir un [*proveedor WMI*](gloss-p.md) en el script.</span><span class="sxs-lookup"><span data-stu-id="79e2d-112">You cannot write a [*WMI provider*](gloss-p.md) in script.</span></span> <span data-ttu-id="79e2d-113">Para obtener más información, consulte [proporcionar datos a WMI](providing-data-to-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="79e2d-113">For more information, see [Providing Data to WMI](providing-data-to-wmi.md).</span></span>

<span data-ttu-id="79e2d-114">Los scripts de WMI se pueden escribir en cualquier lenguaje de scripting que pueda interactuar con objetos ActiveX.</span><span class="sxs-lookup"><span data-stu-id="79e2d-114">WMI scripts can be written in any scripting language that can interact with ActiveX objects.</span></span>

<span data-ttu-id="79e2d-115">Windows PowerShell proporciona un entorno sencillo para la administración y el scripting de WMI.</span><span class="sxs-lookup"><span data-stu-id="79e2d-115">Windows PowerShell provides a simple environment for WMI administration and scripting.</span></span> <span data-ttu-id="79e2d-116">Para obtener más información sobre PowerShell, vea [Introducción con Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="79e2d-116">For more information about PowerShell, see [Getting Started with Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7&preserve-view=true).</span></span>

<span data-ttu-id="79e2d-117">Active Directory scripts de interfaces de servicio (ADSI) proporciona acceso a objetos de Active Directory Domain Services (AD DS).</span><span class="sxs-lookup"><span data-stu-id="79e2d-117">Active Directory Service Interfaces (ADSI) scripts provides access to Active Directory Domain Services (AD DS) objects.</span></span> <span data-ttu-id="79e2d-118">Tanto los scripts de WSH como ADSI tienen acceso a objetos y permiten procedimientos no disponibles a través de archivos por lotes.</span><span class="sxs-lookup"><span data-stu-id="79e2d-118">Both WSH and ADSI scripts access objects and allow procedures not available through batch files.</span></span>

## <a name="related-topics"></a><span data-ttu-id="79e2d-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="79e2d-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79e2d-120">Acerca de WMI</span><span class="sxs-lookup"><span data-stu-id="79e2d-120">About WMI</span></span>](about-wmi.md)
</dt> <dt>

[<span data-ttu-id="79e2d-121">API de scripting para WMI</span><span class="sxs-lookup"><span data-stu-id="79e2d-121">Scripting API for WMI</span></span>](scripting-api-for-wmi.md)
</dt> </dl>

 

 
