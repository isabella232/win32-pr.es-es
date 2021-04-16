---
description: Instrumental de administración de Windows (WMI) es la infraestructura de datos y operaciones de administración en sistemas operativos basados en Windows.
ms.assetid: 4804152f-2042-4c6a-83c6-75c5e1ab7a04
ms.tgt_platform: multiple
title: Instrumental de administración de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ec2313ca7ee744ebe6f14be42a33e2e5878960b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696916"
---
# <a name="windows-management-instrumentation"></a><span data-ttu-id="2eede-103">Instrumental de administración de Windows</span><span class="sxs-lookup"><span data-stu-id="2eede-103">Windows Management Instrumentation</span></span>

## <a name="purpose"></a><span data-ttu-id="2eede-104">Propósito</span><span class="sxs-lookup"><span data-stu-id="2eede-104">Purpose</span></span>

<span data-ttu-id="2eede-105">Instrumental de administración de Windows (WMI) es la infraestructura de datos y operaciones de administración en sistemas operativos basados en Windows.</span><span class="sxs-lookup"><span data-stu-id="2eede-105">Windows Management Instrumentation (WMI) is the infrastructure for management data and operations on Windows-based operating systems.</span></span> <span data-ttu-id="2eede-106">Puede escribir scripts o aplicaciones de WMI para automatizar las tareas administrativas en equipos remotos, pero WMI también proporciona datos de administración a otras partes del sistema operativo y los productos, por ejemplo System Center Operations Manager, anteriormente Microsoft Operations Manager (MOM) o Administración remota de Windows ([WinRM](/windows/desktop/WinRM/portal)).</span><span class="sxs-lookup"><span data-stu-id="2eede-106">You can write WMI scripts or applications to automate administrative tasks on remote computers but WMI also supplies management data to other parts of the operating system and products, for example System Center Operations Manager, formerly Microsoft Operations Manager (MOM), or Windows Remote Management ([WinRM](/windows/desktop/WinRM/portal)).</span></span>

