---
description: .
ms.assetid: 6d1f9703-6dc9-4fdc-b52f-e6bb60a2fe8d
title: AppInit_DLLs en Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31db695805b751e5dcd39293d0170c7fb78a11ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697784"
---
# <a name="appinit_dlls-in-windows-7-and-windows-server-2008-r2"></a><span data-ttu-id="39af2-103">\_Archivos dll de Appinit en Windows 7 y Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="39af2-103">AppInit\_DLLs in Windows 7 and Windows Server 2008 R2</span></span>

## <a name="platform"></a><span data-ttu-id="39af2-104">Plataforma</span><span class="sxs-lookup"><span data-stu-id="39af2-104">Platform</span></span>

<span data-ttu-id="39af2-105">**Clientes** : Windows 7</span><span class="sxs-lookup"><span data-stu-id="39af2-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="39af2-106">**Servidores** : Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="39af2-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="39af2-107">Impacto en las características</span><span class="sxs-lookup"><span data-stu-id="39af2-107">Feature Impact</span></span>

 <span data-ttu-id="39af2-108">**Gravedad** baja</span><span class="sxs-lookup"><span data-stu-id="39af2-108">**Severity** - Low</span></span>  
<span data-ttu-id="39af2-109">**Frecuencia** : baja</span><span class="sxs-lookup"><span data-stu-id="39af2-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="39af2-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="39af2-110">Description</span></span>

<span data-ttu-id="39af2-111">AppInit \_ dll es un mecanismo que permite cargar una lista arbitraria de archivos dll en cada proceso de modo de usuario del sistema.</span><span class="sxs-lookup"><span data-stu-id="39af2-111">AppInit\_DLLs is a mechanism that allows an arbitrary list of DLLs to be loaded into each user mode process on the system.</span></span> <span data-ttu-id="39af2-112">Microsoft está modificando la instalación de los archivos dll de AppInit en Windows 7 y Windows Server 2008 R2 para agregar un nuevo requisito de firma de código.</span><span class="sxs-lookup"><span data-stu-id="39af2-112">Microsoft is modifying the AppInit DLLs facility in Windows 7 and Windows Server 2008 R2 to add a new code-signing requirement.</span></span> <span data-ttu-id="39af2-113">Esto ayudará a mejorar la confiabilidad y el rendimiento del sistema, así como a mejorar la visibilidad del origen del software.</span><span class="sxs-lookup"><span data-stu-id="39af2-113">This will help improve the system reliability and performance, as well as improve visibility into the origin of software.</span></span>

## <a name="configuration"></a><span data-ttu-id="39af2-114">Configuración</span><span class="sxs-lookup"><span data-stu-id="39af2-114">Configuration</span></span>

