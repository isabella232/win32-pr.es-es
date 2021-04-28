---
description: AppInit_DLLs en Windows 7 y Windows Server 2008 R2
ms.assetid: 6d1f9703-6dc9-4fdc-b52f-e6bb60a2fe8d
title: AppInit_DLLs en Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4820fcb9840bbec139ff78f3c6cc082b2dca4eeb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088713"
---
# <a name="appinit_dlls-in-windows-7-and-windows-server-2008-r2"></a><span data-ttu-id="33b81-103">Archivos DLL de AppInit \_ en Windows 7 y Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="33b81-103">AppInit\_DLLs in Windows 7 and Windows Server 2008 R2</span></span>

## <a name="platform"></a><span data-ttu-id="33b81-104">Plataforma</span><span class="sxs-lookup"><span data-stu-id="33b81-104">Platform</span></span>

<span data-ttu-id="33b81-105">**Clientes:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="33b81-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="33b81-106">**Servidores:** Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="33b81-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="33b81-107">Impacto en las características</span><span class="sxs-lookup"><span data-stu-id="33b81-107">Feature Impact</span></span>

 <span data-ttu-id="33b81-108">**Gravedad:** baja</span><span class="sxs-lookup"><span data-stu-id="33b81-108">**Severity** - Low</span></span>  
<span data-ttu-id="33b81-109">**Frecuencia:** baja</span><span class="sxs-lookup"><span data-stu-id="33b81-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="33b81-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="33b81-110">Description</span></span>

<span data-ttu-id="33b81-111">Los archivos DLL de AppInit son un mecanismo que permite cargar una lista arbitraria de archivos DLL en cada proceso de modo de usuario \_ del sistema.</span><span class="sxs-lookup"><span data-stu-id="33b81-111">AppInit\_DLLs is a mechanism that allows an arbitrary list of DLLs to be loaded into each user mode process on the system.</span></span> <span data-ttu-id="33b81-112">Microsoft está modificando la instalación de archivos DLL de AppInit en Windows 7 y Windows Server 2008 R2 para agregar un nuevo requisito de firma de código.</span><span class="sxs-lookup"><span data-stu-id="33b81-112">Microsoft is modifying the AppInit DLLs facility in Windows 7 and Windows Server 2008 R2 to add a new code-signing requirement.</span></span> <span data-ttu-id="33b81-113">Esto ayudará a mejorar la confiabilidad y el rendimiento del sistema, así como a mejorar la visibilidad del origen del software.</span><span class="sxs-lookup"><span data-stu-id="33b81-113">This will help improve the system reliability and performance, as well as improve visibility into the origin of software.</span></span>

## <a name="configuration"></a><span data-ttu-id="33b81-114">Configuración</span><span class="sxs-lookup"><span data-stu-id="33b81-114">Configuration</span></span>

