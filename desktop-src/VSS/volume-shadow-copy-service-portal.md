---
description: Copia de seguridad de volúmenes mientras las aplicaciones de un sistema siguen escribiendo en los volúmenes. Minimice el tiempo de inactividad de la aplicación mediante la creación rápida de una instantánea (instantánea) de un volumen que duplica todos los datos. Realice una copia de seguridad multivolume.
ms.assetid: 1eca1e3e-fc86-44b5-b3c4-bcee41bc5a43
title: Servicio de instantáneas de volumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2159d39f407f7ae5dbde454ab6cf3562307d892c
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443086"
---
# <a name="volume-shadow-copy-service"></a><span data-ttu-id="d2318-105">Servicio de instantáneas de volumen</span><span class="sxs-lookup"><span data-stu-id="d2318-105">Volume Shadow Copy Service</span></span>

## <a name="purpose"></a><span data-ttu-id="d2318-106">Propósito</span><span class="sxs-lookup"><span data-stu-id="d2318-106">Purpose</span></span>

<span data-ttu-id="d2318-107">El Servicio de instantáneas de volumen (VSS) es un conjunto de interfaces COM que implementa un marco para permitir realizar copias de seguridad de volúmenes mientras las aplicaciones de un sistema siguen escribiendo en los volúmenes.</span><span class="sxs-lookup"><span data-stu-id="d2318-107">The Volume Shadow Copy Service (VSS) is a set of COM interfaces that implements a framework to allow volume backups to be performed while applications on a system continue to write to the volumes.</span></span>

<span data-ttu-id="d2318-108">Para obtener una introducción a VSS para administradores del sistema, [consulte Servicio de instantáneas de volumen](/windows-server/storage/file-server/volume-shadow-copy-service) en la biblioteca de TechNet.</span><span class="sxs-lookup"><span data-stu-id="d2318-108">For an introduction to VSS for system administrators, see [Volume Shadow Copy Service](/windows-server/storage/file-server/volume-shadow-copy-service) in the TechNet Library.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="d2318-109">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="d2318-109">Run-time requirements</span></span>

<span data-ttu-id="d2318-110">VSS es compatible con Microsoft Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d2318-110">VSS is supported on Microsoft Windows XP and later.</span></span> <span data-ttu-id="d2318-111">Para obtener información sobre los requisitos en tiempo de ejecución para un elemento de programación determinado, vea la sección Requisitos de la documentación de ese elemento.</span><span class="sxs-lookup"><span data-stu-id="d2318-111">For information about run-time requirements for a particular programming element, see the Requirements section of the documentation for that element.</span></span>

<span data-ttu-id="d2318-112">Todas las aplicaciones VSS de 32 bits (solicitantes, proveedores y escritores) deben ejecutarse como aplicaciones nativas de 32 o 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d2318-112">All 32-bit VSS applications (requesters, providers, and writers) must run as native 32-bit or 64-bit applications.</span></span> <span data-ttu-id="d2318-113">No se admite su ejecución en WOW64.</span><span class="sxs-lookup"><span data-stu-id="d2318-113">Running them under WOW64 is not supported.</span></span> <span data-ttu-id="d2318-114">Para obtener más información, [vea Configuraciones y restricciones admitidas.](usage-conventions.md)</span><span class="sxs-lookup"><span data-stu-id="d2318-114">For more information, see [Supported Configurations and Restrictions](usage-conventions.md).</span></span>

<span data-ttu-id="d2318-115">**Windows Server 2003 y Windows XP:** Se admite la ejecución de solicitantes de VSS de 32 bits en WOW64, pero no para copias de seguridad de estado del sistema.</span><span class="sxs-lookup"><span data-stu-id="d2318-115">**Windows Server 2003 and Windows XP:** Running 32-bit VSS requesters under WOW64 is supported, but not for system-state backups.</span></span> <span data-ttu-id="d2318-116">No se admite la ejecución de escritores y proveedores de VSS de 32 bits en WOW64.</span><span class="sxs-lookup"><span data-stu-id="d2318-116">Running 32-bit VSS providers and writers under WOW64 is not supported.</span></span> <span data-ttu-id="d2318-117">Se quitó la compatibilidad con la ejecución de solicitantes de 32 bits en WOW64 en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d2318-117">Support for running 32-bit requesters under WOW64 was removed in Windows Vista and subsequent versions.</span></span>

