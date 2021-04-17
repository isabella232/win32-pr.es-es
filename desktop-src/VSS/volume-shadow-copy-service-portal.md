---
description: Realice una copia de seguridad de los volúmenes mientras las aplicaciones de un sistema siguen escribiendo en los volúmenes. Minimice el tiempo de inactividad de la aplicación mediante la creación rápida de una instantánea (instantánea) de un volumen que duplique todos los datos. Realice una copia de seguridad multivolumen.
ms.assetid: 1eca1e3e-fc86-44b5-b3c4-bcee41bc5a43
title: Servicio de instantáneas de volumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 438ef32f1cbbc5fc82878486d9ad35b549f4535a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696476"
---
# <a name="volume-shadow-copy-service"></a><span data-ttu-id="e80bf-105">Servicio de instantáneas de volumen</span><span class="sxs-lookup"><span data-stu-id="e80bf-105">Volume Shadow Copy Service</span></span>

## <a name="purpose"></a><span data-ttu-id="e80bf-106">Propósito</span><span class="sxs-lookup"><span data-stu-id="e80bf-106">Purpose</span></span>

<span data-ttu-id="e80bf-107">El Servicio de instantáneas de volumen (VSS) es un conjunto de interfaces COM que implementa un marco para permitir la realización de copias de seguridad de volumen mientras las aplicaciones de un sistema siguen escribiendo en los volúmenes.</span><span class="sxs-lookup"><span data-stu-id="e80bf-107">The Volume Shadow Copy Service (VSS) is a set of COM interfaces that implements a framework to allow volume backups to be performed while applications on a system continue to write to the volumes.</span></span>

<span data-ttu-id="e80bf-108">Para obtener una introducción a VSS para los administradores del sistema, consulte [servicio de instantáneas de volumen](/windows-server/storage/file-server/volume-shadow-copy-service) en la biblioteca de TechNet.</span><span class="sxs-lookup"><span data-stu-id="e80bf-108">For an introduction to VSS for system administrators, see [Volume Shadow Copy Service](/windows-server/storage/file-server/volume-shadow-copy-service) in the TechNet Library.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="e80bf-109">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="e80bf-109">Run-time requirements</span></span>

<span data-ttu-id="e80bf-110">VSS es compatible con Microsoft Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="e80bf-110">VSS is supported on Microsoft Windows XP and later.</span></span> <span data-ttu-id="e80bf-111">Para obtener información sobre los requisitos de tiempo de ejecución para un elemento de programación determinado, consulte la sección de requisitos de la documentación de ese elemento.</span><span class="sxs-lookup"><span data-stu-id="e80bf-111">For information about run-time requirements for a particular programming element, see the Requirements section of the documentation for that element.</span></span>

<span data-ttu-id="e80bf-112">Todas las aplicaciones VSS de 32 bits (solicitantes, proveedores y escritores) deben ejecutarse como aplicaciones nativas de 32 bits o de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="e80bf-112">All 32-bit VSS applications (requesters, providers, and writers) must run as native 32-bit or 64-bit applications.</span></span> <span data-ttu-id="e80bf-113">No se admite su ejecución en WOW64.</span><span class="sxs-lookup"><span data-stu-id="e80bf-113">Running them under WOW64 is not supported.</span></span> <span data-ttu-id="e80bf-114">Para obtener más información, vea [configuraciones y restricciones admitidas](usage-conventions.md).</span><span class="sxs-lookup"><span data-stu-id="e80bf-114">For more information, see [Supported Configurations and Restrictions](usage-conventions.md).</span></span>

<span data-ttu-id="e80bf-115">**Windows Server 2003 y Windows XP:** Se admite la ejecución de solicitantes de VSS de 32 bits bajo WOW64, pero no para copias de seguridad de estado del sistema.</span><span class="sxs-lookup"><span data-stu-id="e80bf-115">**Windows Server 2003 and Windows XP:** Running 32-bit VSS requesters under WOW64 is supported, but not for system-state backups.</span></span> <span data-ttu-id="e80bf-116">No se admite la ejecución de proveedores y escritores de VSS de 32 bits en WOW64.</span><span class="sxs-lookup"><span data-stu-id="e80bf-116">Running 32-bit VSS providers and writers under WOW64 is not supported.</span></span> <span data-ttu-id="e80bf-117">Se quitó la compatibilidad con la ejecución de solicitantes de 32 bits en WOW64 en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="e80bf-117">Support for running 32-bit requesters under WOW64 was removed in Windows Vista and subsequent versions.</span></span>