<span data-ttu-id="39af2-115">Los valores almacenados en la \_ clave HKEY local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Windows en el registro determinan el comportamiento de la infraestructura de dll de Appinit \_ .</span><span class="sxs-lookup"><span data-stu-id="39af2-115">Values stored under the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion \\Windows key in the registry determine the behavior of the AppInit\_DLLs infrastructure.</span></span> <span data-ttu-id="39af2-116">En la tabla siguiente se describen estos valores del registro:</span><span class="sxs-lookup"><span data-stu-id="39af2-116">The table below describes these registry values:</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="39af2-117">Value</span><span class="sxs-lookup"><span data-stu-id="39af2-117">Value</span></span></th>
<th><span data-ttu-id="39af2-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="39af2-118">Description</span></span></th>
<th><span data-ttu-id="39af2-119">Valores de ejemplo</span><span class="sxs-lookup"><span data-stu-id="39af2-119">Sample Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="39af2-120">LoadAppInit_DLLs (REG_DWORD) $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="39af2-120">LoadAppInit_DLLs (REG_DWORD)${REMOVE}$</span></span><br />
</td>
<td rowspan="2"><span data-ttu-id="39af2-121">Habilita o deshabilita globalmente AppInit_DLLs. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="39af2-121">Globally enables or disables AppInit_DLLs.${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="39af2-122">0X0: AppInit_DLLs están deshabilitados.</span><span class="sxs-lookup"><span data-stu-id="39af2-122">0x0 – AppInit_DLLs are disabled.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="39af2-123">0x1: AppInit_DLLs están habilitadas.</span><span class="sxs-lookup"><span data-stu-id="39af2-123">0x1 – AppInit_DLLs are enabled.</span></span></td>


</tr>
<tr class="odd">
<td><span data-ttu-id="39af2-124">AppInit_DLLs (REG_SZ)</span><span class="sxs-lookup"><span data-stu-id="39af2-124">AppInit_DLLs (REG_SZ)</span></span></td>
<td><span data-ttu-id="39af2-125">Espacio o lista delimitada por comas de los archivos DLL que se van a cargar.</span><span class="sxs-lookup"><span data-stu-id="39af2-125">Space or comma delimited list of DLLs to load.</span></span> <span data-ttu-id="39af2-126">La ruta de acceso completa al archivo DLL debe especificarse mediante nombres cortos.</span><span class="sxs-lookup"><span data-stu-id="39af2-126">The complete path to the DLL should be specified using Short Names.</span></span></td>
<td><span data-ttu-id="39af2-127">C:\ PROGRAMA ~ 1 \ WID288 ~ 1 \ MICROS ~1.DLL</span><span class="sxs-lookup"><span data-stu-id="39af2-127">C:\ PROGRA~1\WID288~1\MICROS~1.DLL</span></span></td>
</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="39af2-128">RequireSignedAppInit_DLLs (REG_DWORD) $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="39af2-128">RequireSignedAppInit_DLLs (REG_DWORD)${REMOVE}$</span></span><br />
</td>
<td rowspan="2"><span data-ttu-id="39af2-129">Cargar solo archivos DLL con firma de código. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="39af2-129">Only load code-signed DLLs.${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="39af2-130">0X0: cargar cualquier dll.</span><span class="sxs-lookup"><span data-stu-id="39af2-130">0x0 – Load any DLLs.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="39af2-131">0x1: cargar solo archivos DLL con firma de código.</span><span class="sxs-lookup"><span data-stu-id="39af2-131">0x1 – Load only code-signed DLLs.</span></span></td>


</tr>
</tbody>
</table>



 

<span data-ttu-id="39af2-132">**Windows 7**</span><span class="sxs-lookup"><span data-stu-id="39af2-132">**Windows 7**</span></span>

<span data-ttu-id="39af2-133">Todos los archivos dll cargados por la \_ infraestructura de archivos dll de Appinit deben tener firma de código.</span><span class="sxs-lookup"><span data-stu-id="39af2-133">All DLLs that are loaded by the AppInit\_DLLs infrastructure should be code-signed.</span></span> <span data-ttu-id="39af2-134">En aras de la compatibilidad de aplicaciones, el sistema operativo Windows 7 cargará todos los archivos dll de AppInit.</span><span class="sxs-lookup"><span data-stu-id="39af2-134">In the interests of application compatibility, the Windows 7 Operating System will load all AppInit DLLs.</span></span> <span data-ttu-id="39af2-135">Sin embargo, Microsoft recomienda que todos los desarrolladores de aplicaciones firmen el código de los archivos DLL para ayudar a mejorar la confiabilidad de Windows y prepararse para el cumplimiento de la firma de código en versiones futuras de Windows.</span><span class="sxs-lookup"><span data-stu-id="39af2-135">However, Microsoft recommends that all application developers code-sign their DLLs to help improve the reliability of Windows and prepare for code-signing enforcement in future versions of Windows.</span></span> <span data-ttu-id="39af2-136">La \_ clave del registro RequireSignedAppInit DLL controla este comportamiento y su valor en Windows 7 se establece en 0 de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="39af2-136">The RequireSignedAppInit\_DLLs registry key controls this behavior and its value on Windows 7 is set to 0 by default.</span></span>

<span data-ttu-id="39af2-137">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="39af2-137">**Windows Server 2008 R2**</span></span>

<span data-ttu-id="39af2-138">Todos los archivos dll cargados por la \_ infraestructura de archivos dll de Appinit deben tener firma de código.</span><span class="sxs-lookup"><span data-stu-id="39af2-138">All DLLs that are loaded by the AppInit\_DLLs infrastructure must be code-signed.</span></span> <span data-ttu-id="39af2-139">La \_ clave del registro RequireSignedAppInit DLL controla este comportamiento y su valor en Windows Server 2008 R2 se establece en 1 de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="39af2-139">The RequireSignedAppInit\_DLLs registry key controls this behavior and its value on Windows Server 2008 R2 is set to 1 by default.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="39af2-140">Vínculos a otros recursos</span><span class="sxs-lookup"><span data-stu-id="39af2-140">Links to Other Resources</span></span>

<dl>

[<span data-ttu-id="39af2-141">Archivos dll de AppInit en Windows 7 y Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="39af2-141">AppInit DLLs in Windows 7 and Windows Server 2008 R2</span></span>](/windows-hardware/drivers/install/)  
</dl>

 

 
