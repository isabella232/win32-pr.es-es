---
description: Wmiadap es una aplicación que se ejecuta en Windows y que puede actualizar la información de rendimiento en el repositorio WMI.
ms.assetid: 459fe19e-3e2e-4a58-b3e7-75fd285f7389
ms.tgt_platform: multiple
title: wmiadap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa5d2de65e8566283b341c5af52048cc79cc0299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279278"
---
# <a name="wmiadap"></a><span data-ttu-id="c8ec5-103">wmiadap</span><span class="sxs-lookup"><span data-stu-id="c8ec5-103">wmiadap</span></span>

<span data-ttu-id="c8ec5-104">Wmiadap es una aplicación que se ejecuta en Windows y que puede actualizar la información de rendimiento en el repositorio WMI.</span><span class="sxs-lookup"><span data-stu-id="c8ec5-104">Wmiadap is a application that runs on Windows that can update performance information in the WMI repository.</span></span> <span data-ttu-id="c8ec5-105">Por lo general, esto permite a los desarrolladores y administradores de ti crear scripts que tengan acceso a información de rendimiento, como la cantidad de memoria utilizada por una aplicación.</span><span class="sxs-lookup"><span data-stu-id="c8ec5-105">Generally, this allows developers and IT Administrators to create scripts that access performance information, such as the amount of memory used by an application.</span></span> <span data-ttu-id="c8ec5-106">En el siguiente tema se describe la interfaz de la línea de comandos que puede usar para controlar cómo wmiadap recupera la información.</span><span class="sxs-lookup"><span data-stu-id="c8ec5-106">The following topic describes the command-line interface you can use to control how wmiadap retrieves information.</span></span>

<span data-ttu-id="c8ec5-107">Wmiadap se instala con el sistema operativo en la mayoría de los sistemas, en el directorio C: \\ Windows \\ system32 \\ WBEM.</span><span class="sxs-lookup"><span data-stu-id="c8ec5-107">Wmiadap is installed with the operating system on most systems, in the C:\\Windows\\System32\\wbem directory.</span></span> <span data-ttu-id="c8ec5-108">Si ve mensajes de error relacionados con wmiadap.exe, busque [soporte técnico de Microsoft](https://support.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="c8ec5-108">If you are seeing error messages concerning wmiadap.exe, search [Microsoft Support](https://support.microsoft.com/).</span></span> <span data-ttu-id="c8ec5-109">Por lo general, no debe eliminar wmiadap.exe del sistema, a menos que se indique lo contrario.</span><span class="sxs-lookup"><span data-stu-id="c8ec5-109">Generally, you should not delete wmiadap.exe from your system, unless otherwise instructed.</span></span>

<span data-ttu-id="c8ec5-110">La transferencia de datos de las bibliotecas de rendimiento y la actualización de clases derivadas de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) y [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) se realiza mediante los proveedores [WmiPerfClass](wmi-providers.md) y [WMIPerfInst](wmi-providers.md) .</span><span class="sxs-lookup"><span data-stu-id="c8ec5-110">The transfer of data from the performance libraries and the refresh of classes derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) and [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) is done by the [WmiPerfClass](wmi-providers.md) and [WMIPerfInst](wmi-providers.md) providers.</span></span> <span data-ttu-id="c8ec5-111">El proveedor WmiPerfClass actualiza [las clases de contador de rendimiento](/windows/desktop/CIMWin32Prov/performance-counter-classes) de WMI solo cuando se agrega un nuevo objeto de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="c8ec5-111">The WmiPerfClass provider updates WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes) only when a new performance object is added.</span></span> <span data-ttu-id="c8ec5-112">Todavía puede ejecutar Wmiadap con el modificador **/r** para analizar los controladores de modelo de controlador de Windows para crear objetos de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="c8ec5-112">You still can run Wmiadap with the **/r** switch to parse the Windows Driver Model drivers to create performance objects.</span></span> <span data-ttu-id="c8ec5-113">El modificador **/f** todavía fuerza una actualización de las clases WMI de las bibliotecas de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="c8ec5-113">The **/f** switch still forces an update of the WMI classes from the performance libraries.</span></span>

<span data-ttu-id="c8ec5-114">Los siguientes modificadores están disponibles en el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="c8ec5-114">The following switches are available at the command prompt.</span></span>

<span data-ttu-id="c8ec5-115">**wmiadap** \[  \] /f \[ **/r**\]</span><span class="sxs-lookup"><span data-stu-id="c8ec5-115">**wmiadap** \[**/f**\]\[**/r**\]</span></span>

## <a name="switches"></a><span data-ttu-id="c8ec5-116">Conmutadores</span><span class="sxs-lookup"><span data-stu-id="c8ec5-116">Switches</span></span>

<dl> <dt>

<span data-ttu-id="c8ec5-117"><span id="_f"></span><span id="_F"></span>**/f**</span><span class="sxs-lookup"><span data-stu-id="c8ec5-117"><span id="_f"></span><span id="_F"></span>**/f**</span></span>
</dt> <dd>

<span data-ttu-id="c8ec5-118">Analiza todas las bibliotecas de rendimiento en el sistema y actualiza las clases derivadas de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) y [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span><span class="sxs-lookup"><span data-stu-id="c8ec5-118">Parses all the performance libraries on the system and refreshes the classes derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) and [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span>

</dd> <dt>

<span data-ttu-id="c8ec5-119"><span id="_r"></span><span id="_R"></span>**/r**</span><span class="sxs-lookup"><span data-stu-id="c8ec5-119"><span id="_r"></span><span id="_R"></span>**/r**</span></span>
</dt> <dd>

<span data-ttu-id="c8ec5-120">Analiza todos los controladores de Modelo de controlador de Windows del sistema para crear objetos de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="c8ec5-120">Parses all the Windows Driver Model drivers on the system to create performance objects.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="c8ec5-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="c8ec5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8ec5-122">Bibliotecas de rendimiento y WMI</span><span class="sxs-lookup"><span data-stu-id="c8ec5-122">Performance Libraries and WMI</span></span>](performance-libraries-and-wmi.md)
</dt> <dt>

[<span data-ttu-id="c8ec5-123">**WinMgmt**</span><span class="sxs-lookup"><span data-stu-id="c8ec5-123">**winmgmt**</span></span>](winmgmt.md)
</dt> </dl>

 

 