<span data-ttu-id="33b81-115">Los valores almacenados en la clave HKEY LOCAL MACHINE SOFTWARE Microsoft Windows NT CurrentVersion windows en el Registro determinan el comportamiento de la \_ infraestructura de archivos DLL de \_ \\ \\ \\ \\ \\ \_ AppInit.</span><span class="sxs-lookup"><span data-stu-id="33b81-115">Values stored under the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion \\Windows key in the registry determine the behavior of the AppInit\_DLLs infrastructure.</span></span> <span data-ttu-id="33b81-116">En la tabla siguiente se describen estos valores del Registro:</span><span class="sxs-lookup"><span data-stu-id="33b81-116">The table below describes these registry values:</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="33b81-117">Valor</span><span class="sxs-lookup"><span data-stu-id="33b81-117">Value</span></span></th>
<th><span data-ttu-id="33b81-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="33b81-118">Description</span></span></th>
<th><span data-ttu-id="33b81-119">Valores de ejemplo</span><span class="sxs-lookup"><span data-stu-id="33b81-119">Sample Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="33b81-120">LoadAppInit_DLLs (REG_DWORD)${REMOVE}$</span><span class="sxs-lookup"><span data-stu-id="33b81-120">LoadAppInit_DLLs (REG_DWORD)${REMOVE}$</span></span><br />
</td>
<td rowspan="2"><span data-ttu-id="33b81-121">Habilita o deshabilita globalmente AppInit_DLLs.${REMOVE}$</span><span class="sxs-lookup"><span data-stu-id="33b81-121">Globally enables or disables AppInit_DLLs.${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="33b81-122">0x0: los AppInit_DLLs están deshabilitados.</span><span class="sxs-lookup"><span data-stu-id="33b81-122">0x0 – AppInit_DLLs are disabled.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33b81-123">0x1: AppInit_DLLs están habilitados.</span><span class="sxs-lookup"><span data-stu-id="33b81-123">0x1 – AppInit_DLLs are enabled.</span></span></td>


</tr>
<tr class="odd">
<td><span data-ttu-id="33b81-124">AppInit_DLLs (REG_SZ)</span><span class="sxs-lookup"><span data-stu-id="33b81-124">AppInit_DLLs (REG_SZ)</span></span></td>
<td><span data-ttu-id="33b81-125">Lista delimitada por espacios o comas de archivos DLL que se cargarán.</span><span class="sxs-lookup"><span data-stu-id="33b81-125">Space or comma delimited list of DLLs to load.</span></span> <span data-ttu-id="33b81-126">La ruta de acceso completa al archivo DLL debe especificarse mediante nombres cortos.</span><span class="sxs-lookup"><span data-stu-id="33b81-126">The complete path to the DLL should be specified using Short Names.</span></span></td>
<td><span data-ttu-id="33b81-127">C:\ PROGRA~1\WID288~1\MICROS~1.DLL</span><span class="sxs-lookup"><span data-stu-id="33b81-127">C:\ PROGRA~1\WID288~1\MICROS~1.DLL</span></span></td>
</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="33b81-128">RequireSignedAppInit_DLLs (REG_DWORD)${REMOVE}$</span><span class="sxs-lookup"><span data-stu-id="33b81-128">RequireSignedAppInit_DLLs (REG_DWORD)${REMOVE}$</span></span><br />
</td>
<td rowspan="2"><span data-ttu-id="33b81-129">Cargar solo archivos DLL firmados por código.${REMOVE}$</span><span class="sxs-lookup"><span data-stu-id="33b81-129">Only load code-signed DLLs.${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="33b81-130">0x0: cargue los archivos DLL.</span><span class="sxs-lookup"><span data-stu-id="33b81-130">0x0 – Load any DLLs.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33b81-131">0x1: cargue solo archivos DLL firmados por código.</span><span class="sxs-lookup"><span data-stu-id="33b81-131">0x1 – Load only code-signed DLLs.</span></span></td>


</tr>
</tbody>
</table>



 

<span data-ttu-id="33b81-132">**Windows 7**</span><span class="sxs-lookup"><span data-stu-id="33b81-132">**Windows 7**</span></span>

<span data-ttu-id="33b81-133">Todos los archivos DLL cargados por la infraestructura de archivos DLL de AppInit \_ deben estar firmados por código.</span><span class="sxs-lookup"><span data-stu-id="33b81-133">All DLLs that are loaded by the AppInit\_DLLs infrastructure should be code-signed.</span></span> <span data-ttu-id="33b81-134">En a favor de la compatibilidad de aplicaciones, el sistema operativo Windows 7 cargará todos los archivos DLL de AppInit.</span><span class="sxs-lookup"><span data-stu-id="33b81-134">In the interests of application compatibility, the Windows 7 Operating System will load all AppInit DLLs.</span></span> <span data-ttu-id="33b81-135">Sin embargo, Microsoft recomienda que todos los desarrolladores de aplicaciones firmen sus archivos DLL para ayudar a mejorar la confiabilidad de Windows y prepararse para el cumplimiento de la firma de código en versiones futuras de Windows.</span><span class="sxs-lookup"><span data-stu-id="33b81-135">However, Microsoft recommends that all application developers code-sign their DLLs to help improve the reliability of Windows and prepare for code-signing enforcement in future versions of Windows.</span></span> <span data-ttu-id="33b81-136">La clave del Registro RequireSignedAppInit controla este comportamiento y su valor en Windows 7 se establece \_ en 0 de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="33b81-136">The RequireSignedAppInit\_DLLs registry key controls this behavior and its value on Windows 7 is set to 0 by default.</span></span>

<span data-ttu-id="33b81-137">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="33b81-137">**Windows Server 2008 R2**</span></span>

<span data-ttu-id="33b81-138">Todos los archivos DLL cargados por la infraestructura de archivos DLL de AppInit \_ deben estar firmados por código.</span><span class="sxs-lookup"><span data-stu-id="33b81-138">All DLLs that are loaded by the AppInit\_DLLs infrastructure must be code-signed.</span></span> <span data-ttu-id="33b81-139">La clave del Registro RequireSignedAppInit controla este comportamiento y su valor en Windows Server 2008 R2 está establecido en \_ 1 de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="33b81-139">The RequireSignedAppInit\_DLLs registry key controls this behavior and its value on Windows Server 2008 R2 is set to 1 by default.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="33b81-140">Vínculos a otros recursos</span><span class="sxs-lookup"><span data-stu-id="33b81-140">Links to Other Resources</span></span>

<dl>

[<span data-ttu-id="33b81-141">Archivos DLL de AppInit en Windows 7 y Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="33b81-141">AppInit DLLs in Windows 7 and Windows Server 2008 R2</span></span>](/windows-hardware/drivers/install/)  
</dl>

 

 