> [!Note]  
> <span data-ttu-id="e80bf-118">Una instantánea creada en Windows Server 2003 R2 o Windows Server 2003 no se puede usar en un equipo que ejecute Windows Server 2008 R2 o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="e80bf-118">A shadow copy that was created on Windows Server 2003 R2 or Windows Server 2003 cannot be used on a computer that is running Windows Server 2008 R2 or Windows Server 2008.</span></span> <span data-ttu-id="e80bf-119">Una instantánea creada en Windows Server 2008 R2 o Windows Server 2008 no se puede usar en un equipo que ejecute Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e80bf-119">A shadow copy that was created on Windows Server 2008 R2 or Windows Server 2008 cannot be used on a computer that is running Windows Server 2003.</span></span> <span data-ttu-id="e80bf-120">Sin embargo, una instantánea creada en Windows Server 2008 puede usarse en un equipo que ejecute Windows Server 2008 R2 y viceversa.</span><span class="sxs-lookup"><span data-stu-id="e80bf-120">However, a shadow copy that was created on Windows Server 2008 can be used on a computer that is running Windows Server 2008 R2, and vice versa.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="e80bf-121">En esta sección</span><span class="sxs-lookup"><span data-stu-id="e80bf-121">In this section</span></span>



| <span data-ttu-id="e80bf-122">Tema</span><span class="sxs-lookup"><span data-stu-id="e80bf-122">Topic</span></span>                                                          | <span data-ttu-id="e80bf-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="e80bf-123">Description</span></span>                                                                                                                         |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e80bf-124">Información general</span><span class="sxs-lookup"><span data-stu-id="e80bf-124">Overview</span></span>](volume-shadow-copy-service-overview.md)<br/> | <span data-ttu-id="e80bf-125">Describe el modelo de objetos de VSS, las estrategias de copia de seguridad y restauración, y cómo crear proveedores, solicitantes y escritores de VSS.</span><span class="sxs-lookup"><span data-stu-id="e80bf-125">Describes the VSS object model, backup and restore strategies, and how to create VSS providers, requesters, and writers.</span></span><br/> |
| [<span data-ttu-id="e80bf-126">Referencia</span><span class="sxs-lookup"><span data-stu-id="e80bf-126">Reference</span></span>](volume-shadow-copy-reference.md)<br/>       | <span data-ttu-id="e80bf-127">Describe las clases, los tipos de datos, las enumeraciones, las funciones, las interfaces y las estructuras de VSS.</span><span class="sxs-lookup"><span data-stu-id="e80bf-127">Describes VSS classes, data types, enumerations, functions, interfaces, and structures.</span></span><br/>                                  |



 

## <a name="additional-resources"></a><span data-ttu-id="e80bf-128">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="e80bf-128">Additional resources</span></span>



|                                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e80bf-129">Windows Vista y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="e80bf-129">Windows Vista and later</span></span>            | <span data-ttu-id="e80bf-130">VSS está disponible en el kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e80bf-130">VSS is available in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e80bf-131">Puede instalar el SDK para Windows 7 y Windows Server 2008 R2 desde el [centro de descarga de Windows](https://www.microsoft.com/download/details.aspx?id=8279).</span><span class="sxs-lookup"><span data-stu-id="e80bf-131">You can install the SDK for Windows 7 and Windows Server 2008 R2 from the [Windows Download Center](https://www.microsoft.com/download/details.aspx?id=8279).</span></span> <span data-ttu-id="e80bf-132">También puede descargar la [versión ISO](https://www.microsoft.com/download/details.aspx?id=8442) del SDK desde el centro de descarga de Windows.</span><span class="sxs-lookup"><span data-stu-id="e80bf-132">You can also download the [ISO version](https://www.microsoft.com/download/details.aspx?id=8442) of the SDK from the Windows Download Center.</span></span> <span data-ttu-id="e80bf-133">Las versiones anteriores del SDK se pueden descargar desde la [Página de descarga de Windows SDK](https://msdn.microsoft.com/windows/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e80bf-133">Previous versions of the SDK can be downloaded from the [Windows SDK Download Page](https://msdn.microsoft.com/windows/bb980924.aspx).</span></span> |
| <span data-ttu-id="e80bf-134">Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="e80bf-134">Windows Server 2003 and Windows XP</span></span> | <span data-ttu-id="e80bf-135">VSS está disponible en el SDK de Servicio de instantáneas de volumen 7,2, que se puede descargar desde el [centro de descarga de Windows](https://www.microsoft.com/download/details.aspx?id=23490).</span><span class="sxs-lookup"><span data-stu-id="e80bf-135">VSS is available in the Volume Shadow Copy Service 7.2 SDK, which you can download from the [Windows Download Center](https://www.microsoft.com/download/details.aspx?id=23490).</span></span> <span data-ttu-id="e80bf-136">Tenga en cuenta que los archivos vssapi. lib de 64 bits en los directorios del \\ directorio obj de Win2003 se pueden usar para las versiones de 64 bits de Windows Server 2003 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e80bf-136">Note that the 64-bit vssapi.lib files in the directories under the Win2003\\Obj directory can be used for the 64-bit versions of Windows Server 2003 and Windows XP.</span></span>                                                                                                                                                                 |



 

 

 