> [!Note]  
> <span data-ttu-id="d2318-118">No se puede usar una instantánea creada en Windows Server 2003 R2 o Windows Server 2003 en un equipo que ejecute Windows Server 2008 R2 o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="d2318-118">A shadow copy that was created on Windows Server 2003 R2 or Windows Server 2003 cannot be used on a computer that is running Windows Server 2008 R2 or Windows Server 2008.</span></span> <span data-ttu-id="d2318-119">No se puede usar una instantánea creada en Windows Server 2008 R2 o Windows Server 2008 en un equipo que ejecute Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d2318-119">A shadow copy that was created on Windows Server 2008 R2 or Windows Server 2008 cannot be used on a computer that is running Windows Server 2003.</span></span> <span data-ttu-id="d2318-120">Sin embargo, una instantánea que se creó en Windows Server 2008 se puede usar en un equipo que ejecuta Windows Server 2008 R2 y viceversa.</span><span class="sxs-lookup"><span data-stu-id="d2318-120">However, a shadow copy that was created on Windows Server 2008 can be used on a computer that is running Windows Server 2008 R2, and vice versa.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="d2318-121">En esta sección</span><span class="sxs-lookup"><span data-stu-id="d2318-121">In this section</span></span>



| <span data-ttu-id="d2318-122">Tema</span><span class="sxs-lookup"><span data-stu-id="d2318-122">Topic</span></span>                                                          | <span data-ttu-id="d2318-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="d2318-123">Description</span></span>                                                                                                                         |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d2318-124">Información general</span><span class="sxs-lookup"><span data-stu-id="d2318-124">Overview</span></span>](volume-shadow-copy-service-overview.md)<br/> | <span data-ttu-id="d2318-125">Describe el modelo de objetos de VSS, las estrategias de copia de seguridad y restauración, y cómo crear proveedores, solicitantes y escritores de VSS.</span><span class="sxs-lookup"><span data-stu-id="d2318-125">Describes the VSS object model, backup and restore strategies, and how to create VSS providers, requesters, and writers.</span></span><br/> |
| [<span data-ttu-id="d2318-126">Referencia</span><span class="sxs-lookup"><span data-stu-id="d2318-126">Reference</span></span>](volume-shadow-copy-reference.md)<br/>       | <span data-ttu-id="d2318-127">Describe clases, tipos de datos, enumeraciones, funciones, interfaces y estructuras de VSS.</span><span class="sxs-lookup"><span data-stu-id="d2318-127">Describes VSS classes, data types, enumerations, functions, interfaces, and structures.</span></span><br/>                                  |



 

## <a name="additional-resources"></a><span data-ttu-id="d2318-128">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="d2318-128">Additional resources</span></span>



|   <span data-ttu-id="d2318-129">Recurso</span><span class="sxs-lookup"><span data-stu-id="d2318-129">Resource</span></span>                                 |   <span data-ttu-id="d2318-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="d2318-130">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2318-131">Windows Vista y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="d2318-131">Windows Vista and later</span></span>            | <span data-ttu-id="d2318-132">VSS está disponible en microsoft Kit de desarrollo de software de Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="d2318-132">VSS is available in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d2318-133">Puede instalar el SDK para Windows 7 y Windows Server 2008 R2 desde el Centro [de descarga de Windows.](https://www.microsoft.com/download/details.aspx?id=8279)</span><span class="sxs-lookup"><span data-stu-id="d2318-133">You can install the SDK for Windows 7 and Windows Server 2008 R2 from the [Windows Download Center](https://www.microsoft.com/download/details.aspx?id=8279).</span></span> <span data-ttu-id="d2318-134">También puede descargar la [versión ISO](https://www.microsoft.com/download/details.aspx?id=8442) del SDK desde el Centro de descarga de Windows.</span><span class="sxs-lookup"><span data-stu-id="d2318-134">You can also download the [ISO version](https://www.microsoft.com/download/details.aspx?id=8442) of the SDK from the Windows Download Center.</span></span> <span data-ttu-id="d2318-135">Las versiones anteriores del SDK se pueden descargar desde la [Windows SDK descargar](https://msdn.microsoft.com/windows/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d2318-135">Previous versions of the SDK can be downloaded from the [Windows SDK Download Page](https://msdn.microsoft.com/windows/bb980924.aspx).</span></span> |
| <span data-ttu-id="d2318-136">Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="d2318-136">Windows Server 2003 and Windows XP</span></span> | <span data-ttu-id="d2318-137">VSS está disponible en el SDK Servicio de instantáneas de volumen 7.2, que puede descargar desde el Centro [de descarga de Windows.](https://www.microsoft.com/download/details.aspx?id=23490)</span><span class="sxs-lookup"><span data-stu-id="d2318-137">VSS is available in the Volume Shadow Copy Service 7.2 SDK, which you can download from the [Windows Download Center](https://www.microsoft.com/download/details.aspx?id=23490).</span></span> <span data-ttu-id="d2318-138">Tenga en cuenta que los archivos vssapi.lib de 64 bits de los directorios del directorio Obj de Win2003 se pueden usar para las versiones de 64 bits de \\ Windows Server 2003 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d2318-138">Note that the 64-bit vssapi.lib files in the directories under the Win2003\\Obj directory can be used for the 64-bit versions of Windows Server 2003 and Windows XP.</span></span>                                                                                                                                                                 |



 

 

 