> [!Note]  
> <span data-ttu-id="2eede-107">La siguiente documentación está dirigida a desarrolladores y administradores de ti.</span><span class="sxs-lookup"><span data-stu-id="2eede-107">The following documentation is targeted for developers and IT administrators.</span></span> <span data-ttu-id="2eede-108">Si es un usuario final que ha experimentado un mensaje de error relacionado con WMI, debe ir a [soporte técnico de Microsoft](https://support.microsoft.com/) y buscar el código de error que aparece en el mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="2eede-108">If you are an end-user that has experienced an error message concerning WMI, you should go to [Microsoft Support](https://support.microsoft.com/) and search for the error code you see on the error message.</span></span> <span data-ttu-id="2eede-109">Para obtener más información acerca de la solución de problemas con los scripts WMI y el servicio WMI, vea [WMI no funciona.](/previous-versions/tn-archive/ff406382(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="2eede-109">For more information about troubleshooting problems with WMI scripts and the WMI service, see [WMI Isn't Working!](/previous-versions/tn-archive/ff406382(v=msdn.10))</span></span>

 

> [!Note]  
> <span data-ttu-id="2eede-110">WMI es totalmente compatible con Microsoft; sin embargo, la versión más reciente del control y scripting administrativo está disponible a través de la infraestructura de administración de Windows (MI).</span><span class="sxs-lookup"><span data-stu-id="2eede-110">WMI is fully supported by Microsoft; however, the latest version of administrative scripting and control is available through the Windows Management Infrastructure (MI).</span></span> <span data-ttu-id="2eede-111">MI es totalmente compatible con las versiones anteriores de WMI y proporciona un host de características y ventajas que facilitan el diseño y el desarrollo de proveedores y clientes.</span><span class="sxs-lookup"><span data-stu-id="2eede-111">MI is fully compatible with previous versions of WMI, and provides a host of features and benefits that make designing and developing providers and clients easier than ever.</span></span> <span data-ttu-id="2eede-112">Para obtener más información, consulte [infraestructura de administración de Windows (mi)](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure).</span><span class="sxs-lookup"><span data-stu-id="2eede-112">For more information, see [Windows Management Infrastructure (MI)](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure).</span></span>

 

## <a name="where-applicable"></a><span data-ttu-id="2eede-113">Donde sea aplicable</span><span class="sxs-lookup"><span data-stu-id="2eede-113">Where applicable</span></span>

<span data-ttu-id="2eede-114">WMI se puede usar en todas las aplicaciones basadas en Windows y es muy útil en aplicaciones empresariales y scripts administrativos.</span><span class="sxs-lookup"><span data-stu-id="2eede-114">WMI can be used in all Windows-based applications, and is most useful in enterprise applications and administrative scripts.</span></span>

<span data-ttu-id="2eede-115">Los administradores del sistema pueden encontrar información sobre el uso de WMI en TechNet [ScriptCenter](https://www.microsoft.com/technet/scriptcenter/default.mspx)y en varios libros sobre WMI.</span><span class="sxs-lookup"><span data-stu-id="2eede-115">System administrators can find information about using WMI at the TechNet [ScriptCenter](https://www.microsoft.com/technet/scriptcenter/default.mspx), and in various books about WMI.</span></span> <span data-ttu-id="2eede-116">Para obtener más información, vea más [información](further-information.md).</span><span class="sxs-lookup"><span data-stu-id="2eede-116">For more information, see [Further Information](further-information.md).</span></span>

## <a name="developer-audience"></a><span data-ttu-id="2eede-117">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="2eede-117">Developer audience</span></span>

<span data-ttu-id="2eede-118">WMI está diseñado para los programadores que utilizan C/C++, la aplicación de Microsoft Visual Basic o un lenguaje de scripting que tiene un motor de Windows y controla los objetos de Microsoft ActiveX.</span><span class="sxs-lookup"><span data-stu-id="2eede-118">WMI is designed for programmers who use C/C++, the Microsoft Visual Basic application, or a scripting language that has an engine on Windows and handles Microsoft ActiveX objects.</span></span> <span data-ttu-id="2eede-119">Aunque es útil cierta familiaridad con la programación COM, los desarrolladores de C++ que escriben aplicaciones pueden encontrar buenos ejemplos para empezar a [crear una aplicación WMI con C++](creating-a-wmi-application-using-c-.md).</span><span class="sxs-lookup"><span data-stu-id="2eede-119">While some familiarity with COM programming is helpful, C++ developers who are writing applications can find good examples for getting started at [Creating a WMI Application Using C++](creating-a-wmi-application-using-c-.md).</span></span>

<span data-ttu-id="2eede-120">Para desarrollar proveedores de código administrados o aplicaciones en C# o Visual Basic .NET mediante el .NET Framework, vea [WMI en .NET Framework](/previous-versions/dotnet/netframework-1.1/aa720264(v=vs.71)).</span><span class="sxs-lookup"><span data-stu-id="2eede-120">To develop managed code providers or applications in C# or Visual Basic .NET using the .NET Framework, see [WMI in .NET Framework](/previous-versions/dotnet/netframework-1.1/aa720264(v=vs.71)).</span></span>

<span data-ttu-id="2eede-121">Muchos administradores y profesionales de ti acceden a WMI a través de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2eede-121">Many administrators and IT professionals access WMI through PowerShell.</span></span> <span data-ttu-id="2eede-122">El cmdlet Get-WMI para PowerShell permite recuperar información de un repositorio de WMI local o remoto.</span><span class="sxs-lookup"><span data-stu-id="2eede-122">The Get-WMI cmdlet for PowerShell enables you to retrieve information for a local or remote WMI repository.</span></span> <span data-ttu-id="2eede-123">Como tal, una serie de temas y clases, especialmente en la sección [creación de clientes WMI](creating-wmi-clients.md) , contiene ejemplos de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2eede-123">As such, a number of topics and classes, especially in the [Creating WMI Clients](creating-wmi-clients.md) section, contain PowerShell examples.</span></span> <span data-ttu-id="2eede-124">Para obtener información adicional sobre el uso de PowerShell, vea [Windows PowerShell](https://msdn.microsoft.com/library/dd835506.aspx) y [scripting con Windows PowerShell](https://technet.microsoft.com/library/bb978526.aspx).</span><span class="sxs-lookup"><span data-stu-id="2eede-124">For additional information on using PowerShell, see [Windows PowerShell](https://msdn.microsoft.com/library/dd835506.aspx) and [Scripting with Windows PowerShell](https://technet.microsoft.com/library/bb978526.aspx).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="2eede-125">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="2eede-125">Run-time requirements</span></span>

<span data-ttu-id="2eede-126">Para obtener más información sobre qué sistema operativo se requiere para utilizar un elemento de API específico o una clase WMI, consulte la sección de requisitos de cada tema en la documentación de WMI.</span><span class="sxs-lookup"><span data-stu-id="2eede-126">For more information about which operating system is required to use a specific API element or WMI class, see the Requirements section of each topic in the WMI documentation.</span></span>

<span data-ttu-id="2eede-127">Si parece que falta un componente esperado, consulte [disponibilidad del sistema operativo de los componentes de WMI](operating-system-availability-of-wmi-components.md).</span><span class="sxs-lookup"><span data-stu-id="2eede-127">If an expected component appears to be missing, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

<span data-ttu-id="2eede-128">No es necesario descargar ni instalar un desarrollo de software (SDK) específico para crear scripts o aplicaciones para WMI.</span><span class="sxs-lookup"><span data-stu-id="2eede-128">You do not need to download or install a specific software development (SDK) in order to create scripts or applications for WMI.</span></span> <span data-ttu-id="2eede-129">Sin embargo, hay algunas herramientas administrativas de WMI que los desarrolladores pueden encontrar útiles.</span><span class="sxs-lookup"><span data-stu-id="2eede-129">However, there are some WMI administrative tools that developers find useful.</span></span> <span data-ttu-id="2eede-130">Para obtener más información, consulte la sección descargas en [información adicional](further-information.md).</span><span class="sxs-lookup"><span data-stu-id="2eede-130">For more information, see the Downloads section in [Further Information](further-information.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2eede-131">En esta sección</span><span class="sxs-lookup"><span data-stu-id="2eede-131">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="2eede-132">Acerca de WMI</span><span class="sxs-lookup"><span data-stu-id="2eede-132">About WMI</span></span>](about-wmi.md)
</dt> <dd>

<span data-ttu-id="2eede-133">Información general sobre WMI.</span><span class="sxs-lookup"><span data-stu-id="2eede-133">General information about WMI.</span></span>

</dd> <dt>

[<span data-ttu-id="2eede-134">Usar WMI</span><span class="sxs-lookup"><span data-stu-id="2eede-134">Using WMI</span></span>](using-wmi.md)
</dt> <dd>

<span data-ttu-id="2eede-135">Información sobre cómo desarrollar aplicaciones para usar WMI, que incluye información sobre las herramientas.</span><span class="sxs-lookup"><span data-stu-id="2eede-135">Information about how to develop applications to use WMI, which includes information about tools.</span></span>

</dd> <dt>

[<span data-ttu-id="2eede-136">Referencia de WMI</span><span class="sxs-lookup"><span data-stu-id="2eede-136">WMI Reference</span></span>](wmi-reference.md)
</dt> <dd>

<span data-ttu-id="2eede-137">Documentación acerca de las clases de WMI, clases de C++ de WMI, API COM de WMI, API de scripting y otro material de referencia de WMI.</span><span class="sxs-lookup"><span data-stu-id="2eede-137">Documentation about the WMI classes, WMI C++ classes, WMI COM API, Scripting API, and other WMI reference material.</span></span>

</dd> </dl>

 

 
